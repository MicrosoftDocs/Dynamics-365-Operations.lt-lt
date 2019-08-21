---
title: Paketinio užsakymo ciklas nuo sukūrimo iki apdorojimo
description: Šioje procedūroje pamatysite pirmąją paketinio užsakymo ciklo dalį.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a1803822bebf58a3370afe8c5dc9f519c65917d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843822"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="17b4b-103">Paketinio užsakymo ciklas nuo sukūrimo iki apdorojimo</span><span class="sxs-lookup"><span data-stu-id="17b4b-103">Batch order lifecycle from create to start</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17b4b-104">Šioje procedūroje pamatysite pirmąją paketinio užsakymo ciklo dalį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="17b4b-105">Nuo kūrimo, savikainos įvertinimo ir gamybos užduoties planavimo iki faktinio paketinio užsakymo paleidimo.</span><span class="sxs-lookup"><span data-stu-id="17b4b-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="17b4b-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="17b4b-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="17b4b-107">Būtina šios procedūros vykdymo sąlyga su kitu duomenų rinkiniu yra patvirtintas produktas su aktyvia formule ir maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="17b4b-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="17b4b-108">Kurti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="17b4b-108">Create a batch order</span></span>
1. <span data-ttu-id="17b4b-109">Eikite į Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="17b4b-109">Go to All production orders.</span></span>
2. <span data-ttu-id="17b4b-110">Spustelėkite Naujas paketinis užsakymas.</span><span class="sxs-lookup"><span data-stu-id="17b4b-110">Click New batch order.</span></span>
3. <span data-ttu-id="17b4b-111">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="17b4b-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="17b4b-112">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="17b4b-112">Click Create.</span></span>
5. <span data-ttu-id="17b4b-113">Naudodami spartųjį filtrą filtruokite lauką Gamyba verte 'b'.</span><span class="sxs-lookup"><span data-stu-id="17b4b-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="17b4b-114">Peržiūrėti gamybos formulę ir numatomus sudėtinius produktus</span><span class="sxs-lookup"><span data-stu-id="17b4b-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="17b4b-115">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="17b4b-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="17b4b-116">Spustelėkite Formulė.</span><span class="sxs-lookup"><span data-stu-id="17b4b-116">Click Formula.</span></span>
3. <span data-ttu-id="17b4b-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-117">Close the page.</span></span>
4. <span data-ttu-id="17b4b-118">Spustelėkite Sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="17b4b-118">Click Co-products.</span></span>
5. <span data-ttu-id="17b4b-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="17b4b-120">Įvertinti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="17b4b-120">Estimate the batch order</span></span>
1. <span data-ttu-id="17b4b-121">Spustelėkite Įvertinti.</span><span class="sxs-lookup"><span data-stu-id="17b4b-121">Click Estimate.</span></span>
2. <span data-ttu-id="17b4b-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="17b4b-122">Click OK.</span></span>
3. <span data-ttu-id="17b4b-123">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="17b4b-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="17b4b-124">Spustelėkite Peržiūrėti skaičiavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="17b4b-124">Click View calculation details.</span></span>
5. <span data-ttu-id="17b4b-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="17b4b-126">Patvirtinti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="17b4b-126">Release the batch order</span></span>
1. <span data-ttu-id="17b4b-127">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="17b4b-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="17b4b-128">Spustelėkite Išleisti.</span><span class="sxs-lookup"><span data-stu-id="17b4b-128">Click Release.</span></span>
3. <span data-ttu-id="17b4b-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="17b4b-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="17b4b-130">Planuoti gamybos užduotis</span><span class="sxs-lookup"><span data-stu-id="17b4b-130">Schedule production jobs</span></span>
1. <span data-ttu-id="17b4b-131">Veiksmų srityje spustelėkite Grafikas.</span><span class="sxs-lookup"><span data-stu-id="17b4b-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="17b4b-132">Spustelėkite Planuoti užduotis.</span><span class="sxs-lookup"><span data-stu-id="17b4b-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="17b4b-133">Lauke Ribotas pajėgumas pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="17b4b-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="17b4b-134">Lauke Ribotos medžiagos pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="17b4b-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="17b4b-135">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="17b4b-135">Click OK.</span></span>
6. <span data-ttu-id="17b4b-136">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="17b4b-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="17b4b-137">Spustelėkite Visos užduotys.</span><span class="sxs-lookup"><span data-stu-id="17b4b-137">Click All jobs.</span></span>
8. <span data-ttu-id="17b4b-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="17b4b-139">Paleisti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="17b4b-139">Start the batch order</span></span>
1. <span data-ttu-id="17b4b-140">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="17b4b-140">Click Start.</span></span>
2. <span data-ttu-id="17b4b-141">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="17b4b-141">Click the General tab.</span></span>
3. <span data-ttu-id="17b4b-142">Lauke Registruoti išrinkimo dokumentą dabar pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="17b4b-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="17b4b-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="17b4b-143">Click OK.</span></span>
5. <span data-ttu-id="17b4b-144">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="17b4b-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="17b4b-145">Spustelėkite Išrinkimo dokumentas.</span><span class="sxs-lookup"><span data-stu-id="17b4b-145">Click Picking list.</span></span>
7. <span data-ttu-id="17b4b-146">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="17b4b-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="17b4b-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-147">Close the page.</span></span>
9. <span data-ttu-id="17b4b-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-148">Close the page.</span></span>
10. <span data-ttu-id="17b4b-149">Spustelėkite Technologinė kortelė.</span><span class="sxs-lookup"><span data-stu-id="17b4b-149">Click Route card.</span></span>
11. <span data-ttu-id="17b4b-150">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="17b4b-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="17b4b-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-151">Close the page.</span></span>
13. <span data-ttu-id="17b4b-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="17b4b-152">Close the page.</span></span>

