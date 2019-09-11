---
title: Siuntų vežėjų nustatymas
description: Šioje temoje aprašyta, kaip nustatyti siuntų vežėją ir jo išsamią informaciją, pavyzdžiui, tarnybą, siuntimo būdą, transportavimo mokėjimo priemonę, transportavimo apribojimus ir siuntimo tarifą.
author: ShylaThompson
manager: AnnBe
ms.date: 07/19/2019
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
ms.openlocfilehash: 7a43a99e10b915f1265be14f2442069dae3a22e5
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867032"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="c0e63-103">Siuntų vežėjų nustatymas</span><span class="sxs-lookup"><span data-stu-id="c0e63-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0e63-104">Šioje temoje aprašyta, kaip nustatyti siuntų vežėją ir jo išsamią informaciją, pavyzdžiui, tarnybą, siuntimo būdą, transportavimo mokėjimo priemonę, transportavimo apribojimus ir siuntimo tarifą.</span><span class="sxs-lookup"><span data-stu-id="c0e63-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="c0e63-105">Transportavimo koordinatorius tada gali priskirti siuntų vežėją gaunamam arba siunčiamam kroviniui.</span><span class="sxs-lookup"><span data-stu-id="c0e63-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="c0e63-106">Kurti naują siuntų vežėją</span><span class="sxs-lookup"><span data-stu-id="c0e63-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="c0e63-107">Eikite į **Naršymo sritis > Moduliai > Transportavimo valdymas > Sąranka > Vežėjai > Siuntų vežėjai**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="c0e63-108">Veiksmų srityje pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="c0e63-109">Lauke **Siuntų vežėjas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c0e63-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="c0e63-110">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c0e63-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c0e63-111">Lauke **Būdas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="c0e63-112">Įvesti bendrą siuntų vežėjo informaciją</span><span class="sxs-lookup"><span data-stu-id="c0e63-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="c0e63-113">Perjunkite skyriaus **Apžvalga** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="c0e63-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="c0e63-114">Pažymėkite arba atžymėkite žymės langelį **Aktyvinti siuntų vežėją**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="c0e63-115">Lauke **Tiekėjo sąskaita** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="c0e63-116">Pasirinkite tiekėjo sąskaitą, kad priskirtumėte siuntų vežėjui.</span><span class="sxs-lookup"><span data-stu-id="c0e63-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="c0e63-117">Lauke **Transportavimo mokėjimo priemonės tipas** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="c0e63-118">Norėdami naudoti transportavimo mokėjimo priemonės puslapį pasirinkite **Neautomatinis**, o norėdami atnaujinti mokėjimo priemonę naudojant elektroninius duomenų mainus (EDI), pasirinkite **EDI**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="c0e63-119">Pažymėkite arba atžymėkite žymės langelį **Aktyvinti vežėjų vertinimą**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="c0e63-120">Sukurti siuntų vežėjui būtinas paslaugas</span><span class="sxs-lookup"><span data-stu-id="c0e63-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="c0e63-121">Perjunkite skyriaus **Paslaugos** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="c0e63-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="c0e63-122">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-122">Select **New**.</span></span>
3. <span data-ttu-id="c0e63-123">Lauke **Vežėjo tarnyba** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c0e63-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="c0e63-124">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c0e63-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c0e63-125">Lauke **Transportavimo būdas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="c0e63-126">Nustatyti vežėjo adresą (pasirinktinai)</span><span class="sxs-lookup"><span data-stu-id="c0e63-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="c0e63-127">Perjunkite skyriaus **Adresai** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="c0e63-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="c0e63-128">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-128">Select **New**.</span></span>
3. <span data-ttu-id="c0e63-129">Lauke **Pavadinimas arba aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c0e63-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="c0e63-130">Lauke **Šalis / regionas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="c0e63-131">Lauke **Pašto indeksas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="c0e63-132">Lauke **Gatvė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c0e63-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="c0e63-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="c0e63-134">Nustatyti siuntų vežėjo vertinimo šabloną</span><span class="sxs-lookup"><span data-stu-id="c0e63-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="c0e63-135">Perjunkite skyriaus **Vertinimo profiliai** išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="c0e63-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="c0e63-136">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-136">Select **New**.</span></span>
3. <span data-ttu-id="c0e63-137">Lauke **Vertinimo profilis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c0e63-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="c0e63-138">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c0e63-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="c0e63-139">Lauke **Vieta** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="c0e63-140">Lauke **Sandėlys** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="c0e63-141">Lauke **Tarifų mechanizmas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="c0e63-142">Pasirinkite tarifų mechanizmą, kuris atitinka jūsų sutartį su vežėju.</span><span class="sxs-lookup"><span data-stu-id="c0e63-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="c0e63-143">Lauke **Pagrindinis tarifas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="c0e63-144">Lauke **Tranzito laiko mechanizmas** išplečiamajame meniu pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="c0e63-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="c0e63-145">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c0e63-145">Select **Save**.</span></span>

