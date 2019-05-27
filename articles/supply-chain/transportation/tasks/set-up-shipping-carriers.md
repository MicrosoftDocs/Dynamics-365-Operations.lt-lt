---
title: Siuntų vežėjų nustatymas
description: Ši procedūra nurodo, kaip nustatyti siuntų vežėją ir nurodyti kitą informaciją, tokią kaip paslauga, siuntimo būdas, transportavimo mokėjimo priemonė, transportavimo apribojimai ir siuntimo tarifas.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569107"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="a8839-103">Siuntų vežėjų nustatymas</span><span class="sxs-lookup"><span data-stu-id="a8839-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a8839-104">Ši procedūra nurodo, kaip nustatyti siuntų vežėją ir nurodyti kitą informaciją, tokią kaip paslauga, siuntimo būdas, transportavimo mokėjimo priemonė, transportavimo apribojimai ir siuntimo tarifas.</span><span class="sxs-lookup"><span data-stu-id="a8839-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="a8839-105">Transportavimo koordinatorius tada gali priskirti siuntų vežėją gaunamam arba siunčiamam kroviniui.</span><span class="sxs-lookup"><span data-stu-id="a8839-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="a8839-106">Kurti naują siuntų vežėją</span><span class="sxs-lookup"><span data-stu-id="a8839-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="a8839-107">Pasirinkite Transportavimo valdymas > Nustatymas > Vežėjai > Siuntų vežėjai.</span><span class="sxs-lookup"><span data-stu-id="a8839-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="a8839-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a8839-108">Click New.</span></span>
3. <span data-ttu-id="a8839-109">Lauke „Siuntų vežėjas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8839-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="a8839-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8839-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a8839-111">Lauke „Režimas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a8839-112">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8839-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a8839-113">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="a8839-114">Įvesti bendrą siuntų vežėjo informaciją</span><span class="sxs-lookup"><span data-stu-id="a8839-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="a8839-115">Perjunkite skyriaus „Apžvalga“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a8839-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="a8839-116">Pažymėkite arba atžymėkite žymės langelį „Suaktyvinti siuntų vežėją“.</span><span class="sxs-lookup"><span data-stu-id="a8839-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="a8839-117">Lauke „Tiekėjas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a8839-118">Pasirinkite tiekėjo sąskaitą, kad priskirtumėte siuntų vežėjui.</span><span class="sxs-lookup"><span data-stu-id="a8839-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="a8839-119">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8839-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a8839-120">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a8839-121">Lauke „Transportavimo mokėjimo priemonės tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="a8839-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="a8839-122">Pasirinkite vadovą, kad galėtumėte naudoti transportavimo mokėjimo priemonės puslapį, arba pasirinkite EDI, kad atnaujintumėte mokėjimo priemonę naudodami elektroninių duomenų mainus (EDI).</span><span class="sxs-lookup"><span data-stu-id="a8839-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="a8839-123">Pažymėkite arba atžymėkite žymės langelį „Suaktyvinti vežėjo vertinimą“.</span><span class="sxs-lookup"><span data-stu-id="a8839-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="a8839-124">Sukurti siuntų vežėjui būtinas paslaugas</span><span class="sxs-lookup"><span data-stu-id="a8839-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="a8839-125">Perjunkite skyriaus „Paslaugos“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a8839-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="a8839-126">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a8839-126">Click New.</span></span>
3. <span data-ttu-id="a8839-127">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a8839-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a8839-128">Lauke „Vežėjo paslauga“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8839-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="a8839-129">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8839-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="a8839-130">Lauke „Transportavimo metodas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a8839-131">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8839-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a8839-132">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="a8839-133">Nustatyti vežėjo adresą (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="a8839-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="a8839-134">Perjunkite dalies Adresai išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a8839-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="a8839-135">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a8839-135">Click New.</span></span>
3. <span data-ttu-id="a8839-136">Lauke Pavadinimas arba aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8839-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="a8839-137">Lauke „Šalis / Regionas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a8839-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a8839-139">Lauke „Pašto kodas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a8839-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8839-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a8839-141">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a8839-142">Lauke Gatvė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8839-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="a8839-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a8839-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="a8839-144">Nustatyti siuntų vežėjo vertinimo šabloną</span><span class="sxs-lookup"><span data-stu-id="a8839-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="a8839-145">Perjunkite skyriaus „Vertinimo šablonai“ išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="a8839-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="a8839-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a8839-146">Click New.</span></span>
3. <span data-ttu-id="a8839-147">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a8839-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a8839-148">Lauke „Vertinimo profilis“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8839-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="a8839-149">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a8839-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="a8839-150">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a8839-151">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8839-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a8839-152">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a8839-153">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="a8839-154">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8839-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="a8839-155">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="a8839-156">Lauke „Tarifų mechanizmas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a8839-157">Pasirinkite tarifų mechanizmą, kuris atitinka jūsų sutartį su vežėju.</span><span class="sxs-lookup"><span data-stu-id="a8839-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="a8839-158">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8839-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a8839-159">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="a8839-160">Lauke „Pagrindinis tarifas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="a8839-161">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a8839-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="a8839-162">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="a8839-163">Lauke „Tranzito laiko mechanizmas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a8839-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="a8839-164">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a8839-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="a8839-165">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a8839-165">Click Save.</span></span>

