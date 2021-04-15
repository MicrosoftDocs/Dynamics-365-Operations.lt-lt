---
title: STRINGJOIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama STRINGJOIN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: ac21651e0f5b5a1579b9335bb7f3217370c4d5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745526"
---
# <a name="stringjoin-er-function"></a>STRINGJOIN ER funkcija

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]