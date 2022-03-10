---
title: Funkcija WEEKNUM ER
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama WEEKNUM Elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 37e62b32896e2030b3322a89ac4acdd6c18d5e3c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982182"
---
# <a name="weeknum-er-function"></a>Funkcija WEEKNUM ER

[!include [banner](../includes/banner.md)]

Funkcija `WEEKNUM` grąžina vertę *[Integer,](er-formula-supported-data-types-primitive.md#integer)* kuri nurodo metų savaitę, į kurią įtraukta nurodyta *[datos](er-formula-supported-data-types-primitive.md#date)* vertė. Skaičiavimas paremtas nuo kultūros priklausančiomis taisyklėmis, kurios nurodo kalendorinę savaitę ir pirmą savaitės dieną.

## <a name="syntax"></a>Sintaksė

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumentai</a>

`date`: *Data*

Datos vertė, nurodanti datą, kurią reikia naudoti skaičiuojant metų savaitę.

`culture`: *[eilutė](er-formula-supported-data-types-primitive.md#string)*

Skaičiavime naudojami kultūra. Galite naudoti kultūros kodus, palaikomus pagal .NET [standartus](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Grįžimo vertės

*Sveikasis skaičius*

Gaunama skaitinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Metų savaitė skaičiuojama pagal [ISO 8601 standartą, jei šį standartą priėmė šalis arba regionas, kuriame lokalė pateikiama](https://www.iso.org/iso-8601-date-and-time-format.html) vykdyklėje. Kitu atveju skaičiavimas remiasi šaliai/regionui konkrečiais šalies standartais.

Jei nepalaikomas [kultūros](#arguments) kodas pateikiamas kaip funkcijos `WEEKNUM` argumentas apdorojimo metu, pateikiama išimtis. Jei tuščia eilutė pateikiama kaip kultūros kodas, savaitės numeriui apskaičiuoti naudojamas anglų šalies neutrali kalendorius.

## <a name="examples"></a>Pavyzdžiai

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` grąžina **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` grąžina **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` grąžina **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` grąžina **21**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
