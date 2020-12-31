---
title: CH_BANK_MOD_10 ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CH_BANK_MOD_10 elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: bca82cd596ba1e3ec42b3dba91ee6c4871ff8601
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686863"
---
# <a name="ch_bank_mod_10-er-function"></a>CH_BANK_MOD_10 ER funkcija

[!include [banner](../includes/banner.md)]

`CH_BANK_MOD_10` funkcija grąžina *Eilutės* reikšmę, kuri nurodo kreditoriaus nuorodą kaip MOD10 išraišką pagal nurodyto sąskaitos faktūros numerio skaitmenis.

## <a name="syntax"></a>Sintaksė

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumentai

`invoice number digits`: *Eilutė*

Tekstinė reikšmė, nurodanti sąskaitos faktūros numerio skaitmenis.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`CH_BANK_MOD_10 ("VEND-200002")` grąžina **3**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)
