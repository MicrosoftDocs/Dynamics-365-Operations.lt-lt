--- 
title: "Kurti KS (2016 m. vasario mėn.)"
description: "Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų KS struktūrą."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="create-boms-february-2016"></a><span data-ttu-id="281f6-103">Kurti KS (2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="281f6-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="281f6-104">Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų KS struktūrą.</span><span class="sxs-lookup"><span data-stu-id="281f6-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="281f6-105">Tai ketvirtoji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="281f6-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="281f6-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="281f6-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="281f6-107">Kurti pusiau baigto produkto KS</span><span class="sxs-lookup"><span data-stu-id="281f6-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="281f6-108">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="281f6-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="281f6-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="281f6-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="281f6-110">Pasirinkite prekės numerį BOM_2.</span><span class="sxs-lookup"><span data-stu-id="281f6-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="281f6-111">Veiksmų srityje spustelėkite Inžinierius.</span><span class="sxs-lookup"><span data-stu-id="281f6-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="281f6-112">Spustelėkite KS versijos.</span><span class="sxs-lookup"><span data-stu-id="281f6-112">Click BOM versions.</span></span>
5. <span data-ttu-id="281f6-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="281f6-113">Click New.</span></span>
6. <span data-ttu-id="281f6-114">Spustelėkite KS ir KS versija.</span><span class="sxs-lookup"><span data-stu-id="281f6-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="281f6-115">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="281f6-116">Pavyzdžiui, įveskite BOM_2.</span><span class="sxs-lookup"><span data-stu-id="281f6-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="281f6-117">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="281f6-118">Šiame pavyzdyje įveskite arba pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="281f6-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="281f6-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="281f6-119">Click OK.</span></span>
10. <span data-ttu-id="281f6-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="281f6-120">Click New.</span></span>
11. <span data-ttu-id="281f6-121">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="281f6-122">Šiame pavyzdyje įveskite ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="281f6-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="281f6-123">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="281f6-124">Šiame pavyzdyje įveskite arba pasirinkite 11.</span><span class="sxs-lookup"><span data-stu-id="281f6-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="281f6-125">Spustelėkite Antraštė.</span><span class="sxs-lookup"><span data-stu-id="281f6-125">Click Header.</span></span>
14. <span data-ttu-id="281f6-126">Norėdami patvirtinti KS, spustelėkite Patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="281f6-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="281f6-127">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="281f6-127">Click OK.</span></span>
16. <span data-ttu-id="281f6-128">Spustelėkite „Patvirtinti“.</span><span class="sxs-lookup"><span data-stu-id="281f6-128">Click Approve.</span></span>
    * <span data-ttu-id="281f6-129">Mygtukas Tvirtinti yra įrankių juostos dalyje KS versijos.</span><span class="sxs-lookup"><span data-stu-id="281f6-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="281f6-130">Norėdami matyti užslėptą mygtuką Tvirtinti, puslapio Komplektavimo specifikacijos dešinėje viršutinėje srityje spustelėkite Antraštė.</span><span class="sxs-lookup"><span data-stu-id="281f6-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="281f6-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="281f6-131">Click OK.</span></span>
18. <span data-ttu-id="281f6-132">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="281f6-132">Click Activate.</span></span>
19. <span data-ttu-id="281f6-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="281f6-133">Close the page.</span></span>
20. <span data-ttu-id="281f6-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="281f6-134">Close the page.</span></span>
21. <span data-ttu-id="281f6-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="281f6-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="281f6-136">Kurti galutinio produkto KS</span><span class="sxs-lookup"><span data-stu-id="281f6-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="281f6-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="281f6-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="281f6-138">Pasirinkite prekės numerį BOM_1.</span><span class="sxs-lookup"><span data-stu-id="281f6-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="281f6-139">Veiksmų srityje spustelėkite Inžinierius.</span><span class="sxs-lookup"><span data-stu-id="281f6-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="281f6-140">Spustelėkite KS versijos.</span><span class="sxs-lookup"><span data-stu-id="281f6-140">Click BOM versions.</span></span>
4. <span data-ttu-id="281f6-141">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="281f6-141">Click New.</span></span>
5. <span data-ttu-id="281f6-142">Spustelėkite KS ir KS versija.</span><span class="sxs-lookup"><span data-stu-id="281f6-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="281f6-143">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="281f6-144">Pavyzdžiui, įveskite BOM_1.</span><span class="sxs-lookup"><span data-stu-id="281f6-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="281f6-145">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="281f6-146">Šiame pavyzdyje įveskite arba pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="281f6-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="281f6-147">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="281f6-147">Click OK.</span></span>
9. <span data-ttu-id="281f6-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="281f6-148">Click New.</span></span>
10. <span data-ttu-id="281f6-149">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="281f6-150">Šiame pavyzdyje įveskite ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="281f6-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="281f6-151">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="281f6-152">Šiame pavyzdyje pasirinkite 11.</span><span class="sxs-lookup"><span data-stu-id="281f6-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="281f6-153">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="281f6-153">Click New.</span></span>
13. <span data-ttu-id="281f6-154">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="281f6-155">Šiame pavyzdyje įveskite ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="281f6-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="281f6-156">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="281f6-157">Šiame pavyzdyje įveskite arba pasirinkite 11.</span><span class="sxs-lookup"><span data-stu-id="281f6-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="281f6-158">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="281f6-158">Click New.</span></span>
16. <span data-ttu-id="281f6-159">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="281f6-160">Šiame pavyzdyje įveskite BOM_2.</span><span class="sxs-lookup"><span data-stu-id="281f6-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="281f6-161">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="281f6-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="281f6-162">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="281f6-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="281f6-163">Šiame pavyzdyje įveskite arba pasirinkite 11 sandėlį.</span><span class="sxs-lookup"><span data-stu-id="281f6-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="281f6-164">Spustelėkite Antraštė.</span><span class="sxs-lookup"><span data-stu-id="281f6-164">Click Header.</span></span>
20. <span data-ttu-id="281f6-165">Norėdami patvirtinti KS, spustelėkite Patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="281f6-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="281f6-166">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="281f6-166">Click OK.</span></span>
22. <span data-ttu-id="281f6-167">Spustelėkite „Patvirtinti“.</span><span class="sxs-lookup"><span data-stu-id="281f6-167">Click Approve.</span></span>
    * <span data-ttu-id="281f6-168">Mygtukas Tvirtinti yra įrankių juostos dalyje KS versijos.</span><span class="sxs-lookup"><span data-stu-id="281f6-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="281f6-169">Norėdami matyti užslėptą mygtuką Tvirtinti, puslapio Komplektavimo specifikacijos dešinėje viršutinėje srityje spustelėkite Antraštė.</span><span class="sxs-lookup"><span data-stu-id="281f6-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="281f6-170">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="281f6-170">Click OK.</span></span>
24. <span data-ttu-id="281f6-171">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="281f6-171">Click Activate.</span></span>
25. <span data-ttu-id="281f6-172">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="281f6-172">Close the page.</span></span>
26. <span data-ttu-id="281f6-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="281f6-173">Close the page.</span></span>
27. <span data-ttu-id="281f6-174">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="281f6-174">Close the page.</span></span>


