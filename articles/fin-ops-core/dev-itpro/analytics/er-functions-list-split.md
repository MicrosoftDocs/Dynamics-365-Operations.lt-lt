---
title: ER SPLIT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) SPLIT funkcija.
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
ms.openlocfilehash: 31caf7c728a92d31428f47320c074fa9fc35bda6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916113"
---
# <a name="SPLIT">ER SPLIT funkcija</a>

[!include [banner](../includes/banner.md)]

`SPLIT` funkcija nurodytą įvesties eilutę išskaido į antrines eilutes ir rezultatą pateikia kaip naują tipo *Įrašų sąrašas* reikšmę.

## <a name="syntax-1"></a>1-oji sintaksė

```
SPLIT (input, length)
```

Ši sintaksė naudojama norint nurodytą įvesties eilutę skaidyti į antrines eilutes, iš kurių kiekvienos ilgis nurodomas atskirai.

## <a name="syntax-2"></a>2-oji sintaksė

```
SPLIT (input, delimiter)
```

Ši sintaksė naudojama norint nurodytą įvesties eilutę skaidyti į antrines eilutes (pagal nurodytą skyriklį).

## <a name="arguments"></a>Argumentai

`input`: *Eilutė*

Skaidytinas tekstas.

`length`: *Sveikasis*

Maksimalus vienos antrinės eilutės ilgis.

`delimiter`: *Eilutė*

Skyriklis, naudojamas antrinėms eilutėms atskirti.

## <a name="return-values"></a>Pateikiamos reikšmės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Pateikto sąrašo įrašų struktūrą sudaro tipo *Eilutė* laukas **Reikšmė**. Šiame kiekvieno pateikto sąrašo įrašo lauke pateikiamos sugeneruotos antrinės eilutės.

Jei `delimiter` argumentas tuščias, pateiktą naują sąrašą sudaro vienas įrašas, kuriame yra tipo *Eilutė* laukas **Reikšmė**. Šiame lauke yra įvesties tekstas.

Jei `input` argumentas tuščias, pateikiamas naujas tuščias sąrašas. Jei `input` arba `delimiter` argumentas nenurodytas (neapibrėžtas), pateikiama programos išimtis.

## <a name="example-1"></a>1 pavyzdys

`SPLIT ("abcd", 3)` pateikia naują sąrašą, sudarytą iš dviejų įrašų, kuriuose yra tipo *Eilutė* laukas **Reikšmė**. Pirmame įraše esančiame lauke **Reikšmė** yra tekstas **„abc“**, o antrame įraše esančiame lauke **Reikšmė** yra tekstas **„d“**.

## <a name="example-2"></a>2 pavyzdys

`SPLIT ("XAb aBy", "aB")` pateikia naują sąrašą, sudarytą iš trijų įrašų, kuriuose yra tipo *Eilutė* laukas **Reikšmė**. Pirmo įrašo lauke **Reikšmė** yra tekstas **„X“**, antro įrašo lauke **Reikšmė** yra tekstas **„&nbsp;“**, o trečio įrašo lauke **Reikšmė** yra tekstas **„y“**. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)