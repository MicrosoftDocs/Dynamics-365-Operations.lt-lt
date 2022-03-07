---
title: CONVERTCURRENCY ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CONVERTCURRENCY elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: dc71ccedcdfc8a3dc9d7e087d29467bd3bbe72c3c5588872dbeaf3aa1dd35d2b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738605"
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