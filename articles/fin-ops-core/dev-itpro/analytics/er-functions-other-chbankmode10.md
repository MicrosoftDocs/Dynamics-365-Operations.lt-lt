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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c18a7f96096fbc6bbc7b6d15135c11bd70960d26
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744475"
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
