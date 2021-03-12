---
title: Gamybos užduočių sekos nustatymas gamybai
description: Šioje procedūroje kaip pavyzdys naudojami dažų produktai, kad būtų galima parodyti, kaip suplanuotų užsakymų seką nustatyti pagal spalvos ir pakuotės dydžio prioritetą.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e22c767a3de8fd937d9032a5bf285dfb4ced3d55
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981067"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="a39a9-103">Gamybos užduočių sekos nustatymas gamybai</span><span class="sxs-lookup"><span data-stu-id="a39a9-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a39a9-104">Šioje procedūroje kaip pavyzdys naudojami dažų produktai, kad būtų galima parodyti, kaip suplanuotų užsakymų seką nustatyti pagal spalvos ir pakuotės dydžio prioritetą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="a39a9-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USPI.</span><span class="sxs-lookup"><span data-stu-id="a39a9-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="a39a9-106">Ši procedūra yra skirta gamybos planuotojui.</span><span class="sxs-lookup"><span data-stu-id="a39a9-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="a39a9-107">USPI bendrojo planavimo vykdymas</span><span class="sxs-lookup"><span data-stu-id="a39a9-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="a39a9-108">Pasirinkite Bendrasis planavimas > Bendrasis planavimas > Vykdyti > Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="a39a9-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="a39a9-109">Lauke „Bendrasis planas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a39a9-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a39a9-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a39a9-111">Pasirinkite MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="a39a9-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="a39a9-112">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a39a9-112">Click OK.</span></span>
    * <span data-ttu-id="a39a9-113">Taip pradedamas bendrasis planavimas, įskaitant sekos procesą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="a39a9-114">Šis procesas gali užtrukti kelias minutes.</span><span class="sxs-lookup"><span data-stu-id="a39a9-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="a39a9-115">Suplanuotų dažų produktų užsakymų peržiūra</span><span class="sxs-lookup"><span data-stu-id="a39a9-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="a39a9-116">Pasirinkite Bendrasis planavimas > Bendrasis planavimas > Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="a39a9-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="a39a9-117">Išplėskite „FactBox‟ dalį Prekės informacija.</span><span class="sxs-lookup"><span data-stu-id="a39a9-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="a39a9-118">Išplėskite „FactBox‟ dalį Grafiko informacija.</span><span class="sxs-lookup"><span data-stu-id="a39a9-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="a39a9-119">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a39a9-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a39a9-121">Pasirinkite MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="a39a9-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="a39a9-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a39a9-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a39a9-123">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Prekės numeris pagal reikšmę P300.</span><span class="sxs-lookup"><span data-stu-id="a39a9-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="a39a9-124">Atrakinkite, norėdami slinkti į dešinę, kad matytumėte užsakymo datą ir pristatymo datą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="a39a9-125">Atkreipkite dėmesį, kad šių elementų užsakymo data yra Šiandien ir suplanuotų užsakymų pristatymo datų seka nenustatyta pagal spalvos ir pakuotės dydžio prioritetą, kaip parodyta produkto pavadinime.</span><span class="sxs-lookup"><span data-stu-id="a39a9-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="a39a9-126">Galite pelės žymeklį palaikyti virš prekės numerio ir matyti produkto pavadinimą bei prioritetą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="a39a9-127">Suplanuotų dažų užsakymų sekos nustatymas</span><span class="sxs-lookup"><span data-stu-id="a39a9-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="a39a9-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a39a9-128">Close the page.</span></span>
2. <span data-ttu-id="a39a9-129">Pasirinkite Bendrasis planavimas > Bendrasis planavimas > Sekos suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="a39a9-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="a39a9-130">Išplėskite „FactBox‟ dalį Prekės informacija.</span><span class="sxs-lookup"><span data-stu-id="a39a9-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="a39a9-131">Išplėskite „FactBox‟ dalį Grafiko informacija.</span><span class="sxs-lookup"><span data-stu-id="a39a9-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="a39a9-132">Pastaba. Čia matote, kad suplanuotų užsakymų Pradžios datos / laikos seka nustatyta pagal spalvą ir pakuotės dydį 28 dienų įkainojimo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="a39a9-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="a39a9-133">Šiuos laikotarpius apibrėžia lauko Kampanija skaičius.</span><span class="sxs-lookup"><span data-stu-id="a39a9-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="a39a9-134">Sekos suplanuoto užsakymo forma veikia kaip įprasta suplanuoto užsakymo forma, ir joje gamybos planuotojas gali tvirtinti suplanuotus užsakymus.</span><span class="sxs-lookup"><span data-stu-id="a39a9-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="a39a9-135">Pažymėkite visas eilutes.</span><span class="sxs-lookup"><span data-stu-id="a39a9-135">Mark all rows.</span></span>
6. <span data-ttu-id="a39a9-136">Spustelėkite Priimti.</span><span class="sxs-lookup"><span data-stu-id="a39a9-136">Click Accept.</span></span>
    * <span data-ttu-id="a39a9-137">Taip suplanuoti užsakymai bus atnaujinti pasirinktu sekos veiksmu – Atidėti arba Perkelti į priekį.</span><span class="sxs-lookup"><span data-stu-id="a39a9-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="a39a9-138">Suplanuotų užsakymų sekos tikrinimas</span><span class="sxs-lookup"><span data-stu-id="a39a9-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="a39a9-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a39a9-139">Close the page.</span></span>
2. <span data-ttu-id="a39a9-140">Pasirinkite Bendrasis planavimas > Bendrasis planavimas > Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="a39a9-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="a39a9-141">Išplėskite „FactBox‟ dalį Prekės informacija.</span><span class="sxs-lookup"><span data-stu-id="a39a9-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="a39a9-142">Išplėskite „FactBox‟ dalį Grafiko informacija.</span><span class="sxs-lookup"><span data-stu-id="a39a9-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="a39a9-143">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a39a9-144">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a39a9-145">Pasirinkite MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="a39a9-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="a39a9-146">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a39a9-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a39a9-147">Naudokite spartųjį filtrą, kad atfiltruotumėte lauką Prekės numeris pagal reikšmę P300.</span><span class="sxs-lookup"><span data-stu-id="a39a9-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="a39a9-148">Atkreipkite dėmesį, kad užsakymų seka dabar nustatoma pagal spalvos ir dydžio prioritetą, o suplanuoti užsakymai pradedami anksčiausią užsakymo datą ir pristatymo datą.</span><span class="sxs-lookup"><span data-stu-id="a39a9-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="a39a9-149">Stulpelį Užsakymo data arba pradžios datą galite patikrinti „FactBox‟ dalyje Grafiko informacija.</span><span class="sxs-lookup"><span data-stu-id="a39a9-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

