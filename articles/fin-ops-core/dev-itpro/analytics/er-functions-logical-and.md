---
title: AND ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama AND elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 4d327f0f961a11fecdbc055ffbb1f3d8bc15bcfdd732e2565d0a5e9e2c0a31ca
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756434"
---
# <a name="and-er-function"></a>AND ER funkcija

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]