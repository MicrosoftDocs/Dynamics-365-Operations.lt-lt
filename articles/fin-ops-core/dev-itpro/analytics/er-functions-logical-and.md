---
title: AND ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama AND elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041820"
---
# <a name="AND">AND ER funkcija</a>

[!include [banner](../includes/banner.md)]

`AND` funkcija pateikia *Bulio logikos* reikšmę **TEISINGA**, jei visos nurodytos sąlygos yra teisingos. Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.

## <a name="syntax"></a>Sintaksė

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumentai

`condition 1`: *Bulio logika*

Tinkama sąlyginė išraiška, kuri turi būti patikrinta. Šis argumentas yra būtinas.

`condition N`: *Bulio logika*

Tinkama sąlyginė išraiška, kuri turi būti patikrinta. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Grįžties vertės

*Būlio logika*

Gaunama *Bulio logikos* reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Loginių funkcijų argumentuose galite naudoti duomenų šaltinio nuorodas, skaitines ir tekstines reikšmes, Bulio logikos reikšmes, palyginimo operatorius ir kitas elektroninių ataskaitų (ER) funkcijas. Tačiau visi argumentai turi būti vertinami pagal *Bulio logikos* reikšmę **TEISINGA** arba **KLAIDINGA**.

## <a name="example"></a>Pavyzdys

`AND (1=1, "a"="a")` grąžina **TEISINGA**.

`AND (1=2, "a"="a")` grąžina **KLAIDINGA**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)
