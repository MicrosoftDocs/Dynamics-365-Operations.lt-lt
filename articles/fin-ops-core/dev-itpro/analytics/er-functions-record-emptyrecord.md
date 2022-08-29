---
title: EMPTYRECORD ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama EMPTYRECORD elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5046a1cb43f12863ddbdf241e8ba72071d1016ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280162"
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
