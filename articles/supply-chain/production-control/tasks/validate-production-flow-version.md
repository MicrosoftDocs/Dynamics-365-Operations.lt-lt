--- 
title: "Patikrinti gamybos eigą ir versiją"
description: "Ši procedūra nurodo, kaip sukurti naują gamybos eigą ir pirmąją „lean manufacturing“ versiją."
author: ChristianRytt
manager: AnnBe
ms.date: 02/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7fb52291f15bfe9063b2a9d4a572dcdc44286402
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="c6599-103">Patikrinti gamybos eigą ir versiją</span><span class="sxs-lookup"><span data-stu-id="c6599-103">Validate a production flow and version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6599-104">Ši procedūra nurodo, kaip sukurti naują gamybos eigą ir pirmąją „lean manufacturing“ versiją.</span><span class="sxs-lookup"><span data-stu-id="c6599-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="c6599-105">Būtinos sąlygos: turi būti nurodyti „lean manufacturing“ parametrai ir klasės laiko matavimo vienetai.</span><span class="sxs-lookup"><span data-stu-id="c6599-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="c6599-106">Būtina nurodyti vertės srautą ir gamybos grupę.</span><span class="sxs-lookup"><span data-stu-id="c6599-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="c6599-107">Žr. „Lean manufacturing“ techninę dokumentaciją, kad susipažintumėte su gamybos eigos koncepcijomis ir veiklomis.</span><span class="sxs-lookup"><span data-stu-id="c6599-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="c6599-108">Ši procedūra taikoma juridiniams subjektui USMF ir demonstraciniams duomenims.</span><span class="sxs-lookup"><span data-stu-id="c6599-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="c6599-109">Tačiau jeigu juridinis subjektas sukonfigūruotas „Lean manufacturing“, gali būti naudojami kiti juridiniai subjektai.</span><span class="sxs-lookup"><span data-stu-id="c6599-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="c6599-110">Gamybos eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="c6599-110">Create a production flow</span></span>
1. <span data-ttu-id="c6599-111">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="c6599-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c6599-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c6599-112">Click New.</span></span>
3. <span data-ttu-id="c6599-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c6599-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c6599-114">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c6599-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c6599-115">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="c6599-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c6599-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c6599-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c6599-117">Vertės srautas yra valdymo vienetas, kuris apima visas veiklas ir vertės srauto eigas.</span><span class="sxs-lookup"><span data-stu-id="c6599-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="c6599-118">Šiame etape valdymo vienetai yra tik juridinis subjektas ir jiems nepriskirta jokia kita funkcija.</span><span class="sxs-lookup"><span data-stu-id="c6599-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="c6599-119">Lauke Gamybos grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="c6599-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c6599-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c6599-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c6599-121">Gamybos grupės leidžia apibrėžti gamybos proceso medžiagą, darbą ir NG sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="c6599-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="c6599-122">Norint susieti apskaitos kontekstą su gamybos eiga, reikia pasirinkti gamybos grupę.</span><span class="sxs-lookup"><span data-stu-id="c6599-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="c6599-123">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c6599-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="c6599-124">Kurti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="c6599-124">Create a production flow version</span></span>
1. <span data-ttu-id="c6599-125">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="c6599-125">Click Add.</span></span>
2. <span data-ttu-id="c6599-126">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="c6599-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="c6599-127">Galite atnaujinti versijos galiojimo datą bet kuriuo metu, net ir aktyvioms versijoms.</span><span class="sxs-lookup"><span data-stu-id="c6599-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="c6599-128">Naudokite versijos galiojimo datą planuodami palaipsniui ją pašalinti.</span><span class="sxs-lookup"><span data-stu-id="c6599-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="c6599-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c6599-129">Click OK.</span></span>
4. <span data-ttu-id="c6599-130">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c6599-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="c6599-131">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c6599-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="c6599-132">Pasirinkite Vieneto gamybos laiko vienetas.</span><span class="sxs-lookup"><span data-stu-id="c6599-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="c6599-133">Lauke Vidutinis vieneto gamybos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c6599-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="c6599-134">Nurodykite gamybos eigos versijos vieneto gamybos kontrolės numatomą vidutinį vieneto gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="c6599-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="c6599-135">Vieneto gamybos laikas yra apibrėžiamas kaip kiekis per laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="c6599-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="c6599-136">Pateiktame pavyzdyje vieneto gamybos laikas yra 10 vienetų per 0,2 valandos.</span><span class="sxs-lookup"><span data-stu-id="c6599-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="c6599-137">Kai darbo laikas yra 8 valandos, našumo pajėgumas yra 400 vienetų per dieną.</span><span class="sxs-lookup"><span data-stu-id="c6599-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="c6599-138">Lauke Ciklo kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c6599-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="c6599-139">Išplėskite arba sutraukite skyrių Versijos informacija.</span><span class="sxs-lookup"><span data-stu-id="c6599-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="c6599-140">Lauke Trumpiausias vieneto gamybos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c6599-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="c6599-141">Trumpiausias vieneto gamybos laikas turi būti trumpesnis negu vidutinis vieneto gamybos laikas arba jam lygus.</span><span class="sxs-lookup"><span data-stu-id="c6599-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="c6599-142">Lauke Ilgiausias vieneto gamybos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c6599-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="c6599-143">Ilgiausias vieneto gamybos laikas turi būti ilgesnis negu vidutinis vieneto gamybos laikas arba jam lygus.</span><span class="sxs-lookup"><span data-stu-id="c6599-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="c6599-144">Dalyje Faktinio ciklo laiko laikotarpis įveskite dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="c6599-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="c6599-145">Faktinio ciklo laiko laikotarpis yra dienų skaičius, per kurias sujungiamos užduotys nuo faktinės minutės atgal, kad būtų galima apskaičiuoti faktinį ciklo laiką.</span><span class="sxs-lookup"><span data-stu-id="c6599-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="c6599-146">Reikšmę galima pakeisti bet kuriuo metu ir ji naudojama tik skaičiuojant faktinius ciklo laikus.</span><span class="sxs-lookup"><span data-stu-id="c6599-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="c6599-147">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="c6599-147">Click Save.</span></span>

