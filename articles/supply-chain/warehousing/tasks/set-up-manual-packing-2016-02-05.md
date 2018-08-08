--- 
title: "Neautomatinio pakavimo nustatymas (2016 m. vasario ir gegužės mėn.)"
description: "Atliekant pakavimo procesą, produktus galima tikrinti ir pakuoti į konteinerius."
author: ShylaThompson
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 7e776a08ec2adc48b77c86c16e1f291e524a8d00
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="97aed-103">Neautomatinio pakavimo nustatymas (2016 m. vasario ir gegužės mėn.)</span><span class="sxs-lookup"><span data-stu-id="97aed-103">Set up manual packing (February & May 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97aed-104">Atliekant pakavimo procesą, produktus galima tikrinti ir pakuoti į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="97aed-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="97aed-105">Atlikdami ši procesą sandėlio darbininkai produktus paima iš saugojimo vietų ir perkelia į pakavimo stotį, kurioje jie patikrina prekių kiekį ir tipus bei jas priskiria į atitinkamus konteinerius.</span><span class="sxs-lookup"><span data-stu-id="97aed-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="97aed-106">Kai konteineris yra visiškai supakuotas, jie jį gali uždaryti ir perkelti į pakrovimo rampas, ir produktus galima siųsti.</span><span class="sxs-lookup"><span data-stu-id="97aed-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="97aed-107">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="97aed-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="97aed-108">Nustatyti vietų šablonus</span><span class="sxs-lookup"><span data-stu-id="97aed-108">Set up location profiles</span></span>
1. <span data-ttu-id="97aed-109">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlis > Vietos profiliai.</span><span class="sxs-lookup"><span data-stu-id="97aed-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="97aed-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="97aed-110">Click New.</span></span>
    * <span data-ttu-id="97aed-111">Vietos profilis naudojamas su pakavimo stotimis ir jame pateikiama vietos informacija ir taisyklės.</span><span class="sxs-lookup"><span data-stu-id="97aed-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="97aed-112">Lauke Vietos šablono ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="97aed-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="97aed-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="97aed-114">Lauke Vietos formatas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="97aed-115">Lauke Vietos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="97aed-116">Lauke Leisti skirtingas prekes pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="97aed-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="97aed-117">Lauke Leisti įvairias atsargų būsenas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="97aed-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="97aed-118">Lauke Nepaisyti paketo dienų taisyklių pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="97aed-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="97aed-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="97aed-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="97aed-120">Sandėlio valdymo parametrų valdymas</span><span class="sxs-lookup"><span data-stu-id="97aed-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="97aed-121">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="97aed-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="97aed-122">Spustelėkite skirtuką Pakavimas.</span><span class="sxs-lookup"><span data-stu-id="97aed-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="97aed-123">Lauke Pakavimo vietos profilio ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="97aed-124">Pasirinkite vietos profilį, kurį norite naudoti pakuodami.</span><span class="sxs-lookup"><span data-stu-id="97aed-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="97aed-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="97aed-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="97aed-126">Konteinerių tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="97aed-126">Set up container types</span></span>
1. <span data-ttu-id="97aed-127">Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių tipai.</span><span class="sxs-lookup"><span data-stu-id="97aed-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="97aed-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="97aed-128">Click New.</span></span>
    * <span data-ttu-id="97aed-129">Galite apibrėžti naudotinų konteinerių tipus.</span><span class="sxs-lookup"><span data-stu-id="97aed-129">You can define the types of containers to use.</span></span> <span data-ttu-id="97aed-130">Galite nurodyti faktines konteinerio dimensijas – taros svorį, didžiausią svorį, didžiausią tūrį, ilgį, plotį ir svorį.</span><span class="sxs-lookup"><span data-stu-id="97aed-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="97aed-131">Atributai yra pritaikyti laukai, kuriuose galite įtraukti papildomų konteinerio tipo dimensijų.</span><span class="sxs-lookup"><span data-stu-id="97aed-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="97aed-132">Lauke Konteinerio tipo kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="97aed-133">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="97aed-134">Lauke „Taros svoris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="97aed-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="97aed-135">Lauke Didžiausias svoris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="97aed-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="97aed-136">Lauke „Tūris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="97aed-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="97aed-137">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="97aed-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="97aed-138">Lauke Plotis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="97aed-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="97aed-139">Lauke Aukštis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="97aed-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="97aed-140">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="97aed-140">Click Save.</span></span>
12. <span data-ttu-id="97aed-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="97aed-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="97aed-142">Pakavimo profilių nustatymas</span><span class="sxs-lookup"><span data-stu-id="97aed-142">Set up packing profiles</span></span>
1. <span data-ttu-id="97aed-143">Pasirinkite Sandėlio valdymas > Nustatymas > Pakavimas > Pakavimo profiliai.</span><span class="sxs-lookup"><span data-stu-id="97aed-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="97aed-144">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="97aed-144">Click New.</span></span>
3. <span data-ttu-id="97aed-145">Lauke Pakavimo profilio ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="97aed-146">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="97aed-147">Lauke Konteinerio uždarymo profilio ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="97aed-148">Konteinerio uždarymo profilio ID yra neprivalomas ir jis yra numatytasis šio pakavimo profilio konteinerio uždarymo profilis.</span><span class="sxs-lookup"><span data-stu-id="97aed-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="97aed-149">Lauke Konteinerio ID režimas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="97aed-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="97aed-150">Šia parinktimi nustatoma, ar konteinerio ID bus automatiškai sugeneruotas konteinerį sukūrus, ar konteinerio ID bus sukurtas rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="97aed-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="97aed-151">Lauke Konteinerio tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="97aed-152">Konteinerio tipas pagal numatytuosius parametrus bus naudojamas kuriant naują konteinerį.</span><span class="sxs-lookup"><span data-stu-id="97aed-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="97aed-153">Pasirinkite žymės langelį Automatiškai kurti konteinerį uždarant konteinerį.</span><span class="sxs-lookup"><span data-stu-id="97aed-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="97aed-154">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="97aed-154">Click Save.</span></span>
10. <span data-ttu-id="97aed-155">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="97aed-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="97aed-156">Konteinerių uždarymo profilių nustatymas</span><span class="sxs-lookup"><span data-stu-id="97aed-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="97aed-157">Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių uždarymo profiliai.</span><span class="sxs-lookup"><span data-stu-id="97aed-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="97aed-158">Konteinerių uždarymo profiliais apibrėžiama, kas vyksta konteinerį uždarius.</span><span class="sxs-lookup"><span data-stu-id="97aed-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="97aed-159">Galite nustatyti kelis konteinerių uždarymo profilius.</span><span class="sxs-lookup"><span data-stu-id="97aed-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="97aed-160">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="97aed-160">Click New.</span></span>
3. <span data-ttu-id="97aed-161">Lauke Konteinerio uždarymo profilio ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="97aed-162">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="97aed-163">Lauke Deklaracija pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="97aed-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="97aed-164">Nurodykite, ar deklaruojama bus uždarant konteinerius, ar patvirtinant siuntą.</span><span class="sxs-lookup"><span data-stu-id="97aed-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="97aed-165">Atkreipkite dėmesį, kad, norint deklaruoti, reikalingas modulis Transportavimo valdymas.</span><span class="sxs-lookup"><span data-stu-id="97aed-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="97aed-166">Kad deklaravimas veiktų, jį reikia įdiegti transportavimo mechanizmuose.</span><span class="sxs-lookup"><span data-stu-id="97aed-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="97aed-167">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="97aed-168">Lauke Galutinės siuntos numatytoji vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="97aed-169">Tai bus vieta, į kurią produktai bus perkelti uždarius konteinerius.</span><span class="sxs-lookup"><span data-stu-id="97aed-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="97aed-170">Sandėlio parametruose turi būti apibrėžtas šios vietos profilis.</span><span class="sxs-lookup"><span data-stu-id="97aed-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="97aed-171">Lauke Svorio vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="97aed-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="97aed-172">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="97aed-172">Click Save.</span></span>


