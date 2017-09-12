--- 
title: "Nustatyti dalinį vietos ciklų skaičiavimo procesą "
description: "Kai naudojate ciklo skaičiavimo planus skaičiavimo darbui sukurti, galite nukreipti faktines skaičiavimo operacijas, nurodydami, kad būtų skaičiuojami tik konkretūs produktai ir produkto variantai vietoj visų turimų atsargų vietoje inventorizavimo."
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 030f0f75d64c97f1109f36c9fd38283c2d1fa7b0
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="d5745-103">Nustatyti dalinį vietos ciklų skaičiavimo procesą </span><span class="sxs-lookup"><span data-stu-id="d5745-103">Define partial location cycle counting process</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5745-104">Kai naudojate ciklo skaičiavimo planus skaičiavimo darbui sukurti, galite nukreipti faktines skaičiavimo operacijas, nurodydami, kad būtų skaičiuojami tik konkretūs produktai ir produkto variantai vietoj visų turimų atsargų vietoje inventorizavimo.</span><span class="sxs-lookup"><span data-stu-id="d5745-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="d5745-105">Filtruodamas konkrečius produktus, sandėlio vadovas gali sumažinti peržiūros pridėtines išlaidas, padėti išvengti konsolidavimo klaidų ir sutaupyti laiko.</span><span class="sxs-lookup"><span data-stu-id="d5745-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="d5745-106">Sąrankos užduotis paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="d5745-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="d5745-107">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="d5745-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="d5745-108">Sukurkite ciklo skaičiavimo darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="d5745-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="d5745-109">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="d5745-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="d5745-110">Lauke Darbo užsakymo tipas pasirinkite „Ciklo skaičiavimas“.</span><span class="sxs-lookup"><span data-stu-id="d5745-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="d5745-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d5745-111">Click New.</span></span>
4. <span data-ttu-id="d5745-112">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d5745-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="d5745-113">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="d5745-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="d5745-114">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="d5745-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="d5745-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d5745-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="d5745-116">Lauke „Darbo šablonas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5745-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="d5745-117">Lauke Darbo šablonas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="d5745-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="d5745-118">Lauke Darbo telkinio ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5745-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="d5745-119">Lauke Darbo prioritetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d5745-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="d5745-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d5745-120">Click Save.</span></span>
11. <span data-ttu-id="d5745-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d5745-121">Click New.</span></span>
12. <span data-ttu-id="d5745-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d5745-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="d5745-123">Lauke Darbo tipas pasirinkite „Skaičiavimas‟.</span><span class="sxs-lookup"><span data-stu-id="d5745-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="d5745-124">Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5745-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="d5745-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d5745-125">Click Save.</span></span>
16. <span data-ttu-id="d5745-126">Spustelėkite Darbo eilučių lūžiai.</span><span class="sxs-lookup"><span data-stu-id="d5745-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="d5745-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d5745-127">Click New.</span></span>
18. <span data-ttu-id="d5745-128">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d5745-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="d5745-129">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="d5745-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="d5745-130">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="d5745-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="d5745-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d5745-131">Click Save.</span></span>
20. <span data-ttu-id="d5745-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d5745-132">Close the page.</span></span>
21. <span data-ttu-id="d5745-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d5745-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="d5745-134">Sukurkite ciklo skaičiavimo planą</span><span class="sxs-lookup"><span data-stu-id="d5745-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="d5745-135">Pasirinkite Sandėlio valdymas > Nustatymai > Ciklo skaičiavimas > Ciklų skaičiavimo planai.</span><span class="sxs-lookup"><span data-stu-id="d5745-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="d5745-136">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d5745-136">Click New.</span></span>
3. <span data-ttu-id="d5745-137">Lauke Ciklo skaičiavimo plano ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="d5745-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="d5745-138">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5745-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d5745-139">Lauke Maksimalus ciklų skaičiavimo skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d5745-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="d5745-140">Lauke Darbo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5745-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="d5745-141">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="d5745-141">Click New.</span></span>
8. <span data-ttu-id="d5745-142">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d5745-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="d5745-143">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="d5745-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="d5745-144">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="d5745-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="d5745-145">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5745-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="d5745-146">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="d5745-146">Click Save.</span></span>
11. <span data-ttu-id="d5745-147">Spustelėkite Apibrėžti produkto užklausą.</span><span class="sxs-lookup"><span data-stu-id="d5745-147">Click Define product query.</span></span>
12. <span data-ttu-id="d5745-148">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="d5745-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="d5745-149">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d5745-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="d5745-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d5745-150">Click OK.</span></span>
15. <span data-ttu-id="d5745-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d5745-151">Close the page.</span></span>


