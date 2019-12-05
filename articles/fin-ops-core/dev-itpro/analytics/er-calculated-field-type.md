---
title: Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti ER duomenų šaltinių apskaičiuoto lauko tipą.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f331401f8d191243f72961333e4f1dbe84d0be5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771334"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip galima kurti elektroninių ataskaitų (ER) duomenų šaltinį naudojant **apskaičiuoto lauko** tipą. Šiame duomenų šaltinyje gali būti naudojama ER išraiška, kurią vykdymo metu galima kontroliuoti nurodant parametro argumentų reikšmes, kurios sukonfigūruotos šio duomenų šaltinio kvietimui. Konfigūruodami tokio duomenų šaltinio parametrizuotus kvietimus, galite naudoti vieną duomenų šaltinį daugeliui susiejimų, o tai sumažina bendrą duomenų šaltinių, kuriuos reikia sukonfigūruoti ER modelio susiejimams arba ER formatams, skaičių. Be to, taip supaprastinamas sukonfigūruotas komponentas, o tai sumažina priežiūros išlaidas ir naudojimo išlaidas kitiems vartotojams.

## <a name="prerequisites"></a>Būtinieji komponentai
Norint įvykdyti šios temos pavyzdžių užduotis, reikia toliau nurodytų prieigų.

- Prieiga prie vieno iš šių vaidmenų:

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

- Prieiga prie „Regulatory Configuration Services“ (RCS), kuris sukurtas tam pačiam kaip ir „Finance and Operations“ nuomotojui vienam iš toliau nurodytų vaidmenų:

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

Iš [„Microsoft“ atsisiuntimo centro](https://go.microsoft.com/fwlink/?linkid=874684) atsisiųskite suspaustą (suglaudintą) failą **Apskaičiuoto lauko tipo ER duomenų šaltinių parametrizuotų kvietimų palaikymas**. Jame yra nurodytos ER konfigūracijos, kurias reikia išskleisti ir saugoti vietoje.

| **Turinys**                           | **Failo vardas**                                        |
|---------------------------------------|------------------------------------------------------|
| ER duomenų modelio konfigūracijos pavyzdys    | Parametrizuotų kvietimų mokymo modelis.versija.1.xml     |
| ER metaduomenų konfigūracijos pavyzdys      | Parametrizuotų kvietimų mokymo metaduomenys.versija.1.xml  |
| ER modelio susiejimo konfigūracijos pavyzdys | Parametrizuotų kvietimų mokymo susiejimas.versija.1.1.xml |
| ER formato konfigūracijos pavyzdys        | Parametrizuotų kvietimų mokymo formatas.versija.1.1.xml  |

## <a name="sign-in-to-your-rcs-instance"></a>Prisijunkite prie savo RCS egzemplioriaus
Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc.“ konfigūraciją. Pirmiausia naudodami RCS turite atlikti tolesnius procedūros [Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius](tasks/er-configuration-provider-mark-it-active-2016-11.md) veiksmus.

1. Numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Importuokite atsisiųstas konfigūracijas į RCS tokia tvarka: duomenų modelis, metaduomenys, modelio susiejimas, formatas. Atlikite šiuos veiksmus su kiekviena ER konfigūracija:

    1. Pasirinkite **Keitimas.**
    2. Pasirinkite **Įkelti iš XML failo**.
    3. Pasirinkite **Naršyti**, o tada pasirinkite reikiamą ER konfigūraciją XML formatu.
    4. Pasirinkite **Gerai.**

## <a name="review-the-provided-er-solution"></a>Pateikto ER sprendimo peržiūra

### <a name="review-model-mapping"></a>Modelio susiejimo peržiūra

1. Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.
2. Pasirinkite **Parametrizuotų kvietimų mokymo susiejimas**.
3. Pasirinkite **Dizaino įrankis**.
4. Pasirinkite **Dizaino įrankis**.  
   
    Šis ER modelio susiejimas sukurtas toliau nurodytiems veiksmams:

    - Pateikti mokesčių kodų (duomenų šaltinis **Mokestis**), įrašytų lentelėje **TaxTable**, sąrašą.
    - Pateikti mokesčių operacijų (duomenų šaltinis **Operacija**), įrašytų lentelėje **TaxTrans**, sąrašą.
    
        - Sugrupuoti pateiktų operacijų sąrašą (duomenų šaltinis **Gr**) pagal mokesčio kodą.
        - Apskaičiuoti sugrupuotas operacijas po verčių agregavimo pagal mokesčio kodą.

            - Mokesčio bazinių verčių suma.
            - Mokesčio verčių suma.
            - Mažiausioji taikomo mokesčio tarifo vertė.

    Modelio susiejimas šioje konfigūracijoje taikomas kaip bazinis duomenų modelis visiems šiam modeliui sukurtiems ir vykdomiems „Finance and Operations“ ER formatams. Todėl duomenų šaltinių **Mokestis** ir **Gr** turinys tampa prieinamas ER formatams, pvz., abstrakčių duomenų šaltiniams.

    ![Modelio susiejimo konstruktoriaus puslapis, kuriame rodomi duomenų šaltiniai „Mokestis“ ir „Gr“](media/er-calculated-field-type-01.png)

5.  Uždarykite puslapį **Modelio susiejimo dizaino įrankis**.
6.  Uždarykite puslapį **Modelio susiejimas**.

### <a name="review-format"></a>Formato peržiūra

1. Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.
2. Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.
3. Pasirinkite **Dizaino įrankis**. Šis ER formatas sukurtas toliau nurodytiems veiksmams:

    - Sugeneruoti mokesčių ataskaitą XML formatu.
    - Mokesčių ataskaitoje pateiki šiuos apmokestinimo lygius: „reguliarus“, „sumažintas“ ir „nėra“.
    - Pateikti įvairią skirtingo išsamumo kiekvieno apmokestinimo lygio informaciją.

    ![Formato dizaino įrankio puslapis](media/er-calculated-field-type-02.png)

4. Pasirinkite **Susiejimas**.
5. Išskleiskite elementus **Modelis**, **Duomenys** ir **Suvestinė**. 

    Apskaičiuotame lauke **Model.Data.Summary.Level** yra išraiška, kuri grąžina apmokestinimo lygio kodą (**Reguliarus**, **Sumažintas**, **Nėra** arba **Kita**) kaip bet kurio mokesčio kodo tekstinę reikšmę, kurią galima gauti iš duomenų šaltinio **Model.Data.Summary** vykdymo metu.

    ![Formato konstruktoriaus puslapis, kuriame pateikiama informacija apie duomenų modelį „Parametrizuotų kvietimų mokymo modelis“](media/er-calculated-field-type-03.png)

6. Išplėskite elementą **Model**.**Data2**.
7. Išplėskite elementą **Model**.**Data2.Summary2**.
   
    Duomenų šaltinis **Model**.**Data2.Summary2** yra sukonfigūruotas taip, kad duomenų šaltinio **Model.Data.Summary** operacijų informacija būtų grupuojama pagal apmokestinimo lygį (kurį grąžina apskaičiuotas laukas **Model.Data.Summary.Level**) ir būtų skaičiuojami agreguoti duomenys.

    ![Formato konstruktoriaus puslapis, kuriame pateikiama duomenų šaltinio Model.Data2.Summary2 informacija](media/er-calculated-field-type-04.png)

8. Peržiūrėkite apskaičiuotus laukus **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ir **Model**.**Data2.Level3.** Šie apskaičiuoti laukai naudojami filtruoti įrašų sąrašui **Model**.**Data2.Summary2** ir pateikia tik įrašus, atitinkančius konkretų apmokestinimo lygį.
9. Uždarykite puslapį **Formato dizaino įrankis**.

## <a name="create-a-derived-format"></a>Sukurkite išvestinį formatą
Pateiktą formatą galite patobulini į filtrą įtraukdami vieną apskaičiuotą lauką, kad filtravimas būtų atliekamas pagal reikiamą apmokestinimo lygį, o ne naudojant tris esamus laukus: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ir **Model**.**Data2.Level3**. Reikiamą apmokestinimo lygį galima nurodyti vietoje, kurioje bus kviečiamas šis naujas apskaičiuotas laukas.

1. Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.
2. Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.
3. Pasirinkite **Kurti konfigūraciją**.
4. Pasirinkite **Kildinti iš pavadinimo: parametrizuotų kvietimų mokymo formatas, „Microsoft“**.
5. Lauke **Pavadinimas** įveskite **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.
6. Pasirinkite **Kurti konfigūraciją.**

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Konfigūruokite parametrizuotą apskaičiuotą lauką, kuriame pateikiamas įrašų sąrašas

### <a name="start-adding-a-new-calculated-field"></a>Pradėkite naujai apskaičiuoto lauko pridėjimo veiksmus

1. Pasirinkite **Dizaino įrankis**.
2. Pasirinkite **Išplėsti / sutraukti**, kad išplėstumėte visus formato elementus.
3. Pasirinkite **Susiejimas**.
4. Išplėskite elementą **Modelis**.
5. Pasirinkite elementą **Modelis.Duomenys2**.
6. Pasirinkite **Įtraukti**.
7. Pasirinkite **Funkcijos\\Apskaičiuotas laukas**.
8. Lauke **Pavadinimas** įveskite **Lygiai**.
9. Pasirinkite **Redaguoti formulę**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Nurodykite apskaičiuoto lauko pridėjimo parametrą

1. Pasirinkite **Parametrai**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite **Mokesčio lygis**.
4. Lauke **Tipas** pasirinkite **Eilutė**.

    Nurodant parametro argumento tipą, galima naudoti tik primityviuosius duomenų tipus. Todėl šiam tikslui negalima naudoti tipų **Įrašų sąrašas**, **Įrašas** ir **Išvardijimas**.

    Didžiausias parametrų, kuriuos galima nurodyti vienam apskaičiuotam laukui, skaičius yra 8.

    ![Duomenų šaltinių sąrašo parametras](media/er-calculated-field-type-05.png)

5. Pasirinkite **Gerai**.

Pridėdami šį parametrą, nurodote sąlygą, kuri turi būti taikoma šiam apskaičiuojamam laukui iškviesti. Kai kviečiate šį apskaičiuotą lauką, turite nurodyti parametro **Mokesčio lygis** argumentą, kuris pateikiamas formatu **Eilutė**.

   Įsitikinkite, kad parametrus nurodote tik tiems apskaičiuotiems laukams, kurie yra konteineryje (**Įrašų sąrašas**, **Įrašas** arba **Konteineris**).

   Sukonfigūruotas parametras yra pasiekiamas šio apskaičiuoto lauko duomenų šaltinių sąraše. Parametrą į sukonfigūruotą išraišką galite įtraukti pasirinkdami **Įtraukti duomenų šaltinį.**

   ![Duomenų šaltinio laukai](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Nurodykite apskaičiuoto lauko įtraukimo išraišką

1. Laukė **Formulė** įveskite: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Iš duomenų šaltinių sąrašo pasirinkite parametrą **Mokesčio lygis**.
3. Pasirinkite **Įtraukti duomenų šaltinį**.
4. Lauke **Formulė** užbaikite išraišką:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Mokesčio lygis')**

5. Pasirinkite **Įrašyti**.

    ![Duomenų šaltinio lauko informacija](media/er-calculated-field-type-07.png)

6. Uždarykite puslapį **Formulės konstruktorius**.

### <a name="finish-adding-a-new-calculated-field"></a>Užbaikite naujo apskaičiuoto lauko įtraukimą

- Pasirinkite **Gerai**.

Puslapyje **Formato kūrimo įrankis** sukonfigūruotam parametrizuotam apskaičiuotam laukui **Lygiai** reikia argumento **Eilutė**.

![Išplėstas apskaičiuoto lauko lygių sąrašas](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Naudokite sukonfigūruotą apskaičiuotą lauką formato elementams susieti

1. Pasirinkite **Model.Data2.Levels**, kad pasirinktumėte sukonfigūruotą apskaičiuotą lauką.
2. Pasirinkite formato elementą **Statement.Taxation.Regular**.
3. Pasirinkite **Susieti**.
4. Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level1** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.

    Taikomas susiejimas sukurtas kaip parametrizuoto apskaičiuoto lauko kvietimas. Esant numatytiesiems nustatymams, susieto formato elemento pavadinimas yra naudojamas kaip parametrizuoto apskaičiuoto lauko argumentas esant šioms sąlygoms:

      - Apskaičiuotas laukas sukonfigūruotas, kad naudotų vieną parametrą.
      - Šio parametro duomenų tipas nurodytas kaip **Eilutė.**

    Kai susieto formato elemento pavadinimas yra tuščias, taikomame susiejime naudojamas šio elemento duomenų šaltinio pavadinimas.

5. Pasirinkite formato elementą **Statement.Taxation.Reduced**.
6. Pasirinkite **Susieti**.
7. Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level2** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.
8. Pasirinkite formato elementą **Statement.Taxation.None**.
9. Pasirinkite **Susieti**.
10. Pasirinkite **Taip**, kad patvirtintumėte naudojamo duomenų šaltinio **Level3** pakeitimą nauju duomenų šaltiniu **Lygiai** visuose pasirinkto formato elemento įdėtuosiuose formato elementuose.

   Kai nurodote XML elemento, atitinkančio apmokestinimo lygį, parametrizuoto apskaičiuoto lauko argumentą (pavyzdžiui, **Model.Data2.Levels("Reduced")** kaip tekstinę reikšmę), jums nebereikia to atlikti su įdėtaisiais XML atributais – susiejimuose bus automatiškai paveldėta pirminiame lygyje nurodyta argumento reikšmė (**Model.Data2.Levels.aggregated.Base**, ne **Model.Data2.Levels("Reduced").aggregated.Base**).

Negalimi pasikartojantys parametrizuoto apskaičiuoto lauko kvietimai.

Galite pasirinkti **Redaguoti formulę**ir pakeisti pasirinkto susiejimo parametrizuoto apskaičiuoto lauko numatytąjį argumentą. Jei šio argumento nėra, vykdymo metu gali kilti klaidų – vartotojai informuojami apie tokią situaciją naudojamo formato patikrinimo metu.

![Tikrinimo įspėjimo pranešimas](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Sukonfigūruokite parametrizuotą apskaičiuotą lauką, kuris pateikia įrašą
Kai parametrizuotas apskaičiuotas laukas pateikia įrašą, turite leisti atskirų šio įrašo laukų susiejimą su elementais. Tokiais atvejais nebus pirminio susiejimo su argumento reikšme parametrizuoto apskaičiuoto lauko iškvietimui – šią reikšmę reikia nurodyti vieno įrašo lauko susiejime.

### <a name="start-adding-a-new-calculated-field"></a>Pradėkite naujai apskaičiuoto lauko pridėjimo veiksmus

1. Pasirinkite elementą **Modelis.Duomenys2**.
2. Pasirinkite **Įtraukti**.
3. Pasirinkite **Funkcijos\\Apskaičiuotas laukas**.
4. Lauke **Pavadinimas** įveskite **LevelRecord**.
5. Pasirinkite **Redaguoti formulę**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Nurodykite apskaičiuoto lauko pridėjimo parametrą

1. Pasirinkite **Parametrai**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite **Mokesčio lygis**.
4. Lauke **Tipas** pasirinkite **Eilutė**.
5. Pasirinkite **Gerai**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Nurodykite apskaičiuoto lauko įtraukimo išraišką

1. Lauke **Formulė** įveskite šią išraišką:  
    
    **FIRSTORNULL(\@.Levels(**

2. Pasirinkite parametrą **Apmokestinimo lygis**.
3. Pasirinkite **Įtraukti duomenų šaltinį**.
4. Lake **Formulė** papildykite atliekant 1 veiksmą įvestą išraišką įvesdami **'Apmokestinimo lygis'))**, kad galutinė išraiška būtų tokia:  
    
    **FIRSTORNULL(\@.Levels('Apmokestinimo lygis'))**

5. Pasirinkite **Įrašyti**.
6. Uždarykite puslapį **Formulės konstruktorius**.

### <a name="finish-adding-a-new-calculated-field"></a>Užbaikite naujo apskaičiuoto lauko įtraukimą

-   Pasirinkite **Gerai**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Naudokite sukonfigūruotą apskaičiuotą lauką formato elementams susieti

1. Išplėskite **Model.Data2.LevelRecord**, kad pasirinktumėte sukonfigūruotą apskaičiuotą lauką.
2. Išplėskite sukonfigūruoto apskaičiuoto lauko konteinerį **Model.Data2.LevelRecord.aggregated**.
3. Pasirinkite lauką **Model.Data2.LevelRecord.aggregated.Base**.
4. Pasirinkite formato elementą **Statement.Taxation.None**.
5. Pasirinkite **Atsieti**.
6. Pasirinkite formato elementą **Statement.Taxation.None.Base**.
7. Pasirinkite **Susieti**.
8. Pasirinkite **Redaguoti formulę**.
9. Pakeiskite išraišką į **Model.Data2.LevelRecord("None").aggregated.Base**.

![Atnaujinta išraiška](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Pašalinkite nenaudojamus apskaičiuotus laukus

1. Pasirinkite **Model.Data2.Level1**.
2. Pasirinkite **Naikinti**.
3. Pasirinkite **Model.Data2.Level2**.
4. Pasirinkite **Naikinti**.
5. Pasirinkite **Model.Data2.Level3**.
6. Pasirinkite **Naikinti**.
7. Pasirinkite **Įrašyti**.

  > [!NOTE]
  > Susiedami formatą jūs pakartotinai kelis kartus panaudojote tą patį apskaičiuotą lauką **Model.Data2.Levels**. Daug paprasčiau naudoti ir tvarkyti vieną apskaičiuojamą lauką, o ne kelis panašius laukus.

8. Uždarykite puslapį **Formato dizaino įrankis**.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Užbaikite pakoreguotą išvestinio formato versiją

1. „FastTab“ elemente **Versijos** pasirinkite **Keisti būseną**.
2. Pasirinkite **Baigti**.

## <a name="export-completed-version-of-a-derived-format"></a>Eksportuokite užbaigtą išvestinio formato versiją

1. Konfigūracijų medyje pasirinkite formatą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.
2. „FastTab“ elemente **Versijos** pasirinkite 1.1.1 užbaigtą versiją.
3. Pasirinkite **Keitimas**.
4. Pasirinkite **Eksportuoti kaip XML failą**.
5. Atsisiųstą konfigūraciją išsaugokite vietoje XML formatu.

## <a name="test-er-formats"></a>Patikrinkite ER formatus 
Galite paleisti pradinį ir patobulintą ER formatus, kad įsitikintumėte, jog sukonfigūruoti parametrizuoti apskaičiuoti laukai veikia tinkamai.

### <a name="import-er-configurations"></a>Importuokite ER konfigūracijas
Peržiūrėtas konfigūracijas galite importuoti iš RCS naudodami **RCS** tipo ER saugyklą. Jei jau atlikote temoje [Elektroninių ataskaitų (ER) konfigūracijų importavimas iš „Regulatory Configuration Services“ (RCS)](rcs-download-configurations.md) aprašytus veiksmus, naudodami sukonfigūruotą ER saugyklą į savo aplinką importuokite prieš tai šioje temoje aptartas konfigūracijas. Priešingu atveju atlikite toliau nurodytus veiksmus:

1. Pasirinkite įmonę **DEMF** ir numatytoje ataskaitų srityje pasirinkite **Elektroninės ataskaitos**.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Importuokite iš „Microsoft“ atsisiuntimo centro gautas konfigūracijas tokia tvarka: duomenų modelis, modelio susiejimas, formatas. Atlikite šiuos veiksmus su kiekviena ER konfigūracija:

    1. Pasirinkite **Keitimas.**
    2. Pasirinkite **Įkelti iš XML failo**.
    3. Pasirinkite **Naršyti**, kad galėtumėte pasirinkti reikiamą ER konfigūraciją XML formatu.
    4. Pasirinkite **Gerai**.

4. Importuokite eksportuotą iš RCS formato **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)** 1.1.1 baigtą versiją:

    1. Pasirinkite **Keitimas.**
    2. Pasirinkite **Įkelti iš XML failo**.
    3. Pasirinkite **Naršyti**, kad pasirinktumėte vietoje saugomą XML formato failą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.
    4. Pasirinkite **Gerai**.

### <a name="run-er-formats"></a>Vykdykite ER formatus

1. Konfigūracijos medyje išplėskite elemento **Parametrizuotų kvietimų mokymo modelis** turinį.
2. Pasirinkite **Parametrizuotų kvietimų mokymo formatas**.
3. Viršutinėje juostoje pasirinkite **Vykdyti**.
4. Įrašykite vietoje sugeneruotą išvestį.
5. Pasirinkite elementą **Parametrizuotų kvietimų mokymo formatas (pasirinktinis)**.
6. Viršutinėje juostoje pasirinkite **Vykdyti**.
7. Vietoje įrašykite sugeneruotą išvestį. 
8. Palyginkite sugeneruotų išvesčių turinį.

## <a name="additional-resources"></a>Papildomi ištekliai
[Elektroninių ataskaitų (ER) formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)
