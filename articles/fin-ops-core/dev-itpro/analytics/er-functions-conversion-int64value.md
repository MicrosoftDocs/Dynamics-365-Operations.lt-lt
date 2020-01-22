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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916550"
---
# <a name="INT64VALUE">INT64VALUE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`INT64VALUE` funkcija pateikia *Int64* reikšmę, kuri nurodo nurodytą eilutę.

## <a name="syntax-1"></a>1-oji sintaksė

```
INT64VALUE (text)
```

## <a name="syntax-2"></a>2-oji sintaksė

```
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
