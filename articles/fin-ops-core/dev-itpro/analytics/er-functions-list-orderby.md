---
title: ER ORDERBY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ORDERBY funkcija.
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
ms.openlocfilehash: 963d55bcf98a9109c8b6ceb57edf5b55f15a2b0f
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075179"
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
> Šią sintaksę palaiko „Microsoft“.Dynamics 365 Finance 10.0.25 ir naujesnės versijos.

## <a name="arguments"></a>Argumentai

`location`:*[Styga](er-formula-supported-data-types-primitive.md#string)*

Vieta, kurioje turėtų būti vykdomas rūšiavimas. Galioja šios parinktys:

- "Užklausa"
- "Atmintyje"

`list`:*[Įrašų sąrašas](er-formula-supported-data-types-composite.md#record-list)*

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

Duomenų rūšiavimas visada atliekamas programų serverio atmintyje. Norėdami gauti daugiau informacijos, žr [1 pavyzdys](#example-1).

### <a name="syntax-2"></a>Sintaksė 2

### <a name="sorting-in-memory"></a>Rūšiavimas atmintyje

Kai`location` argumentas nurodytas kaip **Atmintyje**, duomenų rūšiavimas atliekamas programų serverio atmintyje. Norėdami gauti daugiau informacijos, žr [2 pavyzdys](#example-2).

### <a name="sorting-in-database"></a>Rūšiavimas duomenų bazėje

Kai`location` argumentas nurodytas kaip **Užklausa**, duomenų rūšiavimas atliekamas duomenų bazės lygiu. Šiuo atveju,`list` argumentas turi nurodyti vieną iš šių dalykų [Elektroninis ataskaitų teikimas (ER)](general-electronic-reporting.md) duomenų šaltiniai, nurodantys programos šaltinį, kuriam galima sukurti tiesioginę duomenų bazės užklausą:

- Duomenų šaltinis *Stalo įrašai* tipo
- Duomenų šaltinio ryšys *Stalo įrašai* tipo
- Duomenų šaltinis *Skaičiavimo laukas* tipo

The`expression 1` ir`expression N` argumentai turi nurodyti ER duomenų šaltinio laukus, kurie nurodo atitinkamus programos šaltinio laukus, kuriems taip pat galima nustatyti tiesioginę duomenų bazės užklausą.

Jei tiesioginės duomenų bazės užklausos nustatyti nepavyksta, patvirtinimas [klaida](er-components-inspections.md#i18) įvyksta ER modelio atvaizdavimo projektuotoje. Gautame pranešime teigiama, kad ER reiškinio, apimančio funkciją `ORDERBY`, negalima vykdyti vykdymo metu.

Siekiant geresnio veikimo, rekomenduojame naudoti **Užklausa** parinktis, kai rūšiavimas sukonfigūruotas taikomųjų programų duomenų šaltiniams, kuriuose gali būti daug įrašų (pavyzdžiui, operacijų taikomųjų programų lentelėms).

> [!NOTE]
> The`ORDEBY` pati funkcija negali būti išversta į tiesioginę duomenų bazės užklausą. Todėl ER duomenų šaltinio, kuriame yra ši funkcija, užklausa negalima. Jis taip pat negali būti naudojamas atliekant ER funkcijas, pvz.,[FILTRAS](er-functions-list-filter.md) ir [ALLITEMSQUERY](er-functions-list-allitemsquery.md), kur galima naudoti tik užklausų duomenų šaltinius.

Norėdami gauti daugiau informacijos, žr [3 pavyzdys](#example-3) ir [4 pavyzdys](#example-4).

### <a name="comparability"></a>Palyginamumas

Kadangi SQL duomenų bazės variklis ir programos „Finance“ serveris vienam simboliui gali naudoti skirtingą reitingavimo reikšmę, to paties įrašų sąrašo rūšiavimo rezultatas gali skirtis, kai [Styga](er-formula-supported-data-types-primitive.md#string) rūšiavimui naudojamas laukas. Norėdami gauti daugiau informacijos, žr [5 pavyzdys](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a> 1 pavyzdys: numatytasis vykdymas atmintyje

Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( ORDERBY( DS, DS. Value)).Value` pateikia teksto reikšmę **„A“**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a> 2 pavyzdys: aiškus vykdymas atmintyje

Jeigu **Pardavėjas** yra sukonfigūruotas kaip ER duomenų šaltinis *Stalo įrašai* tipas, kuris nurodo **Pardavimo lentelė** lentelė, tiek išraiška`ORDERBY (Vendor, Vendor.'name()')` ir išraiška`ORDERBY ("InMemory", Vendor, Vendor.'name()')` grąžinti tiekėjų sąrašą, surūšiuotą pagal pavadinimą didėjančia tvarka.

Kai konfigūruojate išraišką`ORDERBY ("Query", Vendor, Vendor.'name()')` ER modelio kartografavimo projektuotoje – patvirtinimas [klaida](er-components-inspections.md#i8) įvyksta projektavimo metu, nes`Vendor.'name()'` kelias nurodo taikymo metodą, kurio logika negali būti išversta į tiesioginę duomenų bazės užklausą.

## <a name="example-3-database-query"></a><a name="example-3"></a> 3 pavyzdys: duomenų bazės užklausa

Jeigu **TaxTransaction** yra sukonfigūruotas kaip ER duomenų šaltinis *Stalo įrašai* tipas, kuris nurodo **TaxTrans** lentelė, išraiška`ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` rūšiuoja įrašus programų duomenų bazės lygiu ir pateikia mokesčių operacijų sąrašą, kuris surūšiuotas pagal mokesčių kodą didėjančia tvarka.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a> 4 pavyzdys: užklausų duomenų šaltiniai

Jeigu **TaxTransaction** yra sukonfigūruotas kaip ER duomenų šaltinis *Stalo įrašai* tipas, kuris nurodo **TaxTrans** stalas, **TaxTransactionFiltered** ER duomenų šaltinį galima sukonfigūruoti taip, kad jame būtų išraiška`FILTER(TaxTransaction, TaxCode="VAT19")` kad bus pateiktos nurodyto mokesčių kodo operacijos. Kadangi sukonfigūruotas **TaxTransactionFiltered** ER duomenų šaltinis yra užklausa, išraiška`ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` galima sukonfigūruoti taip, kad būtų pateiktas filtruotų mokesčių operacijų sąrašas, surūšiuotas pagal operacijos datą didėjančia tvarka.

Jei sukonfigūruosite **TaxTransactionOrdered** kaip ER duomenų šaltinis *Apskaičiuotas laukas* tipas, kuriame yra išraiška`ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` ir ER duomenų šaltinis *Apskaičiuotas laukas* tipas, kuriame yra išraiška`FILTER(TaxTransactionOrdered, TaxCode="VAT19")`, patvirtinimas [klaida](er-components-inspections.md#i18) įvyksta projektavimo metu ER modelio atvaizdavimo projektuotoje. Ši klaida atsiranda dėl to, kad pirmasis argumentas [FILTRAS](er-functions-list-filter.md#usage-notes) funkcija turi nurodyti ER duomenų šaltinį, už kurį galima pateikti užklausą, tačiau **TaxTransactionOrdered** duomenų šaltinis, kuriame yra`ORDERBY` funkcija nėra užklausa.

## <a name="example-5-comparability"></a><a name="example-5"></a> 5 pavyzdys: palyginamumas

### <a name="prerequisites"></a>Būtinieji komponentai

1. Įveskite duomenų šaltinį **DS1** iš *Apskaičiuotas laukas* tipas, kuriame yra išraiška `SPLIT ("D1|_D2|D3", "|")`.
2. Atidaryk **[Finansinės dimensijos reikšmės](../../../finance/general-ledger/financial-dimensions.md)** puslapį ir pasirinkite **CostCenter** matmuo.
3. Įveskite šias matmenų reikšmes: **D1**,**\_ D2**, ir **D3**.

### <a name="sorting-in-memory"></a>Rūšiavimas atmintyje

1. Konfigūruoti duomenų šaltinį **DS2** iš *Apskaičiuotas laukas* tipas, kuriame yra išraiška `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Atkreipkite dėmesį, kad išraiška`FIRST(DS2).Value` grąžina teksto reikšmę **"D1"**, išsireiškimas`INDEX(DS2, COUNT(DS2)).Value` grąžina teksto reikšmę **“\_ D2"**, ir išraiška`STRINGJOIN(DS2, DS2.Value, "|")` grąžina teksto reikšmę **"D1\| D3\|\_ D2"**.

### <a name="sorting-in-database"></a>Rūšiavimas duomenų bazėje

1. Įveskite duomenų šaltinį **DS3** iš *Stalo įrašai* tipas, kuris nurodo **FinancialDimensionValueEntity** subjektas.
2. Konfigūruoti duomenų šaltinį **DS4** iš *Apskaičiuotas laukas* tipas, kuriame yra išraiška `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Konfigūruoti duomenų šaltinį **DS5** iš *Apskaičiuotas laukas* tipas, kuriame yra išraiška `ORDERBY(DS4, DS4.DimensionValue)`.
4. Atkreipkite dėmesį, kad išraiška`FIRST(DS5).Value` grąžina teksto reikšmę **“\_ D2"**, išsireiškimas`INDEX(DS5, COUNT(DS5)).Value` grąžina teksto reikšmę **"D3"**, ir išraiška`STRINGJOIN(DS5, DS5.Value, "|")` grąžina teksto reikšmę **“\_ D2\| D1\| D3"**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
