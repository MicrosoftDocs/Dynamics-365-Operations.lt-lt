---
title: ER DATETIMEFORMAT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETIMEFORMAT funkcija.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 8044f81ee59af4a11bfab38525afdac5a46acd2c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891262"
---
# <a name="datetimeformat-er-function"></a>ER DATETIMEFORMAT funkcija

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos / laiko reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) ir [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>1-oji sintaksė

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>2-oji sintaksė

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Argumentai

`datetime`: *DateTime*

Datos / laiko reikšmė, nurodanti formatuotinus datą ir laiką.

`format`: *Eilutė*

Išvesties eilutės formatas.

> [!NOTE]
> Formato eilutė skiria didžiąsias ir mažąsias raides, kai naudojate tiek standartinį formatą, tiek pasirinktinį formatą. Pavyzdžiui, [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) „d” formato specifikatorius pateikia datą naudodamas trumpąjį datos formatas, o standartinis „D” formato specifikatorius pateikia datą naudodamas ilgąjį datos formatą. Taip pat, [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings) „M” formato specifikatorius pateikia mėnesį nuo 1 iki 12, o pasirinktinis „m” formato specifikatorius pateikia minučių skaičių nuo 0 iki 59.

`culture`: *Eilutė*

Formatuojant naudotina kultūra.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gauta eilutės reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas. Pavyzdžiui, jei `DATETIMEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą. Numatytoji `culture` reikšmė yra **EN-US**.

Kai `DATETIMEFORMAT` funkcija konvertuoja nurodytą datos / laiko reikšmę, ji atsižvelgia į programos vartotojo, vykdančio ER formatą, kurio kontekste funkcija iškviesta, laiko juostos parametrą.

## <a name="example-1"></a>1 pavyzdys

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pateikia dabartinę programos serverio datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **„24-12-2015“** pagal nurodytą pasirinktinį formatą.

## <a name="example-2"></a>2 pavyzdys

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **24.12.2015**.

## <a name="example-3"></a>3 pavyzdys

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` pateikia eilutės reikšmę **„2019-11-12T08:00:00.0000000-08:00”** tada, kai funkcija iškviečiama vykdant procesą, kurį inicijavo programos vartotojas, pasirinkęs **(GMT-08:00) Ramiojo vandenyno laikas (JAV ir Kanada)** laiko juostos reikšmę **Kalba ir šalies/regiono nuostatos** skyriuje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]