---
title: Siuntų vežėjų nustatymas
description: Šioje temoje aprašyta, kaip nustatyti siuntų vežėją ir jo išsamią informaciją, pavyzdžiui, tarnybą, siuntimo būdą, transportavimo mokėjimo priemonę, transportavimo apribojimus ir siuntimo tarifą.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 124f7473cbdae8890f74115d461603f50cc58be8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004882"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="7e7ed-103">Siuntų vežėjų nustatymas</span><span class="sxs-lookup"><span data-stu-id="7e7ed-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7e7ed-104">Šioje temoje aprašyta, kaip nustatyti siuntų vežėją ir jo išsamią informaciją, pavyzdžiui, tarnybą, siuntimo būdą, transportavimo mokėjimo priemonę, transportavimo apribojimus ir siuntimo tarifą.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="7e7ed-105">Transportavimo koordinatorius tada gali priskirti siuntų vežėją gaunamam arba siunčiamam kroviniui.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="7e7ed-106">Kurti naują siuntų vežėją</span><span class="sxs-lookup"><span data-stu-id="7e7ed-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="7e7ed-107">Eikite į **Naršymo sritis > Moduliai > Transportavimo valdymas > Sąranka > Vežėjai > Siuntų vežėjai**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="7e7ed-108">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="7e7ed-109">Lauke **Siuntų vežėjas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="7e7ed-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7e7ed-111">Lauke **Būdas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="7e7ed-112">Įvesti bendrą siuntų vežėjo informaciją</span><span class="sxs-lookup"><span data-stu-id="7e7ed-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="7e7ed-113">Perjunkite skyriaus **Apžvalga** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="7e7ed-114">Pažymėkite arba atžymėkite žymės langelį **Aktyvinti siuntų vežėją**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="7e7ed-115">Lauke **Tiekėjo sąskaita** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="7e7ed-116">Pasirinkite tiekėjo sąskaitą, kad priskirtumėte siuntų vežėjui.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="7e7ed-117">Lauke **Transportavimo mokėjimo priemonės tipas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="7e7ed-118">Norėdami naudoti transportavimo mokėjimo priemonės puslapį pasirinkite **Neautomatinis**, o norėdami atnaujinti mokėjimo priemonę naudojant elektroninius duomenų mainus (EDI), pasirinkite **EDI**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="7e7ed-119">Pažymėkite arba atžymėkite žymės langelį **Aktyvinti vežėjų vertinimą**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="7e7ed-120">Sukurti siuntų vežėjui būtinas paslaugas</span><span class="sxs-lookup"><span data-stu-id="7e7ed-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="7e7ed-121">Perjunkite skyriaus **Paslaugos** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="7e7ed-122">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-122">Select **New**.</span></span>
3. <span data-ttu-id="7e7ed-123">Lauke **Vežėjo tarnyba** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="7e7ed-124">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7e7ed-125">Lauke **Transportavimo būdas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="7e7ed-126">Nustatyti vežėjo adresą (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="7e7ed-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="7e7ed-127">Perjunkite skyriaus **Adresai** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="7e7ed-128">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-128">Select **New**.</span></span>
3. <span data-ttu-id="7e7ed-129">Lauke **Pavadinimas arba aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="7e7ed-130">Lauke **Šalis / regionas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="7e7ed-131">Lauke **Pašto indeksas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="7e7ed-132">Lauke **Gatvė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="7e7ed-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="7e7ed-134">Nustatyti siuntų vežėjo vertinimo šabloną</span><span class="sxs-lookup"><span data-stu-id="7e7ed-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="7e7ed-135">Perjunkite skyriaus **Vertinimo profiliai** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="7e7ed-136">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-136">Select **New**.</span></span>
3. <span data-ttu-id="7e7ed-137">Lauke **Vertinimo profilis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="7e7ed-138">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7e7ed-139">Lauke **Vieta** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="7e7ed-140">Lauke **Sandėlys** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="7e7ed-141">Lauke **Tarifų mechanizmas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="7e7ed-142">Pasirinkite tarifų mechanizmą, kuris atitinka jūsų sutartį su vežėju.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="7e7ed-143">Lauke **Pagrindinis tarifas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="7e7ed-144">Lauke **Tranzito laiko mechanizmas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="7e7ed-145">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7e7ed-145">Select **Save**.</span></span>

