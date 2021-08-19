---
title: EMPTYRECORD ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama EMPTYRECORD elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 5aea5533f5d0530cdc9ccae0b0b8355245599bc77e37fde87a13e8e5a1443695
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725191"
---
# <a name="emptyrecord-er-function"></a>EMPTYRECORD ER funkcija

[!include [banner](../includes/banner.md)]

`EMPTYRECORD` funkcija grąžina nulinę *konteinerio (įrašo)* reikšmę, kurios struktūra yra tokia pati kaip nurodyto įrašų sąrašo arba įrašo.

## <a name="syntax"></a>Sintaksė

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas* arba *Konteineris (įrašas)*

Tinkamas *Įrašų sąrašo* arba *Konteinerio (įrašo)* tipo duomenų šaltinio maršrutas.

## <a name="return-values"></a>Grįžties vertės

*Konteineris (įrašas)*

Gauta įrašo reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

> [!NOTE] 
> Neapibrėžtas įrašas yra toks, kurio visų laukų reikšmės yra tuščios. Tuščia skaičių reikšmė yra **0** (nulis), eilučių – tuščia eilutė ir t. t.

## <a name="example"></a>Pavyzdys

`EMPTYRECORD (SPLIT ("abc", 1))` grąžina naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį grąžina `SPLIT` funkcija. Daugiau informacijos žr. [SPLIT](er-functions-list-split.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Įrašo funkcijos](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]