---
title: CONVERTCURRENCY ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CONVERTCURRENCY elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567645"
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