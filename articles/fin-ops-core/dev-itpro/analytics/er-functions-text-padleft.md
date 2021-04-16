---
title: PADLEFT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama PADLEFT elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 806b1d318f18b0ade01f7b03909c90b1e4fd29b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746248"
---
# <a name="padleft-er-function"></a>PADLEFT ER funkcija

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]