--- 
title: "Kurti žaliavas (2016 m. vasario mėn.)"
description: "Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų komponentus."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="7f69f-103">Kurti žaliavas (2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="7f69f-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f69f-104">Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų komponentus.</span><span class="sxs-lookup"><span data-stu-id="7f69f-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="7f69f-105">Tai trečioji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="7f69f-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="7f69f-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="7f69f-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="7f69f-107">Kurti pirmąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="7f69f-107">Create the first material</span></span>
1. <span data-ttu-id="7f69f-108">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="7f69f-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7f69f-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-109">Click New.</span></span>
3. <span data-ttu-id="7f69f-110">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7f69f-111">Šiame pavyzdyje įveskite ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7f69f-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="7f69f-112">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-113">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="7f69f-113">Select STD.</span></span> <span data-ttu-id="7f69f-114">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="7f69f-115">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-116">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-116">For example, select Audio.</span></span> <span data-ttu-id="7f69f-117">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="7f69f-118">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-119">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7f69f-119">Select SiteWH.</span></span> <span data-ttu-id="7f69f-120">Demonstravimui bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="7f69f-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="7f69f-121">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-122">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7f69f-123">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="7f69f-123">Select None.</span></span>  
8. <span data-ttu-id="7f69f-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7f69f-124">Click OK.</span></span>
9. <span data-ttu-id="7f69f-125">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="7f69f-126">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-126">Click Default order settings.</span></span>
11. <span data-ttu-id="7f69f-127">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-128">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7f69f-129">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-130">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7f69f-131">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-132">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="7f69f-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-133">Close the page.</span></span>
15. <span data-ttu-id="7f69f-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-134">Close the page.</span></span>
16. <span data-ttu-id="7f69f-135">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7f69f-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f69f-136">Spustelėkite ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7f69f-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="7f69f-137">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="7f69f-138">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7f69f-139">Šiame pavyzdyje įveskite M2.</span><span class="sxs-lookup"><span data-stu-id="7f69f-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="7f69f-140">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="7f69f-141">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="7f69f-141">Click Item price.</span></span>
21. <span data-ttu-id="7f69f-142">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-142">Click New.</span></span>
22. <span data-ttu-id="7f69f-143">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-144">Šiame pavyzdyje pasirinkite 10, kuris yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="7f69f-145">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-146">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="7f69f-147">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7f69f-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7f69f-148">Šiame pavyzdyje įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="7f69f-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="7f69f-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7f69f-149">Click Save.</span></span>
26. <span data-ttu-id="7f69f-150">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="7f69f-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="7f69f-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-151">Close the page.</span></span>
28. <span data-ttu-id="7f69f-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="7f69f-153">Kurti antrąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="7f69f-153">Create the second material</span></span>
1. <span data-ttu-id="7f69f-154">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-154">Click New.</span></span>
2. <span data-ttu-id="7f69f-155">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7f69f-156">Šiame pavyzdyje įveskite ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7f69f-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="7f69f-157">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-158">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="7f69f-158">Select STD.</span></span> <span data-ttu-id="7f69f-159">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7f69f-160">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-161">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-161">For example, select Audio.</span></span> <span data-ttu-id="7f69f-162">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7f69f-163">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-164">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7f69f-164">Select SiteWH.</span></span> <span data-ttu-id="7f69f-165">Šiame pavyzdyje bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="7f69f-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="7f69f-166">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-167">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7f69f-168">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="7f69f-168">Select None.</span></span>  
7. <span data-ttu-id="7f69f-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7f69f-169">Click OK.</span></span>
8. <span data-ttu-id="7f69f-170">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7f69f-171">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-171">Click Default order settings.</span></span>
10. <span data-ttu-id="7f69f-172">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-173">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7f69f-174">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-175">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7f69f-176">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-177">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7f69f-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-178">Close the page.</span></span>
14. <span data-ttu-id="7f69f-179">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-179">Close the page.</span></span>
15. <span data-ttu-id="7f69f-180">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7f69f-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f69f-181">Spustelėkite ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7f69f-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="7f69f-182">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7f69f-183">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7f69f-184">Šiame pavyzdyje įveskite M2.</span><span class="sxs-lookup"><span data-stu-id="7f69f-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="7f69f-185">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7f69f-186">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="7f69f-186">Click Item price.</span></span>
20. <span data-ttu-id="7f69f-187">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-187">Click New.</span></span>
21. <span data-ttu-id="7f69f-188">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-189">Šiame pavyzdyje pasirinkite 10.</span><span class="sxs-lookup"><span data-stu-id="7f69f-189">For this example, select 10.</span></span> <span data-ttu-id="7f69f-190">Tai yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7f69f-191">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-192">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7f69f-193">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7f69f-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7f69f-194">Norėdami demonstruoti, įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="7f69f-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="7f69f-195">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7f69f-195">Click Save.</span></span>
25. <span data-ttu-id="7f69f-196">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="7f69f-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7f69f-197">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-197">Close the page.</span></span>
27. <span data-ttu-id="7f69f-198">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="7f69f-199">Kurti trečiąją medžiagą</span><span class="sxs-lookup"><span data-stu-id="7f69f-199">Create the third material</span></span>
1. <span data-ttu-id="7f69f-200">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-200">Click New.</span></span>
2. <span data-ttu-id="7f69f-201">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7f69f-202">Norėdami demonstruoti, įveskite ITEM_C</span><span class="sxs-lookup"><span data-stu-id="7f69f-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="7f69f-203">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-204">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="7f69f-204">Select STD.</span></span> <span data-ttu-id="7f69f-205">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7f69f-206">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-207">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-207">For example, select Audio.</span></span> <span data-ttu-id="7f69f-208">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7f69f-209">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-210">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7f69f-210">Select SiteWH.</span></span> <span data-ttu-id="7f69f-211">Demonstravimui bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="7f69f-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="7f69f-212">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-213">Šiame pavyzdyje sekimo dimensijos nenaudojamos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7f69f-214">Pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="7f69f-214">Select None.</span></span>  
7. <span data-ttu-id="7f69f-215">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7f69f-215">Click OK.</span></span>
8. <span data-ttu-id="7f69f-216">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7f69f-217">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="7f69f-217">Click Default order settings.</span></span>
10. <span data-ttu-id="7f69f-218">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-219">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7f69f-220">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-221">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7f69f-222">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-223">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7f69f-224">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-224">Close the page.</span></span>
14. <span data-ttu-id="7f69f-225">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-225">Close the page.</span></span>
15. <span data-ttu-id="7f69f-226">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7f69f-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f69f-227">Spustelėkite ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="7f69f-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="7f69f-228">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7f69f-229">Lauke Išlaidų grupė įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7f69f-230">Šiame pavyzdyje įveskite M1.</span><span class="sxs-lookup"><span data-stu-id="7f69f-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="7f69f-231">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7f69f-232">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="7f69f-232">Click Item price.</span></span>
20. <span data-ttu-id="7f69f-233">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-233">Click New.</span></span>
21. <span data-ttu-id="7f69f-234">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-235">Šiame pavyzdyje pasirinkite 10.</span><span class="sxs-lookup"><span data-stu-id="7f69f-235">For this example, select 10.</span></span> <span data-ttu-id="7f69f-236">Tai yra standartinių išlaidų įkainojimo tipas.</span><span class="sxs-lookup"><span data-stu-id="7f69f-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7f69f-237">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7f69f-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7f69f-238">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="7f69f-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7f69f-239">Lauke Kaina įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7f69f-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7f69f-240">Šiame pavyzdyje įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="7f69f-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="7f69f-241">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7f69f-241">Click Save.</span></span>
25. <span data-ttu-id="7f69f-242">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="7f69f-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7f69f-243">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-243">Close the page.</span></span>
27. <span data-ttu-id="7f69f-244">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7f69f-244">Close the page.</span></span>


