---
title: ER DATEFORMAT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATEFORMAT funkcija.
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
ms.openlocfilehash: 0a9580b0ab9e472796375f498059ec0864a919ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563659"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="d3ec6-103">ER DATEFORMAT funkcija</span><span class="sxs-lookup"><span data-stu-id="d3ec6-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3ec6-104">`DATEFORMAT` funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="d3ec6-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="d3ec6-105">Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="d3ec6-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d3ec6-106">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="d3ec6-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d3ec6-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="d3ec6-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d3ec6-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="d3ec6-108">Arguments</span></span>

<span data-ttu-id="d3ec6-109">`date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="d3ec6-109">`date`: *Date*</span></span>

<span data-ttu-id="d3ec6-110">Datos reikšmė, nurodanti formatuotiną datą.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="d3ec6-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="d3ec6-111">`format`: *String*</span></span>

<span data-ttu-id="d3ec6-112">Išvesties eilutės formatas.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="d3ec6-113">Formato eilutė skiria didžiąsias ir mažąsias raides, kai naudojate tiek standartinį formatą, tiek pasirinktinį formatą.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="d3ec6-114">Pavyzdžiui, [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) „d” formato specifikatorius pateikia datą naudodamas trumpąjį datos formatas, o standartinis „D” formato specifikatorius pateikia datą naudodamas ilgąjį datos formatą.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="d3ec6-115">Taip pat, [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) „M” formato specifikatorius pateikia mėnesį nuo 1 iki 12, o pasirinktinis „m” formato specifikatorius pateikia minučių skaičių nuo 0 iki 59.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="d3ec6-116">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="d3ec6-116">`culture`: *String*</span></span>

<span data-ttu-id="d3ec6-117">Formatuojant naudotina kultūra.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="d3ec6-118">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="d3ec6-118">Return values</span></span>

<span data-ttu-id="d3ec6-119">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="d3ec6-119">*String*</span></span>

<span data-ttu-id="d3ec6-120">Gauta eilutės reikšmė.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d3ec6-121">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="d3ec6-121">Usage notes</span></span>

<span data-ttu-id="d3ec6-122">Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="d3ec6-123">Pavyzdžiui, jei `DATEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="d3ec6-124">Numatytoji `culture` reikšmė yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="d3ec6-125">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d3ec6-125">Example 1</span></span>

<span data-ttu-id="d3ec6-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` dabartinę programos serverio datą – 2015 m. gruodžio 24 d. – pagal nurodytą pasirinktinį formatą pateikia kaip eilutę **„24-12-2015“**.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="d3ec6-127">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d3ec6-127">Example 2</span></span>

<span data-ttu-id="d3ec6-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datą – 2015 m. gruodžio 24 d. – kaip eilutę **24-12-2015**.</span><span class="sxs-lookup"><span data-stu-id="d3ec6-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3ec6-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d3ec6-129">Additional resources</span></span>

[<span data-ttu-id="d3ec6-130">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="d3ec6-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]