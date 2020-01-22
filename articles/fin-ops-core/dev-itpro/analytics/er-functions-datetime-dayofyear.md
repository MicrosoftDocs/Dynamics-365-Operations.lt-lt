---
title: ER DAYOFYEAR funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DAYOFYEAR funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1080a1c2e30cd7ca64ea43120c11eb90d3c99416
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916343"
---
# <a name="DAYOFYEAR">ER DAYOFYEAR funkcija</a>

[!include [banner](../includes/banner.md)]

`DAYOFYEAR` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų nuo sausio 1 d. iki nurodytos datos skaičių.

## <a name="syntax"></a>Sintaksė

```
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumentai

`date`: *Data*

Datos reikšmė, nurodanti datą, naudotiną dienų skaičiui skaičiuoti.

## <a name="return-values"></a>Pateikiamos reikšmės

*Sveikasis skaičius*

Gaunama skaitinė reikšmė.

## <a name="example-1"></a>1 pavyzdys

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` pateikia **61**.

## <a name="example-2"></a>2 pavyzdys

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` pateikia **1**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)
