---
title: 'Nustatyti dalinį vietos ciklų skaičiavimo procesą '
description: Kai naudojate ciklo skaičiavimo planus skaičiavimo darbui sukurti, galite nukreipti faktines skaičiavimo operacijas, nurodydami, kad būtų skaičiuojami tik konkretūs produktai ir produkto variantai vietoj visų turimų atsargų vietoje inventorizavimo.
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: bacad87e2b9146e08e6fe16af01356954eb90574
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2019
ms.locfileid: "373412"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="fe1f0-103">Nustatyti dalinį vietos ciklų skaičiavimo procesą </span><span class="sxs-lookup"><span data-stu-id="fe1f0-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fe1f0-104">Kai naudojate ciklo skaičiavimo planus skaičiavimo darbui sukurti, galite nukreipti faktines skaičiavimo operacijas, nurodydami, kad būtų skaičiuojami tik konkretūs produktai ir produkto variantai vietoj visų turimų atsargų vietoje inventorizavimo.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="fe1f0-105">Filtruodamas konkrečius produktus, sandėlio vadovas gali sumažinti peržiūros pridėtines išlaidas, padėti išvengti konsolidavimo klaidų ir sutaupyti laiko.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="fe1f0-106">Sąrankos užduotis paprastai atlieka sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="fe1f0-107">Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="fe1f0-108">Sukurkite ciklo skaičiavimo darbo šabloną</span><span class="sxs-lookup"><span data-stu-id="fe1f0-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="fe1f0-109">Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="fe1f0-110">Lauke Darbo užsakymo tipas pasirinkite „Ciklo skaičiavimas“.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="fe1f0-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-111">Click New.</span></span>
4. <span data-ttu-id="fe1f0-112">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="fe1f0-113">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="fe1f0-114">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="fe1f0-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="fe1f0-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="fe1f0-116">Lauke „Darbo šablonas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="fe1f0-117">Lauke Darbo šablonas įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="fe1f0-118">Lauke Darbo telkinio ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="fe1f0-119">Lauke Darbo prioritetas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="fe1f0-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-120">Click Save.</span></span>
11. <span data-ttu-id="fe1f0-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-121">Click New.</span></span>
12. <span data-ttu-id="fe1f0-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="fe1f0-123">Lauke Darbo tipas pasirinkite „Skaičiavimas‟.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="fe1f0-124">Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="fe1f0-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-125">Click Save.</span></span>
16. <span data-ttu-id="fe1f0-126">Spustelėkite Darbo eilučių lūžiai.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="fe1f0-127">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-127">Click New.</span></span>
18. <span data-ttu-id="fe1f0-128">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="fe1f0-129">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="fe1f0-130">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="fe1f0-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="fe1f0-131">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-131">Click Save.</span></span>
20. <span data-ttu-id="fe1f0-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-132">Close the page.</span></span>
21. <span data-ttu-id="fe1f0-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="fe1f0-134">Sukurkite ciklo skaičiavimo planą</span><span class="sxs-lookup"><span data-stu-id="fe1f0-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="fe1f0-135">Pasirinkite Sandėlio valdymas > Nustatymai > Ciklo skaičiavimas > Ciklų skaičiavimo planai.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="fe1f0-136">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-136">Click New.</span></span>
3. <span data-ttu-id="fe1f0-137">Lauke Ciklo skaičiavimo plano ID įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="fe1f0-138">Lauke Aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fe1f0-139">Lauke Maksimalus ciklų skaičiavimo skaičius įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="fe1f0-140">Lauke Darbo šablonas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="fe1f0-141">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-141">Click New.</span></span>
8. <span data-ttu-id="fe1f0-142">Lauke Sekos numeris įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="fe1f0-143">Rūšiavimo tvarka yra nuo mažiausio iki didžiausio skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="fe1f0-144">Reikšmė turi būti didesnė už 0 (nulį).</span><span class="sxs-lookup"><span data-stu-id="fe1f0-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="fe1f0-145">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="fe1f0-146">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-146">Click Save.</span></span>
11. <span data-ttu-id="fe1f0-147">Spustelėkite Apibrėžti produkto užklausą.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-147">Click Define product query.</span></span>
12. <span data-ttu-id="fe1f0-148">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="fe1f0-149">Lauke Kriterijai įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="fe1f0-150">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-150">Click OK.</span></span>
15. <span data-ttu-id="fe1f0-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="fe1f0-151">Close the page.</span></span>

