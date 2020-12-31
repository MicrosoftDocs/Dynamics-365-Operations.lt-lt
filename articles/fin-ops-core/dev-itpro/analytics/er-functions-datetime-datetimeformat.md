---
title: ER DATETIMEFORMAT funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) DATETIMEFORMAT funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d42767b814f36eb75b4a43d07c663b2dd1b2c879
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684959"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="a80ff-103">ER DATETIMEFORMAT funkcija</span><span class="sxs-lookup"><span data-stu-id="a80ff-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a80ff-104">`DATETIMEFORMAT` funkcija pateikia tipo *Eilutė* reikšmę, kurioje pateikiama nurodyta datos / laiko reikšmė kaip tekstas nurodytu formatu ir, jei tai pasirenkama, nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="a80ff-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="a80ff-105">Daugiau informacijos apie palaikomus formatus rasite temose [standartinis](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="a80ff-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="a80ff-106">1-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="a80ff-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="a80ff-107">2-oji sintaksė</span><span class="sxs-lookup"><span data-stu-id="a80ff-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="a80ff-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="a80ff-108">Arguments</span></span>

<span data-ttu-id="a80ff-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="a80ff-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="a80ff-110">Datos / laiko reikšmė, nurodanti formatuotinus datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="a80ff-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="a80ff-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="a80ff-111">`format`: *String*</span></span>

<span data-ttu-id="a80ff-112">Išvesties eilutės formatas.</span><span class="sxs-lookup"><span data-stu-id="a80ff-112">The format of the output string.</span></span>

<span data-ttu-id="a80ff-113">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="a80ff-113">`culture`: *String*</span></span>

<span data-ttu-id="a80ff-114">Formatuojant naudotina kultūra.</span><span class="sxs-lookup"><span data-stu-id="a80ff-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="a80ff-115">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="a80ff-115">Return values</span></span>

<span data-ttu-id="a80ff-116">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="a80ff-116">*String*</span></span>

<span data-ttu-id="a80ff-117">Gauta eilutės reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a80ff-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a80ff-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="a80ff-118">Usage notes</span></span>

<span data-ttu-id="a80ff-119">Kai kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, `culture` reikšmę apibrėžia iškvietimo kontekstas.</span><span class="sxs-lookup"><span data-stu-id="a80ff-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="a80ff-120">Pavyzdžiui, jei `DATETIMEFORMAT` funkcija iškviečiama naudojant 1-ąją sintaksę elemento **FILE**, sukonfigūruoto naudoti Vokietijos kultūrą, modulio Elektroninės ataskaitos (ER) formate, bus konvertuojama naudojant Vokietijos kultūrą.</span><span class="sxs-lookup"><span data-stu-id="a80ff-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="a80ff-121">Numatytoji `culture` reikšmė yra **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="a80ff-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="a80ff-122">Kai `DATETIMEFORMAT` funkcija konvertuoja nurodytą datos / laiko reikšmę, ji atsižvelgia į programos vartotojo, vykdančio ER formatą, kurio kontekste funkcija iškviesta, laiko juostos parametrą.</span><span class="sxs-lookup"><span data-stu-id="a80ff-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="a80ff-123">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a80ff-123">Example 1</span></span>

<span data-ttu-id="a80ff-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` pateikia dabartinę programos serverio datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **„24-12-2015“** pagal nurodytą pasirinktinį formatą.</span><span class="sxs-lookup"><span data-stu-id="a80ff-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="a80ff-125">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a80ff-125">Example 2</span></span>

<span data-ttu-id="a80ff-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` pagal pasirinktą Vokietijos kultūrą ir nurodytą formatą pateikia dabartinę programos seanso datos / laiko reikšmę – 2015 m. gruodžio 24 d. – kaip **24.12.2015**.</span><span class="sxs-lookup"><span data-stu-id="a80ff-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="a80ff-127">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="a80ff-127">Example 3</span></span>

<span data-ttu-id="a80ff-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` pateikia eilutės reikšmę **2019-11-12T08:00:00.0000000-08:00**, kai ji iškviečiama vykdant procesą, kurį inicijavo programos vartotojas, skyriuje **Kalba ir šalies / regiono nuostatos** pasirinkęs laiko juostos reikšmę **(GMT-08:00) Ramiojo vandenyno laikas (JAV ir Kanada)**.</span><span class="sxs-lookup"><span data-stu-id="a80ff-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a80ff-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a80ff-129">Additional resources</span></span>

[<span data-ttu-id="a80ff-130">Datos ir laiko funkcijos</span><span class="sxs-lookup"><span data-stu-id="a80ff-130">Date and time functions</span></span>](er-functions-category-datetime.md)
