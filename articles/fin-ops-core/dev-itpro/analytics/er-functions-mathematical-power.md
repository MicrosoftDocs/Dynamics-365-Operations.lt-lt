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
ms.openlocfilehash: cb768b400e3ddb99e7c8b05905d7a2dd9e4392de
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915906"
---
# <span data-ttu-id="95101-103"><a name="POWER">POWER ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="95101-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95101-104">`POWER` funkcija grąžina *realiojo skaičiaus* reikšmę, atsižvelgiant į rezultatą pakeliant laipsniu nurodytą teigiamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="95101-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="95101-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="95101-105">Syntax</span></span>

```
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="95101-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="95101-106">Arguments</span></span>

<span data-ttu-id="95101-107">`number`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="95101-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="95101-108">Skaitinė reikšmė, kurią reikia pakelti nurodytu laipsniu.</span><span class="sxs-lookup"><span data-stu-id="95101-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="95101-109">`power`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="95101-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="95101-110">Skaitinė reikšmė, nurodanti konkretų laipsnį.</span><span class="sxs-lookup"><span data-stu-id="95101-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="95101-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="95101-111">Return values</span></span>

<span data-ttu-id="95101-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="95101-112">*Real*</span></span>

<span data-ttu-id="95101-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="95101-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="95101-114">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="95101-114">Example 1</span></span>

<span data-ttu-id="95101-115">`POWER (10, 2)` grąžina **100**.</span><span class="sxs-lookup"><span data-stu-id="95101-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="95101-116">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="95101-116">Example 2</span></span>

<span data-ttu-id="95101-117">`POWER (4, 0.5)` grąžina **2**.</span><span class="sxs-lookup"><span data-stu-id="95101-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95101-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="95101-118">Additional resources</span></span>

[<span data-ttu-id="95101-119">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="95101-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
