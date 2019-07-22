---
title: Testavimo automatizavimas naudojant elektronines ataskaitas
description: Šioje temoje paaiškinta, kaip naudojant elektroninių ataskaitų (ER) sistemos pagrindinės informacijos funkciją automatizuoti „Microsoft Dynamics 365 for Finance and Operations“ funkcijų, kurias teikia ER, testavimą.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 7d21bff6e7d5e8f206a0495408b75c0760a6f80f
ms.sourcegitcommit: 48004c98b16dcd93a7b2568322e058c4b3ff02d3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726732"
---
# <a name="automate-testing-with-electronic-reporting"></a>Testavimo automatizavimas naudojant elektronines ataskaitas

[!include[banner](../includes/banner.md)]

Šioje temoje paaiškinta, kaip naudojant elektroninių ataskaitų (ER) sistemą automatizuoti kai kurių „Microsoft Dynamics 365 for Finance and Operations“ funkcijų testavimą. Šioje temoje pateiktame pavyzdyje parodyta, kaip automatizuoti tiekėjo mokėjimo apdorojimo testavimą.

„Finance and Operations“ naudoja ER sistemą, kad sugeneruotų mokėjimo failus ir atitinkamus dokumentus atliekant tiekėjo mokėjimo apdorojimą. ER sistemą sudaro duomenų modelis, modelio susiejimai ir formato komponentai, kurie leidžia apdoroti skirtingų tipų mokėjimus ir sugeneruoti dokumentus skirtingais formatais. Šiuos komponentus galima atsisiųsti iš „Microsoft Dynamics Lifecycle Services“ (LCS) ir importuoti į „Finance and Operations“ egzempliorių.

Taip pat galite tinkinti kiekvieną „Microsoft“ komponentą ir naudoti jį kaip savo pasirinktinio komponento pagrindą. Kurdami pasirinktinę versiją, galite atlikti keitimus, kurie atitinka specifinius reikalavimus. Pavyzdžiui, galite pakoreguoti ER dokumentų modelį ir ER modelio susiejimą, kad būtų galima pasiekti konkretaus kliento programos duomenis, arba galite pakeisti ER formatą, kad būtų galima modifikuoti sugeneruoto dokumento maketą.

Galite naudoti tinkintus ER formatus savo „Finance and Operations“ egzemplioriuje, kad apdorotumėte mokėjimo failus, kuriuos generuoja tiekėjo mokėjimai, ir taip pat apdorotumėte kontrolės ataskaitas. Palaikomas ER komponentų versijos kūrimas. Todėl „Microsoft“ gali pateikti atnaujintas ER sprendimų, skirtų tiekėjo mokėjimams apdoroti, versijas ir jūs galite automatiškai sujungti atnaujintą versiją su savo tinkintu komponentu atlikdami pritaikymą kitoje vietoje. Tačiau reikia atlikti naujoje vietoje pritaikytos versijos testavimą ir įsitikinti, kad ji veikia taip, kaip tikitės.

ER duomenų modeliai ir ER modelio susiejimai yra bendri daugeliui ER formatų, kurie naudojami siekiant apdoroti įvairių tipų mokėjimus ir generuoti konkrečios šalies / regiono mokėjimo dokumentus. Todėl labai pageidautina automatizuoti vartotojo priėmimo ir integravimo testavimą, kad tai būtų automatiškai atliekama keliose „Finance and Operations“ įmonėse, bet būtų atsižvelgiama į kiekvienos tikslinės įmonės šalies / regiono kontekstą, būtų naudojami skirtingi duomenų rinkiniai ir pan.

Daugiau informacijos, kaip sukurti pasirinktinę formato versiją, pagrįstą iš konfigūracijos teikėjo gautu formatu, žr. [ER: formato naujinimas pritaikant naują pagrindinę to formato versiją](./tasks/er-upgrade-format.md).

## <a name="key-concepts"></a>Pagrindinės koncepcijos

Funkcijų valdymo teises turintys vartotojai gali kurti vartotojo priėmimo ir integravimo testavimą ir jiems nereikia rašyti išeitinio kodo.

- Naudokite ER pagrindinę informaciją, kad palygintumėte sugeneruotus dokumentus su pagrindinėmis kopijomis. Daugiau informacijos žr. [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su bazinėmis vertėmis](er-trace-reports-compare-baseline.md).
- Naudokite užduočių įrašymo priemonę, kad įrašytumėte testų aprašus ir įtrauktumėte pagrindinės informacijos įvertinimą. Daugiau informacijos žr. [Užduočių įrašymo priemonė](../user-interface/task-recorder.md).
- Grupuokite testų aprašus pagal reikiamus testavimo scenarijus. Daugiau informacijos žr. [Vartotojo priėmimo testavimų bibliotekų kūrimas naudojant užduočių įrašus ir BPM](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).

    - LCS naudokite verslo procesų modeliavimo įrankį (BPM), kad sukurtumėte vartotojo priėmimo testams skirtas bibliotekas.
    - Naudokite BPM testų bibliotekas, kad sukurtumėte testavimo planą ir testavimo paketus naudodami „Microsoft Azure DevOps“ paslaugas („Azure DevOps“).

Funkcijų valdymo teises turintys vartotojai gali vykdyti vartotojo priėmimo ir integravimo testus.

- Naudokite „Regression Suite Automation Tool“ (RSAT), kad vykdytumėte norimo testavimo paketo testų aprašus.
- Praneškite testavimo rezultatus „Azure DevOps“ ir naudodami šią paslaugą išanalizuokite tuos rezultatus.

## <a name="prerequisites"></a>Būtinieji komponentai

Norint atlikti šioje temoje esančias užduotis, būtina įgyvendinti toliau nurodytus reikalavimus.

- Įdiekite „Finance and Operations“ topologiją, palaikančią testavimo automatizavimą. Turite turėti vaidmens **Sistemos administratorius** teises pasiekti šios topologijos „Finance and Operations“ egzempliorių. Ši topologija turi apimti „Finance and Operations“ demonstracinius duomenis, kurie bus naudojami šiame pavyzdyje. Daugiau informacijos žr. [Visuotinis topologijų, palaikančių nuolatinio komponavimo versijų ir testavimo automatizavimo funkciją, diegimas](../perf-test/continuous-build-test-automation.md).
- Norint automatiškai vykdyti vartotojo priėmimo ir integravimo testus, reikia įdiegti RSAT topologijoje, kurią naudojate, ir atitinkamai jį konfigūruoti. Informacijos, kaip įdiegti RSAT ir jį konfigūruoti, kad jis veiktų su „Finance and Operations“ ir „Azure DevOps“, žr. [Dynamics 365 for Finance and Operations, Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357). Atkreipkite dėmesį į būtinąsias įrankio naudojimo sąlygas. Tolesnėje iliustracijoje pateikiamas RSAT parametrų pavyzdys. Mėlyname stačiakampyje nurodomi parametrai, kurie apibrėžia prieigą prie „Azure DevOps“. Žaliame stačiakampyje nurodomi parametrai, kurie apibrėžia prieigą prie „Finance and Operations“ egzemplioriaus.

    ![RSAT parametras](media/GER-Configure.png "RSAT parametrų dialogo lango ekrano kopija")

- Jei norite tvarkyti paketuose esančius testų aprašus, kad užtikrintumėte tinkamą vykdymo seką ir gautumėte testų vykdymo žurnalus tolesnių ataskaitų generavimo ir tyrimo tikslais, turite turėti prieigą prie „Azure DevOps“ iš įdiegtos „Finance and Operations“ topologijos.
- Kad užbaigtumėte šioje temoje pateiktą pavyzdį, rekomenduojame atsisiųsti [ER naudojimas siekiant atlikti RSAT testus](https://go.microsoft.com/fwlink/?linkid=874684). Šiame ZIP faile yra šie užduočių vedliai:

    | Turinys                                           | Failo vardas ir vieta |
    |---------------------------------------------------|------------------------|
    | Užduoties įrašo pavyzdys, skirtas testavimo duomenims paruošti | Prepare\\Recording.xml |
    | Užduoties įrašo pavyzdys, skirtas tiekėjo mokėjimui apdoroti   | Process\\Recording.xml |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a>Mokėtinų sumų modulio paruošimas, kad būtų galima apdoroti tiekėjo mokėjimus

1. Prisijunkite prie savo „Finance and Operations“ egzemplioriaus.
2. Atsisiųskite toliau nurodytas ER konfigūracijas iš LCS. Instrukcijų žr. [ER: konfigūracijos importavimas iš „Lifecycle Services‟](./tasks/er-import-configuration-lifecycle-services.md).

    - ER modelio **Mokėjimo modelis** konfigūracija
    - ER modelio susiejimo **Mokėjimo modelio susiejimas 1611** konfigūracija
    - **BACS (JK)** ER formato konfigūracija

    ![Elektroninių ataskaitų konfigūracijos](media/GER-Configurations.png "Elektroninių ataskaitų konfigūracijų puslapio ekrano kopija")

3. Pasirinkite demonstracinių duomenų įmonę **GBSI**, kurios šalies / regiono kontekstas yra Didžiojoje Britanijoje.
4. Sukonfigūruokite mokėtinų sumų modulio parametrus:

    1. Eikite į **Mokėtinos sumos \> Mokėjimo nustatymas \> Mokėjimo būdai**.
    2. Pasirinkite mokėjimo būdą **Elektroninis**.
    3. Konfigūruokite pasirinktą mokėjimo būdą, kad jame būtų naudojamas **BACS (JK)** ER formatas, kurį atsisiuntėte anksčiau tiekėjo mokėjimo apdorojimo tikslais:

        1. „FastTab“ **Failo formatai** nustatykite parinktį **Bendras elektroninis eksportavimo formatas** į **Taip**.
        2. Lauke **Eksportuoti formato konfigūraciją** pasirinkite **BACS (JK)**.

    ![Mokėjimo būdų puslapis](media/GER-APParameters.png "Mokėjimo būdų puslapio ekrano kopija")

    > [!NOTE]
    > Jei turite išvestą šio ER formato versiją, sukurtą tinkinimo tikslais, galite pasirinkti šią konfigūraciją mokėjimo būdo **Elektroninis** dalyje.

5. Sukurkite tiekėjo mokėjimo pavyzdį:

    1. Eikite į **Mokėtinos sumos \> Mokėjimai \> Mokėjimų žurnalas**.
    2. Įsitikinkite, kad neužregistravote mokėjimų žurnalo.

        ![Mokėjimų žurnalo puslapis](media/GER-APJournal.png "Mokėjimų žurnalo puslapio ekrano kopija")

    3. Pasirinkite **Eilutės** ir įveskite eilutę, kurioje yra toliau nurodyta informacija.

        | Laukas               | Reikšmės pavyzdys   |
        |---------------------|-----------------|
        | Tiekėjo vardas         | GB\_SI\_000001  |
        | Debetas               | 1,000.00        |
        | Valiuta            | LT             |
        | Koresp. sąsk. tipas | Bankas            |
        | Korespondentinė sąskaita      | GBSI OPER       |
        | Mokėjimo būdas   | Elektroninis      |

    ![Tiekėjo mokėjimų puslapis](media/GER-APJournalLines.png "Tiekėjo mokėjimų puslapio ekrano kopija")

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a>ER sistemos paruošimas, kad būtų galima apdoroti tiekėjo mokėjimus

### <a name="configure-er-parameters"></a>ER parametrų konfigūravimas

1. Pasirinkite **Organizacijos administravimas \> Elektroninės ataskaitos \> Elektroninių ataskaitų parametrai**.
2. Skirtuko **Priedai** lauke **Pagrindinė informacija** pasirinkite **Failas** kaip dokumento tipą, kurį naudoja dokumentų valdymo (DM) sistema, kad išsaugotų dokumentus, susijusius su pagrindinės informacijos funkcija, kaip DM priedus.

    ![Elektroninių ataskaitų parametrų puslapis](media/GER-ERParameters.png "Elektroninių ataskaitų parametrų puslapio ekrano kopija")

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a>Tiekėjo mokėjimo dokumentų pagrindinės informacijos kopijų generavimas

1. Eikite į **Mokėtinos sumos \> Mokėjimai \> Mokėjimų žurnalas**.
2. Pasirinkite **Eilutės**.
3. Pasirinkite **Generuoti mokėjimus**.
4. Pasirinkite mokėjimo būdą **Elektroninis**.
5. Pasirinkite **GBSI OPER** banko sąskaitą.
6. Nustatykite parinktį **Spausdinti kontrolės ataskaitą** į **Taip**.
7. Atsisiųskite sugeneruotą išvestį kaip ZIP failą.
8. Atidarykite atsisiųstą failą.
9. Išskleiskite toliau nurodytus failus iš atsisiųsto failo:

    - Mokėjimo failas **Failas** teksto formatu
    - **ERVendOutPaymControlReport** kontrolės ataskaitos failas XLSX formatu

    ![Išskleisti failai](media/GER-APJournalProcessed.png "Išskleistų failų vardų „Windows“ naršyklėje ekrano kopija")

### <a name="turn-on-the-er-baseline-feature"></a>ER pagrindinės informacijos funkcijos įjungimas

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
2. Veiksmų srities skirtuke **Konfigūracijos** pasirinkite **Vartotojo parametrai**.
3. Nustatykite parinktį **Vykdyti derinimo režimu** kaip **Taip**.

Įjungę parametrą **Vykdyti derinimo režimu**, priversite ER sistemą atlikti toliau nurodytus veiksmus, kai bus įvykdytas bet koks ER formatas, generuojantis siunčiamus dokumentus:

1. Nustatykite, ar buvo sukonfigūruota vykdyto ER formato kurio nors komponento pagrindinė informacija.
2. Nustatykite, ar visa sukonfigūruota pagrindinė informacija taikytina esamomis sąlygomis (prisijungusios įmonės kodas, sugeneruotos išvesties failo vardas ir failo vardo plėtinys ir pan.).
3. Atlikite toliau nurodytus veiksmus naudodami kiekvieną taikytiną pagrindinę informaciją:

    1. Palyginkite išvestį, sugeneruotą vykdant ER formatą naudojant atitinkamą pagrindinę informaciją.
    2. Išsaugokite palyginimo rezultatus ER konfigūracijų derinimo žurnale.

### <a name="configure-er-baselines-for-vendor-payment-processing"></a>Konfigūruokite ER pagrindinę informaciją, skirtą tiekėjo mokėjimams apdoroti

1. Eikite į **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijos**.
2. Pasirinkite **Pagrindinė informacija**.
3. Pasirinkite **Naujas**.
4. Lauke **Nuoroda** pasirinkite formatą **BACS (JK)**.
5. Pasirinkite **Priedai**.
6. Įtraukite naują tiekėjo mokėjimo failo pagrindinę informaciją:

    1. Pasirinkite **Naujas**.
    2. Lauke **Tipas** pasirinkite DM dokumentų tipą **Failas**, kurį sukonfigūravote ER parametrų dalyje, kad saugotumėte pagrindinės informacijos artefaktus.
    3. Naršykite ir pasirinkite vietoje įrašytą mokėjimo failą **Failas** teksto formatu.
    4. Lauke **Aprašas** įveskite **Mokėjimo TXT failas**.

7. Įtraukite naują pagrindinę informaciją, skirtą tiekėjo mokėjimų kontrolės ataskaitai:

    1. Pasirinkite **Naujas**.
    2. Lauke **Tipas** pasirinkite DM dokumentų tipą **Failas**, kurį sukonfigūravote ER parametrų dalyje, kad saugotumėte pagrindinės informacijos artefaktus.
    3. Naršykite ir pasirinkite vietoje įrašytą kontrolės ataskaitos failą **ERVendOutPaymControlReport** XLSX formatu.
    4. Lauke **Aprašas** įveskite **Mokėjimo XLSX kontrolės ataskaita**.

    ![Pagrindinė informacija, skirta tiekėjo mokėjimo failui ir kontrolės ataskaitai](media/GER-BaselineAttachments.png "Konfigūracijų puslapio, kuriame pasirinkta mokėjimo XLSX kontrolės ataskaita, ekrano kopija")

8. Uždarykite puslapį.
9. „FastTab“ **Pagrindinė informacija** pasirinkite **Nauja** ir sukonfigūruokite mokėjimo failo pagrindinę informaciją:

    1. Sukurkite eilutės **Mokėjimo failo pagrindinės informacijos parametras** pavadinimą.
    2. Lauke **Failo komponento pavadinimas** pasirinkite **Failas**, kad taikytumėte šią pagrindinę informaciją ER formato išvesčiai, generuojančiai mokėjimo failą BACS (JK) teksto formatu.
    3. Lauke **Įmonės** pasirinkite **GBSI**, kad taikytumėte šią pagrindinę informaciją, kai **BACS (JK)** ER formatas vykdomas GBSI įmonėje.
    4. Lauke **Failo vardo šablonas** įveskite **\*.TXT**, kad taikytumėte šią pagrindinę informaciją tik **failo** formato komponento išvestims, kurių failo vardo plėtinys **.txt**.
    5. Lauke **Pagrindinė informacija** pasirinkite **Mokėjimo TXT failas**, kad ši pagrindinė informacija būtų naudojama atliekant palyginimą su sugeneruota išvestimi.

10. Pasirinkite **Nauja**, kad sukonfigūruotumėte kontrolės ataskaitos pagrindinę informaciją:

    1. Sukurkite eilutės **Kontrolės ataskaitos pagrindinės informacijos parametras** pavadinimą.
    2. Lauke **Failo komponento pavadinimas** pasirinkite **ERVendOutPaymControlReport**, kad taikytumėte šią pagrindinę informaciją ER formato išvesčiai, generuojančiai kontrolės ataskaitą.
    3. Lauke **Įmonės** pasirinkite **GBSI**, kad taikytumėte šią pagrindinę informaciją, kai **BACS (JK)** ER formatas vykdomas GBSI įmonėje.
    4. Lauke **Failo vardo šablonas** įveskite **\*.XLSX**, kad taikytumėte šią pagrindinę informaciją tik **ERVendOutPaymControlReport** formato komponento išvestims, kurių failo vardo plėtinys **.xslx**.
    5. Lauke **Pagrindinė informacija** pasirinkite **Mokėjimo XLSX kontrolės ataskaita**, kad ši pagrindinė informacija būtų naudojama atliekant palyginimą su sugeneruota išvestimi.

    ![Pagrindinės informacijos „FastTab“ konfigūracijų puslapyje](media/GER-BaselineRules.png "Pagrindinės informacijos „FastTab“ konfigūracijų puslapyje ekrano kopija")

## <a name="record-tests-to-validate-vendor-payment-processing"></a>Įrašykite tiekėjo mokėjimų apdorojimo patikrinimo testus

Kadangi esate funkcijų valdymo teises turintis vartotojas, galite įrašyti savo veiksmus, kuriuos atliekant testuojamas tiekėjo mokėjimų apdorojimas. Rekomenduojame paleisti (ir, jei reikia, redaguoti) **Prepare\\Recording.xml** užduoties įrašą, kurį atsisiuntėte anksčiau. Šis įrašas naudojamas siekiant nustatyti tinkamą visų testavimo duomenų būseną. Šį veiksmą reikia atlikti, nes testavimą galima atlikti daug kartų ir kiekvienas testas turi naudoti tos pačios būsenos duomenis.

### <a name="reset-user-settings"></a>Iš naujo nustatykite vartotojo parametrus

1. Atidarykite numatytąją „Finance and Operations‟ ataskaitų sritį.
2. Pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis).
3. Pasirinkite **Vartotojo parinktys**.
4. Pasirinkite **Naudojimo duomenys**.
5. Pasirinkite **Nustatyti iš naujo**.
6. Pasirinkite **Taip**, kad patvirtintumėte, kad norite iš naujo nustatyti naudojimo duomenis.
7. Uždarykite puslapį.

### <a name="record-the-steps-to-prepare-data-for-testing"></a>Įrašykite testavimo duomenų paruošimo veiksmus

1. Pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis).
2. Pasirinkite **Užduočių įrašymo priemonė**.
3. Pasirinkite **Atkurti įrašą**.
4. Pasirinkite **Atidaryti iš šio kompiuterio**.
5. Pasirinkite **Naršyti** ir pasirinkite vietoje įrašytą failą **Prepare\\Recording.xml**.
6. Pasirinkite **Paleisti**.
7. Vis pasirinkite **Paleisti kitą laukiantį veiksmą**, kol paleisite visus įrašo veiksmus.

Pagal šį užduoties įrašą atliekami toliau nurodyti veiksmai.

1. Nustatykite apdorotos mokėjimo eilutės būseną **Nėra**.

    ![Užduoties įrašo 3–4 veiksmai](media/GER-Recording1Review1.png "Užduoties įrašo 3–4 veiksmų ekrano kopija")

2. Įjunkite **Vykdyti derinimo režimu** ER vartotojo parametrą.

    ![Užduoties įrašo 9–10 veiksmai](media/GER-Recording1Review2.png "Užduoties įrašo 9–10 veiksmų ekrano kopija")

3. Išvalykite ER derinimo žurnalą, kuriame yra sugeneruotų failų palyginimo su pagrindine informacija rezultatai.

    ![Užduoties įrašo 13–15 veiksmai](media/GER-Recording1Review3.png "Užduoties įrašo 13–15 veiksmų ekrano kopija")

### <a name="record-the-steps-to-test-vendor-payment-processing"></a>Įrašykite tiekėjo mokėjimų apdorojimo testavimo veiksmus

Rekomenduojame paleisti (ir, jei reikia, redaguoti) **Process\\Recording.xml** užduoties įrašą, kurį atsisiuntėte anksčiau. Šis įrašas naudojamas siekiant apdoroti tiekėjo mokėjimus ir patikrinti sugeneruotų dokumentų palyginimo su atitinkama pagrindine informacija rezultatus.

1. Pasirinkite mygtuką **Parametrai** (krumpliaračio simbolis).
2. Pasirinkite **Užduočių įrašymo priemonė**.
3. Pasirinkite **Atkurti įrašą**.
4. Pasirinkite **Atidaryti iš šio kompiuterio**.
5. Pasirinkite **Naršyti** ir pasirinkite vietoje įrašytą failą **Process\\Recording.xml**.
6. Pasirinkite **Paleisti**.
7. Vis pasirinkite **Paleisti kitą laukiantį veiksmą**, kol paleisite visus įrašo veiksmus.

Pagal šį užduoties įrašą atliekami toliau nurodyti veiksmai.

1. Pradėkite tiekėjo mokėjimų apdorojimą.
2. Pasirinkite tinkamus vykdymo parametrus ir įjunkite kontrolės ataskaitos generavimą.

    ![Užduoties įrašo 3–8 veiksmai](media/GER-Recording2Review1.png "Užduoties įrašo 3–8 veiksmų ekrano kopija")

3. Pasiekite ER derinimo žurnalą, kad įrašytumėte sugeneruotos išvesties palyginimo su atitinkama pagrindine informacija rezultatus.

    ER derinimo žurnale palyginimo rezultatai rodomi lauke **Sugeneruotas tekstas**. Laukai **Formato komponentas** ir **Formato kelias, dėl kurio atsirado žurnalo įrašas** nurodo failo komponentą, kurio sugeneruota išvestis buvo palyginta su pagrindine informacija.

    ![Elektroninių ataskaitų vykdymo žurnalų puslapio įrašai](media/GER-ERDebugLog.png "Elektroninių ataskaitų vykdymo žurnalų puslapio įrašų ekrano kopija")

4. Dabartinės išvesties palyginimas su pagrindine informacija įrašomas naudojant užduočių įrašymo priemonės parinktį **Tikrinti** ir pasirinkus  **Dabartinė reikšmė**.

    ![Tikrinimo parinkties naudojimas siekiant palyginti su dabartine reikšme](media/GER-TRRecordValidation.png "Tikrinimo parinkties naudojimo siekiant palyginti su dabartine reikšme ekrano kopija")

    Toliau pateiktoje iliustracijoje parodyta, kaip atrodo įrašyti tikrinimo veiksmai užduoties įraše.

    ![Užduoties įrašo 13 ir 15 veiksmai](media/GER-Recording2Review2.png "Užduoties įrašo 13 ir 15 veiksmų ekrano kopija")

## <a name="add-the-recorded-tests-to-azure-devops"></a>Įtraukite įrašytus testus į „Azure DevOps“

1. Atidarykite „Azure DevOps“ aplinką.
2. Pasirinkite projektą, kurį apibrėžėte RSAT parametrų dalyje, kai [konfigūravote įrankį](#prerequisites).
3. Pasirinkite testavimo planą, kurį apibrėžėte RSAT parametrų dalyje, kai [konfigūravote įrankį](#prerequisites).
4. Sukurkite naują pasirinkto testavimo plano testo aprašą:

    1. Sukurkite testo aprašo pavadinimą **Paruošti duomenis, skirtus tiekėjo elektroninių mokėjimų apdorojimui testuoti**.
    2. Pridėkite failą **Recording.xml** iš aplanko **Paruošti**, kurį atsisiuntėte anksčiau.

5. Sukurkite naują pasirinkto testavimo plano testo aprašą:

    1. Sukurkite testo aprašo pavadinimą **Testuoti tiekėjo mokėjimų apdorojimą naudojant ER formatą BACS (JK)**.
    2. Pridėkite failą **Recording.xml** iš aplanko **Apdoroti**, kurį atsisiuntėte anksčiau.

    ![Pasirinkto testavimo plano nauji testų aprašai](media/GER-RSAT-DevOps-Tests-Passed.png "Pasirinkto testavimo plano naujų testų aprašų ekrano kopija")

> [!NOTE]
> Užtikrinkite tinkamą įtrauktų testų vykdymo tvarką.

## <a name="prepare-rsat-to-run-the-recorded-tests"></a>Paruoškite RSAT vykdyti įrašytus testus

### <a name="load-the-tests-from-azure-devops-to-rsat"></a>Įkelkite testus iš „Azure DevOps“ į RSAT

1. Atidarykite vietinę RSAT programą dabartinėje topologijoje.
2. Pasirinkite **Įkelti**, kad įkeltumėte testus, kurie šiuo metu laikomi „Azure DevOps“, į RSAT.

    ![Į RSAT įkelti testai](media/GER-RSAT-RSAT-Tests-Loaded.png "Į RSAT įkeltų testų ekrano kopija")

### <a name="create-automation-and-parameters-files"></a>Kurkite automatizavimo ir parametrų failus

1. RSAT pasirinkite testus, kuriuos įkėlėte iš „Azure DevOps“.
2. Pasirinkite **Naujas**, kad sukurtumėte RSAT automatizavimo ir parametrų failus.

    ![RSAT automatizavimo ir parametrų failai, sukurti RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "RSAT automatizavimo ir parametrų failų, sukurtų RSAT, ekrano kopija")

### <a name="modify-the-parameters-files"></a>Modifikuokite parametrų failus

1. RSAT pasirinkite atvejo aprašą **Paruošti duomenis, skirtus tiekėjo elektroninių mokėjimų apdorojimui testuoti**.
2. Pasirinkite **Redaguoti**.
3. Atidarytos „Microsoft Excel“ darbaknygės darbalapyje **Bendra** pakeiskite įmonės kodą į **GBSI**, nes ši įmonė bus naudojama vykdant testą.
4. RSAT pasirinkite testo aprašą **Testuoti tiekėjo mokėjimų apdorojimą naudojant ER formatą BACS (JK)**.
5. Pasirinkite **Redaguoti**.
6. Atidarytos „Excel“ darbaknygės darbalapyje **Bendra** pakeiskite įmonės kodą į **GBSI**.
7. Darbalapyje **ERFormatMappingRunLogTable** pamatysite, kad A:3 ir C:3 langeliuose yra ER derinimo žurnalo lentelės laukų, naudojamų išvesties palyginimo su pagrindine informacija rezultatams tikrinti, tekstas. Šie tekstai bus naudojami siekiant įvertinti ER derinimo žurnalo įrašus, kurie sukuriami vykdant testą.

    ![ERFormatMappingRunLogTable darbalapis](media/GER-RSAT-RSAT-ExcelParameters.png "ERFormatMappingRunLogTable darbalapio ekrano kopija")

## <a name="run-the-tests-and-analyze-the-results"></a>Vykdykite testus ir analizuokite rezultatus

### <a name="run-the-tests-in-rsat"></a>Vykdykite testus RSAT

1. RSAT pasirinkite įkeltus testus.
2. Pasirinkite **Vykdyti**.

Atkreipkite dėmesį, kad testų aprašai yra automatiškai vykdomi „Finance and Operations“ naudojant žiniatinklio naršyklę.

### <a name="analyze-the-results-of-test-execution"></a>Analizuokite testo vykdymo rezultatus

Testo vykdymo rezultatai saugomi RSAT. Atkreipkite dėmesį, kad abiejų testų rezultatai teigiami.

![Testai, kurių rezultatai teigiami RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Testų, kurių rezultatai teigiami RSAT, ekrano kopija")

Atkreipkite dėmesį, kad testo vykdymo rezultatai taip pat siunčiami „Azure DevOps“, kad galėtumėte atlikti tolesnę analizę.

![Testo vykdymo rezultatai, esantys „Azure DevOps“](media/GER-RSAT-DevOps-Tests-Added.png "Testo vykdymo rezultatų, esančių „Azure DevOps“, ekrano kopija")

### <a name="simulate-a-situation-where-tests-fail"></a>Sumodeliuokite situaciją, kurioje būtų gauti neigiami testo rezultatai

Turi būti gauti neigiami šio testų paketo rezultatai, kai bent viena sugeneruota išvestis neatitinka atitinkamos pagrindinės informacijos. Norėdami sukurti tokią situaciją, galite naudoti savo išvestą **BACS (JK)** formato versiją, kuri sugeneruos mokėjimo failą, kurio turinys skiriasi nuo atitinkamos pagrindinės informacijos. Norėdami sumodeliuoti šią situaciją, galite naudoti tą patį **BACS (JK)** formatą, bet apdorotoje mokėjimo eilutėje pakeiskite mokėjimo sumą.

1. Žiniatinklio naršyklėje atidarykite „Finance and Operations“.
2. Eikite į **Mokėtinos sumos \> Mokėjimai \> Mokėjimų žurnalas**.
3. Pasirinkite **Eilutės**.
4. Pasirinkite mokėjimo eilutę ir pasirinkite **Mokėjimo būsena \> Nėra**.
5. Lauke **Debetas** pakeiskite **1 000,00** reikšmę į **2 000,00**.
6. Pasirinkite **Įrašyti**, kad įrašytumėte pakeitimus.

### <a name="run-the-tests-in-rsat"></a>Vykdykite testus RSAT

1. RSAT pasirinkite įkeltus testus.
2. Pasirinkite **Vykdyti**.

Atkreipkite dėmesį, kad testų aprašai yra automatiškai vykdomi „Finance and Operations“ naudojant žiniatinklio naršyklę.

### <a name="analyze-the-results-of-test-execution"></a>Analizuokite testo vykdymo rezultatus

Testo vykdymo rezultatai saugomi RSAT. Atkreipkite dėmesį, kad vykdant antrą kartą gauti neigiami antro testo rezultatai.

![Neigiami testo rezultatai RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Neigiamų testo rezultatų RSAT ekrano kopija")

Atkreipkite dėmesį, kad testo vykdymo rezultatai taip pat siunčiami „Azure DevOps“, kad galėtumėte atlikti tolesnę analizę.

![Neigiami testo rezultatai „Azure DevOps“](media/GER-RSAT-DevOps-Tests-Failed.png "Neigiamų testo rezultatų „Azure DevOps“ ekrano kopija")

Galite pasiekti kiekvieno testo būseną. Taip pat galite pasiekti vykdymo žurnalą, kad galėtumėte analizuoti klaidų priežastis. Toliau pateiktame vykdymo žurnale parodyta, kad klaida kilo todėl, kad skiriasi sugeneruoto mokėjimo failo ir jo pagrindinės informacijos turinys.

![Vykdymo žurnalas, leidžiantis analizuoti klaidas „Azure DevOps“](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Vykdymo žurnalo, leidžiančio analizuoti klaidas „Azure DevOps“, ekrano kopija")

Todėl, kaip matėte, bet kokio ER formato veikimą galima įvertinti automatiškai naudojant RSAT kaip testavimo platformą ir naudojant užduočių įrašymo priemonės testų aprašus, naudojančius ER pagrindinės informacijos funkciją.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Užduoties įrašymo priemonė](../user-interface/task-recorder.md)
- [„Regression Suite Automation Tool”](https://www.microsoft.com/download/details.aspx?id=57357)
- [Vartotojo priėmimo testų bibliotekų kūrimas naudojant užduoties įrašus ir BPM](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [Visuotinis topologijų, palaikančių nuolatinio komponavimo versijų ir bandymo automatizavimo funkciją, diegimas](../perf-test/continuous-build-test-automation.md)
- [Sugeneruotų ataskaitų rezultatų sekimas ir jų palyginimas su ER bazinėmis vertėmis](er-trace-reports-compare-baseline.md)
- [ER formato atnaujinimas pritaikant naują pagrindinę to formato versiją](tasks/er-upgrade-format.md)
- [ER konfigūracijos importavimas iš „Lifecycle Services‟](tasks/er-import-configuration-lifecycle-services.md)
