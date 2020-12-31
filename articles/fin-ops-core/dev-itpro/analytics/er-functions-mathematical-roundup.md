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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ed86e2a848248dd8f2fc99401d12e0a162bf20a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686839"
---
# <a name="roundup-er-function"></a><span data-ttu-id="fe1d3-103">ROUNDUP ER funkcija</span><span class="sxs-lookup"><span data-stu-id="fe1d3-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe1d3-104">`ROUNDUP` funkcija grąžina nurodytą skaičių kaip *realiojo skaičiaus* reikšmę, suapvalintą su pertekliumi iki nurodyto skaičiaus po kablelio.</span><span class="sxs-lookup"><span data-stu-id="fe1d3-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe1d3-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="fe1d3-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="fe1d3-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="fe1d3-106">Arguments</span></span>

<span data-ttu-id="fe1d3-107">`number`: *Realusis*</span><span class="sxs-lookup"><span data-stu-id="fe1d3-107">`number`: *Real*</span></span>

<span data-ttu-id="fe1d3-108">Skaitinė reikšmė, kurią reikia apvalinti su pertekliumi.</span><span class="sxs-lookup"><span data-stu-id="fe1d3-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="fe1d3-109">`decimals`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="fe1d3-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="fe1d3-110">Skaitinė reikšmė, nurodanti skaičių po kablelio.</span><span class="sxs-lookup"><span data-stu-id="fe1d3-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="fe1d3-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="fe1d3-111">Return values</span></span>

<span data-ttu-id="fe1d3-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="fe1d3-112">*Real*</span></span>

<span data-ttu-id="fe1d3-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="fe1d3-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fe1d3-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="fe1d3-114">Usage notes</span></span>

<span data-ttu-id="fe1d3-115">Ši funkcija veikia kaip ir [ROUND](er-functions-mathematical-round.md), bet ji visada apvalina nurodytą skaičių į didesnę pusę (nuo nulio).</span><span class="sxs-lookup"><span data-stu-id="fe1d3-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="fe1d3-116">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="fe1d3-116">Example 1</span></span>

<span data-ttu-id="fe1d3-117">`ROUNDUP (1200.763, 2)` suapvalina su pertekliumi iki dviejų skaičių po kablelio ir grąžina **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="fe1d3-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fe1d3-118">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="fe1d3-118">Example 2</span></span>

<span data-ttu-id="fe1d3-119">`ROUNDUP (1200.767, -3)` suapvalina su pertekliumi iki artimiausio 1000 kartotinio ir grąžina **2000**.</span><span class="sxs-lookup"><span data-stu-id="fe1d3-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe1d3-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="fe1d3-120">Additional resources</span></span>

[<span data-ttu-id="fe1d3-121">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="fe1d3-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
