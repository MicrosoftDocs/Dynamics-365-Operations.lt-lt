---
title: NUMBERFORMAT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NUMBERFORMAT elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070557"
---
# <a name="NUMBERFORMAT">NUMBERFORMAT ER funkcija</a>

[!include [banner](../includes/banner.md)]

`NUMBERFORMAT` funkcija grąžina *Eilutės* reikšmę, kuri pateikia nurodytą skaičių nurodytu formatu ir pasirinktinai nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

## <a name="syntax-1"></a>Sintaksė 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Sintaksė 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumentai

`number`: *Sveikasis* arba *Realusis*

Skaitinė reikšmė, nurodanti skaičių, kuris turi būti suformatuotas.

`format`: *Eilutė*

*Eilutės* reikšmė, nurodanti formatą.

`culture`: *Eilutė*

*Eilutės* reikšmė, kuri nurodo formatavimui naudoti skirtą kultūrą.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, kontekstas, kuriame vykdoma ši funkcija, nustato kultūrą, naudojamą skaičiams formatuoti.

## <a name="example-1"></a>1 pavyzdys

**EN-US** kultūrai `NUMBERFORMAT (0.45, "p")` grąžina **„45.00 %“**, o `NUMBERFORMAT (10.45, "#")` grąžina **„10“**.

## <a name="example-2"></a>2 pavyzdys

`NUMBERFORMAT (10/3, "F2", "de")` grąžina **3,33**, o `NUMBERFORMAT (10/3, "F2", "en-us")` grąžina **3.33**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
