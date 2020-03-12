---
title: ER DATETIMEFORMAT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETIMEFORMAT funkcija.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 9e550b0c7634c7aac3f8c597a1c1eac3f8125e3b
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070718"
---
# <a name="DATETIMEFORMAT">ER DATETIMEFORMAT funkcija</a>

[!include [banner](../includes/banner.md)]

`DATETIMEFORMAT` funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos / laiko reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

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

`culture`: *Eilutė*

Formatuojant naudotina kultūra.

## <a name="return-values"></a>Pateikiamos reikšmės

*Eilutė*

Gauta eilutės reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas. Pavyzdžiui, jei `DATETIMEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą. Numatytoji `culture` reikšmė yra **EN-US**.

Kai `DATETIMEFORMAT` funkcija konvertuoja nurodytą datos / laiko reikšmę, ji atsižvelgia į programos vartotojo, vykdančio ER formatą, kurio kontekste funkcija iškviesta, laiko juostos parametrą.

## <a name="example-1"></a>1 pavyzdys

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pateikia dabartinę programos serverio datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **„24-12-2015“** pagal nurodytą pasirinktinį formatą.

## <a name="example-2"></a>2 pavyzdys

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **24.12.2015**.

## <a name="example-3"></a>3 pavyzdys

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` pateikia eilutės reikšmę **2019-11-12T08:00:00.0000000-08:00**, kai ji iškviečiama vykdant procesą, kurį inicijavo programos vartotojas, skyriuje **Kalba ir šalies / regiono nuostatos** pasirinkęs laiko juostos reikšmę **(GMT-08:00) Ramiojo vandenyno laikas (JAV ir Kanada)**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)
