---
title: Kurti daug pardavimo pasiūlymų
description: Ši procedūra parodo, kaip efektyviai kurti pasiūlymus, kuriuose siūlomi produktų ar paslaugų rinkiniai, ketinami siųsti keliems klientams.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1a9c7235f37ccdedc87ce70d3846443f645c0fe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211887"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="78770-103">Kurti daug pardavimo pasiūlymų</span><span class="sxs-lookup"><span data-stu-id="78770-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78770-104">Ši procedūra parodo, kaip efektyviai kurti pasiūlymus, kuriuose siūlomi produktų ar paslaugų rinkiniai, ketinami siųsti keliems klientams.</span><span class="sxs-lookup"><span data-stu-id="78770-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="78770-105">Šis masinis pasiūlymo kūrimas pagrįstas pasiūlymų šablonais.</span><span class="sxs-lookup"><span data-stu-id="78770-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="78770-106">Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="78770-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="78770-107">Kurti pasiūlymo šabloną</span><span class="sxs-lookup"><span data-stu-id="78770-107">Create a quotation template</span></span>
1. <span data-ttu-id="78770-108">Eikite į Pardavimas ir rinkodaras > Nustatymas > Pasiūlymai > Šablonų grupės.</span><span class="sxs-lookup"><span data-stu-id="78770-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="78770-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="78770-109">Click New.</span></span>
3. <span data-ttu-id="78770-110">Lauke Grupės ID įveskite savo pasirinktą ID.</span><span class="sxs-lookup"><span data-stu-id="78770-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="78770-111">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78770-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="78770-112">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="78770-112">Click Save.</span></span>
6. <span data-ttu-id="78770-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="78770-113">Close the page.</span></span>
7. <span data-ttu-id="78770-114">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="78770-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="78770-115">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="78770-115">Click New.</span></span>
9. <span data-ttu-id="78770-116">Lauke Sąskaitos tipas pasirinkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="78770-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="78770-117">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78770-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="78770-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="78770-118">Click OK.</span></span>
    * <span data-ttu-id="78770-119">Tam, kad pasiūlymas taptų šablonu, turite atlikti pasiūlymo antraštės nustatymo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="78770-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="78770-120">Tai reikia padaryti prieš įtraukiant eilutes į pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="78770-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="78770-121">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="78770-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="78770-122">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="78770-122">Click Change view.</span></span>
14. <span data-ttu-id="78770-123">Spustelėkite antraštės rodinį.</span><span class="sxs-lookup"><span data-stu-id="78770-123">Click Header view.</span></span>
15. <span data-ttu-id="78770-124">Išplėskite skyrių Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="78770-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="78770-125">Lauke Grupės ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="78770-126">Lauke Šablono pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78770-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="78770-127">Lauke Aktyvus pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="78770-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="78770-128">Kai taikote šabloną naujam pardavimo pasiūlymui, galima naudoti tik aktyvius šablonus.</span><span class="sxs-lookup"><span data-stu-id="78770-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="78770-129">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="78770-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="78770-130">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="78770-130">Click Change view.</span></span>
21. <span data-ttu-id="78770-131">Spustelėkite Eilutės rodinys.</span><span class="sxs-lookup"><span data-stu-id="78770-131">Click Line view.</span></span>
22. <span data-ttu-id="78770-132">Lauke Prekė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="78770-133">Lauke Prekė įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="78770-134">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="78770-134">Close the page.</span></span>
25. <span data-ttu-id="78770-135">Lauke Nuolaidos procentas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="78770-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="78770-136">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="78770-136">Click Add line.</span></span>
27. <span data-ttu-id="78770-137">Lauke Prekė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="78770-138">Lauke Prekė įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="78770-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="78770-139">Close the page.</span></span>
30. <span data-ttu-id="78770-140">Lauke Vieneto kaina įveskite naują kainą arba pakeiskite dabartinę.</span><span class="sxs-lookup"><span data-stu-id="78770-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="78770-141">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="78770-141">Click Add line.</span></span>
32. <span data-ttu-id="78770-142">Lauke Prekė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="78770-143">Lauke Prekė įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="78770-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="78770-144">Close the page.</span></span>
35. <span data-ttu-id="78770-145">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="78770-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="78770-146">Lauke Nuolaida įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="78770-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="78770-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="78770-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="78770-148">Taikyti šabloną vienam pasiūlymui sukurti</span><span class="sxs-lookup"><span data-stu-id="78770-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="78770-149">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="78770-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="78770-150">Atkreipkite dėmesį, kad pasiūlymas, kurį ką tik sukūrėte pažymėtas kaip šablonas.</span><span class="sxs-lookup"><span data-stu-id="78770-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="78770-151">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="78770-151">Click New.</span></span>
3. <span data-ttu-id="78770-152">Lauke Sąskaitos tipas pasirinkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="78770-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="78770-153">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="78770-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="78770-154">Išplėskite skyrių Šablonas.</span><span class="sxs-lookup"><span data-stu-id="78770-154">Expand the Template section.</span></span>
6. <span data-ttu-id="78770-155">Lauke Grupės ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="78770-156">Lauke Šablono pavadinimas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="78770-157">Lauke Skaičiavimo metodas, pasirinkite 'Pagrįsta šablonų vertėmis'.</span><span class="sxs-lookup"><span data-stu-id="78770-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="78770-158">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="78770-158">Click OK.</span></span>
    * <span data-ttu-id="78770-159">Naujas pasiūlymas sukurtas atsižvelgiant į šablono duomenis ir sąlygas.</span><span class="sxs-lookup"><span data-stu-id="78770-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="78770-160">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="78770-160">Close the page.</span></span>
11. <span data-ttu-id="78770-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="78770-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="78770-162">Taikyti šabloną kuriant daug pasiūlymų</span><span class="sxs-lookup"><span data-stu-id="78770-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="78770-163">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Pasiūlymo atnaujinimas > Kurti daug pasiūlymų.</span><span class="sxs-lookup"><span data-stu-id="78770-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="78770-164">Lauke Sąskaitos tipas pasirinkite Klientas.</span><span class="sxs-lookup"><span data-stu-id="78770-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="78770-165">Lauke Grupės ID įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="78770-166">Lauke Šablono pavadinimas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="78770-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="78770-167">Lauke Skaičiavimo metodas, pasirinkite 'Pagrįsta šablonų vertėmis'.</span><span class="sxs-lookup"><span data-stu-id="78770-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="78770-168">Išplėskite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="78770-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="78770-169">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="78770-169">Click Filter.</span></span>
8. <span data-ttu-id="78770-170">Lauke Kriterijus nustatykite filtrą, kuris apimtų diapazoną klientų, kuriuos norite įtraukti į šio masinio pasiūlymo kūrimą.</span><span class="sxs-lookup"><span data-stu-id="78770-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="78770-171">Naudokite šį formatą: „Customer1... CustomerN.</span><span class="sxs-lookup"><span data-stu-id="78770-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="78770-172">Pvz., galite nustatyti filtrą į: US-001... US-004</span><span class="sxs-lookup"><span data-stu-id="78770-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="78770-173">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="78770-173">Click OK.</span></span>
10. <span data-ttu-id="78770-174">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="78770-174">Click OK.</span></span>
11. <span data-ttu-id="78770-175">Eikite į Pardavimas ir rinkodara > Pardavimo pasiūlymai > Visi pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="78770-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="78770-176">Patikrinkite, kad pasiūlymai buvo sukurti visiems klientams, nurodytiems masinio atnaujinimo procedūros metu, remiantis pasirinktu šablonu.</span><span class="sxs-lookup"><span data-stu-id="78770-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

