---
title: ER ISEMPTY funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama ISEMPTY elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e1f1ac1cc1729ef6d0f0301f12cc3f4b07fc6110
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273225"
---
# <a name="isempty-er-function"></a>ER ISEMPTY funkcija

[!include [banner](../includes/banner.md)]

Jei nurodytame sąraše nėra įrašų, `ISEMPTY` funkcija pateikia *Bulio logikos* reikšmę **TRUE**. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.

## <a name="syntax"></a>Sintaksė

```vb
ISEMPTY (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

## <a name="return-values"></a>Pateikiamos reikšmės

*Būlio logika*

Gaunama *Bulio logikos* reikšmė.

## <a name="example-1"></a>1 pavyzdys

Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `ISEMPTY(DS)` pateikia **FALSE**.

## <a name="example-2"></a>2 pavyzdys

Reiškinys `ISEMPTY (SPLIT ("",1))` pateikia **TRUE**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
