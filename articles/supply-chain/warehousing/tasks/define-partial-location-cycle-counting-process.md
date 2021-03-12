---
title: Nustatyti dalinį vietos ciklų skaičiavimo procesą
description: Kai naudojate ciklo skaičiavimo planus skaičiavimo darbui sukurti, galite nukreipti faktines skaičiavimo operacijas, nurodydami, kad būtų skaičiuojami tik konkretūs produktai ir produkto variantai vietoj visų turimų atsargų vietoje inventorizavimo.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0778cc7c1703dcfd5ea77979aafc99f4f040830d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977143"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="311bf-103">Nustatyti dalinį vietos ciklų skaičiavimo procesą</span><span class="sxs-lookup"><span data-stu-id="311bf-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="311bf-104">Kai naudojate ciklo skaičiavimo planus skaičiavimo darbui sukurti, galite nukreipti faktines skaičiavimo operacijas, nurodydami, kad būtų skaičiuojami tik konkretūs produktai ir produkto variantai vietoj visų turimų atsargų vietoje inventorizavimo.</span><span class="sxs-lookup"><span data-stu-id="311bf-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="311bf-105">Filtruodamas konkrečius produktus, sandėlio vadovas gali sumažinti peržiūros pridėtines išlaidas, padėti išvengti konsolidavimo klaidų ir sutaupyti laiko.</span><span class="sxs-lookup"><span data-stu-id="311bf-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="311bf-106">Sąrankos užduotis paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="311bf-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="311bf-107">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="311bf-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="311bf-108">Sukurkite ciklo skaičiavimo darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="311bf-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="311bf-109">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="311bf-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="311bf-110">Lauke Darbo užsakymo tipas pasirinkite „Ciklo skaičiavimas“.</span><span class="sxs-lookup"><span data-stu-id="311bf-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="311bf-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="311bf-111">Click New.</span></span>
4. <span data-ttu-id="311bf-112">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="311bf-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="311bf-113">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="311bf-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="311bf-114">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="311bf-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="311bf-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="311bf-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="311bf-116">Lauke „Darbo šablonas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="311bf-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="311bf-117">Lauke Darbo šablonas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="311bf-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="311bf-118">Lauke Darbo telkinio ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="311bf-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="311bf-119">Lauke Darbo prioritetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="311bf-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="311bf-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="311bf-120">Click Save.</span></span>
11. <span data-ttu-id="311bf-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="311bf-121">Click New.</span></span>
12. <span data-ttu-id="311bf-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="311bf-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="311bf-123">Lauke Darbo tipas pasirinkite „Skaičiavimas‟.</span><span class="sxs-lookup"><span data-stu-id="311bf-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="311bf-124">Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="311bf-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="311bf-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="311bf-125">Click Save.</span></span>
16. <span data-ttu-id="311bf-126">Spustelėkite Darbo eilučių lūžiai.</span><span class="sxs-lookup"><span data-stu-id="311bf-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="311bf-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="311bf-127">Click New.</span></span>
18. <span data-ttu-id="311bf-128">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="311bf-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="311bf-129">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="311bf-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="311bf-130">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="311bf-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="311bf-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="311bf-131">Click Save.</span></span>
20. <span data-ttu-id="311bf-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="311bf-132">Close the page.</span></span>
21. <span data-ttu-id="311bf-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="311bf-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="311bf-134">Sukurkite ciklo skaičiavimo planą</span><span class="sxs-lookup"><span data-stu-id="311bf-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="311bf-135">Pasirinkite Sandėlio valdymas > Nustatymai > Ciklo skaičiavimas > Ciklų skaičiavimo planai.</span><span class="sxs-lookup"><span data-stu-id="311bf-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="311bf-136">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="311bf-136">Click New.</span></span>
3. <span data-ttu-id="311bf-137">Lauke Ciklo skaičiavimo plano ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="311bf-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="311bf-138">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="311bf-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="311bf-139">Lauke Maksimalus ciklų skaičiavimo skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="311bf-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="311bf-140">Lauke Darbo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="311bf-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="311bf-141">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="311bf-141">Click New.</span></span>
8. <span data-ttu-id="311bf-142">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="311bf-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="311bf-143">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="311bf-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="311bf-144">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="311bf-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="311bf-145">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="311bf-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="311bf-146">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="311bf-146">Click Save.</span></span>
11. <span data-ttu-id="311bf-147">Spustelėkite Apibrėžti produkto užklausą.</span><span class="sxs-lookup"><span data-stu-id="311bf-147">Click Define product query.</span></span>
12. <span data-ttu-id="311bf-148">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="311bf-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="311bf-149">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="311bf-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="311bf-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="311bf-150">Click OK.</span></span>
15. <span data-ttu-id="311bf-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="311bf-151">Close the page.</span></span>

