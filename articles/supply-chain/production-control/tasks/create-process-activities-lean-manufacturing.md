---
title: Kurti „lean manufacturing“ proceso veiklas
description: Sukurkite „lean manufacturing“ proceso veiklą.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup, PlanActivityDetails, KanbanJobPickingListPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd505446456791b26850d676722b6676b50dca4b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981211"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="0d085-103">Kurti „lean manufacturing“ proceso veiklas</span><span class="sxs-lookup"><span data-stu-id="0d085-103">Create process activities for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d085-104">Sukurkite „lean manufacturing“ proceso veiklą.</span><span class="sxs-lookup"><span data-stu-id="0d085-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="0d085-105">Išankstiniai reikalavimai:</span><span class="sxs-lookup"><span data-stu-id="0d085-105">Prerequisites:</span></span> 

1. <span data-ttu-id="0d085-106">Turi būti sukurta gamybos eiga ir neaktyvi versija.</span><span class="sxs-lookup"><span data-stu-id="0d085-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="0d085-107">Turi būti sukurtas darbo elementas.</span><span class="sxs-lookup"><span data-stu-id="0d085-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="0d085-108">Kaip rasti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="0d085-108">Find the production flow version</span></span>
1. <span data-ttu-id="0d085-109">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="0d085-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="0d085-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0d085-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0d085-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0d085-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="0d085-112">Naujos veiklos kūrimas</span><span class="sxs-lookup"><span data-stu-id="0d085-112">Create a new activity</span></span>
1. <span data-ttu-id="0d085-113">Spustelėkite Veiklos.</span><span class="sxs-lookup"><span data-stu-id="0d085-113">Click Activities.</span></span>
    * <span data-ttu-id="0d085-114">Užtikrinkite, kad pasirinkta gamybos eiga turi juodraščio versiją ir pasirinkite tą versiją.</span><span class="sxs-lookup"><span data-stu-id="0d085-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="0d085-115">Spustelėkite Kurti naują plano veiklą.</span><span class="sxs-lookup"><span data-stu-id="0d085-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="0d085-116">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="0d085-116">Click Next.</span></span>
4. <span data-ttu-id="0d085-117">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0d085-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0d085-118">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0d085-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="0d085-119">Atkreipkite dėmesį, kad pavadinimas turi būti unikalus visų versijų duotai gamybos eigai.</span><span class="sxs-lookup"><span data-stu-id="0d085-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="0d085-120">Lauke Proceso kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d085-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="0d085-121">Nepamirškite, kad nepriklausomai nuo to, koks užduoties kiekis bus apdorojamas, tai mažiausias darbo kiekis darbo išlaidoms apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="0d085-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="0d085-122">Jei darbo kiekis skiriasi nuo šio kiekio, bus sukurtas darbo išlaidų nuokrypis.</span><span class="sxs-lookup"><span data-stu-id="0d085-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="0d085-123">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="0d085-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="0d085-124">Kaip pasirinkti darbo elementą</span><span class="sxs-lookup"><span data-stu-id="0d085-124">Select the work cell</span></span>
1. <span data-ttu-id="0d085-125">Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0d085-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="0d085-126">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0d085-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="0d085-127">Atsargų atnaujinimų nurodymas</span><span class="sxs-lookup"><span data-stu-id="0d085-127">Define the inventory updates</span></span>
1. <span data-ttu-id="0d085-128">Pažymėkite arba išvalykite žymės langelį Atnaujinti gautas turimas atsargas.</span><span class="sxs-lookup"><span data-stu-id="0d085-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="0d085-129">Jei atliekamas veiksmas Atnaujinti turimas atsargas = Ne, galite nurodyti veiklą ir gauti pusiau baigtą produktą (veikla nepatenka į kitą KS lygį).</span><span class="sxs-lookup"><span data-stu-id="0d085-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="0d085-130">Taip pat galite pasirinkti naudoti pusiau baigtus produktus.</span><span class="sxs-lookup"><span data-stu-id="0d085-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="0d085-131">Išrinkimo veiklų nurodymas</span><span class="sxs-lookup"><span data-stu-id="0d085-131">Define the picking activities</span></span>
1. <span data-ttu-id="0d085-132">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="0d085-132">Click Next.</span></span>
2. <span data-ttu-id="0d085-133">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0d085-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0d085-134">Sukuriama pasirinkto darbo elemento įvesties vietos numatytoji išrinkimo veikla.</span><span class="sxs-lookup"><span data-stu-id="0d085-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="0d085-135">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="0d085-135">Click Add.</span></span>
    * <span data-ttu-id="0d085-136">Galite sukurti papildomų išrinkimo veiklų, skirtų konkretiems darbo elemento įvesties veikloje nesuskirstytiems produktams.</span><span class="sxs-lookup"><span data-stu-id="0d085-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="0d085-137">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0d085-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="0d085-138">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0d085-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="0d085-139">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0d085-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0d085-140">Šiuo apibrėžimu visos veikloje suvartotos medžiagos, išskyrus antrojoje išrinkimo veikloje nurodytą prekę, paimamos iš numatytojo įvesties sandėlio ir vietos.</span><span class="sxs-lookup"><span data-stu-id="0d085-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="0d085-141">Ši prekė bus paimta iš kito sandėlio ir kitos vietos.</span><span class="sxs-lookup"><span data-stu-id="0d085-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="0d085-142">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0d085-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="0d085-143">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0d085-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0d085-144">Pažymėkite arba išvalykite žymės langelį Registruoti nurašymus.</span><span class="sxs-lookup"><span data-stu-id="0d085-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="0d085-145">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="0d085-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="0d085-146">Veiklos laikų nurodymas</span><span class="sxs-lookup"><span data-stu-id="0d085-146">Define the activity times</span></span>
1. <span data-ttu-id="0d085-147">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0d085-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0d085-148">Būtinas dalies Apdorojimo laikas apibrėžimas.</span><span class="sxs-lookup"><span data-stu-id="0d085-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="0d085-149">Apdorojimo laikas naudojamas skaičiuojant išlaidas ir „kanban“ užduočių našumo laikus.</span><span class="sxs-lookup"><span data-stu-id="0d085-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="0d085-150">Apdorojimo laikai nenaudojami skaičiuojant pajėgumą ir suvartojimą, nes tai apskaičiuojama pagal iš gamybos eigos versijos užduoties gautą ciklo laiką.</span><span class="sxs-lookup"><span data-stu-id="0d085-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="0d085-151">Lauke Laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d085-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="0d085-152">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0d085-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="0d085-153">Pasirinkite Laiko vienetas.</span><span class="sxs-lookup"><span data-stu-id="0d085-153">Select the Time unit.</span></span>
5. <span data-ttu-id="0d085-154">Lauke Už kiekį įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d085-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="0d085-155">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="0d085-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0d085-156">Laukimo eilėje laikai nebūtini.</span><span class="sxs-lookup"><span data-stu-id="0d085-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="0d085-157">Lauke Laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d085-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="0d085-158">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0d085-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="0d085-159">Pasirinkite Laiko vienetas.</span><span class="sxs-lookup"><span data-stu-id="0d085-159">Select the Time unit.</span></span>
10. <span data-ttu-id="0d085-160">Lauke Už kiekį įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0d085-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="0d085-161">Spustelėkite Pirmyn.</span><span class="sxs-lookup"><span data-stu-id="0d085-161">Click Next.</span></span>
12. <span data-ttu-id="0d085-162">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="0d085-162">Click Finish.</span></span>
13. <span data-ttu-id="0d085-163">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0d085-163">Close the page.</span></span>

