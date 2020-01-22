---
title: CONCATENATE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama CONCATENATE elektroninių ataskaitų (ER) funkcija
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915768"
---
# <span data-ttu-id="45f82-103"><a name="CONCATENATE">CONCATENATE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="45f82-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45f82-104">`CONCATENATE` funkcija grąžina visas nurodytas teksto eilutes kaip *Eilutės* reikšmę, sujungus jas į vieną eilutę.</span><span class="sxs-lookup"><span data-stu-id="45f82-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="45f82-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="45f82-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="45f82-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="45f82-106">Arguments</span></span>

<span data-ttu-id="45f82-107">`text 1`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="45f82-107">`text 1`: *String*</span></span>

<span data-ttu-id="45f82-108">Nuoroda į duomenų šaltinį, kuris yra *Eilutės* duomenų tipas.</span><span class="sxs-lookup"><span data-stu-id="45f82-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="45f82-109">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="45f82-109">This argument is required.</span></span>

<span data-ttu-id="45f82-110">`text N`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="45f82-110">`text N`: *String*</span></span>

<span data-ttu-id="45f82-111">Nuoroda į duomenų šaltinį, kuris yra *Eilutės* duomenų tipas.</span><span class="sxs-lookup"><span data-stu-id="45f82-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="45f82-112">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="45f82-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="45f82-113">Grįžimo vertės</span><span class="sxs-lookup"><span data-stu-id="45f82-113">Return values</span></span>

<span data-ttu-id="45f82-114">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="45f82-114">*String*</span></span>

<span data-ttu-id="45f82-115">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="45f82-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="45f82-116">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="45f82-116">Example</span></span>

<span data-ttu-id="45f82-117">`CONCATENATE ("abc", "def")`grąžina **„abcdef“**.</span><span class="sxs-lookup"><span data-stu-id="45f82-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="45f82-118">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="45f82-118">Usage notes</span></span>

<span data-ttu-id="45f82-119">Išraiška `"abc" & "def"` taip pat grąžina **„abcdef“**.</span><span class="sxs-lookup"><span data-stu-id="45f82-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45f82-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="45f82-120">Additional resources</span></span>

[<span data-ttu-id="45f82-121">Tekstinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="45f82-121">Text functions</span></span>](er-functions-category-text.md)
