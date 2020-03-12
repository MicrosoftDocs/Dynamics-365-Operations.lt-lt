---
title: AND ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama AND elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 1836d25ad07ad1ce735fda5e008a3315626b62bb
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041820"
---
# <span data-ttu-id="64017-103"><a name="AND">AND ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="64017-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64017-104">`AND` funkcija pateikia *Bulio logikos* reikšmę **TEISINGA**, jei visos nurodytos sąlygos yra teisingos.</span><span class="sxs-lookup"><span data-stu-id="64017-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="64017-105">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="64017-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="64017-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="64017-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="64017-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="64017-107">Arguments</span></span>

<span data-ttu-id="64017-108">`condition 1`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="64017-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="64017-109">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="64017-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="64017-110">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="64017-110">This argument is required.</span></span>

<span data-ttu-id="64017-111">`condition N`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="64017-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="64017-112">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="64017-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="64017-113">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="64017-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="64017-114">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="64017-114">Return values</span></span>

<span data-ttu-id="64017-115">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="64017-115">*Boolean*</span></span>

<span data-ttu-id="64017-116">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="64017-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="64017-117">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="64017-117">Usage notes</span></span>

<span data-ttu-id="64017-118">Loginių funkcijų argumentuose galite naudoti duomenų šaltinio nuorodas, skaitines ir tekstines reikšmes, Bulio logikos reikšmes, palyginimo operatorius ir kitas elektroninių ataskaitų (ER) funkcijas.</span><span class="sxs-lookup"><span data-stu-id="64017-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="64017-119">Tačiau visi argumentai turi būti vertinami pagal *Bulio logikos* reikšmę **TEISINGA** arba **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="64017-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="64017-120">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="64017-120">Example</span></span>

<span data-ttu-id="64017-121">`AND (1=1, "a"="a")` grąžina **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="64017-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="64017-122">`AND (1=2, "a"="a")` grąžina **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="64017-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64017-123">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="64017-123">Additional resources</span></span>

[<span data-ttu-id="64017-124">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="64017-124">Logical functions</span></span>](er-functions-category-logical.md)
