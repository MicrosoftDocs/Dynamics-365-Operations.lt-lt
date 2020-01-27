---
title: CONCATENATE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CONCATENATE elektroninių ataskaitų (ER) funkcija
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915768"
---
# <a name="CONCATENATE">CONCATENATE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`CONCATENATE` funkcija grąžina visas nurodytas teksto eilutes kaip *Eilutės* reikšmę, sujungus jas į vieną eilutę.

## <a name="syntax"></a>Sintaksė

```
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
