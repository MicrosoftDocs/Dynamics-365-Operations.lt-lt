--- 
title: "Min.–maks. papildymo proceso nustatymas"
description: "Šia procedūra paaiškinama, kaip nustatyti naują papildymo procesą, kuris naudoja minimalaus / maksimalaus papildymo strategiją."
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02af5d1beb2d4eb6a7162b47c42854725fbdbec2
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-min-max-replenishment-process"></a><span data-ttu-id="0476a-103">Min.–maks. papildymo proceso nustatymas</span><span class="sxs-lookup"><span data-stu-id="0476a-103">Set up a min-max replenishment process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0476a-104">Šia procedūra paaiškinama, kaip nustatyti naują papildymo procesą, kuris naudoja minimalaus / maksimalaus papildymo strategiją.</span><span class="sxs-lookup"><span data-stu-id="0476a-104">This procedure shows you how to set up a new replenishment process which uses the minimum/maximum replenishment strategy.</span></span> <span data-ttu-id="0476a-105">Kai atsargos nukris žemiau minimalaus lygio, papildyti tai vietai bus sukurtas darbas.</span><span class="sxs-lookup"><span data-stu-id="0476a-105">When inventory falls below the minimum level, work will be created to replenish the location.</span></span> <span data-ttu-id="0476a-106">Šia procedūra taip pat rodoma, kaip naudojant fiksuotas paėmimo vietas leisti papildyti sandėlį, net jei atsargos nukrenta žemiau minimalaus lygio, ir kaip įgalinti reguliarų papildymo proceso vykdymą, naudojant paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="0476a-106">The procedure also shows how to use fixed picking locations to allow restocking even if inventory falls below the minimum level, and how to enable the replenishment process to run regularly using a batch job.</span></span> <span data-ttu-id="0476a-107">Šias užduotis paprastai turėtų atlikti sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="0476a-107">These tasks would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="0476a-108">Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF, naudodami pastabų reikšmių pavyzdžius, arba ją galite vykdyti su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="0476a-108">You can run this procedure in the USMF demo data company using the example values in the notes, or can run it on your own data.</span></span> <span data-ttu-id="0476a-109">Jei naudojate savo duomenis, įsitikinkite, kad turite sandėlį, kuriame galima atlikti sandėlio valdymo procesus.</span><span class="sxs-lookup"><span data-stu-id="0476a-109">If you’re using your own data, make sure that you have a warehouse that’s enabled for Warehouse management processes.</span></span>


## <a name="create-a-fixed-picking-location"></a><span data-ttu-id="0476a-110">Fiksuotos paėmimo vietos kūrimas</span><span class="sxs-lookup"><span data-stu-id="0476a-110">Create a fixed picking location</span></span>
1. <span data-ttu-id="0476a-111">Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlis > Fiksuotos vietos.</span><span class="sxs-lookup"><span data-stu-id="0476a-111">Go to Warehouse management > Setup > Warehouse > Fixed locations.</span></span>
    * <span data-ttu-id="0476a-112">Tai – neprivaloma min.–maks. papildymo užduotis, tačiau, jei naudojate fiksuotą paėmimo vietą, taip atsargas galima papildyti net jei jos nukrenta žemiau minimalaus lygio, nes sistema gali nustatyti, kurias prekes reikia papildyti, net jei jų nelikę.</span><span class="sxs-lookup"><span data-stu-id="0476a-112">This is an optional task for min-max replenishment, but if you use fixed picking location, this allows stock to be replenished even if it falls below the minimum level, because the system can determine which items need to be replenished, even if there aren't any left.</span></span>  
2. <span data-ttu-id="0476a-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-113">Click New.</span></span>
3. <span data-ttu-id="0476a-114">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-114">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-115">Jei naudojate USMF, galite pasirinkti prekę A0001.</span><span class="sxs-lookup"><span data-stu-id="0476a-115">If you’re using USMF, you can select item A0001.</span></span>  
4. <span data-ttu-id="0476a-116">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-116">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-117">Jei naudojate USMF, galite pasirinkti 2-ąją vietą.</span><span class="sxs-lookup"><span data-stu-id="0476a-117">If you’re using USMF, you can select site 2.</span></span>  
5. <span data-ttu-id="0476a-118">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-118">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-119">Jei naudojate USMF, galite pasirinkti 24-ąjį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="0476a-119">If you’re using USMF, you can select warehouse 24.</span></span>  
6. <span data-ttu-id="0476a-120">Lauke Vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-120">In the Location field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-121">Jei naudojate USMF, galite pasirinkti CP-003.</span><span class="sxs-lookup"><span data-stu-id="0476a-121">If you’re using USMF, you can select CP-003.</span></span>  
7. <span data-ttu-id="0476a-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0476a-122">Close the page.</span></span>

## <a name="create-a-replenishment-location-directive"></a><span data-ttu-id="0476a-123">Papildymo vietos nurodymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="0476a-123">Create a replenishment location directive</span></span>
1. <span data-ttu-id="0476a-124">Pasirinkite Sandėlio valdymas > Nustatymai > Vietos nurodymai.</span><span class="sxs-lookup"><span data-stu-id="0476a-124">Go to Warehouse management > Setup > Location directives.</span></span>
    * <span data-ttu-id="0476a-125">Vietos nurodymai naudojami nustatyti, iš kur atliekant papildymo procesą reikėtų imti prekes.</span><span class="sxs-lookup"><span data-stu-id="0476a-125">Location directives are used to determine where items should be picked from in the replenishment process.</span></span>  
2. <span data-ttu-id="0476a-126">Lauke Darbo užsakymo tipas pasirinkite Papildymas.</span><span class="sxs-lookup"><span data-stu-id="0476a-126">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="0476a-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-127">Click New.</span></span>
4. <span data-ttu-id="0476a-128">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-128">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0476a-129">Lauke Darbo tipas pasirinkite 'Paimti'.</span><span class="sxs-lookup"><span data-stu-id="0476a-129">In the Work type field, select 'Pick'.</span></span>
6. <span data-ttu-id="0476a-130">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-130">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-131">Jei naudojate USMF, galite pasirinkti 2-ąją vietą.</span><span class="sxs-lookup"><span data-stu-id="0476a-131">If you’re using USMF, you can select site 2.</span></span>  
7. <span data-ttu-id="0476a-132">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-132">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-133">Jei naudojate USMF, galite pasirinkti 24-ąjį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="0476a-133">If you’re using USMF, you can select warehouse 24.</span></span>  
8. <span data-ttu-id="0476a-134">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-134">Click Save.</span></span>
9. <span data-ttu-id="0476a-135">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-135">Click New.</span></span>
10. <span data-ttu-id="0476a-136">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0476a-136">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="0476a-137">Lauke Galutinis kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0476a-137">In the To quantity field, enter a number.</span></span>
    * <span data-ttu-id="0476a-138">Pavyzdžiui, galite nustatyti 9999.</span><span class="sxs-lookup"><span data-stu-id="0476a-138">For example, you can set it to 9999.</span></span>  
12. <span data-ttu-id="0476a-139">Pažymėkite žymės langelį Leisti skaidyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-139">Select the Allow split check box.</span></span>
    * <span data-ttu-id="0476a-140">Jei pasirinksite šią parinktį, atliekant darbo kūrimo procesą, darbo eilučių kiekius bus galima išskaidyti keliose vietose.</span><span class="sxs-lookup"><span data-stu-id="0476a-140">If you select this option, the work creation process will allow work line quantities to be split across multiple locations.</span></span>  
13. <span data-ttu-id="0476a-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-141">Click Save.</span></span>
14. <span data-ttu-id="0476a-142">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-142">Click New.</span></span>
15. <span data-ttu-id="0476a-143">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0476a-143">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="0476a-144">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-144">In the Name field, type a value.</span></span>
17. <span data-ttu-id="0476a-145">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-145">Click Save.</span></span>
18. <span data-ttu-id="0476a-146">Spustelėkite Redaguoti užklausą.</span><span class="sxs-lookup"><span data-stu-id="0476a-146">Click Edit query.</span></span>
    * <span data-ttu-id="0476a-147">Šią užklausą galite redaguoti ir į ją įtraukti apribojimų, kad atsargas būtų galima pasirinkti atliekant papildymo procesą.</span><span class="sxs-lookup"><span data-stu-id="0476a-147">You can edit this query to add restrictions where inventory can be selected from in the replenishment process.</span></span> <span data-ttu-id="0476a-148">Pavyzdžiui, gali būti, kad atsargas reikėtų naudoti tik iš sandėlio sandėliavimo vietos.</span><span class="sxs-lookup"><span data-stu-id="0476a-148">For example, it could be that inventory should only be used from the Bulk area of the warehouse.</span></span>  
19. <span data-ttu-id="0476a-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0476a-149">Click OK.</span></span>
20. <span data-ttu-id="0476a-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0476a-150">Close the page.</span></span>

## <a name="create-a-replenishment-work-template"></a><span data-ttu-id="0476a-151">Papildymo darbo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="0476a-151">Create a replenishment work template</span></span>
1. <span data-ttu-id="0476a-152">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="0476a-152">Go to Warehouse management > Setup > Work > Work templates.</span></span>
    * <span data-ttu-id="0476a-153">Darbo šablonas naudojamas valdyti sistemai – kaip reikia kurti min. / maks. papildymo darbą.</span><span class="sxs-lookup"><span data-stu-id="0476a-153">The work template is use to guide the system as to how the min/max replenishment work must be created.</span></span> <span data-ttu-id="0476a-154">Turi būti bent paėmimo ir padėjimo darbo šablono eilutė.</span><span class="sxs-lookup"><span data-stu-id="0476a-154">As a minimum, there must be a work template line for a pick and a put.</span></span> <span data-ttu-id="0476a-155">Kol nebus įvesta visa būtina informacija, bus rodoma, kad darbo šablonas netinkamas.</span><span class="sxs-lookup"><span data-stu-id="0476a-155">The work template will say that it’s Invalid until all the necessary information has been filled in.</span></span>  
2. <span data-ttu-id="0476a-156">Lauke Darbo užsakymo tipas pasirinkite Papildymas.</span><span class="sxs-lookup"><span data-stu-id="0476a-156">In the Work order type field, select 'Replenishment'.</span></span>
3. <span data-ttu-id="0476a-157">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-157">Click New.</span></span>
4. <span data-ttu-id="0476a-158">Lauke „Darbo šablonas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-158">In the Work template field, type a value.</span></span>
5. <span data-ttu-id="0476a-159">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-159">Click Save.</span></span>
6. <span data-ttu-id="0476a-160">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-160">Click New.</span></span>
7. <span data-ttu-id="0476a-161">Lauke Darbo tipas pasirinkite 'Paimti'.</span><span class="sxs-lookup"><span data-stu-id="0476a-161">In the Work type field, select 'Pick'.</span></span>
8. <span data-ttu-id="0476a-162">Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-162">In the Work class ID field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-163">Tai turėtų būti darbo klasė, susijusi su papildymu.</span><span class="sxs-lookup"><span data-stu-id="0476a-163">This should be a work class related to replenishment.</span></span> <span data-ttu-id="0476a-164">Jei naudojate USMF, pasirinkite Papildyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-164">If you’re using USMF, select Replenish.</span></span>  
9. <span data-ttu-id="0476a-165">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-165">Click New.</span></span>
10. <span data-ttu-id="0476a-166">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0476a-166">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="0476a-167">Lauke Darbo tipas pasirinkite „Padėjimas“.</span><span class="sxs-lookup"><span data-stu-id="0476a-167">In the Work type field, select 'Put'.</span></span>
12. <span data-ttu-id="0476a-168">Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-168">In the Work class ID field, enter or select a value.</span></span>
13. <span data-ttu-id="0476a-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-169">Click Save.</span></span>
14. <span data-ttu-id="0476a-170">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0476a-170">Close the page.</span></span>

## <a name="create-a-new-replenishment-template"></a><span data-ttu-id="0476a-171">Naujo papildymo šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="0476a-171">Create a new replenishment template</span></span>
1. <span data-ttu-id="0476a-172">Pasirinkite Sandėlio valdymas > Nustatymas > Papildymas > Papildymo šablonai.</span><span class="sxs-lookup"><span data-stu-id="0476a-172">Go to Warehouse management > Setup > Replenishment > Replenishment templates.</span></span>
    * <span data-ttu-id="0476a-173">Papildymo šablonas naudojamas apibrėžti, kurias prekes, kiekius ir vietą reikia papildyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-173">The replenishment template is used to define the items and quantities, and the location to replenish.</span></span>  
2. <span data-ttu-id="0476a-174">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-174">Click New.</span></span>
3. <span data-ttu-id="0476a-175">Lauke Papildymo šablonas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-175">In the Replenish template field, type a value.</span></span>
    * <span data-ttu-id="0476a-176">Šablonui suteikite pavadinimą, nurodantį, kad jis skirtas min. / maks. papildymui.</span><span class="sxs-lookup"><span data-stu-id="0476a-176">Give the template a name to indicate that it’s for min/max replenishment.</span></span>  
4. <span data-ttu-id="0476a-177">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-177">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0476a-178">Pažymėkite žymės langelį Leisti poreikio bangai naudoti nerezervuotus kiekius.</span><span class="sxs-lookup"><span data-stu-id="0476a-178">Select the Allow wave demand to use unreserved quantities check box.</span></span>
    * <span data-ttu-id="0476a-179">Jei pasirenkate šią parinktį, atliekant bangos bangos paklausos papildymą galima vartoti kiekius, kurie yra susiję su min. / maks. papildymu.</span><span class="sxs-lookup"><span data-stu-id="0476a-179">If you select this option, it enables wave demand replenishment to consume quantities that are related to min/max replenishment.</span></span> <span data-ttu-id="0476a-180">Pavyzdžiui, tai gali būti naudinga, jei min. / maks. papildymo darbas apdorojamas ne iš karto, kad nebūtų sukurta nereikalingo paklausos papildymo darbo.</span><span class="sxs-lookup"><span data-stu-id="0476a-180">For example, this might be useful if the min/max replenishment work isn’t processed immediately, to avoid unnecessary demand replenishment work from being created.</span></span>  
6. <span data-ttu-id="0476a-181">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0476a-181">Click New.</span></span>
7. <span data-ttu-id="0476a-182">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0476a-182">In the Sequence number field, enter a number.</span></span>
8. <span data-ttu-id="0476a-183">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-183">In the Description field, type a value.</span></span>
9. <span data-ttu-id="0476a-184">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0476a-184">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="0476a-185">Lauke Papildymo vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-185">In the Replenishment unit field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-186">Pvz., pasirinkite vnt.</span><span class="sxs-lookup"><span data-stu-id="0476a-186">For example, select pcs.</span></span> <span data-ttu-id="0476a-187">Šis parametras yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="0476a-187">This setting is mandatory.</span></span> <span data-ttu-id="0476a-188">Juo galima nurodyti papildymo darbo matavimo vienetą, kuris skiriasi nuo nurodyto šio šablono mažiausio ir didžiausio atsargų lygio vieneto.</span><span class="sxs-lookup"><span data-stu-id="0476a-188">It allows you to specify a different unit of measurement for replenishment work compared to the unit specified for the minimum and maximum stock levels in this template.</span></span>  
11. <span data-ttu-id="0476a-189">Lauke Darbo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-189">In the Work template field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-190">Pasirinkite darbo šabloną, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="0476a-190">Choose the work template that you created earlier.</span></span>  
12. <span data-ttu-id="0476a-191">Lauke Mažiausias kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0476a-191">In the Minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="0476a-192">Pasirinkite mažiausią kiekį, kuris turėtų paleisti papildymą.</span><span class="sxs-lookup"><span data-stu-id="0476a-192">Select the minimum quantity that should trigger the replenishment.</span></span> <span data-ttu-id="0476a-193">Pavyzdžiui, nustatykite 50.</span><span class="sxs-lookup"><span data-stu-id="0476a-193">For example, set this to 50.</span></span> <span data-ttu-id="0476a-194">Šį kiekį galima palikti nustatytą į nulį – jei papildote fiksuotą vietą ir parinktis Papildyti tuščias fiksuotas vietas nustatyta į Taip.</span><span class="sxs-lookup"><span data-stu-id="0476a-194">It is possible to leave this set to zero, if you’re replenishing a fixed location and the Replenish empty fixed locations option is set to Yes.</span></span> <span data-ttu-id="0476a-195">Taip pat rekomenduojame pasirinkti parinktį Papildyti atsargas tik fiksuotose vietose, kad procesas būtų našesnis.</span><span class="sxs-lookup"><span data-stu-id="0476a-195">We also recommend that you select the Replenish only fixed locations option for performance reasons.</span></span>  
13. <span data-ttu-id="0476a-196">Lauke Didžiausias kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0476a-196">In the Maximum quantity field, enter a number.</span></span>
    * <span data-ttu-id="0476a-197">Pavyzdžiui, nustatykite 100.</span><span class="sxs-lookup"><span data-stu-id="0476a-197">For example, set this to 100.</span></span>  
14. <span data-ttu-id="0476a-198">Lauke Vienetas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-198">In the Unit field, enter or select a value.</span></span>
    * <span data-ttu-id="0476a-199">Priskirkite mažiausio ir didžiausio kiekių vienetą.</span><span class="sxs-lookup"><span data-stu-id="0476a-199">Assign the unit for the minimum and maximum quantities.</span></span> <span data-ttu-id="0476a-200">Pavyzdžiui, nustatykite „vnt.‟.</span><span class="sxs-lookup"><span data-stu-id="0476a-200">For example, set this to pcs.</span></span>  
15. <span data-ttu-id="0476a-201">Pažymėkite žymės langelį Papildyti tuščias fiksuotas vietas.</span><span class="sxs-lookup"><span data-stu-id="0476a-201">Select the Replenish empty fixed locations check box.</span></span>
    * <span data-ttu-id="0476a-202">Pažymėkite šį žymės langelį, kad fiksuotas vietas papildytumėte, kai jos tuščios.</span><span class="sxs-lookup"><span data-stu-id="0476a-202">Select this check box to replenish fixed locations when they are empty.</span></span> <span data-ttu-id="0476a-203">Kitu atveju bus papildytos tik vietos, kuriose yra turimas kiekis.</span><span class="sxs-lookup"><span data-stu-id="0476a-203">Otherwise, only the locations where there is a quantity on hand will be replenished.</span></span>  
16. <span data-ttu-id="0476a-204">Pažymėkite žymės langelį Papildyti atsargas tik fiksuotose vietose.</span><span class="sxs-lookup"><span data-stu-id="0476a-204">Select the Replenish only fixed locations check box.</span></span>
17. <span data-ttu-id="0476a-205">Spustelėkite Pasirinkite produktus.</span><span class="sxs-lookup"><span data-stu-id="0476a-205">Click Select products.</span></span>
    * <span data-ttu-id="0476a-206">Tai yra vieta, kurioje galima apibrėžti, kuriuos produktus reikėtų papildyti.</span><span class="sxs-lookup"><span data-stu-id="0476a-206">This is the place to define which products should be replenished.</span></span> <span data-ttu-id="0476a-207">Jei pasirinkta parinktis Fiksuotos paėmimo vietos, tas vietas taip pat turite apibrėžti šioje užklausoje.</span><span class="sxs-lookup"><span data-stu-id="0476a-207">If the Fixed picking locations option is selected, you also need to define the locations in this query.</span></span> <span data-ttu-id="0476a-208">Galima naudoti konkrečių variantų užklausas ir konkrečių produktų užklausas.</span><span class="sxs-lookup"><span data-stu-id="0476a-208">Variant-specific queries are available as well product-specific queries.</span></span>  
18. <span data-ttu-id="0476a-209">Pasirinkite eilutę Prekės.</span><span class="sxs-lookup"><span data-stu-id="0476a-209">Select the Items row.</span></span>
19. <span data-ttu-id="0476a-210">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-210">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0476a-211">Pasirinkite prekes, kurias reikėtų papildyti fiksuotose vietose.</span><span class="sxs-lookup"><span data-stu-id="0476a-211">Select the items that should be replenished at the fixed locations.</span></span> <span data-ttu-id="0476a-212">Pavyzdžiui, įveskite A*, kad pasirinktumėte visus prekių numerius, prasidedančius A.</span><span class="sxs-lookup"><span data-stu-id="0476a-212">For example, type A* to select all item numbers beginning with A.</span></span>  
20. <span data-ttu-id="0476a-213">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="0476a-213">Click Add.</span></span>
    * <span data-ttu-id="0476a-214">Įtraukite objektą Vieta (nebent jis jau yra), kad galėtumėte nustatyti, jog papildymo darbas turėtų būti atliekamas tik fiksuotose paėmimo vietose, esančiose konkrečioje sandėlio vietoje.</span><span class="sxs-lookup"><span data-stu-id="0476a-214">Add the Location entity (unless it already exists) to be able to restrict the replenishment work to the fixed picking locations within a specific area of the warehouse.</span></span>  
21. <span data-ttu-id="0476a-215">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0476a-215">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="0476a-216">Lauką Lentelė nustatykite į Vietos.</span><span class="sxs-lookup"><span data-stu-id="0476a-216">Set the Table field to Locations.</span></span>
23. <span data-ttu-id="0476a-217">Lauke Laukas pasirinkite Vietos profilio ID.</span><span class="sxs-lookup"><span data-stu-id="0476a-217">In the Field field, select Location profile ID.</span></span>
24. <span data-ttu-id="0476a-218">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-218">In the Criteria field, enter or select a value.</span></span>
25. <span data-ttu-id="0476a-219">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0476a-219">Click OK.</span></span>
26. <span data-ttu-id="0476a-220">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0476a-220">Close the page.</span></span>

## <a name="set-the-replenishment-process-to-run-as-a-batch-job"></a><span data-ttu-id="0476a-221">Nustatymas, kad papildymo procesas būtų vykdomas kaip paketinė užduotis</span><span class="sxs-lookup"><span data-stu-id="0476a-221">Set the replenishment process to run as a batch job</span></span>
1. <span data-ttu-id="0476a-222">Pasirinkite Sandėlio valdymas > Papildymas > Papildymai.</span><span class="sxs-lookup"><span data-stu-id="0476a-222">Go to Warehouse management > Replenishment > Replenishments.</span></span>
    * <span data-ttu-id="0476a-223">Puslapyje Papildymai galima nustatyti, kad papildymas būtų vykdomas kaip paketinė užduotis, arba reikalauti, kad jis būtų pradedamas rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="0476a-223">The Replenishments page allows you to set up replenishment to run as a batch job, or to require that it’s started manually.</span></span>  
2. <span data-ttu-id="0476a-224">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="0476a-224">Click Filter.</span></span>
3. <span data-ttu-id="0476a-225">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0476a-225">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0476a-226">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0476a-226">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="0476a-227">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="0476a-227">Click OK.</span></span>
6. <span data-ttu-id="0476a-228">Išplėskite dalį Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="0476a-228">Expand the Run in the background section.</span></span>
7. <span data-ttu-id="0476a-229">Parinktį Paketinis vykdymas nustatykite į Taip.</span><span class="sxs-lookup"><span data-stu-id="0476a-229">Set the Batch processing option to Yes.</span></span>
8. <span data-ttu-id="0476a-230">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="0476a-230">Click Recurrence.</span></span>
9. <span data-ttu-id="0476a-231">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="0476a-231">Select the No end date option.</span></span>
10. <span data-ttu-id="0476a-232">Nustatykite pasikartojimo modelį.</span><span class="sxs-lookup"><span data-stu-id="0476a-232">Set the Recurrance pattern.</span></span>
    * <span data-ttu-id="0476a-233">Pavyzdžiui, pasirinkite Dienos.</span><span class="sxs-lookup"><span data-stu-id="0476a-233">For example, select Days.</span></span>  
11. <span data-ttu-id="0476a-234">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0476a-234">Click OK.</span></span>
12. <span data-ttu-id="0476a-235">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0476a-235">Click OK.</span></span>

