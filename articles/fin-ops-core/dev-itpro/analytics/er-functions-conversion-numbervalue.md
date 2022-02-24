---
title: ER NUMBERVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) NUMBERVALUE funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3eec6dc5a472f366c9029456fe05cf1e431e1c5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685984"
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
