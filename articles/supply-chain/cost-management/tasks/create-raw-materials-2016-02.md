--- 
title: "Kurti žaliavas (tik 2016 m. vasario mėn.)"
description: "Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų komponentus."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3d77dcc20fe7402af83dd724e7fef848977e5bf8
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="601ad-103">Kurti žaliavas (tik 2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="601ad-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="601ad-104">Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų komponentus.</span><span class="sxs-lookup"><span data-stu-id="601ad-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="601ad-105">Tai trečioji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="601ad-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="601ad-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="601ad-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="601ad-107">Kurti pirmąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="601ad-107">Create the first material</span></span>
1. <span data-ttu-id="601ad-108">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="601ad-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="601ad-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="601ad-109">Click New.</span></span>
3. <span data-ttu-id="601ad-110">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="601ad-111">Šiame pavyzdyje įveskite ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="601ad-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="601ad-112">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-113">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="601ad-113">Select STD.</span></span> <span data-ttu-id="601ad-114">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="601ad-115">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="601ad-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-116">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="601ad-116">For example, select Audio.</span></span> <span data-ttu-id="601ad-117">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="601ad-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="601ad-118">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-119">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="601ad-119">Select SiteWH.</span></span> <span data-ttu-id="601ad-120">Demonstravimui bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="601ad-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="601ad-121">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-122">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="601ad-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="601ad-123">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="601ad-123">Select None.</span></span>  
8. <span data-ttu-id="601ad-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="601ad-124">Click OK.</span></span>
9. <span data-ttu-id="601ad-125">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="601ad-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="601ad-126">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="601ad-126">Click Default order settings.</span></span>
11. <span data-ttu-id="601ad-127">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-128">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="601ad-129">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-130">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="601ad-131">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-132">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="601ad-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-133">Close the page.</span></span>
15. <span data-ttu-id="601ad-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-134">Close the page.</span></span>
16. <span data-ttu-id="601ad-135">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="601ad-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="601ad-136">Spustelėkite ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="601ad-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="601ad-137">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="601ad-138">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="601ad-139">Šiame pavyzdyje įveskite M2.</span><span class="sxs-lookup"><span data-stu-id="601ad-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="601ad-140">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="601ad-141">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="601ad-141">Click Item price.</span></span>
21. <span data-ttu-id="601ad-142">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="601ad-142">Click New.</span></span>
22. <span data-ttu-id="601ad-143">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-144">Šiame pavyzdyje pasirinkite 10, kuris yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="601ad-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="601ad-145">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-146">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="601ad-147">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="601ad-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="601ad-148">Šiame pavyzdyje įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="601ad-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="601ad-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="601ad-149">Click Save.</span></span>
26. <span data-ttu-id="601ad-150">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="601ad-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="601ad-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-151">Close the page.</span></span>
28. <span data-ttu-id="601ad-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="601ad-153">Kurti antrąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="601ad-153">Create the second material</span></span>
1. <span data-ttu-id="601ad-154">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="601ad-154">Click New.</span></span>
2. <span data-ttu-id="601ad-155">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="601ad-156">Šiame pavyzdyje įveskite ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="601ad-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="601ad-157">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-158">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="601ad-158">Select STD.</span></span> <span data-ttu-id="601ad-159">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="601ad-160">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="601ad-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-161">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="601ad-161">For example, select Audio.</span></span> <span data-ttu-id="601ad-162">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="601ad-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="601ad-163">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-164">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="601ad-164">Select SiteWH.</span></span> <span data-ttu-id="601ad-165">Šiame pavyzdyje bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="601ad-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="601ad-166">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-167">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="601ad-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="601ad-168">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="601ad-168">Select None.</span></span>  
7. <span data-ttu-id="601ad-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="601ad-169">Click OK.</span></span>
8. <span data-ttu-id="601ad-170">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="601ad-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="601ad-171">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="601ad-171">Click Default order settings.</span></span>
10. <span data-ttu-id="601ad-172">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-173">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="601ad-174">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-175">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="601ad-176">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-177">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="601ad-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-178">Close the page.</span></span>
14. <span data-ttu-id="601ad-179">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-179">Close the page.</span></span>
15. <span data-ttu-id="601ad-180">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="601ad-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="601ad-181">Spustelėkite ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="601ad-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="601ad-182">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="601ad-183">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="601ad-184">Šiame pavyzdyje įveskite M2.</span><span class="sxs-lookup"><span data-stu-id="601ad-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="601ad-185">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="601ad-186">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="601ad-186">Click Item price.</span></span>
20. <span data-ttu-id="601ad-187">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="601ad-187">Click New.</span></span>
21. <span data-ttu-id="601ad-188">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-189">Šiame pavyzdyje pasirinkite 10.</span><span class="sxs-lookup"><span data-stu-id="601ad-189">For this example, select 10.</span></span> <span data-ttu-id="601ad-190">Tai yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="601ad-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="601ad-191">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-192">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="601ad-193">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="601ad-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="601ad-194">Norėdami demonstruoti, įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="601ad-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="601ad-195">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="601ad-195">Click Save.</span></span>
25. <span data-ttu-id="601ad-196">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="601ad-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="601ad-197">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-197">Close the page.</span></span>
27. <span data-ttu-id="601ad-198">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="601ad-199">Kurti trečiąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="601ad-199">Create the third material</span></span>
1. <span data-ttu-id="601ad-200">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="601ad-200">Click New.</span></span>
2. <span data-ttu-id="601ad-201">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="601ad-202">Norėdami demonstruoti, įveskite ITEM_C</span><span class="sxs-lookup"><span data-stu-id="601ad-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="601ad-203">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-204">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="601ad-204">Select STD.</span></span> <span data-ttu-id="601ad-205">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="601ad-206">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="601ad-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-207">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="601ad-207">For example, select Audio.</span></span> <span data-ttu-id="601ad-208">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="601ad-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="601ad-209">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-210">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="601ad-210">Select SiteWH.</span></span> <span data-ttu-id="601ad-211">Demonstravimui bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="601ad-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="601ad-212">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-213">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="601ad-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="601ad-214">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="601ad-214">Select None.</span></span>  
7. <span data-ttu-id="601ad-215">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="601ad-215">Click OK.</span></span>
8. <span data-ttu-id="601ad-216">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="601ad-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="601ad-217">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="601ad-217">Click Default order settings.</span></span>
10. <span data-ttu-id="601ad-218">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-219">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="601ad-220">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-221">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="601ad-222">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-223">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="601ad-224">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-224">Close the page.</span></span>
14. <span data-ttu-id="601ad-225">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-225">Close the page.</span></span>
15. <span data-ttu-id="601ad-226">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="601ad-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="601ad-227">Spustelėkite ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="601ad-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="601ad-228">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="601ad-229">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="601ad-230">Šiame pavyzdyje įveskite M1.</span><span class="sxs-lookup"><span data-stu-id="601ad-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="601ad-231">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="601ad-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="601ad-232">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="601ad-232">Click Item price.</span></span>
20. <span data-ttu-id="601ad-233">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="601ad-233">Click New.</span></span>
21. <span data-ttu-id="601ad-234">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-235">Šiame pavyzdyje pasirinkite 10.</span><span class="sxs-lookup"><span data-stu-id="601ad-235">For this example, select 10.</span></span> <span data-ttu-id="601ad-236">Tai yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="601ad-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="601ad-237">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="601ad-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="601ad-238">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="601ad-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="601ad-239">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="601ad-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="601ad-240">Šiame pavyzdyje įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="601ad-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="601ad-241">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="601ad-241">Click Save.</span></span>
25. <span data-ttu-id="601ad-242">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="601ad-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="601ad-243">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-243">Close the page.</span></span>
27. <span data-ttu-id="601ad-244">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="601ad-244">Close the page.</span></span>


