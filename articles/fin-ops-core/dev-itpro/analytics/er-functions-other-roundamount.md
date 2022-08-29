---
title: ROUNDAMOUNT ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama ROUNDAMOUNT elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0e4de43f865ca21822ab2c0c345026d2e9113ca2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286036"
---
# <a name="roundamount-er-function"></a>ROUNDAMOUNT ER funkcija

[!include [banner](../includes/banner.md)]

`ROUNDAMOUNT` funkcija grąžina *realiojo skaičiaus* reikšmę kaip nurodyto skaičiaus apvalinimo rezultatą iki artimiausio kito skaičiaus kartotinio pagal nurodytą apvalinimo taisyklę.

## <a name="syntax"></a>Sintaksė

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Argumentai

`number`: *Sveik.* arba *Realusis*

Skaitinė reikšmė, kurią reikia apvalinti.

`decimals`: *Sveik.* arba *Realusis*

Skaičius, kurio parametro `number` reikšmė turi būti suapvalinta iki kartotinio.

`round rule`: *Išvard. reikšmė*

Išvardijimo reikšmės **RoundOffType** išvardijimas, apibrėžiantis apvalinimo taisyklę. Šis išvardijimas siūlo šias reikšmes:

- Normalusis (paprastasis)
- Su trūkumu (RoundDown)
- Su pertekliumi (RoundUp)

## <a name="return-values"></a>Grįžties vertės

*Tikrasis*

Gauta skaitinė reikšmė yra parametro `decimals` nurodytos reikšmės kartotinis ir yra arčiausiai parametro `number` nurodytos reikšmės.

## <a name="usage-notes"></a>Naudojimo pastabos

Kai parametras `number` yra nulis, ši funkcija visada grąžina nulį.

Kai parametras `decimals` yra nulis, ši funkcija suapvalinama iki numatytosios apvalinimo reikšmės. Kai parametras `round rule`nustatytas kaip **RoundOffType.Ordinary**, numatytoji apvalinimo reikšmė yra **0,01**. Priešingu atveju numatytoji apvalinimo reikšmė yra **1,0**.

Kai parametras `round rule` nustatytas kaip **RoundOffType.Ordinary**, ši funkcija suapvalinama iki artimiausios apvalinimo sumos.

Kai parametras `round rule` nustatytas kaip **RoundOffType.RoundDown**, ši funkcija suapvalinama iki artimiausios apvalinimo sumos, lygios nuliui.

Kai parametras `round rule` nustatytas kaip **RoundOffType.RoundUp**, ši funkcija suapvalinama iki artimiausios apvalinimo sumos, kad nebūtų lygi nuliui.

Kai parametras `round rule`nustatytas kaip **RoundOffType.Ordinary**, ši funkcija veikia kaip X ++ funkcija [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel funkcija ir [Round](../dev-ref/xpp-math-run-time-functions.md#round).

## <a name="remarks"></a>Pastabos

Norėdami apvalinti skaitinę reikšmę iki nurodyto skaičiaus po kablelio, naudokite funkciją [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>Pavyzdys

Jei parametras **model.RoundOff** nustatytas kaip **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)`grąžina 7,35. 

Jei parametras **model.RoundOff** nustatytas kaip **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)`grąžina 7,35. 

Jei parametras **model.RoundOff** nustatytas kaip **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)`grąžina 8,4.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)

[Matematinės funkcijos](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
