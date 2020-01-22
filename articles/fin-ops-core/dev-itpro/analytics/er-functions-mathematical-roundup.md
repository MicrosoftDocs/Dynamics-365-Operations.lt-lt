---
title: ROUNDUP ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ROUNDUP elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917056"
---
# <span data-ttu-id="27a65-103"><a name="ROUNDUP">ROUNDUP ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="27a65-103"><a name="ROUNDUP">ROUNDUP ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27a65-104">`ROUNDUP` funkcija grąžina nurodytą skaičių kaip *realiojo skaičiaus* reikšmę, suapvalintą su pertekliumi iki nurodyto skaičiaus po kablelio.</span><span class="sxs-lookup"><span data-stu-id="27a65-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="27a65-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="27a65-105">Syntax</span></span>

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="27a65-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="27a65-106">Arguments</span></span>

<span data-ttu-id="27a65-107">`number`: *Realusis*</span><span class="sxs-lookup"><span data-stu-id="27a65-107">`number`: *Real*</span></span>

<span data-ttu-id="27a65-108">Skaitinė reikšmė, kurią reikia apvalinti su pertekliumi.</span><span class="sxs-lookup"><span data-stu-id="27a65-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="27a65-109">`decimals`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="27a65-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="27a65-110">Skaitinė reikšmė, nurodanti skaičių po kablelio.</span><span class="sxs-lookup"><span data-stu-id="27a65-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="27a65-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="27a65-111">Return values</span></span>

<span data-ttu-id="27a65-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="27a65-112">*Real*</span></span>

<span data-ttu-id="27a65-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="27a65-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="27a65-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="27a65-114">Usage notes</span></span>

<span data-ttu-id="27a65-115">Ši funkcija veikia kaip ir [ROUND](er-functions-mathematical-round.md), bet ji visada apvalina nurodytą skaičių į didesnę pusę (nuo nulio).</span><span class="sxs-lookup"><span data-stu-id="27a65-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="27a65-116">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="27a65-116">Example 1</span></span>

<span data-ttu-id="27a65-117">`ROUNDUP (1200.763, 2)` suapvalina su pertekliumi iki dviejų skaičių po kablelio ir grąžina **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="27a65-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="27a65-118">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="27a65-118">Example 2</span></span>

<span data-ttu-id="27a65-119">`ROUNDUP (1200.767, -3)` suapvalina su pertekliumi iki artimiausio 1000 kartotinio ir grąžina **2000**.</span><span class="sxs-lookup"><span data-stu-id="27a65-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27a65-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="27a65-120">Additional resources</span></span>

[<span data-ttu-id="27a65-121">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="27a65-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
