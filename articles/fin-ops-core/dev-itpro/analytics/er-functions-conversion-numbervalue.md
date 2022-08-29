---
title: ER NUMBERVALUE funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama NUMBERVALUE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 2e39cf59cabd44583e78ff2c35a7ae4d6edbd7ee
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282598"
---
# <a name="numbervalue-er-function"></a>ER NUMBERVALUE funkcija

[!include [banner](../includes/banner.md)]

`NUMBERVALUE` funkcija pateikia tipo *Realusis skaičius* reikšmę, konvertuotą iš nurodytos tipo *Eilutė* reikšmės. Konvertuojant atsižvelgiama į nurodytus dešimtainius ir skaitmenų grupavimo skyriklius.

## <a name="syntax"></a>Sintaksė

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Teksto reikšmė, kurią reikia konvertuoti į tipo *Realusis* skaičių.

`decimal separator`: Eilutė

Dešimtainis skyriklis. Jis naudojamas dešimtainio skaičiaus sveikajai ir trupmeninei dalims atskirti.

`digit grouping separator`: *Eilutė*

Skaitmenų grupavimo skyriklis. Jis naudojamas kaip tūkstančių skyriklis.

## <a name="return-values"></a>Pateikiamos reikšmės

*Tikrasis*

Gaunama skaitinė reikšmė.

## <a name="example"></a>Pavyzdys

`NUMBERVALUE( "1 234,56", ",", " ")` pateikia **1234,56**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tipų konvertavimo funkcijos](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
