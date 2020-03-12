---
title: POWER ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama POWER elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: c57222d7fcc133faa679bab43431272c984c9d8b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041635"
---
# <span data-ttu-id="6ecd4-103"><a name="POWER">POWER ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="6ecd4-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ecd4-104">`POWER` funkcija grąžina *realiojo skaičiaus* reikšmę, atsižvelgiant į rezultatą pakeliant laipsniu nurodytą teigiamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="6ecd4-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ecd4-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="6ecd4-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="6ecd4-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="6ecd4-106">Arguments</span></span>

<span data-ttu-id="6ecd4-107">`number`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="6ecd4-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="6ecd4-108">Skaitinė reikšmė, kurią reikia pakelti nurodytu laipsniu.</span><span class="sxs-lookup"><span data-stu-id="6ecd4-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="6ecd4-109">`power`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="6ecd4-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="6ecd4-110">Skaitinė reikšmė, nurodanti konkretų laipsnį.</span><span class="sxs-lookup"><span data-stu-id="6ecd4-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ecd4-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="6ecd4-111">Return values</span></span>

<span data-ttu-id="6ecd4-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="6ecd4-112">*Real*</span></span>

<span data-ttu-id="6ecd4-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="6ecd4-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="6ecd4-114">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ecd4-114">Example 1</span></span>

<span data-ttu-id="6ecd4-115">`POWER (10, 2)` grąžina **100**.</span><span class="sxs-lookup"><span data-stu-id="6ecd4-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6ecd4-116">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ecd4-116">Example 2</span></span>

<span data-ttu-id="6ecd4-117">`POWER (4, 0.5)` grąžina **2**.</span><span class="sxs-lookup"><span data-stu-id="6ecd4-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ecd4-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6ecd4-118">Additional resources</span></span>

[<span data-ttu-id="6ecd4-119">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="6ecd4-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
