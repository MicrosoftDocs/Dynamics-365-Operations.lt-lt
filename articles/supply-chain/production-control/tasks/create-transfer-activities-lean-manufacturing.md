---
title: Kurti „lean manufacturing“ perdavimo veiklas
description: Sukurkite „lean manufacturing“ perkėlimo veiklą.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae31cca96825665f9482b4523b66586415504b65
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210806"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="c1f15-103">Kurti „lean manufacturing“ perdavimo veiklas</span><span class="sxs-lookup"><span data-stu-id="c1f15-103">Create transfer activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1f15-104">Sukurkite „lean manufacturing“ perkėlimo veiklą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="c1f15-105">Išankstiniai reikalavimai:</span><span class="sxs-lookup"><span data-stu-id="c1f15-105">Prerequisites:</span></span> 

1. <span data-ttu-id="c1f15-106">Turi būti sukurta gamybos eiga ir neaktyvi versija.</span><span class="sxs-lookup"><span data-stu-id="c1f15-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="c1f15-107">Turi būti sukurti iš ir į sandėliai ir vietos.</span><span class="sxs-lookup"><span data-stu-id="c1f15-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="c1f15-108">Pasirinktinai turėtų būti sukurtas papildantis arba papildytas darbo elementas.</span><span class="sxs-lookup"><span data-stu-id="c1f15-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="c1f15-109">Kaip rasti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="c1f15-109">Find the production flow version</span></span>
1. <span data-ttu-id="c1f15-110">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="c1f15-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c1f15-111">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c1f15-112">Nepamirškite, kad gamybos eiga turi turėti juodraščio būsenos versiją.</span><span class="sxs-lookup"><span data-stu-id="c1f15-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="c1f15-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c1f15-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="c1f15-114">Naujos veiklos kūrimas</span><span class="sxs-lookup"><span data-stu-id="c1f15-114">Create a new activity</span></span>
1. <span data-ttu-id="c1f15-115">Spustelėkite Veiklos.</span><span class="sxs-lookup"><span data-stu-id="c1f15-115">Click Activities.</span></span>
    * <span data-ttu-id="c1f15-116">Užtikrinkite, kad pasirinkta gamybos eiga turi juodraščio versiją ir pasirinkite tą versiją.</span><span class="sxs-lookup"><span data-stu-id="c1f15-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="c1f15-117">Spustelėkite Kurti naują plano veiklą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="c1f15-118">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="c1f15-118">Click Next.</span></span>
4. <span data-ttu-id="c1f15-119">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f15-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c1f15-120">Lauke Veiklos tipas pasirinkite „Perkėlimas“.</span><span class="sxs-lookup"><span data-stu-id="c1f15-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="c1f15-121">Lauke Proceso kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f15-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="c1f15-122">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="c1f15-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="c1f15-123">Darbo elementų pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="c1f15-123">Select the Work cells</span></span>
1. <span data-ttu-id="c1f15-124">Lauke Papildymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c1f15-125">Norėdami darbo elemento išeigos vietą perkėlimo veikloje naudoti kaip vietą iš, pasirinkite darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="c1f15-126">Tą patį galima atlikti naudojant papildytą darbo elementą, kuris nustato perkėlimo veiklos paskirties vietą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="c1f15-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c1f15-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="c1f15-128">Atsargų atnaujinimų nurodymas</span><span class="sxs-lookup"><span data-stu-id="c1f15-128">Define the inventory updates</span></span>
1. <span data-ttu-id="c1f15-129">Lauke Produkto tipas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="c1f15-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="c1f15-130">Atkreipkite dėmesį, kad perkėlimas nepakeičia produkto tipo.</span><span class="sxs-lookup"><span data-stu-id="c1f15-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="c1f15-131">Galite perkelti baigtus arba pusiau baigtus produktus (perkėlimas tarp dviejų gamybos eigos veiklų ir galbūt „kanban“ srauto).</span><span class="sxs-lookup"><span data-stu-id="c1f15-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="c1f15-132">Perkeldami baigtus produktus galite pasirinkti, ar paimant arba gaunant pradedama atsargų operacija.</span><span class="sxs-lookup"><span data-stu-id="c1f15-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="c1f15-133">Perkėlimo vietų nurodymas</span><span class="sxs-lookup"><span data-stu-id="c1f15-133">Define the transfer locations</span></span>
1. <span data-ttu-id="c1f15-134">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="c1f15-134">Click Next.</span></span>
2. <span data-ttu-id="c1f15-135">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="c1f15-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c1f15-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c1f15-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c1f15-138">Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c1f15-139">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c1f15-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c1f15-140">Lauke Transportuoja pasirinkite „Siuntėjas“.</span><span class="sxs-lookup"><span data-stu-id="c1f15-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="c1f15-141">Galimos pasirinktys: Siuntėjas – siuntimo sandėlį valdanti organizacija, Gavėjas – gavimo sandėlį valdanti organizacija, Vežėjas – trečiosios šalies tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="c1f15-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="c1f15-142">Jei valdanti organizacija yra tiekėjas, norint atlikti perkėlimo veiklą reikalinga subrangos sutartis.</span><span class="sxs-lookup"><span data-stu-id="c1f15-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="c1f15-143">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="c1f15-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="c1f15-144">Veiklos laikų nurodymas</span><span class="sxs-lookup"><span data-stu-id="c1f15-144">Define the activity times</span></span>
1. <span data-ttu-id="c1f15-145">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c1f15-146">Būtinas dalies Apdorojimo laikas apibrėžimas.</span><span class="sxs-lookup"><span data-stu-id="c1f15-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="c1f15-147">Apdorojimo laikas naudojamas skaičiuojant savikainą ir „kanban“ užduočių našumo laikus.</span><span class="sxs-lookup"><span data-stu-id="c1f15-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="c1f15-148">Apdorojimo laikai nenaudojami skaičiuojant pajėgumą ir suvartojimą, kurie apskaičiuojami pagal iš gamybos eigos versijos užduoties gautą ciklo laiką.</span><span class="sxs-lookup"><span data-stu-id="c1f15-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="c1f15-149">Lauke Laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f15-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="c1f15-150">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f15-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="c1f15-151">Pasirinkite Laiko vienetas.</span><span class="sxs-lookup"><span data-stu-id="c1f15-151">Select the Time unit.</span></span>
5. <span data-ttu-id="c1f15-152">Lauke Už kiekį įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f15-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="c1f15-153">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="c1f15-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c1f15-154">Laukimo eilėje laikai nebūtini.</span><span class="sxs-lookup"><span data-stu-id="c1f15-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="c1f15-155">Lauke Laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f15-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="c1f15-156">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c1f15-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="c1f15-157">Pasirinkite Laiko vienetas.</span><span class="sxs-lookup"><span data-stu-id="c1f15-157">Select the Time unit.</span></span>
10. <span data-ttu-id="c1f15-158">Lauke Už kiekį įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c1f15-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="c1f15-159">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="c1f15-159">Click Next.</span></span>
12. <span data-ttu-id="c1f15-160">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="c1f15-160">Click Finish.</span></span>
13. <span data-ttu-id="c1f15-161">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c1f15-161">Close the page.</span></span>

