---
title: Bendrojo planavimo efektyvumo patobulinimas
description: Šioje temoje paaiškinamos įvairios parinktys, kurios gali padėti pagerinti bendrojo planavimo ar trikčių šalinimo efektyvumą.
author: ChristianRytt
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: fcbc732fce4120268acd774cc4d42193ba95787d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570926"
---
# <a name="improve-master-planning-performance"></a>Bendrojo planavimo efektyvumo patobulinimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinamos įvairios parinktys, kurios gali padėti pagerinti bendrojo planavimo ar trikčių šalinimo efektyvumą. Joje pateikta informacijos apie parametrus bei rekomenduojamas konfigūracijas ir veiksmus. Joje taip pat yra visų svarbių parametrų, kuriuos reikia apsvarstyti, kai susiduriate su ilgai trunkančiomis bendrojo planavimo užduotimis, suvestinė.

Ši tema skirta sistemos administratoriams arba IT vartotojams, turintiems galimybę spręsti problemas. Ji taip pat skirta gamybos ar tiekimo planuotojams, nes joje pateikta informacijos apie parametrus, susijusius su verslo planavimo poreikiais. 

## <a name="parameters-related-to-master-planning-performance"></a>Parametrai, susiję su bendrojo planavimo našumu

Įvairūs parametrai įtakoja bendrojo planavimo vykdymo laiką ir į juos reikia atsižvelgti.

### <a name="number-of-threads"></a>Gijų skaičius

Parametru **Gijų skaičius** galite koreguoti bendrojo planavimo procesą, kad pagerintumėte konkretaus duomenų rinkinio našumą. Šis parametras nurodo bendrą gijų skaičių, kuris bus naudojamas vykdant bendrąjį planavimą. Jis sukelia bendrojo planavimo vykdymo lygiagretumą, o tai padeda sutrumpinti vykdymo laiką. 

Parametrą **Gijų skaičius** galite nustatyti dialogo lange **Bendrojo planavimo vykdymas**. Norėdami atidaryti šį dialogo langą, pasirinkite **Bendrasis planavimas \> Bendrasis planavimas \> Vykdyti \> Bendrasis planavimas** arba pasirinkite **Vykdyti** darbo srityje **Bendrasis planavimas**. Norėdami nustatyti tinkamiausią šio parametro reikšmę, turite pasikliauti bandymų ir klaidų procesu. Tačiau, norėdami apskaičiuoti pradinę vertę, galite naudoti toliau nurodytas formules.

- **Jei jūsų sektorius gamina:** (gijų skaičius) = (suplanuotų užsakymų skaičius ÷ 1000)
- **Kitu atveju:** (gijų skaičius) = (prekių skaičius ÷ 1000)

Pagelbiklių, naudojamų bendrojo planavimo metu, skaičius turi būti mažesnis arba lygus didžiausiam gijų, leidžiamų paketinio apdorojimo serveryje, skaičiui. Jeigu pagelbiklių skaičius viršija paketinio apdorojimo serverio gijų skaičių, papildomos gijos neveiks.

> [!NOTE]
> Nustatant parametrą **Gijų skaičius** kaip **0** (nulį) pailgėja bendrojo planavimo vykdymo laikas. Todėl rekomenduojame visuomet nustatyti reikšmę, kuri yra daugiau nei 0.

### <a name="number-of-tasks-in-helper-task-bundle"></a>Pagelbiklio užduočių grupėje esančių užduočių skaičius

Keisdami parametrą **Užduočių grupėje esančių užduočių skaičius** (t. y. grupės dydį) galėtumėte sumažinti vykdymo laiką. Šis parametras valdo elementų, kuriuos bendrai planuoja vienas pagelbiklis, skaičių.

Parametrą **Užduočių grupėje esančių užduočių skaičius** galite nustatyti skiltyje **Efektyvumas**, kuri pateikta puslapio **Bendrojo planavimo parametrai** skirtuke **Bendra** (**Bendrasis planavimas \> Sąranka \>Bendrojo planavimo parametrai**). Tinkamiausia šio parametro reikšmė priklauso nuo jūsų duomenų. Todėl rekomenduojame pradėti nuo reikšmės **1**, o tada bandymų ir klaidų metodu nustatyti reikšmę, tinkamiausią jūsų sąrankai.

Paprastai rekomenduojame padidinti užduočių skaičių, kai prekių skaičius yra labai didelis (šimtai tūkstančių). Kitu atveju turite sumažinti užduočių skaičių. Jei dirbate vienoje iš tolesnių sektorių, atsižvelkite į nurodytas rekomendacijas.

- Mažmeninės prekybos ir platinimo sektoriuose, kuriuose yra daug nepriklausomų prekių, naudokite daug pagelbiklių, nes tarp prekių priklausomybių nėra. 
- Gamybos sektoriuje, kuriame yra daug komplektavimo specifikacijų (KS) ir bendrų subkomponentų, naudokite mažiau pagelbiklių, nes dėl priklausomybių tarp prekių laukimo laikas gali pailgėti.

> [!TIP]
> Jei kyla našumo problemų, rekomenduojame sumažinti parametrą **Užduočių grupėje esančių pagelbiklių skaičius** į **1**. Tada galite atlikti bandomų ir klaidų procesą, kad rastumėte reikšmę, tinkamiausią jūsų sąrankai. Paprastai efektyvumo problemos kyla, kai viena prekė apdorojama ilgiau nei likusios prekės. Šiuo atveju matysite, kad dviejų paskesnių užduočių, kurių būsena bendrojo planavimo metu yra **Padengimas**, vykdomo laikai pastebimai skirsis. Kraštutiniais atvejais šis skirtumas gali būti 30 minučių. Nustatyti, kiek laiko užduotys bus vykdomos, galite patikrinę kiekvienos užduoties trukmę.

### <a name="use-of-cache"></a>Sparčiosios atminties naudojimas

Parametras **Sparčiosios atminties naudojimas** suteikia galimybę koreguoti bendrojo planavimo procesą, kad jis galėtų geriau atlikti konkretų duomenų rinkinį. Pavyzdžiui, galite jį koreguoti, kad pasiektumėte toliau nurodytus rezultatus.

- Jei naudojama daugiau sparčiosios atminties, daugiau atminties surenkama į duomenų atmintį. Tikimasi, kad duomenys bus naudojami dar kartą vėliau. Jei duomenys yra atmintyje, galite įrašyti kai kurias duomenų bazės užklausas. Tačiau, jei naudojama daugiau sparčiosios atminties, atminties poreikiai padidėja.
- Jei naudojama mažiau sparčiosios atminties, gali reikėti tuos pačius duomenis surinkti iš duomenų bazės dažniau. Be to, programos objektų serveris (AOS) išsaugo truputį duomenų atmintyje viso proceso metu.

Sunku nuspėti, kuri parinktis bus tinkamesnė, nes kiekvienas atvejis priklauso ne tik nuo duomenų, bet ir nuo aparatūros. Pavyzdžiui, kadangi naudojant mažiau sparčiosios atminties duomenų bazės serveryje susidaro papildoma apkrova, turbūt nėra naudinga naudoti šią parinktį, jei jūsų duomenų bazės serveris jau yra perkrautas.

Parametrą **Sparčiosios atminties naudojimas** galite nustatyti skiltyje **Efektyvumas**, kuri pateikta puslapio **Bendrojo planavimo parametrai** skirtuke **Bendra** (**Bendrasis planavimas \> Sąranka \>Bendrojo planavimo parametrai**). Sparčiosios atminties naudojimo efektyvumas stipriai priklauso nuo kliento duomenų. Pvz., jei talpyklinių duomenų nereikia niekada, jūs tiesiog eikvosite atmintį, jei saugosite duomenis iki planavimo proceso pabaigos. Tokiu atveju, jei sukonfigūruosite naudoti mažiau sparčiosios atminties, efektyvumas gali padidėti, nes AOS reikalauja mažiau atminties ir serverio ištekliai yra atlaisvinami kitoms užduotims atlikti.

> [!TIP]
> Paprastai rekomenduojame nustatyti talpyklos parametrą **Sparčiosios atminties naudojimas** į parinktį **Maksimalus**, nes parametras yra našumo didinimo funkcija. Rekomenduojame nustatyti parametrą **Minimalus**, jei naudojate vietinę versiją ir turite ribotą atmintį (apytiksliai 2 gigabaitus \[GB\]).

### <a name="number-of-orders-in-firming-bundle"></a>Užsakymų tvirtinamame pakete skaičius

Parametras **Tvirtinimo grupėje esančių užsakymų skaičius** nurodo bendrą užsakymų, kuriuos apdoros kiekviena gija / paketinis vykdymas, skaičių. Jis sukelia automatinio tvirtinimo lygiavimo procesą.

Parametrą **Tvirtinimo grupėje esančių užsakymų skaičius** galite nustatyti skiltyje **Efektyvumas**, kuri pateikta puslapio **Bendrojo planavimo parametrai** skirtuke **Bendra** (**Bendrasis planavimas \> Sąranka \>Bendrojo planavimo parametrai**). Automatinio tvirtinimo proceso lygiagretumas yra pagrįstas užsakymais, kuriuos reikia apdoroti kartu. Pavyzdžiui, jei šis parametras nustatytas į **50**, kiekviena gija arba paketinė užduotis vienu metu paims ir kartu apdoros 50 užsakymų. Norint rasti tinkamiausią reikšmę, rekomenduojame naudoti bandymų ir klaidų metodą. Tačiau, norėdami apskaičiuoti pradinę vertę, galite naudoti toliau nurodytą formulę.

(Grupėje esančių užsakymų skaičius) = (poreikio prekių skaičius ÷ gijų skaičius)

> [!NOTE]
> Jei parametrą **Užsakymų tvirtinamame pakete skaičius** nustatote į **0** (nulis), automatinio tvirtinimo lygiagretumas neįvyks. Visas procesas bus vykdomas vienoje paketinėje užduotyje ir turės kaupiamąjį vykdymo laiką. Todėl padidės bendrojo planavimo vykdymo laikas. Dėl šios priežasties rekomenduojame nustatyti šį parametrą į reikšmę, kuri yra didesnė nei **0** (nulis).

### <a name="time-fences"></a>Laiko ribos

Laiko ribos nurodo, kaip tolimoje ateityje skaičiavimai ir kiti poreikiai turi būti skaičiuojami bendrojo planavimo metu. Kuo ilgesnė laiko riba, tuo ilgiau bus vykdomas bendrasis planavimas. Todėl nustatykite laiko ribą pagal savo verslo poreikius. Daugiau informacijos apie laiko ribas žr. [Bendrojo planavimo sąranka](master-planning-setup.md).

### <a name="actions"></a>Veiksmai

Tarp laiko ribų taip pat galite rasti parametrą **Veiksmo pranešimas**. Dėl veiksmų pranešimų skaičiavimo bendrasis planavimas gali užtrukti ilgiau. Jei veiksmų pranešimai nėra reguliariai analizuojami ir taikomi (kasdien, kas savaitę ir t. t.), bendrojo planavimo vykdymo metu išjunkite skaičiavimą. Norėdami išjungti skaičiavimą, puslapyje **Bendrieji planai** (**Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**) nustatykite parinkties **Veiksmų pranešimas** vykdomo bendrojo plano laiko ribą į **0** (nulį). Taip pat įsitikinkite, kad parametras **Veiksmo pranešimas** yra išjungtas visose padengimo grupėse.

### <a name="futures"></a>Ateities datos

Dėl ateities datų skaičiavimo bendrasis planavimas gali užtrukti ilgiau. Jei neplanuojate KS arba jei atidėjimų nereikia perduoti iš pasiūlos į poreikį planavimo metu, išjunkite ateities datų skaičiavimą bendrojo planavimo metu. Norėdami išjungti skaičiavimą, nustatykite vykdomo bendrojo plano parinkties **Ateities datos** laiko ribą į **0** (nulis). Taip pat įsitikinkite, kad parametras **Ateities datos** yra išjungtas visose padengimo grupėse.

## <a name="one-heavy-routine-at-a-time"></a>Vienu metu – viena sudėtinga procedūra

Planuodami bendrąjį planavimą, neplanuoti jokios kitos paketinės užduoties tuo pačiu metu. Būkite itin atsargūs ir tuo pačiu metu neplanuojate jokių kitų sudėtingų procedūrų, pvz., atsargų uždarymo.

## <a name="review-the-session-log"></a>Seanso žurnalo peržiūra

Sistema gali surinkti papildomos informacijos apie užduotis, kurios vykdomos atliekant bendrąjį planavimą. Jei norite, kad sistema rinktų šią informaciją, įjunkite dialogo lango **Bendrojo planavimo vykdymas** parametrą **Sekti apdorojimo laiką**. Surinkta informacija gali padėti rasti silpnąsias vykdymo sritis. Pavyzdžiui, kai parametras **Pagelbiklio užduočių grupėje esančių užduočių skaičius** nustatytas į **1**, galite identifikuoti prekę, kurios vykdymo laikas yra ilgiausias. Taip pat galite palyginti įvairių gijų, kurių būsena yra **Padengimas**, vykdymo laiką ir palyginti kiekvienos užduoties trukmę.

Norėdami peržiūrėti savo sistemos bendrojo planavimo vykdymus, atlikite vieną iš toliau nurodytų veiksmų.

- Darbo srityje **Bendrasis planavimas**, išplečiamajame lauke pasirinkite bendrąjį planą, tada plytelėje **Bendrasis planavimas** pasirinkite **Retrospektyva**. Pasirinkite užduotį „FastTab“ **Užklausos**, tada pasirinkite **Apdoroti užduoties trukmę**.
- Puslapyje **Bendrieji planai**, kairiojoje srityje pasirinkite planą, tada „FastTab“ pasirinkite **Retrospektyva**. Pasirinkite užduotį „FastTab“ **Užklausos**, tada pasirinkite **Apdoroti užduoties trukmę**.

Kai peržiūrite seanso žurnalą, atsižvelkite į tai:

- **Atnaujinimas** neturėtų trukti ilgą laiką (paprastai jis turi trukti iki 30 minučių) tačiau negalima tuomet vykdyti kitų veiksmų.
- **Kopijavimo planas** neturėtų trukti ilgai (jis turi trukti apie vieną minutę).
- **Automatinis tvirtinimas** paprastai trunka apie 30 minučių. Tačiau tai gali trukti iki kelių valandų, atsižvelgiant į užsakymų skaičių ir prekių sudėtingumą.
- **Automatinis tvirtinimas** turi trukti trumpiau nei **Padengimas**.
- **Padengimas** turi trukti ilgiausiai, lyginant su likusiais procesais.
- **Veiksmas** ir **Būsimas pranešimas** gali trukti ilgai, atsižvelgiant į duomenis ir KS skaičių.

## <a name="filtering-of-items"></a>Prekių filtravimas

Filtrai, kurie taikomi dialogo lange **Bendrojo planavimo vykdymas**, paveikia bendrojo planavimo vykdymo trukmę. Pasirinkite **Bendrasis planavimas \> Bendrasis planavimas \> Vykdyti \> Bendrasis planavimas** arba pasirinkite **Vykdyti** darbo srityje **Bendrasis planavimas**. Norėdami pašalinti prekes iš vykdymo, rekomenduojame filtruoti pagal prekės gyvavimo ciklo būseną (ne pagal prekių numerius). Kai filtruojate pagal gyvavimo ciklo būseną, atnaujinimo procesas truks trumpiau, nei filtruojant pagal prekių numerius.

## <a name="automatically-filter-by-items-with-direct-demand"></a>Automatiškai filtruoti pagal tiesioginio poreikio prekes

Norėdami patobulinti bendrojo planavimo vykdymo laiką, galite pasirinkti įtraukti tik tuos elementus, kurių poreikis yra tiesioginis. Šis filtras gali būti naudojamas tik tam, kad būtų vykdomas visiškas bendrasis planavimas, kai lauke **Įtrauktini įrašai** netaikomi jokie kiti filtrai. Su filtrais vykdomas bendrasis planavimas nepaisys parametro **Automatiškai filtruoti pagal prekes, turinčias tiesioginį poreikį**.

Laukas **Automatiškai filtruoti pagal prekes, turinčias tiesioginį poreikį** randamas puslapyje **Bendrojo planavimo parametrai** ir gali būti naudojamas su išankstinio apdorojimo ir tolesnio apdorojimo parametrais.

### <a name="pre-processing"></a>Išankstinis apdorojimas
Parametru **Išankstinis apdorojimas: automatiškai filtruoti pagal prekes, turinčias tiesioginį poreikį** užtikrinama, kad bendrojo planavimo išankstinio apdorojimo etapas apimtų tik prekes, kurios tenkina bent vieną iš šių sąlygų:
  - Prekės numatomas gavimas arba išdavimas, pvz., pirkimo užsakymas, pardavimo užsakymas, pasiūlymas, perkėlimo užsakymas arba gamybos užsakymas. 
  - Prekė turi prekės padengimą bei pakankamų atsargų (bent turimas atsargas).
  - Prognozuoti šios prekės poreikį po šios dienos.
  - Prognozuoti šios prekės tiekimą po šios dienos.
  - Prekė apima bet kokias tęstinumo eilutes iš skambučių centro modulio, kuris dar turi būti sukurtas.

> [!NOTE]
> Prekei, kurios turimos atsargos yra fiziškai pasiekiamos, poreikio operacija nebus rodoma, nes prekės poreikio nėra.

### <a name="post-processing"></a>Tolesnis apdorojimas
Parinktis **Tolesnis apdorojimas: automatiškai filtruoti pagal prekes, turinčias tiesioginį poreikį** yra aktuali tik tada, jei nustatote **KS versijos reikalavimą** savo padengimo grupėse. Kitu atveju parametro įjungti nereikia. 

Prieš pradedant padengimo veiksmą, yra išankstinio padengimo veiksmas, kurio metu su padengimo parametru **KS versijos reikalavimas** įgalintos prekės bus vėl apdorojamos. Tai atliekama siekiant užtikrinti, kad prekės iš reikiamos KS versijos būtų suplanuotos. Prekės, kurios, manoma, turi poreikį išankstinio apdorojimo metu, nebėra paklausios ir todėl turėtų būti neįtrauktos vykdant planavimą.

## <a name="performance-checklist-summary"></a>Efektyvumo kontrolinio sąrašo suvestinė

- **Gijų skaičius** – nustatykite į reikšmę, kuri yra didesnė nei **0** (nulis).
- **Pagelbiklio užduočių grupėje esančių užduočių skaičius** – nustatykite reikšmę, kuri yra didesnė nei **0** (nulis). (Naudokite anksčiau šioje temoje pateiktas formules.)
- **Sparčiosios atminties naudojimas** – nustatykite reikšmę **Maksimalus**, nebent jūsų sistemoje yra mažai atminties.
- **Užsakymų tvirtinamame pakete skaičius** – nustatykite reikšmę, kuri yra didesnė nei **0** (nulis). (Naudokite anksčiau šioje temoje pateiktą formulę.)
- **Laiko ribos** – pakoreguokite pagal savo verslo poreikius.
- **Veiksmai ir ateities datos** – išjunkite veiksmus ir ateities datas, jei jų nenaudojate.
- **Vienu metu – viena sudėtinga procedūra** – nevykdykite bendrojo planavimo kartu su kitomis sudėtingomis procedūromis.
- **Seanso žurnalo peržiūra.**
- **Prekių filtravimas** – naudokite gyvavimo ciklo būseną, kad neįtrauktumėte prekių į bendrąjį planavimą. (Nenaudokite prekių numerių.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]