---
title: Medžiagų tvarkymo įrangos sąsaja (MHAX)
description: Šiame straipsnyje aprašoma, kaip nustatyti medžiagų tvarkymo įrangos sąsają (MHAX), kad galėtumėte prisijungti prie išorinių faktinių medžiagų tvarkymo (MH) sistemų.
author: Mirzaab
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMHEParameters, WMHESubscription, WMHEQueueManagerWorkspace, WMHEInboundQueue, WMHEOutboundQueue
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c4b0d991d320d5a679d0ed60880c56a6cb849e2d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907093"
---
# <a name="material-handling-equipment-interface-mhax"></a>Medžiagų tvarkymo įrangos sąsaja (MHAX)

[!include [banner](../../includes/banner.md)]

*Medžiagų tvarkymo įrangos sąsają* (MHAX) galite naudoti išorinių faktinių medžiagų tvarkymo (MH) sistemoms prijungti prie sandėlio, kuris valdomas pagal išplėstinį sandėlio valdymą (WMS) programoje „Microsoft Dynamics 365 Supply Chain Management”. WMS ir MH sistemų sąsają sudaro dvi eilės: viena skirta siuntimo įvykiams (iš WMS į MH), kita – gavimo įvykiams (iš MH į WMS). WMS sistema sugeneruoja siuntimo įvykius pagal darbo eilutes, sukurtas įvairių darbo kūrimo ir vykdymo procesų metu. Tada MH sistema reguliariai apklausia WMS sistemą dėl naujų įvykių ir apdoroja atsakymus. Po to, kai MH sistema baigia tvarkyti įvykius pagal darbo instrukcijas, ji išsiunčia gavimo įvykius, pavyzdžiui, darbo eilutės baigimą ir nevisišką paėmimą.

Toliau pateiktoje iliustracijoje parodomi įvairūs elementai ir tvarka, pagal kurią vykdomi procesai naudojant MHAX integravimą.

![MHAX komponentai ir sąveikos.](media/mhax-components.png "MHAX komponentai ir sąveikos")

Toliau pateikiamas sąveikų, kurios parodytos ankstesnėje iliustracijoje, paaiškinimas.

1. Kuriant ar vykdant darbą, siuntimo įvykiai sukuriami siunčiamų pranešimų eilėje.
2. MH įranga jungiasi prie MH įrangos paslaugos, apklausia dėl naujų su ja susijusių įvykių ir apdoroja tuos įvykius.
3. Kai MH įranga parengta ataskaitai grąžinti, ji vėl prisijungia prie paslaugos ir pateikia gavimo įvykius. Šiuos įvykius iš karto apdorojo eilės procesorius.
4. Atsižvelgdamas į gavimo įvykio duomenis, eilės procesorius gali paleisti esamą darbą, modifikuoti jį arba sukurti naują darbą.

## <a name="turn-on-the-mhax-feature"></a>MHAX funkcijos įjungimas

Prieš pradedami naudoti MHAX funkciją, turite įjungti ir jos funkciją, ir jos konfigūracijos raktą.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.
2. Darbo srityje **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** įjunkite funkciją, pavadintą *Medžiagų tvarkymo įrangos sąsaja*.
3. Įdėkite savo sistemą į priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
4. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
5. Išplėskite **Prekyba \> Sandėlio ir gabenimo valdymas**, tada pažymėkite žymės langelį **Medžiagų tvarkymo įrangos sąsaja**.
6. Išjunkite priežiūros režimą kaip aprašyta [Priežiūros režime](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

## <a name="set-mhax-parameters"></a>MHAX parametrų nustatymas

Norėdami sukonfigūruoti funkciją, turite nustatyti keletą bendrųjų parametrų puslapyje **Medžiagų tvarkymo įrangos sąsajos parametrai**.

1. Eikite į **Medžiagų tvarkymo įrangos sąsaja \> Sąranka \> Medžiagų tvarkymo įrangos sąsajos parametrai**.
2. Skirtuke **Bendra** nustatykite toliau pateiktus laukus.

    - **Vartotojo ID** – pasirinkite darbuotoją. Šis darbuotojas bus naudojamas visoms darbo operacijoms (paėmimams ir padėjimams), apdorojamoms gaunamų pranešimų eilėje, vykdyti.
    - **Įgalinti gaunamo pranešimo ID** – kai ši parinktis nustatyta į *Taip*, jei gaunamo pranešimo ID dubliuojasi, pranešimas bus atmestas, o klaidos pranešimas nurodys, kad pranešimas jau egzistuoja. Kai ši parinktis nustatyta į *Ne*, bus leidžiami gaunamų pranešimų ID dublikatai.

3. Skirtuke **Numeracijos** pasirinkite visos sistemos numeracijas, kurias reikia naudoti generuojant unikalius gaunamų ir siunčiamų pranešimų eilių elementų bei darbo eilučių porų ID.

## <a name="outbound-events"></a>Siuntimo įvykiai

Tam tikru darbo kūrimo ar vykdymo metu sistema nustato, ar ji turi sugeneruoti siuntimo įvykius, kurie bus išsiunčiami į MH sistemą. Jei abonementas sukonfigūruojamas tam tikram apdorojimo sandėlyje etapui, sistema sugeneruoja įvykį pagal abonemento nustatymą.

### <a name="structure-of-outbound-events"></a>Siuntimo įvykių struktūra

Kiekvienas siuntimo įvykis unikaliai identifikuojamas pagal siunčiamų pranešimų eilės ID. Siuntimo operacijos tipas nustato įvykio tipą. Sandėlis ir įvykį sugeneravusio abonemento ID taip pat įrašomi įvykyje.

Norint perkelti duomenis į MH sistemą, siuntimo įvykyje yra 10 duomenims skirtų laukų (nuo **data01** iki **data10**). Šie duomenų laukai susiejami su esamais duomenų bazės laukais ryšiu vienas su vienu (1:1). Tiksliau sakant, jos gaunamos iš darbo eilutės ir darbo antraštės lentelių laukų. Laukus galima pasirinkti laisvai. Juos nustatote kurdami abonementą.

Be 10 duomenų laukų, kuriuose yra 1:1 susiejimas su esamais duomenų bazės laukais, įvykyje gali būti papildomas duomenų laukas, kuris žinomas kaip *mokamoji krova*. Šio lauko turinį generuoja pasirinktinis X++ kodas, vadinamas *mokamosios krovos generatoriumi*. Bet kuris naudoti skirtas mokamosios krovos generatorius nustatomas abonemente.

Norint užtikrinti, kad MH sistema kiekvieną siunčiamų pranešimų eilės ID gaus tik vieną kartą, būsenos laukas naudojamas nurodyti, ar įvykis parengtas siųsti į išorinę sistemą, ar jis jau išsiųstas.

### <a name="outbound-queue-subscriptions"></a>Siunčiamų pranešimų eilės abonementai

Prieš generuojant bet kokius įvykius, reikia nustatyti abonementą, kad MHAX funkcijai būtų galima nurodyti, ar ir kaip generuoti įvykius. Sugeneruoti įvykiai pažymimi abonemento identifikatoriumi. Todėl kelios MH sistemos gali prisijungti prie tos pačios WMS sistemos, tačiau jų įvykiai išlieka atskiri. Kai MHAX paslauga apklausiama dėl naujų įvykių, abonementas yra viena iš galimų parinkčių įvykiams nuskaityti.

Norėdami sukurti abonementą, eikite į **Medžiagų tvarkymo įrangos sąsaja \> Sąranka \> Abonementai**. Galimi toliau pateikti kiekvieno abonemento parametrai.

- **Abonemento ID** – unikalus pavadinimas, kuris identifikuoja abonementą.
- **Aprašymas** – laisvos formos tekstinis abonemento aprašymas.
- **Sandėlis** – konkretūs sandėliai, pagal kuriuos reikia filtruoti įvykius.
- **Siuntimo operacijos tipas** – įvykių, kurie turėtų būti abonemente, tipas.
- **Mokamosios krovos generatorius** – pasirinktinis kodo plėtinys, kuris gali įvesti papildomos informacijos siuntimo įvykio lauke **Mokamoji krova**.

Su kiekvienu abonementu galima susieti užklausą. Šioje užklausoje filtruojamos darbo eilutės ir antraštės, siekiant dar labiau apriboti darbą, kuris naudos abonementą įvykiams generuoti. Norėdami įtraukti užklausą į abonementą, pasirinkite atitinkamo abonemento žymės langelį **Vykdyti užklausą** puslapyje **Abonementai**, tada veiksmų srityje pasirinkite **Redaguoti užklausą**. Atidaroma standartinė „Supply Chain Management” užklausos rengyklė.

Be to, abonemente yra *abonemento susiejimas*, pagal poreikį susiejantis darbo antraštės arba darbo eilutės laukus su kai kuriais arba visais 10 laisvų siuntimo įvykio duomenų laukų. Norint grąžinti informaciją į MHAX paslaugą, paprastai reikia įtraukti darbo eilutės įrašo ID arba *darbo eilučių poros ID*. (Darbo eilučių poros ID yra nauja ypatybė, leidžianti sistemai naudoti vieną grąžinimo komandą paėmimo ir padėjimo eilutėms apdoroti.) Likę laukai priklauso nuo naudojimo atvejo. Kai kurie pavyzdžiai pateikiami vėliau šiame straipsnyje.

Norėdami nustatyti abonemento susiejimą, pasirinkite reikiamą abonementą puslapyje **Abonementai**, tada veiksmų srityje pasirinkite **Abonemento susiejimas**. Atsiradusiame dialogo lange **Abonemento susiejimas** galite kiekvienam galimam duomenų laukui priskirti lentelę ir lauką, jei reikia.

### <a name="outbound-event-types"></a>Siuntimo įvykių tipai

Šiame skyriuje aprašomi įvairūs galimi įvykių tipai. (Įvykių tipai taip pat vadinami *operacijų tipais*.) Taip pat paaiškinama, kada WMS sistemoje sukuriamas kiekvieno tipo įvykis.

#### <a name="work-creation-events"></a>Darbo kūrimo įvykiai

Darbo kūrimo įvykiai sukuriami programai sugeneravus darbą. Tai taikoma daugumai darbo kūrimo procesų tipų, dažniausiai paėmimo ir papildymo darbo kūrimui. Apskritai, jei darbas sukurtas esant būsenai *Atidaryta*, kuri nurodo, kad darbuotojas darbą jau gali paleisti, bus sugeneruotas darbo kūrimo įvykis. Be to, bus generuojami pagrindinio perkėlimo darbo (ne perkėlimo pagal šabloną darbo) kūrimo įvykiai, net jei darbas nesukurtas kaip atidarytas darbas.

Įsidėmėtina šio elgesio išimtis yra ciklų skaičiavimo darbai, kurie šiuo metu nepalaikomi. Inventorizacijos MH sistemoje nepatenka į MHAX aprėptį, o inventorizacijos rezultatai turi būti importuoti į atsargų skaičiavimo žurnalą.

Po darbo sukūrimo MHAX paslauga apdoroja sugeneruotas darbo eilutes ir priskiria darbo eilučių poros ID visoms kiekvienos darbo antraštės sugeneruotoms darbo eilutėms. Tikslas yra sugrupuoti visas paėmimo darbo eilutes su paskesniais padėjimais į vieną darbo eilučių poros ID. (Grupės atitinka paėmimo / padėjimo poras darbo šablonuose.) Tokiu būdu, galima naudoti vieną ID visų susijusių paėmimo ir padėjimo eilučių darbo baigimo ataskaitoje. Grupavimo procesas prasideda nuo pirmos eilutės, tada tęsiamas su tuo pačiu ID, kol susiduria su paskesne padėjimo / paėmimo darbo eilučių pora. Vykdomas ID priskiriamas tos poros padėjimo eilutei. Tada poros paėmimo eilutėje naudojamas naujas ID. Šis procesas tęsiasi, kol apdorojamos visos eilutės, priklausančios darbo antraštei.

Speciali darbo kūrimo įvykių funkcija: jei darbo antraštėje parinktis **Užblokuota banga** nustatyta į *Taip*, sugeneruotų įvykių būsena bus *Užblokuota*, o ne įprasta būsena *Parengta*, naudojama jiems siųsti į MH sistemą. Darbo antraštėje esanti vėliavėlė **Užblokuota banga** nurodo, kad darbo antraštė dar neparuošta darbuotojams paleisti (galbūt dėl nebaigto papildymo darbo). Išvalius vėliavėlę **Užblokuota banga**, jau sugeneruoti įvykiai atblokuojami ir MH sistema gali juos nuskaityti iš eilės.

#### <a name="work-initiation-events"></a>Darbo inicijavimo įvykiai

Darbo inicijavimo įvykiai suaktyvinami, kai darbo atnaujinimo metu darbo būsena pasikeičia iš *Atidaryta* į *Apdorojama*.

#### <a name="work-completion-events"></a>Darbo užbaigimo įvykiai

Darbo užbaigimo įvykiai suaktyvinami, kai darbo atnaujinimo metu darbo būsena pasikeičia iš *Apdorojama* į *Uždaryta*.

#### <a name="work-cancellation-events"></a>Darbo atšaukimo įvykiai

Darbo atšaukimo įvykiai suaktyvinami, kai darbo atnaujinimo metu darbo būsena pasikeičia iš bet kokios būsenos, išskyrus *Atšaukta* į *Atšaukta*. Be to, visi kiti įvykiai, susiję su darbo antrašte, panaikinami iš visų abonementų eilės. Tokiu būdu išorinės sistemos apsaugomos nuo įvykių, kurių nereikia, apdorojimo.

#### <a name="pickput-completion-events"></a>Paėmimo / padėjimo užbaigimo įvykiai

Paėmimo / padėjimo užbaigimo įvykiai suaktyvinami, kai darbo eilutės atnaujinimo metu paėmimo / padėjimo eilutės būsena pasikeičia iš *Apdorojama* į *Uždaryta*.

### <a name="monitor-the-outbound-queue"></a>Siunčiamų pranešimų eilės stebėjimas

Norėdami peržiūrėti siunčiamų pranešimų eilę, eikite į **Medžiagų tvarkymo įrangos sąsaja \> Bendra \> Siunčiamų pranešimų eilė**. Puslapyje **Siunčiamų pranešimų eilė** išvardyti visi siunčiamų pranešimų eilės elementai ir jų būsenos. Pasirinkite eilės elementą, norėdami peržiūrėti jo informaciją. Šioje informacijoje yra prekės operacijos tipas, naudotas abonementas, kiekvieno duomenų lauko (nuo **data01** iki **data10**) ir mokamosios krovos vertės.

### <a name="clean-up-the-outbound-queue"></a>Siunčiamų pranešimų eilės valymas

Ilgainiui jūsų siunčiamų pranešimų eilėje bus daug jau išsiųstų prekių. Norėdami pašalinti šias prekes, eikite į **Medžiagų tvarkymo įrangos sąsaja \> Periodinės užduotys \> Valymas \> Siunčiamų pranešimų eilės valymas.**

## <a name="inbound-events"></a>Gavimo įvykiai

Šiame skyriuje aprašomi įvairūs gavimo įvykių tipai, kuriuos MH sistema gali siųsti WMS sistemai. Taip pat paaiškinama, kaip MH sistema turi pateikti duomenis ir kaip kiekvienas gavimo įvykis veikia WMS sistemoje.

### <a name="structure-of-inbound-events"></a>Gavimo įvykių struktūra

Kai gavimo įvykis pateikiamas, išorinė sistema turi pateikti gavimo operacijos tipą kartu su iki 10 parametrų (nuo **data01** iki **data10**). Pasirinktinis tikrinimas gali užtikrinti, kad MHAX paslauga to paties gavimo įvykio negavo daugiau nei vieną kartą. Norint įgalinti šį tikrinimą, kiekvienas gavimo įvykis turi turėti unikalų pranešimo ID. Jei gauto pranešimo ID dubliuojasi ir jei puslapio **Medžiagų tvarkymo įrangos sąsajos parametrai** parinktis **Įgalinti gaunamo pranešimo ID** nustatyta į *Taip*, pranešimas bus atmestas. Klaidos pranešime bus nurodyta, kad pranešimas jau egzistuoja.

Be gaunamų duomenų laukų, sistema priskiria įvykiui unikalų gaunamų pranešimų eilės ID.

### <a name="inbound-event-types"></a>Gavimo įvykių tipai

Šiame skyriuje aprašomi palaikomi gavimo įvykių tipai (operacijų tipai) ir duomenys, kurie turi būti pateikti, kad įvykiai būtų apdoroti.

#### <a name="work-confirm-events"></a>Darbo patvirtinimo įvykiai

Darbo patvirtinimo įvykiai reikalauja, kad gaunamų duomenų laukuose būtų toliau pateikta informacija.

- **data01** – darbo eilučių poros ID.
- **data02** – darbo eilutės įrašo ID (`RecId` vertė).

    > [!NOTE]
    > Turi būti *arba* laukas **data01**, *arba* **data02**.

- **data03** – numerio lentelės, iš kurios reikia paimti, ID.
- **data04** – darbo antraštės paskirties numerio lentelės ID.

Jei pateikiamas darbo eilučių poros ID, visos paėmimo, padėjimo ar pasirinktinės darbo eilutės, kurios pažymėtos darbo eilučių poros ID ir kurių būsena yra *Atidaryta* arba *Apdorojama*, paleidžiamos nuosekliai. Jei pateikiamas darbo eilutės įrašo ID (`RecId` vertė), darbo eilutė turi būti paėmimo, padėjimo arba pasirinktinė darbo eilutė, kurios būsena yra *Atidaryta* arba *Apdorojama*.

Paėmimo eilutės iš numerio lentelėmis kontroliuojamų vietų reikalauja, kad laukas **data03** nurodytų numerio lentelę, iš kurios reikia paimti, nepaisant to, ar eilutės pažymėtos pagal darbo eilutės įrašo ID, ar darbo eilučių poros ID. Lauke **data04** turi būti nurodyta paėmimo darbo antraštės paskirties numerio lentelė.

Padėjimo eilutėse negali būti papildomos informacijos. Jos paleidžiamos tik pagal dabartinę darbo eilutės vietą ir darbo paskirties numerio lentelę. Jei padėti reikia kitoje vietoje, pakeiskite darbo eilutės vietą, [kaip](#override-events) toliau šiame straipsnyje nurodyta skyriuje Nepaisyti įvykių.

Pasirinktinės darbo eilutės nereikalauja ir nepalaiko jokios papildomos gavimo įvykio informacijos.

#### <a name="short-pick-events"></a>Nevisiško paėmimo įvykiai

Nevisiško paėmimo įvykiai reikalauja, kad gaunamų duomenų laukuose būtų toliau pateikta informacija.

- **data02** – darbo įrašo ID (`RecId` vertė).
- **data03** – numerio lentelės, iš kurios reikia paimti, ID.
- **data04** – paimamas kiekis.
- **data05** – nevisiško paėmimo išimties kodas.
- **data06** – darbo antraštės paskirties numerio lentelės ID.

> [!NOTE]
> Laukas **data01** nėra taikomas nevisiško paėmimo įvykiams.

Šis įvykis panašus į darbo patvirtinimo įvykį, bet jis taikomas tik paėmimo eilutėms.

#### <a name="override-events"></a><a id="override-events"></a>Įvykių keitimas

Keitimo įvykiai reikalauja, kad gaunamų duomenų laukuose būtų toliau pateikta informacija.

- **data01** – darbo įrašo ID (`RecId` vertė).
- **data02** – naujos vietos ID.

Darbo eilutės būsena turi būti arba *Atidaryta*, arba *Apdorojama*, ir turi būti pateikta nauja vieta.

#### <a name="license-plate-receipt-events"></a>Numerio lentelės gavimo įvykiai

Numerio lentelės gavimo įvykiai reikalauja, kad gaunamų duomenų laukuose būtų toliau pateikta informacija.

- **data01** – gaunamos numerio lentelės ID.

Sistema atlieka numerio lentelės gavimo operaciją pagal numerio lentelę, kuri įrašyta kaip vertė lauke **data01**.

### <a name="monitor-the-inbound-queue"></a>Gaunamų pranešimų eilės stebėjimas

Norėdami peržiūrėti gaunamų pranešimų eilę, eikite į **Medžiagų tvarkymo įrangos sąsaja \> Bendra \> Gaunamų pranešimų eilė**. Puslapyje **Gaunamų pranešimų eilė** išvardyti visi gaunamų pranešimų eilės elementai ir jų būsenos. Pasirinkite eilės elementą, norėdami peržiūrėti jo informaciją. Šioje informacijoje yra prekės operacijos tipas, pranešimo ID, kiekvieno duomenų lauko (nuo **data01** iki **data10**) vertės.

Jei apdorojant gavimo įvykius įvyko klaida arba kito tipo žurnalo elementas, galite patikrinti žurnalą veiksmų srityje pasirinkdami **Klaidų žurnalas**.

### <a name="inbound-event-processing"></a>Gavimo įvykio apdorojimas

Gavimo įvykiai pirmiausia įrašomi į duomenų bazę, o tada jie iš karto (sinchroniškai) paleidžiami. Jei apdorojimo metu įvyksta klaida, įvykis vis tiek įrašomas į eilę, tačiau būsena nustatoma į *Klaida*. MHAX paslauga pateikia klaidos pranešimą MH sistemai ir išsaugo klaidų žurnalą gavimo įvykio įraše vėlesniam tyrimui.

Įvykiai, kurių būsena yra *Klaida*, vėliau gali būti pakartotinai apdoroti, jei klaidos sąlyga išsprendžiama. Norėdami pakartotinai juos apdoroti, atlikite vieną iš toliau pateiktų veiksmų.

- Eikite į **Medžiagų tvarkymo įrangos sąsaja \> Bendra \> Gaunamų pranešimų eilė**. Pasirinkite reikiamą gaunamų pranešimų eilę, o tada veiksmų srityje pasirinkite **Pakartotinai apdoroti**.
- Eikite į **Medžiagų tvarkymo įrangos sąsaja \> Bendra \> Pakartotinai apdoroti gaunamų pranešimų eilę**. Atsiranda standartinis paketinės užduoties dialogo langas. Jame galite nustatyti įrašo filtrą ir suplanuoti arba paleisti paketinę užduotį, kad eilė būtų apdorota.

Visos darbo operacijos (paėmimo ir padėjimo) paleidžiamos naudojant darbuotoją, kuris pasirinktas puslapio **Medžiagų tvarkymo įrangos sąsajos parametrai** lauke **Vartotojo ID**.

### <a name="clean-up-the-inbound-queue"></a>Gaunamų pranešimų eilės valymas

Ilgainiui jūsų gaunamų pranešimų eilėje bus daug jau apdorotų prekių. Norėdami pašalinti šias prekes, eikite į **Medžiagų tvarkymo įrangos sąsaja \> Periodinės užduotys \> Valymas \> Gaunamų pranešimų eilės valymas.**

## <a name="get-a-quick-overview-by-using-the-queue-manager"></a>Greitai apžvelkite naudodami eilės tvarkytuvą

Norėdami greitai peržiūrėti visą veiklą, susijusią su gaunamų ir siunčiamų pranešimų eilėmis, eikite į **Medžiagų tvarkymo įrangos sąsaja \> Darbo sritys \> Eilės tvarkytuvas**. Puslapyje **Eilės tvarkytuvas** pateikiamas skirtukų ir plytelių rinkinys, kurį galite naudoti savo eilėms stebėti ir tirti. Taip pat pateikiami naudingi saitai į daugelį kitų šiame straipsnyje paminėtų puslapių.

## <a name="connect-to-the-mhax-service"></a>Prisijungimas prie MHAX paslaugos

MHAX įdiegta kaip pasirinktinė paslauga. Todėl ji pasiekiama per SOAP ir REST skambučius. Toliau pateikiami SOAP ir REST galinių punktų adresai.

- **SOAP:** `https://base_environment_URL/soap/services/WMHEServices`
- **REST:** `https://base_environment_URL/api/services/WMHEServices/WMHEService`

## <a name="retrieve-messages-from-the-outbound-queue"></a>Pranešimų nuskaitymas iš siunčiamų pranešimų eilės

Norėdami nuskaityti pranešimus iš siunčiamų pranešimų eilės, naudokite vieną iš toliau pateiktų būdų.

- Naudokite `readOutboundSubscriptionQueue`, norėdami nuskaityti įvykius pagal abonemento ID.
- Naudokite `readOutboundWarehouseQueue`, norėdami nuskaityti įvykius pagal įvykio tipą ir kelių abonementų sandėlio ID.
