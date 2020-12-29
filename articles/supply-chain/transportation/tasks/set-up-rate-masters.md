---
title: Pagrindinių tarifų nustatymas
description: Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/29/2020
ms.locfileid: "4434055"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="1047d-103">Pagrindinių tarifų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1047d-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1047d-104">Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą.</span><span class="sxs-lookup"><span data-stu-id="1047d-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="1047d-105">Pagrindinius tarifus paprastai nustato logistikos vadovas atsižvelgdamas į su vežėjais pasirašytas sutartis.</span><span class="sxs-lookup"><span data-stu-id="1047d-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="1047d-106">Šiame scenarijuje nustatysite pagrindinį tarifą oro vežėjui.</span><span class="sxs-lookup"><span data-stu-id="1047d-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="1047d-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="1047d-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="1047d-108">Nustatykite pertrūkio pagrindinius duomenis</span><span class="sxs-lookup"><span data-stu-id="1047d-108">Set up break master</span></span>

1. <span data-ttu-id="1047d-109">Eikite į **Gabenimo valdymas > Nustatymai > Reitingavimas > Pagrindinių duomenų pertraukimas**.</span><span class="sxs-lookup"><span data-stu-id="1047d-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="1047d-110">Bendrosios ribos naudojamos kainodaros struktūrai ir jos ribiniams taškams apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="1047d-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="1047d-111">Kainodaros struktūra naudoja pakopinę kainodarą, paremtą faktiniais matmenimis.</span><span class="sxs-lookup"><span data-stu-id="1047d-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="1047d-112">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1047d-112">Select **New**.</span></span>
1. <span data-ttu-id="1047d-113">Laukelyje **Pagrindinių duomenų pertraukimas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="1047d-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="1047d-114">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1047d-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="1047d-115">Laukelyje **Duomenų tipas** pasirinkite duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="1047d-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="1047d-116">Laukelyje **Palyginimas** įveskite būtiną palyginimo tipą (naudodami operatorius).</span><span class="sxs-lookup"><span data-stu-id="1047d-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="1047d-117">Laukelyje **Pertraukimo vienetas** įveskite pertraukimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="1047d-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="1047d-118">Skyriuje **Išsami informacija** sukurkite tiek pertraukimų kiek reikia kainų struktūrai.</span><span class="sxs-lookup"><span data-stu-id="1047d-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="1047d-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1047d-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="1047d-120">Nustatyti pagrindinį tarifą</span><span class="sxs-lookup"><span data-stu-id="1047d-120">Set up rate master</span></span>

1. <span data-ttu-id="1047d-121">Eikite į **Gabenimo valdymas > Nustatymai > Reitingavimas > Pagrindinių duomenų reitingavimas**.</span><span class="sxs-lookup"><span data-stu-id="1047d-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="1047d-122">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1047d-122">Select **New**.</span></span>
1. <span data-ttu-id="1047d-123">Laukelyje **Pagrindinių duomenų reitingavimas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="1047d-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="1047d-124">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1047d-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="1047d-125">Laukelyje **Reitingavimo metaduomenų ID** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="1047d-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="1047d-126">Reitingavimo metaduomenų ID nustatys duomenis būtinus pagrindinių duomenų reitingui, nes jie nustato tikėtinus metaduomenis gabenimo valdymo varikliui, kuris reitinguoja pagrindinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="1047d-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="1047d-127">Šiam pavyzdžiui, rinkitės P2P parinktį.</span><span class="sxs-lookup"><span data-stu-id="1047d-127">For this example, select the P2P option.</span></span> <span data-ttu-id="1047d-128">Ją jau nustato demontraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="1047d-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="1047d-129">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1047d-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="1047d-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1047d-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="1047d-131">Nustatyti tarifo pagrindą</span><span class="sxs-lookup"><span data-stu-id="1047d-131">Set up rate base</span></span>

1. <span data-ttu-id="1047d-132">Rinkitės **Reitinguoti pagrindinius**.</span><span class="sxs-lookup"><span data-stu-id="1047d-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="1047d-133">Tarifo pagrindas nulemia vežėjo tarifą ir gali būti naudojamas tarifų struktūrai nustatyti, nes jis nustato tarifų ribinius taškus, apibrėžtus bendrosiose ribose.</span><span class="sxs-lookup"><span data-stu-id="1047d-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="1047d-134">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1047d-134">Select **New**.</span></span>
3. <span data-ttu-id="1047d-135">Laukelyje **Reitinguoti pagrindinius** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="1047d-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="1047d-136">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1047d-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="1047d-137">Laukelyje **Pagrindinių duomenų pertraukimo** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="1047d-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1047d-138">Bendrosios ribos naudojamos kainodaros struktūrai ir jos ribiniams taškams apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="1047d-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="1047d-139">Kainodaros struktūra naudoja pakopinę kainodarą, paremtą faktiniais matmenimis.</span><span class="sxs-lookup"><span data-stu-id="1047d-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="1047d-140">Šiam pavyzdžiui, naudokite svorį.</span><span class="sxs-lookup"><span data-stu-id="1047d-140">For this example, use weight.</span></span> <span data-ttu-id="1047d-141">Ją jau nustato demontraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="1047d-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="1047d-142">Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1047d-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="1047d-143">Išpėskite **Išsamios informacijos** skyrių.</span><span class="sxs-lookup"><span data-stu-id="1047d-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="1047d-144">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1047d-144">Select **New**.</span></span>
10. <span data-ttu-id="1047d-145">Laukelyje **Pašto kodo rikiavimas pagal**, įveskite „30301".</span><span class="sxs-lookup"><span data-stu-id="1047d-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="1047d-146">Laukelyje **Pašto kodo rikiavimas į**, įveskite „30318".</span><span class="sxs-lookup"><span data-stu-id="1047d-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="1047d-147">Laukelyje **Šalies regiono rikiavimas**, įveskite „USA".</span><span class="sxs-lookup"><span data-stu-id="1047d-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="1047d-148">Laukelyje **<1 00 svarai** įveskite „100".</span><span class="sxs-lookup"><span data-stu-id="1047d-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="1047d-149">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 1 svaras.</span><span class="sxs-lookup"><span data-stu-id="1047d-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="1047d-150">Laukelyje **<5 00 svarai** įveskite „300".</span><span class="sxs-lookup"><span data-stu-id="1047d-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="1047d-151">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 5 svarai.</span><span class="sxs-lookup"><span data-stu-id="1047d-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="1047d-152">Laukelyje **<20 00 svarai** įveskite „500".</span><span class="sxs-lookup"><span data-stu-id="1047d-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="1047d-153">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 20 svarų.</span><span class="sxs-lookup"><span data-stu-id="1047d-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="1047d-154">Laukelyje **<100 00 svarai** įveskite „1000".</span><span class="sxs-lookup"><span data-stu-id="1047d-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="1047d-155">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 100 svarų.</span><span class="sxs-lookup"><span data-stu-id="1047d-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="1047d-156">Laukelyje **<1 000 00 svarai** įveskite „3000".</span><span class="sxs-lookup"><span data-stu-id="1047d-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="1047d-157">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 1000 svarų.</span><span class="sxs-lookup"><span data-stu-id="1047d-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="1047d-158">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1047d-158">Select **Save**.</span></span>
19. <span data-ttu-id="1047d-159">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1047d-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="1047d-160">Priskirti tarifo pagrindą</span><span class="sxs-lookup"><span data-stu-id="1047d-160">Assign rate base</span></span>

1. <span data-ttu-id="1047d-161">Išplėskite **Reitinguoti pagrindinius priskyrimus** skyrių.</span><span class="sxs-lookup"><span data-stu-id="1047d-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="1047d-162">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1047d-162">Select **New**.</span></span>
    * <span data-ttu-id="1047d-163">Kiekvienam pagrindiniam tarifui galite priskirti keletą tarifų pagrindų.</span><span class="sxs-lookup"><span data-stu-id="1047d-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="1047d-164">Tai sudaro galimybę kiekvienam vežėjui sukurti keletą skirtingų kainos apvalinimo taisyklių, atsižvelgiant į paskirties vietas, paslaugas ar skirtingus tarifų pagrindus.</span><span class="sxs-lookup"><span data-stu-id="1047d-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="1047d-165">Šioje procedūroje sukursite tik vieną tarifo pagrindo priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="1047d-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="1047d-166">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1047d-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="1047d-167">Laukelyje **Reitinguoti pagrindinius duomenis** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="1047d-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1047d-168">Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1047d-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="1047d-169">Laukelyje **Paslaugos** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="1047d-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="1047d-170">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="1047d-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="1047d-171">Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1047d-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="1047d-172">Laukelyje **Paėmimo pašto kodas**, įveskite „98052".</span><span class="sxs-lookup"><span data-stu-id="1047d-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="1047d-173">Nurodykite, nuo kurio pašto kodo galios šis tarifo pagrindo priskyrimas.</span><span class="sxs-lookup"><span data-stu-id="1047d-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="1047d-174">Laukelyje **Paėmimo regiono rikiavimas**, įveskite „USA".</span><span class="sxs-lookup"><span data-stu-id="1047d-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="1047d-175">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1047d-175">Select **Save**.</span></span>
