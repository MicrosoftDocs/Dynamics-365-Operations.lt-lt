---
title: ER FIRSTORNULL funkcija
description: Šioje temoje paaiškinama, kaip naudojama modulio Elektroninės ataskaitos (ER) FIRSTORNULL funkcija
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 18c8f79d7d6306d9973c5a3f129b9cde38d05d58502a2c83ac89a2bd10aaaeab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749714"
---
# <a name="firstornull-er-function"></a>ER FIRSTORNULL funkcija

[!include [banner](../includes/banner.md)]

`FIRSTORNULL` funkcija pirmąjį nurodyto sąrašo įrašą pateikia kaip tipo *Konteineris (įrašas)* reikšmę (jei tas įrašas nėra tuščias). Jei įrašas tuščias, ši funkcija pateikia neapibrėžtą tipo *Konteineris (įrašas)* reikšmę.

## <a name="syntax"></a>Sintaksė

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

## <a name="return-values"></a>Pateikiamos reikšmės

*Konteineris (įrašas)*

Gauta įrašo reikšmė.

## <a name="example"></a>Pavyzdys

Reiškinys `FIRSTORNULL(SPLIT("",1)).Value` pateikia tuščią eilutę (**„“**).

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]