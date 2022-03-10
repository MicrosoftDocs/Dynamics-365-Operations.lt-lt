---
title: ER NUMBERVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) NUMBERVALUE funkcija.
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
ms.openlocfilehash: bcb76310a53c86b68f18085e203d11f405b16946a25fe1be67e649f83335d1f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733802"
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