---
title: Paketinio užsakymo ciklas nuo sukūrimo iki apdorojimo
description: Šioje procedūroje pamatysite pirmąją paketinio užsakymo ciklo dalį.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67c44341b1c8633917f41fa82593ab66611ca1ea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255426"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="a96ce-103">Paketinio užsakymo ciklas nuo sukūrimo iki apdorojimo</span><span class="sxs-lookup"><span data-stu-id="a96ce-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a96ce-104">Šioje procedūroje pamatysite pirmąją paketinio užsakymo ciklo dalį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="a96ce-105">Nuo kūrimo, savikainos įvertinimo ir gamybos užduoties planavimo iki faktinio paketinio užsakymo paleidimo.</span><span class="sxs-lookup"><span data-stu-id="a96ce-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="a96ce-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="a96ce-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="a96ce-107">Būtina šios procedūros vykdymo sąlyga su kitu duomenų rinkiniu yra patvirtintas produktas su aktyvia formule ir maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="a96ce-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="a96ce-108">Kurti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="a96ce-108">Create a batch order</span></span>
1. <span data-ttu-id="a96ce-109">Eikite į Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="a96ce-109">Go to All production orders.</span></span>
2. <span data-ttu-id="a96ce-110">Spustelėkite Naujas paketinis užsakymas.</span><span class="sxs-lookup"><span data-stu-id="a96ce-110">Click New batch order.</span></span>
3. <span data-ttu-id="a96ce-111">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a96ce-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="a96ce-112">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="a96ce-112">Click Create.</span></span>
5. <span data-ttu-id="a96ce-113">Naudodami spartųjį filtrą filtruokite lauką Gamyba verte 'b'.</span><span class="sxs-lookup"><span data-stu-id="a96ce-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="a96ce-114">Peržiūrėti gamybos formulę ir numatomus sudėtinius produktus</span><span class="sxs-lookup"><span data-stu-id="a96ce-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="a96ce-115">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="a96ce-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="a96ce-116">Spustelėkite Formulė.</span><span class="sxs-lookup"><span data-stu-id="a96ce-116">Click Formula.</span></span>
3. <span data-ttu-id="a96ce-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-117">Close the page.</span></span>
4. <span data-ttu-id="a96ce-118">Spustelėkite Sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="a96ce-118">Click Co-products.</span></span>
5. <span data-ttu-id="a96ce-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="a96ce-120">Įvertinti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="a96ce-120">Estimate the batch order</span></span>
1. <span data-ttu-id="a96ce-121">Spustelėkite Įvertinti.</span><span class="sxs-lookup"><span data-stu-id="a96ce-121">Click Estimate.</span></span>
2. <span data-ttu-id="a96ce-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a96ce-122">Click OK.</span></span>
3. <span data-ttu-id="a96ce-123">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="a96ce-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="a96ce-124">Spustelėkite Peržiūrėti skaičiavimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="a96ce-124">Click View calculation details.</span></span>
5. <span data-ttu-id="a96ce-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="a96ce-126">Patvirtinti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="a96ce-126">Release the batch order</span></span>
1. <span data-ttu-id="a96ce-127">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="a96ce-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="a96ce-128">Spustelėkite Išleisti.</span><span class="sxs-lookup"><span data-stu-id="a96ce-128">Click Release.</span></span>
3. <span data-ttu-id="a96ce-129">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a96ce-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="a96ce-130">Planuoti gamybos užduotis</span><span class="sxs-lookup"><span data-stu-id="a96ce-130">Schedule production jobs</span></span>
1. <span data-ttu-id="a96ce-131">Veiksmų srityje spustelėkite Grafikas.</span><span class="sxs-lookup"><span data-stu-id="a96ce-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="a96ce-132">Spustelėkite Planuoti užduotis.</span><span class="sxs-lookup"><span data-stu-id="a96ce-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="a96ce-133">Lauke Ribotas pajėgumas pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="a96ce-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="a96ce-134">Lauke Ribotos medžiagos pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="a96ce-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="a96ce-135">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="a96ce-135">Click OK.</span></span>
6. <span data-ttu-id="a96ce-136">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="a96ce-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="a96ce-137">Spustelėkite Visos užduotys.</span><span class="sxs-lookup"><span data-stu-id="a96ce-137">Click All jobs.</span></span>
8. <span data-ttu-id="a96ce-138">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="a96ce-139">Paleisti paketinį užsakymą</span><span class="sxs-lookup"><span data-stu-id="a96ce-139">Start the batch order</span></span>
1. <span data-ttu-id="a96ce-140">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="a96ce-140">Click Start.</span></span>
2. <span data-ttu-id="a96ce-141">Spustelėkite skirtuką Bendra.</span><span class="sxs-lookup"><span data-stu-id="a96ce-141">Click the General tab.</span></span>
3. <span data-ttu-id="a96ce-142">Lauke Registruoti išrinkimo dokumentą dabar pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="a96ce-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="a96ce-143">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a96ce-143">Click OK.</span></span>
5. <span data-ttu-id="a96ce-144">Veiksmų srityje spustelėkite Peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="a96ce-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="a96ce-145">Spustelėkite Išrinkimo dokumentas.</span><span class="sxs-lookup"><span data-stu-id="a96ce-145">Click Picking list.</span></span>
7. <span data-ttu-id="a96ce-146">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a96ce-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a96ce-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-147">Close the page.</span></span>
9. <span data-ttu-id="a96ce-148">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-148">Close the page.</span></span>
10. <span data-ttu-id="a96ce-149">Spustelėkite Technologinė kortelė.</span><span class="sxs-lookup"><span data-stu-id="a96ce-149">Click Route card.</span></span>
11. <span data-ttu-id="a96ce-150">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a96ce-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="a96ce-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-151">Close the page.</span></span>
13. <span data-ttu-id="a96ce-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a96ce-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]