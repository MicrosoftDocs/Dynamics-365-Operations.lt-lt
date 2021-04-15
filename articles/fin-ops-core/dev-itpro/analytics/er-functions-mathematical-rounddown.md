---
title: ROUNDDOWN ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ROUNDDOWN elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 89fc134ec11a47506211ce68ec3aaf966d9a308b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744468"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="17fa2-103">ROUNDDOWN ER funkcija</span><span class="sxs-lookup"><span data-stu-id="17fa2-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17fa2-104">`ROUNDDOWN` funkcija grąžina nurodytą skaičių kaip *realiojo skaičiaus* reikšmę, suapvalintą su trūkumu iki nurodyto skaičiaus po kablelio.</span><span class="sxs-lookup"><span data-stu-id="17fa2-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fa2-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="17fa2-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="17fa2-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="17fa2-106">Arguments</span></span>

<span data-ttu-id="17fa2-107">`number`: *Realusis*</span><span class="sxs-lookup"><span data-stu-id="17fa2-107">`number`: *Real*</span></span>

<span data-ttu-id="17fa2-108">Skaitinė reikšmė, kurią reikia apvalinti su trūkumu.</span><span class="sxs-lookup"><span data-stu-id="17fa2-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="17fa2-109">`decimals`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="17fa2-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="17fa2-110">Skaitinė reikšmė, nurodanti skaičių po kablelio.</span><span class="sxs-lookup"><span data-stu-id="17fa2-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="17fa2-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="17fa2-111">Return values</span></span>

<span data-ttu-id="17fa2-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="17fa2-112">*Real*</span></span>

<span data-ttu-id="17fa2-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="17fa2-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17fa2-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="17fa2-114">Usage notes</span></span>

<span data-ttu-id="17fa2-115">Ši funkcija veikia kaip ir [ROUND](er-functions-mathematical-round.md), bet ji visada apvalina nurodytą skaičių į mažesnę pusę (link nulio).</span><span class="sxs-lookup"><span data-stu-id="17fa2-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="17fa2-116">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="17fa2-116">Example 1</span></span>

<span data-ttu-id="17fa2-117">`ROUNDDOWN (1200.767, 2)` suapvalina su trūkumu iki dviejų skaičių po kablelio ir grąžina **1200,76**.</span><span class="sxs-lookup"><span data-stu-id="17fa2-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="17fa2-118">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="17fa2-118">Example 2</span></span>

<span data-ttu-id="17fa2-119">`ROUNDDOWN (1700.767, -3)` suapvalina su trūkumu iki artimiausio 1000 kartotinio ir grąžina **1000**.</span><span class="sxs-lookup"><span data-stu-id="17fa2-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17fa2-120">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="17fa2-120">Additional resources</span></span>

[<span data-ttu-id="17fa2-121">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="17fa2-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]