---
title: ER DATEFORMAT funkcija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudojama DATEFORMAT elektroninių ataskaitų (ER) funkcija.
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: 5a21e65df705e33c0bd502ea2c17e18b5385c0d4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287405"
---
# <a name="dateformat-er-function"></a>ER DATEFORMAT funkcija

[!include [banner](../includes/banner.md)]

Funkcija `DATEFORMAT` grąžina *[Eilutės](er-formula-supported-data-types-primitive.md#string)* reikšmę, kurioje pateikiama nurodyta datos reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) ir [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>1-oji sintaksė

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>2-oji sintaksė

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumentai

`date`: *[Data](er-formula-supported-data-types-primitive.md#date)*

Datos reikšmė, nurodanti formatuotiną datą.

`format`: *Eilutė*

Išvesties eilutės formatas. Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) ir [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> Formato eilutė skiria didžiąsias ir mažąsias raides, kai naudojate tiek standartinį formatą, tiek pasirinktinį formatą. Pavyzdžiui, [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) „d” formato specifikatorius pateikia datą naudodamas trumpąjį datos formatas, o standartinis „D” formato specifikatorius pateikia datą naudodamas ilgąjį datos formatą. Taip pat, [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings) „M” formato specifikatorius pateikia mėnesį nuo 1 iki 12, o pasirinktinis „m” formato specifikatorius pateikia minučių skaičių nuo 0 iki 59.

`culture`: *Eilutė*

Formatuojant naudotina kultūra. Daugiau informacijos apie palaikomas kultūras rasite [kultūra](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gauta eilutės reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas. Pavyzdžiui, jei `DATEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą. Numatytoji `culture` reikšmė yra **EN-US**.

## <a name="example-1"></a>1 pavyzdys

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` dabartinę programos serverio datą – 2015 m. gruodžio 24 d. – pagal nurodytą pasirinktinį formatą pateikia kaip eilutę **„24-12-2015“**.

## <a name="example-2"></a>2 pavyzdys

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datą – 2015 m. gruodžio 24 d. – kaip eilutę **24-12-2015**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
