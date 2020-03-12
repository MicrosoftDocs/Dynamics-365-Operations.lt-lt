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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040876"
---
# <a name="RIGHT">RIGHT ER funkcija</a>

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
