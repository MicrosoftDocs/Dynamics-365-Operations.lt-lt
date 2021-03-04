---
title: FA_BALANCE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama FA_BALANCE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 5570e1295ff6da0eadd7e18143a2206032597ae5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684840"
---
# <a name="fa_balance-er-function"></a>FA_BALANCE ER funkcija

[!include [banner](../includes/banner.md)]

`FA_BALANCE` funkcija grąžina *konteinerio (įrašo)* reikšmę, kurią sudaro nurodyto ilgalaikio turto elemento, vertinimo modelio kodo, ataskaitinių metų ir ataskaitos datos ilgalaikio turto balanso duomenys.

## <a name="syntax"></a>Sintaksė

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumentai

`fixed asset code`: *Eilutė*

*Eilutės* vertė, reiškianti ilgalaikio turto elemento, kurio balansas skaičiuojamas, kodą.

`value model code`: *Eilutė*

*Eilutės* vertė, reiškianti reikšmės modelio, kurio balansas skaičiuojamas, kodą.

`reporting year`: *Išvardijimo vertė*

Programos išvardijimo **Assetyear**, apibrėžiančio balanso skaičiavimo laikotarpį, išvardijimo reikšmė.

`reporting date`: *Data*

*Datos* reikšmė, nurodanti balanso skaičiavimo datą.

## <a name="return-values"></a>Grįžties vertės

*Konteineris (įrašas)*

Gauta įrašo reikšmė.

## <a name="example"></a>Pavyzdys

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` grąžina ilgalaikio turto **COMP-000001**, dabartinio programos seanso datą paruošto reikšmės modeliui **Dabartinis**, balansų duomenų konteinerį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]