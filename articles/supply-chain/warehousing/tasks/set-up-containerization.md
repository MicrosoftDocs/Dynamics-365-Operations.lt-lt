---
title: Nustatyti krovimą į konteinerius
description: Šia procedūra aprašoma, kaip automatizuoti krovinių krovimą į konteinerius modulyje Sandėlio valdymas.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "321690"
---
# <a name="set-up-containerization"></a><span data-ttu-id="04603-103">Nustatyti krovimą į konteinerius</span><span class="sxs-lookup"><span data-stu-id="04603-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04603-104">Šia procedūra aprašoma, kaip automatizuoti krovinių krovimą į konteinerius modulyje Sandėlio valdymas.</span><span class="sxs-lookup"><span data-stu-id="04603-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="04603-105">Vykstant automatizuoto krovimo į konteinerius procesui, apdorojant bangą siuntoms sukuriami konteineriai ir paėmimo darbas, o darbo eilutes galima išskaidyti į kiekius, telpančius į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="04603-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="04603-106">Taip sandėlio darbininkams lengviau prekes paimti tiesiai į pasirinktą konteinerį.</span><span class="sxs-lookup"><span data-stu-id="04603-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="04603-107">Palyginti su rankinio pakavimo procesu, tokias užduotis kaip konteinerių kūrimas, prekių priskyrimas ir konteinerių uždarymas automatizuoja sistema.</span><span class="sxs-lookup"><span data-stu-id="04603-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="04603-108">Atliekant šią procedūrą naudojama demonstracinė įmonė USMF, o ją atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="04603-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="04603-109">Bangos šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="04603-109">Set up a wave template</span></span>
1. <span data-ttu-id="04603-110">Pasirinkite Sandėlio valdymas > Nustatymas > Bangos > Bangų šablonai.</span><span class="sxs-lookup"><span data-stu-id="04603-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="04603-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-111">Click New.</span></span>
3. <span data-ttu-id="04603-112">Lauke Bangos šablono pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="04603-113">Lauke Bangos šablono aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="04603-114">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="04603-115">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="04603-116">Išplėskite dalį Būdai.</span><span class="sxs-lookup"><span data-stu-id="04603-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="04603-117">Srityje Pasirinkti metodai pateikiami pasirinkto bangos šablono tipo metodai.</span><span class="sxs-lookup"><span data-stu-id="04603-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="04603-118">Bangos šablone turi būti krovimo į konteinerius metodas.</span><span class="sxs-lookup"><span data-stu-id="04603-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="04603-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="04603-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="04603-120">Lauke Bangos veiksmo kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="04603-121">Įveskite įtraukto metodo bangos veiksmo kodą – tai gali būti bet koks kodas.</span><span class="sxs-lookup"><span data-stu-id="04603-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="04603-122">Įtraukti metodą galimą keletą kartų ir galima priskirti skirtingus bangos veiksmų kodus.</span><span class="sxs-lookup"><span data-stu-id="04603-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="04603-123">Norėdami tai padaryti, puslapyje Bangos apdorojimo metodai prie šio metodo pasirinkite Galima kartoti.</span><span class="sxs-lookup"><span data-stu-id="04603-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="04603-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="04603-124">Click Save.</span></span>
11. <span data-ttu-id="04603-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="04603-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="04603-126">Konteinerio tipo nustatymas</span><span class="sxs-lookup"><span data-stu-id="04603-126">Set up a container type</span></span>
1. <span data-ttu-id="04603-127">Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių tipai.</span><span class="sxs-lookup"><span data-stu-id="04603-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="04603-128">Savo konteinerius galite apibrėžti puslapyje Konteinerių tipai.</span><span class="sxs-lookup"><span data-stu-id="04603-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="04603-129">Galite sukonfigūruoti faktines konteinerių dimensijas – taros svorį, didžiausią svorį, didžiausią tūrį, ilgį, plotį ir aukštį.</span><span class="sxs-lookup"><span data-stu-id="04603-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="04603-130">Šiame pavyzdyje turime tris skirtingus dėžių dydžius.</span><span class="sxs-lookup"><span data-stu-id="04603-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="04603-131">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-131">Click New.</span></span>
3. <span data-ttu-id="04603-132">Lauke Konteinerio tipo kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="04603-133">Lauke „Taros svoris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="04603-134">Lauke Didžiausias svoris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="04603-135">Lauke „Tūris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="04603-136">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="04603-137">Lauke Plotis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="04603-138">Lauke Aukštis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="04603-139">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="04603-140">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="04603-140">Click Save.</span></span>
12. <span data-ttu-id="04603-141">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-141">Click New.</span></span>
13. <span data-ttu-id="04603-142">Lauke Konteinerio tipo kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="04603-143">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="04603-144">Lauke „Taros svoris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="04603-145">Lauke Didžiausias svoris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="04603-146">Lauke „Tūris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="04603-147">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="04603-148">Lauke Plotis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="04603-149">Lauke Aukštis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="04603-150">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="04603-150">Click Save.</span></span>
22. <span data-ttu-id="04603-151">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-151">Click New.</span></span>
23. <span data-ttu-id="04603-152">Lauke Konteinerio tipo kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="04603-153">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="04603-154">Lauke „Taros svoris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="04603-155">Lauke Didžiausias svoris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="04603-156">Lauke „Tūris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="04603-157">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="04603-158">Lauke Plotis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="04603-159">Lauke Aukštis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="04603-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="04603-160">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="04603-160">Click Save.</span></span>
32. <span data-ttu-id="04603-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="04603-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="04603-162">Konteinerių grupės nustatymas</span><span class="sxs-lookup"><span data-stu-id="04603-162">Set up a container group</span></span>
1. <span data-ttu-id="04603-163">Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių grupės.</span><span class="sxs-lookup"><span data-stu-id="04603-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="04603-164">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-164">Click New.</span></span>
    * <span data-ttu-id="04603-165">Galite nustatyti logines konteinerių tipų grupes.</span><span class="sxs-lookup"><span data-stu-id="04603-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="04603-166">Kiekvienai grupei galite nurodyti seką, kuria bus pakuojami konteineriai, ir konteinerių užpildymo procentą. Naudojami prekės matmenų dydžiai siekiant nustatyti, ar ji tilps konteineryje.</span><span class="sxs-lookup"><span data-stu-id="04603-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="04603-167">Naudojamas konteineris, artimiausias prekės dydžio matmenims.</span><span class="sxs-lookup"><span data-stu-id="04603-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="04603-168">Jei grupėje turite kelis konteinerių tipus, rekomenduojame išdėstyti seką pagal dydį, kad didžiausias konteineris sekoje būtų pirmas (Nr. 1), o mažiausias – paskutinis.</span><span class="sxs-lookup"><span data-stu-id="04603-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="04603-169">Lauke Konteinerių grupės ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="04603-170">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="04603-171">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-171">Click New.</span></span>
6. <span data-ttu-id="04603-172">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="04603-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="04603-173">Lauke Konteinerio tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="04603-174">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-174">Click New.</span></span>
9. <span data-ttu-id="04603-175">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="04603-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="04603-176">Lauke Konteinerio tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="04603-177">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-177">Click New.</span></span>
12. <span data-ttu-id="04603-178">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="04603-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="04603-179">Lauke Konteinerio tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="04603-180">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="04603-180">Click Save.</span></span>
15. <span data-ttu-id="04603-181">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="04603-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="04603-182">Konteinerio kūrimo šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="04603-182">Set up a container build template</span></span>
1. <span data-ttu-id="04603-183">Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių kūrimo šablonai.</span><span class="sxs-lookup"><span data-stu-id="04603-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="04603-184">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-184">Click New.</span></span>
    * <span data-ttu-id="04603-185">Konteinerio kūrimo šablonas priklauso nuo to, kuris iš krovimo į konteinerius procesų atliekamas.</span><span class="sxs-lookup"><span data-stu-id="04603-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="04603-186">Kiekvienu konteinerio kūrimo šablonu apibrėžiamas vienas krovimo į konteinerius procesas, kurį naudos bangos šablonas.</span><span class="sxs-lookup"><span data-stu-id="04603-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="04603-187">Parinktimi Redaguoti užklausą galima apibrėžti sąlygas, kuriomis pasirinktas šablonas bus apdorojamas.</span><span class="sxs-lookup"><span data-stu-id="04603-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="04603-188">Pavyzdžiui, galbūt krovimo į konteinerius procesą norėsite vykdyti tik su konkrečiais klientais, produktais ar sandėliais, arba į šabloną galite įtraukti atitinkamų užklausos intervalų.</span><span class="sxs-lookup"><span data-stu-id="04603-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="04603-189">Lauku Bangos veiksmo kodas nustatoma, kaip konteinerio kūrimo šablonas susietas su bangos šablono veiksmais.</span><span class="sxs-lookup"><span data-stu-id="04603-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="04603-190">Kai vykdoma banga, ja nustatoma, kuris konteinerio kūrimo šablonas (-ai) naudojamas inicijuoti krovimo į konteinerius procesui.</span><span class="sxs-lookup"><span data-stu-id="04603-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="04603-191">Lauku Pagrindinis užklausos tipas nustatoma, ką pakuoti ir kuo grįsti filtro užklausą.</span><span class="sxs-lookup"><span data-stu-id="04603-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="04603-192">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="04603-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="04603-193">Lauke Konteinerio šablono ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="04603-194">Lauke Konteinerių grupės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="04603-195">Lauke Bangos veiksmo kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="04603-196">Pažymėkite žymės langelį Leisti skaidyti paėmimus.</span><span class="sxs-lookup"><span data-stu-id="04603-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="04603-197">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="04603-197">Click Save.</span></span>
9. <span data-ttu-id="04603-198">Spustelėkite Konteinerių maišymo apribojimai.</span><span class="sxs-lookup"><span data-stu-id="04603-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="04603-199">Maišymo logikos skaidymais galima nustatyti paskirstymo eilučių pakavimo konteineriuose taisykles.</span><span class="sxs-lookup"><span data-stu-id="04603-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="04603-200">Pavyzdžiui, jei įtrauksite lauką Prekės numeris, prekes priskiriant konteineriams ir esant naujam prekės numeriui, bus sukurtas naujas konteineris.</span><span class="sxs-lookup"><span data-stu-id="04603-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="04603-201">Taip darbininkai tame pačiame konteineryje nesupakuos paskirstymo eilučių dviem skirtingiems klientams.</span><span class="sxs-lookup"><span data-stu-id="04603-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="04603-202">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="04603-202">Click New.</span></span>
11. <span data-ttu-id="04603-203">Lauke Lentelė pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="04603-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="04603-204">Lauke Laukų pasirinkimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="04603-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="04603-205">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="04603-205">Click OK.</span></span>

