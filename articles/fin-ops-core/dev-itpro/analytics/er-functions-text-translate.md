---
title: TRANSLATE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TRANSLATE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040922"
---
# <a name="TRANSLATE">TRANSLATE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`TRANSLATE` funkcija grąžina nurodytą teksto eilutę kaip *Eilutės* reikšmę po to, kai visa arba jos dalis buvo pakeista kita eilute.

## <a name="syntax"></a>Sintaksė

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.

`pattern`: *Eilutė*

Tekstas, kuris turi būti pakeistas.

`replacement`: *Eilutė*

Tekstas, kurį norite naudoti kaip pakaitą.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`TRANSLATE ("abcdef", "cd", "GH")` pakeičia šabloną **„cd“** į eilutę **„GH“** ir grąžinama **„abGHef“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
