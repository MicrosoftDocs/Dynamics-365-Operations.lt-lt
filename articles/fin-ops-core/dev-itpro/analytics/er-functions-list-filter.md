---
title: ER FILTER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) FILTER funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2783fbfa0ba45c8d3772cf9ca16d110549d227b4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917378"
---
# <a name="FILTER">ER FILTER funkcija</a>

[!include [banner](../includes/banner.md)]

`FILTER` funkcija pateikia nurodytą sąrašą kaip tipo *Įrašų sąrašas* reikšmę, užklausą pakeitus taip, kad ji taikytų nurodytos sąlygos filtrą.

## <a name="syntax"></a>Sintaksė

```
FILTER (list, condition)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`condition`: *Bulio logika*

Tinkama sąlyginė išraiška, naudojama nurodyto sąrašo įrašams filtruoti.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Ši funkcija skiriasi nuo funkcijos [WHERE](er-functions-list-where.md), nes nurodyta sąlyga duomenų bazės lygiu taikoma bet kuriam modulio Elektroninės ataskaitos (ER) duomenų šaltiniui, kurio tipas – *Lentelės įrašai*. Sąrašą ir sąlygas galima nustatyti naudojant lenteles ir ryšius.

Jei vienu ar abiem argumentais, kurie sukonfigūruoti šiai funkcijai (`list` ir `condition`), negalima siųsti šios užklausos paversti į tiesioginę SQL iškvietą, kuriant pateikiama išimtis. Ši išimtis vartotoją informuoja, kad arba `list`, arba `condition` negalima naudoti norint teikti duomenų bazės užklausą.

## <a name="example-1"></a>1 pavyzdys

Jei **Tiekėjas** sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `FILTER (Vendors, Vendors.VendGroup = "40")` pateikia tik tų tiekėjų, kurie priklauso 40 tiekėjų grupei, sąrašą.

## <a name="example-2"></a>2 pavyzdys

Jei **Tiekėjas** sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, o **parmVendorBankGroup** sukonfigūruotas kaip ER duomenų šaltinis, pateikiantis duomenų tipo *Eilutė* reikšmę, reiškinys `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` pateikia tik tų tiekėjų, kurie priklauso konkrečiai banko grupei, sąskaitų sąrašą.

## <a name="example-3"></a>3 pavyzdys

Įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A,B,C", ",")`. Tada įvedate kitą reiškinį `FILTER( DS, DS.Value = "B")`. Šį reiškinį bandant įrašyti ER formulių kūrimo įrankyje, pateikiama tokia išimtis: „Tikrinimo klaida: FILTER funkcijos sąrašo reiškinio užklausų teikti negalima.“

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)
