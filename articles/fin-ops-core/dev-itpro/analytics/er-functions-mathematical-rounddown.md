---
title: ROUNDDOWN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ROUNDDOWN elektroninių ataskaitų (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686887"
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