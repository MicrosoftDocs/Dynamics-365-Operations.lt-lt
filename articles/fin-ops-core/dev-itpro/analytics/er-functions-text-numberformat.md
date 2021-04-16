---
title: NUMBERFORMAT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NUMBERFORMAT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746223"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER funkcija

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]