---
title: Neautomatinio pakavimo nustatymas (2016 m. vasario ir 2016 m. gegužės mėn.)
description: Atliekant pakavimo procesą, produktus galima tikrinti ir pakuoti į konteinerius.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2843c42474fcd4afbbc2cd7753c0d06cfe467dbe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810371"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="051b1-103">Neautomatinio pakavimo nustatymas (2016 m. vasario ir 2016 m. gegužės mėn.)</span><span class="sxs-lookup"><span data-stu-id="051b1-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="051b1-104">Atliekant pakavimo procesą, produktus galima tikrinti ir pakuoti į konteinerius.</span><span class="sxs-lookup"><span data-stu-id="051b1-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="051b1-105">Atlikdami ši procesą sandėlio darbininkai produktus paima iš saugojimo vietų ir perkelia į pakavimo stotį, kurioje jie patikrina prekių kiekį ir tipus bei jas priskiria į atitinkamus konteinerius.</span><span class="sxs-lookup"><span data-stu-id="051b1-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="051b1-106">Kai konteineris yra visiškai supakuotas, jie jį gali uždaryti ir perkelti į pakrovimo rampas, ir produktus galima siųsti.</span><span class="sxs-lookup"><span data-stu-id="051b1-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="051b1-107">Šioje procedūroje naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="051b1-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="051b1-108">Ši procedūra skirta tik 2016 m. vasario ir 2016 m. gegužės „Dynamics 365 for Operations“ versijoms.</span><span class="sxs-lookup"><span data-stu-id="051b1-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="051b1-109">Nustatyti vietų šablonus</span><span class="sxs-lookup"><span data-stu-id="051b1-109">Set up location profiles</span></span>
1. <span data-ttu-id="051b1-110">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlis > Vietos profiliai.</span><span class="sxs-lookup"><span data-stu-id="051b1-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="051b1-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="051b1-111">Click New.</span></span>
    * <span data-ttu-id="051b1-112">Vietos profilis naudojamas su pakavimo stotimis ir jame pateikiama vietos informacija ir taisyklės.</span><span class="sxs-lookup"><span data-stu-id="051b1-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="051b1-113">Lauke Vietos šablono ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="051b1-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="051b1-114">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="051b1-115">Lauke Vietos formatas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="051b1-116">Lauke Vietos tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="051b1-117">Lauke Leisti skirtingas prekes pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="051b1-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="051b1-118">Lauke Leisti įvairias atsargų būsenas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="051b1-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="051b1-119">Lauke Nepaisyti paketo dienų taisyklių pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="051b1-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="051b1-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="051b1-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="051b1-121">Sandėlio valdymo parametrų valdymas</span><span class="sxs-lookup"><span data-stu-id="051b1-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="051b1-122">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="051b1-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="051b1-123">Spustelėkite skirtuką Pakavimas.</span><span class="sxs-lookup"><span data-stu-id="051b1-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="051b1-124">Lauke Pakavimo vietos profilio ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="051b1-125">Pasirinkite vietos profilį, kurį norite naudoti pakuodami.</span><span class="sxs-lookup"><span data-stu-id="051b1-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="051b1-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="051b1-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="051b1-127">Konteinerių tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="051b1-127">Set up container types</span></span>
1. <span data-ttu-id="051b1-128">Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių tipai.</span><span class="sxs-lookup"><span data-stu-id="051b1-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="051b1-129">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="051b1-129">Click New.</span></span>
    * <span data-ttu-id="051b1-130">Galite apibrėžti naudotinų konteinerių tipus.</span><span class="sxs-lookup"><span data-stu-id="051b1-130">You can define the types of containers to use.</span></span> <span data-ttu-id="051b1-131">Galite nurodyti faktines konteinerio dimensijas – taros svorį, didžiausią svorį, didžiausią tūrį, ilgį, plotį ir svorį.</span><span class="sxs-lookup"><span data-stu-id="051b1-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="051b1-132">Atributai yra pritaikyti laukai, kuriuose galite įtraukti papildomų konteinerio tipo dimensijų.</span><span class="sxs-lookup"><span data-stu-id="051b1-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="051b1-133">Lauke Konteinerio tipo kodas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="051b1-134">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="051b1-135">Lauke „Taros svoris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="051b1-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="051b1-136">Lauke Didžiausias svoris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="051b1-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="051b1-137">Lauke „Tūris“ įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="051b1-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="051b1-138">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="051b1-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="051b1-139">Lauke Plotis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="051b1-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="051b1-140">Lauke Aukštis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="051b1-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="051b1-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="051b1-141">Click Save.</span></span>
12. <span data-ttu-id="051b1-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="051b1-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="051b1-143">Pakavimo profilių nustatymas</span><span class="sxs-lookup"><span data-stu-id="051b1-143">Set up packing profiles</span></span>
1. <span data-ttu-id="051b1-144">Pasirinkite Sandėlio valdymas > Nustatymas > Pakavimas > Pakavimo profiliai.</span><span class="sxs-lookup"><span data-stu-id="051b1-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="051b1-145">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="051b1-145">Click New.</span></span>
3. <span data-ttu-id="051b1-146">Lauke Pakavimo profilio ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="051b1-147">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="051b1-148">Lauke Konteinerio uždarymo profilio ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="051b1-149">Konteinerio uždarymo profilio ID yra neprivalomas ir jis yra numatytasis šio pakavimo profilio konteinerio uždarymo profilis.</span><span class="sxs-lookup"><span data-stu-id="051b1-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="051b1-150">Lauke Konteinerio ID režimas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="051b1-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="051b1-151">Šia parinktimi nustatoma, ar konteinerio ID bus automatiškai sugeneruotas konteinerį sukūrus, ar konteinerio ID bus sukurtas rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="051b1-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="051b1-152">Lauke Konteinerio tipas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="051b1-153">Konteinerio tipas pagal numatytuosius parametrus bus naudojamas kuriant naują konteinerį.</span><span class="sxs-lookup"><span data-stu-id="051b1-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="051b1-154">Pasirinkite žymės langelį Automatiškai kurti konteinerį uždarant konteinerį.</span><span class="sxs-lookup"><span data-stu-id="051b1-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="051b1-155">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="051b1-155">Click Save.</span></span>
10. <span data-ttu-id="051b1-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="051b1-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="051b1-157">Konteinerių uždarymo profilių nustatymas</span><span class="sxs-lookup"><span data-stu-id="051b1-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="051b1-158">Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių uždarymo profiliai.</span><span class="sxs-lookup"><span data-stu-id="051b1-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="051b1-159">Konteinerių uždarymo profiliais apibrėžiama, kas vyksta konteinerį uždarius.</span><span class="sxs-lookup"><span data-stu-id="051b1-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="051b1-160">Galite nustatyti kelis konteinerių uždarymo profilius.</span><span class="sxs-lookup"><span data-stu-id="051b1-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="051b1-161">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="051b1-161">Click New.</span></span>
3. <span data-ttu-id="051b1-162">Lauke Konteinerio uždarymo profilio ID įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="051b1-163">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="051b1-164">Lauke Deklaracija pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="051b1-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="051b1-165">Nurodykite, ar deklaruojama bus uždarant konteinerius, ar patvirtinant siuntą.</span><span class="sxs-lookup"><span data-stu-id="051b1-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="051b1-166">Atkreipkite dėmesį, kad, norint deklaruoti, reikalingas modulis Transportavimo valdymas.</span><span class="sxs-lookup"><span data-stu-id="051b1-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="051b1-167">Kad deklaravimas veiktų, jį reikia įdiegti transportavimo mechanizmuose.</span><span class="sxs-lookup"><span data-stu-id="051b1-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="051b1-168">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="051b1-169">Lauke Galutinės siuntos numatytoji vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="051b1-170">Tai bus vieta, į kurią produktai bus perkelti uždarius konteinerius.</span><span class="sxs-lookup"><span data-stu-id="051b1-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="051b1-171">Sandėlio parametruose turi būti apibrėžtas šios vietos profilis.</span><span class="sxs-lookup"><span data-stu-id="051b1-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="051b1-172">Lauke Svorio vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="051b1-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="051b1-173">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="051b1-173">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]