---
title: POWER ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama POWER elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: cb768b400e3ddb99e7c8b05905d7a2dd9e4392de
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915906"
---
# <a name="POWER">POWER ER funkcija</a>

[!include [banner](../includes/banner.md)]

`POWER` funkcija grąžina *realiojo skaičiaus* reikšmę, atsižvelgiant į rezultatą pakeliant laipsniu nurodytą teigiamą skaičių.

## <a name="syntax"></a>Sintaksė

```
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
