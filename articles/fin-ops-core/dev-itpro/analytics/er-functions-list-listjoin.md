---
title: LISTJOIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama LISTJOIN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9346afc88adb89c08098f39a5fd1c2cb82f664af2244b8cafbbe8a4d2f516c6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755807"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER funkcija

[!include [banner](../includes/banner.md)]

`LISTJOIN` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, nurodančią naują jungtinį įrašų sąrašą, sukurtą iš nurodytų argumentų.

## <a name="syntax"></a>Sintaksė

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Argumentai

`list 1`: *Įrašų sąrašas*

Nuoroda į duomenų tipo *Įrašų sąrašas* duomenų šaltinį. Šis argumentas yra privalomas.

`list N`: *Įrašų sąrašas*

Nuoroda į duomenų tipo *Įrašų sąrašas* duomenų šaltinį. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Grįžties vertės

*Įrašų sąrašas*

Gautas įrašų sąrašas.

## <a name="usage-notes"></a>Naudojimo pastabos

Sukurto sąrašo struktūroje yra tik tie laukai, kurie pateikiami kiekvieno argumentuose nurodyto įrašų sąrašo struktūroje.

## <a name="example"></a>Pavyzdys

Įvedate tipo `Container` duomenų šaltinį **1-asis įrašas**. Šiame duomenų šaltinyje yra tolesni įdėtieji tipo `Calculated field` laukai.

- **Kodas**. Šiame lauke yra reiškinys, pateikiantis tipo `String` reikšmę.
- **Suma**. Šiame lauke yra reiškinys, pateikiantis tipo `Real` reikšmę.

Tada įvedate tipo `Container` duomenų šaltinį **2-asis įrašas**. Šiame duomenų šaltinyje yra tolesni įdėtieji tipo `Calculated field` laukai.

- **Suma**. Šiame lauke yra reiškinys, pateikiantis tipo `Real` reikšmę.
- **IsValid**. Šiame lauke yra reiškinys, pateikiantis tipo `Boolean` reikšmę.

![ER modelio susiejimo dizaino įrankio puslapis.](./media/er-functions-list-listjoin-image1.gif)

Šiuo atveju reiškinys `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` pateikia naują sąrašą, kuriame yra du įrašai.

![ER modelio susiejimo dizaino įrankio puslapis su dviem įrašais.](./media/er-functions-list-listjoin-image2.gif)

Šio sąrašo struktūrą sudaro vienas tipo `Real` laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.

![ER modelio susiejimo dizaino įrankio puslapio sumos laukas.](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)

[Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
