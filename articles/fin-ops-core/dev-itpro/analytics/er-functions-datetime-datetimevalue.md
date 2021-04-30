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
# <a name="datetimevalue-er-function"></a><span data-ttu-id="cc8d6-103">ER DATETIMEVALUE funkcija</span><span class="sxs-lookup"><span data-stu-id="cc8d6-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc8d6-104">`DATETIMEVALUE` funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes), konvertuojama į datos / laiko reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="cc8d6-105">Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](/dotnet/standard/base-types/standard-date-and-time-format-strings) ir [pasirinktinis](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="cc8d6-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="cc8d6-106">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="cc8d6-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="cc8d6-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="cc8d6-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="cc8d6-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="cc8d6-108">Arguments</span></span>

<span data-ttu-id="cc8d6-109">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="cc8d6-109">`text`: *String*</span></span>

<span data-ttu-id="cc8d6-110">Tekstas, nurodantis formatuotiną reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-110">Text that represents the value to format.</span></span>

<span data-ttu-id="cc8d6-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="cc8d6-111">`format`: *String*</span></span>

<span data-ttu-id="cc8d6-112">Nurodyto teksto formatas.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-112">The format of the given text.</span></span>

<span data-ttu-id="cc8d6-113">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="cc8d6-113">`culture`: *String*</span></span>

<span data-ttu-id="cc8d6-114">Kultūra, naudojama nurodytam tekstui formatuoti.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="cc8d6-115">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="cc8d6-115">Return values</span></span>

<span data-ttu-id="cc8d6-116">*Data ir laikas*</span><span class="sxs-lookup"><span data-stu-id="cc8d6-116">*DateTime*</span></span>

<span data-ttu-id="cc8d6-117">Gauta datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cc8d6-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="cc8d6-118">Usage notes</span></span>

<span data-ttu-id="cc8d6-119">Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="cc8d6-120">Pavyzdžiui, jei `DATETIMEVALUE` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="cc8d6-121">Numatytoji `culture` reikšmė yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="cc8d6-122">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="cc8d6-122">Example 1</span></span>

<span data-ttu-id="cc8d6-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` pagal nurodytą pasirinktinį formatą ir numatytąją programos **EN-US** kultūrą pateikia **2:55:00 AM on December 21, 2016**.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="cc8d6-124">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="cc8d6-124">Example 2</span></span>

<span data-ttu-id="cc8d6-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` pagal nurodytą pasirinktinį formatą ir kultūrą pateikia **2:55:00 AM on December 21, 2016**.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="cc8d6-126">Tačiau `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` pateikia išimtį, kad informuotų vartotoją, jog nurodyta eilutė nėra atpažįstama kaip tinkama nurodytos kultūros datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="cc8d6-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc8d6-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cc8d6-127">Additional resources</span></span>

[<span data-ttu-id="cc8d6-128">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="cc8d6-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]