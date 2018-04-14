--- 
title: "Paketinio užsakymo ciklas nuo sukūrimo iki apdorojimo"
description: "Šioje procedūroje pamatysite pirmąją paketinio užsakymo ciklo dalį."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7f7198ea7f752fbb4aa40e4a39f2c75a205b09ca
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="abeb4-103">Paketinio užsakymo ciklas nuo sukūrimo iki apdorojimo</span><span class="sxs-lookup"><span data-stu-id="abeb4-103">Batch order lifecycle from create to start</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="abeb4-104">Šioje procedūroje pamatysite pirmąją paketinio užsakymo ciklo dalį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="abeb4-105">Nuo kūrimo, savikainos įvertinimo ir gamybos užduoties planavimo iki faktinio paketinio užsakymo paleidimo.</span><span class="sxs-lookup"><span data-stu-id="abeb4-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="abeb4-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="abeb4-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="abeb4-107">Būtina šios procedūros vykdymo sąlyga su kitu duomenų rinkiniu yra patvirtintas produktas su aktyvia formule ir maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="abeb4-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="abeb4-108">Kurti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="abeb4-108">Create a batch order</span></span>
1. <span data-ttu-id="abeb4-109">Eikite į Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="abeb4-109">Go to All production orders.</span></span>
2. <span data-ttu-id="abeb4-110">Spustelėkite Naujas paketinis užsakymas.</span><span class="sxs-lookup"><span data-stu-id="abeb4-110">Click New batch order.</span></span>
3. <span data-ttu-id="abeb4-111">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="abeb4-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="abeb4-112">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="abeb4-112">Click Create.</span></span>
5. <span data-ttu-id="abeb4-113">Naudodami spartųjį filtrą filtruokite lauką Gamyba verte 'b'.</span><span class="sxs-lookup"><span data-stu-id="abeb4-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="abeb4-114">Peržiūrėti gamybos formulę ir numatomus sudėtinius produktus</span><span class="sxs-lookup"><span data-stu-id="abeb4-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="abeb4-115">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="abeb4-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="abeb4-116">Spustelėkite Formulė.</span><span class="sxs-lookup"><span data-stu-id="abeb4-116">Click Formula.</span></span>
3. <span data-ttu-id="abeb4-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-117">Close the page.</span></span>
4. <span data-ttu-id="abeb4-118">Spustelėkite Sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="abeb4-118">Click Co-products.</span></span>
5. <span data-ttu-id="abeb4-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="abeb4-120">Įvertinti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="abeb4-120">Estimate the batch order</span></span>
1. <span data-ttu-id="abeb4-121">Spustelėkite Įvertinti.</span><span class="sxs-lookup"><span data-stu-id="abeb4-121">Click Estimate.</span></span>
2. <span data-ttu-id="abeb4-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="abeb4-122">Click OK.</span></span>
3. <span data-ttu-id="abeb4-123">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="abeb4-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="abeb4-124">Spustelėkite Peržiūrėti skaičiavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="abeb4-124">Click View calculation details.</span></span>
5. <span data-ttu-id="abeb4-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="abeb4-126">Patvirtinti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="abeb4-126">Release the batch order</span></span>
1. <span data-ttu-id="abeb4-127">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="abeb4-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="abeb4-128">Spustelėkite Išleisti.</span><span class="sxs-lookup"><span data-stu-id="abeb4-128">Click Release.</span></span>
3. <span data-ttu-id="abeb4-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="abeb4-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="abeb4-130">Planuoti gamybos užduotis</span><span class="sxs-lookup"><span data-stu-id="abeb4-130">Schedule production jobs</span></span>
1. <span data-ttu-id="abeb4-131">Veiksmų srityje spustelėkite Grafikas.</span><span class="sxs-lookup"><span data-stu-id="abeb4-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="abeb4-132">Spustelėkite Planuoti užduotis.</span><span class="sxs-lookup"><span data-stu-id="abeb4-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="abeb4-133">Lauke Ribotas pajėgumas pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="abeb4-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="abeb4-134">Lauke Ribotos medžiagos pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="abeb4-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="abeb4-135">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="abeb4-135">Click OK.</span></span>
6. <span data-ttu-id="abeb4-136">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="abeb4-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="abeb4-137">Spustelėkite Visos užduotys.</span><span class="sxs-lookup"><span data-stu-id="abeb4-137">Click All jobs.</span></span>
8. <span data-ttu-id="abeb4-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="abeb4-139">Paleisti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="abeb4-139">Start the batch order</span></span>
1. <span data-ttu-id="abeb4-140">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="abeb4-140">Click Start.</span></span>
2. <span data-ttu-id="abeb4-141">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="abeb4-141">Click the General tab.</span></span>
3. <span data-ttu-id="abeb4-142">Lauke Registruoti išrinkimo dokumentą dabar pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="abeb4-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="abeb4-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="abeb4-143">Click OK.</span></span>
5. <span data-ttu-id="abeb4-144">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="abeb4-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="abeb4-145">Spustelėkite Išrinkimo dokumentas.</span><span class="sxs-lookup"><span data-stu-id="abeb4-145">Click Picking list.</span></span>
7. <span data-ttu-id="abeb4-146">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="abeb4-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="abeb4-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-147">Close the page.</span></span>
9. <span data-ttu-id="abeb4-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-148">Close the page.</span></span>
10. <span data-ttu-id="abeb4-149">Spustelėkite Technologinė kortelė.</span><span class="sxs-lookup"><span data-stu-id="abeb4-149">Click Route card.</span></span>
11. <span data-ttu-id="abeb4-150">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="abeb4-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="abeb4-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-151">Close the page.</span></span>
13. <span data-ttu-id="abeb4-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="abeb4-152">Close the page.</span></span>


