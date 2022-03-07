---
title: IF ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama IF elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 3674618acae79170daf94413895d17d86a491996
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753173"
---
# <a name="if-er-function"></a>IF ER funkcija

[!include [banner](../includes/banner.md)]

`IF` funkcija grąžina pirmą nurodytą reikšmę, jei nurodyta sąlyga yra tenkinama. Kitu atveju ji pateikia antrą nurodytą reikšmę. Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.

## <a name="syntax"></a>Sintaksė

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumentai

`condition`: *Bulio logika*

Tinkama sąlyginė išraiška, kuri turi būti patikrinta.

`first value`: *Bet kuris iš palaikomų duomenų tipų*

Rezultatas, kuris grąžinamas, jei sąlyga tenkinama.

`second value`: *Bet kuris iš palaikomų duomenų tipų*

Rezultatas, kuris grąžinamas, jei sąlyga netenkinama.

## <a name="return-values"></a>Grįžties vertės

*Bet kuris iš palaikomų duomenų tipų*

Gauta bet kurio palaikomų duomenų tipo reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Argumentai `first value` ir `second value` turi būti nurodyti naudojant tą patį duomenų tipą. Jei sukonfigūruotų reikšmių duomenų tipai nesutampa, kūrimo metu pateikiama išimtis.

Jei pirmoji reikšmė ir antroji reikšmė yra duomenų tipo *Konteineris (įrašas)* arba *Įrašų sąrašas* reikšmės, rezultatai apima tik tuos laukus, kurie yra abiejose reikšmėse.

## <a name="example"></a>Pavyzdys

`IF (1=2, "condition is met", "condition is not met")` grąžina eilutę **„sąlyga netenkinama“**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Loginės funkcijos](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]