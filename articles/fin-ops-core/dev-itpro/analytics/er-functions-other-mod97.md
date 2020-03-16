---
title: MOD_97 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama MOD_97 elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: ce2192c7bc849996e08573d71d8ed43956c8fb89
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070534"
---
# <a name="MOD_97">MOD_97 ER funkcija</a>

[!include [banner](../includes/banner.md)]

`MOD_97` funkcija grąžina *Eilutės* reikšmę, kuri nurodo kreditoriaus nuorodą kaip MOD97 išraišką pagal nurodyto sąskaitos faktūros numerio skaitmenis.

## <a name="syntax"></a>Sintaksė

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>Argumentai

`invoice number digits`: *Eilutė*

Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`MOD_97 ("VEND-200002")` grąžina **„20000285“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)
