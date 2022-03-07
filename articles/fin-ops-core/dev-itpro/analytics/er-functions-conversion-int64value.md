---
title: INT64VALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) INT64VALUE funkcija.
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
ms.openlocfilehash: 375117745b90b9e3e0e15ea45605de5bee6f133e6366d08adf5bae98423abd71
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748429"
---
# <a name="int64value-er-function"></a>INT64VALUE ER funkcija

[!include [banner](../includes/banner.md)]

`INT64VALUE` funkcija pateikia *Int64* reikšmę, kuri nurodo nurodytą eilutę.

## <a name="syntax-1"></a>1-oji sintaksė

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>2-oji sintaksė

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Teksto reikšmė, kurią reikia konvertuoti į *Int64* skaičių.

`number`: *Realusis* arba *Sveikasis*

Skatinė tipo *Realusis skaičius* arba *Sveikasis skaičius* reikšmė, kurią reikia konvertuoti į *Int64* skaičių.

## <a name="return-values"></a>Pateikiamos reikšmės

*Int64*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Visi skaičiai po kablelio pašalinami.

## <a name="example-1"></a>1 pavyzdys

`INT64VALUE ("22565422744")` pateikia *Int64* reikšmę **22565422744**.

## <a name="example-2"></a>2 pavyzdys

`INT64VALUE ( VALUE("22565422744.77"))` pateikia *Int64* reikšmę **22565422744**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tipų konvertavimo funkcijos](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]