---
title: Kompensavimo tinklelių nustatymas
description: Kompensavimo tinkleliai naudojami nustatyti ir prižiūrėti pastoviųjų atlyginimo dalių planų mokėjimo struktūras.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d5ada0817dd73caad38bb2e50302869857c71d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419704"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="b6d6b-103">Kompensavimo tinklelių nustatymas</span><span class="sxs-lookup"><span data-stu-id="b6d6b-103">Set up compensation grids</span></span>

<span data-ttu-id="b6d6b-104">Kompensavimo tinkleliai naudojami nustatyti ir prižiūrėti pastoviųjų atlyginimo dalių planų mokėjimo struktūras.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="b6d6b-105">Kompensacijos tinklelius galima bendrai naudoti keliems planams arba nukopijuoti kuriant naują kompensavimo planą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="b6d6b-106">Prieš kuriant kompensacijos tinklelį, Lygiai ir Nuorodos taškai turi būti nustatyti.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="b6d6b-107">Šiame pavyzdyje bus sukurtas naujas kompensacijos tinklelio Klasės tipas naudojant demonstracinius duomenis Lygiams ir Nuorodos taškams.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="b6d6b-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="b6d6b-109">Nustatyti informaciją apie kompensacijos tinklelį</span><span class="sxs-lookup"><span data-stu-id="b6d6b-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="b6d6b-110">Pasirinkite Personalas > Kompensacija > Pastovioji atlyginimo dalis > Kompensacijos tinkleliai.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="b6d6b-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-111">Click New.</span></span>
3. <span data-ttu-id="b6d6b-112">Lauke Tinklelis įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="b6d6b-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b6d6b-114">Lauke „Tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="b6d6b-115">Lauke Nuorodos nustatymas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="b6d6b-116">Lauke Valiuta įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="b6d6b-117">Lauke Valiuta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="b6d6b-118">Lauke Įsigaliojimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="b6d6b-119">Įtraukti lygius į kompensacijos struktūrą</span><span class="sxs-lookup"><span data-stu-id="b6d6b-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="b6d6b-120">Spustelėkite Kompensacijos struktūra.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="b6d6b-121">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b6d6b-122">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="b6d6b-123">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-123">Click New.</span></span>
5. <span data-ttu-id="b6d6b-124">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b6d6b-125">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="b6d6b-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-126">Click New.</span></span>
8. <span data-ttu-id="b6d6b-127">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="b6d6b-128">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="b6d6b-129">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-129">Click New.</span></span>
11. <span data-ttu-id="b6d6b-130">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="b6d6b-131">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="b6d6b-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-132">Click New.</span></span>
14. <span data-ttu-id="b6d6b-133">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="b6d6b-134">Lauke Lygis įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="b6d6b-135">Užpildyti kompensacijos struktūrą vertėmis</span><span class="sxs-lookup"><span data-stu-id="b6d6b-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="b6d6b-136">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b6d6b-137">Šiuo momentu kompensacijų vertes galima įvesti rankiniu būdu į kiekvieną lentelės lauką arba galima naudoti Masinio keitimo funkciją norint lengvai užpildyti kelis laukus ir atlikti pagrindinius skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="b6d6b-138">Spustelėkite Masinis keitimas.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-138">Click Mass change.</span></span>
    * <span data-ttu-id="b6d6b-139">Šiam tinkleliui pirmiausia pritaikysime pirmojo lygio vidurio taško vertę visuose lentelės laukuose.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="b6d6b-140">Tai bus kompensavimo matricos pagrindas.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="b6d6b-141">Lauke Koregavimo tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="b6d6b-142">Lauke Koregavimo suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="b6d6b-143">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="b6d6b-144">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="b6d6b-145">Dabar naudojame masinio keitimo funkciją sumai padidinti kiekviename tolesniame lygyje pagal tam tikrą procentą arba sumą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="b6d6b-146">Šiame pavyzdyje kiekvienas lygis turės 12,5 % paplitimą tarp jų vidurio taškų.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="b6d6b-147">Lauke Koregavimo tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="b6d6b-148">Lauke Koregavimo suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="b6d6b-149">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b6d6b-150">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="b6d6b-151">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b6d6b-152">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="b6d6b-153">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="b6d6b-154">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b6d6b-155">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="b6d6b-156">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="b6d6b-157">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="b6d6b-158">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="b6d6b-159">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="b6d6b-160">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="b6d6b-161">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="b6d6b-162">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="b6d6b-163">Dabar naudosime masinio keitimo funkciją kiekvieno lygio minimaliam ir maksimaliam nuorodos taškams koreguoti.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="b6d6b-164">Šiame pavyzdyje naudosime 50 % paplitimą, kad Minimalus atskaitos taškas būtų pakoreguotas -20 %, o Maksimalus – pakoreguotas +20 %.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="b6d6b-165">Lauke Koregavimo suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="b6d6b-166">Lauke Nuorodos taškas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="b6d6b-167">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="b6d6b-168">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="b6d6b-169">Lauke Koregavimo suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="b6d6b-170">Lauke Nuorodos taškas įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="b6d6b-171">Pažymėkite arba atžymėkite visas sąrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="b6d6b-172">Spustelėkite Taikyti tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="b6d6b-172">Click Apply to grid.</span></span>

