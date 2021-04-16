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
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746223"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="9b805-103">NUMBERFORMAT ER funkcija</span><span class="sxs-lookup"><span data-stu-id="9b805-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b805-104">`NUMBERFORMAT` funkcija grąžina *Eilutės* reikšmę, kuri pateikia nurodytą skaičių nurodytu formatu ir pasirinktinai nurodytoje [kultūroje](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="9b805-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="9b805-105">Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="9b805-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="9b805-106">Sintaksė 1</span><span class="sxs-lookup"><span data-stu-id="9b805-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="9b805-107">Sintaksė 2</span><span class="sxs-lookup"><span data-stu-id="9b805-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="9b805-108">Argumentai</span><span class="sxs-lookup"><span data-stu-id="9b805-108">Arguments</span></span>

<span data-ttu-id="9b805-109">`number`: *Sveikasis* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="9b805-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="9b805-110">Skaitinė reikšmė, nurodanti skaičių, kuris turi būti suformatuotas.</span><span class="sxs-lookup"><span data-stu-id="9b805-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="9b805-111">`format`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9b805-111">`format` : *String*</span></span>

<span data-ttu-id="9b805-112">*Eilutės* reikšmė, nurodanti formatą.</span><span class="sxs-lookup"><span data-stu-id="9b805-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="9b805-113">`culture`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9b805-113">`culture`: *String*</span></span>

<span data-ttu-id="9b805-114">*Eilutės* reikšmė, kuri nurodo formatavimui naudoti skirtą kultūrą.</span><span class="sxs-lookup"><span data-stu-id="9b805-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="9b805-115">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="9b805-115">Return values</span></span>

<span data-ttu-id="9b805-116">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="9b805-116">*String*</span></span>

<span data-ttu-id="9b805-117">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="9b805-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9b805-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="9b805-118">Usage notes</span></span>

<span data-ttu-id="9b805-119">Jei kultūra nėra apibrėžiama kaip iškviestos funkcijos argumentas, kontekstas, kuriame vykdoma ši funkcija, nustato kultūrą, naudojamą skaičiams formatuoti.</span><span class="sxs-lookup"><span data-stu-id="9b805-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="9b805-120">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9b805-120">Example 1</span></span>

<span data-ttu-id="9b805-121">**EN-US** kultūrai `NUMBERFORMAT (0.45, "p")` grąžina **„45.00 %“**, o `NUMBERFORMAT (10.45, "#")` grąžina **„10“**.</span><span class="sxs-lookup"><span data-stu-id="9b805-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="9b805-122">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9b805-122">Example 2</span></span>

<span data-ttu-id="9b805-123">`NUMBERFORMAT (10/3, "F2", "de")` grąžina **3,33**, o `NUMBERFORMAT (10/3, "F2", "en-us")` grąžina **3.33**.</span><span class="sxs-lookup"><span data-stu-id="9b805-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b805-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9b805-124">Additional resources</span></span>

[<span data-ttu-id="9b805-125">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="9b805-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]