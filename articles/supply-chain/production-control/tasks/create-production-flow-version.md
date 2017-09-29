--- 
title: "Kurti gamybos eigos versiją"
description: "Šioje procedūroje dėmesys skiriamas naujos gamybos eigos versijos kūrimui."
author: cvocph
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 58b3c9cd265b97a814541315e4ba8378010eb2b2
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="8b44b-103">Kurti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="8b44b-103">Create a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b44b-104">Šioje procedūroje dėmesys skiriamas naujos gamybos eigos versijos kūrimui.</span><span class="sxs-lookup"><span data-stu-id="8b44b-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="8b44b-105">Šiai procedūrai turi būti nurodyti „lean manufacturing“ parametrai ir klasės laiko matavimo vienetai.</span><span class="sxs-lookup"><span data-stu-id="8b44b-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="8b44b-106">Taip pat būtina nurodyti vertės srautą ir gamybos grupę.</span><span class="sxs-lookup"><span data-stu-id="8b44b-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="8b44b-107">Norėdami sužinoti daugiau apie gamybos eigas ir „lean manufacturing“ veiklas, žr. „Microsoft Dynamics AX“ „Lean Manufacturing“ techninę dokumentaciją.</span><span class="sxs-lookup"><span data-stu-id="8b44b-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="8b44b-108">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="8b44b-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="8b44b-109">Gamybos eigos kūrimas</span><span class="sxs-lookup"><span data-stu-id="8b44b-109">Create a production flow</span></span>
1. <span data-ttu-id="8b44b-110">Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.</span><span class="sxs-lookup"><span data-stu-id="8b44b-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="8b44b-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8b44b-111">Click New.</span></span>
3. <span data-ttu-id="8b44b-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b44b-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8b44b-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b44b-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8b44b-114">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="8b44b-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8b44b-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8b44b-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8b44b-116">Pasirinkite vertės srauto tipo valdymo vienetą.</span><span class="sxs-lookup"><span data-stu-id="8b44b-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="8b44b-117">Vertės srautas yra valdymo vienetas, kuris apima visas veiklas ir vertės srauto srautus.</span><span class="sxs-lookup"><span data-stu-id="8b44b-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="8b44b-118">Šiame etape valdymo vienetai yra tik juridinis subjektas ir jiems nepriskirta jokia kita funkcija.</span><span class="sxs-lookup"><span data-stu-id="8b44b-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="8b44b-119">Lauke Gamybos grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="8b44b-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8b44b-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8b44b-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8b44b-121">Pasirinkite gamybos eigos gamybos grupę.</span><span class="sxs-lookup"><span data-stu-id="8b44b-121">Select a production group for the production flow.</span></span> <span data-ttu-id="8b44b-122">Gamybos grupės leidžia apibrėžti gamybos proceso medžiagą, darbą ir NG sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="8b44b-122">Production groups allow the definition of material, labour, and WIP accounts for a production process.</span></span> <span data-ttu-id="8b44b-123">Norint susieti apskaitos kontekstą su gamybos eiga, reikia pasirinkti gamybos grupę.</span><span class="sxs-lookup"><span data-stu-id="8b44b-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="8b44b-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8b44b-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="8b44b-125">Kurti gamybos eigos versiją</span><span class="sxs-lookup"><span data-stu-id="8b44b-125">Create a production flow version</span></span>
1. <span data-ttu-id="8b44b-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8b44b-126">Click Add.</span></span>
2. <span data-ttu-id="8b44b-127">Lauke Galiojimo data įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="8b44b-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="8b44b-128">Jei reikia, nurodykite versijos galiojimo datą.</span><span class="sxs-lookup"><span data-stu-id="8b44b-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="8b44b-129">Galite atnaujinti ją bet kuriuo metu, net ir aktyvioms versijoms.</span><span class="sxs-lookup"><span data-stu-id="8b44b-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="8b44b-130">Galite naudoti ją planuodami palaipsniui pašalinti versiją.</span><span class="sxs-lookup"><span data-stu-id="8b44b-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="8b44b-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="8b44b-131">Click OK.</span></span>
4. <span data-ttu-id="8b44b-132">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8b44b-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="8b44b-133">Lauke „Vienetas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8b44b-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="8b44b-134">Nustačius keičiasi vienetas.</span><span class="sxs-lookup"><span data-stu-id="8b44b-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="8b44b-135">Lauke Vidutinis vieneto gamybos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8b44b-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="8b44b-136">Nurodykite vidutinį versijos vieneto gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="8b44b-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="8b44b-137">Nurodykite gamybos eigos versijos vieneto gamybos kontrolės numatomą vidutinį vieneto gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="8b44b-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="8b44b-138">Vieneto gamybos laikas yra apibrėžiamas kaip kiekis per laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="8b44b-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="8b44b-139">Pateiktame pavyzdyje vieneto gamybos laikas yra 10 vienetų per 0,2 valandos.</span><span class="sxs-lookup"><span data-stu-id="8b44b-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="8b44b-140">Kai darbo laikas yra 8 valandos, našumo pajėgumas yra 400 vienetų per dieną.</span><span class="sxs-lookup"><span data-stu-id="8b44b-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="8b44b-141">Lauke Ciklo kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8b44b-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="8b44b-142">Nurodykite kiekį per ciklą, susijusį su vidutiniu vieneto gamybos laiku.</span><span class="sxs-lookup"><span data-stu-id="8b44b-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="8b44b-143">Perjunkite skyriaus Versijos informacija išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="8b44b-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="8b44b-144">Lauke Trumpiausias vieneto gamybos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8b44b-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="8b44b-145">Nurodykite trumpiausią vieneto gamybos laiką.</span><span class="sxs-lookup"><span data-stu-id="8b44b-145">Define the minimum takt time.</span></span> <span data-ttu-id="8b44b-146">Trumpiausias vieneto gamybos laikas turi būti trumpesnis negu vidutinis vieneto gamybos laikas arba jam lygus.</span><span class="sxs-lookup"><span data-stu-id="8b44b-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="8b44b-147">Lauke Ilgiausias vieneto gamybos laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8b44b-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="8b44b-148">Ilgiausias vieneto gamybos laikas turi būti ilgesnis negu vidutinis vieneto gamybos laikas arba jam lygus.</span><span class="sxs-lookup"><span data-stu-id="8b44b-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="8b44b-149">Dalyje Faktinio ciklo laiko laikotarpis (dienomis) įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="8b44b-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="8b44b-150">Dalyje Faktinio ciklo laiko laikotarpis įveskite dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="8b44b-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="8b44b-151">Faktinio ciklo laiko laikotarpis yra dienų skaičius, per kurias sujungiamos užduotys nuo faktinės minutės atgal, kad būtų galima apskaičiuoti faktinį ciklo laiką.</span><span class="sxs-lookup"><span data-stu-id="8b44b-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="8b44b-152">Reikšmę galima pakeisti bet kuriuo metu ir ji naudojama tik skaičiuojant faktinius ciklo laikus.</span><span class="sxs-lookup"><span data-stu-id="8b44b-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="8b44b-153">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8b44b-153">Click Save.</span></span>


