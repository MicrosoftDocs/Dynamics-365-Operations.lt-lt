---
title: Sandėlio, kuriame veikia WMS, vietų konfigūravimas
description: Šiame vadove aprašoma, kaip konfigūruoti naujo sandėlio, kuriame veikia WMS (sandėlio, kuriame naudojami patobulinti sandėlio valdymo procesai) vietos nustatymą.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2be3c7cb33225041872e8b747ba28063f897dae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "337330"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="a9570-103">Sandėlio, kuriame veikia WMS, vietų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a9570-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9570-104">Šiame vadove aprašoma, kaip konfigūruoti naujo sandėlio, kuriame veikia WMS (sandėlio, kuriame naudojami patobulinti sandėlio valdymo procesai) vietos nustatymą.</span><span class="sxs-lookup"><span data-stu-id="a9570-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="a9570-105">Šį procesą paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="a9570-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="a9570-106">Šią vadovą galite paleisti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="a9570-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="a9570-107">Galioja išankstinė sąlyga, kad turėtumėte sukonfigūruotą bent vieną vietą.</span><span class="sxs-lookup"><span data-stu-id="a9570-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="a9570-108">Naujo sandėlio kūrimas</span><span class="sxs-lookup"><span data-stu-id="a9570-108">Create a new warehouse</span></span>
1. <span data-ttu-id="a9570-109">Eikite į Sandėliai.</span><span class="sxs-lookup"><span data-stu-id="a9570-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="a9570-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-110">Click New.</span></span>
3. <span data-ttu-id="a9570-111">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="a9570-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a9570-113">Lauke Teritorija surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="a9570-114">Išplėskite arba sutraukite sekciją Sandėlis.</span><span class="sxs-lookup"><span data-stu-id="a9570-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="a9570-115">Nustatykite parinkties Naudoti sandėlio valdymo procesus padėtį Taip.</span><span class="sxs-lookup"><span data-stu-id="a9570-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="a9570-116">Šis nustatymas leidžia vykdyti išankstinius sandėliavimo procesus, naudojant sandėlio darbą ir mobiliuosius įrenfinius.</span><span class="sxs-lookup"><span data-stu-id="a9570-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="a9570-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="a9570-118">Vietos formato nustatymas</span><span class="sxs-lookup"><span data-stu-id="a9570-118">Define a location format</span></span>
1. <span data-ttu-id="a9570-119">Eikite į Vietos formatai.</span><span class="sxs-lookup"><span data-stu-id="a9570-119">Go to Location formats.</span></span>
    * <span data-ttu-id="a9570-120">Vietų formatai yra vardų sistema, naudojama siekiant sukurti unikalius ir nuoseklius sandėlyje naudojamų skirtingoms vietos talpyklos padėtims skirtus pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="a9570-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="a9570-121">Kaip vietos formatą gali būti naudinga naudoti skyriklius, kad būtų lengviau nustatyti vietos komponentus, pavyzdžiui, perėjimo numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="a9570-122">Šiame pavyzdyje mes sukursime pavadinimą su keturiais komponentais.</span><span class="sxs-lookup"><span data-stu-id="a9570-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="a9570-123">Šie komponentai gali būti, pavyzdžiui, perėjimas, stelažas, lentyna ir talpykla.</span><span class="sxs-lookup"><span data-stu-id="a9570-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="a9570-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-124">Click New.</span></span>
3. <span data-ttu-id="a9570-125">Lauke Vietos formatas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="a9570-126">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a9570-127">Lauke Segmento aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="a9570-128">Čia aprašoma, ką nurodo vietos pavadinimo pirmasis komponentas.</span><span class="sxs-lookup"><span data-stu-id="a9570-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="a9570-129">Pavyzdžiui, tai gali būti Perėjimas.</span><span class="sxs-lookup"><span data-stu-id="a9570-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="a9570-130">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a9570-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="a9570-131">Nustatoma, kiek simbolių turi būti šioje vietos pavadinimo dalyje.</span><span class="sxs-lookup"><span data-stu-id="a9570-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="a9570-132">Atkreipkite dėmesį, iš viso pavadinime negali būti daugiau negu 10 simbolių, įskaitant skyriklius.</span><span class="sxs-lookup"><span data-stu-id="a9570-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="a9570-133">Lauke Skyriklis įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="a9570-134">Taip nurodoma, koks simbolis naudojamas tarp pirmojo ir antrojo pavadinimo komponento.</span><span class="sxs-lookup"><span data-stu-id="a9570-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="a9570-135">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-135">Click New.</span></span>
9. <span data-ttu-id="a9570-136">Lauke Segmento aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="a9570-137">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a9570-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="a9570-138">Lauke Skyriklis įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="a9570-139">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-139">Click New.</span></span>
13. <span data-ttu-id="a9570-140">Lauke Segmento aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="a9570-141">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a9570-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="a9570-142">Lauke Skyriklis įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="a9570-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-143">Click New.</span></span>
17. <span data-ttu-id="a9570-144">Lauke Segmento aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="a9570-145">Lauke Ilgis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a9570-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="a9570-146">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a9570-146">Click Save.</span></span>
20. <span data-ttu-id="a9570-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="a9570-148">Vietų tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a9570-148">Define location types</span></span>
1. <span data-ttu-id="a9570-149">Eikite į Vietos tipai.</span><span class="sxs-lookup"><span data-stu-id="a9570-149">Go to Location types.</span></span>
    * <span data-ttu-id="a9570-150">Vietų tipus galima naudoti kaip filtravimo parinktis, kad būtų galima kontroliuoti skirtingus sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="a9570-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="a9570-151">Tam, kad galėtumėte apibrėžti siuntimo sandėlio valdymo procesą, turite sukurti bent jau išdėstymo ir galutinės siuntimo vietos tipus.</span><span class="sxs-lookup"><span data-stu-id="a9570-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="a9570-152">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-152">Click New.</span></span>
3. <span data-ttu-id="a9570-153">Lauke „Vietos tipas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="a9570-154">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a9570-155">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="a9570-156">Vietos šablono nustatymas</span><span class="sxs-lookup"><span data-stu-id="a9570-156">Define location profile</span></span>
1. <span data-ttu-id="a9570-157">Eikite į Vietos šablonai.</span><span class="sxs-lookup"><span data-stu-id="a9570-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="a9570-158">Vietos šablonų apibrėžimas yra labai svarbus.</span><span class="sxs-lookup"><span data-stu-id="a9570-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="a9570-159">Sugrupuotų vietų pajėgumą galima kontroliuoti čia, taip pat galima kontroliuoti, su kokiomis atsargomis susijusios strategijos bus išsaugotos ir kaip jos bus išsaugotos.</span><span class="sxs-lookup"><span data-stu-id="a9570-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="a9570-160">Vietų šablonus galima naudoti kaip filtravimo parinktis, kad būtų galima kontroliuoti skirtingus sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="a9570-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="a9570-161">Norėdami įjungti sandėlio valdumo procesus, turite sukurti bent jau vartotojo vietos profilį.</span><span class="sxs-lookup"><span data-stu-id="a9570-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="a9570-162">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-162">Click New.</span></span>
3. <span data-ttu-id="a9570-163">Lauke Vietos šablono ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="a9570-164">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a9570-165">Lauke Vietos formatas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a9570-166">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a9570-167">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a9570-168">Lauke Vietos tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a9570-169">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a9570-170">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a9570-171">Pažymėkite arba atžymėkite žymės langelį Leisti įvairias atsargų būsenas.</span><span class="sxs-lookup"><span data-stu-id="a9570-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="a9570-172">Įgalinkite šią pasirinktį, jei norite leisti įvairias atsargų būsenos vertes, kurios bus naudojamos šio vietos šablono grupuojamose vietose.</span><span class="sxs-lookup"><span data-stu-id="a9570-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="a9570-173">Pažymėkite arba atžymėkite žymės langelį Nepaisyti paketo dienų taisyklių.</span><span class="sxs-lookup"><span data-stu-id="a9570-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="a9570-174">Įgalinkite šią pasirinktį, norėdami nepaisyti taisyklės tiek dienų, kiek skirsis atsargų paketo galiojimo datos, kad galėtumėte maišyti šiai taisyklei nepaklūstančius atsargų paketus.</span><span class="sxs-lookup"><span data-stu-id="a9570-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="a9570-175">Pažymėkite arba išvalykite žymės langelį Leisti ciklo skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="a9570-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="a9570-176">Įgalinkite šią pasirinktį, jei norite leisti apdoroti ciklo skaičiavimo procesą visose šio vietos šablono grupuojamose vietose.</span><span class="sxs-lookup"><span data-stu-id="a9570-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="a9570-177">Išplėskite arba sutraukite sekciją Dimensijos.</span><span class="sxs-lookup"><span data-stu-id="a9570-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="a9570-178">Dimensijų skirtukas leidžia nustatyti parametrus ir metodus, kuriais naudodamiesi galite tiksliai apskaičiuoti kiekvienos vietos pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="a9570-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="a9570-179">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="a9570-180">Sandėlio valdymo parametrų įgalinimas</span><span class="sxs-lookup"><span data-stu-id="a9570-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="a9570-181">Eikite į Sandėlio valdymo parametrai.</span><span class="sxs-lookup"><span data-stu-id="a9570-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="a9570-182">Tam, kad būtų galima apdoroti sandėlio darbą, turite nustatyti vartotojo vietos šablono išdėstymo vietos tipo parametrus ir galutinės siuntimo vietos tipą. Kai siuntimo procesas baigiasi jūsų nurodytu galutinės siuntimo vietos tipu, susijusių siunčiamų operacijų būsena atnaujinama į „Paimta“.</span><span class="sxs-lookup"><span data-stu-id="a9570-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="a9570-183">Išplėskite arba sutraukite sekciją Vietos šablonai.</span><span class="sxs-lookup"><span data-stu-id="a9570-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="a9570-184">Lauke Vartotojo vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a9570-185">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a9570-186">Išplėskite arba sutraukite sekciją Vietų tipai.</span><span class="sxs-lookup"><span data-stu-id="a9570-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="a9570-187">Lauke Surinkimo vietos tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a9570-188">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a9570-189">Lauke Galutinės siuntimo vietos tipas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a9570-190">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a9570-191">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="a9570-192">Sandėlio zonų grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="a9570-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="a9570-193">Eikite į Sandėlio zonų grupės.</span><span class="sxs-lookup"><span data-stu-id="a9570-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="a9570-194">Sandėlio zonas galima naudoti kaip parinkčių filtrus, kad būtų galima kontroliuoti skirtingus sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="a9570-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="a9570-195">Prieš nurodydami zoną turite sukurti zonų grupę.</span><span class="sxs-lookup"><span data-stu-id="a9570-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="a9570-196">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-196">Click New.</span></span>
3. <span data-ttu-id="a9570-197">Lauke Zonų grupės ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="a9570-198">Lauke Zonų grupės pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="a9570-199">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="a9570-200">Sandėlio zonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a9570-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="a9570-201">Eikite į Zonos.</span><span class="sxs-lookup"><span data-stu-id="a9570-201">Go to Zones.</span></span>
2. <span data-ttu-id="a9570-202">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-202">Click New.</span></span>
3. <span data-ttu-id="a9570-203">Lauke Zonos ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="a9570-204">Lauke Zonos pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="a9570-205">Lauke Zonų grupės ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a9570-206">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a9570-207">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a9570-208">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="a9570-209">Vietų kūrimas naudojant vietos nustatymo vedlį</span><span class="sxs-lookup"><span data-stu-id="a9570-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="a9570-210">Eikite į Vietos nustatymo vedlys.</span><span class="sxs-lookup"><span data-stu-id="a9570-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="a9570-211">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a9570-212">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a9570-213">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a9570-214">Lauke Zonos ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a9570-215">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a9570-216">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a9570-217">Lauke Vietos šablono ID spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="a9570-218">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a9570-219">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a9570-220">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a9570-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="a9570-221">Lauke Nuo numerio įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="a9570-222">Laukuose Nuo numerio ir Iki numerio nurodoma, kiek vietų bus sukurta.</span><span class="sxs-lookup"><span data-stu-id="a9570-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="a9570-223">Pvz., jei visoms keturioms vietos formato eilutėms Nuo numerio nurodote 1, o Iki numerio – 3, bus sukurta 81 vieta (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="a9570-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="a9570-224">Lauke Iki numerio įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="a9570-225">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a9570-226">Lauke Nuo numerio įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="a9570-227">Lauke Iki numerio įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="a9570-228">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="a9570-229">Lauke Nuo numerio įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="a9570-230">Lauke Iki numerio įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="a9570-231">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9570-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="a9570-232">Lauke Nuo numerio įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="a9570-233">Lauke Iki numerio įveskite numerį.</span><span class="sxs-lookup"><span data-stu-id="a9570-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="a9570-234">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="a9570-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="a9570-235">Vietų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="a9570-235">Create locations manually</span></span>
1. <span data-ttu-id="a9570-236">Eikite į Vietos.</span><span class="sxs-lookup"><span data-stu-id="a9570-236">Go to Locations.</span></span>
    * <span data-ttu-id="a9570-237">Galima lengvai rankiniu būdu kurti sandėlio vietas.</span><span class="sxs-lookup"><span data-stu-id="a9570-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="a9570-238">Vietos pavadinimo ir vietos šablono ID reikšmės yra privalomos.</span><span class="sxs-lookup"><span data-stu-id="a9570-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="a9570-239">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-239">Click New.</span></span>
3. <span data-ttu-id="a9570-240">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="a9570-241">Lauke Vieta surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="a9570-242">Atkreipkite dėmesį, kad čia jūs kuriate naują vietą, todėl reikia įvesti naują unikalų pavadinimą, o ne pasirinkti vieną iš esamų.</span><span class="sxs-lookup"><span data-stu-id="a9570-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="a9570-243">Lauke Vietos šablono ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="a9570-244">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="a9570-245">Paketų dydžių kategorijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a9570-245">Define Pack size categories</span></span>
1. <span data-ttu-id="a9570-246">Eikite į Paketų dydžių kategorijos.</span><span class="sxs-lookup"><span data-stu-id="a9570-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="a9570-247">Paketo dydžio kategorijas galima naudoti norint grupuoti prekes, kurių paketų dydžiai panašūs.</span><span class="sxs-lookup"><span data-stu-id="a9570-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="a9570-248">Šiame pavyzdyje paketo dydžio kategorija bus naudojama norint kontroliuoti pajėgumą konkrečiose sandėlio paėmimo vietose.</span><span class="sxs-lookup"><span data-stu-id="a9570-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="a9570-249">Atkreipkite dėmesį, kad paketo dydžio kategorijos ID turi būti priskirtas prie išleisto produkto objekto, kad jį būtų galima panaudoti kaip sandėliavimo limitų apdorojimo dalį.</span><span class="sxs-lookup"><span data-stu-id="a9570-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="a9570-250">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-250">Click New.</span></span>
3. <span data-ttu-id="a9570-251">Lauke Paketo dydžio kategorijos ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="a9570-252">Lauke Paketo dydžio kategorijos pavadinimas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="a9570-253">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="a9570-254">Vietos sandėliavimo apribojimų apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="a9570-254">Define location stocking limits</span></span>
1. <span data-ttu-id="a9570-255">Eikite į Vietų sandėliavimo limitai.</span><span class="sxs-lookup"><span data-stu-id="a9570-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="a9570-256">Vietos sandėliavimo limitai padeda norint įsitikinti, kad sukūrus darbą atsargas būtų prašoma padėtį ne į tokią vietą, kuri būtų fiziškai nepajėgi jų sutalpinti.</span><span class="sxs-lookup"><span data-stu-id="a9570-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="a9570-257">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-257">Click New.</span></span>
3. <span data-ttu-id="a9570-258">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="a9570-259">Lauke Vietos šablono ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="a9570-260">Lauke Paketo dydžio kategorijos ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="a9570-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="a9570-261">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="a9570-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="a9570-262">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a9570-262">Click Save.</span></span>
8. <span data-ttu-id="a9570-263">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="a9570-264">Fiksuotų paėmimo vietų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a9570-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="a9570-265">Eikite į Fiksuotos vietos.</span><span class="sxs-lookup"><span data-stu-id="a9570-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="a9570-266">Galite nurodyti kiekvienam produktui arba produkto variantui naudotinas vietas.</span><span class="sxs-lookup"><span data-stu-id="a9570-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="a9570-267">Galima sukurti keletą to paties produkto, esančio tame pačiame sandėlyje, fiksuotų vietų.</span><span class="sxs-lookup"><span data-stu-id="a9570-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="a9570-268">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a9570-268">Click New.</span></span>
3. <span data-ttu-id="a9570-269">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="a9570-270">Lauke Sandėlis surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9570-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="a9570-271">Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a9570-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a9570-272">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a9570-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a9570-273">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a9570-273">Close the page.</span></span>

