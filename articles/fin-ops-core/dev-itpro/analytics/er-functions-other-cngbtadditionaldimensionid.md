---
title: CN_GBT_ADDITIONALDIMENSIONID ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai CN_GBT_ADDITIONALDIMENSIONID naudojama elektroninės ataskaitos (ER) funkcija.
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
ms.openlocfilehash: 0ed2593f865a4764b1c6172722d701a0a10ba5f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281759"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER funkcija

[!include [banner](../includes/banner.md)]

`CN_GBT_ADDITIONALDIMENSIONID` funkcija grąžina *Eilutės* reikšmę, nurodančią vieną finansinės dimensijos ID, paimtą iš nurodytos eilutės. Nurodytoje eilutėje visos dimensijos pateikiamos kaip kableliais atskirtų ID sąrašas.

## <a name="syntax"></a>Sintaksė

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

*Eilutės* reikšmė, kuri pateikia visus matmenis kaip kableliais atskirtų ID sąrašą.

`number`: Sveikasis

*Sveikojo skaičiaus* reikšmė nurodo pageidaujamos dimensijos sekos kodą nurodytoje eilutėje.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="example"></a>Pavyzdys

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` grąžina **„CC“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
