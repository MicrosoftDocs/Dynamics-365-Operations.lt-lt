---
title: Pagrindinių tarifų nustatymas
description: Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą.
author: ShylaThompson
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb25726e05f11420c7355c39f7e262abca5da62
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808995"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="7dd09-103">Pagrindinių tarifų nustatymas</span><span class="sxs-lookup"><span data-stu-id="7dd09-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7dd09-104">Ši procedūra nurodo, kaip nustatyti pagrindinį tarifą.</span><span class="sxs-lookup"><span data-stu-id="7dd09-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="7dd09-105">Pagrindinius tarifus paprastai nustato logistikos vadovas atsižvelgdamas į su vežėjais pasirašytas sutartis.</span><span class="sxs-lookup"><span data-stu-id="7dd09-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="7dd09-106">Šiame scenarijuje nustatysite pagrindinį tarifą oro vežėjui.</span><span class="sxs-lookup"><span data-stu-id="7dd09-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="7dd09-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="7dd09-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="7dd09-108">Nustatykite pertrūkio pagrindinius duomenis</span><span class="sxs-lookup"><span data-stu-id="7dd09-108">Set up break master</span></span>

1. <span data-ttu-id="7dd09-109">Eikite į **Gabenimo valdymas > Nustatymai > Reitingavimas > Pagrindinių duomenų pertraukimas**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="7dd09-110">Bendrosios ribos naudojamos kainodaros struktūrai ir jos ribiniams taškams apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="7dd09-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="7dd09-111">Kainodaros struktūra naudoja pakopinę kainodarą, paremtą faktiniais matmenimis.</span><span class="sxs-lookup"><span data-stu-id="7dd09-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="7dd09-112">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-112">Select **New**.</span></span>
1. <span data-ttu-id="7dd09-113">Laukelyje **Pagrindinių duomenų pertraukimas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="7dd09-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="7dd09-114">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7dd09-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="7dd09-115">Laukelyje **Duomenų tipas** pasirinkite duomenų tipą.</span><span class="sxs-lookup"><span data-stu-id="7dd09-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="7dd09-116">Laukelyje **Palyginimas** įveskite būtiną palyginimo tipą (naudodami operatorius).</span><span class="sxs-lookup"><span data-stu-id="7dd09-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="7dd09-117">Laukelyje **Pertraukimo vienetas** įveskite pertraukimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="7dd09-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="7dd09-118">Skyriuje **Išsami informacija** sukurkite tiek pertraukimų kiek reikia kainų struktūrai.</span><span class="sxs-lookup"><span data-stu-id="7dd09-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="7dd09-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="7dd09-120">Nustatyti pagrindinį tarifą</span><span class="sxs-lookup"><span data-stu-id="7dd09-120">Set up rate master</span></span>

1. <span data-ttu-id="7dd09-121">Eikite į **Gabenimo valdymas > Nustatymai > Reitingavimas > Pagrindinių duomenų reitingavimas**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="7dd09-122">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-122">Select **New**.</span></span>
1. <span data-ttu-id="7dd09-123">Laukelyje **Pagrindinių duomenų reitingavimas** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="7dd09-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="7dd09-124">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7dd09-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="7dd09-125">Laukelyje **Reitingavimo metaduomenų ID** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="7dd09-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="7dd09-126">Reitingavimo metaduomenų ID nustatys duomenis būtinus pagrindinių duomenų reitingui, nes jie nustato tikėtinus metaduomenis gabenimo valdymo varikliui, kuris reitinguoja pagrindinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="7dd09-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="7dd09-127">Šiam pavyzdžiui, rinkitės P2P parinktį.</span><span class="sxs-lookup"><span data-stu-id="7dd09-127">For this example, select the P2P option.</span></span> <span data-ttu-id="7dd09-128">Ją jau nustato demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="7dd09-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="7dd09-129">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7dd09-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="7dd09-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="7dd09-131">Nustatyti tarifo pagrindą</span><span class="sxs-lookup"><span data-stu-id="7dd09-131">Set up rate base</span></span>

1. <span data-ttu-id="7dd09-132">Rinkitės **Reitinguoti pagrindinius**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="7dd09-133">Tarifo pagrindas nulemia vežėjo tarifą ir gali būti naudojamas tarifų struktūrai nustatyti, nes jis nustato tarifų ribinius taškus, apibrėžtus bendrosiose ribose.</span><span class="sxs-lookup"><span data-stu-id="7dd09-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="7dd09-134">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-134">Select **New**.</span></span>
3. <span data-ttu-id="7dd09-135">Laukelyje **Reitinguoti pagrindinius** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="7dd09-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="7dd09-136">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7dd09-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7dd09-137">Laukelyje **Pagrindinių duomenų pertraukimo** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="7dd09-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7dd09-138">Bendrosios ribos naudojamos kainodaros struktūrai ir jos ribiniams taškams apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="7dd09-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="7dd09-139">Kainodaros struktūra naudoja pakopinę kainodarą, paremtą faktiniais matmenimis.</span><span class="sxs-lookup"><span data-stu-id="7dd09-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="7dd09-140">Šiam pavyzdžiui, naudokite svorį.</span><span class="sxs-lookup"><span data-stu-id="7dd09-140">For this example, use weight.</span></span> <span data-ttu-id="7dd09-141">Ją jau nustato demonstraciniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="7dd09-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="7dd09-142">Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7dd09-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="7dd09-143">Išplėskite **Išsamios informacijos** skyrių.</span><span class="sxs-lookup"><span data-stu-id="7dd09-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="7dd09-144">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-144">Select **New**.</span></span>
10. <span data-ttu-id="7dd09-145">Laukelyje **Pašto kodo rikiavimas pagal**, įveskite „30301".</span><span class="sxs-lookup"><span data-stu-id="7dd09-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="7dd09-146">Laukelyje **Pašto kodo rikiavimas į**, įveskite „30318".</span><span class="sxs-lookup"><span data-stu-id="7dd09-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="7dd09-147">Laukelyje **Šalies regiono rikiavimas**, įveskite „USA".</span><span class="sxs-lookup"><span data-stu-id="7dd09-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="7dd09-148">Laukelyje **<1 00 svarai** įveskite „100".</span><span class="sxs-lookup"><span data-stu-id="7dd09-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="7dd09-149">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 1 svaras.</span><span class="sxs-lookup"><span data-stu-id="7dd09-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="7dd09-150">Laukelyje **<5 00 svarai** įveskite „300".</span><span class="sxs-lookup"><span data-stu-id="7dd09-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="7dd09-151">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 5 svarai.</span><span class="sxs-lookup"><span data-stu-id="7dd09-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="7dd09-152">Laukelyje **<20 00 svarai** įveskite „500".</span><span class="sxs-lookup"><span data-stu-id="7dd09-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="7dd09-153">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 20 svarų.</span><span class="sxs-lookup"><span data-stu-id="7dd09-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="7dd09-154">Laukelyje **<100 00 svarai** įveskite „1000".</span><span class="sxs-lookup"><span data-stu-id="7dd09-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="7dd09-155">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 100 svarų.</span><span class="sxs-lookup"><span data-stu-id="7dd09-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="7dd09-156">Laukelyje **<1 000 00 svarai** įveskite „3000".</span><span class="sxs-lookup"><span data-stu-id="7dd09-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="7dd09-157">Įveskite vertę pagal svarus, jei bendras krovinio svoris yra mažesnis nei 1000 svarų.</span><span class="sxs-lookup"><span data-stu-id="7dd09-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="7dd09-158">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-158">Select **Save**.</span></span>
19. <span data-ttu-id="7dd09-159">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7dd09-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="7dd09-160">Priskirti tarifo pagrindą</span><span class="sxs-lookup"><span data-stu-id="7dd09-160">Assign rate base</span></span>

1. <span data-ttu-id="7dd09-161">Išplėskite **Reitinguoti pagrindinius priskyrimus** skyrių.</span><span class="sxs-lookup"><span data-stu-id="7dd09-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="7dd09-162">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-162">Select **New**.</span></span>
    * <span data-ttu-id="7dd09-163">Kiekvienam pagrindiniam tarifui galite priskirti keletą tarifų pagrindų.</span><span class="sxs-lookup"><span data-stu-id="7dd09-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="7dd09-164">Tai sudaro galimybę kiekvienam vežėjui sukurti keletą skirtingų kainos apvalinimo taisyklių, atsižvelgiant į paskirties vietas, paslaugas ar skirtingus tarifų pagrindus.</span><span class="sxs-lookup"><span data-stu-id="7dd09-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="7dd09-165">Šioje procedūroje sukursite tik vieną tarifo pagrindo priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="7dd09-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="7dd09-166">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7dd09-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="7dd09-167">Laukelyje **Reitinguoti pagrindinius duomenis** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="7dd09-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7dd09-168">Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7dd09-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="7dd09-169">Laukelyje **Paslaugos** pasirinkite iškrentantį mygtuką, kad atvertumėte paiešką.</span><span class="sxs-lookup"><span data-stu-id="7dd09-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7dd09-170">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7dd09-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="7dd09-171">Šiame sąraše pasirinkite nuorodą pažymėtoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7dd09-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="7dd09-172">Laukelyje **Paėmimo pašto kodas**, įveskite „98052".</span><span class="sxs-lookup"><span data-stu-id="7dd09-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="7dd09-173">Nurodykite, nuo kurio pašto kodo galios šis tarifo pagrindo priskyrimas.</span><span class="sxs-lookup"><span data-stu-id="7dd09-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="7dd09-174">Laukelyje **Paėmimo regiono rikiavimas**, įveskite „USA".</span><span class="sxs-lookup"><span data-stu-id="7dd09-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="7dd09-175">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7dd09-175">Select **Save**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]