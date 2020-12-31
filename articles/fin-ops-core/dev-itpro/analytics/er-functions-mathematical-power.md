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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 858f59cf0bc6387b09cbb6f0c59f58ba8107582c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683334"
---
# <a name="power-er-function"></a><span data-ttu-id="c8b4c-103">POWER ER funkcija</span><span class="sxs-lookup"><span data-stu-id="c8b4c-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8b4c-104">`POWER` funkcija grąžina *realiojo skaičiaus* reikšmę, atsižvelgiant į rezultatą pakeliant laipsniu nurodytą teigiamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b4c-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="c8b4c-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="c8b4c-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="c8b4c-106">Arguments</span></span>

<span data-ttu-id="c8b4c-107">`number`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="c8b4c-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="c8b4c-108">Skaitinė reikšmė, kurią reikia pakelti nurodytu laipsniu.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="c8b4c-109">`power`: *Realusis* arba *Sveikasis*</span><span class="sxs-lookup"><span data-stu-id="c8b4c-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="c8b4c-110">Skaitinė reikšmė, nurodanti konkretų laipsnį.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="c8b4c-111">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="c8b4c-111">Return values</span></span>

<span data-ttu-id="c8b4c-112">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="c8b4c-112">*Real*</span></span>

<span data-ttu-id="c8b4c-113">Gaunama skaitinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="c8b4c-114">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c8b4c-114">Example 1</span></span>

<span data-ttu-id="c8b4c-115">`POWER (10, 2)` grąžina **100**.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c8b4c-116">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c8b4c-116">Example 2</span></span>

<span data-ttu-id="c8b4c-117">`POWER (4, 0.5)` grąžina **2**.</span><span class="sxs-lookup"><span data-stu-id="c8b4c-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8b4c-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c8b4c-118">Additional resources</span></span>

[<span data-ttu-id="c8b4c-119">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="c8b4c-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
