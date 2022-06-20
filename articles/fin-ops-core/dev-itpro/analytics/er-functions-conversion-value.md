---
title: ER VALUE funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama funkcija VALUE Electronic Reporting (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: e96d274962ad79969a3158f7e352d3c72bd4072c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892986"
---
# <a name="value-er-function"></a>ER VALUE funkcija

[!include [banner](../includes/banner.md)]

`VALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos eilutės.

## <a name="syntax"></a>Sintaksė

```vb
VALUE (text)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Eilutės reikšmė, kurią reikia konvertuoti į skaitinę reikšmę.

## <a name="return-values"></a>Pateikiamos reikšmės

*Tikrasis*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas. Jei nurodytoje eilutėje yra kitų neskaitinių simbolių, vykdant pateikiama išimtis.

## <a name="example-1"></a>1 pavyzdys

`VALUE ("1 234,56")` pateikia išimtį.

## <a name="example-2"></a>2 pavyzdys

`VALUE ("1234,56")` pateikia **1234,56**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tipų konvertavimo funkcijos](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]