--- 
title: "Pagrindinių tarifų nustatymas"
description: "Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a3ba01bc05d130991e8a744d9026d53edf93ee20
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-rate-masters"></a><span data-ttu-id="baa78-103">Pagrindinių tarifų nustatymas</span><span class="sxs-lookup"><span data-stu-id="baa78-103">Set up rate masters</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="baa78-104">Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą.</span><span class="sxs-lookup"><span data-stu-id="baa78-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="baa78-105">Pagrindinius tarifus paprastai nustato logistikos vadovas atsižvelgdamas į su vežėjais pasirašytas sutartis.</span><span class="sxs-lookup"><span data-stu-id="baa78-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="baa78-106">Šiame scenarijuje nustatysite pagrindinį tarifą oro vežėjui.</span><span class="sxs-lookup"><span data-stu-id="baa78-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="baa78-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="baa78-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="baa78-108">Nustatyti pagrindinį tarifą</span><span class="sxs-lookup"><span data-stu-id="baa78-108">Set up rate master</span></span>
1. <span data-ttu-id="baa78-109">Pasirinkite Transportavimo valdymas > Nustatymas > Vertinimas > Pagrindinis tarifas.</span><span class="sxs-lookup"><span data-stu-id="baa78-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="baa78-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="baa78-110">Click New.</span></span>
3. <span data-ttu-id="baa78-111">Lauke „Pagrindinis tarifas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="baa78-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="baa78-112">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="baa78-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="baa78-113">Lauke „Vertinimo metaduomenų ID“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="baa78-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="baa78-114">Vertinimo metaduomenų ID nulemia pagrindiniam tarifui reikalingus duomenis, nes jis apibrėžia metaduomenis, kurie skirti šį pagrindinį tarifą naudojančiam TMS mechanizmui.</span><span class="sxs-lookup"><span data-stu-id="baa78-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="baa78-115">Šiam pavyzdžiui pasirinkite parinktį P2P</span><span class="sxs-lookup"><span data-stu-id="baa78-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="baa78-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="baa78-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="baa78-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="baa78-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="baa78-118">Nustatyti tarifo pagrindą</span><span class="sxs-lookup"><span data-stu-id="baa78-118">Set up rate base</span></span>
1. <span data-ttu-id="baa78-119">Spustelėkite „Tarifo pagrindas“.</span><span class="sxs-lookup"><span data-stu-id="baa78-119">Click Rate base.</span></span>
    * <span data-ttu-id="baa78-120">Tarifo pagrindas nulemia vežėjo tarifą ir gali būti naudojamas tarifų struktūrai nustatyti, nes jis nustato tarifų ribinius taškus, apibrėžtus bendrosiose ribose.</span><span class="sxs-lookup"><span data-stu-id="baa78-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="baa78-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="baa78-121">Click New.</span></span>
3. <span data-ttu-id="baa78-122">Lauke „Tarifo pagrindas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="baa78-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="baa78-123">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="baa78-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="baa78-124">Lauke „Bendrosios ribos“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="baa78-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="baa78-125">Bendrosios ribos naudojamos kainodaros struktūrai ir jos ribiniams taškams apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="baa78-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="baa78-126">Kainodaros struktūra naudoja pakopinę kainodarą, paremtą faktiniais matmenimis.</span><span class="sxs-lookup"><span data-stu-id="baa78-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="baa78-127">Šiam pavyzdžiui naudoti svorį</span><span class="sxs-lookup"><span data-stu-id="baa78-127">For this example, use weight</span></span>
7. <span data-ttu-id="baa78-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="baa78-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="baa78-129">Perjunkite skyriaus „Išsami informacija“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="baa78-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="baa78-130">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="baa78-130">Click New.</span></span>
10. <span data-ttu-id="baa78-131">Lauke „Pašto kodas atidavimui iš“ įveskite „30301“.</span><span class="sxs-lookup"><span data-stu-id="baa78-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="baa78-132">Lauke „Pašto kodas atidavimui į“ įveskite „30318“.</span><span class="sxs-lookup"><span data-stu-id="baa78-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="baa78-133">Lauke „Atidavimo šalis, regionas“ įveskite „JAV“.</span><span class="sxs-lookup"><span data-stu-id="baa78-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="baa78-134">Lauke „<1,00 Lbs“ įveskite „100“.</span><span class="sxs-lookup"><span data-stu-id="baa78-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="baa78-135">Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 1 svaras.</span><span class="sxs-lookup"><span data-stu-id="baa78-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="baa78-136">Lauke „< 5,00 Lbs“ įveskite „300“.</span><span class="sxs-lookup"><span data-stu-id="baa78-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="baa78-137">Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 5 svarai.</span><span class="sxs-lookup"><span data-stu-id="baa78-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="baa78-138">Lauke „< 20,00 Lbs“ įveskite „500“.</span><span class="sxs-lookup"><span data-stu-id="baa78-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="baa78-139">Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 20 svarų.</span><span class="sxs-lookup"><span data-stu-id="baa78-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="baa78-140">Lauke „< 100,00 Lbs“ įveskite „1000“.</span><span class="sxs-lookup"><span data-stu-id="baa78-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="baa78-141">Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 100 svarų.</span><span class="sxs-lookup"><span data-stu-id="baa78-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="baa78-142">Lauke „< 1.000,00 Lbs“ įveskite „3000“.</span><span class="sxs-lookup"><span data-stu-id="baa78-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="baa78-143">Įterpkite vieno lbs tarifą, jeigu bendrasis krovinio svoris mažesnis nei 1000 svarų.</span><span class="sxs-lookup"><span data-stu-id="baa78-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="baa78-144">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="baa78-144">Click Save.</span></span>
19. <span data-ttu-id="baa78-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="baa78-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="baa78-146">Priskirti tarifo pagrindą</span><span class="sxs-lookup"><span data-stu-id="baa78-146">Assign rate base</span></span>
1. <span data-ttu-id="baa78-147">Perjunkite skyriaus „Tarifo pagrindo priskyrimai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="baa78-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="baa78-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="baa78-148">Click New.</span></span>
    * <span data-ttu-id="baa78-149">Kiekvienam pagrindiniam tarifui galite priskirti keletą tarifų pagrindų.</span><span class="sxs-lookup"><span data-stu-id="baa78-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="baa78-150">Tai sudaro galimybę kiekvienam vežėjui sukurti keletą skirtingų kainos apvalinimo taisyklių, atsižvelgiant į paskirties vietas, paslaugas ar skirtingus tarifų pagrindus.</span><span class="sxs-lookup"><span data-stu-id="baa78-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="baa78-151">Šioje procedūroje sukursite tik vieną tarifo pagrindo priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="baa78-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="baa78-152">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="baa78-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="baa78-153">Lauke „Tarifo pagrindas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="baa78-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="baa78-154">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="baa78-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="baa78-155">Lauke „Paslauga“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="baa78-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="baa78-156">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="baa78-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="baa78-157">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="baa78-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="baa78-158">Lauke „Paėmimo pašto kodas“ įveskite „98052“.</span><span class="sxs-lookup"><span data-stu-id="baa78-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="baa78-159">Nurodykite, nuo kurio pašto kodo galios šis tarifo pagrindo priskyrimas.</span><span class="sxs-lookup"><span data-stu-id="baa78-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="baa78-160">Lauke „Paėmimo šalis, regionas“ įveskite „JAV“.</span><span class="sxs-lookup"><span data-stu-id="baa78-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="baa78-161">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="baa78-161">Click Save.</span></span>


