---
title: ER formatų konfigūravimas, kurį atlikus naudojami juridiniam subjektui nurodyti parametrai
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti elektroninių ataskaitų (ER) formatus, kad būtų naudojami kiekvienam juridiniam subjektui nurodyti parametrai.
author: kfend
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
ms.openlocfilehash: b81c9c8fd1639b9af53c8e15a041c00db8c19752
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292683"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>Kaip sukonfigūruoti, kad būtų naudojami ER formatų parametrai, nurodyti kiekvienam juridiniam subjektui

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Peržiūrėti

Daugelyje modulio Elektroninės ataskaitos (ER) formatų, kuriuos kursite, turite filtruoti duomenis naudodami reikšmių, kurios yra konkrečios jūsų egzemplioriaus juridinio subjekto reikšmės, rinkinį (pavyzdžiui, mokesčių kodų rinkinį mokesčių operacijoms filtruoti). Šiuo metu, kai ER formate sukonfigūruotas šio tipo filtravimas, ER formato reiškiniuose naudojant nuo juridinio subjekto priklausančias reikšmes (pavyzdžiui, mokesčių kodus) nurodomos duomenų filtravimo taisyklės. Todėl ER formatas sukuriamas konkrečiam juridiniam subjektui ir, norėdami kurti reikiamas ataskaitas, kiekvienam juridiniam subjektui, kuriam turite vykdyti ER formatą, turite sukurti išvestines pradinio ER formato kopijas. Kiekvieną išvestinį ER formatą reikia redaguoti, kad į jį būtų perkeltos konkretaus juridinio subjekto reikšmės, reikia keisti jo pagrindą, kai tik atnaujinama pradinė (bazinė) versija, reikia eksportuoti iš testavimo aplinkos ir importuoti į gamybos aplinką, kai jį reikia įdiegti gamybiniam naudojimui, ir kita. Todėl šio tipo sukonfigūruoto ER sprendimo tvarkymas yra sudėtingas ir atima daug laiko dėl kelių priežasčių:

-   Kuo yra daugiau juridinių subjektų, tuo daugiau ER formatų konfigūracijų reikia tvarkyti.
-   Kad įmonių vartotojai galėtų tvarkyti ER konfigūracijas, jiems reikia turėti ER žinių.

Naudodami konkrečiai ER programai skirtų parametrų funkciją, patyrę vartotojai ER formate gali sukonfigūruoti duomenų filtravimą, kad jis būtų pagrįstas abstrakčių taisyklių rinkiniu. Galima sukonfigūruoti, kad šis taisyklių rinkinys naudotų ER formate esančius duomenų šaltinius. Įmonių vartotojai tada gali nurodyti tikras ne tik ER sistemoje taikomas taisykles – tai jie gali daryti naudodami vartotojo sąsają (UI), kuri automatiškai sugeneruojama pagal atitinkamo ER formato parametrus ir tuometinius juridinio subjekto duomenis, kuriuos naudos ER formato duomenų šaltiniai. Taisyklių rinkinį, nurodytą ER formatu, galima eksportuoti iš dabartinio "Dynamics 365 Finance (Finance) egzemplioriaus juridinio subjekto. Tada jį galima importuoti į kitą to paties „Finance“ egzemplioriaus arba kito egzemplioriaus juridinį subjektą kaip to paties ER formato taisyklių rinkinį.

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami užbaigti pavyzdžius šiame straipsnyje, turite turėti prieigą prie reguliavimo konfigūracijos tarnybų (RCS), kurios buvo rastos tam pačiam nuomininkui kaip ir finansai vienam iš toliau nurodytų vaidmenų, egzemplioriaus:

- Elektroninės ataskaitos kūrėjas
- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Rekomenduojame atlikti veiksmus parametrų [ER duomenų šaltinių, kurie yra suskaičiuoto lauko tipo straipsnis, palaikymo dalyje](er-calculated-field-type.md). Jei tuos veiksmus jau atlikote, galite praleisti tolesniame skyriuje **ER konfigūracijų importavimas į RCS** aprašytus veiksmus.

## <a name="import-er-configurations-into-rcs"></a>ER konfigūracijų importavimas į RCS

Atsisiųskite ir saugokite šias ER konfigūracijas.

| **Turinio aprašas**                        | **Failo vardas**                                        |
|------------------------------------------------|------------------------------------------------------|
| **ER duomenų modelio** konfigūracijos pavyzdžio failas    | [Parametrizuotų kvietimų mokymo modelis.versija.1.xml](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| **ER metaduomenų** konfigūracijos pavyzdžio failas      | [Parametrizuotų kvietimų mokymo metaduomenys.versija.1.xml](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| **ER modelio susiejimo** konfigūracijos pavyzdžio failas | [Parametrizuotų kvietimų mokymo susiejimas.versija.1.1.xml](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| **ER formato** konfigūracijos pavyzdys             | [Parametrizuotų kvietimų mokymo formatas.versija.1.1.xml](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

Tada prisijunkite prie savo RCS egzemplioriaus.

Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūraciją. Norėdami užbaigti šią procedūrą, [turite](tasks/er-configuration-provider-mark-it-active-2016-11.md) atlikti konfigūracijos teikėjo kūrimo veiksmus ir pažymėti juos kaip aktyvų RCS straipsnį.

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

    ![Keli ER formato lygiai; formatas, skirtas sužinoti parametruotus skambučius.](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Skirtuke **Susiejimas** išplėskite elementus **Modelis**, **Duomenys** ir **Suvestinė**.

    Duomenų šaltinis **Model.Data.Summary** pateikia mokesčių operacijų sąrašą. Šių operacijų suvestinė pateikiama pagal mokesčio kodą. Naudojant šį duomenų šaltinį, apskaičiuotas laukas **Model.Data.Summary.Level** sukonfigūruotas taip, kad jame būtų pateikiamas kiekvieno apibendrinto įrašo apmokestinimo lygio kodas. Pasirinkus mokesčio kodą, kurį vykdymo metu galima gauti iš duomenų šaltinio **Model.Data.Summary**, apskaičiuotame lauke kaip tekstinė reikšmė pateikiamas apmokestinimo lygio kodas (**Įprastas**, **Sumažintas**, **Joks** arba **Kita**). Apskaičiuotas laukas **Model.Data.Summary.Level** naudojamas norint filtruoti duomenų šaltinio **Model.Data.Summary** įrašus ir filtruotus duomenis įvesti kiekviename XML elemente, vaizduojančiame apmokestinimo lygį – naudojami laukai **Model.Data2.Level1**, **Model.Data2.Level2** ir **Model.Data2.Level3**.

    ![Duomenų šaltinis Model.Data.Summary pateikia mokesčių operacijų sąrašą.](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Apskaičiuotas laukas **Model.Data.Summary.Level** sukonfigūruotas taip, kad jame būtų ER reiškinys. Mokesčių kodai (**„VAT19”**, **„InVAT19”**, **„VAT7”**, **„InVAT7”**, **„THIRD”** ir **„InVAT0”**) yra užprogramuoti į šią konfigūraciją. Todėl šis ER formatas priklauso nuo juridinio subjekto, kuriam šie mokesčių kodai buvo sukonfigūruoti.

    ![Model.Data.Summary.Level apskaičiuotas laukas su užkoduotais mokesčių kodais.](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

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

    ![Naujas įrašas formatų išvardijimo puslapyje.](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Kadangi nurodydami nuo juridinio subjekto priklausančius mokesčių kodų rinkinius įmonių vartotojai gali naudoti skirtingas kalbas, rekomenduojame šio išvardijimo reikšmes išversti į kalbas, kurios yra sukonfigūruotos kaip pageidaujamos tų vartotojų kalbos programoje „Finance“.

14. Pasirinkite įrašą **Apmokestinimo nėra**.
15. Spustelėkite lauką **Žyma**.
16. Pasirinkite **Versti**.
17. Srities **Teksto vertimas** lauke **Žymos ID** įveskite **„LBL_LEVELENUM_NO”**.
18. Lauke **Tekstas numatytąja kalba** įveskite **Apmokestinimo nėra**.
19. Lauke **Kalba** pasirinkite **LT**.
20. Lauke **Išverstas tekstas** įveskite **Apmokestinimo nėra**.
21. Pasirinkite **Versti**.

    ![Teksto vertimo skaidrė.](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Pasirinkite **Įrašyti**.
23. Uždarykite puslapį **Formatų išvardijimai**.

### <a name="add-a-new-lookup-data-source"></a>Naujo peržvalgos duomenų šaltinio įtraukimas

Toliau įtrauksite naują duomenų šaltinį ir nurodysite, kaip įmonių vartotojai nustatys nuo juridinio subjekto priklausančias taisykles, kad būtų galima atpažinti teisingą kiekvieno apibendrinto operacijos įrašo apmokestinimo lygį.

1.  Skirtuke **Susiejimas** pasirinkite **Įtraukti**.
2.  Pasirinkite **Formatų išvardijimas\Peržvalga**.

    Ką tik nustatėte, kad kiekviena taisyklė, kurią įmonių vartotojai nurodo apmokestinimo lygiui atpažinti, pateiks ER formato išvardijimo reikšmę. Atkreipkite dėmesį, kad duomenų šaltinio tipą **Peržvalga** galima pasiekti ne tik bloke **Formatų išvardijimas**, bet ir blokuose **Duomenų modelis** ir **„Dynamics 365 for Operations“**. Todėl naudojant ER duomenų modelių ir programų išvardijimus, galima nurodyti grąžinamų to tipo duomenų šaltinių reikšmių tipą. Daugiau informacijos apie **Peržvalgos** duomenų šaltinius rasite [Peržvalgos duomenų šaltinių konfigūravimas naudoti ER programai būdingų parametrų funkciją](er-lookup-data-sources.md).
    
3.  Lauke **Pavadinimas** įveskite **Išrinkiklis**.
4.  Lauke **Formatų išvardijimas** pasirinkite **Apmokestinimo lygių sąrašas**.

    Jūs nurodėte, kad kiekvienai taisyklei, nurodytai šiame duomenų šaltinyje, verslo vartotojas kaip grąžinamą reikšmę turi pasirinkti vieną iš formatų išvardijimo **Apmokestinimo lygių sąrašas** reikšmių.
    
5.  Pasirinkite **Redaguoti peržvalgą**.
6.  Pasirinkite **Stulpeliai**.
7.  Išplėskite elementą **Modelis**.
8.  Išplėskite elementą **Duomenys**.
9.  Išplėskite elementą **Mokestis**.
10. Pasirinkite elementą **Model.Data.Tax.Code**.
11. Pasirinkite mygtuką **Įtraukti** (rodyklę dešinėn).

    ![Stulpelių skaidrė.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Ką tik nustatėte, kad kiekvienai taisyklei, šiame duomenų šaltinyje nurodytai apmokestinimo lygiui atpažinti, įmonės vartotojas kaip sąlygą turi pasirinkti vieną iš mokesčių kodų. Mokesčių kodų, kuriuos įmonės vartotojas gali pasirinkti, sąrašas bus pateikiamas duomenų šaltinyje **Model.Data.Tax**. Kadangi šiame duomenų šaltinyje yra laukas **Pavadinimas**, įmonės vartotojui pateikiamoje peržvalgoje bus rodomas kiekvienos mokesčio kodo reikšmės pavadinimas.
    
12. Pasirinkite **Gerai**.

    ![Peržvalgos konstruktoriaus puslapis.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Įmonių vartotojai kaip šio duomenų šaltinio įrašus gali įtraukti kelias taisykles. Kiekvienas įrašas bus sunumeruotas pagal eilutės kodą. Taisyklės bus vertinamos eilutės numerio didėjimo tvarka.

    Kadangi šiame peržvalgos duomenų šaltinyje kaip taisyklių sąlygą pasirinkote lauką **Mokesčio kodas** ir kadangi **Mokesčio kodas** yra nustatytas kaip duomenų tipo **Eilutė** laukas, vykdymo metu kiekviena taisyklė bus vertinama mokesčio kodą, perduotą į duomenų šaltinį, palyginant su mokesčio kodu, kuris nustatytas šiame duomenų šaltinio įraše.

    Kai randama taisyklė, tenkinanti sukonfigūruotą sąlygą, šis duomenų šaltinis pateikia taisyklės, kuri apibrėžta lauke **Peržvalgos rezultatas**, peržvalgos reikšmę. Jei taisyklių nerandama, pateikiama išimtis, vartotojui pranešanti, kad dabartinis duomenų šaltinis negali pateikti teisingos reikšmės.

13. Pasirinkite **Įrašyti**.
14. Uždarykite puslapį **Peržvalgos konstruktorius**.
15. Pasirinkite **Gerai**.

    Atkreipkite dėmesį, kad įtraukėte naują duomenų šaltinį, kuris apmokestinimo lygį pateiks kaip formatų išvardijimo **Apmokestinimo lygių sąrašas** reikšmę bet kuriam mokesčio kodui, į duomenų šaltinį perduodamam kaip duomenų tipo **Eilutė** parametro **Kodas** argumentui.
    
    ![Formato kūrimo puslapis su nauju duomenų šaltiniu.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Sukonfigūruotų taisyklių vertinimas priklauso nuo laukų, kurie buvo pasirinkti tų taisyklių sąlygoms apibrėžti, duomenų tipo. Pasirinkus lauką, kuris sukonfigūruotas kaip duomenų tipo **Skaitinis** arba **Data** laukas, kriterijai skirsis nuo anksčiau aprašytų duomenų tipo **Eilutė** kriterijų. Naudojant laukus **Skaitinis** ir **Data**, taisyklę reikia nurodyti kaip reikšmių intervalą. Tada taisyklės sąlyga bus laikoma įvykdyta, kai į duomenų šaltinį perduota reikšmė bus sukonfigūruotame intervale.
    
    Tolesnėje iliustracijoje pateikiamas šio tipo sąrankos pavyzdys. Be duomenų tipo **Eilutė** lauko **Model.Data.Tax.Code** peržvalgos duomenų šaltinio sąlygoms nurodyti taip pat naudojamas duomenų tipo **Realus** laukas **Model.Tax.Summary.Base**.
    
    ![Peržvalgos konstruktoriaus puslapis su papildomais stulpeliais.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

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
5.  Srities **Teksto vertimas** lauke **Žymos ID** įveskite **„LBL_SELECTOR_DS”**.
6.  Lauke **Tekstas numatytąja kalba** įveskite **Mokesčio lygio pasirinkimas pagal mokesčio kodą**.
7.  Lauke **Kalba** pasirinkite **LT**.
8.  Lauke **Išverstas tekstas** įveskite **Mokesčio lygio pasirinkimas pagal mokesčio kodą**.
9.  Pasirinkite **Versti**.
10. Pasirinkite **Gerai**.

    ![Duomenų šaltinio ypatybės išklydus.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Naujo lauko sukonfigūruotai peržvalgai naudoti įtraukimas

1.  Išplėskite elementą **Model.Data**.
2.  Pasirinkite elementą **Model.Data.Summary**.
3.  Pasirinkite **Įtraukti**.
4.  Pasirinkite **Funkcijos/Apskaičiuotas laukas**.
5.  Lauke **Pavadinimas** įveskite **LevelByLookup**.
6.  Pasirinkite **Redaguoti formulę**.
7.  **Lauke Formulė** įveskite **Model.Selector(Model.Data.Summary.Code)**.
8.  Pasirinkite **Įrašyti**.

    ![Model.Selector(Model.Data.Summary.Code) įtraukimas į formulės konstruktoriaus puslapį.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Uždarykite puslapį **Formulės rengyklė**.
10. Pasirinkite **Gerai**.

    ![Formato kūrimo puslapis su nauja įtraukta formule.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

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

    ![ER operacijų dizaino įrankio puslapis.](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Atkreipkite dėmesį, kad lauko **„Model.Data.Summary.Level”** išraiška dabar grąžins apmokestinimo lygį pagal dabartinio įrašo mokesčio kodą ir taisyklių rinkinį, kurį įmonės vartotojas sukonfigūruoja peržvalgos duomenų šaltinyje **„Model.Data.Selector”**.
    
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

1.  Konfigūracijos medyje pasirinkite elementą **Mokymosi formatas, kaip peržvelgti LE duomenis**.
2.  „FastTab“ elemente **Versijos** pasirinkite įrašą, kurio būsena yra **Baigtas**.
3.  Pasirinkite **Keitimas**.
4.  Pasirinkite **Eksportuoti kaip XML failą**.
5.  Pasirinkite **Gerai**.
6.  Žiniatinklio naršyklė atsiunčia failą **Mokymosi formatas, kaip peržvelgti LE duomenis.xml**. Šį failą išsaugokite vietiniame įrenginyje.

Šio skyriaus veiksmus pakartokite su pirminiais formato **Mokymosi formatas, kaip peržvelgti LE duomenis** elementais ir vietiniame sistemoje išsaugokite šiuos failus:

-   Parametrizuotų iškvietų mokymo formatas.xml
-   Parametrizuotų iškvietų mokymo susiejimas.xml
-   Parametrizuotų iškvietų mokymo modelis.xml

Norėdami sužinoti **, kaip naudoti sukonfigūruotą formatą ir sužinoti, kaip ieškoti LE** duomenų ER formato siekiant nustatyti nuo juridinio subjekto priklausomus mokesčių kodų rinkinius mokesčių operacijoms pagal skirtingus apmokestinimo lygius, atlikite veiksmus, [nurodytus skyriuje Nustatyti juridinio subjekto straipsnio ER](er-app-specific-parameters-set-up.md) formato parametrus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[ER formato parametrų nustatymas kiekvienam juridiniam subjektui](er-app-specific-parameters-set-up.md)

[Peržvalgos duomenų šaltinių konfigūravimas, kad būtų galima naudoti ER programai būdingų parametrų funkciją](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
