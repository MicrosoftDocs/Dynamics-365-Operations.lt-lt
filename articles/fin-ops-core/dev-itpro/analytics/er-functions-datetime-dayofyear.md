---
title: ER DAYOFYEAR funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DAYOFYEAR funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 569e988db91ff992fb7db6e7fd6e8c6aa6a1a3e8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746920"
---
# <a name="dayofyear-er-function"></a>ER DAYOFYEAR funkcija

[!include [banner](../includes/banner.md)]

`DAYOFYEAR` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų nuo sausio 1 d. iki nurodytos datos skaičių.

## <a name="syntax"></a>Sintaksė

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]