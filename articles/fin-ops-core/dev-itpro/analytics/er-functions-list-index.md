---
title: ER INDEX funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) INDEX funkcija.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: e68f1690d6f852b0db560ef67a36fbde9e099715942a4b8a6e486d759af46682
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755784"
---
# <a name="index-er-function"></a>ER INDEX funkcija

[!include [banner](../includes/banner.md)]

`INDEX` funkcija pateikia tipo *Konteineris (įrašas)* reikšmę, kuri pasirenkama naudojant konkretų nurodyto sąrašo skaitinį indeksą. Jei indekse nėra nurodyto sąrašo įrašų intervalo, pateikiama išimtis.

## <a name="syntax"></a>Sintaksė

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumentai

`list`: *Įrašų sąrašas*

Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.

`index`: *Sveikasis skaičius*

Skaitinis indeksas, nurodantis norimo įrašo vietą nurodytame sąraše.

> [!NOTE]
> Kadangi šiai funkcijai naudojamas vienas numeravimas, nurodykite vertę **„1”**, kad būtų grąžinamas pirmas nurodyto sąrašo įrašas.

## <a name="return-values"></a>Grįžties vertės

*Konteineris (įrašas)*

Gauta įrašo reikšmė.

## <a name="example-1"></a>1 pavyzdys

Jei įvedate duomenų šaltinį **DS**, kurio tipas – *Apskaičiuotasis laukas*, ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, reiškinys `DS.Value` pateikia šio įrašų sąrašo antrojo įrašo teksto reikšmę **„B“**. Reiškinys `INDEX (SPLIT ("A|B|C", "|"), 2).Value` taip pat pateikia teksto reikšmę **„B“**.

## <a name="example-2"></a>2 pavyzdys

Jei įvedate tipo *Apskaičiuotasis laukas* duomenų šaltinį **DS** ir jame yra reiškinys `SPLIT ("A|B|C", "|")`, vykdomas reiškinys `INDEX (SPLIT ("A|B|C", "|"), 4).Value` pateikia išimtį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Sąrašo funkcijos](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
