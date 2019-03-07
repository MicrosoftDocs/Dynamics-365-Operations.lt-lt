---
title: Kurti žaliavas (2016 m. vasario mėn.)
description: Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų komponentus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "351061"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="55bae-103">Kurti žaliavas (2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="55bae-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55bae-104">Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų komponentus.</span><span class="sxs-lookup"><span data-stu-id="55bae-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="55bae-105">Tai trečioji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="55bae-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="55bae-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="55bae-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="55bae-107">Kurti pirmąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="55bae-107">Create the first material</span></span>
1. <span data-ttu-id="55bae-108">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="55bae-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="55bae-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="55bae-109">Click New.</span></span>
3. <span data-ttu-id="55bae-110">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="55bae-111">Šiame pavyzdyje įveskite ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="55bae-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="55bae-112">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-113">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="55bae-113">Select STD.</span></span> <span data-ttu-id="55bae-114">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="55bae-115">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="55bae-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-116">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="55bae-116">For example, select Audio.</span></span> <span data-ttu-id="55bae-117">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="55bae-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="55bae-118">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-119">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="55bae-119">Select SiteWH.</span></span> <span data-ttu-id="55bae-120">Demonstravimui bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="55bae-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="55bae-121">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-122">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="55bae-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="55bae-123">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="55bae-123">Select None.</span></span>  
8. <span data-ttu-id="55bae-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="55bae-124">Click OK.</span></span>
9. <span data-ttu-id="55bae-125">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="55bae-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="55bae-126">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="55bae-126">Click Default order settings.</span></span>
11. <span data-ttu-id="55bae-127">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-128">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="55bae-129">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-130">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="55bae-131">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-132">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="55bae-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-133">Close the page.</span></span>
15. <span data-ttu-id="55bae-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-134">Close the page.</span></span>
16. <span data-ttu-id="55bae-135">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="55bae-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="55bae-136">Spustelėkite ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="55bae-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="55bae-137">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="55bae-138">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="55bae-139">Šiame pavyzdyje įveskite M2.</span><span class="sxs-lookup"><span data-stu-id="55bae-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="55bae-140">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="55bae-141">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="55bae-141">Click Item price.</span></span>
21. <span data-ttu-id="55bae-142">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="55bae-142">Click New.</span></span>
22. <span data-ttu-id="55bae-143">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-144">Šiame pavyzdyje pasirinkite 10, kuris yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="55bae-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="55bae-145">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-146">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="55bae-147">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="55bae-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="55bae-148">Šiame pavyzdyje įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="55bae-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="55bae-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="55bae-149">Click Save.</span></span>
26. <span data-ttu-id="55bae-150">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="55bae-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="55bae-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-151">Close the page.</span></span>
28. <span data-ttu-id="55bae-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="55bae-153">Kurti antrąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="55bae-153">Create the second material</span></span>
1. <span data-ttu-id="55bae-154">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="55bae-154">Click New.</span></span>
2. <span data-ttu-id="55bae-155">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="55bae-156">Šiame pavyzdyje įveskite ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="55bae-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="55bae-157">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-158">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="55bae-158">Select STD.</span></span> <span data-ttu-id="55bae-159">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="55bae-160">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="55bae-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-161">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="55bae-161">For example, select Audio.</span></span> <span data-ttu-id="55bae-162">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="55bae-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="55bae-163">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-164">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="55bae-164">Select SiteWH.</span></span> <span data-ttu-id="55bae-165">Šiame pavyzdyje bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="55bae-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="55bae-166">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-167">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="55bae-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="55bae-168">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="55bae-168">Select None.</span></span>  
7. <span data-ttu-id="55bae-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="55bae-169">Click OK.</span></span>
8. <span data-ttu-id="55bae-170">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="55bae-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="55bae-171">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="55bae-171">Click Default order settings.</span></span>
10. <span data-ttu-id="55bae-172">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-173">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="55bae-174">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-175">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="55bae-176">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-177">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="55bae-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-178">Close the page.</span></span>
14. <span data-ttu-id="55bae-179">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-179">Close the page.</span></span>
15. <span data-ttu-id="55bae-180">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="55bae-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="55bae-181">Spustelėkite ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="55bae-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="55bae-182">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="55bae-183">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="55bae-184">Šiame pavyzdyje įveskite M2.</span><span class="sxs-lookup"><span data-stu-id="55bae-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="55bae-185">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="55bae-186">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="55bae-186">Click Item price.</span></span>
20. <span data-ttu-id="55bae-187">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="55bae-187">Click New.</span></span>
21. <span data-ttu-id="55bae-188">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-189">Šiame pavyzdyje pasirinkite 10.</span><span class="sxs-lookup"><span data-stu-id="55bae-189">For this example, select 10.</span></span> <span data-ttu-id="55bae-190">Tai yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="55bae-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="55bae-191">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-192">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="55bae-193">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="55bae-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="55bae-194">Norėdami demonstruoti, įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="55bae-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="55bae-195">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="55bae-195">Click Save.</span></span>
25. <span data-ttu-id="55bae-196">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="55bae-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="55bae-197">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-197">Close the page.</span></span>
27. <span data-ttu-id="55bae-198">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="55bae-199">Kurti trečiąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="55bae-199">Create the third material</span></span>
1. <span data-ttu-id="55bae-200">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="55bae-200">Click New.</span></span>
2. <span data-ttu-id="55bae-201">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="55bae-202">Norėdami demonstruoti, įveskite ITEM_C</span><span class="sxs-lookup"><span data-stu-id="55bae-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="55bae-203">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-204">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="55bae-204">Select STD.</span></span> <span data-ttu-id="55bae-205">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="55bae-206">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="55bae-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-207">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="55bae-207">For example, select Audio.</span></span> <span data-ttu-id="55bae-208">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="55bae-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="55bae-209">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-210">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="55bae-210">Select SiteWH.</span></span> <span data-ttu-id="55bae-211">Demonstravimui bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="55bae-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="55bae-212">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-213">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="55bae-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="55bae-214">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="55bae-214">Select None.</span></span>  
7. <span data-ttu-id="55bae-215">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="55bae-215">Click OK.</span></span>
8. <span data-ttu-id="55bae-216">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="55bae-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="55bae-217">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="55bae-217">Click Default order settings.</span></span>
10. <span data-ttu-id="55bae-218">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-219">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="55bae-220">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-221">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="55bae-222">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-223">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="55bae-224">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-224">Close the page.</span></span>
14. <span data-ttu-id="55bae-225">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-225">Close the page.</span></span>
15. <span data-ttu-id="55bae-226">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="55bae-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="55bae-227">Spustelėkite ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="55bae-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="55bae-228">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="55bae-229">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="55bae-230">Šiame pavyzdyje įveskite M1.</span><span class="sxs-lookup"><span data-stu-id="55bae-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="55bae-231">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="55bae-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="55bae-232">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="55bae-232">Click Item price.</span></span>
20. <span data-ttu-id="55bae-233">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="55bae-233">Click New.</span></span>
21. <span data-ttu-id="55bae-234">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-235">Šiame pavyzdyje pasirinkite 10.</span><span class="sxs-lookup"><span data-stu-id="55bae-235">For this example, select 10.</span></span> <span data-ttu-id="55bae-236">Tai yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="55bae-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="55bae-237">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="55bae-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="55bae-238">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="55bae-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="55bae-239">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="55bae-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="55bae-240">Šiame pavyzdyje įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="55bae-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="55bae-241">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="55bae-241">Click Save.</span></span>
25. <span data-ttu-id="55bae-242">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="55bae-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="55bae-243">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-243">Close the page.</span></span>
27. <span data-ttu-id="55bae-244">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55bae-244">Close the page.</span></span>

