---
title: IF ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama IF elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b29302ffe534f2439519e57c6a6b8c94c1df8d62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917148"
---
# <a name="IF">IF ER funkcija</a>

[!include [banner](../includes/banner.md)]

`IF` funkcija grąžina pirmą nurodytą reikšmę, jei nurodyta sąlyga yra tenkinama. Kitu atveju ji pateikia antrą nurodytą reikšmę. Grąžinama reikšmė gali būti bet kurių palaikomo duomenų tipų reikšmė.

## <a name="syntax"></a>Sintaksė

```
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
