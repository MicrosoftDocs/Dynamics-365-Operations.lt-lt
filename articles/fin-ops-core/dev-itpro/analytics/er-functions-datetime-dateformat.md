---
title: ER DATEFORMAT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATEFORMAT funkcija.
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
ms.openlocfilehash: 759ccd3cf16c6c109faf44cea350745e3b2bff0b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042440"
---
# <span data-ttu-id="ef9ed-103"><a name="DATEFORMAT">ER DATEFORMAT funkcija</a></span><span class="sxs-lookup"><span data-stu-id="ef9ed-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef9ed-104">`DATEFORMAT` funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="ef9ed-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="ef9ed-105">Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ef9ed-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ef9ed-106">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="ef9ed-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ef9ed-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="ef9ed-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ef9ed-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="ef9ed-108">Arguments</span></span>

<span data-ttu-id="ef9ed-109">`date`: *Data*</span><span class="sxs-lookup"><span data-stu-id="ef9ed-109">`date`: *Date*</span></span>

<span data-ttu-id="ef9ed-110">Datos reikšmė, nurodanti formatuotiną datą.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="ef9ed-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="ef9ed-111">`format`: *String*</span></span>

<span data-ttu-id="ef9ed-112">Išvesties eilutės formatas.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-112">The format of the output string.</span></span>

<span data-ttu-id="ef9ed-113">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="ef9ed-113">`culture`: *String*</span></span>

<span data-ttu-id="ef9ed-114">Formatuojant naudotina kultūra.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="ef9ed-115">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="ef9ed-115">Return values</span></span>

<span data-ttu-id="ef9ed-116">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="ef9ed-116">*String*</span></span>

<span data-ttu-id="ef9ed-117">Gauta eilutės reikšmė.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ef9ed-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="ef9ed-118">Usage notes</span></span>

<span data-ttu-id="ef9ed-119">Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ef9ed-120">Pavyzdžiui, jei `DATEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ef9ed-121">Numatytoji `culture` reikšmė yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="ef9ed-122">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ef9ed-122">Example 1</span></span>

<span data-ttu-id="ef9ed-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` dabartinę programos serverio datą – 2015 m. gruodžio 24 d. – pagal nurodytą pasirinktinį formatą pateikia kaip eilutę **„24-12-2015“**.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="ef9ed-124">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ef9ed-124">Example 2</span></span>

<span data-ttu-id="ef9ed-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datą – 2015 m. gruodžio 24 d. – kaip eilutę **24-12-2015**.</span><span class="sxs-lookup"><span data-stu-id="ef9ed-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef9ed-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ef9ed-126">Additional resources</span></span>

[<span data-ttu-id="ef9ed-127">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="ef9ed-127">Date and time functions</span></span>](er-functions-category-datetime.md)
