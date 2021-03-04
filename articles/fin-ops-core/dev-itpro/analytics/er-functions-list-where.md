---
title: WHERE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama WHERE elektroninių ataskaitų (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cc47c5001cf456b1fc600b326f826ea3b8b43ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687055"
---
# <a name="where-er-function"></a>WHERE ER funkcija

[!include [banner](../includes/banner.md)]

`WHERE` funkcija grąžina nurodytą sąrašą kaip *Įrašų sąrašo* reikšmę, baigus ją filtruoti pagal nurodytą sąlygą.

## <a name="syntax"></a>Sintaksė

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`condition`: *Bulio logika*

Tinkama sąlyginė išraiška, naudojama nurodyto sąrašo įrašams filtruoti.

## <a name="return-values"></a>Grįžties vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Ši funkcija skiriasi nuo funkcijos [FILTER](er-functions-list-filter.md), nes nurodyta sąlyga taikoma bet kuriam elektroninių ataskaitų (ER) duomenų šaltiniui, kurio tipas – *Įrašų sąrašas*.

Jei argumentais, kurie sukonfigūruoti šiai funkcijai (`list` ir `condition`), galima siųsti užklausą paversti į tiesioginį SQL skambutį, kuriant rodomas įspėjamasis pranešimas. Šis pranešimas informuoja vartotoją, kad našumas gali būti pagerintas, jei funkcija [FILTER](er-functions-list-filter.md) naudojama vietoj funkcijos `WHERE`.

## <a name="example-1"></a>1 pavyzdys

Jei **Tiekėjas** sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę „VendTable“, išraiška `WHERE (Vendors, Vendors.VendGroup = "40")` grąžina tik tų tiekėjų, kurie priklauso 40 tiekėjų grupei, sąrašą.

## <a name="example-2"></a>2 pavyzdys

Jei įvedate duomenų šaltinį **DS**, kurio tipas – *Apskaičiuotasis laukas*, ir jame yra išraiška `SPLIT ("A|B|C", "|")`, `WHERE( DS, DS.Value = "B")`išraiška grąžina tik vieno įrašo sąrašą, kuriame yra tekstas **„B“** lauke **Reikšmė**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]