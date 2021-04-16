---
title: FA_SUM ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama FA_SUM elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744300"
---
# <a name="fa_sum-er-function"></a>FA_SUM ER funkcija

[!include [banner](../includes/banner.md)]

`FA_SUM` funkcija grąžina *konteinerio (įrašo)* reikšmę, kurią sudaro nurodyto ilgalaikio turto elemento, vertinimo modelio kodo ir datų laikotarpio ilgalaikio turto sumų duomenys.

## <a name="syntax"></a>Sintaksė

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumentai

`fixed asset code`: *Eilutė*

*Eilutės* vertė, reiškianti ilgalaikio turto elemento, kurio balansas skaičiuojamas, kodą.

`value model code`: *Eilutė*

*Eilutės* vertė, reiškianti reikšmės modelio, kurio balansas skaičiuojamas, kodą.

`start date`: *Data*

*Datos* reikšmė, reiškianti laikotarpio, kuriam apskaičiuojamos ilgalaikio turto sumos, pradžios datą.

`end date`: *Data*

*Datos* reikšmė, reiškianti laikotarpio, kuriam apskaičiuojamos ilgalaikio turto sumos, pabaigos datą.

## <a name="return-values"></a>Grįžties vertės

*Konteineris (įrašas)*

Gauta įrašo reikšmė.

## <a name="example"></a>Pavyzdys

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` grąžina ilgalaikio turto **COMP-000001**, paruošto **dabartiniam** reikšmės modeliui ir laikotarpiui nuo **Data1** iki **Data2**, duomenų konteinerį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]