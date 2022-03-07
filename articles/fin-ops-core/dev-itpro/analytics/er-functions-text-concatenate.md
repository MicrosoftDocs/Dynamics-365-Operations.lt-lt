---
title: CONCATENATE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CONCATENATE elektroninių ataskaitų (ER) funkcija
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1507e1b8a31ed45e7c540e4e2ff31b79e8de3b866ffbace9de17d7b3e169e877
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762505"
---
# <a name="concatenate-er-function"></a>CONCATENATE ER funkcija

[!include [banner](../includes/banner.md)]

`CONCATENATE` funkcija grąžina visas nurodytas teksto eilutes kaip *Eilutės* reikšmę, sujungus jas į vieną eilutę.

## <a name="syntax"></a>Sintaksė

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumentai

`text 1`: *Eilutė*

Nuoroda į duomenų šaltinį, kuris yra *Eilutės* duomenų tipas. Šis argumentas yra būtinas.

`text N`: *Eilutė*

Nuoroda į duomenų šaltinį, kuris yra *Eilutės* duomenų tipas. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Grįžimo vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`CONCATENATE ("abc", "def")`grąžina **„abcdef“**.

## <a name="usage-notes"></a>Naudojimo pastabos

Išraiška `"abc" & "def"` taip pat grąžina **„abcdef“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]