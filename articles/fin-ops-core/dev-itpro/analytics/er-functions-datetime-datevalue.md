---
title: ER DATEVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATEVALUE funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cfaf183c61d3663442cbc244239b872b9e1957bb
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891238"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="26833-103">ER DATEVALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="26833-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26833-104">`DATEVALUE` funkcija pateikia tipo *Data* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes), konvertuojama į datos reikšmę.</span><span class="sxs-lookup"><span data-stu-id="26833-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="26833-105">Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) ir [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="26833-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="26833-106">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="26833-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="26833-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="26833-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="26833-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="26833-108">Arguments</span></span>

<span data-ttu-id="26833-109">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="26833-109">`text`: *String*</span></span>

<span data-ttu-id="26833-110">Tekstas, nurodantis formatuotiną reikšmę.</span><span class="sxs-lookup"><span data-stu-id="26833-110">Text that represents the value to format.</span></span>

<span data-ttu-id="26833-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="26833-111">`format`: *String*</span></span>

<span data-ttu-id="26833-112">Nurodyto teksto formatas.</span><span class="sxs-lookup"><span data-stu-id="26833-112">The format of the given text.</span></span>

<span data-ttu-id="26833-113">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="26833-113">`culture`: *String*</span></span>

<span data-ttu-id="26833-114">Kultūra, naudojama nurodytam tekstui formatuoti.</span><span class="sxs-lookup"><span data-stu-id="26833-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="26833-115">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="26833-115">Return values</span></span>

<span data-ttu-id="26833-116">*Data*</span><span class="sxs-lookup"><span data-stu-id="26833-116">*Date*</span></span>

<span data-ttu-id="26833-117">Gauta datos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="26833-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="26833-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="26833-118">Usage notes</span></span>

<span data-ttu-id="26833-119">Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas.</span><span class="sxs-lookup"><span data-stu-id="26833-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="26833-120">Pavyzdžiui, jei `DATEVALUE` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą.</span><span class="sxs-lookup"><span data-stu-id="26833-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="26833-121">Numatytoji `culture` reikšmė yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="26833-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="26833-122">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="26833-122">Example 1</span></span>

<span data-ttu-id="26833-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` pagal nurodytą pasirinktinį formatą ir numatytąją programos **EN-US** kultūrą pateikia datos reikšmę **December 21, 2016**.</span><span class="sxs-lookup"><span data-stu-id="26833-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="26833-124">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="26833-124">Example 2</span></span>

<span data-ttu-id="26833-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` pagal nurodytą pasirinktinį formatą ir kultūrą pateikia datos reikšmę **January 21, 2016**.</span><span class="sxs-lookup"><span data-stu-id="26833-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="26833-126">Tačiau `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` pateikia išimtį, kad informuotų vartotoją, jog nurodyta eilutė nėra atpažįstama kaip tinkama nurodytos kultūros data.</span><span class="sxs-lookup"><span data-stu-id="26833-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26833-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="26833-127">Additional resources</span></span>

[<span data-ttu-id="26833-128">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="26833-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]