---
title: STRINGJOIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama STRINGJOIN elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 10a98e98d913b0b4fe36690f7effd5d8d9a3faf4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041796"
---
# <a name="STRINGJOIN">STRINGJOIN ER funkcija</a>

[!include [banner](../includes/banner.md)]

`STRINGJOIN` funkcija grąžina *Eilutės* reikšmę, kurią sudaro sujungtos nurodyto lauko, esančio nurodytame sąraše, reikšmės. Reikšmes galima skirti nurodytu skyrikliu.

## <a name="syntax"></a>Sintaksė

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`field`: *Laukas*

Tinkamas *Eilutės* duomenų tipo lauko maršrutas nurodytame sąraše.

`delimiter`: *Eilutė*

Skyriklis, naudojamas antrinėms eilutėms atskirti.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

Jei `SPLIT("abc" , 1)`įvesite kaip duomenų šaltinio **DS**, išraiška `STRINGJOIN (DS, DS.Value, "-")`grąžins **„a-b-c“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)
