---
title: ER REVERSE funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama FUNKCIJA REVERSE Electronic Reporting (ER).
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
ms.openlocfilehash: fce611b755865db15e8877e58d59bdf36bc730fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881525"
---
# <a name="reverse-er-function"></a>ER REVERSE funkcija

[!include [banner](../includes/banner.md)]

`REVERSE` funkcija nurodytą sąrašą pateikia kaip tipo *Įrašų sąrašas* reikšmę, surikiuotą atvirkštine tvarka.

## <a name="syntax"></a>Sintaksė

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="example-1"></a>1 pavyzdys

Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("C|B|A", "|")`, reiškinys `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` pateikia teksto reikšmę **„C“**.

## <a name="example-2"></a>2 pavyzdys

Jei **Tiekėjas** sukonfigūruotas kaip modulio Elektroninės ataskaitos (ER) duomenų šaltinis, nurodantis lentelę VendTable, reiškinys `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` pateikia tiekėjų sąrašą, surikiuotą pagal pavadinimą mažėjančia tvarka.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]