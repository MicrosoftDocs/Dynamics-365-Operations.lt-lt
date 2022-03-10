---
title: ER FILTER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) FILTER funkcija.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: e857306574dda7bad5dd25fc7708514997d8e86f
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922428"
---
# <a name="filter-er-function"></a>ER FILTER funkcija

[!include [banner](../includes/banner.md)]

`FILTER` funkcija pateikia nurodytą sąrašą kaip tipo *Įrašų sąrašas* reikšmę, užklausą pakeitus taip, kad ji taikytų nurodytos sąlygos filtrą.

## <a name="syntax"></a>Sintaksė

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`condition`: *Bulio logika*

Tinkama sąlyginė išraiška, naudojama nurodyto sąrašo įrašams filtruoti.

## <a name="return-values"></a>Grįžties vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a><a name="usage-notes"></a>Naudojimo pastabos

Ši funkcija skiriasi nuo funkcijos [WHERE](er-functions-list-where.md), nes nurodyta sąlyga duomenų bazės lygiu taikoma bet kuriam modulio Elektroninės ataskaitos (ER) duomenų šaltiniui, kurio tipas – *Lentelės įrašai*. Sąrašą ir sąlygas galima nustatyti naudojant lenteles ir ryšius.

Jei vienu ar abiem argumentais, kurie sukonfigūruoti šiai funkcijai (`list` ir `condition`), negalima siųsti šios užklausos paversti į tiesioginę SQL iškvietą, kuriant pateikiama išimtis. Ši išimtis vartotoją informuoja, kad arba `list`, arba `condition` negalima naudoti norint teikti duomenų bazės užklausą.

> [!NOTE]
> Kai `FILTER` funkcija naudojama pasirinkimo kriterijams nurodyti, funkcija išsamesnė už `WHERE`[`VALUEIN`](er-functions-logical-valuein.md) funkciją.
> 
> - Jei funkcija naudojama funkcijos aprėptį, o antrasis argumentas nurodo duomenų šaltinį, kuris negrąžina `VALUEIN``WHERE``VALUEIN` įrašų, Būlio logikos klaidinga vertė, į kurią atsižvelgiama *[...](er-formula-supported-data-types-primitive.md#boolean)*`VALUEIN` grąžina. Todėl išraiška `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` negrąžina tiekėjo įrašų, jei **VendGroups duomenų** šaltinis negrąžina tiekėjų grupės įrašų.
> - Jei funkcija naudojama funkcijos aprėptį, o antrasis argumentas nurodo duomenų šaltinį, kuris negrąžina `VALUEIN``FILTER``VALUEIN` įrašų, Būlio logikos klaidinga vertė, kurios *[...](er-formula-supported-data-types-primitive.md#boolean)*`VALUEIN` grąžinimai yra ignoruojami. Todėl išraiška grąžina `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` visus tiekėjų duomenų šaltinio tiekėjo **įrašus**, net jei VendGroups duomenų šaltinis **negrąžina** tiekėjų grupės įrašų.

## <a name="example-1"></a>1 pavyzdys

Jei **Tiekėjas** sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `FILTER (Vendors, Vendors.VendGroup = "40")` pateikia tik tų tiekėjų, kurie priklauso 40 tiekėjų grupei, sąrašą.

## <a name="example-2"></a>2 pavyzdys

Jei **Tiekėjas** sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, o **parmVendorBankGroup** sukonfigūruotas kaip ER duomenų šaltinis, pateikiantis duomenų tipo *Eilutė* reikšmę, reiškinys `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` pateikia tik tų tiekėjų, kurie priklauso konkrečiai banko grupei, sąskaitų sąrašą.

## <a name="example-3"></a>3 pavyzdys

Įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A,B,C", ",")`. Tada įvedate kitą reiškinį `FILTER( DS, DS.Value = "B")`. Šį reiškinį bandant įrašyti ER formulių kūrimo įrankyje, pateikiama tokia išimtis: „Tikrinimo klaida: FILTER funkcijos sąrašo reiškinio užklausų teikti negalima.“

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
