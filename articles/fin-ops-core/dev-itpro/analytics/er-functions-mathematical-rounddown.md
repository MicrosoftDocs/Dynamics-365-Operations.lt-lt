---
title: ROUNDDOWN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ROUNDDOWN elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744532"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="5e5c3-103">ROUNDDOWN ER funkcija</span><span class="sxs-lookup"><span data-stu-id="5e5c3-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e5c3-104">`ROUNDDOWN` funkcija grąžina nurodytą skaičių kaip *realiojo skaičiaus* reikšmę, suapvalintą su trūkumu iki nurodyto skaičiaus po kablelio.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e5c3-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="5e5c3-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="5e5c3-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="5e5c3-106">Arguments</span></span>

<span data-ttu-id="5e5c3-107">`number`: *Realusis*</span><span class="sxs-lookup"><span data-stu-id="5e5c3-107">`number`: *Real*</span></span>

<span data-ttu-id="5e5c3-108">Skaitinė reikšmė, kurią reikia apvalinti su trūkumu.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="5e5c3-109">`decimals`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="5e5c3-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="5e5c3-110">Skaitinė reikšmė, nurodanti skaičių po kablelio.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="5e5c3-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="5e5c3-111">Return values</span></span>

<span data-ttu-id="5e5c3-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="5e5c3-112">*Real*</span></span>

<span data-ttu-id="5e5c3-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5e5c3-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="5e5c3-114">Usage notes</span></span>

<span data-ttu-id="5e5c3-115">Ši funkcija veikia kaip ir [ROUND](er-functions-mathematical-round.md), bet ji visada apvalina nurodytą skaičių į mažesnę pusę (link nulio).</span><span class="sxs-lookup"><span data-stu-id="5e5c3-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="5e5c3-116">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5e5c3-116">Example 1</span></span>

<span data-ttu-id="5e5c3-117">`ROUNDDOWN (1200.767, 2)` suapvalina su trūkumu iki dviejų skaičių po kablelio ir grąžina **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="5e5c3-118">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="5e5c3-118">Example 2</span></span>

<span data-ttu-id="5e5c3-119">`ROUNDDOWN (1700.767, -3)` suapvalina su trūkumu iki artimiausio 1000 kartotinio ir grąžina **1000**.</span><span class="sxs-lookup"><span data-stu-id="5e5c3-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e5c3-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5e5c3-120">Additional resources</span></span>

[<span data-ttu-id="5e5c3-121">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="5e5c3-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
