---
title: POWER ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama POWER elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750161"
---
# <a name="power-er-function"></a>POWER ER funkcija

[!include [banner](../includes/banner.md)]

`POWER` funkcija grąžina *realiojo skaičiaus* reikšmę, atsižvelgiant į rezultatą pakeliant laipsniu nurodytą teigiamą skaičių.

## <a name="syntax"></a>Sintaksė

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumentai

`number`: *Realusis* arba *Sveikasis*

Skaitinė reikšmė, kurią reikia pakelti nurodytu laipsniu.

`power`: *Realusis* arba *Sveikasis*

Skaitinė reikšmė, nurodanti konkretų laipsnį.

## <a name="return-values"></a>Grįžties vertės

*Tikrasis*

Gaunama skaitinė reikšmė.

## <a name="example-1"></a>1 pavyzdys

`POWER (10, 2)` grąžina **100**.

## <a name="example-2"></a>2 pavyzdys

`POWER (4, 0.5)` grąžina **2**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Matematinės funkcijos](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]