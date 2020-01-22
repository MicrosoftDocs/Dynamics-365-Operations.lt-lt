---
title: ROUNDAMOUNT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama ROUNDAMOUNT elektroninių ataskaitų (ER) funkcija.
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
ms.openlocfilehash: c68933352da1f9c7dc5dad76e8635981f8a89fce
ms.sourcegitcommit: 9291e6dc0de076a16684980e528c5aa98845bb34
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2918984"
---
# <span data-ttu-id="0efdc-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="0efdc-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0efdc-104">`ROUNDAMOUNT` funkcija grąžina *realiojo skaičiaus* reikšmę kaip nurodyto skaičiaus apvalinimo rezultatą iki artimiausio kito skaičiaus kartotinio pagal nurodytą apvalinimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="0efdc-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="0efdc-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="0efdc-105">Syntax</span></span>

```
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="0efdc-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="0efdc-106">Arguments</span></span>

<span data-ttu-id="0efdc-107">`number`: *Sveik.* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="0efdc-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="0efdc-108">Skaitinė reikšmė, kurią reikia apvalinti.</span><span class="sxs-lookup"><span data-stu-id="0efdc-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="0efdc-109">`decimals`: *Sveik.* arba *Realusis*</span><span class="sxs-lookup"><span data-stu-id="0efdc-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="0efdc-110">Skaičius, kurio parametro `number` reikšmė turi būti suapvalinta iki kartotinio.</span><span class="sxs-lookup"><span data-stu-id="0efdc-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="0efdc-111">`round rule`: *Išvard. reikšmė*</span><span class="sxs-lookup"><span data-stu-id="0efdc-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="0efdc-112">Išvardijimo reikšmės **RoundOffType** išvardijimas, apibrėžiantis apvalinimo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="0efdc-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="0efdc-113">Šis išvardijimas siūlo šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="0efdc-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="0efdc-114">Normalusis (paprastasis)</span><span class="sxs-lookup"><span data-stu-id="0efdc-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="0efdc-115">Su trūkumu (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="0efdc-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="0efdc-116">Su pertekliumi (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="0efdc-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="0efdc-117">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="0efdc-117">Return values</span></span>

<span data-ttu-id="0efdc-118">*Tikrasis*</span><span class="sxs-lookup"><span data-stu-id="0efdc-118">*Real*</span></span>

<span data-ttu-id="0efdc-119">Gauta skaitinė reikšmė yra parametro `decimals` nurodytos reikšmės kartotinis ir yra arčiausiai parametro `number` nurodytos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="0efdc-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0efdc-120">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="0efdc-120">Usage notes</span></span>

<span data-ttu-id="0efdc-121">Kai parametras `number` yra nulis, ši funkcija visada grąžina nulį.</span><span class="sxs-lookup"><span data-stu-id="0efdc-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="0efdc-122">Kai parametras `decimals` yra nulis, ši funkcija suapvalinama iki numatytosios apvalinimo reikšmės.</span><span class="sxs-lookup"><span data-stu-id="0efdc-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="0efdc-123">Kai parametras `round rule`nustatytas kaip **RoundOffType.Ordinary**, numatytoji apvalinimo reikšmė yra **0,01**.</span><span class="sxs-lookup"><span data-stu-id="0efdc-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="0efdc-124">Priešingu atveju numatytoji apvalinimo reikšmė yra **1,0**.</span><span class="sxs-lookup"><span data-stu-id="0efdc-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="0efdc-125">Kai parametras `round rule` nustatytas kaip **RoundOffType.Ordinary**, ši funkcija suapvalinama iki artimiausios apvalinimo sumos.</span><span class="sxs-lookup"><span data-stu-id="0efdc-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="0efdc-126">Kai parametras `round rule` nustatytas kaip **RoundOffType.RoundDown**, ši funkcija suapvalinama iki artimiausios apvalinimo sumos, lygios nuliui.</span><span class="sxs-lookup"><span data-stu-id="0efdc-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="0efdc-127">Kai parametras `round rule` nustatytas kaip **RoundOffType.RoundUp**, ši funkcija suapvalinama iki artimiausios apvalinimo sumos, kad nebūtų lygi nuliui.</span><span class="sxs-lookup"><span data-stu-id="0efdc-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="0efdc-128">Kai parametras `round rule`nustatytas kaip **RoundOffType.Ordinary**, ši funkcija veikia kaip X ++ funkcija [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel funkcija ir [Round](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round).</span><span class="sxs-lookup"><span data-stu-id="0efdc-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="0efdc-129">Pastabos</span><span class="sxs-lookup"><span data-stu-id="0efdc-129">Remarks</span></span>

<span data-ttu-id="0efdc-130">Norėdami apvalinti skaitinę reikšmę iki nurodyto skaičiaus po kablelio, naudokite funkciją [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="0efdc-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="0efdc-131">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="0efdc-131">Example</span></span>

<span data-ttu-id="0efdc-132">Jei parametras **model.RoundOff** nustatytas kaip **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)`grąžina 7,35.</span><span class="sxs-lookup"><span data-stu-id="0efdc-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="0efdc-133">Jei parametras **model.RoundOff** nustatytas kaip **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)`grąžina 7,35.</span><span class="sxs-lookup"><span data-stu-id="0efdc-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="0efdc-134">Jei parametras **model.RoundOff** nustatytas kaip **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)`grąžina 8,4.</span><span class="sxs-lookup"><span data-stu-id="0efdc-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0efdc-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0efdc-135">Additional resources</span></span>

[<span data-ttu-id="0efdc-136">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="0efdc-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="0efdc-137">Matematinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="0efdc-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
