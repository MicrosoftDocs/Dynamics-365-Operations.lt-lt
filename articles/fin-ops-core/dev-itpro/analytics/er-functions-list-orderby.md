---
title: ER ORDERBY funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama ORDERBY Electronic Reporting (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a922405ea23d2b1ff5ac062785e68626edbc8f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883765"
---
# <a name="orderby-er-function"></a>ER ORDERBY funkcija

[!include [banner](../includes/banner.md)]

`ORDERBY` funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, jį surikiavus pagal nurodytus argumentus. Šiuos argumentus galima apibrėžti kaip išraiškas.

## <a name="syntax-1"></a><a name="syntax-1"></a>Sintaksė 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Sintaksė 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Ši sintaksė palaikoma Microsoft Dynamics 365 10.0.25 ir vėlesnės finansinės versijos.

## <a name="arguments"></a>Argumentai

`location`: *[eilutė](er-formula-supported-data-types-primitive.md#string)*

Vieta, kurioje turi būti vykdomas rūšiavimas. Galimos šios pasirinktys:

- "Užklausa"
- "InMemory"

`list`: *[įrašų sąrašas](er-formula-supported-data-types-composite.md#record-list)*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`expression 1`: *Laukas*

Tinkamas duomenų šaltinio lauko kelias, kurį nurodo iškviestos funkcijos `list` argumentas. Nurodytas laukas turi būti primityviojo duomenų tipo. Šis argumentas yra būtinas.

`expression N`: *Laukas*

Tinkamas duomenų šaltinio lauko kelias, kurį nurodo iškviestos funkcijos `list` argumentas. Nurodytas laukas turi būti primityviojo duomenų tipo. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Grįžimo vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

### <a name="syntax-1"></a>Sintaksė 1

Duomenų rūšiavimas visada atliekamas programos serverio atmintyje. Daugiau informacijos ieškokite [1 pavyzdyje](#example-1).

### <a name="syntax-2"></a>Sintaksė 2

### <a name="sorting-in-memory"></a>Rūšiavimas atmintyje

`location` Kai argumentas nurodomas kaip **InMemory**, duomenų rūšiavimas atliekamas programos serverio atmintyje. Daugiau informacijos ieškokite [2 pavyzdyje](#example-2).

### <a name="sorting-in-database"></a>Duomenų bazės rūšiavimas

Kai argumentas `location` nurodomas kaip **Užklausa**, duomenų rūšiavimas atliekamas duomenų bazės lygiu. Tokiu atveju argumentas turi `list` nurodyti vieną iš šių elektroninių ataskaitų (ER) [duomenų šaltinių, kurie nurodo programos šaltinį,](general-electronic-reporting.md) dėl kurių gali būti nustatyta tiesioginė duomenų bazės užklausa:

- Lentelės įrašų tipo *duomenų* šaltinis
- Lentelės įrašų tipo duomenų *šaltinio* ryšys
- Skaičiavimo lauko tipo *duomenų* šaltinis

Argumentai `expression 1` turi `expression N` nurodyti ER duomenų šaltinio laukus, kurie nurodo atitinkamus programos šaltinio laukus, už kuriuos taip pat galima nustatyti tiesioginės duomenų bazės užklausą.

Jei nepavyko nustatyti tiesioginės duomenų bazės užklausos, ER modelio susiejimo [konstruktoriuje](er-components-inspections.md#i18) įvyksta tikrinimo klaida. Gautame pranešime teigiama, kad ER reiškinio, apimančio funkciją `ORDERBY`, negalima vykdyti vykdymo metu.

Kad našumas būtų geresnė, **rekomenduojame** naudoti pasirinktį Užklausa, kai rūšiavimas konfigūruojamas programos duomenų šaltiniams, kuriuose gali būti daug įrašų (pvz., operacijų programos lentelės).

> [!NOTE]
> Pačios `ORDEBY` funkcijos negalima išversti į tiesioginę duomenų bazės užklausą. Todėl ER duomenų šaltinis, kuriame yra ši funkcija, nėra užklausuojamas. Jo taip pat negalima naudoti ER [funkcijų, pvz., FILTER](er-functions-list-filter.md)[ir ALLITEMSQUERY](er-functions-list-allitemsquery.md), apimtis, kur galima naudoti tik užklausuojamus duomenų šaltinius.

Daugiau informacijos ieškokite [3 ir](#example-3)[4 pavyzdyje](#example-4).

### <a name="comparability"></a>Palyginamumą

Kadangi SQL duomenų bazės modulis ir finansų programos serveris gali naudoti skirtingą vieno simbolio vertinimo vertę, [to](er-formula-supported-data-types-primitive.md#string) paties įrašų sąrašo rūšiavimo rezultatas gali skirtis, kai rūšiuojant naudojamas eilutės laukas. Daugiau informacijos ieškokite [5 pavyzdyje](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a> 1 pavyzdys: numatytasis ne atminties vykdymas

Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( ORDERBY( DS, DS. Value)).Value` pateikia teksto reikšmę **„A“**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a> 2 pavyzdys: Tiesioginis vykdymas ne atminties

Jei **tiekėjas** sukonfigūruotas kaip lentelės įrašų tipo, kuris nurodo VendTable *lentelę, ER* **duomenų** šaltinis, išraiška ir išraiška grąžina tiekėjų sąrašą, `ORDERBY (Vendor, Vendor.'name()')``ORDERBY ("InMemory", Vendor, Vendor.'name()')` kuris surūšiuotas pagal pavadinimą didėjančia tvarka.

Konfigūruojant `ORDERBY ("Query", Vendor, Vendor.'name()')` išraišką ER modelio susiejimo konstruktoriuje, [dizaino](er-components-inspections.md#i8) metu įvyksta tikrinimo klaida, nes maršrutas nurodo programos metodą, `Vendor.'name()'` turiį logiką, kurios negalima išversti į tiesioginę duomenų bazės užklausą.

## <a name="example-3-database-query"></a><a name="example-3"></a> 3 pavyzdys: Duomenų bazės užklausa

Jei **TaxTransaction** sukonfigūruotas kaip lentelės įrašų tipo, kuris nurodo lentelę TaxTrans *, ER* **duomenų** šaltinis, `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` išraiškos rūšiavimo įrašai programos duomenų bazės lygiu ir pateikia mokesčių operacijų, kurios surūšiuotos pagal mokesčio kodą didėjančia tvarka, sąrašą.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a> 4 pavyzdys: Užklausti duomenų šaltiniai

**Jei TaxTransaction** sukonfigūruotas kaip lentelės įrašų tipo, kuris nurodo lentelę TaxTrans *, ER* **duomenų** šaltinis, **TaxTransactionFiltered** ER `FILTER(TaxTransaction, TaxCode="VAT19")` duomenų šaltinis gali būti sukonfigūruotas, kad jame būtų išraiška, kuri ieškos nurodyto mokesčio kodo operacijų. **Kadangi sukonfigūruotas TaxTransactionFiltered** ER duomenų šaltinis yra užklausuojamas, `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` išraiška gali būti sukonfigūruota pateikti filtruotų mokesčių operacijų, kurios surūšiuotos pagal operacijos datą didėjančia tvarka, sąrašą.

Jeigu TaxTransactionOrdered konfigūruojate kaip apskaičiuoto lauko tipo, kuriame yra išraiška ir apskaičiuoto lauko tipo, kuriame yra išraiška, ER duomenų šaltinį ER duomenų šaltinį, **dizaino** metu *ER*`ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)`*·*`FILTER(TaxTransactionOrdered, TaxCode="VAT19")` modelio susiejimo konstruktoriuje įvyksta tikrinimo klaida.[...](er-components-inspections.md#i18) Ši klaida įvyksta todėl, kad pirmasis filter funkcijos argumentas [turi nurodyti užklausos ER duomenų šaltinį, bet TaxTransactionOrdered](er-functions-list-filter.md#usage-notes)**duomenų šaltinis,** kuriame yra funkcija, nėra užklausuojamas.`ORDERBY`

## <a name="example-5-comparability"></a><a name="example-5"></a> 5 pavyzdys: Iš toliau pateiktas pavyzdys

### <a name="prerequisites"></a>Būtinieji komponentai

1. Įvesti apskaičiuoto lauko **tipo, kuriame yra** išraiška *, duomenų šaltinį* DS1`SPLIT ("D1|_D2|D3", "|")`.
2. Atidarykite **[finansinės dimensijos reikšmių](../../../finance/general-ledger/financial-dimensions.md)** puslapį ir pasirinkite **CostCenter dimensiją**.
3. Įveskite šias dimensijų vertes: **D1**, **\_ D2** ir **D3**.

### <a name="sorting-in-memory"></a>Rūšiavimas atmintyje

1. Konfigūruoti apskaičiuoto lauko **tipo, kuriame yra išraiška**, *šaltinį* DS2`ORDERBY("InMemory", DS1, DS1.Value)`.
2. Atkreipkite dėmesį `FIRST(DS2).Value`**, kad išraiška pateikia teksto vertę D1**,`INDEX(DS2, COUNT(DS2)).Value`**\_ išraiška grąžina teksto vertę D2**, `STRINGJOIN(DS2, DS2.Value, "|")`**o išraiškoje pateikiama teksto vertė D1\| D3\|\_ D2**.

### <a name="sorting-in-database"></a>Duomenų bazės rūšiavimas

1. Įveskite lentelės įrašų **tipo, kuris nurodo** FinancialDimensionValueEntity *·* **objektą, duomenų šaltinį DS3.**
2. Konfigūruoti apskaičiuoto lauko **tipo, kuriame yra išraiška**, *šaltinį* DS4`FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Konfigūruoti apskaičiuoto lauko **tipo, kuriame yra išraiška**, *šaltinį* DS5`ORDERBY(DS4, DS4.DimensionValue)`.
4. Atkreipkite dėmesį`FIRST(DS5).Value`**\_, kad išraiška pateikia teksto vertę D2**, `INDEX(DS5, COUNT(DS5)).Value`**išraiška grąžina teksto vertę D3**,`STRINGJOIN(DS5, DS5.Value, "|")`**\_ o išraiškoje pateikiama teksto vertė D2\| D1\| D3.**

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
