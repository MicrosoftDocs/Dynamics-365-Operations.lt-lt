---
title: Kategorijos Data ir laikas ER funkcijų sąrašas
description: Šioje temoje pateikiama informacijos apie datos ir laiko funkcijas, palaikomas modulyje Elektroninės ataskaitos (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916573"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="5773d-103">Kategorijos Data ir laikas ER funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="5773d-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5773d-104">Naudojant modulio Elektroninės ataskaitos (ER) datos ir laiko funkcijas, galima išgauti informaciją iš datos bei laiko reikšmių ir su jomis atlikti operacijas.</span><span class="sxs-lookup"><span data-stu-id="5773d-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="5773d-105">Šioje temoje pateikiama šių funkcijų suvestinė.</span><span class="sxs-lookup"><span data-stu-id="5773d-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="5773d-106">Palaikomų funkcijų sąrašas</span><span class="sxs-lookup"><span data-stu-id="5773d-106">List of supported functions</span></span>

| <span data-ttu-id="5773d-107">Funkcija</span><span class="sxs-lookup"><span data-stu-id="5773d-107">Function</span></span> | <span data-ttu-id="5773d-108">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="5773d-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="5773d-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="5773d-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="5773d-110">Ši funkcija pateikia *DateTime* reikšmę, kuri yra nurodytas dienų skaičius prieš nurodytą pradžios datą arba po jos.</span><span class="sxs-lookup"><span data-stu-id="5773d-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="5773d-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="5773d-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="5773d-112">Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje.</span><span class="sxs-lookup"><span data-stu-id="5773d-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="5773d-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5773d-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="5773d-114">Ši funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos / laiko reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje.</span><span class="sxs-lookup"><span data-stu-id="5773d-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="5773d-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="5773d-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="5773d-116">Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos / laiko reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5773d-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="5773d-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="5773d-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="5773d-118">Ši funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos datos reikšmės konvertuojama į datos / laiko reikšmę universaliojo laiko (Grinvičo laiko \[GMT\]) formatu.</span><span class="sxs-lookup"><span data-stu-id="5773d-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="5773d-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="5773d-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="5773d-120">Ši funkcija pateikia tipo *Data* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje kultūroje, konvertuojama į datos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5773d-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="5773d-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="5773d-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="5773d-122">Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų nuo sausio 1 d. iki nurodytos datos skaičių.</span><span class="sxs-lookup"><span data-stu-id="5773d-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="5773d-123">Dienos</span><span class="sxs-lookup"><span data-stu-id="5773d-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="5773d-124">Ši funkcija pateikia tipo *Sveikasis skaičius* reikšmę, nurodančią dienų tarp pirmos nurodytos datos ir antros nurodytos datos skaičių.</span><span class="sxs-lookup"><span data-stu-id="5773d-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="5773d-125">Now</span><span class="sxs-lookup"><span data-stu-id="5773d-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="5773d-126">Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo dabartinius programos serverio datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="5773d-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="5773d-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="5773d-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="5773d-128">Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo **neapibrėžtą** datą (1900 m. sausio 1 d.).</span><span class="sxs-lookup"><span data-stu-id="5773d-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="5773d-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="5773d-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="5773d-130">Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo **neapibrėžtą** datos / laiko reikšmę (1900 m. sausio 1 d.) universaliojo laiko formatu.</span><span class="sxs-lookup"><span data-stu-id="5773d-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="5773d-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="5773d-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="5773d-132">Ši funkcija pateikia *DateTime* reikšmę, kuri nurodo dabartinius programos seanso datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="5773d-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="5773d-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="5773d-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="5773d-134">Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos seanso datą.</span><span class="sxs-lookup"><span data-stu-id="5773d-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="5773d-135">Šiandien</span><span class="sxs-lookup"><span data-stu-id="5773d-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="5773d-136">Ši funkcija pateikia tipo *Data* reikšmę, kuri nurodo dabartinę programos serverio datą.</span><span class="sxs-lookup"><span data-stu-id="5773d-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="5773d-137">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5773d-137">Additional resources</span></span>

[<span data-ttu-id="5773d-138">Elektroninių ataskaitų apžvalga</span><span class="sxs-lookup"><span data-stu-id="5773d-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="5773d-139">Elektroninių ataskaitų formulių kūrimo įrankis</span><span class="sxs-lookup"><span data-stu-id="5773d-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="5773d-140">Elektroninių ataskaitų formulių kalba</span><span class="sxs-lookup"><span data-stu-id="5773d-140">Electronic reporting formula language</span></span>](er-formula-language.md)
