---
title: Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui
description: Šioje temoje paaiškinama, kaip galite sukonfigūruoti, kad būtų naudojami modulio Elektroninės ataskaitos (ER) formatai, nurodyti kiekvienam juridiniam subjektui.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: d32da76ee46ff5293ae8fefb16d251564b6be21a
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694251"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Peržiūrėti

Daugelyje modulio Elektroninės ataskaitos (ER) formatų, kuriuos kursite, turite filtruoti duomenis naudodami reikšmių, kurios yra konkrečios jūsų egzemplioriaus juridinio subjekto reikšmės, rinkinį (pavyzdžiui, mokesčių kodų rinkinį mokesčių operacijoms filtruoti). Šiuo metu, kai ER formate sukonfigūruotas šio tipo filtravimas, ER formato reiškiniuose naudojant nuo juridinio subjekto priklausančias reikšmes (pavyzdžiui, mokesčių kodus) nurodomos duomenų filtravimo taisyklės. Todėl ER formatas sukuriamas konkrečiam juridiniam subjektui ir, norėdami kurti reikiamas ataskaitas, kiekvienam juridiniam subjektui, kuriam turite vykdyti ER formatą, turite sukurti išvestines pradinio ER formato kopijas. Kiekvieną išvestinį ER formatą reikia redaguoti, kad į jį būtų perkeltos konkretaus juridinio subjekto reikšmės, reikia keisti jo pagrindą, kai tik atnaujinama pradinė (bazinė) versija, formatą reikia eksportuoti iš tikrinimo aplinkos ir importuoti į gamybos aplinką, kai jį reikia įdiegti gamybai, ir t. t. Todėl šio tipo sukonfigūruoto ER sprendimo tvarkymas yra gana sudėtingas ir atima daug laiko dėl kelių tolesnių priežasčių.

-   Kuo yra daugiau juridinių subjektų, tuo daugiau ER formatų konfigūracijų reikia tvarkyti.
-   Kad įmonių vartotojai galėtų tvarkyti ER konfigūracijas, jiems reikia turėti ER žinių.

Naudodami konkrečiai ER programai skirtų parametrų funkciją, patyrę vartotojai ER formate gali sukonfigūruoti duomenų filtravimą, kad jis būtų pagrįstas abstrakčių taisyklių rinkiniu. Galima sukonfigūruoti, kad šis taisyklių rinkinys naudotų ER formate esančius duomenų šaltinius. Įmonių vartotojai tada gali nurodyti tikras ne tik ER sistemoje taikomas taisykles – tai jie gali daryti naudodami vartotojo sąsają (UI), kuri automatiškai sugeneruojama pagal atitinkamo ER formato parametrus ir tuometinius juridinio subjekto duomenis, kuriuos naudos ER formato duomenų šaltiniai. Nurodytą ER formato taisyklių rinkinį galima eksportuoti iš „Dynamics 365 Finance“ („Finance“) egzemplioriaus tuometinio juridinio subjekto. Tada jį galima importuoti į kitą to paties „Finance“ egzemplioriaus arba kito egzemplioriaus juridinį subjektą kaip to paties ER formato taisyklių rinkinį.

## <a name="prerequisites"></a>Būtinieji komponentai

Norint įvykdyti šioje temoje pateikiamus pavyzdžius, reikia turėti prieigą prie „Regulatory Configuration Services“ (RCS) egzemplioriaus, kuris sukonfigūruotas tam pačiam nuomotojui, kaip „Finance“, vienam iš toliau nurodytų vaidmenų atlikti.

- Elektroninės ataskaitos kūrėjas
- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Rekomenduojame atlikti veiksmus, aprašytus temoje [Tipo APSKAIČIUOTAS LAUKAS ER duomenų šaltinių parametrizuotų iškvietų palaikymas](er-calculated-field-type.md). Jei tuos veiksmus jau atlikote, galite praleisti tolesniame skyriuje **ER konfigūracijų importavimas į RCS** aprašytus veiksmus.

## <a name="import-er-configurations-into-rcs"></a>ER konfigūracijų importavimas į RCS

Iš [„Microsoft“ atsisiuntimo centro](https://go.microsoft.com/fwlink/?linkid=851448) atsisiųskite ZIP failą **Tipo APSKAIČIUOTAS LAUKAS ER duomenų šaltinių parametrizuotų iškvietų palaikymas**. Šiame ZIP faile yra tolesnės ER konfigūracijos, kurias reikia išskleisti ir saugoti vietoje.

| **Turinio aprašas**                        | **Failo vardas**                                        |
|------------------------------------------------|------------------------------------------------------|
| **ER duomenų modelio** konfigūracijos pavyzdžio failas    | Parametrizuotų kvietimų mokymo modelis.versija.1.xml     |
| **ER metaduomenų** konfigūracijos pavyzdžio failas      | Parametrizuotų kvietimų mokymo metaduomenys.versija.1.xml  |
| **ER modelio susiejimo** konfigūracijos pavyzdžio failas | Parametrizuotų kvietimų mokymo susiejimas.versija.1.1.xml |
| **ER formato** konfigūracijos pavyzdys             | Parametrizuotų kvietimų mokymo formatas.versija.1.1.xml  |

Tada prisijunkite prie savo RCS egzemplioriaus.

Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Kad galėtumėte atlikti šią procedūrą, turite atlikti RCS temoje [Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu](tasks/er-configuration-provider-mark-it-active-2016-11.md) aprašytus veiksmus.

1.  Numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.
2.  Pasirinkite **Ataskaitų konfigūracijos**.
3.  Anksčiau atsisiųstas ER konfigūracijas tolesne tvarka importuokite į RCS: duomenų modelis, metaduomenys, modelio susiejimas ir formatas. Kurdami kiekvieną ER konfigūraciją atlikite toliau nurodytus veiksmus.

    1.  Pasirinkite **Keitimas**.
    2.  Pasirinkite **Įkelti iš XML failo**.
    3.  Paspaudę **Naršyti** pasirinkite reikiamos ER konfigūracijos failą XML formatu.
    4.  Pasirinkite **Gerai**.

## <a name="review-the-er-solution-that-is-provided"></a>Pateikto ER sprendimo peržiūra

1.  Konfigūracijos medyje išplėskite elemento **Parametrizuotų iškvietų mokymo modelis** turinį.
2.  Pasirinkite elementą **Parametrizuotų iškvietų mokymo formatas**.
3.  Pasirinkite **Dizaino įrankis**.
4.  Pasirinkite **Išplėsti / sutraukti**.

    ER formatas **Parametrizuotų iškvietų mokymo formatas** skirtas tam, kad būtų galima generuoti XML formato mokesčių išrašą, kuriame būtų pateikiami keli apmokestinimo lygiai (įprastas, sumažintas ir joks). Kiekviename lygyje pateikiamas skirtingas informacijos kiekis.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Skirtuke **Susiejimas** išplėskite elementus **Modelis**, **Duomenys** ir **Suvestinė**.

    Duomenų šaltinis **Model.Data.Summary** pateikia mokesčių operacijų sąrašą. Šių operacijų suvestinė pateikiama pagal mokesčio kodą. Naudojant šį duomenų šaltinį, apskaičiuotas laukas **Model.Data.Summary.Level** sukonfigūruotas taip, kad jame būtų pateikiamas kiekvieno apibendrinto įrašo apmokestinimo lygio kodas. Pasirinkus mokesčio kodą, kurį vykdymo metu galima gauti iš duomenų šaltinio **Model.Data.Summary**, apskaičiuotame lauke kaip tekstinė reikšmė pateikiamas apmokestinimo lygio kodas (**Įprastas**, **Sumažintas**, **Joks** arba **Kita**). Apskaičiuotas laukas **Model.Data.Summary.Level** naudojamas norint filtruoti duomenų šaltinio **Model.Data.Summary** įrašus ir filtruotus duomenis įvesti kiekviename XML elemente, vaizduojančiame apmokestinimo lygį – naudojami laukai **Model.Data2.Level1**, **Model.Data2.Level2** ir **Model.Data2.Level3**.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Apskaičiuotas laukas **Model.Data.Summary.Level** sukonfigūruotas taip, kad jame būtų ER reiškinys. Atkreipkite dėmesį, kad mokesčių kodai (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** ir **InVAT0**) į šią konfigūraciją yra įprogramuoti. Todėl šis ER formatas priklauso nuo juridinio subjekto, kuriam šie mokesčių kodai buvo sukonfigūruoti.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Norėdami kiekvienam juridiniam subjektui įjungti skirtingą mokesčių kodų rinkinį, turite atlikti tolesnius veiksmus.

    - Kiekvienam juridiniam subjektui sukurti išvestinę ER formato versiją.
    - Pagal juridinio subjekto parametrą atnaujinti apskaičiuoto lauko **Model.Data.Summary.Level** mokesčių kodus.

6.  Uždarykite puslapį **Formato dizaino įrankis**.

## <a name="create-a-derived-format"></a>Sukurkite išvestinį formatą

Toliau, naudodami konkrečios ER programos parametrų funkciją, įjungsite galimybę viename ER formate kiekvienam juridiniam subjektui naudoti skirtingą mokesčių kodų rinkinį.

1.  Konfigūracijos medyje išplėskite elemento **Parametrizuotų iškvietų mokymo modelis** turinį.
2.  Pasirinkite elementą **Parametrizuotų iškvietų mokymo formatas**.
3.  Pasirinkite **Kurti konfigūraciją**.
4.  Pasirinkite parinktį **Kildinti iš pavadinimo: parametrizuotų iškvietų mokymo formatas, „Microsoft“**.
5.  Lauke **Pavadinimas** įveskite **Mokymo, kaip peržvelgti LE duomenis, formatas**.
6.  Pasirinkite **Kurti konfigūraciją**.

## <a name="configure-a-derived-format"></a>Išvestinio formato konfigūravimas

### <a name="add-a-format-enumeration"></a>Formatų išvardijimo įtraukimas

Toliau įtrauksite naują ER formatų išvardijimą. Šio formato išvardijimo reikšmės bus pateiktos įmonių vartotojams, kurie nurodys įvairių apmokestinimo lygių konkrečius nuo juridinio subjekto priklausomus mokesčių kodų rinkinius, naudojamus ER formate.

1.  Pasirinkite **Dizaino įrankis**.
2.  Pasirinkite **Formatų išvardijimai**.
3.  Pasirinkite **Įtraukti**.
4.  Lauke **Pavadinimas** įveskite **Apmokestinimo lygių sąrašas**.
5.  Pasirinkite **Įrašyti**.
6.  Skirtuke **Formatų išvardijimo reikšmės** pasirinkite **Įtraukti**.
7.  Lauke **Pavadinimas** įveskite **Įprastas apmokestinimas**.
8.  Dar kartą pasirinkite **Įtraukti**.
9.  Lauke **Pavadinimas** įveskite **Sumažintas apmokestinimas**.
10. Dar kartą pasirinkite **Įtraukti**.
11. Lauke **Pavadinimas** įveskite **Apmokestinimo nėra**.
12. Dar kartą pasirinkite **Įtraukti**.
13. Lauke **Pavadinimas** įveskite **Kita**.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Kadangi nurodydami nuo juridinio subjekto priklausančius mokesčių kodų rinkinius įmonių vartotojai gali naudoti skirtingas kalbas, rekomenduojame šio išvardijimo reikšmes išversti į kalbas, kurios yra sukonfigūruotos kaip pageidaujamos tų vartotojų kalbos programoje „Finance“.

14. Pasirinkite įrašą **Apmokestinimo nėra**.
15. Spustelėkite lauką **Žyma**.
16. Pasirinkite **Versti**.
17. Srities **Teksto vertimas** lauke **Žymos ID** įveskite **LBL_LEVELENUM_NO**.
18. Lauke **Tekstas numatytąja kalba** įveskite **Apmokestinimo nėra**.
19. Lauke **Kalba** pasirinkite **LT**.
20. Lauke **Išverstas tekstas** įveskite **Apmokestinimo nėra**.
21. Pasirinkite **Versti**.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Pasirinkite **Įrašyti**.
23. Uždarykite puslapį **Formatų išvardijimai**.

### <a name="add-a-new-lookup-data-source"></a>Naujo peržvalgos duomenų šaltinio įtraukimas

Toliau įtrauksite naują duomenų šaltinį ir nurodysite, kaip įmonių vartotojai nustatys nuo juridinio subjekto priklausančias taisykles, kad būtų galima atpažinti teisingą kiekvieno apibendrinto operacijos įrašo apmokestinimo lygį.

1.  Skirtuke **Susiejimas** pasirinkite **Įtraukti**.
2.  Pasirinkite **Formatų išvardijimas\Peržvalga**.

    Ką tik nustatėte, kad kiekviena taisyklė, kurią įmonių vartotojai nurodo apmokestinimo lygiui atpažinti, pateiks ER formato išvardijimo reikšmę. Atkreipkite dėmesį, kad duomenų šaltinio tipą **Peržvalga** galima pasiekti ne tik bloke **Formatų išvardijimas**, bet ir blokuose **Duomenų modelis** ir **„Dynamics 365 for Operations“**. Todėl, naudojant ER duomenų modelio išvardijimus ir programos išvardijimus, galima nurodyti pateikiamų to tipo duomenų šaltinių reikšmių tipą.
    
3.  Lauke **Pavadinimas** įveskite **Išrinkiklis**.
4.  Lauke **Formatų išvardijimas** pasirinkite **Apmokestinimo lygių sąrašas**.

    Ką tik nustatėte, kad kiekvienai taisyklei, nurodytai šiame duomenų šaltinyje, įmonės vartotojas kaip pateikiamą reikšmę turi pasirinkti vieną iš formatų išvardijimo **Apmokestinimo lygių sąrašas** reikšmių.
    
5.  Pasirinkite **Redaguoti peržvalgą**.
6.  Pasirinkite **Stulpeliai**.
7.  Išplėskite elementą **Modelis**.
8.  Išplėskite elementą **Duomenys**.
9.  Išplėskite elementą **Mokestis**.
10. Pasirinkite elementą **Model.Data.Tax.Code**.
11. Pasirinkite mygtuką **Įtraukti** (rodyklę dešinėn).

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Ką tik nustatėte, kad kiekvienai taisyklei, šiame duomenų šaltinyje nurodytai apmokestinimo lygiui atpažinti, įmonės vartotojas kaip sąlygą turi pasirinkti vieną iš mokesčių kodų. Mokesčių kodų, kuriuos įmonės vartotojas gali pasirinkti, sąrašas bus pateikiamas duomenų šaltinyje **Model.Data.Tax**. Kadangi šiame duomenų šaltinyje yra laukas **Pavadinimas**, įmonės vartotojui pateikiamoje peržvalgoje bus rodomas kiekvienos mokesčio kodo reikšmės pavadinimas.
    
12. Pasirinkite **Gerai**.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Įmonių vartotojai kaip šio duomenų šaltinio įrašus gali įtraukti kelias taisykles. Kiekvienas įrašas bus sunumeruotas pagal eilutės kodą. Taisyklės bus vertinamos eilutės numerio didėjimo tvarka.

    Kadangi šiame peržvalgos duomenų šaltinyje kaip taisyklių sąlygą pasirinkote lauką **Mokesčio kodas** ir kadangi **Mokesčio kodas** yra nustatytas kaip duomenų tipo **Eilutė** laukas, vykdymo metu kiekviena taisyklė bus vertinama mokesčio kodą, perduotą į duomenų šaltinį, palyginant su mokesčio kodu, kuris nustatytas šiame duomenų šaltinio įraše.

    Kai randama taisyklė, tenkinanti sukonfigūruotą sąlygą, šis duomenų šaltinis pateikia taisyklės, kuri apibrėžta lauke **Peržvalgos rezultatas**, peržvalgos reikšmę. Jei taisyklių nerandama, pateikiama išimtis, vartotojui pranešanti, kad dabartinis duomenų šaltinis negali pateikti teisingos reikšmės.

13. Pasirinkite **Įrašyti**.
14. Uždarykite puslapį **Peržvalgos konstruktorius**.
15. Pasirinkite **Gerai**.

    Atkreipkite dėmesį, kad įtraukėte naują duomenų šaltinį, kuris apmokestinimo lygį pateiks kaip formatų išvardijimo **Apmokestinimo lygių sąrašas** reikšmę bet kuriam mokesčio kodui, į duomenų šaltinį perduodamam kaip duomenų tipo **Eilutė** parametro **Kodas** argumentui.
    
    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Atkreipkite dėmesį, kad sukonfigūruotų taisyklių vertinimas priklauso nuo laukų, kurie buvo pasirinkti tų taisyklių sąlygoms apibrėžti, duomenų tipo. Pasirinkus lauką, kuris sukonfigūruotas kaip duomenų tipo **Skaitinis** arba **Data** laukas, kriterijai skirsis nuo anksčiau aprašytų duomenų tipo **Eilutė** kriterijų. Naudojant laukus **Skaitinis** ir **Data**, taisyklę reikia nurodyti kaip reikšmių intervalą. Tada taisyklės sąlyga bus laikoma įvykdyta, kai į duomenų šaltinį perduota reikšmė bus sukonfigūruotame intervale.
    
    Tolesnėje iliustracijoje pateikiamas šio tipo sąrankos pavyzdys. Be duomenų tipo **Eilutė** lauko **Model.Data.Tax.Code** peržvalgos duomenų šaltinio sąlygoms nurodyti taip pat naudojamas duomenų tipo **Realus** laukas **Model.Tax.Summary.Base**.
    
    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Kadangi šiam peržvalgos duomenų šaltiniui pasirinkti laukai **Model.Data.Tax.Code** ir **Model.Tax.Summary.Base**, kiekviena šio duomenų šaltinio taisyklė bus konfigūruojama taip, kaip nurodyta toliau.
    
    -   Pateiktame sąraše formatų išvardijimo **Apmokestinimo lygių sąrašas** reikšmę reikia pasirinkti kaip pateiktą reikšmę.
    -   Mokesčio kodą reikia įvesti kaip šios taisyklės sąlygą. Taikytini tik tie mokesčių kodai, kuriuos pateikia duomenų šaltinis **Model.Data.Tax**.
    -   Kaip šios taisyklės sąlygas reikia įvesti minimalią ir maksimalią bazinės mokesčių sumos reikšmes.

    Vykdymo metu kiekviena šio duomenų šaltinio taisyklė bus vertinama taip, kaip nurodyta toliau.
    -   Ar duomenų tipo **Eilutė** kodas, kuris buvo perduotas į šį duomenų šaltinį, yra lygus taisyklės mokesčio kodui?
    -   Ar duomenų tipo **Realus** reikšmė, kuri buvo perkelta į šį duomenų šaltinį, yra tarp konkrečių minimalios ir maksimalios reikšmių?

    Taisyklė bus taikoma taikytina, kai bus tenkinamos abi sąlygos.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Įtrauktos peržvalgos duomenų šaltinio žymos vertimas

Kadangi nurodydami nuo juridinio subjekto priklausančius mokesčių kodų rinkinius įmonių vartotojai gali naudoti skirtingas kalbas, rekomenduojame bet kokio įtraukto duomenų šaltinio žymą išversti, kad atitinkamame puslapyje ji būtų pateikiama kiekvieno vartotojo pageidaujama kalba.

1.  Pasirinkite duomenų šaltinį **Model.Data.Selector**.
2.  Pasirinkite **Redaguoti**.
3.  Spustelėkite lauką **Žyma**.
4.  Pasirinkite **Versti**.
5.  Srities **Teksto vertimas** lauke **Žymos ID** įveskite **LBL_SELECTOR_DS**.
6.  Lauke **Tekstas numatytąja kalba** įveskite **Mokesčio lygio pasirinkimas pagal mokesčio kodą**.
7.  Lauke **Kalba** pasirinkite **LT**.
8.  Lauke **Išverstas tekstas** įveskite **Mokesčio lygio pasirinkimas pagal mokesčio kodą**.
9.  Pasirinkite **Versti**.
10. Pasirinkite **Gerai**.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Naujo lauko sukonfigūruotai peržvalgai naudoti įtraukimas

1.  Išplėskite elementą **Model.Data**.
2.  Pasirinkite elementą **Model.Data.Summary**.
3.  Pasirinkite **Įtraukti**.
4.  Pasirinkite **Funkcijos/Apskaičiuotas laukas**.
5.  Lauke **Pavadinimas** įveskite **LevelByLookup**.
6.  Pasirinkite **Redaguoti formulę**.
7.  **Lauke Formulė** įveskite **Model.Selector(Model.Data.Summary.Code)**.
8.  Pasirinkite **Įrašyti**.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Uždarykite puslapį **Formulės rengyklė**.
10. Pasirinkite **Gerai**.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Atkreipkite dėmesį, kad jūsų įtrauktas apskaičiuotas laukas **LevelByLookup** apmokestinimo lygį pateiks kaip kiekvieno apibendrinto mokesčių operacijų įrašo formatų išvardijimo **Apmokestinimo lygių sąrašas** reikšmę. Įrašo mokesčio kodas bus perduotas į peržvalgos duomenų šaltinį **Model.Selector** ir šio duomenų šaltinio taisyklių rinkinys bus naudojamas tinkamam apmokestinimo lygiui parinkti.

### <a name="add-a-new-format-enumeration-based-data-source"></a>Naujo formatų išvardijimu paremto duomenų šaltinio įtraukimas

Toliau įtrauksite naują duomenų šaltinį, nurodantį į anksčiau įtrauktą formatų išvardijimą. Šio duomenų šaltinio reikšmės vėliau bus naudojamos ER formato reiškinyje.

1.  Pasirinkite **Įtraukti šaknį**.
2.  Pasirinkite **Formatų išvardijimai\Išvardijimas**.
3.  Lauke **Pavadinimas** įveskite **ApmokestinimoLygis**.
4.  Lauke **Formatų išvardijimas** pasirinkite **Apmokestinimo lygių sąrašas**.
5.  Pasirinkite **Įrašyti**.

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a>Esamo lauko modifikavimas, kad būtų pradėta naudoti peržvalga

Toliau modifikuosite esamą apskaičiuotą lauką, kad jis, naudodamas sukonfigūruotą peržvalgos duomenų šaltinį, pateiktų tinkamą apmokestinimo lygio reikšmę, priklausančią nuo mokesčio kodo.

1.  Pasirinkite elementą **Model.Data.Summary.Level**.
2.  Pasirinkite **Redaguoti**.
3.  Pasirinkite **Redaguoti formulę**.

    Atkreipkite dėmesį, kad dabartiniame lauko **Model.Data.Summary.Level** reiškinyje yra tolesni užprogramuoti mokesčių kodai.
    
    CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")

4.  Lauke **Formulė** įveskite **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.

    ![ER operacijų dizaino įrankio puslapis](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Atkreipkite dėmesį, kad lauko **Model.Data.Summary.Level** reiškinys dabar apmokestinimo lygį pateiks pagal dabartinio įrašo mokesčio kodą ir taisyklių rinkinį, kurį įmonės vartotojas sukonfigūruoja peržvalgos duomenų šaltinyje **Model.Data.Selector**.
    
5.  Pasirinkite **Įrašyti**.
6.  Uždarykite puslapį **Formulės konstruktorius**.
7.  Pasirinkite **Gerai**.
8.  Pasirinkite **Įrašyti**.
9.  Uždarykite puslapį **Formato dizaino įrankis**.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Išvestinio formato versijos juodraščio baigimas

1.  „FastTab“ elemente **Versijos** pasirinkite **Keisti būseną**.
2.  Pasirinkite **Baigti**.
3.  Pasirinkite **Gerai**.

## <a name="export-completed-version-of-modified-format"></a>Baigtos išvestinio formato versijos eksportavimas

1.  Konfigūracijos medyje pasirinkite elementą **Mokymo, kaip peržvelgti LE duomenis, formatas**.
2.  „FastTab“ elemente **Versijos** pasirinkite įrašą, kurio būsena yra **Baigtas**.
3.  Pasirinkite **Keitimas**.
4.  Pasirinkite **Eksportuoti kaip XML failą**.
5.  Pasirinkite **Gerai**.
6.  Žiniatinklio naršyklė atsiunčia failą **Mokymo, kaip peržvelgti LE duomenis, formatas.xml**. Šį failą išsaugokite vietiniame įrenginyje.

Šio skyriaus veiksmus pakartokite su pirminiais formato **Mokymo, kaip peržvelgti LE duomenis, formatas** elementais ir vietiniame įrenginyje išsaugokite tolesnius failus.

-   Parametrizuotų iškvietų mokymo formatas.xml
-   Parametrizuotų iškvietų mokymo susiejimas.xml
-   Parametrizuotų iškvietų mokymo modelis.xml

Norėdami sužinoti, kaip, naudojant sukonfigūruotą ER formatą **Mokymo, kaip peržvelgti LE duomenis, formatas**, nustatyti nuo juridinio subjekto priklausomus mokesčių kodus ir mokesčių operacijas filtruoti pagal skirtingus apmokestinimo lygius, atlikite veiksmus, nurodytus temoje [ER formato parametrų nustatymas kiekvienam juridiniui subjektui](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[ER formato parametrų nustatymas kiekvienam juridiniui subjektui](er-app-specific-parameters-set-up.md)
