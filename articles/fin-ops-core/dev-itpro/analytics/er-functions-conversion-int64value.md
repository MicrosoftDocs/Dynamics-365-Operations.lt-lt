---
title: INT64VALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) INT64VALUE funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042693"
---
# <a name="INT64VALUE">INT64VALUE ER funkcija</a>

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
