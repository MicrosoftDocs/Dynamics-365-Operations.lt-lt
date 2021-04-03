---
title: Atsargų objekto vertės
description: Šiame straipsnyje pateikiama informacija apie tai, kaip apskaičiuojamos atsargų objektą vertės.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f14248ffa8f9f5a460b090ca5754442cd50bf45a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263547"
---
# <a name="inventory-object-values"></a><span data-ttu-id="b6f7e-103">Atsargų objekto vertės</span><span class="sxs-lookup"><span data-stu-id="b6f7e-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6f7e-104">Šiame straipsnyje pateikiama informacija apie tai, kaip apskaičiuojamos atsargų objektą vertės.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="b6f7e-105">Nauja funkcija pavadinimu **faktinis kiekis** leidžia matyti konkretaus atsargų objekto vertes.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="b6f7e-106">Išlaidų objektas atitinka objekto lygį, kuriame atliekama atsargų apskaita.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="b6f7e-107">Daugiau informacijos apie išlaidų objektus rasite [Išlaidų objektai](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="b6f7e-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="b6f7e-108">Norėdami pamatyti konkretaus atsargų objekto vertes, puslapyje **Savikainos objektas** spustelėkite **Faktinis kiekis**.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="b6f7e-109">Toliau nurodyta, kaip skaičiuojama atsargų objekto vertė.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="b6f7e-110">Atsargų objektas.Vertė = Išlaidų objektas.Vidutinė vieneto savikaina × Atsargų objektas.Kiekis</span><span class="sxs-lookup"><span data-stu-id="b6f7e-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="b6f7e-111">Tolesniame pavyzdyje parodyta, kaip skaičiuojamos atsargų objekto ir išlaidų objekto vertės.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="b6f7e-112">Registruoti du prekės A produkto gavimo įvykiai.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="b6f7e-113">1 produkto gavimo kvitas: Kiekis = 100 vnt., Suma = 1 000,00 dol., Teritorija = 1, Sandėlis =11, Paketo Nr.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="b6f7e-114">= B1</span><span class="sxs-lookup"><span data-stu-id="b6f7e-114">= B1</span></span>
-   <span data-ttu-id="b6f7e-115">2 produkto gavimo kvitas: Kiekis = 50 vnt., Suma = 800,00 dol., Teritorija = 1, Sandėlis =11, Paketo Nr.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="b6f7e-116">= B2</span><span class="sxs-lookup"><span data-stu-id="b6f7e-116">= B2</span></span>

<span data-ttu-id="b6f7e-117">Toliau pateikiamoje lentelėje rodomas išlaidų objekto skaičiavimo rezultatas.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="b6f7e-118">Rezultatą galite peržiūrėti **Išlaidų objekto** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="b6f7e-119">Objekto tipas</span><span class="sxs-lookup"><span data-stu-id="b6f7e-119">Object type</span></span></th>
<th><span data-ttu-id="b6f7e-120">Prekės numeris</span><span class="sxs-lookup"><span data-stu-id="b6f7e-120">Item number</span></span></th>
<th><span data-ttu-id="b6f7e-121">Svetainė</span><span class="sxs-lookup"><span data-stu-id="b6f7e-121">Site</span></span></th>
<th><span data-ttu-id="b6f7e-122">Kiekis</span><span class="sxs-lookup"><span data-stu-id="b6f7e-122">Quantity</span></span></th>
<th><span data-ttu-id="b6f7e-123">Atsargų vienetas</span><span class="sxs-lookup"><span data-stu-id="b6f7e-123">Inventory unit</span></span></th>
<th><span data-ttu-id="b6f7e-124">Vertė</span><span class="sxs-lookup"><span data-stu-id="b6f7e-124">Value</span></span></th>
<th><span data-ttu-id="b6f7e-125">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="b6f7e-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6f7e-126">Išlaidų objektas</span><span class="sxs-lookup"><span data-stu-id="b6f7e-126">Cost object</span></span></td>
<td><span data-ttu-id="b6f7e-127">A</span><span class="sxs-lookup"><span data-stu-id="b6f7e-127">A</span></span></td>
<td><span data-ttu-id="b6f7e-128">1</span><span class="sxs-lookup"><span data-stu-id="b6f7e-128">1</span></span></td>
<td><span data-ttu-id="b6f7e-129">150</span><span class="sxs-lookup"><span data-stu-id="b6f7e-129">150</span></span></td>
<td><span data-ttu-id="b6f7e-130">Vnt.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="b6f7e-131">1 800,00 $</span><span class="sxs-lookup"><span data-stu-id="b6f7e-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="b6f7e-132">12,00 $</span><span class="sxs-lookup"><span data-stu-id="b6f7e-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b6f7e-133">Toliau pateikiamoje lentelėje rodomas atsargų objekto skaičiavimo rezultatas.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="b6f7e-134">Rezultatą galite peržiūrėti **Išlaidų objekto** puslapyje spustelėję **Fizinis kiekis**.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="b6f7e-135">Objekto tipas</span><span class="sxs-lookup"><span data-stu-id="b6f7e-135">Object type</span></span></th>
<th><span data-ttu-id="b6f7e-136">Prekės numeris</span><span class="sxs-lookup"><span data-stu-id="b6f7e-136">Item number</span></span></th>
<th><span data-ttu-id="b6f7e-137">Svetainė</span><span class="sxs-lookup"><span data-stu-id="b6f7e-137">Site</span></span></th>
<th><span data-ttu-id="b6f7e-138">Sandėlis</span><span class="sxs-lookup"><span data-stu-id="b6f7e-138">Warehouse</span></span></th>
<th><span data-ttu-id="b6f7e-139">Paketo nr.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-139">Batch No.</span></span></th>
<th><span data-ttu-id="b6f7e-140">Kiekis</span><span class="sxs-lookup"><span data-stu-id="b6f7e-140">Quantity</span></span></th>
<th><span data-ttu-id="b6f7e-141">Atsargų vienetas</span><span class="sxs-lookup"><span data-stu-id="b6f7e-141">Inventory unit</span></span></th>
<th><span data-ttu-id="b6f7e-142">Vertė</span><span class="sxs-lookup"><span data-stu-id="b6f7e-142">Value</span></span></th>
<th><span data-ttu-id="b6f7e-143">Vidutinė vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="b6f7e-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6f7e-144">Atsargų objektas</span><span class="sxs-lookup"><span data-stu-id="b6f7e-144">Inventory object</span></span></td>
<td><span data-ttu-id="b6f7e-145">A</span><span class="sxs-lookup"><span data-stu-id="b6f7e-145">A</span></span></td>
<td><span data-ttu-id="b6f7e-146">1</span><span class="sxs-lookup"><span data-stu-id="b6f7e-146">1</span></span></td>
<td><span data-ttu-id="b6f7e-147">11</span><span class="sxs-lookup"><span data-stu-id="b6f7e-147">11</span></span></td>
<td><span data-ttu-id="b6f7e-148">B1</span><span class="sxs-lookup"><span data-stu-id="b6f7e-148">B1</span></span></td>
<td><span data-ttu-id="b6f7e-149">100</span><span class="sxs-lookup"><span data-stu-id="b6f7e-149">100</span></span></td>
<td><span data-ttu-id="b6f7e-150">Vnt.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="b6f7e-151">1 200,00 $</span><span class="sxs-lookup"><span data-stu-id="b6f7e-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="b6f7e-152">12,00 $</span><span class="sxs-lookup"><span data-stu-id="b6f7e-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6f7e-153">Atsargų objektas</span><span class="sxs-lookup"><span data-stu-id="b6f7e-153">Inventory object</span></span></td>
<td><span data-ttu-id="b6f7e-154">A</span><span class="sxs-lookup"><span data-stu-id="b6f7e-154">A</span></span></td>
<td><span data-ttu-id="b6f7e-155">1</span><span class="sxs-lookup"><span data-stu-id="b6f7e-155">1</span></span></td>
<td><span data-ttu-id="b6f7e-156">11</span><span class="sxs-lookup"><span data-stu-id="b6f7e-156">11</span></span></td>
<td><span data-ttu-id="b6f7e-157">B2</span><span class="sxs-lookup"><span data-stu-id="b6f7e-157">B2</span></span></td>
<td><span data-ttu-id="b6f7e-158">50</span><span class="sxs-lookup"><span data-stu-id="b6f7e-158">50</span></span></td>
<td><span data-ttu-id="b6f7e-159">Vnt.</span><span class="sxs-lookup"><span data-stu-id="b6f7e-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="b6f7e-160">600,00 $</span><span class="sxs-lookup"><span data-stu-id="b6f7e-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="b6f7e-161">12,00 $</span><span class="sxs-lookup"><span data-stu-id="b6f7e-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="b6f7e-162">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b6f7e-162">Additional resources</span></span>
--------

[<span data-ttu-id="b6f7e-163">Savikainos objektai</span><span class="sxs-lookup"><span data-stu-id="b6f7e-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="b6f7e-164">Savikainos įrašai</span><span class="sxs-lookup"><span data-stu-id="b6f7e-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="b6f7e-165">Kas nauja ir pasikeitė</span><span class="sxs-lookup"><span data-stu-id="b6f7e-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]