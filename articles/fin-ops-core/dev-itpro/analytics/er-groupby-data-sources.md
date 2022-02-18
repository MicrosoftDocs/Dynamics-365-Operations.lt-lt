---
title: Grupuokite įrašus ir apibendrinkite skaičiavimus naudodami GROUPBY duomenų šaltinius
description: Šioje temoje paaiškinama, kaip galite naudoti GROUPBY tipo duomenų šaltinius elektroninėse ataskaitose (ER).
author: NickSelin
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a6cdc486c5f799bdedafa38e90be989fd328c96
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075756"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Grupuokite įrašus ir apibendrinkite skaičiavimus naudodami GROUPBY duomenų šaltinius

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Kai konfigūruojate [Elektroninis ataskaitų teikimas (ER)](general-electronic-reporting.md) modelių atvaizdus ar formatus, galite [papildyti](#AddMmDataSource2) būtini duomenų šaltiniai **Grupuoti pagal** tipo.

Projektavimo metu a **Grupuoti pagal** duomenų šaltinis sukonfigūruotas taip, kad nustatytų šiuos elementus:

- A [bazinis duomenų šaltinis](#BaseDataSource) kuriame yra įrašų, kurie bus sugrupuoti vykdymo metu
- [Laukų grupavimas](#GroupingFields) bazinio duomenų šaltinio, kuris bus naudojamas įrašų grupavimui vykdymo metu
- [Suvestinės funkcijos](#AggregateFunctions) kurie nurodo bendrus skaičiavimus, kurie bus atlikti kiekvienai aptiktai grupei vykdymo metu

Vykdymo metu sukonfigūruotas **Grupuoti pagal** duomenų šaltinis sugrupuoja įrašus, kurių grupavimo laukuose yra tos pačios reikšmės, ir grąžina įrašų sąrašą. Kiekvienas įrašas reiškia vieną grupę. Kiekvienos grupės duomenų šaltinis pateikia laukų reikšmes, pagal kurias buvo sugrupuoti pradiniai įrašai, apskaičiuotų suvestinių funkcijų reikšmes ir grupei priklausančio bazinio duomenų šaltinio įrašų sąrašą.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a> Suvestinės funkcijos

Vykdymo metu kiekvienas suvestinis skaičiavimas atliekamas kiekvienai įrašų grupei. Šis skaičiavimas atliekamas naudojant vieno lauko reikšmę arba išraišką duomenų šaltinio įrašuose, kurie buvo pasirinkti grupuoti redaguojamo duomenų šaltinio duomenų šaltinyje.**Grupuoti pagal** tipo. Šiuo metu palaikomos šios suvestinės funkcijos:

- **AVG** – Ši funkcija grąžina grupės reikšmių vidurkį. Jį galima naudoti tik su skaitiniais laukais.
- **SKAIČIUOTI** – Ši funkcija grąžina elementų, kurie buvo rasti grupėje, skaičių.
- **Min** – Ši funkcija grąžina mažiausią reikšmę tarp reikšmių grupėje.
- **Maks** – Ši funkcija grąžina didžiausią reikšmę tarp reikšmių grupėje.
- **SUMA** – Ši funkcija grąžina visų grupės reikšmių sumą. Jį galima naudoti tik su skaitiniais laukais.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Vykdymo vieta

Kai redaguojate a **Grupuoti pagal** duomenų šaltinį ir nurodykite bazinį duomenų šaltinį, kuriame yra įrašai, kurie turi būti sugrupuoti, sistema automatiškai nustato efektyviausią [vieta](#ExecutionLocation) to įvykdymui **Grupuoti pagal** duomenų šaltinis. Jei bazinis duomenų šaltinis yra [galima paklausti](er-functions-list-filter.md#usage-notes) (ty jei ją galima paleisti duomenų bazės lygiu), programos duomenų bazė taip pat nurodoma kaip redaguojamo failo vykdymo vieta **Grupuoti pagal** duomenų šaltinis. Kitu atveju programos serverio atmintis nurodoma kaip vykdymo vieta.

Galite rankiniu būdu pakeisti automatiškai aptiktą vykdymo vietą, pasirinkdami vietą, kuri tinka sukonfigūruotam duomenų šaltiniui. Jei pasirinkta vykdymo vieta netinka, a [patvirtinimo klaida](er-components-inspections.md#i5) yra metamas projektavimo metu.

> [!TIP]
> Rekomenduojame naudoti duomenų bazės vietą duomenų šaltiniams, kuriuose yra daug įrašų, sugrupuoti.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a> Atminties suvartojimas

Pagal numatytuosius nustatymus, jei a **Grupuoti pagal** duomenų šaltinis paleidžiamas atmintyje, taikomųjų programų serverio atmintis naudojama bazinio duomenų šaltinio, priklausančio kiekvienai aptiktai grupei, įrašams saugoti kaip vienos grupės įrašams. Norėdami sumažinti atminties suvartojimą, galite neleisti saugoti įrašų **Grupuoti pagal** duomenų šaltinius, jei jie buvo sukonfigūruoti skaičiuoti tik apibendrintas funkcijas, o jų grupės įrašai nenaudojami vykdymo metu. Norėdami tokiu būdu sumažinti atminties suvartojimą, įjunkite **Sumažinkite atminties naudojimą ER, kai įrašų grupavimas naudojamas tik agregacijai apskaičiuoti** funkcija **Funkcijų valdymas** darbo vieta.

## <a name="alternatives"></a><a name="Alternatives"></a> Alternatyvos

Panašius suminius galima apskaičiuoti naudojant [skirtinga](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) duomenų šaltinių tipai arba ER integruotos funkcijos.

Norėdami daugiau sužinoti apie šią funkciją, atlikite toliau pateiktą pavyzdį.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a> Pavyzdys: naudokite GROUPBY duomenų šaltinį suvestiniams skaičiavimams ir įrašų grupavimui

Šiame pavyzdyje parodyta, kaip sistemos administratoriaus arba elektroninių ataskaitų teikimo konsultanto vaidmens vartotojas gali sukonfigūruoti ER modelio susiejimą, turintį **GRUPUOTI PAGAL** duomenų šaltinis, naudojamas suvestinėms funkcijoms ir grupės įrašams apskaičiuoti. Šis modelio atvaizdavimas naudojamas kontrolės ataskaitai spausdinti, kai generuojama Intrastato deklaracija. Ši ataskaita leidžia peržiūrėti praneštas Intrastato operacijas.

Šiame pavyzdyje aprašytas procedūras galima atlikti **DEMF** įmonė Microsoft Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Paruoškite duomenų pavyzdžius

Įsitikinkite, kad turite Intrastato operacijų, kad galėtumėte teikti ataskaitas **Intrastatas** puslapį. Turite turėti skirtingų transporto kodų operacijas, nes operacijas sugrupuosite pagal **Transportas** lauke šiame pavyzdyje.

![Intrastato operacijų paruošimas Intrastato puslapyje.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>ER sistemos konfigūracija

Atlikite veiksmus, aprašytus skyriuje [Konfigūruoti ER sistemą](er-quick-start2-customize-report.md#ConfigureFramework), kad nustatytumėte minimalų ER parametrų rinkinį. Turite užbaigti šią sąranką prieš pradėdami naudoti ER sistemą, kad sukurtumėte ER modelio atvaizdavimą.

### <a name="import-the-standard-er-format-configuration"></a>Standartinio ER formato konfigūracijos importavimas

Atlikite veiksmus, aprašytus skyriuje [Importuoti standartinio ER formato konfigūracijas](er-quick-start2-customize-report.md#ImportERSolution1), kad įtrauktumėte standartines ER konfigūracijas į dabartinį „Dynamics 365 Finance” egzempliorių. Importuoti 1 versiją **Intrastato modelis** konfigūraciją iš saugyklos.

### <a name="create-a-custom-data-model-configuration"></a>Sukurkite tinkintą duomenų modelio konfigūraciją

Atlikite nurodytus veiksmus [Pridėkite tinkintą duomenų modelio konfigūraciją](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) norėdami rankiniu būdu pridėti naują **Intrastato modelis (Litware)** ER duomenų modelio konfigūracija, kurią gaunate iš importuoto **Intrastato modelis** konfigūracija.

### <a name="configure-a-custom-data-model-component"></a>Konfigūruokite pasirinktinį duomenų modelio komponentą

Atlikite šiuos veiksmus, kad atliktumėte reikiamus pakeitimus **Intrastato modelis (Litware)** duomenų modelį, kad jį būtų galima naudoti norint atskleisti transporto kodus, turinčius reikiamą informaciją.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Ant **Konfigūracijos** puslapyje konfigūracijos medyje pasirinkite **Intrastato modelis (Litware)**.
3. Pasirinkite **Dizaino įrankis**.
4. Ant **Duomenų modelio kūrėjas** puslapyje modelio medyje pasirinkite **Intrastatas**.
5. Pasirinkite **Nauja** norėdami pridėti naują įdėtą mazgą prie pasirinkto **Intrastatas** mazgas. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Viduje konors **vardas** lauką, įveskite **Transportas**.
    2. Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

6. Pasirinkite **Nauja** norėdami pridėti naują įdėtą mazgą **Transportas** mazgas, kurį ką tik pridėjote. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Viduje konors **vardas** lauką, įveskite **Kodas**.
    2. Lauke **Elemento tipas** pasirinkite **Eilutė**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

7. Pasirinkite **Nauja** kad pridėtumėte kitą naują įdėtą mazgą **Transportas** mazgas. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Viduje konors **vardas** lauką, įveskite **TotalInvoicedAmount**.
    2. Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

8. Pasirinkite **Nauja** kad pridėtumėte kitą naują įdėtą mazgą **Transportas** mazgas. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Viduje konors **vardas** lauką, įveskite **Operacijų skaičius**.
    2. Lauke **Elemento tipas** pasirinkite **Sveikasis skaičius**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

9. Pasirinkite **Nauja** kad pridėtumėte kitą naują įdėtą mazgą **Transportas** mazgas. Iškrentančiame teksto laukelyje duomenų modelio mazgo įtraukimui, atlikite šiuos žingsnius:

    1. Viduje konors **vardas** lauką, įveskite **Sandoris**.
    2. Lauke **Elemento tipas** pasirinkite **Įrašų sąrašas**.
    3. Pasirinkite **Įtraukti** tam, kad įtrauktumėte naują mazgą.

10. Už **Sandoris** mazgas, kurį ką tik pridėjote **Mazgas** FastTab, pasirinkite **Perjungti elemento nuorodą**.
11. Viduje konors **Perjungti elemento nuorodą** dialogo lange duomenų modelio medyje pasirinkite **CommodityRecord**. Tada pasirinkite **Gerai**.

![Konfigūruotas duomenų modelis ER duomenų modelio kūrimo įrankyje.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Užbaikite tinkinto duomenų modelio kūrimą

Atlikite nurodytus veiksmus [Užbaikite duomenų modelio kūrimą](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) užbaigti išvestinio dizainą **Intrastato modelis (Litware)** duomenų modelis.

### <a name="create-a-new-model-mapping-configuration"></a>Sukurkite naują modelio žemėlapio konfigūravimą

Atlikite nurodytus veiksmus [Sukurkite naują modelio susiejimo konfigūraciją](er-quick-start1-new-solution.md#CreateModelMapping) norėdami rankiniu būdu pridėti naują **Intrastato pavyzdžių kartografavimas** ER modelio susiejimo konfigūracija išvestinei **Intrastato modelis (Litware)** konfigūracija.

### <a name="add-a-new-model-mapping-component"></a>Pridėkite naują modelio susiejimo komponentą

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Ant **Konfigūracijos** puslapyje, konfigūracijos medyje, išplėskite **Intrastato modelis** konfigūracija.
3. Pasirinkite **Intrastato pavyzdžių kartografavimas** konfigūracija.
4. Norėdami atidaryti susiejimų sąrašą, pasirinkite **Dizaino įrankis**.
5. Pasirinkite **Ištrinti** pašalinti esamą atvaizdavimo komponentą.
6. Pasirinkite **Nauja** norėdami pridėti naują atvaizdavimo komponentą.
7. Viduje konors **Apibrėžimas** lauką, pasirinkite **Intrastatas**.
8. Viduje konors **vardas** lauką, įveskite **Intrastato žemėlapių sudarymas**.
9. Pasirinkite **Dizaineris** norėdami sukonfigūruoti naują susiejimą.

### <a name="design-the-added-model-mapping-component"></a>Sukurkite pridėtą modelio atvaizdavimo komponentą

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a> Pridėkite duomenų šaltinį, kad pasiektumėte programų lentelę

Sukonfigūruokite duomenų šaltinį, kad galėtumėte pasiekti programų lenteles, kuriose yra išsami informacija apie Intrastat operacijas.

1. **Modelio žemėlapio kūrimo įrankis** puslapyje, **Duomenų šaltinio tipai** juostoje, pasirinkite **Dynamics 365 for Operations\\Lentelės įrašai**.
2. Viduje konors **Duomenų šaltinis** sritį, pasirinkite **Pridėti šaknį** pridėti naują duomenų šaltinį, kuris bus naudojamas pasiekti **Intrastatas** stalo. Kiekvienas įrašas **Intrastatas** lentelė vaizduoja vieną Intrastato operaciją.
3. Viduje konors **Duomenų šaltinio savybės** dialogo lange **vardas** lauką, įveskite **Sandoris**.
4. Viduje konors **Lentelė** lauką, įveskite **Intrastatas**.
5. Pasirinkite **Gerai** tam, kad įtrauktumėte naują duomenų šaltinį.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a> Pridėkite duomenų šaltinį prie Intrastato operacijų grupės

Konfigūruoti a **Grupuoti pagal** duomenų šaltinis Intrastato operacijoms grupuoti ir suvestinėms funkcijoms apskaičiuoti.

1. Ant **Modelių žemėlapių kūrėjas** puslapyje, esančiame **Duomenų šaltinių tipai** sritį, pasirinkite **Funkcijos\\ Grupuoti pagal**.
2. Viduje konors **Duomenų šaltinis** sritį, pasirinkite **Pridėti šaknį** pridėti naują duomenų šaltinį, kuris bus naudojamas Intrastato operacijoms grupuoti ir suvestinėms funkcijoms apskaičiuoti.
3. Viduje konors **Duomenų šaltinio savybės** dialogo lange **vardas** lauką, įveskite **TransportRecord**.
4. Pasirinkite **Redaguoti grupę pagal** grupavimo sąlygoms konfigūruoti.
5. Ant **Redaguokite „Grupuoti pagal“ parametrus** puslapyje, dešiniojoje srityje esančiame duomenų šaltinių sąraše pasirinkite **Sandoris** duomenų šaltinį ir išplėskite jį.
6. Pasirinkite **Pridėti lauką prie \> Ką sugrupuoti** nurodyti, kad **Sandoris** duomenų šaltinis pasirinktas kaip <a name="BaseDataSource">bazinis duomenų šaltinis</a> sukonfigūruotiems **Grupuoti pagal** duomenų šaltinis. Įrašai apie **Sandoris** duomenų šaltinis bus sugrupuotas, o šio duomenų šaltinio lauko reikšmės bus naudojamos skaičiuojant suvestinėse funkcijose.
7. Pasirinkite **Sandoris\Transportas** lauką, tada pasirinkite **Pridėti lauką prie \> Sugrupuotas laukas** nurodyti, kad **Transportas** bazinio duomenų šaltinio laukas pasirenkamas kaip <a name="GroupingFields">grupavimo kriterijus</a> sukonfigūruotiems **Grupuoti pagal** duomenų šaltinis. Kitaip tariant, įrašai apie **Sandoris** duomenų šaltinis bus sugrupuotas pagal reikšmę **Transportas** lauke. Kiekvienas sukonfigūruotas įrašas **Grupuoti pagal** duomenų šaltinis atstovaus vienam transportavimo kodui, kuris buvo rastas bazinio duomenų šaltinio įrašuose.
8. Pasirinkite **Sandoris\SumaMST** lauką, tada atlikite šiuos veiksmus:

    1. Pasirinkite **Pridėti lauką prie \> Suvestiniai laukai** nurodyti, kad an<a name="AggregateFunctions">agregatinė funkcija</a> bus skaičiuojamas šiam laukui.
    2. Viduje konors **Agregacijos** srityje, įraše, kuris buvo pridėtas prie pasirinkto **Sandoris\SumaMST** lauke, **Metodas** lauką, pasirinkite **Suma** funkcija.
    3. Viduje konors **vardas** pasirenkamas laukas, įveskite **TotalInvoicedAmount**.

    Šie nustatymai nurodo, kad kiekvienai transporto grupei bendra suma **Sandoris\SumaMST** laukas bus apskaičiuojamas.

9. Pasirinkite **Sandoris\RecId** lauką, tada atlikite šiuos veiksmus:

    1. Pasirinkite **Pridėti lauką prie \> Suvestiniai laukai** nurodyti, kad šiam laukui bus apskaičiuota suminė funkcija.
    2. Viduje konors **Agregacijos** srityje, įraše, kuris buvo pridėtas prie pasirinkto **Sandoris\RecId** lauke, **Metodas** lauką, pasirinkite **Suskaičiuoti** funkcija.
    3. Viduje konors **vardas** pasirenkamas laukas, įveskite **Operacijų skaičius**.

    Šie nustatymai nurodo, kad kiekvienai transporto grupei bus skaičiuojamas operacijų skaičius grupėje.

10. Pasirinkite **Įrašyti**.
11. Peržiūrėkite<a name="ExecutionLocation">egzekucija</a> redaguojamo duomenų šaltinio parametrus. Pastebėti, kad **Automatiškai aptikti** buvo automatiškai pasirinktas **Vykdymo vieta** laukas ir **Egzekucija val** lauke yra reikšmė **SQL**. Šie nustatymai nurodo, kad pasirinkta **Sandoris** bazinio duomenų šaltinio šiuo metu galima užklausti ir galite paleisti redaguojamą **Grupuoti pagal** duomenų šaltinis duomenų bazės lygiu.
12. Atidarykite paiešką **Vykdymo vieta** lauką, kad peržiūrėtumėte galimų reikšmių sąrašą. Atkreipkite dėmesį, kad galite pasirinkti **Užklausa** arba **Atmintyje** priversti tai **Grupuoti pagal** duomenų šaltinis, kuris turi būti paleistas duomenų bazės lygiu arba taikomųjų programų serverio atmintyje.
13. Pasirinkite **Sutaupyti** ir uždarykite **Redaguokite „Grupuoti pagal“ parametrus** puslapį.
14. Pasirinkite **Gerai** norėdami užbaigti nustatymus **Grupuoti pagal** duomenų šaltinis.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a> Susieti GroupBy duomenų šaltinį su duomenų modelio laukais

Susiekite sukonfigūruotą duomenų šaltinį su duomenų modelio laukais, kad nurodytumėte, kaip duomenų modelis bus užpildytas programos duomenimis vykdymo metu.

1. Ant **Modelių žemėlapių kūrėjas** puslapyje, esančiame **Duomenų modelis** sritį, išplėskite **Transportas** mazgas.
2. Viduje konors **Duomenų šaltinis** sritį, išplėskite **TransportRecord** duomenų šaltinis.
3. Pridėkite susiejimą, kad būtų rodomas aptiktų transporto grupių sąrašas:

    1. Viduje konors **Duomenų modelis** sritį, pasirinkite **Transportas** daiktas.
    2. Viduje konors **Duomenų šaltinis** sritį, pasirinkite **TransportRecord** duomenų šaltinis.
    3. Pasirinkite **Susieti**.

4. Pridėkite susiejimą, kad atskleistumėte kiekvienos aptiktos transporto grupės transportavimo kodą:

    1. Pasirinkite **Transportas.Kodas** duomenų modelio elementas.
    2. Pasirinkite **TransportRecord.grouped.TransportMode** sugrupuotas laukas.
    3. Pasirinkite **Susieti**.

5. Pridėkite susiejimą, kad parodytumėte kiekvienos aptiktos transporto grupės apskaičiuotų suvestinių funkcijų reikšmes:

    1. Pasirinkite **Transportas.NumberOfTransactions** duomenų modelio elementas.
    2. Pasirinkite **TransportRecord.aggregated.NumberOfTransactions** agreguotas laukas.
    3. Pasirinkite **Susieti**.
    4. Pasirinkite **Transport.TotalInvoicedAmount** duomenų modelio elementas.
    5. Pasirinkite **TransportRecord.aggregated.TotalInvoicedAmount** agreguotas laukas.
    6. Pasirinkite **Susieti**.

6. Pridėkite susiejimą, kad atskleistumėte operacijų įrašus, priklausančius kiekvienai aptiktai transportavimo grupei:

    1. Pasirinkite **Transportas. Sandoris** duomenų modelio elementas.
    2. Pasirinkite **TransportRecord.lines** lauke.
    3. Pasirinkite **Susieti**.

    Galite ir toliau konfigūruoti įdėtųjų elementų susiejimą **Transportas. Sandoris** duomenų modelio elementą ir **TransportRecord.lines** duomenų šaltinio lauką, kad vykdymo metu būtų rodoma informacija apie Intrastat operacijas, priklausančias kiekvienai aptiktai transporto grupei.

![Konfigūruotas žemėlapio modelis ER duomenų žemėlapio modelio kūrimo įrankyje.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Derinkite pridėtą modelio susiejimo komponentą

Naudoti [ER duomenų šaltinio derinimo priemonė](er-debug-data-sources.md) Norėdami išbandyti sukonfigūruotą modelio atvaizdavimą.

1. Ant **Modelių žemėlapių kūrėjas** puslapį, pasirinkite **Pradėkite derinti**.
2. Ant **Derinti duomenų šaltinius** puslapyje, kairiojoje srityje pasirinkite **TransportRecord** duomenų šaltinį, tada pasirinkite **Skaityti visus įrašus**.
3. Išplėskite **TransportRecord** duomenų šaltinį, tada atlikite šiuos veiksmus:

    1. Pasirinkite **TransportRecord.grouped.TransportMode** duomenų šaltinis.
    2. Pasirinkti **Gauti reikšmę**.
    3. Pasirinkite **TransportRecord.grouped.NumberOfTransactions** duomenų šaltinis.
    4. Pasirinkti **Gauti reikšmę**.
    5. Pasirinkite **TransportRecord.grouped.TotalInvoicedAmount** duomenų šaltinis.
    6. Pasirinkti **Gauti reikšmę**.

4. Dešinėje srityje pasirinkite **Išplėsti viską**.

The **TransportRecord** duomenų šaltinis atskleidžia du įrašus ir pateikia du transportavimo kodus. Kiekvienam transporto kodui apskaičiuojamas operacijų skaičius ir bendra sąskaitoje faktūroje nurodyta suma.

> [!NOTE]
> „tinginio skaitymo“ metodas naudojamas, kai a **Grupuoti pagal** duomenų šaltinis iškviečiamas optimizuoti duomenų bazės skambučius. Todėl kai kurios lauko reikšmės a **Grupuoti pagal** duomenų šaltinis apskaičiuojamas ER duomenų šaltinio derinimo priemonėje tik tada, kai yra susieti su duomenų modelio laukais.

![Duomenų šaltinio derinimo rezultatai puslapyje Derinimo duomenų šaltiniai.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Dažniausiai užduodami klausimai

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Ar yra koks nors būdas apskaičiuoti bendrąsias sumas, kai skaičiuojamos grupės sumos?

Taip. Norėdami apskaičiuoti bendras sumas, sukonfigūruokite kitą **Grupuoti pagal** duomenų šaltinis, kuriame **Grupuoti pagal** duomenų šaltinis, kurį anksčiau sukonfigūravote, naudojamas kaip bazinis duomenų šaltinis. Toliau pateiktoje iliustracijoje rodomas **GroupBy** tipo bendrųjų sumų **duomenų šaltinis**, naudojamas agreguotai **SUM** apskaičiuoti, remiantis **GroupBy** tipo TransportRecord **duomenų šaltinio** SUM **agregavimu**.

![Bendrąsias duomenų šaltinis ER modelių susiejimo dizaino sąskdyte.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Toliau pateiktoje iliustracijoje rodomi duomenų šaltinio **Sumos** derinimo rezultatai.

![Bendrųjų duomenų šaltinio derinimo rezultatai puslapyje Derinimo duomenų šaltiniai.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)
- [Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti](er-debug-data-sources.md)
- [DUOMENŲ RINKIMO duomenų šaltinių naudojimas elektroninių ataskaitų formatuose](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
