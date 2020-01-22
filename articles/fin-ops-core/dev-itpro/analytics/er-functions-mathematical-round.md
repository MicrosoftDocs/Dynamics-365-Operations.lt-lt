---
title: ROUND ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ROUND elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917079"
---
# <span data-ttu-id="89fda-103"><a name="ROUND">ROUND ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="89fda-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89fda-104">`ROUND` funkcija grąžina nurodytą skaičių kaip *realiojo skaičiaus* reikšmę, suapvalintą iki nurodyto skaičiaus po kablelio.</span><span class="sxs-lookup"><span data-stu-id="89fda-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fda-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="89fda-105">Syntax</span></span>

```
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="89fda-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="89fda-106">Arguments</span></span>

<span data-ttu-id="89fda-107">`number`: *Realusis*</span><span class="sxs-lookup"><span data-stu-id="89fda-107">`number`: *Real*</span></span>

<span data-ttu-id="89fda-108">Skaitinė reikšmė, kurią reikia apvalinti.</span><span class="sxs-lookup"><span data-stu-id="89fda-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="89fda-109">`decimals`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="89fda-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="89fda-110">Skaitinė reikšmė, nurodanti skaičių po kablelio.</span><span class="sxs-lookup"><span data-stu-id="89fda-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="89fda-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="89fda-111">Return values</span></span>

<span data-ttu-id="89fda-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="89fda-112">*Real*</span></span>

<span data-ttu-id="89fda-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="89fda-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="89fda-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="89fda-114">Usage notes</span></span>

<span data-ttu-id="89fda-115">Jei argumento `decimals` reikšmė yra didesnė už 0 (nulį), nurodytas skaičius apvalinamas iki tiek skaitmenų po kablelio.</span><span class="sxs-lookup"><span data-stu-id="89fda-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="89fda-116">Jei argumento `decimals` reikšmė yra **0** (nulis), nurodytas skaičius apvalinamas iki artimiausio sveikojo skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="89fda-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="89fda-117">Jei argumento `decimals` reikšmė yra mažesnė už 0 (nulį), nurodytas skaičius apvalinamas į kairę nuo skaičiaus po kablelio.</span><span class="sxs-lookup"><span data-stu-id="89fda-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="89fda-118">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="89fda-118">Example 1</span></span>

<span data-ttu-id="89fda-119">`ROUND (1200.767, 2)` suapvalina iki dviejų skaičių po kablelio ir grąžina **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="89fda-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="89fda-120">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="89fda-120">Example 2</span></span>

<span data-ttu-id="89fda-121">`ROUND (1200.767, -3)` suapvalina iki artimiausio 1,000 kartotinio ir grąžina **1000**.</span><span class="sxs-lookup"><span data-stu-id="89fda-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89fda-122">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="89fda-122">Additional resources</span></span>

[<span data-ttu-id="89fda-123">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="89fda-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
