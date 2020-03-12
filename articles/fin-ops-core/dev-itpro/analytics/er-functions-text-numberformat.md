---
title: NUMBERFORMAT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NUMBERFORMAT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070557"
---
# <span data-ttu-id="befd6-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="befd6-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="befd6-104">`NUMBERFORMAT` funkcija grąžina *Eilutės* reikšmę, kuri pateikia nurodytą skaičių nurodytu formatu ir pasirinktinai nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="befd6-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="befd6-105">Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="befd6-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="befd6-106">Sintaksė 1</span><span class="sxs-lookup"><span data-stu-id="befd6-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="befd6-107">Sintaksė 2</span><span class="sxs-lookup"><span data-stu-id="befd6-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="befd6-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="befd6-108">Arguments</span></span>

<span data-ttu-id="befd6-109">`number`: *Sveikasis* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="befd6-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="befd6-110">Skaitinė reikšmė, nurodanti skaičių, kuris turi būti suformatuotas.</span><span class="sxs-lookup"><span data-stu-id="befd6-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="befd6-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="befd6-111">`format` : *String*</span></span>

<span data-ttu-id="befd6-112">*Eilutės* reikšmė, nurodanti formatą.</span><span class="sxs-lookup"><span data-stu-id="befd6-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="befd6-113">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="befd6-113">`culture`: *String*</span></span>

<span data-ttu-id="befd6-114">*Eilutės* reikšmė, kuri nurodo formatavimui naudoti skirtą kultūrą.</span><span class="sxs-lookup"><span data-stu-id="befd6-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="befd6-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="befd6-115">Return values</span></span>

<span data-ttu-id="befd6-116">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="befd6-116">*String*</span></span>

<span data-ttu-id="befd6-117">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="befd6-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="befd6-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="befd6-118">Usage notes</span></span>

<span data-ttu-id="befd6-119">Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, kontekstas, kuriame vykdoma ši funkcija, nustato kultūrą, naudojamą skaičiams formatuoti.</span><span class="sxs-lookup"><span data-stu-id="befd6-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="befd6-120">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="befd6-120">Example 1</span></span>

<span data-ttu-id="befd6-121">**EN-US** kultūrai `NUMBERFORMAT (0.45, "p")` grąžina **„45.00 %“**, o `NUMBERFORMAT (10.45, "#")` grąžina **„10“**.</span><span class="sxs-lookup"><span data-stu-id="befd6-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="befd6-122">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="befd6-122">Example 2</span></span>

<span data-ttu-id="befd6-123">`NUMBERFORMAT (10/3, "F2", "de")` grąžina **3,33**, o `NUMBERFORMAT (10/3, "F2", "en-us")` grąžina **3.33**.</span><span class="sxs-lookup"><span data-stu-id="befd6-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="befd6-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="befd6-124">Additional resources</span></span>

[<span data-ttu-id="befd6-125">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="befd6-125">Text functions</span></span>](er-functions-category-text.md)
