---
title: ISVALIDCHARACTERISO7064 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ISVALIDCHARACTERISO7064 elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680667"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 ER funkcija

[!include [banner](../includes/banner.md)]

`ISVALIDCHARACTERISO7064` funkcija grąžina *Bulio logikos* reikšmę **TRUE**, jei nurodyta eilutė rodo tinkamą tarptautinį banko sąskaitos numerį (IBAN). Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.

## <a name="syntax"></a>Sintaksė

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tekstinė reikšmė, kuri nurodo IBAN.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` grąžina **TEISINGA**. 

`ISVALIDCHARACTERISO7064 ("AT61")` grąžina **KLAIDINGA**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]