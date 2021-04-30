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
# <a name="datetimeformat-er-function"></a><span data-ttu-id="71164-103">ER DATETIMEFORMAT funkcija</span><span class="sxs-lookup"><span data-stu-id="71164-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71164-104">`DATETIMEFORMAT` funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos / laiko reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="71164-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="71164-105">Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) ir [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="71164-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="71164-106">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="71164-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="71164-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="71164-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="71164-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="71164-108">Arguments</span></span>

<span data-ttu-id="71164-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="71164-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="71164-110">Datos / laiko reikšmė, nurodanti formatuotinus datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="71164-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="71164-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71164-111">`format`: *String*</span></span>

<span data-ttu-id="71164-112">Išvesties eilutės formatas.</span><span class="sxs-lookup"><span data-stu-id="71164-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="71164-113">Formato eilutė skiria didžiąsias ir mažąsias raides, kai naudojate tiek standartinį formatą, tiek pasirinktinį formatą.</span><span class="sxs-lookup"><span data-stu-id="71164-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="71164-114">Pavyzdžiui, [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) „d” formato specifikatorius pateikia datą naudodamas trumpąjį datos formatas, o standartinis „D” formato specifikatorius pateikia datą naudodamas ilgąjį datos formatą.</span><span class="sxs-lookup"><span data-stu-id="71164-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="71164-115">Taip pat, [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings) „M” formato specifikatorius pateikia mėnesį nuo 1 iki 12, o pasirinktinis „m” formato specifikatorius pateikia minučių skaičių nuo 0 iki 59.</span><span class="sxs-lookup"><span data-stu-id="71164-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="71164-116">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71164-116">`culture`: *String*</span></span>

<span data-ttu-id="71164-117">Formatuojant naudotina kultūra.</span><span class="sxs-lookup"><span data-stu-id="71164-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="71164-118">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="71164-118">Return values</span></span>

<span data-ttu-id="71164-119">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="71164-119">*String*</span></span>

<span data-ttu-id="71164-120">Gauta eilutės reikšmė.</span><span class="sxs-lookup"><span data-stu-id="71164-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="71164-121">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="71164-121">Usage notes</span></span>

<span data-ttu-id="71164-122">Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas.</span><span class="sxs-lookup"><span data-stu-id="71164-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="71164-123">Pavyzdžiui, jei `DATETIMEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą.</span><span class="sxs-lookup"><span data-stu-id="71164-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="71164-124">Numatytoji `culture` reikšmė yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="71164-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="71164-125">Kai `DATETIMEFORMAT` funkcija konvertuoja nurodytą datos / laiko reikšmę, ji atsižvelgia į programos vartotojo, vykdančio ER formatą, kurio kontekste funkcija iškviesta, laiko juostos parametrą.</span><span class="sxs-lookup"><span data-stu-id="71164-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="71164-126">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="71164-126">Example 1</span></span>

<span data-ttu-id="71164-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pateikia dabartinę programos serverio datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **„24-12-2015“** pagal nurodytą pasirinktinį formatą.</span><span class="sxs-lookup"><span data-stu-id="71164-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="71164-128">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="71164-128">Example 2</span></span>

<span data-ttu-id="71164-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **24.12.2015**.</span><span class="sxs-lookup"><span data-stu-id="71164-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="71164-130">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="71164-130">Example 3</span></span>

<span data-ttu-id="71164-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` pateikia eilutės reikšmę **„2019-11-12T08:00:00.0000000-08:00”** tada, kai funkcija iškviečiama vykdant procesą, kurį inicijavo programos vartotojas, pasirinkęs **(GMT-08:00) Ramiojo vandenyno laikas (JAV ir Kanada)** laiko juostos reikšmę **Kalba ir šalies/regiono nuostatos** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="71164-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71164-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="71164-132">Additional resources</span></span>

[<span data-ttu-id="71164-133">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="71164-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]