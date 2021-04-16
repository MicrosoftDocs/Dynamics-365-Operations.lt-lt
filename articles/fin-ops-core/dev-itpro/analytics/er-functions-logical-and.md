---
title: AND ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama AND elektroninių ataskaitų (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9851321137b4c7744634df30f85aa3a0b1a0a588
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745478"
---
# <a name="and-er-function"></a><span data-ttu-id="8cf97-103">AND ER funkcija</span><span class="sxs-lookup"><span data-stu-id="8cf97-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8cf97-104">`AND` funkcija pateikia *Bulio logikos* reikšmę **TEISINGA**, jei visos nurodytos sąlygos yra teisingos.</span><span class="sxs-lookup"><span data-stu-id="8cf97-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="8cf97-105">Kitu atveju išraiška grąžina *Bulio logikos* reikšmę **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8cf97-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf97-106">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="8cf97-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="8cf97-107">Argumentai</span><span class="sxs-lookup"><span data-stu-id="8cf97-107">Arguments</span></span>

<span data-ttu-id="8cf97-108">`condition 1`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="8cf97-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="8cf97-109">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="8cf97-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="8cf97-110">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="8cf97-110">This argument is required.</span></span>

<span data-ttu-id="8cf97-111">`condition N`: *Bulio logika*</span><span class="sxs-lookup"><span data-stu-id="8cf97-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="8cf97-112">Tinkama sąlyginė išraiška, kuri turi būti patikrinta.</span><span class="sxs-lookup"><span data-stu-id="8cf97-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="8cf97-113">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="8cf97-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8cf97-114">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="8cf97-114">Return values</span></span>

<span data-ttu-id="8cf97-115">*Būlio logika*</span><span class="sxs-lookup"><span data-stu-id="8cf97-115">*Boolean*</span></span>

<span data-ttu-id="8cf97-116">Gaunama *Bulio logikos* reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8cf97-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8cf97-117">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="8cf97-117">Usage notes</span></span>

<span data-ttu-id="8cf97-118">Loginių funkcijų argumentuose galite naudoti duomenų šaltinio nuorodas, skaitines ir tekstines reikšmes, Bulio logikos reikšmes, palyginimo operatorius ir kitas elektroninių ataskaitų (ER) funkcijas.</span><span class="sxs-lookup"><span data-stu-id="8cf97-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="8cf97-119">Tačiau visi argumentai turi būti vertinami pagal *Bulio logikos* reikšmę **TEISINGA** arba **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="8cf97-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="8cf97-120">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="8cf97-120">Example</span></span>

<span data-ttu-id="8cf97-121">`AND (1=1, "a"="a")` grąžina **TEISINGA**.</span><span class="sxs-lookup"><span data-stu-id="8cf97-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="8cf97-122">`AND (1=2, "a"="a")` grąžina **KLAIDINGA**.</span><span class="sxs-lookup"><span data-stu-id="8cf97-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8cf97-123">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="8cf97-123">Additional resources</span></span>

[<span data-ttu-id="8cf97-124">Loginės funkcijos</span><span class="sxs-lookup"><span data-stu-id="8cf97-124">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]