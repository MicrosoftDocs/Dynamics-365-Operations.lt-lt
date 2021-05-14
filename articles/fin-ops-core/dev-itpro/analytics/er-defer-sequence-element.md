---
title: Sekos elementų ER formatais vykdymo atidėjimas
description: Šioje temoje paaiškinama, kaip atidėti sekos elemento elektroninių ataskaitų (ER) formatu vykdymą.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a7904924d1c2830287e26eb9fb71bd9a03f210d9
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944514"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>Sekos elementų ER formatais vykdymo atidėjimas

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Peržiūrėti

Galite naudoti [elektroninių ataskaitų (ER)](general-electronic-reporting.md) sistemos operacijų dizaino įrankį, kad [sukonfigūruotumėte](tasks/er-format-configuration-2016-11.md) ER sprendimo, naudojamo siunčiamiems dokumentams teksto formatu generuoti, [formato komponentą](general-electronic-reporting.md#FormatComponentOutbound). Sukonfigūruoto formato komponento hierarchinė struktūra susideda iš įvairių tipų formato elementų. Šie formato elementai naudojami sugeneruotiems dokumentams užpildyti reikiama informacija vykdymo metu. Numatyta, kad kai vykdote ER formatą, formato elementai vykdomi tokia pačia tvarka, kokia jie pateikiami formato hierarchijoje: po vieną, iš viršaus į apačią. Tačiau kūrimo metu galite pakeisti bet kurių sukonfigūruoto formato komponento sekos elementų vykdymo tvarką.

Įjungę sekos elemento sukonfigūruotu formatu parinktį <a name="DeferredSequenceExecution"></a>**Atidėtas vykdymas**, galite atidėti (nukelti) to elemento vykdymą. Šiuo atveju elementas nevykdomas, kol neįvykdomi visi kiti jo pirminio elemento elementai.

Norėdami sužinoti daugiau apie šią funkciją, atlikite šioje temoje esantį pavyzdį.

## <a name="limitations"></a>Apribojimai

Parinktis **Atidėtas vykdymas** taikoma tik sekos elementams, kurie sukonfigūruoti ER formatui, naudojamam **siunčiamiems** dokumentams teksto formatu generuoti.

Parinktis **Atidėtas vykdymas** netaikoma sekoms, kurios buvo sukonfigūruotos kaip apkarpytos sekos, kuriose didžiausias ilgis yra ribotas.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Pavyzdys: sekos elemento ER formatu vykdymo atidėjimas

Toliau pateikiamuose veiksmuose paaiškinama, kaip vartotojas, kuriam priskirtas Sistemos administratoriaus arba Elektroninės ataskaitos funkcijų konsultanto [vaidmuo](../sysadmin/tasks/assign-users-security-roles.md), gali konfigūruoti ER formatą, kuriame yra sekos elementas, kai vykdymo tvarka skiriasi nuo tvarkos formato hierarchijoje.

Šiuos veiksmus galima atlikti įmonėje **USMF** programoje „Microsoft Dynamics 365 Finance“.

### <a name="prerequisites"></a>Būtinieji komponentai

Norėdami atlikti šį pavyzdį, turite turėti prieigą prie įmonės **USMF** programoje „Finance“ ir vieną iš tolesnių vaidmenų.

- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Jei dar nebaigėte pavyzdžio, pateikiamo temoje [XML elementų ER formatais vykdymo atidėjimas](er-defer-xml-element.md#Example), atsisiųskite šias ER sprendimo pavyzdžio [konfigūracijas](general-electronic-reporting.md#Configuration).

| Turinio aprašas            | Failo pavadinimas |
|--------------------------------|-----------|
| ER duomenų modelio konfigūracija    | [Modelis, norint sužinoti apie atidėtus elementus.1.versija.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| ER modelio susiejimo konfigūracija | [Susiejimas, norint sužinoti apie atidėtus elementus.1.1.versija.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Prieš pradėdami, taip pat turite atsisiųsti ir įrašyti šią ER sprendimo pavyzdžio konfigūraciją.

| Turinio aprašas     |Failo pavadinimas |
|-------------------------|----------|
| ER formato konfigūracija | [Formatas, norint sužinoti apie atidėtas sekas.1.1.versija.xml](https://download.microsoft.com/download/0/f/5/0f55c341-8285-4d92-a46d-475d9a010927/Formattolearndeferredsequences.version.1.1.xml) |

### <a name="import-the-sample-er-configurations"></a>Pavyzdinių ER konfigūracijų importavimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Puslapyje **Konfigūracijos**, jei konfigūracijos **Modelis, norint sužinoti apie atidėtus elementus** nėra konfigūracijos medyje, importuokite ER duomenų modelio konfigūraciją.

    1. Pasirinkite **Keitimas** ir pasirinkite **Įkelti iš XML failo**.
    2. Pasirinkite **Naršyti**, suraskite ir pasirinkite failą **Modelis, norint sužinoti apie atidėtus elementus.1.xml**, tada pasirinkite **Gerai**.

4. Jei konfigūracijos **Susiejimas, norint sužinoti apie atidėtus elementus** nėra konfigūracijos medyje, importuokite ER modelio susiejimo konfigūraciją.

    1. Pasirinkite **Keitimas** ir pasirinkite **Įkelti iš XML failo**.
    2. Pasirinkite **Naršyti**, suraskite ir pasirinkite failą **Susiejimas, norint sužinoti apie atidėtus elementus.1.1.xml**, tada pasirinkite **Gerai**.

5. ER formato konfigūracijos importavimas

    1. Pasirinkite **Keitimas** ir pasirinkite **Įkelti iš XML failo**.
    2. Pasirinkite **Naršyti**, suraskite ir pasirinkite failą **Formatas, norint sužinoti apie atidėtas sekas.1.1.xml**, tada pasirinkite **Gerai**.

6. Konfigūracijos medyje išplėskite **Modelis, norint sužinoti apie atidėtus elementus**.
7. Peržiūrėkite importuotų ER konfigūracijų sąrašą konfigūracijos medyje.

    ![Importuotos ER konfigūracijos puslapyje Konfigūracijos](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Aktyvinti konfigūracijų teikėją

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Puslapio **Lokalizavimo konfigūracijos** skyriuje **Konfigūracijų teikėjai** įsitikinkite, kad sąraše yra [konfigūracijos teikėjas](general-electronic-reporting.md#Provider), susijęs su pavyzdine įmone „Litware, Inc.“ (`http://www.litware.com`), ir kad jis pažymėtas kaip aktyvus. Jeigu šio konfigūracijos teikėjo sąraše nėra arba jei jis nėra pažymėtas kaip aktyvus, atlikite temoje [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](./tasks/er-configuration-provider-mark-it-active-2016-11.md) nurodytus veiksmus.

    ![Pavyzdinė įmonė „Litware, Inc.“ puslapyje Lokalizavimo konfigūracijos](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Importuotų modelių susiejimo peržiūra

Peržiūrėkite ER modelio susiejimo komponento, kuris konfigūruojamas, kad būtų galima pasiekti mokesčių operacijas ir atskleisti gautus duomenis pagal prašymą, parametrus.

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Pasirinkite **Ataskaitų konfigūracijos**.
3. Puslapyje **Konfigūracijos** konfigūracijos medyje išplėskite **Modelis, norint sužinoti apie atidėtus elementus**.
4. Pasirinkite konfigūraciją **Susiejimas, norint sužinoti apie atidėtus elementus**.
5. Norėdami atidaryti susiejimų sąrašą, pasirinkite **Dizaino įrankis**.
6. Norėdami peržiūrėti susiejimo informaciją, pasirinkite **Dizaino įrankis**.
7. Pasirinkite **Rodyti informaciją**.
8. Peržiūrėkite duomenų šaltinius, kurie sukonfigūruoti, kad būtų galima pasiekti mokesčių operacijas.

    - Duomenų šaltinis **Operacijos**, kurio tipas yra *Lentelės įrašas*, sukonfigūruotas, kad būtų galima pasiekti programos lentelės **TaxTrans** įrašus.
    - Duomenų šaltinis **Kvitai**, kurio tipas yra *Apskaičiuoti laukai*, sukonfigūruotas, kad pateiktų reikiamus kvitų kodus (**INV-10000349** ir **INV-10000350**) kaip įrašų sąrašą.
    - Duomenų šaltinis **Filtruota**, kurio tipas yra *Apskaičiuoti laukai*, sukonfigūruotas taip, kad pasirinktų tik reikiamų kvitų mokesčių operacijas duomenų šaltinyje **Operacijos**.
    - Laukas **\$TaxAmount**, kurio tipas yra *Apskaičiuoti laukai*, įtraukiamas į duomenų šaltinį **Filtruota**, kad atskleistų mokesčio vertę su priešingu ženklu.
    - Duomenų šaltinis **Sugrupuota**, kurio tipas yra *Grupuoti pagal*, sukonfigūruotas, kad grupuotų duomenų šaltinio **Filtruota** mokesčių operacijas.
    - Agregavimo laukas **TotalSum** duomenų šaltinyje **Sugrupuota** sukonfigūruotas taip, kad apibendrintų vertes lauke **\$TaxAmount** duomenų šaltinyje **Filtruota** visų minėto duomenų šaltinio filtruotų mokesčių operacijų atveju.

        ![Agregavimo laukas TotalSum, esantis parametrų puslapyje Redaguoti 'GroupBy'](./media/ER-DeferredSequence-GroupByParameters.png)

9. Peržiūrėkite, kaip sukonfigūruoti duomenų šaltiniai yra susieti su duomenų modeliu ir kaip jie pateikia gautus duomenis, kad būtų galima juos naudoti ER formatu.

    - Duomenų šaltinis **Filtruota** yra susietas su duomenų modelio lauku **Data.List**.
    - Duomenų šaltinio **Filtruota** laukas **\$TaxAmount** yra susietas su duomenų modelio lauku **Data.List.Value**.
    - Duomenų šaltinio **Sugrupuota** laukas **TotalSum** yra susietas su duomenų modelio lauku **Data.Summary.Total**.

    ![Modelio susiejimo dizaino įrankio puslapis](./media/ER-DeferredSequence-ModelMapping.png)

10. Uždarykite puslapius **Modelio susiejimo dizaino įrankis** ir **Modelio susiejimai**.

### <a name="review-the-imported-format"></a>Peržiūrėkite importuotą formatą

1. Puslapyje **Konfigūracijos** konfigūracijos medyje pasirinkite konfigūraciją **Formatas, norint sužinoti apie atidėtas sekas**.
2. Norėdami peržiūrėti formato informaciją, pasirinkite **Dizaino įrankis**.
3. Pasirinkite **Rodyti informaciją**.
4. Peržiūrėkite ER formato komponentų, kurie sukonfigūruoti, kad siunčiami dokumentai būtų generuojami teksto formatu, kuriame yra mokesčių operacijų informacijos, parametrus.

    - Sekos formato elementas **Ataskaita\\Eilutės** yra sukonfigūruotas taip, kad į siunčiamus dokumentus įtrauktų vieną eilutę, sugeneruota iš įdėtųjų sekos elementų (**Antraštė**, **Įrašas** ir **Suvestinė**).

        ![Sekos formato elementas Eilutės ir įdėtieji elementai puslapyje Formato dizaino įrankis](./media/ER-DeferredSequence-Format.png)

    - Sekos formato elementas **Ataskaita\\Eilutės\\Antraštė** yra sukonfigūruotas taip, kad įtrauktų į siunčiamus dokumentus vieną antraštės eilutę, kurioje rodomi apdorojimo pradžios data ir laikas.
    - Sekos formato elementas **Ataskaita\\Eilutės\\Įrašas** sukonfigūruotas taip, kad įtrauktų į siunčiamus dokumentus vieną įrašo eilutę, kurioje pateikiama atskirų mokesčių operacijų informacija. Šios mokesčių operacijos atskiriamos kabliataškiu.

        ![Sekos formato elementas Įrašas, kuriame kabliataškis naudojamas kaip skyriklis](./media/ER-DeferredSequence-Format1.png)

    - Sekos formato elementas **Ataskaita\\Eilutės\\Suvestinė** sukonfigūruotas taip, kad įtrauktų į siunčiamus dokumentus vieną suvestinės eilutę, kurioje yra mokesčių verčių suma iš apdorotų mokesčių operacijų.

4. Skirtuke **Susiejimas** peržiūrėkite toliau pateikiamą informaciją.

    - Elemento **Ataskaita\\Eilutės\\Antraštė** nereikia susieti su duomenų šaltiniu, kad būtų galima sugeneruoti vieną eilutę siuntimo dokumente.
    - Elementas **Prefix1** generuoja simbolius **P1**, parodančius, kad įtraukiama eilutė yra ataskaitos antraštės eilutė.
    - Elementas **ExecutionDateTime** generuoja datą ir laiką (įskaitant milisekundes), kai įtraukiama antraštės eilutė.
    - Elementas **Ataskaita\\Eilutės\\Įrašas** yra susietas su sąrašu **model.Data.List**, kad kiekviename susieto sąrašo įraše būtų sugeneruota viena eilutė.
    - Elementas **Prefix2** generuoja simbolius **P2**, parodančius, kad įtraukiama eilutė yra susijusi su mokesčių operacijų informacija.
    - Elementas **TaxAmount** yra susietas su **model.Data.List.Value** (rodoma kaip **\@.Vertė** santykinio kelio rodinyje), kad būtų galima generuoti esamos mokesčių operacijos mokesčių vertę.
    - Elementas **RunningTotal** yra mokesčių verčių bendros sumos vietos rezervavimo ženklas. Šiuo metu šiame elemente nėra išvesties, nes nesukonfigūruotas nei jo susiejimas, nei numatytoji vertė.
    - Elementas **ExecutionDateTime** generuoja datą ir laiką (įskaitant milisekundes), kai šioje ataskaitoje apdorojama dabartinė operacija.
    - Elemento **Ataskaita\\Eilutės\\Suvestinė** nereikia susieti su duomenų šaltiniu, kad būtų galima sugeneruoti vieną eilutę siuntimo dokumente.
    - Elementas **Prefix3** generuoja simbolius **P3**, parodančius, kad įtraukiamoje eilutėje yra bendra mokesčių vertė.
    - Elementas **TotalTaxAmount** yra susietas su **model.Data.Summary.Total**, kad būtų sugeneruota apdorotų mokesčių operacijų mokesčių verčių suma.
    - Elementas **ExecutionDateTime** generuoja datą ir laiką (įskaitant milisekundes), kai įtraukiama suvestinės eilutė.

    ![Skirtukas Susiejimas puslapyje Formato dizaino įrankis](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>Importuoto formato vykdymas

1. Puslapyje **Formato dizaino įrankis** pasirinkite **Vykdyti**.
2. Atsisiųskite failą, kuris siūlomas žiniatinklio naršyklėje, ir atidarę jį peržiūrėkite.

    ![Atsisiųstas ataskaitos failo pavyzdys](./media/ER-DeferredSequence-Run.png)

Atkreipkite dėmesį, kad 22 suvestinės eilutėje pateikiama apdorotų operacijų mokesčių verčių suma. Kadangi formatas sukonfigūruotas, kad naudotų susiejimą **model.Data.Summary.Total** šiai sumai pateikti, suma apskaičiuojama iškviečiant telkimą **TotalSum** duomenų šaltinyje **Sugrupuota**, kurio tipas yra *GroupBy*, naudojantis modelių susiejimą. Norint apskaičiuoti šį telkimą, modelių susiejimas pakartojamas visose operacijose, kurios buvo pasirinktos duomenų šaltinyje **Filtruota**. Lygindami 21 ir 22 eilučių vykdymo laikus, galite nustatyti, kad sumos apskaičiavimas truko 10 milisekundžių (ms). Lygindami 2 ir 21 eilučių vykdymo laikus, galite nustatyti, kad visų operacijų eilučių generavimas truko 7 ms. Taigi, iš viso prireikė 17 ms.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Formato modifikavimas, kad sumavimas būtų paremtas sugeneruota išvestimi

Jei operacijų kiekis yra daug didesnis, nei kiekis šiame pavyzdyje, sumavimo trukmė gali padidėti ir sukelti našumo problemų. Pakeisdami formato parametrą, galite padėti išvengti šių našumo problemų. Kadangi mokesčių vertės įtraukiamos į sugeneruotą ataskaitą, galima pakartotinai panaudoti šią informaciją mokesčių vertėms sumuoti. Norėdami gauti daugiau informacijos, žr. [Formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti](./tasks/er-format-counting-summing-1.md).

1. Puslapyje **Formato dizaino įrankis** skirtuke **Formatas** formato medyje pasirinkite failo elementą **Ataskaita**.
2. Nustatykite parinkties **Rinkti išeigos informaciją** reikšmę **Taip**. Dabar galite konfigūruoti šį formatą, naudodami esamos ataskaitos turinį kaip duomenų šaltinį, kurį galima pasiekti naudojant įtaisytąsias ER funkcijas kategorijoje [Duomenų rinkimas](er-functions-category-data-collection.md).
3. Skirtuke **Susiejimas** pasirinkite sekos elementą **Ataskaita\\Eilutės**.
4. Sukonfigūruokite išraišką **Surinktų duomenų rakto pavadinimas** kaip `WsColumn`.
5. Sukonfigūruokite išraišką **Surinktų duomenų rakto reikšmė** kaip `WsRow`.

    ![Sekos elementas Eilutės puslapyje Formato dizaino įrankis](./media/ER-DeferredSequence-Format3.png)

6. Pasirinkite skaitinį elementą **Ataskaitos\\Eilutės\\Įrašas\\TaxAmount**.
7. Sukonfigūruokite išraišką **Surinktų duomenų rakto pavadinimas** kaip `SummingAmountKey`.

    ![Skaitinis elementas TaxAmount puslapyje Formato dizaino įrankis](./media/ER-DeferredSequence-Format4.png)

    Galite laikyti šį parametrą virtualaus darbalapio pildymu, kai A1 langelio vertė pridedama prie kiekvienos apdorotos mokesčių operacijos mokesčio sumos vertės.

8. Pasirinkite skaitinį elementą **Ataskaita\\Eilutės\\Įrašas\\RunningTotal**, tada pasirinkite **Redaguoti formulę**.
9. Konfigūruokite išraišką `SUMIF(SummingAmountKey, WsColumn, WsRow)` naudodami įtaisytąją ER funkciją [SUMIF](er-functions-datacollection-sumif.md).
10. Pasirinkite **Įrašyti**.

    ![Išraiška SUMIF](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Uždarykite puslapį **Formulės konstruktorius**.
12. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
13. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas failas – susumuoti mokesčių vertės](./media/ER-DeferredSequence-Run1.png)

    21 eilutėje yra visų apdorotų operacijų bendra mokesčių verčių suma, apskaičiuota naudojant sugeneruotą išvestį kaip duomenų šaltinį. Šis duomenų šaltinis prasideda ataskaitos pradžioje ir tęsiasi iki paskutinės mokesčių operacijos. 22 eilutėje yra visų apdorotų operacijų, apskaičiuotų modelio susiejimo metu naudojant *GroupBy* tipo duomenų šaltinį, mokesčių verčių suma. Atkreipkite dėmesį, kad šios vertės yra lygios. Todėl galima naudoti išvestimi pagrįstą sumavimą, o ne **GroupBy**. Lygindami 2 ir 21 eilučių vykdymo laikus, galite nustatyti, kad visų operacijų eilučių generavimas ir sumavimas truko 9 ms. Todėl, kiek tai susiję su išsamių eilučių generavimu ir mokesčių verčių sumavimu, modifikuotas formatas yra maždaug du kartus spartesnis už pradinį formatą.

14. Pasirinkite skaitinį elementą **Ataskaita\\Eilutės\\Suvestinė\\TotalTaxAmount**, tada pasirinkite **Redaguoti formulę**.
15. Įveskite išraišką `SUMIF(SummingAmountKey, WsColumn, WsRow)` vietoj esamos išraiškos.
16. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
17. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas failas su redaguota formule](./media/ER-DeferredSequence-Run2.png)

    Atkreipkite dėmesį, kad bendra mokesčių verčių suma paskutinėje operacijos informacijos eilutėje dabar yra lygi sumai suvestinės eilutėje.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Išvestimi pagrįsto sumavimo verčių pateikimas ataskaitos antraštėje

Jei, pavyzdžiui, turite pateikti mokesčių verčių sumą ataskaitos antraštėje, galite modifikuoti naudojamą formatą.

1. Puslapyje **Formato dizaino įrankis** skirtuke **Formatas** pasirinkite sekos elementą **Ataskaita\\Eilutės\\Suvestinė**.
2. Pasirinkite **Perkelti aukštyn**.
3. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
4. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas failas, skirtas sumuoti ataskaitos antraštėje](./media/ER-DeferredSequence-Run3.png)

    Atkreipkite dėmesį, kad mokesčių verčių suma 2 suvestinės eilutėje dabar yra lygi 0 (nuliui), nes ši suma dabar apskaičiuojama pagal sugeneruotą išvestį. Kai sugeneruojama 2 eilutė, sugeneruotoje išvestyje dar nėra eilučių, kuriuose būtų operacijų informacijos. Galite sukonfigūruoti šį formatą, kad būtų atidėtas sekos elemento **Ataskaita\\Eilutės\\Suvestinė** vykdymas, kol bus įvykdytas visų mokesčių operacijų sekos elementas **Ataskaita\\Eilutės\\Įrašas**.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Suvestinės sekos vykdymo atidėjimas, kad būtų naudojama apskaičiuota suma

1. Puslapyje **Formato dizaino įrankis** skirtuke **Formatas** pasirinkite sekos elementą **Ataskaita\\Eilutės\\Suvestinė**.
2. Parinktyje **Atidėtas vykdymas** nustatykite **Taip**.

    ![Sekos elemento Suvestinė atidėto vykdymo parinktis puslapyje Formato dizaino įrankis](./media/ER-DeferredSequence-Format5.png)

3. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
4. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas failas – atidėtas vykdymas](./media/ER-DeferredSequence-Run4.png)

    Dabar sekos elementas **Ataskaita\\Eilutės\\Suvestinė** dabar vykdomas tik įvykdžius visus kitus jo pirminio elemento **Ataskaita\\Eilutės** įdėtuosius elementus. Todėl jis vykdomas įvykdžius sekos elementą **Ataskaita\\Eilutės\\Įrašas** visų mokesčių operacijų, kurių duomenų šaltinis yra **model.Data.List**, atžvilgiu. 1, 2 ir 3 eilučių ir paskutinės (22) eilutės vykdymo laikai atskleidžia šį faktą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti](./tasks/er-format-counting-summing-1.md)
- [ER formato vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md)
- [XML elementų ER formatais vykdymo atidėjimas](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
