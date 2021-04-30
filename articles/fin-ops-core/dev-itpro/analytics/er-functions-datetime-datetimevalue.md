---
title: ER DATETIMEVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETIMEVALUE funkcija.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891286"
---
# <a name="datetimevalue-er-function"></a>ER DATETIMEVALUE funkcija

[!include [banner](../includes/banner.md)]

`DATETIMEVALUE` funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes), konvertuojama į datos / laiko reikšmę. Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) ir [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>1-oji sintaksė

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>2-oji sintaksė

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tekstas, nurodantis formatuotiną reikšmę.

`format`: *Eilutė*

Nurodyto teksto formatas.

`culture`: *Eilutė*

Kultūra, naudojama nurodytam tekstui formatuoti.

## <a name="return-values"></a>Pateikiamos reikšmės

*Data ir laikas*

Gauta datos / laiko reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas. Pavyzdžiui, jei `DATETIMEVALUE` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą. Numatytoji `culture` reikšmė yra **EN-US**.

## <a name="example-1"></a>1 pavyzdys

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` pagal nurodytą pasirinktinį formatą ir numatytąją programos **EN-US** kultūrą pateikia **2:55:00 AM on December 21, 2016**.

## <a name="example-2"></a>2 pavyzdys

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` pagal nurodytą pasirinktinį formatą ir kultūrą pateikia **2:55:00 AM on December 21, 2016**.

Tačiau `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` pateikia išimtį, kad informuotų vartotoją, jog nurodyta eilutė nėra atpažįstama kaip tinkama nurodytos kultūros datos / laiko reikšmė.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]