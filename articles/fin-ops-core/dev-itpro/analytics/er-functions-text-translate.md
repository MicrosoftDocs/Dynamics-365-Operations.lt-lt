---
title: TRANSLATE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama TRANSLATE elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040922"
---
# <span data-ttu-id="eb406-103"><a name="TRANSLATE">TRANSLATE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="eb406-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb406-104">`TRANSLATE` funkcija grąžina nurodytą teksto eilutę kaip *Eilutės* reikšmę po to, kai visa arba jos dalis buvo pakeista kita eilute.</span><span class="sxs-lookup"><span data-stu-id="eb406-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb406-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="eb406-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="eb406-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="eb406-106">Arguments</span></span>

<span data-ttu-id="eb406-107">`text`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="eb406-107">`text`: *String*</span></span>

<span data-ttu-id="eb406-108">Tinkamas *Eilutės* tipo duomenų šaltinio maršrutas.</span><span class="sxs-lookup"><span data-stu-id="eb406-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="eb406-109">`pattern`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="eb406-109">`pattern`: *String*</span></span>

<span data-ttu-id="eb406-110">Tekstas, kuris turi būti pakeistas.</span><span class="sxs-lookup"><span data-stu-id="eb406-110">The text that must be replaced.</span></span>

<span data-ttu-id="eb406-111">`replacement`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="eb406-111">`replacement`: *String*</span></span>

<span data-ttu-id="eb406-112">Tekstas, kurį norite naudoti kaip pakaitą.</span><span class="sxs-lookup"><span data-stu-id="eb406-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="eb406-113">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="eb406-113">Return values</span></span>

<span data-ttu-id="eb406-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="eb406-114">*String*</span></span>

<span data-ttu-id="eb406-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="eb406-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="eb406-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="eb406-116">Example</span></span>

<span data-ttu-id="eb406-117">`TRANSLATE ("abcdef", "cd", "GH")` pakeičia šabloną **„cd“** į eilutę **„GH“** ir grąžinama **„abGHef“**.</span><span class="sxs-lookup"><span data-stu-id="eb406-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eb406-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="eb406-118">Additional resources</span></span>

[<span data-ttu-id="eb406-119">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="eb406-119">Text functions</span></span>](er-functions-category-text.md)
