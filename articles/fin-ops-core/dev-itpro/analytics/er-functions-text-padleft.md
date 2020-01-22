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
ms.openlocfilehash: 28306b2e5fb1febce49ab55240c6d84ff240282a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916780"
---
# <a name="PADLEFT">PADLEFT ER funkcija</a>

[!include [banner](../includes/banner.md)]

`PADLEFT` grąžina nurodyto ilgio *Eilutės* reikšmę, kurioje nurodytos eilutės pradžia užpildyta nurodytais simboliais.

## <a name="syntax"></a>Sintaksė

```
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
