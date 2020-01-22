---
title: ER DATETIMEVALUE funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETIMEVALUE funkcija.
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
ms.openlocfilehash: de601ad08b85797a4241ef74ecb3eba37eda37ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917539"
---
# <span data-ttu-id="ee24b-103"><a name="DATETIMEVALUE">ER DATETIMEVALUE funkcija</a></span><span class="sxs-lookup"><span data-stu-id="ee24b-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee24b-104">`DATETIMEVALUE` funkcija pateikia *DateTime* reikšmę, kuri iš nurodytos teksto reikšmės nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes), konvertuojama į datos / laiko reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee24b-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="ee24b-105">Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ee24b-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ee24b-106">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="ee24b-106">Syntax 1</span></span>

```
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ee24b-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="ee24b-107">Syntax 2</span></span>

```
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ee24b-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="ee24b-108">Arguments</span></span>

<span data-ttu-id="ee24b-109">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="ee24b-109">`text`: *String*</span></span>

<span data-ttu-id="ee24b-110">Tekstas, nurodantis formatuotiną reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ee24b-110">Text that represents the value to format.</span></span>

<span data-ttu-id="ee24b-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="ee24b-111">`format`: *String*</span></span>

<span data-ttu-id="ee24b-112">Nurodyto teksto formatas.</span><span class="sxs-lookup"><span data-stu-id="ee24b-112">The format of the given text.</span></span>

<span data-ttu-id="ee24b-113">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="ee24b-113">`culture`: *String*</span></span>

<span data-ttu-id="ee24b-114">Kultūra, naudojama nurodytam tekstui formatuoti.</span><span class="sxs-lookup"><span data-stu-id="ee24b-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="ee24b-115">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="ee24b-115">Return values</span></span>

<span data-ttu-id="ee24b-116">*Data ir laikas*</span><span class="sxs-lookup"><span data-stu-id="ee24b-116">*DateTime*</span></span>

<span data-ttu-id="ee24b-117">Gauta datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="ee24b-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ee24b-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="ee24b-118">Usage notes</span></span>

<span data-ttu-id="ee24b-119">Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas.</span><span class="sxs-lookup"><span data-stu-id="ee24b-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ee24b-120">Pavyzdžiui, jei `DATETIMEVALUE` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą.</span><span class="sxs-lookup"><span data-stu-id="ee24b-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ee24b-121">Numatytoji `culture` reikšmė yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="ee24b-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="ee24b-122">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ee24b-122">Example 1</span></span>

<span data-ttu-id="ee24b-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` pagal nurodytą pasirinktinį formatą ir numatytąją programos **EN-US** kultūrą pateikia **2:55:00 AM on December 21, 2016**.</span><span class="sxs-lookup"><span data-stu-id="ee24b-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="ee24b-124">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ee24b-124">Example 2</span></span>

<span data-ttu-id="ee24b-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` pagal nurodytą pasirinktinį formatą ir kultūrą pateikia **2:55:00 AM on December 21, 2016**.</span><span class="sxs-lookup"><span data-stu-id="ee24b-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="ee24b-126">Tačiau `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` pateikia išimtį, kad informuotų vartotoją, jog nurodyta eilutė nėra atpažįstama kaip tinkama nurodytos kultūros datos / laiko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="ee24b-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee24b-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ee24b-127">Additional resources</span></span>

[<span data-ttu-id="ee24b-128">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="ee24b-128">Date and time functions</span></span>](er-functions-category-datetime.md)
