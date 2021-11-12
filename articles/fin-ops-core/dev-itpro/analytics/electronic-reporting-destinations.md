---
title: Elektroninių ataskaitų (ER) paskirties vietos
description: Šioje temoje pateikiama informacija apie elektroninių ataskaitų paskirties vietų valdymą, palaikomų paskirties vietų tipus ir saugumo klausimus.
author: nselin
ms.date: 09/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: e8e176b8d4e14eee2050b3c66f7547ff878b5174
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647098"
---
# <a name="electronic-reporting-er-destinations"></a>Elektroninių ataskaitų (ER) paskirties vietos

[!include [banner](../includes/banner.md)]

Galite sukonfigūruoti kiekvienos elektroninių ataskaitų (ER) formato konfigūracijos ir jos sukurto komponento paskirties vietą (aplanką arba failą). Vartotojai, turintys reikiamas teises, paskirties vietų parametrus taip pat gali keisti apdorojimo metu. Šioje temoje paaiškinami ER paskirties vietų valdymas, palaikomi paskirties vietų tipai ir saugumo klausimai.

ER formato konfigūracijose paprastai yra bent vienas išvesties komponentas: failas. Paprastai konfigūracijose yra kelių skirtingų tipų (pvz., XML, TXT, XLSX, DOCX arba PDF) failų išvesties komponentų, sugrupuotų į vieną arba kelis aplankus. ER paskirties vietos valdymo funkcija suteikia galimybę iš anksto sukonfigūruoti, kas įvyksta vykdant kiekvieną komponentą. Pagal numatytuosius parametrus paleidus konfigūraciją rodomas dialogo langas, kuriame galima įrašyti arba atidaryti failą. Tas pats procesas taip pat vyksta importuojant ER konfigūraciją ir nesukonfigūruojant jokių konkrečių jos paskirties vietų. Sukūrus pagrindinio išvesties komponento paskirties vietą, ta paskirties vieta perrašo numatytąją ir aplankas arba failas siunčiamas pagal paskirties vietos parametrus.

## <a name="availability-and-general-prerequisites"></a>Prieinamumas ir bendrieji reikalavimai

ER paskirties vietų funkcijų negalima naudoti programoje „Microsoft Dynamics AX“ 7.0 (2016 m. vasario mėn. leidimas). Todėl turite įdiegti „Microsoft Dynamics 365 for Operations“ 1611 versiją (2016 m. lapkričio mėn. leidimą) arba naujesnę versiją, jei norite naudoti toliau pateikiamus paskirties vietų tipus.

- [El. pašto adresas](er-destination-type-email.md)
- [Archyvuoti](er-destination-type-archive.md)
- [Failas](er-destination-type-file.md)
- [Ekranas](er-destination-type-screen.md)
- [„Power BI“](er-destination-type-powerbi.md)

Arba galite įdiegti vieną iš toliau nurodytų būtinųjų komponentų. Tačiau nepamirškite, kad naudojant šias alternatyvas, ER paskirties vietų patirtis bus labiau apribota.

- „Microsoft Dynamics AX“ 7.0.1 programos versija (2016 m. gegužės mėn.)
- [Elektroninių ataskaitų paskirties vietų valdymo programos karštosios pataisos](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Taip pat yra paskirties vietos tipas [Spausdinti](er-destination-type-print.md). Norėdami jį naudoti, turite įdiegti „Microsoft Dynamics 365 Finance“ 10.0.9 versiją (2020 m. balandžio mėn. leidimą).

## <a name="overview"></a>Peržiūrėti

Paskirties vietas galite nustatyti tik į dabartinį „Finance“ egzempliorių [importuotoms](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) ER konfigūracijoms ir tik tokiems formatams, kurie pateikti puslapyje **Elektroninių ataskaitų konfigūracijos**. ER paskirties vietų valdymo funkciją galima rasti pasirinkus **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninių ataskaitų paskirties vieta**.

### <a name="default-behavior"></a>Numatytasis veikimo būdas

Numatytasis ER formato konfigūracijos veikimo būdas priklauso nuo vykdymo tipo, kurį nurodote, kai paleidžiamas ER formatas.

Jei nustatysite parinktį **Paketinis vykdymas** į **Ne**, dialogo lango **Intrastat ataskaita** „FastTab” **Vykdyti fone** ER formatas vykdomas interaktyviuoju režimu nedelsiant. Kai šis vykdymas sėkmingai baigtas, galima atsisiųsti sugeneruotą siuntimo dokumentą.

Jei nustatysite parinktį **Paketinis vykdymas** į **Taip**, ER formatas vykdomas [paketiniu](../sysadmin/batch-processing-overview.md) režimu. Sukuriama reikiama paketinė užduotis, remiantis parametrais, nurodytais dialogo lango **ER parametrai** skirtuke **Vykdyti fone**.

> [!NOTE]
> Užduoties apraše jums pranešama apie ER formato susiejimo vykdymą. Jame taip pat yra įvykdyto ER komponento pavadinimas.

[![ER formato vykdymas.](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

Informacijos apie šią užduotį galite rasti keliose vietose.

- Eikite į **Bendra** \> **Užklausos** \> **Paketinės užduotys** \> **Mano paketinės užduotys**, kad patikrintumėte suplanuotos užduoties būseną.
- Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninės ataskaitos užduotys**, kad patikrintumėte suplanuotos užduoties būseną ir baigtos užduoties vykdymo rezultatus. Kai užduoties vykdymas sėkmingai baigtas, puslapyje **Elektroninės ataskaitos užduotys** pasirinkite **Rodyti failus**, kad gautumėte sugeneruotą siuntimo dokumentą.

    > [!NOTE]
    > Šis dokumentas saugomas kaip dabartinės užduoties įrašo priedas ir jį valdo [dokumentų valdymo](../../fin-ops/organization-administration/configure-document-management.md) sistema. [Dokumento tipas](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types), naudojamas saugoti šio tipo artefaktus, yra sukonfigūruotas naudojant [ER parametrus](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- Puslapyje **Elektroninės ataskaitos užduotys** pasirinkite **Rodyti failus**, kad peržiūrėtumėte klaidų ir įspėjimų, sugeneruotų vykdant užduotį, sąrašą.

    [![ER užduočių sąrašo peržiūra.](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Vartotojo sukonfigūruotas veikimo būdas

Puslapyje **Elektroninių ataskaitų paskirties vieta** galite nepaisyti numatytojo konfigūracijos veikimo būdo. Importuotos konfigūracijos šiame puslapyje bus rodomos tik tada, kai pasirinksite **Nauja** ir tada lauke **Nuoroda** pasirinksite, kuriai konfigūracijai norite kurti paskirties vietų parametrus.

[![Konfigūracijos pasirinkimas lauke Nuoroda.](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Sukūrę nuorodą, galite sukurti kiekvieno į nurodyto ER formato išvesties komponento **Aplankas** ar **Failas** failo paskirties vietą.

[![Failo paskirties vietos kūrimas.](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Paskui dialogo lange **Paskirties vietų parametrai** galite įjungti ir išjungti atskiras failų paskirties vietas. Mygtukas **Parametrai** yra naudojamas siekiant valdyti visas pasirinktos failo paskirties vietos paskirties vietas. Dialogo lange **Paskirties vietos parametrai** galite atskirai valdyti kiekvieną paskirties vietą, nustatydami jos parinktį **Įgalinta**.

„Finance“ versijose, **senesnėse nei 10.0.9 versija**, kiekvienam to paties formato išvesties komponentui galite sukurti **vieną failų paskirties vietą**, pvz., aplanką ar failą, pasirenkamą lauke **Failo pavadinimas**. Tačiau **10.0.9 versijoje ir naujesnėse versijose** galite sukurti **keletą failų paskirties vietų** kiekvienam to paties formato išvesties komponentui.

Pavyzdžiui, galite naudoti šią funkciją norėdami konfigūruoti failo komponento, kuris naudojamas generuojant siuntimo dokumentą „Excel“ formatu, failų paskirties vietas. Vieną paskirties vietą ([Archyvuoti](er-destination-type-archive.md)) galima sukonfigūruoti, kad ER užduočių archyve būtų saugomas pradinis „Excel“ failas, o kitą paskirties vietą ([El. paštas](er-destination-type-email.md)) galima sukonfigūruoti, kad „Excel“ failas būtų vienu metu [konvertuojamas](#OutputConversionToPDF) į PDF formatą ir siunčiamas PDF formatu el. paštu.

[![Vieno formato elemento keleto paskirties vietų konfigūravimas.](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Paleidus ER formatą, visada paleidžiamos visos sukonfigūruotos formato komponentų paskirties vietos. Be to, „Finance” **10.0.17 ir naujesnėse versijose** ER paskirties vietų funkcionalumas pagerėjo ir dabar suteikia jums galimybę viename ER formate konfigūruoti skirtingus paskirties vietų rinkinius. Ši konfigūracija pažymi kiekvieną rinkinį kaip sukonfigūruotą konkrečiam vartotojo veiksmui. ER API buvo [išplėsta](er-apis-app10-0-17.md) tam, kad būtų galima pateikti veiksmą, kurį atlieka vartotojas paleisdamas ER formatą. Pateiktas veiksmo kodas perduodamas į ER paskirties vietas. Atsižvelgdami į pateiktą veiksmo kodą, galite vykdyti skirtingas ER formato paskirties vietas. Daugiau informacijos ieškokite [Nuo veiksmo priklausomų ER paskirties vietų konfigūravimas](er-action-dependent-destinations.md).

## <a name="destination-types"></a>Paskirties vietų tipai

Šios paskirties vietos šiuo metu palaikomos naudojant ER formatus. Galite išjungti arba įjungti visus tipus vienu metu. Tokiu būdu galite nieko nedaryti arba siųsti komponentą į visas sukonfigūruotas paskirties vietas.

- [El. pašto adresas](er-destination-type-email.md)
- [Archyvuoti](er-destination-type-archive.md)
- [Failas](er-destination-type-file.md)
- [Ekranas](er-destination-type-screen.md)
- [„Power BI“](er-destination-type-powerbi.md)
- [Spausdinti](er-destination-type-print.md)

## <a name="applicability"></a>Taikymas

Paskirties vietas galite nustatyti tik importuotoms ER konfigūracijoms ir tik tokiems ER konfigūracijų formatams, kurie pateikti puslapyje **Elektroninių ataskaitų konfigūracijos**.

> [!NOTE]
> Sukonfigūruotos paskirties vietos yra susietos su konkrečia įmone. Jei planuojate naudoti ER formatą skirtingose dabartinio „Finance“ egzemplioriaus įmonėse, turite sukonfigūruoti kiekvienos įmonės ER formato paskirties vietas.

Kai konfigūruojate pasirinkto formato failų paskirties vietas, konfigūruojate viso formato paskirties vietas.

[![Konfigūracijos saitas.](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Tuo pat metu gali būti kelios formato [versijos](general-electronic-reporting.md#component-versioning), kurios buvo importuotos į dabartinį „Finance“ egzempliorių. Galite jas peržiūrėti, pasirinkę saitą **Konfigūracija**, kuris siūlomas pasirinkus lauką **Nuoroda**.

[![Konfigūracijos versijos.](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Pagal numatytuosius nustatymus sukonfigūruotos paskirties vietos taikomos tik tada, kai paleidžiate ER formato versiją, kurios būsena yra **Baigta** arba **Bendrai naudojama**. Tačiau kartais reikia naudoti sukonfigūruotas paskirties vietas, kai vykdoma ER formato juodraščio versija. Pavyzdžiui, modifikuojate savo formato juodraščio versiją ir norite naudoti sukonfigūruotas paskirties vietas, norėdami patikrinti, kaip bus pristatoma sugeneruota išvestis. Atlikite toliau pateikiamus veiksmus, norėdami pritaikyti ER formato paskirties vietas, kai vykdoma juodraščio versija.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Parinktyje **Naudoti paskirties vietas, esant juodraščio būsenai** nustatykite **Taip**.

[![Parinktis Naudoti paskirties vietas, esant juodraščio būsenai.](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Norėdami naudoti ER formato juodraščio versiją, turite atitinkamai pažymėti ER formatą.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Parinktyje **Vykdymo parametras** nustatykite **Taip**.

[![Parinktis Vykdymo parametras.](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Atlikus šį nustatymą, galima naudoti modifikuojamų ER formatų parinktį **Vykdyti juodraštį**. Šioje parinktyje nustačius **Taip**, galima pradėti naudoti formato juodraščio versiją, kai formatas vykdomas.

[![Parinktis Vykdyti juodraštį.](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Paskirties vietų trikčių apdorojimas

Paprastai ER formatas vykdomas kaip konkretaus verslo proceso dalis. Tačiau siuntimo dokumento, generuojamo vykdant ER formatą, pristatymas kartais turi būti laikomas to verslo proceso dalimi. Tokiu atveju, jei nepavyksta pristatyti sugeneruoto siuntimo dokumento į sukonfigūruotą paskirties vietą, verslo proceso vykdymą reikia atšaukti. Norėdami sukonfigūruoti tinkamą ER paskirties vietą, pasirinkite parinktį **Nutraukti apdorojimą trikties atveju**.

Pavyzdžiui, konfigūruojate tiekėjo mokėjimo apdorojimą, kad ER formatas **ISO20022 kredito pervedimas** būtų vykdomas generuojant mokėjimo failą ir papildomus dokumentus (pvz., lydraštį ir kontrolės ataskaitą). Jei mokėjimas turėtų būti laikomas sėkmingai apdorotu tik lydraštį sėkmingai pristačius el. paštu, turite pažymėti žymės langelį **Nutraukti apdorojimą trikties atveju** tinkamos failo paskirties vietos komponente **CoveringLetter**, kaip parodyta tolesnėje iliustracijoje. Šiuo atveju pasirinkto apdorotino mokėjimo būsena **Nėra** bus pakeista į **Išsiųsta** tik „Finance“ egzemplioriuje sukonfigūruotam el. pašto teikėjui sėkmingai priėmus sugeneruotą lydraštį pristatymui atlikti.

[![Procesų apdorojimo konfigūravimas failo paskirties vietos trikties atveju.](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Jei išvalysite žymės langelį **Nutraukti apdorojimą trikties atveju** paskirties vietos komponente **CoveringLetter**, bus laikoma, kad mokėjimas sėkmingai apdorotas, net lydraščio nepristačius el. paštu. Mokėjimo būsena **Nėra** pasikeis į **Išsiųsta**, net jei lydraščio neįmanoma išsiųsti nes, pavyzdžiui, nėra gavėjo arba siuntėjo el. pašto adreso arba adresas yra netikslus.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Išvesties konvertavimas į PDF formatą

Galite naudoti PDF konvertavimo parinktį, norėdami konvertuoti išvestį „Microsoft Office“ („Excel“ arba „Word“) formatu į PDF formatą.

### <a name="make-pdf-conversion-available"></a>PDF konvertavimo įgalinimas

Norėdami, kad PDF konvertavimo parinktis būtų prieinama dabartiniame „Finance“ egzemplioriuje, atidarykite darbo sritį **Funkcijų valdymas** ir įjunkite funkciją **Konvertuoti elektroninių ataskaitų siuntimo dokumentus iš „Microsoft Office“ formatų į PDF**.

[![Siunčiamų dokumentų konvertavimo į PDF funkcijos įjungimas pasirinkus Funkcijų valdymas.](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Taikymas

„Finance“ versijose **ankstesnėse nei 10.0.18**, PDF keitimo parinktis gali būti įjungta tik **Excel\\Failo** komponentams, kurie yra naudojami išvesčiai generuoti „Office“ („Excel“ ar „Word“) formatu. Kai ši parinktis įjungta, išvestis, generuojama „Office“ formatu, automatiškai konvertuojama į PDF formatą. Tačiau **10.0.18 ir naujesnėse versijose** taip pat galima įjungti šią funkciją **bendrojo\\failo** tipo komponentams.

> [!NOTE]
> Atkreipkite dėmesį į įspėjimo pranešimą, kurį gausite, kai įjungsite PDF keitimo parinktį **bendrojo\\failo** tipo ER komponentui. Šis pranešimas informuoja, kad nėra būdo projektavimo metu užtikrinti, kad pasirinktas failo komponentas turinį rodys PDF formatu arba PDF konvertuojamu turiniu vykdymo metu. Todėl šią parinktį turėtumėte įjungti tik tada, kai būsite tikri, kad pasirinktas failo komponentas buvo sukonfigūruotas rodyti turinį PDF formatu arba PDF konvertuojamu turiniu vykdyklėje.
> 
> PDF konvertavimo parinktį įjungus „Excel“ failo formato komponentui, jei tas komponentas turinį rodo kitu nei PDF formatu ir jei rodomo turinio neįmanoma pakeisti į PDF formatą, vykdymo metu bus rodoma išimtis. Gaunamas pranešimas informuoja, kad sugeneruoto turinio negalima konvertuoti į PDF formatą.

### <a name="limitations"></a>Apribojimai

PDF konvertavimo parinktis galima tik debesies diegimams.

Didžiausias gaunamo PDF dokumento dydis yra 300 puslapių.

„Finance” **10.0.9 versijoje** PDF dokumente, gaunamame naudojant „Excel“ išvestį, palaikoma tik gulsčia puslapio padėtis. „Finance” **10.0.10 versijoje (2020 m. gegužės mėn) ir naujesnėse** galite [nurodyti puslapio padėtį](#SelectPdfPageOrientation) PDF dokumente, sukurtame naudojant „Excel” išvestį, kol konfigūruojate ER paskirties vietą.

Tik įprasti „Windows“ operacinės sistemos šriftai naudojami konvertuoti išvestį, kurioje nėra įdėtųjų šriftų.

### <a name="use-the-pdf-conversion-option"></a>PDF konvertavimo parinkties naudojimas

Norėdami įjungti failo paskirties vietos PDF konvertavimą, pažymėkite žymės langelį **Konvertuoti į PDF**.

[![Failo paskirties vietos PDF konvertavimo įjungimas.](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Pasirinkite PDF konvertavimui skirtą puslapio padėtį</a>

Jei sugeneruojate ER konfigūraciją „Excel” formatu ir norite konvertuoti ją į PDF formatą, galite atskirai nurodyti PDF dokumento puslapio padėtį. Kai pasirenkate žymės langelį **Konvertuoti į PDF**, kad įjungtumėte PDF konvertavimą failo paskirties vietai, kurioje gaunamas išvesties failas „Excel” formatu, laukas **Puslapio padėtis** tampa pasiekiamas „FastTab” elemente **PDF konvertavimo parametrai**. Lauke **Puslapio padėtis** pasirinkite pageidaujamą padėtį.

[![PDF konvertavimui skirtos puslapio padėties pasirinkimas.](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

Jei norite turėti parinktį pasirinkti PDF puslapio padėtį, turite įdiegti „Finance ” 10.0.10 arba naujesnę versiją. „Finance“ versijose **prieš 10.0.23 versiją** ši pasirinktis siūlo šias puslapio padėties pasirinktis:

- Vertikali
- Horizontali

Pasirinkto puslapio padėtis taikoma visiems siunčiamo dokumento puslapiams, kurios yra generuojamos „Excel” formatu ir konvertuojamos į PDF formatą.

Tačiau **10.0.23 ir vėlesnėje versijoje** puslapio padėties pasirinkčių sąrašas išplėstas taip:

- Vertikali
- Horizontali
- Skirta darbalapiui

Pasirinkus konkrečią **Darbalapio parinktį** kiekvienas sugeneruotos „Excel“ darbaknygės darbalapis konvertuojamas į PDF naudojant šio darbalapio puslapio padėtį, sukonfigūruotą naudojamame „Excel“ šablone. Taigi, gali būti, kad turite galutinį PDF dokumentą, kuriame yra stačios ir gulsčios puslapių. 

Jei ER konfigūracija „Word” formatu yra konvertuojama į PDF formatą, PDF dokumento padėtis visada gaunama iš „Word” dokumento.

## <a name="output-unfolding"></a>Išeigos išskleidimas

Kai konfigūruojate savo ER formato **Aplanko** komponento paskirties vietą, galite nurodyti, kaip to komponento išeiga bus pristatoma į sukonfigūruotą paskirties vietą.

### <a name="make-output-unfolding-available"></a>Padarykite išeigos išskleidimą prieinamu

Norėdami, kad išvesties išskleidimo parinktis būtų galima dabartiniame „Finance” egzemplioriuje, atidarykite **Funkcijų valdymo** darbo sritį ir įjunkite **Leisti konfigūruoti ER paskirties vietas, kad aplankų turinys būtų siunčiamas kaip atskiri failai** funkciją.

### <a name="applicability"></a>Taikymas

Išeigos išskleidimo parinktį galima konfigūruoti tik **Aplanko** tipo formato komponentams. Kai pradedate konfigūruoti **Aplanko** komponentą, „FastTab” **Bendra** tampa pasiekiamas **Elektroninių ataskaitų paskirties vietos** puslapyje. 

### <a name="use-the-output-unfolding-option"></a>Išeigos išskleidimo parinkties naudojimas

„FastTab” skirtuko **Bendra** lauke **Siųsti aplanką kaip** pasirinkite vieną iš šių reikšmių:

- **„ZIP” archyvas** – Pristatyti sugeneruotą failą kaip suglaudintą failą.
- **Atskiri failai** – Pristatyti kiekvieną sugeneruoto suglaudinto failo failą kaip atskirą failą.

    > [!NOTE]
    > Pasirinkus **Atskiri failai**, sugeneruota išvestis surenkama į atmintį suglaudintoje būsenoje. Todėl maksimalaus [failo dydžio apribojimas](er-compress-outbound-files.md) yra taikomas suglaudintai išeigai, kai realus failo dydis gali viršyti šią ribą. Rekomenduojame pasirinkti šią vertę, kai tikitės gana didelio sugeneruotos išeigos dydžio.

[![Paskirties vietos konfigūravimas Aplanko formato komponentui.](./media/er_destinations-set-unfolding-option.png)](./media/er_destinations-set-unfolding-option.png)

### <a name="limitations"></a>Apribojimai

Jei nustatote lauką **Siųsti aplanką kaip** į **Atskiri failai** komponentui **Aplankas**, kuriame yra kitų įdėtųjų **Aplanko** komponentų, nustatymas nėra rekursyviai taikomas įdėtiems **Aplanko** komponentams.

## <a name="security-considerations"></a>Saugos klausimai

Naudojamos dviejų tipų ER paskirties vietoms skirtos teisės ir pareigos. Vienas tipas valdo bendrą vartotojo galimybę išsaugoti sukonfigūruotas juridinio subjekto paskirties vietas (t. y. valdo prieigą prie puslapio **Elektroninių ataskaitų paskirties vietos**). Kitas tipas valdo programos vartotojo galimybę vykdymo metu perrašyti paskirties vietos parametrus, kuriuos sukonfigūravo ER kūrėjas arba ER funkcijų konsultantas.

| Vaidmuo (AOT pavadinimas)                     | Vaidmens pavadinimas                                  | Pareiga (AOT pavadinimas)                     | Pareigų pavadinimas                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Elektroninės ataskaitos kūrėjas             | ERFormatDestinationConfigure        | Konfigūruoti elektroninių ataskaitų formato paskirties vietą                |
| ERFunctionalConsultant              | Elektroninės ataskaitos funkcijų konsultantas | ERFormatDestinationConfigure        | Konfigūruoti elektroninių ataskaitų formato paskirties vietą                |
| PaymAccountsPayablePaymentsClerk    | Mokėtinų sumų mokėjimo klerkas            | ERFormatDestinationRuntimeConfigure | Konfigūruoti elektroninių ataskaitų formato paskirties vietą vykdymo aplinkoje |
| PaymAccountsReceivablePaymentsClerk | Gautinų sumų mokėjimo klerkas         | ERFormatDestinationRuntimeConfigure | Konfigūruoti elektroninių ataskaitų formato paskirties vietą vykdymo aplinkoje |

> [!NOTE]
> Anksčiau nurodytoms pareigoms taikomos dvi teisės. Šių teisių pavadinimai yra tokie patys, kaip atitinkamų pareigų pavadinimai: **ERFormatDestinationConfigure** ir **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Importavau elektronines konfigūracijas ir matau jas puslapyje Elektroninių ataskaitų konfigūracijos. Tačiau kodėl aš jų nematau puslapyje Elektroninių ataskaitų paskirties vietos?

Įsitikinkite, kad pasirinkote **Nauja**, ir tada pasirinkite konfigūraciją lauke **Nuoroda**. Puslapyje **Elektroninių ataskaitų paskirties vietos** rodomos tik tos konfigūracijos, kurių paskirties vietos sukonfigūruotos.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Ar galima nustatyti, kuri „Microsoft Azure“ saugyklos paskyra ir kuri „Azure‟ didelių dvejetainių objektų saugykla yra naudojamos?

Nr. Naudojama numatytoji „Microsoft Azure‟ didelių dvejetainių objektų saugykla, kuri nurodyta ir naudojama dokumentų valdymo sistemoje.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Kokia yra paskirties vietos parametrų parinkties Failas paskirties vieta paskirtis? Kam šis parametras skirtas?

Paskirties vieta **Failas** naudojama žiniatinklio naršyklės dialogo langui valdyti, kai vykdote ER formatą interaktyviu režimu. Įjungus šią paskirties vietą arba konfigūracijoje nenurodžius paskirties vietos, jūsų naršyklėje bus rodomas atidarymo arba įrašymo dialogo langas po išvesties failo sukūrimo.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Ar galite pateikti formulės, nurodančios tiekėjo kodą, kuriam galėčiau siųsti el. laišką, pavyzdį?

Formulė yra būdinga ER konfigūracijai. Pavyzdžiui, jei naudojate ISO 20022 kredito pervedimo konfigūraciją, galite naudoti **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** arba **model.Payments.Creditor.Identification.SourceID**, norėdami gauti susijusį tiekėjo kodą.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Vienoje iš mano formato konfigūracijų yra daug failų, sugrupuotų į vieną aplanką (pvz., 1 aplanke yra 1 failas, 2 failas ir 3 failas). Kaip nustatyti paskirties vietas, kad 1 aplankas.zip nebūtų sukurtas, 1 failas būtų siunčiamas el. paštu, 2 failas būtų siunčiamas į „SharePoint“, o 3 failą galėčiau atidaryti iš karto paleidęs konfigūraciją?

Pirma norimas formatas turi būti įgalintas ER konfigūracijose. Jei ši būtina sąlyga įvykdyta, atidarykite puslapį **Elektroninių ataskaitų paskirties vietos** ir sukurkite naują nuorodą į konfigūraciją. Kiekvienam iš keturių išvesties komponentų turi būti nurodyta po vieną failo paskirties vietą. Sukurkite pirmąją failo paskirties vietą, suteikite jai pavadinimą, pvz., **Aplankas**, ir pasirinkite failo vardą, kuris jūsų konfigūracijoje nurodo aplanką. Tada pasirinkite **Parametrai** ir įsitikinkite, kad visos paskirties vietos yra išaktyvintos. Šio failo paskirties vietos aplankas nebus sukurtas. Pagal numatytuosius parametrus dėl hierarchinės failų ir pirminių aplankų priklausomybės su visais failais bus atliekamas tas pats veiksmas. Kitaip tariant, jie niekur nebus siunčiami. Norėdami perrašyti numatytuosius parametrus, turite sukurti tris papildomas failų paskirties vietas, t. y. po vieną kiekvienam failui. Kiekvieno failo paskirties vietos parametruose turite suaktyvinti paskirties vietą, į kurią failas turėtų būti siunčiamas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Nuo veiksmo priklausomų ER paskirties vietų konfigūravimas](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
