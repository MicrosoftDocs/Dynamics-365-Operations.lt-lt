---
title: ER DATEVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATEVALUE funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 43e65055b0803ed330a19568f9565c3fae488ab2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682418"
---
# <a name="datevalue-er-function"></a>ER DATEVALUE funkcija

[!include [banner](../includes/banner.md)]

`DATEVALUE` funkcija pateikia tipo *Data* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes), konvertuojama į datos reikšmę. Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>1-oji sintaksė

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>2-oji sintaksė

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumentai

`text`: *Eilutė*

Tekstas, nurodantis formatuotiną reikšmę.

`format`: *Eilutė*

Nurodyto teksto formatas.

`culture`: *Eilutė*

Kultūra, naudojama nurodytam tekstui formatuoti.

## <a name="return-values"></a>Pateikiamos reikšmės

*Data*

Gauta datos reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas. Pavyzdžiui, jei `DATEVALUE` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą. Numatytoji `culture` reikšmė yra **EN-US**.

## <a name="example-1"></a>1 pavyzdys

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` pagal nurodytą pasirinktinį formatą ir numatytąją programos **EN-US** kultūrą pateikia datos reikšmę **December 21, 2016**.

## <a name="example-2"></a>2 pavyzdys

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` pagal nurodytą pasirinktinį formatą ir kultūrą pateikia datos reikšmę **January 21, 2016**.

Tačiau `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` pateikia išimtį, kad informuotų vartotoją, jog nurodyta eilutė nėra atpažįstama kaip tinkama nurodytos kultūros data.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]