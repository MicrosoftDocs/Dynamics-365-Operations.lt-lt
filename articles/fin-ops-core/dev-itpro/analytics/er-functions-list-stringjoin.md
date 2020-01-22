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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917194"
---
# <a name="STRINGJOIN">STRINGJOIN ER funkcija</a>

[!include [banner](../includes/banner.md)]

`STRINGJOIN` funkcija grąžina *Eilutės* reikšmę, kurią sudaro sujungtos nurodyto lauko, esančio nurodytame sąraše, reikšmės. Reikšmes galima skirti nurodytu skyrikliu.

## <a name="syntax"></a>Sintaksė

```
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
