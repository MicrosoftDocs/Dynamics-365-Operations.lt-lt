---
title: LISTJOIN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama LISTJOIN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 035bf720a892e987ff9fc073ab8ed6f6cc6ea18e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745110"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER funkcija

[!include [banner](../includes/banner.md)]

`LISTJOIN` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, nurodančią naują jungtinį įrašų sąrašą, sukurtą iš nurodytų argumentų.

## <a name="syntax"></a>Sintaksė

```vb
LIST (list 1 [, list 2, …, list N])
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

![ER modelio susiejimo dizaino įrankio puslapis](./media/er-functions-list-listjoin-image1.gif)

Šiuo atveju reiškinys `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` pateikia naują sąrašą, kuriame yra du įrašai.

![ER modelio susiejimo dizaino įrankio puslapis su dviem įrašais](./media/er-functions-list-listjoin-image2.gif)

Šio sąrašo struktūrą sudaro vienas tipo `Real` laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.

![ER modelio susiejimo dizaino įrankio puslapio sumos laukas](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)

[Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti](er-debug-data-sources.md)
