---
title: ISVALIDCHARACTERISO7064 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ISVALIDCHARACTERISO7064 elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563371"
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