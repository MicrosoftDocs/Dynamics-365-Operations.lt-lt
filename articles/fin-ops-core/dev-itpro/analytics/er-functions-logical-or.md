---
title: OR ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama OR elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 7c2f110185330ee1e0cc6dc9ac534ae697e4b19b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565861"
---
# <a name="or-er-function"></a><span data-ttu-id="be5f6-103">OR ER funkcija</span><span class="sxs-lookup"><span data-stu-id="be5f6-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be5f6-104">`OR` funkcija grąžina *Bulio logikos* reikšmę **KLAIDINGA**, jei visos nurodytos sąlygos yra klaidingos.</span><span class="sxs-lookup"><span data-stu-id="be5f6-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="be5f6-105">Jei bet kuri nurodyta sąlyga yra teisinga, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="be5f6-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="be5f6-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="be5f6-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="be5f6-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="be5f6-107">Arguments</span></span>

<span data-ttu-id="be5f6-108">`condition 1`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="be5f6-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="be5f6-109">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="be5f6-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="be5f6-110">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="be5f6-110">This argument is required.</span></span>

<span data-ttu-id="be5f6-111">`condition N`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="be5f6-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="be5f6-112">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="be5f6-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="be5f6-113">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="be5f6-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="be5f6-114">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="be5f6-114">Return values</span></span>

<span data-ttu-id="be5f6-115">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="be5f6-115">*Boolean*</span></span>

<span data-ttu-id="be5f6-116">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="be5f6-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="be5f6-117">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="be5f6-117">Example</span></span>

<span data-ttu-id="be5f6-118">`OR (1=2, "a"="a")` grąžina **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="be5f6-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be5f6-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="be5f6-119">Additional resources</span></span>

[<span data-ttu-id="be5f6-120">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="be5f6-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]