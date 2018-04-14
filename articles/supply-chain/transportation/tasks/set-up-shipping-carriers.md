--- 
title: "Siuntų vežėjų nustatymas"
description: "Ši procedūra nurodo, kaip nustatyti siuntų vežėją ir nurodyti kitą informaciją, tokią kaip paslauga, siuntimo būdas, transportavimo mokėjimo priemonė, transportavimo apribojimai ir siuntimo tarifas."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 6e9ce934016139832b474d60d7dfc2e845434da2
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="cd970-103">Siuntų vežėjų nustatymas</span><span class="sxs-lookup"><span data-stu-id="cd970-103">Set up shipping carriers</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd970-104">Ši procedūra nurodo, kaip nustatyti siuntų vežėją ir nurodyti kitą informaciją, tokią kaip paslauga, siuntimo būdas, transportavimo mokėjimo priemonė, transportavimo apribojimai ir siuntimo tarifas.</span><span class="sxs-lookup"><span data-stu-id="cd970-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="cd970-105">Transportavimo koordinatorius tada gali priskirti siuntų vežėją gaunamam arba siunčiamam kroviniui.</span><span class="sxs-lookup"><span data-stu-id="cd970-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="cd970-106">Kurti naują siuntų vežėją</span><span class="sxs-lookup"><span data-stu-id="cd970-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="cd970-107">Pasirinkite Transportavimo valdymas > Nustatymas > Vežėjai > Siuntų vežėjai.</span><span class="sxs-lookup"><span data-stu-id="cd970-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="cd970-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="cd970-108">Click New.</span></span>
3. <span data-ttu-id="cd970-109">Lauke „Siuntų vežėjas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd970-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="cd970-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd970-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cd970-111">Lauke „Režimas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="cd970-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd970-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cd970-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="cd970-114">Įvesti bendrą siuntų vežėjo informaciją</span><span class="sxs-lookup"><span data-stu-id="cd970-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="cd970-115">Perjunkite skyriaus „Apžvalga“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="cd970-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="cd970-116">Pažymėkite arba atžymėkite žymės langelį „Suaktyvinti siuntų vežėją“.</span><span class="sxs-lookup"><span data-stu-id="cd970-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="cd970-117">Lauke „Tiekėjas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cd970-118">Pasirinkite tiekėjo sąskaitą, kad priskirtumėte siuntų vežėjui.</span><span class="sxs-lookup"><span data-stu-id="cd970-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="cd970-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd970-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cd970-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cd970-121">Lauke „Transportavimo mokėjimo priemonės tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="cd970-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="cd970-122">Pasirinkite vadovą, kad galėtumėte naudoti transportavimo mokėjimo priemonės puslapį, arba pasirinkite EDI, kad atnaujintumėte mokėjimo priemonę naudodami elektroninių duomenų mainus (EDI).</span><span class="sxs-lookup"><span data-stu-id="cd970-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="cd970-123">Pažymėkite arba atžymėkite žymės langelį „Suaktyvinti vežėjo vertinimą“.</span><span class="sxs-lookup"><span data-stu-id="cd970-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="cd970-124">Sukurti siuntų vežėjui būtinas paslaugas</span><span class="sxs-lookup"><span data-stu-id="cd970-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="cd970-125">Perjunkite skyriaus „Paslaugos“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="cd970-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="cd970-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="cd970-126">Click New.</span></span>
3. <span data-ttu-id="cd970-127">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="cd970-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cd970-128">Lauke „Vežėjo paslauga“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd970-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="cd970-129">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd970-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="cd970-130">Lauke „Transportavimo metodas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cd970-131">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd970-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cd970-132">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="cd970-133">Nustatyti vežėjo adresą (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="cd970-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="cd970-134">Perjunkite dalies Adresai išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="cd970-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="cd970-135">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="cd970-135">Click New.</span></span>
3. <span data-ttu-id="cd970-136">Lauke Pavadinimas arba aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd970-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="cd970-137">Lauke „Šalis / Regionas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cd970-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cd970-139">Lauke „Pašto kodas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cd970-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd970-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cd970-141">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cd970-142">Lauke Gatvė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd970-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="cd970-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="cd970-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="cd970-144">Nustatyti siuntų vežėjo vertinimo šabloną</span><span class="sxs-lookup"><span data-stu-id="cd970-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="cd970-145">Perjunkite skyriaus „Vertinimo šablonai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="cd970-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="cd970-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="cd970-146">Click New.</span></span>
3. <span data-ttu-id="cd970-147">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="cd970-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cd970-148">Lauke „Vertinimo profilis“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd970-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="cd970-149">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd970-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="cd970-150">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cd970-151">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd970-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="cd970-152">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cd970-153">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="cd970-154">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd970-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="cd970-155">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="cd970-156">Lauke „Tarifų mechanizmas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="cd970-157">Pasirinkite tarifų mechanizmą, kuris atitinka jūsų sutartį su vežėju.</span><span class="sxs-lookup"><span data-stu-id="cd970-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="cd970-158">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd970-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="cd970-159">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="cd970-160">Lauke „Pagrindinis tarifas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="cd970-161">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="cd970-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="cd970-162">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="cd970-163">Lauke „Tranzito laiko mechanizmas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="cd970-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="cd970-164">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd970-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="cd970-165">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="cd970-165">Click Save.</span></span>


