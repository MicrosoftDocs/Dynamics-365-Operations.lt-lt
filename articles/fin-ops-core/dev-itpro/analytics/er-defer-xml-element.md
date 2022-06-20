---
title: XML elementų ER formatais vykdymo atidėjimas
description: Šiame straipsnyje paaiškinama, kaip atidėti XML elemento vykdymą elektroninės ataskaitos (ER) formatu.
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
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 074b14cbb018a8e34b99124b8aaec3a5bdb30be2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861851"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>XML elementų ER formatais vykdymo atidėjimas

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Peržiūrėti

Norėdami sukonfigūruoti [ER sprendimo, kuris naudojamas siunčiamams dokumentams XML formatu generuoti, formato komponentą, galite naudoti elektroninių ataskaitų (ER)](general-electronic-reporting.md)[sistemos](./tasks/er-format-configuration-2016-11.md) operacijų konstruktorių. Sukonfigūruoto formato komponento hierarchinė struktūra susideda iš įvairių tipų formato elementų. Šie formato elementai naudojami sugeneruotiems dokumentams užpildyti reikiama informacija vykdymo metu. Numatyta, kad kai vykdote ER formatą, formato elementai vykdomi tokia pačia tvarka, kokia jie pateikiami formato hierarchijoje: po vieną, iš viršaus į apačią. Tačiau kūrimo metu galite pakeisti bet kurių sukonfigūruoto formato komponento XML elementų vykdymo tvarką.

Įjungę XML elemento sukonfigūruotu formatu parinktį <a name="DeferredXmlElementExecution"></a>**Atidėtas vykdymas**, galite atidėti (nukelti) to elemento vykdymą. Šiuo atveju elementas nevykdomas, kol neįvykdomi visi kiti jo pirminio elemento elementai.

Norėdami daugiau sužinoti apie šią funkciją, užpildykite pavyzdį šiame straipsnyje.

## <a name="limitations"></a>Apribojimai

Parinktis **Atidėtas vykdymas** taikoma tik XML elementams, kurie sukonfigūruoti ER formatui, naudojamam **siunčiamiems** dokumentams XML formatu generuoti.

Parinktis **Atidėtas vykdymas** taikoma tik XML elementams, esantiems tik viename kitame XML elemente. Todėl jis netaikoma XML elementams, esantiems kituose formato elementų tipuose (pvz., elemente **XML seka**).

Parinktis **Atidėtas vykdymas** netaikoma XML elementams, esantiems formato elemente **Bendra\\Failas**, kai parinktyje **Skaidyti failą** nustatyta **Taip**. Daugiau informacijos apie tai, kaip skaidyti XML failus, žr. [Sugeneruotų XML failų skaidymas pagal failo dydį ir turinio kiekį](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Pavyzdys: XML elemento ER formatu vykdymo atidėjimas

Toliau pateikiamuose veiksmuose paaiškinama, kaip vartotojas, kuriam priskirtas Sistemos administratoriaus arba Elektroninės ataskaitos funkcijų konsultanto [vaidmuo](../sysadmin/tasks/assign-users-security-roles.md), gali konfigūruoti ER formatą, kuriame yra XML elementas, kai vykdymo tvarka skiriasi nuo tvarkos formato hierarchijoje.

Šiuos veiksmus galima atlikti JAV dolerių **įmonėje "** Microsoft Dynamics 365 Finance".

### <a name="prerequisites"></a>Būtinieji komponentai

Norėdami atlikti šį pavyzdį, turite turėti prieigą prie įmonės **USMF** programoje „Finance“ ir vieną iš tolesnių vaidmenų.

- Elektroninės ataskaitos funkcijų konsultantas
- Sistemos administratorius

Jei dar nebaigėte [ER formatų straipsnyje atidėto sekos elementų vykdymo pavyzdžio](er-defer-sequence-element.md#Example), [atsisiųskite toliau pateiktas ER sprendimo pavyzdžio konfigūracijas](general-electronic-reporting.md#Configuration).

| Turinio aprašas            | Failo pavadinimas |
|--------------------------------|-----------|
| ER duomenų modelio konfigūracija    | [Modelis, norint sužinoti apie atidėtus elementus.1.versija.xml](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| ER modelio susiejimo konfigūracija | [Susiejimas, norint sužinoti apie atidėtus elementus.1.1.versija.xml](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Prieš pradėdami, taip pat turite atsisiųsti ir įrašyti šią ER sprendimo pavyzdžio konfigūraciją į vietinį kompiuterį.

| Turinio aprašas     | Failo pavadinimas |
|-------------------------|-----------|
| ER formato konfigūracija | [Formatas, norint sužinoti apie atidėtus XML elementus.1.1.versija.xml](https://download.microsoft.com/download/4/7/8/478fa846-22e9-4fa0-89b1-d3aeae660067/FormattolearndeferredXMLelements.version.1.1.xml) |

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
    2. Pasirinkite **Naršyti**, suraskite ir pasirinkite failą **Formatas, norint sužinoti apie atidėtus XML elementus.1.1.xml**, tada pasirinkite **Gerai**.

6. Konfigūracijos medyje išplėskite **Modelis, norint sužinoti apie atidėtus elementus**.
7. Peržiūrėkite importuotų ER konfigūracijų sąrašą konfigūracijos medyje.

    ![Importuotos ER konfigūracijos puslapyje Konfigūracijos.](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Konfigūracijų teikėjo aktyvinimas

1. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
2. Puslapio **Lokalizavimo konfigūracijos** skyriuje **Konfigūracijų teikėjai** įsitikinkite, kad sąraše yra [konfigūracijos teikėjas](general-electronic-reporting.md#Provider), susijęs su pavyzdine įmone „Litware, Inc.“ (`http://www.litware.com`), ir kad jis pažymėtas kaip aktyvus. Jei šio konfigūracijos teikėjo nėra arba jei jis nepažymėtas kaip aktyvus, [atlikite konfigūracijos teikėjo kūrimo veiksmus ir pažymėkite jį kaip aktyvų](./tasks/er-configuration-provider-mark-it-active-2016-11.md) straipsnį.

    ![Pavyzdinė įmonė „Litware, Inc.“ puslapyje Lokalizavimo konfigūracijos.](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

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

        ![Kaupimo laukas „Bendra suma”, esantis parametrų puslapyje Redaguoti „Sugrupuoti pagal”.](./media/ER-DeferredXml-GroupByParameters.png)

9. Peržiūrėkite, kaip sukonfigūruoti duomenų šaltiniai yra susieti su duomenų modeliu ir kaip jie pateikia gautus duomenis, kad būtų galima juos naudoti ER formatu.

    - Duomenų šaltinis **Filtruota** yra susietas su duomenų modelio lauku **Data.List**.
    - Duomenų šaltinio **Filtruota** laukas **\$TaxAmount** yra susietas su duomenų modelio lauku **Data.List.Value**.
    - Duomenų šaltinio **Sugrupuota** laukas **TotalSum** yra susietas su duomenų modelio lauku **Data.Summary.Total**.

    ![Modelio susiejimo dizaino įrankio puslapis.](./media/ER-DeferredXml-ModelMapping.png)

10. Uždarykite puslapius **Modelio susiejimo dizaino įrankis** ir **Modelio susiejimai**.

### <a name="review-the-imported-format"></a>Peržiūrėkite importuotą formatą

1. Puslapyje **Konfigūracijos** konfigūracijos medyje pasirinkite konfigūraciją **Formatas, norint sužinoti apie atidėtus XML elementus**.
2. Norėdami peržiūrėti formato informaciją, pasirinkite **Dizaino įrankis**.
3. Pasirinkite **Rodyti informaciją**.
4. Peržiūrėkite ER formato komponentų, kurie sukonfigūruoti, kad siunčiami dokumentai būtų generuojami XML formatu, kuriame yra mokesčių operacijų informacijos, parametrus.

    - XML elementas **Ataskaita\\Pranešimas** yra sukonfigūruotas taip, kad į siunčiamus dokumentus įtrauktų vieną mazgą, kuriame yra įdėtųjų XML elementų (**Antraštė**, **Įrašas** ir **Suvestinė**).
    - XML elementas **Ataskaita\\Pranešimas\\Antraštė** yra sukonfigūruotas taip, kad įtrauktų į siunčiamus dokumentus vieną antraštės mazgą, kuriame rodomi apdorojimo pradžios data ir laikas.
    - XML elementas **Ataskaita\\Pranešimas\\Įrašas** sukonfigūruotas taip, kad įtrauktų į siunčiamus dokumentus vieną įrašo mazgą, kuriame pateikiama vienos mokesčių operacijos informacija.
    - XML elementas **Ataskaita\\Pranešimas\\Suvestinė** sukonfigūruotas taip, kad įtrauktų į siunčiamus dokumentus vieną suvestinės mazgą, kuriame yra mokesčių verčių suma iš apdorotų mokesčių operacijų.

    ![XML elementas Pranešimas ir įdėtieji XML elementai puslapyje Formato dizaino įrankis.](./media/ER-DeferredXml-Format.png)

5. Skirtuke **Susiejimas** peržiūrėkite toliau pateikiamą informaciją.

    - Elemento **Ataskaita\\Pranešimas\\Antraštė** nereikia susieti su šaltiniu, kad būtų galima sugeneruoti vieną mazgą siuntimo dokumente.
    - Atributas **ExecutionDateTime** generuoja datą ir laiką (įskaitant milisekundes), kai įtraukiamas antraštės mazgas.
    - Elementas **Ataskaita\\Pranešimas\\Įrašas** yra susietas su sąrašu **model.Data.List**, kad kiekviename susieto sąrašo įraše būtų sugeneruotas vienas įrašo mazgas.
    - Atributas **TaxAmount** yra susietas su **model.Data.List.Value** (rodoma kaip **\@.Vertė** santykinio kelio rodinyje), kad būtų galima generuoti esamos mokesčių operacijos mokesčių vertę.
    - Atributas **RunningTotal** yra mokesčių verčių bendros sumos vietos rezervavimo ženklas. Šiuo metu šiame atribute nėra išvesties, nes nesukonfigūruotas nei jo susiejimas, nei numatytoji vertė.
    - Atributas **ExecutionDateTime** generuoja datą ir laiką (įskaitant milisekundes), kai šioje ataskaitoje apdorojama dabartinė operacija.
    - Elemento **Ataskaita\\Pranešimas\\Suvestinė** nereikia susieti su duomenų šaltiniu, kad būtų galima sugeneruoti vieną mazgą siuntimo dokumente.
    - Atributas **TotalTaxAmount** yra susietas su **model.Data.Summary.Total**, kad būtų sugeneruota apdorotų mokesčių operacijų mokesčių verčių suma.
    - Atributas **ExecutionDateTime** generuoja datą ir laiką (įskaitant milisekundes), kai įtraukiamas suvestinės mazgas.

    ![Skirtukas Susiejimas puslapyje Formato dizaino įrankis.](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>Importuoto formato vykdymas

1. Puslapyje **Formato dizaino įrankis** pasirinkite **Vykdyti**.
2. Atsisiųskite failą, kuris siūlomas žiniatinklio naršyklėje, ir atidarę jį peržiūrėkite.

    ![Importuoto formato atsisiųstas failas.](./media/ER-DeferredXml-Run.png)

Atkreipkite dėmesį, kad suvestinės mazge pateikiama apdorotų operacijų mokesčių verčių suma. Kadangi formatas sukonfigūruotas, kad naudotų susiejimą **model.Data.Summary.Total** šiai sumai pateikti, suma apskaičiuojama iškviečiant telkimą **TotalSum** duomenų šaltinyje **Sugrupuota**, kurio tipas yra *GroupBy*, modelių susiejime. Norint apskaičiuoti šį telkimą, modelių susiejimas pakartojamas visose operacijose, kurios buvo pasirinktos duomenų šaltinyje **Filtruota**. Lygindami suvestinės mazgo ir paskutinio įrašo mazgo vykdymo laikus, galite nustatyti, kad sumos skaičiavimas truko 12 milisekundžių (ms). Lygindami pirmo ir paskutinio įrašų mazgų vykdymo laikus, galite nustatyti, kad visų įrašų mazgų generavimas truko 9 ms. Taigi, iš viso prireikė 21 ms.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Formato modifikavimas, kad skaičiavimas būtų paremtas sugeneruota išvestimi

Jei operacijų kiekis yra daug didesnis, nei kiekis šiame pavyzdyje, skaičiavimo trukmė gali padidėti ir sukelti našumo problemų. Pakeisdami formato parametrą, galite padėti išvengti šių našumo problemų. Kadangi mokesčių vertės įtraukiamos į sugeneruotą ataskaitą, galima pakartotinai panaudoti šią informaciją mokesčių vertėms apskaičiuoti. Norėdami gauti daugiau informacijos, žr. [Formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti](./tasks/er-format-counting-summing-1.md).

1. Puslapyje **Formato dizaino įrankis** skirtuke **Formatas** formato medyje pasirinkite failo elementą **Ataskaita**.
2. Nustatykite parinkties **Rinkti išeigos informaciją** reikšmę **Taip**. Dabar galite konfigūruoti šį formatą, naudodami sugeneruotos ataskaitos turinį kaip duomenų šaltinį, kurį galima pasiekti naudojant įtaisytąsias ER funkcijas kategorijoje [Duomenų rinkimas](er-functions-category-data-collection.md).
3. Skirtuke **Susiejimas** pasirinkite XML elementą **Ataskaita\\Pranešimas\\Įrašas**.
4. Sukonfigūruokite išraišką **Surinktų duomenų rakto pavadinimas** kaip `WsColumn`.
5. Sukonfigūruokite išraišką **Surinktų duomenų rakto reikšmė** kaip `WsRow`.

    ![XML elementas Įrašas puslapyje Formato dizaino įrankis.](./media/ER-DeferredXml-Format3.png)

6. Pasirinkite atributą **Ataskaita\\Pranešimas\\Įrašas\\TaxAmount**.
7. Sukonfigūruokite išraišką **Surinktų duomenų rakto pavadinimas** kaip `SummingAmountKey`.

    ![Atributas TaxAmount puslapyje Formato dizaino įrankis.](./media/ER-DeferredXml-Format4.png)

    Galite laikyti šį parametrą virtualaus darbalapio pildymu, kai A1 langelio vertė pridedama prie kiekvienos apdorotos mokesčių operacijos mokesčio sumos vertės.

8. Pasirinkite atributą **Ataskaita\\Pranešimas\\Įrašas\\RunningTotal**, tada pasirinkite **Redaguoti formulę**.
9. Konfigūruokite išraišką `SUMIF(SummingAmountKey, WsColumn, WsRow)` naudodami įtaisytąją ER funkciją [SUMIF](er-functions-datacollection-sumif.md), tada pasirinkite **Įrašyti**.

    ![Išraiška SUMIF.](./media/ER-DeferredXml-FormulaDesigner.png)

10. Uždarykite puslapį **Formulės konstruktorius**.
11. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
12. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Sugeneruotas mokesčių vertės su vykdoma suma sąrašas.](./media/ER-DeferredXml-Run1.png)

    Paskutiniame įrašo mazge yra visų apdorotų operacijų bendra mokesčių verčių suma, apskaičiuota naudojant sugeneruotą išvestį kaip duomenų šaltinį. Šis duomenų šaltinis prasideda ataskaitos pradžioje ir tęsiasi iki paskutinės mokesčių operacijos. Suvestinės mazge yra visų apdorotų operacijų, apskaičiuotų modelio susiejimo metu naudojant *GroupBy* tipo duomenų šaltinį, mokesčių verčių suma. Atkreipkite dėmesį, kad šios vertės yra lygios. Todėl galima naudoti išvestimi pagrįstą sumavimą, o ne **GroupBy**. Lygindami pirmo įrašo mazgo ir suvestinės mazgo vykdymo laikus, galite nustatyti, kad visų įrašų mazgų generavimas ir sumavimas truko 11 ms. Todėl, kiek tai susiję su įrašų mazgų generavimu ir mokesčių verčių sumavimu, modifikuotas formatas yra maždaug du kartus spartesnis už pradinį formatą.

13. Pasirinkite atributą **Ataskaita\\Pranešimas\\Suvestinė\\TotalTaxAmount**, tada pasirinkite **Redaguoti formulę**.
14. Įveskite išraišką `SUMIF(SummingAmountKey, WsColumn, WsRow)` vietoj esamos išraiškos.
15. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
16. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Sugeneruotas mokesčių verčių sąrašas naudojant redaguotą formulę.](./media/ER-DeferredXml-Run2.png)

    Atkreipkite dėmesį, kad bendra mokesčių verčių suma paskutiniame įrašo mazge dabar yra lygi sumai suvestinės mazge.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Išvestimi pagrįsto sumavimo verčių pateikimas ataskaitos antraštėje

Jei, pavyzdžiui, turite pateikti mokesčių verčių sumą ataskaitos antraštėje, galite modifikuoti naudojamą formatą.

1. Puslapyje **Formato dizaino įrankis** skirtuke **Formatas** pasirinkite XML elementą **Ataskaita\\Pranešimas\\Suvestinė**.
2. Pasirinkite **Perkelti aukštyn**.
3. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
4. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas ataskaitos antraštės mokesčių verčių failas.](./media/ER-DeferredXml-Run3.png)

    Atkreipkite dėmesį, kad mokesčių verčių suma suvestinės mazge dabar yra lygi 0 (nuliui), nes ši suma dabar apskaičiuojama pagal sugeneruotą išvestį. Kai sugeneruojamas pirmas įrašo mazgas, sugeneruotoje išvestyje dar nėra įrašų mazgų, kuriuose būtų operacijų informacijos. Galite sukonfigūruoti šį formatą, kad būtų atidėtas elemento **Ataskaita\\Pranešimas\\Suvestinė** vykdymas, kol bus įvykdytas visų mokesčių operacijų elementas **Ataskaita\\Pranešimas\\Įrašas**.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>Suvestinės XML elemento vykdymo atidėjimas, kad būtų naudojama apskaičiuota suma

1. Puslapyje **Formato dizaino įrankis** skirtuke **Formatas** pasirinkite XML elementą **Ataskaita\\Pranešimas\\Suvestinė**.
2. Parinktyje **Atidėtas vykdymas** nustatykite **Taip**.

    ![XML elemento Suvestinė atidėto vykdymo parinktis puslapyje Formato dizaino įrankis.](./media/ER-DeferredXml-Format5.png)

3. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
4. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas failas – atidėtas vykdymas.](./media/ER-DeferredXml-Run4.png)

    Dabar elementas **Ataskaita\\Pranešimas\\Suvestinė** dabar vykdomas tik įvykdžius visus kitus jo pirminio elemento **Ataskaita\\Pranešimas** įdėtuosius elementus. Todėl jis vykdomas įvykdžius elementą **Ataskaita\\Pranešimas\\Įrašas** visų mokesčių operacijų, kurių duomenų šaltinis yra **model.Data.List**, atžvilgiu. Pirmo ir paskutinio įrašų mazgų ir antraštės bei suvestinės mazgų vykdymo laikai atskleidžia šį faktą.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti](./tasks/er-format-counting-summing-1.md)
- [ER formato vykdymo sekimas siekiant diagnozuoti našumo problemas](trace-execution-er-troubleshoot-perf.md)
- [Sekos elementų ER formatais vykdymo atidėjimas](er-defer-sequence-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
