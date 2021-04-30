---
title: NUMBERFORMAT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NUMBERFORMAT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890388"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="d7688-103">NUMBERFORMAT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="d7688-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7688-104">`NUMBERFORMAT` funkcija grąžina *Eilutės* reikšmę, kuri pateikia nurodytą skaičių nurodytu formatu ir pasirinktinai nurodytoje [kultūroje](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="d7688-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="d7688-105">Daugiau informacijos apie palaikomus formatus rasite [standartinis](/dotnet/standard/base-types/standard-numeric-format-strings) ir [pasirinktinis](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="d7688-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d7688-106">Sintaksė 1</span><span class="sxs-lookup"><span data-stu-id="d7688-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d7688-107">Sintaksė 2</span><span class="sxs-lookup"><span data-stu-id="d7688-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d7688-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="d7688-108">Arguments</span></span>

<span data-ttu-id="d7688-109">`number`: *Sveikasis* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="d7688-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="d7688-110">Skaitinė reikšmė, nurodanti skaičių, kuris turi būti suformatuotas.</span><span class="sxs-lookup"><span data-stu-id="d7688-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="d7688-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="d7688-111">`format` : *String*</span></span>

<span data-ttu-id="d7688-112">*Eilutės* reikšmė, nurodanti formatą.</span><span class="sxs-lookup"><span data-stu-id="d7688-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="d7688-113">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="d7688-113">`culture`: *String*</span></span>

<span data-ttu-id="d7688-114">*Eilutės* reikšmė, kuri nurodo formatavimui naudoti skirtą kultūrą.</span><span class="sxs-lookup"><span data-stu-id="d7688-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7688-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="d7688-115">Return values</span></span>

<span data-ttu-id="d7688-116">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="d7688-116">*String*</span></span>

<span data-ttu-id="d7688-117">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="d7688-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d7688-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="d7688-118">Usage notes</span></span>

<span data-ttu-id="d7688-119">Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, kontekstas, kuriame vykdoma ši funkcija, nustato kultūrą, naudojamą skaičiams formatuoti.</span><span class="sxs-lookup"><span data-stu-id="d7688-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="d7688-120">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d7688-120">Example 1</span></span>

<span data-ttu-id="d7688-121">**EN-US** kultūrai `NUMBERFORMAT (0.45, "p")` grąžina **„45.00 %“**, o `NUMBERFORMAT (10.45, "#")` grąžina **„10“**.</span><span class="sxs-lookup"><span data-stu-id="d7688-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d7688-122">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="d7688-122">Example 2</span></span>

<span data-ttu-id="d7688-123">`NUMBERFORMAT (10/3, "F2", "de")` grąžina **3,33**, o `NUMBERFORMAT (10/3, "F2", "en-us")` grąžina **3.33**.</span><span class="sxs-lookup"><span data-stu-id="d7688-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7688-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d7688-124">Additional resources</span></span>

[<span data-ttu-id="d7688-125">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="d7688-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]