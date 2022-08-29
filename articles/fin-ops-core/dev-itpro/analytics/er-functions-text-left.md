---
title: LEFT ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama kairiosios elektroninės ataskaitos (ER) funkcija.
author: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 866c1b59fee9aa58afafbd82a83cff57e4cadeeb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268003"
---
# <a name="left-er-function"></a>LEFT ER funkcija

[!include [banner](../includes/banner.md)]

`LEFT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pradžios.

## <a name="syntax"></a>Sintaksė

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

*Eilutės* reikšmė, nurodanti pradinį tekstą.

`number`: *Sveikasis*

Simbolių, kuriuos reikia grąžinti iš pradinio teksto pradžios, skaičius.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`LEFT ("Sample", 3)` grąžina **„Pavyz“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
