---
title: Planavimas, kai turimi kiekiai neigiami
description: Šioje temoje paaiškinama, kaip tvarkomas neigiamas turimas kiekis naudojant planavimo optimizavimo funkciją.
author: ChristianRytt
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ca12d13f7318f649cb1dbc0f7c3cf56502c9d3ea
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077489"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="1c871-103">Planavimas, kai turimi kiekiai neigiami</span><span class="sxs-lookup"><span data-stu-id="1c871-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c871-104">Jei sistemoje rodomas neigiamas bendrasis turimas kiekis, planavimo mechanizmas kiekį laiko 0 (nuliu), kad padėtų išvengti tiekimo pertekliaus.</span><span class="sxs-lookup"><span data-stu-id="1c871-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="1c871-105">Toliau nurodyta, kaip ši funkcija veikia.</span><span class="sxs-lookup"><span data-stu-id="1c871-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="1c871-106">Planavimo optimizavimo funkcija sujungia turimus kiekius taikydama mažiausią padengimo dimensijų lygį.</span><span class="sxs-lookup"><span data-stu-id="1c871-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="1c871-107">(Pavyzdžiui, jei *vieta* nėra padengimo dimensija, planavimo optimizavimo funkcija turimus kiekius sujungia *sandėlio* lygiu.)</span><span class="sxs-lookup"><span data-stu-id="1c871-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="1c871-108">Jei bendrasis turimas kiekis taikant mažiausią padengimo dimensijų lygį yra neigiamas, sistema daro prielaidą, kad turimas kiekis tikrai yra 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="1c871-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c871-109">Planavimo sistema gali būti tik tiek tiksli, kiek tikslūs įvesti duomenys.</span><span class="sxs-lookup"><span data-stu-id="1c871-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="1c871-110">Jei įvesti duomenys yra netikslūs, neigiamo turimo kiekio įrašai nurodys, kad „Microsoft Dynamics 365 Supply Chain Management“ atsargų informacija nesusinchronizuota su realiu pasauliu.</span><span class="sxs-lookup"><span data-stu-id="1c871-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="1c871-111">Todėl planavimo rezultatas bus klaidingas.</span><span class="sxs-lookup"><span data-stu-id="1c871-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="1c871-112">Norėdami gauti tikslų planavimo rezultatą, turite sumažinti įrašų, kuriuose rodomas neigiamas turimas kiekis, skaičių.</span><span class="sxs-lookup"><span data-stu-id="1c871-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="1c871-113">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1c871-113">Example 1</span></span>

<span data-ttu-id="1c871-114">13 sandėlis sukonfigūruotas taip, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="1c871-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="1c871-115">**Padengimo kodas:** min. / maks.</span><span class="sxs-lookup"><span data-stu-id="1c871-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="1c871-116">**Minimalus** 15 vienetų (vnt.)</span><span class="sxs-lookup"><span data-stu-id="1c871-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="1c871-117">**Maksimalus:** 25 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="1c871-118">Mažiausias padengimo dimensijų lygis yra *sandėlis*, o tolesni turimi kiekiai įrašomi *vietos* lygiu.</span><span class="sxs-lookup"><span data-stu-id="1c871-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="1c871-119">**1 objektas, 13 sandėlis, 1 vieta:** 20 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="1c871-120">**1 objektas, 13 sandėlis, 2 vieta:** &minus;8 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="1c871-121">Todėl bendrasis turimas 13 sandėlio kiekis yra 12 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="1c871-122">(= 20 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-122">(= 20 pcs.</span></span> <span data-ttu-id="1c871-123">&minus; 8 vnt.).</span><span class="sxs-lookup"><span data-stu-id="1c871-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="1c871-124">Šiuo atveju planavimo mechanizmas naudoja 12 vnt. bendrąjį turimą kiekį.</span><span class="sxs-lookup"><span data-stu-id="1c871-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="1c871-125">13 sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="1c871-125">for warehouse 13.</span></span>

<span data-ttu-id="1c871-126">Rezultatas yra suplanuotas 13 vnt. užsakymas</span><span class="sxs-lookup"><span data-stu-id="1c871-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="1c871-127">(= 25 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-127">(= 25 pcs.</span></span> <span data-ttu-id="1c871-128">&minus; 12 vnt.), kad 13 sandėlis būtų pripildytas nuo 12 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="1c871-129">iki 25 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="1c871-130">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="1c871-130">Example 2</span></span>

<span data-ttu-id="1c871-131">13 sandėlis sukonfigūruotas taip, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="1c871-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="1c871-132">**Padengimo kodas:** min. / maks.</span><span class="sxs-lookup"><span data-stu-id="1c871-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="1c871-133">**Minimalus:** 15 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="1c871-134">**Maksimalus:** 25 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="1c871-135">Mažiausias padengimo dimensijų lygis yra *sandėlis*, o tolesni turimi kiekiai įrašomi *vietos* lygiu.</span><span class="sxs-lookup"><span data-stu-id="1c871-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="1c871-136">**1 objektas, 13 sandėlis, 1 vieta:** 4 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="1c871-137">**1 objektas, 13 sandėlis, 2 vieta:** &minus;8 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="1c871-138">Todėl bendrasis turimas 13 sandėlio kiekis yra &minus;4 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="1c871-139">(= 4 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-139">(= 4 pcs.</span></span> <span data-ttu-id="1c871-140">&minus; 8 vnt.).</span><span class="sxs-lookup"><span data-stu-id="1c871-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="1c871-141">Kitaip tariant, mažiau nei 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="1c871-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="1c871-142">Šiuo atveju planavimo mechanizmas daro prielaidą, kad turimas 13 sandėlio kiekis yra 0 vnt.,</span><span class="sxs-lookup"><span data-stu-id="1c871-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="1c871-143">o ne &minus;4 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="1c871-144">Rezultatas yra suplanuotas 25 vnt. užsakymas</span><span class="sxs-lookup"><span data-stu-id="1c871-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="1c871-145">(= 25 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-145">(= 25 pcs.</span></span> <span data-ttu-id="1c871-146">&minus; 0 vnt.), kad 13 sandėlis būtų pripildytas nuo 0 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="1c871-147">iki 25 vnt.</span><span class="sxs-lookup"><span data-stu-id="1c871-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="1c871-148">Susiję ištekliai</span><span class="sxs-lookup"><span data-stu-id="1c871-148">Related resources</span></span>

[<span data-ttu-id="1c871-149">Planavimo optimizavimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="1c871-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="1c871-150">Darbo su planavimo optimizavimu pradžia</span><span class="sxs-lookup"><span data-stu-id="1c871-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="1c871-151">Planavimo optimizavimo tinkamumo analizė</span><span class="sxs-lookup"><span data-stu-id="1c871-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="1c871-152">Plano retrospektyvos ir planavimo žurnalų peržiūra</span><span class="sxs-lookup"><span data-stu-id="1c871-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="1c871-153">Planavimo užduoties atšaukimas</span><span class="sxs-lookup"><span data-stu-id="1c871-153">Cancel a planning job</span></span>](cancel-planning-job.md)