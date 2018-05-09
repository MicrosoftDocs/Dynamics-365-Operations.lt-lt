--- 
title: "Kurti daug pardavimo pasiūlymų"
description: "Ši procedūra parodo, kaip efektyviai kurti pasiūlymus, kuriuose siūlomi produktų ar paslaugų rinkiniai, ketinami siųsti keliems klientams."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e3bc39912d19880258ff7dd56c74b77b52deda3a
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="8ccb9-103">Kurti daug pardavimo pasiūlymų</span><span class="sxs-lookup"><span data-stu-id="8ccb9-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ccb9-104">Ši procedūra parodo, kaip efektyviai kurti pasiūlymus, kuriuose siūlomi produktų ar paslaugų rinkiniai, ketinami siųsti keliems klientams.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="8ccb9-105">Šis masinis pasiūlymo kūrimas pagrįstas pasiūlymų šablonais.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="8ccb9-106">Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="8ccb9-107">Kurti pasiūlymo šabloną</span><span class="sxs-lookup"><span data-stu-id="8ccb9-107">Create a quotation template</span></span>
1. <span data-ttu-id="8ccb9-108">Eikite į Pardavimas ir rinkodaras > Nustatymas > Pasiūlymai > Šablonų grupės.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="8ccb9-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-109">Click New.</span></span>
3. <span data-ttu-id="8ccb9-110">Lauke Grupės ID įveskite savo pasirinktą ID.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="8ccb9-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8ccb9-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-112">Click Save.</span></span>
6. <span data-ttu-id="8ccb9-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-113">Close the page.</span></span>
7. <span data-ttu-id="8ccb9-114">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="8ccb9-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-115">Click New.</span></span>
9. <span data-ttu-id="8ccb9-116">Lauke Sąskaitos tipas pasirinkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="8ccb9-117">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="8ccb9-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-118">Click OK.</span></span>
    * <span data-ttu-id="8ccb9-119">Tam, kad pasiūlymas taptų šablonu, turite atlikti pasiūlymo antraštės nustatymo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="8ccb9-120">Tai reikia padaryti prieš įtraukiant eilutes į pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="8ccb9-121">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="8ccb9-122">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-122">Click Change view.</span></span>
14. <span data-ttu-id="8ccb9-123">Spustelėkite antraštės rodinį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-123">Click Header view.</span></span>
15. <span data-ttu-id="8ccb9-124">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="8ccb9-125">Lauke Grupės ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="8ccb9-126">Lauke Šablono pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="8ccb9-127">Lauke Aktyvus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="8ccb9-128">Kai taikote šabloną naujam pardavimo pasiūlymui, galima naudoti tik aktyvius šablonus.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="8ccb9-129">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="8ccb9-130">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-130">Click Change view.</span></span>
21. <span data-ttu-id="8ccb9-131">Spustelėkite Eilutės rodinys.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-131">Click Line view.</span></span>
22. <span data-ttu-id="8ccb9-132">Lauke Prekė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="8ccb9-133">Lauke Prekė įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="8ccb9-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-134">Close the page.</span></span>
25. <span data-ttu-id="8ccb9-135">Lauke Nuolaidos procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="8ccb9-136">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-136">Click Add line.</span></span>
27. <span data-ttu-id="8ccb9-137">Lauke Prekė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="8ccb9-138">Lauke Prekė įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="8ccb9-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-139">Close the page.</span></span>
30. <span data-ttu-id="8ccb9-140">Lauke Vieneto kaina įveskite naują kainą arba pakeiskite dabartinę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="8ccb9-141">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-141">Click Add line.</span></span>
32. <span data-ttu-id="8ccb9-142">Lauke Prekė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="8ccb9-143">Lauke Prekė įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="8ccb9-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-144">Close the page.</span></span>
35. <span data-ttu-id="8ccb9-145">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="8ccb9-146">Lauke Nuolaida įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="8ccb9-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="8ccb9-148">Taikyti šabloną vienam pasiūlymui sukurti</span><span class="sxs-lookup"><span data-stu-id="8ccb9-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="8ccb9-149">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="8ccb9-150">Atkreipkite dėmesį, kad pasiūlymas, kurį ką tik sukūrėte pažymėtas kaip šablonas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="8ccb9-151">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-151">Click New.</span></span>
3. <span data-ttu-id="8ccb9-152">Lauke Sąskaitos tipas pasirinkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="8ccb9-153">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="8ccb9-154">Išplėskite skyrių Šablonas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-154">Expand the Template section.</span></span>
6. <span data-ttu-id="8ccb9-155">Lauke Grupės ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="8ccb9-156">Lauke Šablono pavadinimas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="8ccb9-157">Lauke Skaičiavimo metodas, pasirinkite 'Pagrįsta šablonų vertėmis'.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="8ccb9-158">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-158">Click OK.</span></span>
    * <span data-ttu-id="8ccb9-159">Naujas pasiūlymas sukurtas atsižvelgiant į šablono duomenis ir sąlygas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="8ccb9-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-160">Close the page.</span></span>
11. <span data-ttu-id="8ccb9-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="8ccb9-162">Taikyti šabloną kuriant daug pasiūlymų</span><span class="sxs-lookup"><span data-stu-id="8ccb9-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="8ccb9-163">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Pasiūlymo atnaujinimas > Kurti daug pasiūlymų.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="8ccb9-164">Lauke Sąskaitos tipas pasirinkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="8ccb9-165">Lauke Grupės ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="8ccb9-166">Lauke Šablono pavadinimas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="8ccb9-167">Lauke Skaičiavimo metodas, pasirinkite 'Pagrįsta šablonų vertėmis'.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="8ccb9-168">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="8ccb9-169">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-169">Click Filter.</span></span>
8. <span data-ttu-id="8ccb9-170">Lauke Kriterijus nustatykite filtrą, kuris apimtų diapazoną klientų, kuriuos norite įtraukti į šio masinio pasiūlymo kūrimą.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="8ccb9-171">Naudokite šį formatą: „Customer1... CustomerN.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="8ccb9-172">Pvz., galite nustatyti filtrą į: US-001... US-004</span><span class="sxs-lookup"><span data-stu-id="8ccb9-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="8ccb9-173">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-173">Click OK.</span></span>
10. <span data-ttu-id="8ccb9-174">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-174">Click OK.</span></span>
11. <span data-ttu-id="8ccb9-175">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="8ccb9-176">Patikrinkite, kad pasiūlymai buvo sukurti visiems klientams, nurodytiems masinio atnaujinimo procedūros metu, remiantis pasirinktu šablonu.</span><span class="sxs-lookup"><span data-stu-id="8ccb9-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


