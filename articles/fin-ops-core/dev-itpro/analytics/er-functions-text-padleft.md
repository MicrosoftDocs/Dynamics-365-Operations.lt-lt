---
title: PADLEFT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama PADLEFT elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040968"
---
# <a name="PADLEFT">PADLEFT ER funkcija</a>

[!include [banner](../includes/banner.md)]

`PADLEFT` grąžina nurodyto ilgio *Eilutės* reikšmę, kurioje nurodytos eilutės pradžia užpildyta nurodytais simboliais.

## <a name="syntax"></a>Sintaksė

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

*Eilutės* reikšmė, nurodanti pradinį tekstą.

`length`: *Sveikasis*

*Sveikojo skaičiaus* reikšmė, reiškianti galutinį simbolių skaičių, esantį užpildytoje eilutėje.

`padding chars`: *Eilutė*

Simboliai, naudojami užpildant.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`PADLEFT ("1234", 10, "`&nbsp;`")` grąžina teksto eilutę **„&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
