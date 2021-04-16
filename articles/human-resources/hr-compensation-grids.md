---
title: Kompensavimo tinklelių nustatymas
description: Kompensavimo tinkleliai naudojami nustatyti ir prižiūrėti pastoviųjų atlyginimo dalių planų mokėjimo struktūras.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c393dc3393b5331b5594e39254ffe208ff439bc7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800956"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="ccefe-103">Kompensavimo tinklelių nustatymas</span><span class="sxs-lookup"><span data-stu-id="ccefe-103">Set up compensation grids</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ccefe-104">Kompensavimo tinkleliai naudojami nustatyti ir prižiūrėti pastoviųjų atlyginimo dalių planų mokėjimo struktūras.</span><span class="sxs-lookup"><span data-stu-id="ccefe-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="ccefe-105">Kompensacijos tinklelius galima bendrai naudoti keliems planams arba nukopijuoti kuriant naują kompensavimo planą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="ccefe-106">Prieš kuriant kompensacijos tinklelį, Lygiai ir Nuorodos taškai turi būti nustatyti.</span><span class="sxs-lookup"><span data-stu-id="ccefe-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="ccefe-107">Šiame pavyzdyje bus sukurtas naujas kompensacijos tinklelio Klasės tipas naudojant demonstracinius duomenis Lygiams ir Nuorodos taškams.</span><span class="sxs-lookup"><span data-stu-id="ccefe-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="ccefe-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="ccefe-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="ccefe-109">Nustatyti informaciją apie kompensacijos tinklelį</span><span class="sxs-lookup"><span data-stu-id="ccefe-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="ccefe-110">Pasirinkite Personalas > Kompensacija > Pastovioji atlyginimo dalis > Kompensacijos tinkleliai.</span><span class="sxs-lookup"><span data-stu-id="ccefe-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="ccefe-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ccefe-111">Click New.</span></span>
3. <span data-ttu-id="ccefe-112">Lauke Tinklelis įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="ccefe-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ccefe-114">Lauke „Tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="ccefe-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="ccefe-115">Lauke Nuorodos nustatymas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="ccefe-116">Lauke Valiuta įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="ccefe-117">Lauke Valiuta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="ccefe-118">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="ccefe-119">Įtraukti lygius į kompensacijos struktūrą</span><span class="sxs-lookup"><span data-stu-id="ccefe-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="ccefe-120">Spustelėkite Kompensacijos struktūra.</span><span class="sxs-lookup"><span data-stu-id="ccefe-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="ccefe-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ccefe-122">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="ccefe-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ccefe-123">Click New.</span></span>
5. <span data-ttu-id="ccefe-124">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ccefe-125">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="ccefe-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ccefe-126">Click New.</span></span>
8. <span data-ttu-id="ccefe-127">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ccefe-128">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="ccefe-129">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ccefe-129">Click New.</span></span>
11. <span data-ttu-id="ccefe-130">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="ccefe-131">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="ccefe-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ccefe-132">Click New.</span></span>
14. <span data-ttu-id="ccefe-133">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="ccefe-134">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="ccefe-135">Užpildyti kompensacijos struktūrą vertėmis</span><span class="sxs-lookup"><span data-stu-id="ccefe-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="ccefe-136">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ccefe-137">Šiuo momentu kompensacijų vertes galima įvesti rankiniu būdu į kiekvieną lentelės lauką arba galima naudoti Masinio keitimo funkciją norint lengvai užpildyti kelis laukus ir atlikti pagrindinius skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="ccefe-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="ccefe-138">Spustelėkite Masinis keitimas.</span><span class="sxs-lookup"><span data-stu-id="ccefe-138">Click Mass change.</span></span>
    * <span data-ttu-id="ccefe-139">Šiam tinkleliui pirmiausia pritaikysime pirmojo lygio vidurio taško vertę visuose lentelės laukuose.</span><span class="sxs-lookup"><span data-stu-id="ccefe-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="ccefe-140">Tai bus kompensavimo matricos pagrindas.</span><span class="sxs-lookup"><span data-stu-id="ccefe-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="ccefe-141">Lauke Koregavimo tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="ccefe-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="ccefe-142">Lauke Koregavimo suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ccefe-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="ccefe-143">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="ccefe-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="ccefe-144">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="ccefe-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="ccefe-145">Dabar naudojame masinio keitimo funkciją sumai padidinti kiekviename tolesniame lygyje pagal tam tikrą procentą arba sumą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="ccefe-146">Šiame pavyzdyje kiekvienas lygis turės 12,5 % paplitimą tarp jų vidurio taškų.</span><span class="sxs-lookup"><span data-stu-id="ccefe-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="ccefe-147">Lauke Koregavimo tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="ccefe-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="ccefe-148">Lauke Koregavimo suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ccefe-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="ccefe-149">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ccefe-150">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="ccefe-151">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ccefe-152">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="ccefe-153">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="ccefe-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="ccefe-154">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ccefe-155">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="ccefe-156">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ccefe-157">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="ccefe-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="ccefe-158">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="ccefe-159">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="ccefe-160">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="ccefe-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="ccefe-161">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="ccefe-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="ccefe-162">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="ccefe-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="ccefe-163">Dabar naudosime masinio keitimo funkciją kiekvieno lygio minimaliam ir maksimaliam nuorodos taškams koreguoti.</span><span class="sxs-lookup"><span data-stu-id="ccefe-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="ccefe-164">Šiame pavyzdyje naudosime 50 % paplitimą, kad Minimalus atskaitos taškas būtų pakoreguotas -20 %, o Maksimalus – pakoreguotas +20 %.</span><span class="sxs-lookup"><span data-stu-id="ccefe-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="ccefe-165">Lauke Koregavimo suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ccefe-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="ccefe-166">Lauke Nuorodos taškas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="ccefe-167">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="ccefe-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="ccefe-168">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="ccefe-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="ccefe-169">Lauke Koregavimo suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ccefe-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="ccefe-170">Lauke Nuorodos taškas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="ccefe-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="ccefe-171">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="ccefe-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="ccefe-172">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="ccefe-172">Click Apply to grid.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]