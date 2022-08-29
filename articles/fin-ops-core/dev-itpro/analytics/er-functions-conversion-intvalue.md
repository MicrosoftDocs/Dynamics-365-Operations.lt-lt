---
title: ER INTVALUE funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama INTVALUE elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282628"
---
# <a name="intvalue-er-function"></a>ER INTVALUE funkcija

[!include [banner](../includes/banner.md)]

`INTVALUE` funkcija pateikia *Int* reikšmę, kuri nurodo nurodytą eilutę.

## <a name="syntax-1"></a>1-oji sintaksė

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>2-oji sintaksė

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Teksto reikšmė, kurią reikia konvertuoti į *Int* skaičių.

`number`: *Realusis* arba *Sveikasis*

Skatinė tipo *Realusis skaičius* arba *Sveikasis skaičius* reikšmė, kurią reikia konvertuoti į *Int* skaičių.

## <a name="return-values"></a>Pateikiamos reikšmės

*Int*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Visi skaičiai po kablelio pašalinami.

## <a name="example-1"></a>1 pavyzdys

`INTVALUE ("100.77")` pateikia *Int* reikšmę **100**.

## <a name="example-2"></a>2 pavyzdys

`INTVALUE (-100.77)` pateikia *Int* reikšmę **–100**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tipų konvertavimo funkcijos](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
