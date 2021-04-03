---
title: ER DATETIMEFORMAT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETIMEFORMAT funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b7516620763e87440c0fb866ce507c744223a229
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563635"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="73bda-103">ER DATETIMEFORMAT funkcija</span><span class="sxs-lookup"><span data-stu-id="73bda-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73bda-104">`DATETIMEFORMAT` funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos / laiko reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="73bda-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="73bda-105">Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="73bda-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="73bda-106">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="73bda-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="73bda-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="73bda-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="73bda-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="73bda-108">Arguments</span></span>

<span data-ttu-id="73bda-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="73bda-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="73bda-110">Datos / laiko reikšmė, nurodanti formatuotinus datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="73bda-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="73bda-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="73bda-111">`format`: *String*</span></span>

<span data-ttu-id="73bda-112">Išvesties eilutės formatas.</span><span class="sxs-lookup"><span data-stu-id="73bda-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="73bda-113">Formato eilutė skiria didžiąsias ir mažąsias raides, kai naudojate tiek standartinį formatą, tiek pasirinktinį formatą.</span><span class="sxs-lookup"><span data-stu-id="73bda-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="73bda-114">Pavyzdžiui, [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) „d” formato specifikatorius pateikia datą naudodamas trumpąjį datos formatas, o standartinis „D” formato specifikatorius pateikia datą naudodamas ilgąjį datos formatą.</span><span class="sxs-lookup"><span data-stu-id="73bda-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="73bda-115">Taip pat, [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) „M” formato specifikatorius pateikia mėnesį nuo 1 iki 12, o pasirinktinis „m” formato specifikatorius pateikia minučių skaičių nuo 0 iki 59.</span><span class="sxs-lookup"><span data-stu-id="73bda-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="73bda-116">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="73bda-116">`culture`: *String*</span></span>

<span data-ttu-id="73bda-117">Formatuojant naudotina kultūra.</span><span class="sxs-lookup"><span data-stu-id="73bda-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="73bda-118">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="73bda-118">Return values</span></span>

<span data-ttu-id="73bda-119">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="73bda-119">*String*</span></span>

<span data-ttu-id="73bda-120">Gauta eilutės reikšmė.</span><span class="sxs-lookup"><span data-stu-id="73bda-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="73bda-121">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="73bda-121">Usage notes</span></span>

<span data-ttu-id="73bda-122">Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas.</span><span class="sxs-lookup"><span data-stu-id="73bda-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="73bda-123">Pavyzdžiui, jei `DATETIMEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą.</span><span class="sxs-lookup"><span data-stu-id="73bda-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="73bda-124">Numatytoji `culture` reikšmė yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="73bda-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="73bda-125">Kai `DATETIMEFORMAT` funkcija konvertuoja nurodytą datos / laiko reikšmę, ji atsižvelgia į programos vartotojo, vykdančio ER formatą, kurio kontekste funkcija iškviesta, laiko juostos parametrą.</span><span class="sxs-lookup"><span data-stu-id="73bda-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="73bda-126">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="73bda-126">Example 1</span></span>

<span data-ttu-id="73bda-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pateikia dabartinę programos serverio datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **„24-12-2015“** pagal nurodytą pasirinktinį formatą.</span><span class="sxs-lookup"><span data-stu-id="73bda-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="73bda-128">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="73bda-128">Example 2</span></span>

<span data-ttu-id="73bda-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **24.12.2015**.</span><span class="sxs-lookup"><span data-stu-id="73bda-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="73bda-130">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="73bda-130">Example 3</span></span>

<span data-ttu-id="73bda-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` pateikia eilutės reikšmę **„2019-11-12T08:00:00.0000000-08:00”** tada, kai funkcija iškviečiama vykdant procesą, kurį inicijavo programos vartotojas, pasirinkęs **(GMT-08:00) Ramiojo vandenyno laikas (JAV ir Kanada)** laiko juostos reikšmę **Kalba ir šalies/regiono nuostatos** skyriuje.</span><span class="sxs-lookup"><span data-stu-id="73bda-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73bda-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="73bda-132">Additional resources</span></span>

[<span data-ttu-id="73bda-133">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="73bda-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]