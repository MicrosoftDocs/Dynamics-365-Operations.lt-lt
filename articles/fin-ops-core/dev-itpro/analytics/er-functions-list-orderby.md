---
title: ER ORDERBY funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ORDERBY funkcija.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753197"
---
# <a name="orderby-er-function"></a>ER ORDERBY funkcija

[!include [banner](../includes/banner.md)]

`ORDERBY` funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, jį surikiavus pagal nurodytus argumentus. Šiuos argumentus galima apibrėžti kaip išraiškas.

## <a name="syntax"></a>Sintaksė

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`expression 1`: *Laukas*

Tinkamas duomenų šaltinio lauko kelias, kurį nurodo iškviestos funkcijos `list` argumentas. Nurodytas laukas turi būti primityviojo duomenų tipo. Šis argumentas yra būtinas.

`expression N`: *Laukas*

Tinkamas duomenų šaltinio lauko kelias, kurį nurodo iškviestos funkcijos `list` argumentas. Nurodytas laukas turi būti primityviojo duomenų tipo. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="example-1"></a>1 pavyzdys

Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( ORDERBY( DS, DS. Value)).Value` pateikia teksto reikšmę **„A“**.

## <a name="example-2"></a>2 pavyzdys

Jei **Tiekėjas** sukonfigūruotas kaip modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `ORDERBY (Vendors, Vendors.'name()')` pateikia tiekėjų sąrašą, surikiuotą pagal pavadinimą didėjančia tvarka.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]