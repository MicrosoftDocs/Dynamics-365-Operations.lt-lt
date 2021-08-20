---
title: ROUND ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ROUND elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 10/21/2020
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
ms.openlocfilehash: b0c28ba2faebf117aa008106f8a77f79af8f4de3122df858825aa15a6dae3616
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744415"
---
# <a name="round-er-function"></a>ROUND ER funkcija

[!include [banner](../includes/banner.md)]

`ROUND` funkcija grąžina nurodytą skaičių kaip *realiojo skaičiaus* reikšmę, suapvalintą iki nurodyto skaičiaus po kablelio.

## <a name="syntax"></a>Sintaksė

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Argumentai

`number`: *Realusis*

Skaitinė reikšmė, kurią reikia apvalinti.

`decimals`: *Sveikasis*

Skaitinė reikšmė, nurodanti skaičių po kablelio.

## <a name="return-values"></a>Grįžties vertės

*Tikrasis*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Jei argumento `decimals` reikšmė yra didesnė už 0 (nulį), nurodytas skaičius apvalinamas iki tiek skaitmenų po kablelio.

Jei argumento `decimals` reikšmė yra **0** (nulis), nurodytas skaičius apvalinamas iki artimiausio lyginio sveikojo skaičiaus.

Jei argumento `decimals` reikšmė yra mažesnė už 0 (nulį), nurodytas skaičius apvalinamas į kairę nuo skaičiaus po kablelio.

## <a name="example-1"></a>1 pavyzdys

`ROUND (1200.767, 2)` suapvalina iki dviejų skaičių po kablelio ir grąžina **1200,77**.

## <a name="example-2"></a>2 pavyzdys

`ROUND (1200.767, -3)` suapvalina iki artimiausio 1,000 kartotinio ir grąžina **1000**.

## <a name="example-3"></a>3 pavyzdys

`ROUND (1200.5, 0)` suapvalina iki artimiausio lyginio sveikojo skaičiaus ir pateikia **1200**, o `ROUND (1201.5, 0)` atlieka tą patį ir pateikia **1202**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Matematinės funkcijos](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]