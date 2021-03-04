---
title: OR ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama OR elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686983"
---
# <a name="or-er-function"></a>OR ER funkcija

[!include [banner](../includes/banner.md)]

`OR` funkcija grąžina *Bulio logikos* reikšmę **KLAIDINGA**, jei visos nurodytos sąlygos yra klaidingos. Jei bet kuri nurodyta sąlyga yra teisinga, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**.

## <a name="syntax"></a>Sintaksė

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumentai

`condition 1`: *Bulio logika*

Tinkama sąlyginė išraiška, kuri turi būti patikrinta. Šis argumentas yra būtinas.

`condition N`: *Bulio logika*

Tinkama sąlyginė išraiška, kuri turi būti patikrinta. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Grįžties vertės

*Būlio logika*

Gaunama *Bulio logikos* reikšmė.

## <a name="example"></a>Pavyzdys

`OR (1=2, "a"="a")` grąžina **TEISINGA**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]