---
title: Kategorijos Data ir laikas ER funkcijų sąrašas
description: Šiame straipsnyje pateikta informacija apie datos ir laiko funkcijas, kurias palaiko elektroninės ataskaitos (ER).
author: kfend
ms.date: 09/09/2021
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
ms.openlocfilehash: d77f41e10d927a9aae06b9ba0fc58ca237c071cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291331"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Kategorijos Data ir laikas ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant modulio Elektroninės ataskaitos (ER) datos ir laiko funkcijas, galima išgauti informaciją iš datos bei laiko reikšmių ir su jomis atlikti operacijas. Šiame straipsnyje pateikiama šių funkcijų suvestinė.

## <a name="list-of-supported-functions"></a>Palaikomų funkcijų sąrašas

| Funkcija | Aprašymas |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Ši funkcija pateikia *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | Ši funkcija pateikia *DateTime* eikšmę, kuri iš nurodytos datos reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko kitoje laiko juostoje. |
| [DateFormat](er-functions-datetime-dateformat.md) | Ši funkcija pateikia tipo *[Eilutė](er-formula-supported-data-types-primitive.md#string)* reikšmę, kurioje pateikiama nurodyta datos reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos / laiko reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos / laiko reikšmę. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos datos reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko (Grinvičo laiko \[GMT\]) formatu. |
| [DateValue](er-functions-datetime-datevalue.md) | Ši funkcija grąžina *[datos](er-formula-supported-data-types-primitive.md#date)* vertę, kuri konvertuojama iš nurodytos teksto vertės nurodytu formatu ir pasirinktinai nurodytu formatu į datos vertę. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Ši funkcija grąžina vertę *[Integer](er-formula-supported-data-types-primitive.md#integer)*, kuri nurodo dienų skaičių nuo sausio 1 d. iki nurodytos datos. |
| [Dienos](er-functions-datetime-days.md) | Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų tarp pirmos nurodytos datos ir antros nurodytos datos skaičių. |
| [Now](er-functions-datetime-now.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo dabartinius programos serverio datą ir laiką. |
| [NullDate](er-functions-datetime-nulldate.md) | Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo **neapibrėžtą** datą (1900 m. sausio 1 d.). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo **neapibrėžtą** datos / laiko reikšmę (1900 m. sausio 1 d.) universaliojo laiko formatu. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo dabartinius programos seanso datą ir laiką. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos seanso datą. |
| [Šiandien](er-functions-datetime-today.md) | Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos serverio datą. |
| [WeekNum](er-functions-datetime-weeknum.md) | Ši funkcija grąžina *vertę Integer*, kuri nurodo metų savaitę. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
