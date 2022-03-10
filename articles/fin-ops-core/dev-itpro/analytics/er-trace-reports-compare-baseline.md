---
title: Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis
description: Šioje temoje paaiškinama, kaip galima palyginti sugeneruotų elektroninių ataskaitų (ER) rezultatus su bazinės ataskaitos vertėmis.
author: NickSelin
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 9fabdef96b02747c84a76bf42997633842f185e9
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605210"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis

[!include[banner](../includes/banner.md)]

Galite sekti elektroninių ataskaitų formatų, kuriais generuojami siunčiami elektroniniai dokumentai, rezultatus. Kai įjungtas sekimo generavimas (naudojant ER vartotojo parametrą **Vykdyti derinimo režimu**), naujas sekimo įrašas ER formato vykdymo žurnale sugeneruojamas kiekvieną kartą, kai paleidžiama ER ataskaita. Ši išsami informacija saugoma kiekviename sugeneruojamame sekime:

- Visi įspėjimai, sugeneruoti naudojant tikrinimo taisykles
- Visos klaidos, sugeneruotos naudojant tikrinimo taisykles
- Visi sugeneruoti failai, saugomi kaip sekimo įrašo priedai

Galite išsaugoti bet kurio ER formato individualius bazinius programos failus. Failai laikomi baziniais failais, kai jie aprašo numatytus vykdomų ataskaitų rezultatus. Jei yra ER formato bazinis failas, paleistas įjungus sekimo generavimą, sekimo informacija saugo kartu su išsamia informacija, kuri buvo paminėta anksčiau, sugeneruoto elektroninio dokumento palyginimo su baziniu failu rezultatą. Vienu spustelėjimu galite gauti ir sugeneruotą elektroninį dokumentą, ir jo bazinį failą viename suglaudintame faile. Tada galite atlikti išsamų palyginimą naudodami išorinį įrankį, pvz., „WinDiff“.

Galite įvertinti sekimą, analizuodami, ar sugeneruojami elektroniniai dokumentai apima numatytą turinį. Šį įvertinimą galite atlikti vartotojo priėmimo bandymų (UAT) aplinkoje, kai pakeistas pagrindinis kodas (pvz., kai perkėlėte į naują programos egzempliorių, įdiegėte karštųjų pataisų paketus arba įdiegėte kodų pakeitimus). Taip galite užtikrinti, kad vertinimas neturės įtakos naudojamų ER ataskaitų vykdymui. Daugelio ER ataskaitų vertinimą galima atlikti režimu be priežiūros.

Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlius **ER ataskaitų generavimas ir rezultatų palyginimas (1 dalis)** ir **ER ataskaitų generavimas ir rezultatų palyginimas (2 dalis)**, kurie yra verslo proceso **7.5.4.3 Tikrinti IT paslaugas ir sprendimus (10679)** dalis, juos galima atsisiųsti iš [„Microsoft“ atsisiuntimo centro](https://go.microsoft.com/fwlink/?linkid=874684). Šie užduočių vedliai parodys jums ER sistemos konfigūravimo procesą, norint naudoti bazinius failus sugeneruotiems elektroniniams dokumentams įvertinti.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Pavyzdys. Sekimo sugeneruotų ataskaitų rezultatai ir jų palyginimas su bazinėmis vertėmis

Šia procedūra paaiškinama, kaip konfigūruoti ER sistemą, kad būtų renkama informacija apie ER formato naudojimą, o tada įvertinami šio naudojimo rezultatai. Atliekant šį vertinimą sugeneruoti dokumentai palyginami su jų pradiniais failais. Šiame pavyzdyje kursite reikiamas pavyzdinės įmonės „Litware, Inc.“ ER konfigūracijas. Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant bet kurį duomenų rinkinį.

Norėdami atlikti veiksmus šiame pavyzdyje, pirmiausia turite atlikti veiksmus [Konfigūracijų teikėjų kūrimas ir pažymėjimas kaip aktyvių](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Puslapio **Lokalizavimo konfigūracijos** dalyje **Konfigūravimo teikėjai** įsitikinkite, kad yra sąraše yra pavyzdinės įmonės „Litware, Inc.“ konfigūracijos teikėjas ir kad ji pažymėta kaip **Aktyvus**. Jei nematote šio konfigūracijų teikėjo, atlikite veiksmus [Konfigūracijų teikėjų kūrimas ir pažymėjimas kaip aktyvių](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Dokumentų valdymo parametrų konfigūravimas

1. Eikite į **Organizacijos administravimas** \> **Dokumentų valdymas** \> **Dokumentų tipai** ir sukurkite naują dokumento tipą, kur bus saugomi pradiniai failai.
2. Lauke **Klasė** įveskite **Pridėti failą**.
3. Lauke **Grupė** įveskite **Failas**.

![Puslapis Dokumentų tipai.](media/GER-BaselineSample-SetupDocumentType.PNG "Dokumentų tipų puslapio ekrano kopija")

> [!NOTE]
> Naujas dokumento tipas, turintis tokį patį pavadinimą, turi būti sukonfigūruotas kiekvienam duomenų rinkiniui, kuriame planuojate naudoti ER bazinę funkciją.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>Konfigūruoti ER parametrus, kad būtų pradėta naudoti bazinė funkcija

1. Darbo srities **Elektroninės ataskaitos** dalyje **Susiję saitai** pasirinkite **Elektroninių ataskaitų parametrai**.

    ![Elektroninių ataskaitų darbo sritis.](media/GER-BaselineSample-ERWorkspace.PNG "Elektroninių ataskaitų (ER) darbo srities ekrano kopija")

2. Skirtuko **Priedai** lauke **Pradinė informacija** įveskite arba pasirinkite ką tik sukurto dokumento tipą.

    ![Elektroninių ataskaitų parametrų puslapio priedų skirtukas.](media/GER-BaselineSample-ERParameters.PNG "Elektroninių ataskaitų (ER) parametrų ekrano kopija")

3. Pasirinkite **Įrašyti** ir uždarykite puslapį **Elektroninių ataskaitų parametrai**.

### <a name="add-a-new-er-model-configuration"></a>Įtraukti naują ER modelio konfigūraciją

1. Darbo srities **Elektroninės ataskaitos** dalyje **Konfigūracijos** pasirinkite plytelę **Ataskaitų konfigūracijos**.
2. Veiksmų srityje pasirinkite **Kurti konfigūraciją**.
3. Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite **Modelis, kuris turi mokytis ER pagrindinę informaciją**.
4. Pasirinkite **Kurti konfigūraciją**, kad būtų galima patvirtinti naujo ER duomenų modelio įrašo kūrimą.

![Kurti konfigūracijos dialogo langą, pridėti naują ER modelio konfigūraciją.](media/GER-BaselineSample-ModelAdd.PNG "Konfigūracijos išplečiamojo dialogo lauko kūrimo ekrano kopija")

### <a name="design-a-data-model"></a>Duomenų modelio kūrimas

1. Puslapio **Konfigūracijos** veiksmų srityje pasirinkite **Dizaino įrankis**.
2. Pasirinkite **Naujas**.
3. Išplečiamojo dialogo lango lauke **Pavadinimas** įveskite **Šakninis**.
4. Pasirinkite **Įtraukti**.
5. Pasirinkite **Šakninė rekomendacija**.
6. Pasirinkite **Gerai**, tada pasirinkite **Įrašyti**.
7. Uždarykite puslapį **Modelio dizaino įrankis**.
8. Pasirinkti **Keisti būseną**.
9. Pasirinkite **Užbaigti**, tada pasirinkite **Gerai**.

![Puslapis Konfigūracijos.](media/GER-BaselineSample-ModelComplete.PNG "Konfigūracijų puslapio ekrano kopija")

### <a name="add-a-new-er-format-configuration"></a>Įtraukite naują ER formato konfigūraciją

1. Puslapio **Konfigūracijos** veiksmų srityje pasirinkite **Kurti konfigūraciją**.
2. Išplečiamojo dialogo lango laukų grupėje **Naujas** pasirinkite parinktį **Formatas pagal duomenų modelį „Modelis, kuris turi mokytis ER pagrindinę informaciją“**.
3. Lauke **Pavadinimas** įveskite **Formatas, kuris turi mokytis ER pagrindinę informaciją**.
4. Pasirinkite **Kurti konfigūraciją**, kad būtų galima patvirtinti naujo ER formato įrašo kūrimą.

![Kurti konfigūracijos dialogo langą, pridėti naują ER formato konfigūraciją.](media/GER-BaselineSample-FormatAdd.PNG "Konfigūracijos išplečiamojo dialogo lauko kūrimo ekrano kopija")

### <a name="design-a-format"></a>Formato kūrimas

Pagal šį pavyzdį sukursite paprastą ER formatą XML dokumentams generuoti.

1. Puslapio **Konfigūracijos** veiksmų srityje pasirinkite **Dizaino įrankis**.
2. Pasirinkite **Įtraukti šaknį**.
3. Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.

    1. Medyje pasirinkite **Bendra\\Failas**.
    2. Lauke **Pavadinimas** įveskite **Išvestis**.
    3. Pasirinkite **Gerai**.

4. Pasirinkite **Įtraukti**.
5. Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.

    1. Medyje pasirinkite **XML\\Elementas**.
    2. Lauke **Pavadinimas** įveskite **Dokumentas**.
    3. Pasirinkite **Gerai**.

6. Medyje pasirinkite **Išvestis\\Dokumentas**.
7. Pasirinkite **Įtraukti**.
8. Išplečiamajame dialogo lange atlikite toliau nurodytus veiksmus.

    1. Medyje pasirinkite **XML\\Atributas**.
    2. Lauke **Pavadinimas** įveskite **ID**.
    3. Pasirinkite **Gerai**.

    ![Formato dizaino puslapis, XML atributas, pasirinktas medyje.](media/GER-BaselineSample-FormatLayoutDesign.PNG "Formato kūrimo įrankio puslapio ekrano kopija")

9. Skirtuke **Susiejimas** pasirinkite **Naikinti**.
10. Pasirinkite **Įtraukti šaknį**.
11. Išplečiamojo dialogo lango medyje pasirinkite **Bendra\\Vartotojo įvesties parametras** ir atlikite šiuos veiksmus.

    1. Lauke **Pavadinimas** įveskite **ID**.
    2. Lauke **Žyma** įveskite **ID**.
    3. Pasirinkite **Gerai**.

12. Medyje pasirinkite **Išvestis\\Dokumentas\\ID**.
13. Pasirinkite **Susieti**, tada pasirinkite **Įrašyti**.

![Formato dizainerio puslapis, skirtukas Žemėlapis.](media/GER-BaselineSample-FormatMappingDesign.PNG "Formato kūrimo įrankio puslapio ekrano kopija")

Remiantis sukurta struktūra, sukonfigūruotas formatas sugeneruos XML failą. Šiame XML yra **Šakninis** elementas, turintis **ID** atributą, kuris nustatytas kaip reikšmė, kurią vartotojas įveda ER vykdymo dialogo lange.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Naujo pagrindinio failo generavimas pagal sukurtą ER formatą

1. Puslapio **Konfigūracijos** „FastTab“ **Versijos** pasirinkite **Vykdyti**.
2. Lauke **Įveskite ID** įveskite **1**.
3. Pasirinkite **Gerai**.

    ![Elektroninių ataskaitų parametrų dialogo langas.](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Elektroninių ataskaitų (ER) parametrų dialogo lango ekrano kopija")

4. Įrašykite sugeneruoto **out.Admin.xml** failo vietinę kopiją, kad vėliau galėtumėte jį naudoti kaip pradinį šio ER formato failą.

    ![Pranešimas apie konfigūracijų puslapyje sugeneruotą failą.](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Pranešimo apie konfigūracijų puslapyje sugeneruotą failą ekrano kopija")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>Konfigūruoti ER parametrus, kad būtų naudojama bazinė funkcija

1. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos** pasirinkite **Vartotojo parametrai**.
2. Nustatykite parinktį **Vykdyti derinimo režimu** kaip **Taip**.
3. Pasirinkite **Gerai**.

![Vartotojo parametrų dialogo langas.](media/GER-BaselineSample-ERUserParameters.PNG "Vartotojo parametrų dialogo lango ekrano kopija")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Naujos pagrindinės informacijos įtraukimas pagal sukurtą ER formatą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Veiksmų srityje pasirinkite **Pagrindinė informacija**.

    ![Bazinis mygtukas konfigūracijų puslapyje.](media/GER-BaselineSample-OpenBaselinePage.PNG "Bazinio mygtuko konfigūracijų puslapyje ekrano kopija")

3. Veiksmų srityje pasirinkite **Naujas**.
4. Pasirinkite **Formatas, kuris turi mokytis ER pagrindinę informaciją** anksčiau sukurtą ER formatą.
5. Pasirinkite **Įrašyti**.

![Elektroninės ataskaitos formato bazinis puslapis.](media/GER-BaselineSample-AddBaseline.PNG "Elektroninės ataskaitos (ER) formato bazinio puslapio ekrano kopija")

Pagridinė informacija įtraukiama į formatą **Formatas, kuris turi mokytis ER pagrindinę informaciją**.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Konfigūruoti įtrauktos pagrindinės informacijos pagrindinę taisyklę

1. Puslapio **Elektroninių ataskaitų formato pagrindinė informacija** veiksmų srityje pasirinkite mygtuką **Priedai** (sąvaržėlės simbolis).
2. Veiksmų srityje pasirinkite **Naujas** \> **Failas**. ER parametruose dokumento tipas **Failas** anksčiau turi būti pasirinktas kaip dokumento tipas, naudojamas pradiniams failams saugoti.
3. Pasirinkite **Naršyti** ir pasirinkite **out.Admin.xml** failą, kuris buvo sugeneruotas, kai anksčiau vykdėte sukonfigūruotą ER formatą.

    ![Priedų puslapis.](media/GER-BaselineSample-UploadBaselineFile.PNG "Priedų puslapio ekrano kopija")

4. Uždarykite puslapį **Priedai**.
5. „FastTab“ **Pagrindinė informacija** pasirinkite **Naujas**.
6. Lauke **Pavadinimas** įveskite **1 pagrindinė informacija**.
7. Lauke **Failo komponento pavadinimas** įveskite arba pasirinkite **Išvestis**. Ši vertė nurodo, kad konfigūruota pagrindinė informacija bus lyginama su failu, kuris generuojamas naudojant **Išvestis** formato elementą.
8. Lauke **Failo vardo šablonas** įveskite **\*.xml**.

    > [!NOTE]
    > Galite nurodyti failo vardo šabloną. Nustačius failo vardo šabloną, pagrindinės informacijos įrašas bus naudojamas įvertinant sugeneruotą išvestį tik tada, kai sugeneruoto išvesties failo vardas atitinka tą šabloną.

9. Jei sukonfigūruota pagrindinė informacija turi būti naudojama tik tada, kai **Formatas, kuris turi mokytis ER pagrindinę informaciją** ER formatą vykdo vartotojai, kurie prisijungę prie konkrečių įmonių, pasirinkite tas įmones lauke **Įmonės**.
10. Lauke **Pagrindinė informacija** įveskite arba pasirinkite priedą **out.Admin**.
11. Pasirinkite **Įrašyti**.

![Elektroninės ataskaitos formato bazinis puslapis, Bazinis FastTab bazinės eilutės pasirinktos.](media/GER-BaselineSample-SetupBaselineLine.PNG "Elektroninės ataskaitos (ER) formato bazinio puslapio ekrano kopija")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Vykdyti sukurtą ER formatą ir peržiūrėti žurnalą, kad būtų išanalizuoti rezultatai

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Medyje išplėskite **Modelis, kuris turi mokytis ER pagrindinę informaciją** ir pasirinkite **Modelis, kuris turi mokytis ER pagrindinę informaciją\\Formatas, kuris turi mokytis ER pagrindinę informaciją**.
3. „FastTab“ **Versijos** pasirinkite **Vykdyti**.
4. Lauke **Įveskite ID** įveskite **1**.
5. Pasirinkite **Gerai**.
6. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos derinimo žurnalai**.

    ![Elektroninės ataskaitos paleidimo žurnalų puslapis su vienodais baziniais parametrais.](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Elektroninių ataskaitų (ER) vykdymo žurnalų ekrano kopija")

    > [!NOTE]
    > Vykdymo žurnale yra informacijos apie sugeneruoto failo palyginimo su sukonfigūruota pagrindine informacija rezultatus. Šiame pavyzdyje žurnalas nurodo, kad sugeneruotas failas ir pagrindinė informacija yra vienodi.

7. Pasirinkite **Naikinti viską**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Vykdyti sukurtą ER formatą ir peržiūrėti žurnalą, kad būtų išanalizuoti rezultatai

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Medyje išplėskite **Modelis, kuris turi mokytis ER pagrindinę informaciją** ir pasirinkite **Modelis, kuris turi mokytis ER pagrindinę informaciją\\Formatas, kuris turi mokytis ER pagrindinę informaciją**.
3. „FastTab“ **Versijos** pasirinkite **Vykdyti**.
4. Lauke **Įveskite ID** įveskite **2**.
5. Pasirinkite **Gerai**.
6. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos derinimo žurnalai**.

    ![Elektroninės ataskaitos paleidimo žurnalų puslapis su skirtingais baziniais parametrais.](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Elektroninių ataskaitų (ER) vykdymo žurnalų ekrano kopija")

    > [!NOTE]
    > Vykdymo žurnale yra informacijos apie sugeneruoto failo palyginimo su sukonfigūruota pagrindine informacija rezultatus. Šiame pavyzdyje žurnalas nurodo, kad sugeneruotas failas ir pagrindinė informacija skiriasi.

7. Pasirinkite **Įmonė**.

> [!NOTE]
> Sugeneruotas failas ir pradinis failas yra siūlomi kaip suarchyvuotas failas. Galite naudoti išorinius palyginimo įrankius, pvz., WinDiff, norėdami palyginti failus ir peržiūrėti skirtumus.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
