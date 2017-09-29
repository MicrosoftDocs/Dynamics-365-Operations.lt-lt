---
title: "Atsargų objekto vertės"
description: "Šiame straipsnyje pateikiama informacija apie tai, kaip apskaičiuojamos atsargų objektą vertės."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4aec6e70325c7e4d00e6070293a1ab0c719e420b
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="inventory-object-values"></a><span data-ttu-id="bed88-103">Atsargų objekto vertės</span><span class="sxs-lookup"><span data-stu-id="bed88-103">Inventory object values</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bed88-104">Šiame straipsnyje pateikiama informacija apie tai, kaip apskaičiuojamos atsargų objektą vertės.</span><span class="sxs-lookup"><span data-stu-id="bed88-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="bed88-105">Nauja funkcija pavadinimu **faktinis kiekis** leidžia matyti konkretaus atsargų objekto vertes.</span><span class="sxs-lookup"><span data-stu-id="bed88-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="bed88-106">Išlaidų objektas atitinka objekto lygį, kuriame atliekama atsargų apskaita.</span><span class="sxs-lookup"><span data-stu-id="bed88-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="bed88-107">Daugiau informacijos apie išlaidų objektus rasite [Išlaidų objektai](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="bed88-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="bed88-108">Norėdami pamatyti konkretaus atsargų objekto vertes, puslapyje **Savikainos objektas** spustelėkite **Faktinis kiekis**.</span><span class="sxs-lookup"><span data-stu-id="bed88-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="bed88-109">Toliau nurodyta, kaip skaičiuojama atsargų objekto vertė.</span><span class="sxs-lookup"><span data-stu-id="bed88-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="bed88-110">Atsargų objektas.Vertė = Išlaidų objektas.Vidutinė vieneto savikaina × Atsargų objektas.Kiekis</span><span class="sxs-lookup"><span data-stu-id="bed88-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="bed88-111">Tolesniame pavyzdyje parodyta, kaip skaičiuojamos atsargų objekto ir išlaidų objekto vertės.</span><span class="sxs-lookup"><span data-stu-id="bed88-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="bed88-112">Registruoti du prekės A produkto gavimo įvykiai.</span><span class="sxs-lookup"><span data-stu-id="bed88-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="bed88-113">1 produkto gavimo kvitas: Kiekis = 100 vnt., Suma = 1 000,00 dol., Teritorija = 1, Sandėlis =11, Paketo Nr.</span><span class="sxs-lookup"><span data-stu-id="bed88-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="bed88-114">= B1</span><span class="sxs-lookup"><span data-stu-id="bed88-114">= B1</span></span>
-   <span data-ttu-id="bed88-115">2 produkto gavimo kvitas: Kiekis = 50 vnt., Suma = 800,00 dol., Teritorija = 1, Sandėlis =11, Paketo Nr.</span><span class="sxs-lookup"><span data-stu-id="bed88-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="bed88-116">= B2</span><span class="sxs-lookup"><span data-stu-id="bed88-116">= B2</span></span>

<span data-ttu-id="bed88-117">Toliau pateikiamoje lentelėje rodomas išlaidų objekto skaičiavimo rezultatas.</span><span class="sxs-lookup"><span data-stu-id="bed88-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="bed88-118">Rezultatą galite peržiūrėti **Išlaidų objekto** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="bed88-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bed88-119">Objekto tipas</span><span class="sxs-lookup"><span data-stu-id="bed88-119">Object type</span></span></th>
<th><span data-ttu-id="bed88-120">Prekės numeris</span><span class="sxs-lookup"><span data-stu-id="bed88-120">Item number</span></span></th>
<th><span data-ttu-id="bed88-121">Svetainė</span><span class="sxs-lookup"><span data-stu-id="bed88-121">Site</span></span></th>
<th><span data-ttu-id="bed88-122">Kiekis</span><span class="sxs-lookup"><span data-stu-id="bed88-122">Quantity</span></span></th>
<th><span data-ttu-id="bed88-123">Atsargų vienetas</span><span class="sxs-lookup"><span data-stu-id="bed88-123">Inventory unit</span></span></th>
<th><span data-ttu-id="bed88-124">Vertė</span><span class="sxs-lookup"><span data-stu-id="bed88-124">Value</span></span></th>
<th><span data-ttu-id="bed88-125">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="bed88-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bed88-126">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="bed88-126">Cost object</span></span></td>
<td><span data-ttu-id="bed88-127">A</span><span class="sxs-lookup"><span data-stu-id="bed88-127">A</span></span></td>
<td><span data-ttu-id="bed88-128">1</span><span class="sxs-lookup"><span data-stu-id="bed88-128">1</span></span></td>
<td><span data-ttu-id="bed88-129">150</span><span class="sxs-lookup"><span data-stu-id="bed88-129">150</span></span></td>
<td><span data-ttu-id="bed88-130">Vnt.</span><span class="sxs-lookup"><span data-stu-id="bed88-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="bed88-131">1 800,00 $</span><span class="sxs-lookup"><span data-stu-id="bed88-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="bed88-132">12,00 $</span><span class="sxs-lookup"><span data-stu-id="bed88-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bed88-133">Toliau pateikiamoje lentelėje rodomas atsargų objekto skaičiavimo rezultatas.</span><span class="sxs-lookup"><span data-stu-id="bed88-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="bed88-134">Rezultatą galite peržiūrėti **Išlaidų objekto** puslapyje spustelėję **Fizinis kiekis**.</span><span class="sxs-lookup"><span data-stu-id="bed88-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bed88-135">Objekto tipas</span><span class="sxs-lookup"><span data-stu-id="bed88-135">Object type</span></span></th>
<th><span data-ttu-id="bed88-136">Prekės numeris</span><span class="sxs-lookup"><span data-stu-id="bed88-136">Item number</span></span></th>
<th><span data-ttu-id="bed88-137">Svetainė</span><span class="sxs-lookup"><span data-stu-id="bed88-137">Site</span></span></th>
<th><span data-ttu-id="bed88-138">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="bed88-138">Warehouse</span></span></th>
<th><span data-ttu-id="bed88-139">Paketo nr.</span><span class="sxs-lookup"><span data-stu-id="bed88-139">Batch No.</span></span></th>
<th><span data-ttu-id="bed88-140">Kiekis</span><span class="sxs-lookup"><span data-stu-id="bed88-140">Quantity</span></span></th>
<th><span data-ttu-id="bed88-141">Atsargų vienetas</span><span class="sxs-lookup"><span data-stu-id="bed88-141">Inventory unit</span></span></th>
<th><span data-ttu-id="bed88-142">Vertė</span><span class="sxs-lookup"><span data-stu-id="bed88-142">Value</span></span></th>
<th><span data-ttu-id="bed88-143">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="bed88-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bed88-144">Atsargų objektas</span><span class="sxs-lookup"><span data-stu-id="bed88-144">Inventory object</span></span></td>
<td><span data-ttu-id="bed88-145">A</span><span class="sxs-lookup"><span data-stu-id="bed88-145">A</span></span></td>
<td><span data-ttu-id="bed88-146">1</span><span class="sxs-lookup"><span data-stu-id="bed88-146">1</span></span></td>
<td><span data-ttu-id="bed88-147">11</span><span class="sxs-lookup"><span data-stu-id="bed88-147">11</span></span></td>
<td><span data-ttu-id="bed88-148">B1</span><span class="sxs-lookup"><span data-stu-id="bed88-148">B1</span></span></td>
<td><span data-ttu-id="bed88-149">100</span><span class="sxs-lookup"><span data-stu-id="bed88-149">100</span></span></td>
<td><span data-ttu-id="bed88-150">Vnt.</span><span class="sxs-lookup"><span data-stu-id="bed88-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="bed88-151">1 200,00 $</span><span class="sxs-lookup"><span data-stu-id="bed88-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="bed88-152">12,00 $</span><span class="sxs-lookup"><span data-stu-id="bed88-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bed88-153">Atsargų objektas</span><span class="sxs-lookup"><span data-stu-id="bed88-153">Inventory object</span></span></td>
<td><span data-ttu-id="bed88-154">A</span><span class="sxs-lookup"><span data-stu-id="bed88-154">A</span></span></td>
<td><span data-ttu-id="bed88-155">1</span><span class="sxs-lookup"><span data-stu-id="bed88-155">1</span></span></td>
<td><span data-ttu-id="bed88-156">11</span><span class="sxs-lookup"><span data-stu-id="bed88-156">11</span></span></td>
<td><span data-ttu-id="bed88-157">B2</span><span class="sxs-lookup"><span data-stu-id="bed88-157">B2</span></span></td>
<td><span data-ttu-id="bed88-158">50</span><span class="sxs-lookup"><span data-stu-id="bed88-158">50</span></span></td>
<td><span data-ttu-id="bed88-159">Vnt.</span><span class="sxs-lookup"><span data-stu-id="bed88-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="bed88-160">600,00 $</span><span class="sxs-lookup"><span data-stu-id="bed88-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="bed88-161">12,00 $</span><span class="sxs-lookup"><span data-stu-id="bed88-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="bed88-162">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="bed88-162">See also</span></span>
--------

[<span data-ttu-id="bed88-163">Savikainos objektai</span><span class="sxs-lookup"><span data-stu-id="bed88-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="bed88-164">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="bed88-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="bed88-165">Kas nauja ir pasikeitė</span><span class="sxs-lookup"><span data-stu-id="bed88-165">What's new and changed</span></span>](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)




