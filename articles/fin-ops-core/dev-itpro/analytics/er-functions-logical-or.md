---
title: OR ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama OR elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686983"
---
# <a name="or-er-function"></a><span data-ttu-id="c43e7-103">OR ER funkcija</span><span class="sxs-lookup"><span data-stu-id="c43e7-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c43e7-104">`OR` funkcija grąžina *Bulio logikos* reikšmę **KLAIDINGA**, jei visos nurodytos sąlygos yra klaidingos.</span><span class="sxs-lookup"><span data-stu-id="c43e7-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="c43e7-105">Jei bet kuri nurodyta sąlyga yra teisinga, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="c43e7-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43e7-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="c43e7-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="c43e7-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="c43e7-107">Arguments</span></span>

<span data-ttu-id="c43e7-108">`condition 1`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="c43e7-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="c43e7-109">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="c43e7-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="c43e7-110">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="c43e7-110">This argument is required.</span></span>

<span data-ttu-id="c43e7-111">`condition N`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="c43e7-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="c43e7-112">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="c43e7-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="c43e7-113">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="c43e7-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="c43e7-114">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="c43e7-114">Return values</span></span>

<span data-ttu-id="c43e7-115">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="c43e7-115">*Boolean*</span></span>

<span data-ttu-id="c43e7-116">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c43e7-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="c43e7-117">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c43e7-117">Example</span></span>

<span data-ttu-id="c43e7-118">`OR (1=2, "a"="a")` grąžina **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="c43e7-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c43e7-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c43e7-119">Additional resources</span></span>

[<span data-ttu-id="c43e7-120">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="c43e7-120">Logical functions</span></span>](er-functions-category-logical.md)
