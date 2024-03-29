---
title: ER SPLIT funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama SPLIT elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 04/01/2021
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
ms.openlocfilehash: e95ecaae46ee73899736b1d5729d7f9639fc6803
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274056"
---
# <a name="split-er-function"></a>ER SPLIT funkcija

[!include [banner](../includes/banner.md)]

`SPLIT` funkcija nurodytą įvesties eilutę išskaido į antrines eilutes ir rezultatą pateikia kaip naują tipo *Įrašų sąrašas* reikšmę.

## <a name="syntax-1"></a>1-oji sintaksė

```vb
SPLIT (input, length)
```

Ši sintaksė naudojama norint nurodytą įvesties eilutę skaidyti į antrines eilutes, iš kurių kiekvienos ilgis nurodomas atskirai.

## <a name="syntax-2"></a>2-oji sintaksė

```vb
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

## <a name="example-3"></a>3 pavyzdys

Galite naudoti funkciją [RODYKLĖ](er-functions-list-index.md), kad pasiektumėte atskirus nurodytos įvesties eilutės elementus. Jei įvedate **Apskaičiuotojo lauko** tipo duomenų šaltinį **Mano sąrašas** ir jam konfigūruojate išraišką `SPLIT("abc", 1)`, išraiška `INDEX(MyList,2).Value` grąžina teksto reikšmę **„b“**.

## <a name="example-4"></a>4 pavyzdys

Funkcija [IŠVARDYTI](er-functions-list-enumerate.md) taip pat jums gali padėti pasiekti atskirus nurodytos įvesties eilutės elementus. Jei pirmiausia įvedate **Apskaičiuotojo lauko** tipo duomenų šaltinį **Mano sąrašas** ir jam konfigūruojate išraišką `SPLIT("abc", 1)`, o tada įvedate **Apskaičiuotojo lauko** tipo duomenų šaltinį **Sunumeruotas sąrašas** ir jam konfigūruojate išraišką `ENUMERATE(MyList)`, išraiška `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` grąžina teksto reikšmę **„b”**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
