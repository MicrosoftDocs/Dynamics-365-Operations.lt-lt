---
title: ROUNDDOWN ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama ROUNDDOWN elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: e0fa2c92fe63c3c89548b5cc23dd714d3d7589af
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286096"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN ER funkcija

[!include [banner](../includes/banner.md)]

`ROUNDDOWN` funkcija grąžina nurodytą skaičių kaip *realiojo skaičiaus* reikšmę, suapvalintą su trūkumu iki nurodyto skaičiaus po kablelio.

## <a name="syntax"></a>Sintaksė

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumentai

`number`: *Realusis*

Skaitinė reikšmė, kurią reikia apvalinti su trūkumu.

`decimals`: *Sveikasis*

Skaitinė reikšmė, nurodanti skaičių po kablelio.

## <a name="return-values"></a>Grįžties vertės

*Tikrasis*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Ši funkcija veikia kaip ir [ROUND](er-functions-mathematical-round.md), bet ji visada apvalina nurodytą skaičių į mažesnę pusę (link nulio).

## <a name="example-1"></a>1 pavyzdys

`ROUNDDOWN (1200.767, 2)` suapvalina su trūkumu iki dviejų skaičių po kablelio ir grąžina **1200,76**. 

## <a name="example-2"></a>2 pavyzdys

`ROUNDDOWN (1700.767, -3)` suapvalina su trūkumu iki artimiausio 1000 kartotinio ir grąžina **1000**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Matematinės funkcijos](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
