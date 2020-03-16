---
title: ER DATEFORMAT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATEFORMAT funkcija.
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
ms.openlocfilehash: 759ccd3cf16c6c109faf44cea350745e3b2bff0b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042440"
---
# <a name="DATEFORMAT">ER DATEFORMAT funkcija</a>

[!include [banner](../includes/banner.md)]

`DATEFORMAT` funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>1-oji sintaksė

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>2-oji sintaksė

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumentai

`date`: *Data*

Datos reikšmė, nurodanti formatuotiną datą.

`format`: *Eilutė*

Išvesties eilutės formatas.

`culture`: *Eilutė*

Formatuojant naudotina kultūra.

## <a name="return-values"></a>Pateikiamos reikšmės

*Eilutė*

Gauta eilutės reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas. Pavyzdžiui, jei `DATEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą. Numatytoji `culture` reikšmė yra **EN-US**.

## <a name="example-1"></a>1 pavyzdys

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` dabartinę programos serverio datą – 2015 m. gruodžio 24 d. – pagal nurodytą pasirinktinį formatą pateikia kaip eilutę **„24-12-2015“**.

## <a name="example-2"></a>2 pavyzdys

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datą – 2015 m. gruodžio 24 d. – kaip eilutę **24-12-2015**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)
