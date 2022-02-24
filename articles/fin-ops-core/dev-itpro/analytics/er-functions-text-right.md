---
title: RIGHT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama RIGHT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682947"
---
# <a name="right-er-function"></a>RIGHT ER funkcija

[!include [banner](../includes/banner.md)]

`RIGHT` funkcija grąžina *Eilutės* reikšmę, kurioje pateikiamas nurodytas simbolių skaičius iš nurodytos eilutės pabaigos.

## <a name="syntax"></a>Sintaksė

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

*Eilutės* reikšmė, nurodanti pradinį tekstą.

`number`: *Sveikasis*

Simbolių, kuriuos reikia grąžinti iš pradinio teksto pabaigos, skaičius.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`RIGHT ("Sample", 3)` grąžina **„dys“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
