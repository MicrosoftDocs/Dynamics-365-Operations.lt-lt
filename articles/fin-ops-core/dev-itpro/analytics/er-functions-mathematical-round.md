---
title: ROUND ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ROUND elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570403"
---
# <a name="round-er-function"></a><span data-ttu-id="677b8-103">ROUND ER funkcija</span><span class="sxs-lookup"><span data-stu-id="677b8-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="677b8-104">`ROUND` funkcija grąžina nurodytą skaičių kaip *realiojo skaičiaus* reikšmę, suapvalintą iki nurodyto skaičiaus po kablelio.</span><span class="sxs-lookup"><span data-stu-id="677b8-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="677b8-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="677b8-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="677b8-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="677b8-106">Arguments</span></span>

<span data-ttu-id="677b8-107">`number`: *Realusis*</span><span class="sxs-lookup"><span data-stu-id="677b8-107">`number`: *Real*</span></span>

<span data-ttu-id="677b8-108">Skaitinė reikšmė, kurią reikia apvalinti.</span><span class="sxs-lookup"><span data-stu-id="677b8-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="677b8-109">`decimals`: *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="677b8-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="677b8-110">Skaitinė reikšmė, nurodanti skaičių po kablelio.</span><span class="sxs-lookup"><span data-stu-id="677b8-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="677b8-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="677b8-111">Return values</span></span>

<span data-ttu-id="677b8-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="677b8-112">*Real*</span></span>

<span data-ttu-id="677b8-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="677b8-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="677b8-114">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="677b8-114">Usage notes</span></span>

<span data-ttu-id="677b8-115">Jei argumento `decimals` reikšmė yra didesnė už 0 (nulį), nurodytas skaičius apvalinamas iki tiek skaitmenų po kablelio.</span><span class="sxs-lookup"><span data-stu-id="677b8-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="677b8-116">Jei argumento `decimals` reikšmė yra **0** (nulis), nurodytas skaičius apvalinamas iki artimiausio lyginio sveikojo skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="677b8-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="677b8-117">Jei argumento `decimals` reikšmė yra mažesnė už 0 (nulį), nurodytas skaičius apvalinamas į kairę nuo skaičiaus po kablelio.</span><span class="sxs-lookup"><span data-stu-id="677b8-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="677b8-118">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="677b8-118">Example 1</span></span>

<span data-ttu-id="677b8-119">`ROUND (1200.767, 2)` suapvalina iki dviejų skaičių po kablelio ir grąžina **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="677b8-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="677b8-120">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="677b8-120">Example 2</span></span>

<span data-ttu-id="677b8-121">`ROUND (1200.767, -3)` suapvalina iki artimiausio 1,000 kartotinio ir grąžina **1000**.</span><span class="sxs-lookup"><span data-stu-id="677b8-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="677b8-122">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="677b8-122">Example 3</span></span>

<span data-ttu-id="677b8-123">`ROUND (1200.5, 0)` suapvalina iki artimiausio lyginio sveikojo skaičiaus ir pateikia **1200**, o `ROUND (1201.5, 0)` atlieka tą patį ir pateikia **1202**.</span><span class="sxs-lookup"><span data-stu-id="677b8-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="677b8-124">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="677b8-124">Additional resources</span></span>

[<span data-ttu-id="677b8-125">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="677b8-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]