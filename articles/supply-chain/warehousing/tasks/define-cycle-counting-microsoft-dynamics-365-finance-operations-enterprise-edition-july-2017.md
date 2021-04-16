---
title: Apibrėžti ciklo skaičiavimą
description: Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes.
author: MarkusFogelberg
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 995212dd40f8665da64ca0bf8e1c878002778904
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830959"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="d101f-103">Apibrėžti ciklo skaičiavimą</span><span class="sxs-lookup"><span data-stu-id="d101f-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d101f-104">Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes.</span><span class="sxs-lookup"><span data-stu-id="d101f-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="d101f-105">Šios užduoties įraše rodoma, kaip nustatyti numatytąjį skaičiavimo darbo prioritetą, įgalinti mobiliojo įrenginio meniu elementą, kad būtų apdorojamos išrinkimo ir skaičiavimo operacijos, įgalinti skaičiavimo ribinės vertės paleidiklį, kai vieta taps tuščia ir įgalinti konkrečiame sandėlyje esančios konkrečios prekės ciklo skaičiavimo planą.</span><span class="sxs-lookup"><span data-stu-id="d101f-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="d101f-106">Šias užduotis paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="d101f-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="d101f-107">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="d101f-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="d101f-108">Skaičiavimo darbo prioriteto nustatymas</span><span class="sxs-lookup"><span data-stu-id="d101f-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="d101f-109">Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Sandėlio valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d101f-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="d101f-110">Spustelėkite skirtuką **Ciklo skaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="d101f-111">Lauke **Numatytasis ciklo skaičiavimo darbo prioritetas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d101f-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="d101f-112">Šis veiksmas pakeičia ciklo skaičiavimo darbo prioritetą, palyginti su kitais darbo sandėlyje tipais.</span><span class="sxs-lookup"><span data-stu-id="d101f-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="d101f-113">Įvesdami skaičių, mažesnį negu kitiems darbo tipams, didesnį prioritetą suteikiate ciklo skaičiavimo darbui.</span><span class="sxs-lookup"><span data-stu-id="d101f-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="d101f-114">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d101f-114">Click **Save**.</span></span>
5. <span data-ttu-id="d101f-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d101f-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="d101f-116">Įgalinkite mobilųjį įrenginį</span><span class="sxs-lookup"><span data-stu-id="d101f-116">Enable the mobile device</span></span>
1. <span data-ttu-id="d101f-117">Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="d101f-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="d101f-118">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-118">Click **New**.</span></span>
3. <span data-ttu-id="d101f-119">Lauke **Meniu elemento pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="d101f-120">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="d101f-121">Lauke **Režimas** pasirinkite Darbas.</span><span class="sxs-lookup"><span data-stu-id="d101f-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="d101f-122">Nustatykite parinktį **Naudoti esamą darbą** į Taip.</span><span class="sxs-lookup"><span data-stu-id="d101f-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="d101f-123">Kai nustatote šią parinktį Taip, sistema ieškos esamo darbo, kuriam atlikti naudojamas mobiliojo įrenginio meniu elementas.</span><span class="sxs-lookup"><span data-stu-id="d101f-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="d101f-124">Lauke **Nurodyta pagal** pasirinkite Sistemos nurodyta.</span><span class="sxs-lookup"><span data-stu-id="d101f-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="d101f-125">Pasirinkus „Sistemos nurodyta“, sandėlio darbuotojas bus nukreiptas atlikti atvirą darbą, apibrėžtą darbo klasėse.</span><span class="sxs-lookup"><span data-stu-id="d101f-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="d101f-126">(Mes sukursime šias darbo klases paskui.)</span><span class="sxs-lookup"><span data-stu-id="d101f-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="d101f-127">Išplėskite parinkties **Darbo klasės** „fastTab“.</span><span class="sxs-lookup"><span data-stu-id="d101f-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="d101f-128">Dabar mes sukursime dvi darbo klases, kurios bus naudojamos su šiuo mobiliojo įrenginio meniu elementu.</span><span class="sxs-lookup"><span data-stu-id="d101f-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="d101f-129">Naudojant meniu elementą bus ieškoma šių darbo klasių, ir todėl vartotojui bus rodomas darbas, kurio prioritetas aukščiausias.</span><span class="sxs-lookup"><span data-stu-id="d101f-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="d101f-130">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-130">Click **New**.</span></span>
10. <span data-ttu-id="d101f-131">Lauke **Darbo klasės ID** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="d101f-132">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-132">Click **New**.</span></span>
12. <span data-ttu-id="d101f-133">Lauke **Darbo klasės ID** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="d101f-134">Parinktyje **Veiksmų sritis** spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d101f-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="d101f-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d101f-135">Close the page.</span></span>
15. <span data-ttu-id="d101f-136">Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu**.</span><span class="sxs-lookup"><span data-stu-id="d101f-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="d101f-137">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d101f-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="d101f-138">Medyje pasirinkite meniu elementą, kurį ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="d101f-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="d101f-139">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="d101f-139">Click **Edit**.</span></span>
19. <span data-ttu-id="d101f-140">Norėdami įtraukti meniu elementą į meniu, spustelėkite rodyklę.</span><span class="sxs-lookup"><span data-stu-id="d101f-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="d101f-141">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d101f-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="d101f-142">Sukurkite skaičiavimo ribinę vertę</span><span class="sxs-lookup"><span data-stu-id="d101f-142">Create a counting threshold</span></span>
1. <span data-ttu-id="d101f-143">Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Ciklo skaičiavimas > Ciklo skaičiavimo ribinės vertės**.</span><span class="sxs-lookup"><span data-stu-id="d101f-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="d101f-144">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-144">Click **New**.</span></span>
3. <span data-ttu-id="d101f-145">Lauke **Ciklo skaičiavimo ribinės vertės ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="d101f-146">Nustatykite parinktį **Nedelsiant apdoroti ciklo skaičiavimą** į Taip.</span><span class="sxs-lookup"><span data-stu-id="d101f-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="d101f-147">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="d101f-148">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d101f-148">Click **Save**.</span></span>
7. <span data-ttu-id="d101f-149">Spustelėkite **Pasirinkti vietas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="d101f-150">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d101f-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d101f-151">Lauke **Kriterijai** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="d101f-152">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d101f-152">Click **OK**.</span></span>
11. <span data-ttu-id="d101f-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d101f-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="d101f-154">Sukurkite ciklų skaičiavimo planą</span><span class="sxs-lookup"><span data-stu-id="d101f-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="d101f-155">Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Ciklo skaičiavimas > Ciklo skaičiavimo planai**.</span><span class="sxs-lookup"><span data-stu-id="d101f-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="d101f-156">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-156">Click **New**.</span></span>
3. <span data-ttu-id="d101f-157">Lauke **Ciklo skaičiavimo plano ID** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="d101f-158">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="d101f-159">Lauke **Maksimalus ciklo skaičiavimų skaičius** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d101f-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="d101f-160">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d101f-160">Click **Save**.</span></span>
7. <span data-ttu-id="d101f-161">Spustelėkite **Pasirinkti vietas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="d101f-162">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d101f-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d101f-163">Lauke **Kriterijai** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="d101f-164">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d101f-164">Click **OK**.</span></span>
11. <span data-ttu-id="d101f-165">Lauke **Dienos tarp ciklo skaičiavimų** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d101f-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="d101f-166">Pavyzdžiui, jei lauke **Dienos tarp ciklo skaičiavimų** nustatysite 5, ciklo skaičiavimo darbas bus sukurtas kas penkias dienas.</span><span class="sxs-lookup"><span data-stu-id="d101f-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="d101f-167">Tačiau jei ciklo skaičiavimo darbas apdorojamas trečią dieną, kitas ciklo skaičiavimo darbas bus sukurtas po penkių dienų nuo paskutinio ciklo skaičiavimo, 8 dieną.</span><span class="sxs-lookup"><span data-stu-id="d101f-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="d101f-168">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d101f-168">Click **Save**.</span></span>
13. <span data-ttu-id="d101f-169">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d101f-169">Click **New**.</span></span>
14. <span data-ttu-id="d101f-170">Lauke **Sekos skaičius** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d101f-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="d101f-171">Rūšiuojama yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="d101f-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="d101f-172">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="d101f-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="d101f-173">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d101f-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="d101f-174">Lauke **Aprašo laukas** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="d101f-175">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d101f-175">Click **Save**.</span></span>
18. <span data-ttu-id="d101f-176">Spustelėkite užklausą **Apibrėžti produktą**.</span><span class="sxs-lookup"><span data-stu-id="d101f-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="d101f-177">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d101f-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="d101f-178">Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d101f-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="d101f-179">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d101f-179">Click **OK**.</span></span>
22. <span data-ttu-id="d101f-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d101f-180">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]