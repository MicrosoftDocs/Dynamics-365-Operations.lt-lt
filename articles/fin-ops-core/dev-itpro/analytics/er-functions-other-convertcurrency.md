---
title: CONVERTCURRENCY ER funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama funkcija CONVERTCURRENCY Elektroninės ataskaitos (ER).
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: e51086d977652e4be4c19390a824d4f4507b60d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898468"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY ER funkcija

[!include [banner](../includes/banner.md)]

`CONVERTCURRENCY` funkcija grąžina *realiojo skaičiaus* reikšmę, nurodančią gautą rezultatą konvertuojant nurodytą piniginę sumą iš nurodytos pirminės valiutos į nurodytą norimą valiutą naudojant nurodytos įmonės parametrus nurodytą dieną.

## <a name="syntax"></a>Sintaksė

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumentai

`amount`: *Sveikasis* arba *Realusis*

Skaitinė reikšmė, nurodanti piniginę sumą, kurią reikia konvertuoti.

`source currency`: *Eilutė*

Pirminės valiutos kodas.

`target currency`: *Eilutė*

Antrinės valiutos kodas.

`date`: *Data*

*Datos* reikšmė, kuri nurodo datą, naudojamą konvertavimo valiutos kurso datai nustatyti.

`company`: *Eilutė*

*Eilutės* reikšmė, kuri nurodo įmonės, teikiančios parametrus, naudojamus konvertuojant, kodą.

## <a name="return-values"></a>Grįžties vertės

*Tikrasis*

Gaunama skaitinė reikšmė.

## <a name="example"></a>Pavyzdys

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` grąžina vieno euro atitikmenį JAV doleriais dabartinio seanso dieną, atsižvelgiant į **DEMF** įmonės parametrus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]