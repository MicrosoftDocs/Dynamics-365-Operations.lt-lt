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
ms.openlocfilehash: 198210f15e75de761dbb03e5087ba7c77a95721a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041750"
---
# <a name="IF">IF ER funkcija</a>

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
