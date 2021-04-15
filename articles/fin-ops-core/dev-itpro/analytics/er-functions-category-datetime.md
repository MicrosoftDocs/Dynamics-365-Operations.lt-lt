---
title: Kategorijos Data ir laikas ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie datos ir laiko funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 2dd8524c9cd368f0fe64347e3212b419bb0902b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744566"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Kategorijos Data ir laikas ER funkcijų sąrašas

[!include [banner](../includes/banner.md)]

Naudojant modulio Elektroninės ataskaitos (ER) datos ir laiko funkcijas, galima išgauti informaciją iš datos bei laiko reikšmių ir su jomis atlikti operacijas. Šioje temoje pateikiama šių funkcijų suvestinė.

## <a name="list-of-supported-functions"></a>Palaikomų funkcijų sąrašas

| Funkcija | Aprašymas |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos. |
| [DateFormat](er-functions-datetime-dateformat.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos / laiko reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos / laiko reikšmę. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos datos reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko (Grinvičo laiko \[GMT\]) formatu. |
| [DateValue](er-functions-datetime-datevalue.md) | Ši funkcija pateikia tipo *Data* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos reikšmę. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų nuo sausio 1 d. iki nurodytos datos skaičių. |
| [Dienos](er-functions-datetime-days.md) | Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų tarp pirmos nurodytos datos ir antros nurodytos datos skaičių. |
| [Now](er-functions-datetime-now.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo dabartinius programos serverio datą ir laiką. |
| [NullDate](er-functions-datetime-nulldate.md) | Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo **neapibrėžtą** datą (1900 m. sausio 1 d.). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo **neapibrėžtą** datos / laiko reikšmę (1900 m. sausio 1 d.) universaliojo laiko formatu. |
| [SessionNow](er-functions-datetime-sessionnow.md) | Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo dabartinius programos seanso datą ir laiką. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos seanso datą. |
| [Šiandien](er-functions-datetime-today.md) | Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos serverio datą. |

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų formulių kalba](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]