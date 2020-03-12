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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a850b1cbe7224ab1a7b2bd39ac4667304781cbb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041681"
---
# <span data-ttu-id="74eea-103"><a name="OR">OR ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="74eea-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74eea-104">`OR` funkcija grąžina *Bulio logikos* reikšmę **KLAIDINGA**, jei visos nurodytos sąlygos yra klaidingos.</span><span class="sxs-lookup"><span data-stu-id="74eea-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="74eea-105">Jei bet kuri nurodyta sąlyga yra teisinga, ši funkcija pateikia *Bulio logikos* reikšmę **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="74eea-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="74eea-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="74eea-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="74eea-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="74eea-107">Arguments</span></span>

<span data-ttu-id="74eea-108">`condition 1`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="74eea-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="74eea-109">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="74eea-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="74eea-110">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="74eea-110">This argument is required.</span></span>

<span data-ttu-id="74eea-111">`condition N`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="74eea-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="74eea-112">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="74eea-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="74eea-113">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="74eea-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="74eea-114">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="74eea-114">Return values</span></span>

<span data-ttu-id="74eea-115">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="74eea-115">*Boolean*</span></span>

<span data-ttu-id="74eea-116">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="74eea-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="74eea-117">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="74eea-117">Example</span></span>

<span data-ttu-id="74eea-118">`OR (1=2, "a"="a")` grąžina **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="74eea-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74eea-119">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="74eea-119">Additional resources</span></span>

[<span data-ttu-id="74eea-120">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="74eea-120">Logical functions</span></span>](er-functions-category-logical.md)
