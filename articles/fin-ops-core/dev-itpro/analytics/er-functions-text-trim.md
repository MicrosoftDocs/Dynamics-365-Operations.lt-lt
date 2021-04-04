---
title: TRIM ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TRIM elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: b671ef72a3558c17fb16db939770394b225656da
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560042"
---
# <a name="trim-er-function"></a>TRIM ER funkcija

[!include [banner](../includes/banner.md)]

`TRIM` funkcija grąžina nurodytą teksto eilutę kaip *Eilutės* reikšmę, sutrumpinus priekinius ir galinius tarpus bei pašalinus perteklinius tarpus tarp žodžių.

## <a name="syntax"></a>Sintaksė

```vb
TRIM (text )
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` grąžina **„Teksto pavyzdys“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]