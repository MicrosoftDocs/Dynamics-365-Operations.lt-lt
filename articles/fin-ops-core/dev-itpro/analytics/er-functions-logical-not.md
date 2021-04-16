---
title: NOT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NOT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751724"
---
# <a name="not-er-function"></a>NOT ER funkcija

[!include [banner](../includes/banner.md)]

`NOT` funkcija grąžina nurodytos sąlygos atvirkštinės reikšmės loginę reikšmę kaip *Bulio logikos* reikšmę.

## <a name="syntax"></a>Sintaksė

```vb
NOT (condition)
```

## <a name="arguments"></a>Argumentai

`condition`: *Bulio logika*

Tinkama sąlyginė išraiška, kuri turi būti atvirkščiai perdaryta.

## <a name="return-values"></a>Grįžimo vertės

*Būlio logika*

Gaunama *Bulio logikos* reikšmė.

## <a name="example"></a>Pavyzdys

`NOT (TRUE)` grąžina **KLAIDINGA**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]