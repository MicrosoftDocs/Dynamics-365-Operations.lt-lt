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
ms.openlocfilehash: c7f78b687865e63e658c1c1c4f148b50595bf063
ms.sourcegitcommit: 54bdcf8e9b6d1b1aae2a244f7a82754879d12053
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/31/2020
ms.locfileid: "3740668"
---
# <a name=""></a><a name="LISTJOIN">LISTJOIN ER funkcija</a>

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

![ER modelio susiejimo dizaino įrankio puslapis](./media/er-functions-list-listjoin-image2.gif)

Šio sąrašo struktūrą sudaro vienas tipo `Real` laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.

![ER modelio susiejimo dizaino įrankio puslapis](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)

[Įvykdyto ER formato duomenų šaltinių derinimas duomenų srautams ir transformacijai analizuoti](er-debug-data-sources.md)
