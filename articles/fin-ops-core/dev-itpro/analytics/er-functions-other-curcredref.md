---
title: CURCREDREF ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CURCREDREF elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 3923126060963122634d90c2ba8a380f534e9178
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686767"
---
# <a name="curcredref-er-function"></a>CURCREDREF ER funkcija

[!include [banner](../includes/banner.md)]

`CURCREDREF` funkcija grąžina *Eilutės* reikšmę, kuri nurodo kreditoriaus nuorodą pagal nurodyto sąskaitos faktūros numerio skaitmenis.

## <a name="syntax"></a>Sintaksė

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a>Argumentai

`invoice number digits`: *Eilutė*

Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`CURCredRef ("VEND-200002")` grąžina **„2200002“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]