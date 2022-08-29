---
title: ER EMPTYLIST funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama EMPTYLIST elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 5fd14456a615d5dc6fb565f4bed523db5432c871
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268123"
---
# <a name="emptylist-er-function"></a>ER EMPTYLIST funkcija

[!include [banner](../includes/banner.md)]

`EMPTYLIST` funkcija pateikia tuščią tipo *Įrašų sąrašas* reikšmę, kaip sąrašo struktūros šaltinį naudodama nurodytą sąrašą.

## <a name="syntax"></a>Sintaksė

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="example"></a>Pavyzdys

`EMPTYLIST (SPLIT ("abc", 1))` pateikia naują tuščią sąrašą, kuris yra tokios pačios struktūros, kaip ir sąrašas, kurį pateikia naudojama `SPLIT` funkcija.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
