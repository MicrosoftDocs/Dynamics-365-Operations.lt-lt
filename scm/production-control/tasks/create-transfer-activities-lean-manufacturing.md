--- 
title: "Kurti „lean manufacturing“ perdavimo veiklas"
description: "Sukurkite „lean manufacturing“ perkėlimo veiklą."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e5f28b26cee2501f1294cd34a495ee925e6b1ba8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="af143-103">Kurti „lean manufacturing“ perdavimo veiklas</span><span class="sxs-lookup"><span data-stu-id="af143-103">Create transfer activities for lean manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af143-104">Sukurkite „lean manufacturing“ perkėlimo veiklą.</span><span class="sxs-lookup"><span data-stu-id="af143-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="af143-105">Išankstiniai reikalavimai:</span><span class="sxs-lookup"><span data-stu-id="af143-105">Prerequisites:</span></span> 

1. <span data-ttu-id="af143-106">Turi būti sukurta gamybos eiga ir neaktyvi versija.</span><span class="sxs-lookup"><span data-stu-id="af143-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="af143-107">Turi būti sukurti iš ir į sandėliai ir vietos.</span><span class="sxs-lookup"><span data-stu-id="af143-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="af143-108">Pasirinktinai turėtų būti sukurtas papildantis arba papildytas darbo elementas.</span><span class="sxs-lookup"><span data-stu-id="af143-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="af143-109">Kaip rasti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="af143-109">Find the production flow version</span></span>
1. <span data-ttu-id="af143-110">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="af143-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="af143-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="af143-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="af143-112">Nepamirškite, kad gamybos eiga turi turėti juodraščio būsenos versiją.</span><span class="sxs-lookup"><span data-stu-id="af143-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="af143-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="af143-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="af143-114">Naujos veiklos kūrimas</span><span class="sxs-lookup"><span data-stu-id="af143-114">Create a new activity</span></span>
1. <span data-ttu-id="af143-115">Spustelėkite Veiklos.</span><span class="sxs-lookup"><span data-stu-id="af143-115">Click Activities.</span></span>
    * <span data-ttu-id="af143-116">Užtikrinkite, kad pasirinkta gamybos eiga turi juodraščio versiją ir pasirinkite tą versiją.</span><span class="sxs-lookup"><span data-stu-id="af143-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="af143-117">Spustelėkite Kurti naują plano veiklą.</span><span class="sxs-lookup"><span data-stu-id="af143-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="af143-118">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="af143-118">Click Next.</span></span>
4. <span data-ttu-id="af143-119">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af143-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="af143-120">Lauke Veiklos tipas pasirinkite „Perkėlimas“.</span><span class="sxs-lookup"><span data-stu-id="af143-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="af143-121">Lauke Proceso kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="af143-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="af143-122">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="af143-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="af143-123">Darbo elementų pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="af143-123">Select the Work cells</span></span>
1. <span data-ttu-id="af143-124">Lauke Papildymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="af143-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="af143-125">Norėdami darbo elemento išeigos vietą perkėlimo veikloje naudoti kaip vietą iš, pasirinkite darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="af143-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="af143-126">Tą patį galima atlikti naudojant papildytą darbo elementą, kuris nustato perkėlimo veiklos paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="af143-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="af143-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="af143-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="af143-128">Atsargų atnaujinimų nurodymas</span><span class="sxs-lookup"><span data-stu-id="af143-128">Define the inventory updates</span></span>
1. <span data-ttu-id="af143-129">Lauke Produkto tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="af143-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="af143-130">Atkreipkite dėmesį, kad perkėlimas nepakeičia produkto tipo.</span><span class="sxs-lookup"><span data-stu-id="af143-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="af143-131">Galite perkelti baigtus arba pusiau baigtus produktus (perkėlimas tarp dviejų gamybos eigos veiklų ir galbūt „kanban“ srauto).</span><span class="sxs-lookup"><span data-stu-id="af143-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="af143-132">Perkeldami baigtus produktus galite pasirinkti, ar paimant arba gaunant pradedama atsargų operacija.</span><span class="sxs-lookup"><span data-stu-id="af143-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="af143-133">Perkėlimo vietų nurodymas</span><span class="sxs-lookup"><span data-stu-id="af143-133">Define the transfer locations</span></span>
1. <span data-ttu-id="af143-134">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="af143-134">Click Next.</span></span>
2. <span data-ttu-id="af143-135">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="af143-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="af143-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="af143-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="af143-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="af143-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="af143-138">Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="af143-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="af143-139">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="af143-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="af143-140">Lauke Transportuoja pasirinkite „Siuntėjas“.</span><span class="sxs-lookup"><span data-stu-id="af143-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="af143-141">Galimos pasirinktys: Siuntėjas – siuntimo sandėlį valdanti organizacija, Gavėjas – gavimo sandėlį valdanti organizacija, Vežėjas – trečiosios šalies tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="af143-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="af143-142">Jei valdanti organizacija yra tiekėjas, norint atlikti perkėlimo veiklą reikalinga subrangos sutartis.</span><span class="sxs-lookup"><span data-stu-id="af143-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="af143-143">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="af143-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="af143-144">Veiklos laikų nurodymas</span><span class="sxs-lookup"><span data-stu-id="af143-144">Define the activity times</span></span>
1. <span data-ttu-id="af143-145">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="af143-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="af143-146">Būtinas dalies Apdorojimo laikas apibrėžimas.</span><span class="sxs-lookup"><span data-stu-id="af143-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="af143-147">Apdorojimo laikas naudojamas skaičiuojant savikainą ir „kanban“ užduočių našumo laikus.</span><span class="sxs-lookup"><span data-stu-id="af143-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="af143-148">Apdorojimo laikai nenaudojami skaičiuojant pajėgumą ir suvartojimą, kurie apskaičiuojami pagal iš gamybos eigos versijos užduoties gautą ciklo laiką.</span><span class="sxs-lookup"><span data-stu-id="af143-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="af143-149">Lauke Laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="af143-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="af143-150">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af143-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="af143-151">Pasirinkite Laiko vienetas.</span><span class="sxs-lookup"><span data-stu-id="af143-151">Select the Time unit.</span></span>
5. <span data-ttu-id="af143-152">Lauke Už kiekį įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="af143-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="af143-153">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="af143-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="af143-154">Laukimo eilėje laikai nebūtini.</span><span class="sxs-lookup"><span data-stu-id="af143-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="af143-155">Lauke Laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="af143-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="af143-156">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="af143-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="af143-157">Pasirinkite Laiko vienetas.</span><span class="sxs-lookup"><span data-stu-id="af143-157">Select the Time unit.</span></span>
10. <span data-ttu-id="af143-158">Lauke Už kiekį įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="af143-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="af143-159">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="af143-159">Click Next.</span></span>
12. <span data-ttu-id="af143-160">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="af143-160">Click Finish.</span></span>
13. <span data-ttu-id="af143-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="af143-161">Close the page.</span></span>


