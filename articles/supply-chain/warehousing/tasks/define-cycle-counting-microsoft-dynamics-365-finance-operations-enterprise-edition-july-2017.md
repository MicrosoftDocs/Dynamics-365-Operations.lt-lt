--- 
title: "Apibrėžti ciklo skaičiavimą "
description: "Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f9cdb0a7de0199363279c53e817c98085b31fe6b
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="define-cycle-counting"></a><span data-ttu-id="25868-103">Apibrėžti ciklo skaičiavimą </span><span class="sxs-lookup"><span data-stu-id="25868-103">Define cycle counting</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25868-104">Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes.</span><span class="sxs-lookup"><span data-stu-id="25868-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="25868-105">Šios užduoties įraše rodoma, kaip nustatyti numatytąjį skaičiavimo darbo prioritetą, įgalinti mobiliojo įrenginio meniu elementą, kad būtų apdorojamos išrinkimo ir skaičiavimo operacijos, įgalinti skaičiavimo ribinės vertės paleidiklį, kai vieta taps tuščia ir įgalinti konkrečiame sandėlyje esančios konkrečios prekės ciklo skaičiavimo planą.</span><span class="sxs-lookup"><span data-stu-id="25868-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="25868-106">Šias užduotis paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="25868-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="25868-107">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="25868-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="25868-108">Skaičiavimo darbo prioriteto nustatymas</span><span class="sxs-lookup"><span data-stu-id="25868-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="25868-109">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="25868-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="25868-110">Spustelėkite skirtuką Ciklo skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="25868-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="25868-111">Lauke Numatytasis ciklų skaičiavimo darbo prioritetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="25868-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="25868-112">Šis veiksmas pakeičia ciklo skaičiavimo darbo prioritetą, palyginti su kitais darbo sandėlyje tipais.</span><span class="sxs-lookup"><span data-stu-id="25868-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="25868-113">Įvesdami skaičių, mažesnį negu kitiems darbo tipams, didesnį prioritetą suteikiate ciklo skaičiavimo darbui.</span><span class="sxs-lookup"><span data-stu-id="25868-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="25868-114">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25868-114">Click Save.</span></span>
5. <span data-ttu-id="25868-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25868-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="25868-116">Įgalinkite mobilųjį įrenginį</span><span class="sxs-lookup"><span data-stu-id="25868-116">Enable the mobile device</span></span>
1. <span data-ttu-id="25868-117">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="25868-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="25868-118">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25868-118">Click New.</span></span>
3. <span data-ttu-id="25868-119">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25868-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="25868-120">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25868-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="25868-121">Lauke Režimas pasirinkite „Darbas“.</span><span class="sxs-lookup"><span data-stu-id="25868-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="25868-122">Nustatykite pasirinkties Naudoti esamą darbą padėtį Taip.</span><span class="sxs-lookup"><span data-stu-id="25868-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="25868-123">Kai nustatote šią parinktį Taip, sistema ieškos esamo darbo, kuriam atlikti naudojamas mobiliojo įrenginio meniu elementas.</span><span class="sxs-lookup"><span data-stu-id="25868-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="25868-124">Lauke Nukreipė pasirinkite „Nurodomas sistemos“.</span><span class="sxs-lookup"><span data-stu-id="25868-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="25868-125">Pasirinkus „Sistemos nurodyta“, sandėlio darbuotojas bus nukreiptas atlikti atvirą darbą, apibrėžtą darbo klasėse.</span><span class="sxs-lookup"><span data-stu-id="25868-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="25868-126">(Mes sukursime šias darbo klases paskui.)</span><span class="sxs-lookup"><span data-stu-id="25868-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="25868-127">Išplėskite arba sutraukite sekciją Darbo klasės.</span><span class="sxs-lookup"><span data-stu-id="25868-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="25868-128">Dabar mes sukursime dvi darbo klases, kurios bus naudojamos su šiuo mobiliojo įrenginio meniu elementu.</span><span class="sxs-lookup"><span data-stu-id="25868-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="25868-129">Naudojant meniu elementą bus ieškoma šių darbo klasių, ir todėl vartotojui bus rodomas darbas, kurio prioritetas aukščiausias.</span><span class="sxs-lookup"><span data-stu-id="25868-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="25868-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25868-130">Click New.</span></span>
10. <span data-ttu-id="25868-131">Lauke Darbo klasės ID pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="25868-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="25868-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25868-132">Click New.</span></span>
12. <span data-ttu-id="25868-133">Lauke Darbo klasės ID pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="25868-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="25868-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25868-134">Click Save.</span></span>
14. <span data-ttu-id="25868-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25868-135">Close the page.</span></span>
15. <span data-ttu-id="25868-136">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu.</span><span class="sxs-lookup"><span data-stu-id="25868-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="25868-137">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="25868-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="25868-138">Medyje pasirinkite meniu elementą, kurį ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="25868-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="25868-139">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="25868-139">Click Edit.</span></span>
19. <span data-ttu-id="25868-140">Norėdami įtraukti meniu elementą į meniu, spustelėkite rodyklę.</span><span class="sxs-lookup"><span data-stu-id="25868-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="25868-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25868-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="25868-142">Sukurkite skaičiavimo ribinę vertę</span><span class="sxs-lookup"><span data-stu-id="25868-142">Create a counting threshold</span></span>
1. <span data-ttu-id="25868-143">Pasirinkite Sandėlio valdymas > Nustatymai > Ciklo skaičiavimas > Ciklų skaičiavimo ribinės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="25868-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="25868-144">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25868-144">Click New.</span></span>
3. <span data-ttu-id="25868-145">Lauke Ciklo skaičiavimo ribinės vertės ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="25868-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="25868-146">Nustatykite pasirinkties Apdoroti ciklo skaičiavimą nedelsiant padėtį Taip.</span><span class="sxs-lookup"><span data-stu-id="25868-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="25868-147">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25868-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="25868-148">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25868-148">Click Save.</span></span>
7. <span data-ttu-id="25868-149">Spustelėkite Pasirinkti vietas.</span><span class="sxs-lookup"><span data-stu-id="25868-149">Click Select locations.</span></span>
8. <span data-ttu-id="25868-150">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25868-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="25868-151">Lauke Kriterijai pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="25868-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="25868-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="25868-152">Click OK.</span></span>
11. <span data-ttu-id="25868-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25868-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="25868-154">Sukurkite ciklų skaičiavimo planą</span><span class="sxs-lookup"><span data-stu-id="25868-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="25868-155">Pasirinkite Sandėlio valdymas > Nustatymai > Ciklo skaičiavimas > Ciklų skaičiavimo planai.</span><span class="sxs-lookup"><span data-stu-id="25868-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="25868-156">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25868-156">Click New.</span></span>
3. <span data-ttu-id="25868-157">Lauke Ciklo skaičiavimo plano ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="25868-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="25868-158">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25868-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="25868-159">Lauke Maksimalus ciklų skaičiavimo skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="25868-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="25868-160">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25868-160">Click Save.</span></span>
7. <span data-ttu-id="25868-161">Spustelėkite Pasirinkti vietas.</span><span class="sxs-lookup"><span data-stu-id="25868-161">Click Select locations.</span></span>
8. <span data-ttu-id="25868-162">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25868-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="25868-163">Lauke Kriterijai pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="25868-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="25868-164">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="25868-164">Click OK.</span></span>
11. <span data-ttu-id="25868-165">Lauke Dienos tarp ciklo skaičiavimų įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="25868-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="25868-166">Pavyzdžiui, jei lauke Dienos tarp ciklo skaičiavimų nustatyta 5, ciklo skaičiavimo darbas bus sukuriamas kas penkias dienas.</span><span class="sxs-lookup"><span data-stu-id="25868-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="25868-167">Tačiau jei ciklo skaičiavimo darbas apdorojamas trečią dieną, kitas ciklo skaičiavimo darbas bus sukurtas po penkių dienų nuo paskutinio ciklo skaičiavimo, 8 dieną.</span><span class="sxs-lookup"><span data-stu-id="25868-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="25868-168">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25868-168">Click Save.</span></span>
13. <span data-ttu-id="25868-169">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25868-169">Click New.</span></span>
14. <span data-ttu-id="25868-170">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="25868-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="25868-171">Rūšiuojama yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="25868-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="25868-172">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="25868-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="25868-173">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25868-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="25868-174">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25868-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="25868-175">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="25868-175">Click Save.</span></span>
18. <span data-ttu-id="25868-176">Spustelėkite Apibrėžti produkto užklausą.</span><span class="sxs-lookup"><span data-stu-id="25868-176">Click Define product query.</span></span>
19. <span data-ttu-id="25868-177">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25868-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="25868-178">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25868-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="25868-179">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="25868-179">Click OK.</span></span>
22. <span data-ttu-id="25868-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25868-180">Close the page.</span></span>


