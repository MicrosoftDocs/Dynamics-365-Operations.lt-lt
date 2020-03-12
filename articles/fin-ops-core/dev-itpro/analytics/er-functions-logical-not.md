---
title: NOT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NOT elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041727"
---
# <a name="NOT">NOT ER funkcija</a>

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
