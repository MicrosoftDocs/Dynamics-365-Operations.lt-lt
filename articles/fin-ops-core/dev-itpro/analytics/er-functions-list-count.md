---
title: ER COUNT funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama COUNT Electronic Reporting (ER) funkcija.
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
ms.openlocfilehash: b848bd179806b676435c219f0eb983516f3d0bf9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895401"
---
# <a name="count-er-function"></a>ER COUNT funkcija

[!include [banner](../includes/banner.md)]

`COUNT` funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią konkretaus sąrašo įrašų skaičių (jei sąrašas nėra tuščias). Jei sąrašas tuščias, ši funkcija pateikia **0** (nulį).

## <a name="syntax"></a>Sintaksė

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

## <a name="return-values"></a>Pateikiamos reikšmės

*Sveikasis skaičius*

Gaunama skaitinė reikšmė.

## <a name="example"></a>Pavyzdys

`COUNT (SPLIT("abcd" , 3))` pateikia **2**, nes šiame pavyzdyje naudojama `SPLIT` funkcija sukuria sąrašą, sudarytą iš dviejų įrašų.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]