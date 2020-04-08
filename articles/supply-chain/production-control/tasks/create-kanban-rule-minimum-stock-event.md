---
title: Kurti „kanban“ taisyklę naudojant minimalių atsargų įvykį
description: Šioje procedūroje dėmesys skiriamas sąrankai, kuri reikalinga siekiant „kanban“ taisyklę kurti pagal minimalių atsargų įvykį ir užtikrinti, kad konkrečioje vietoje visada turima konkretaus produkto.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6ca5a2e2180235e51ef569fd93ad06867c3dddae
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149325"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="bfe3b-103">Kurti „kanban“ taisyklę naudojant minimalių atsargų įvykį</span><span class="sxs-lookup"><span data-stu-id="bfe3b-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bfe3b-104">Šioje procedūroje dėmesys skiriamas sąrankai, kuri reikalinga siekiant „kanban“ taisyklę kurti pagal minimalių atsargų įvykį ir užtikrinti, kad konkrečioje vietoje visada turima konkretaus produkto.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="bfe3b-105">„Kanban“ taisyklė sukuriama, siekiant medžiagą perkelti į vietą, kai atsargų lygis būna mažesnis nei 200 vienetų.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="bfe3b-106">Vykdant iškvietimo įvykių apdorojimą, sukuriami reikiami „kanban“.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="bfe3b-107">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bfe3b-108">Ši užduotis skirta proceso inžinieriui arba vertės srauto vadovui, nes jie parengia naujos arba pakeistos prekės gamybą „lean“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="bfe3b-109">Kurti naują „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="bfe3b-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="bfe3b-110">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="bfe3b-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-111">Click New.</span></span>
3. <span data-ttu-id="bfe3b-112">Lauke Tipas pasirinkite Išėmimas.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="bfe3b-113">Šis tipas naudojamas perkėlimo „kanban‟ kurti.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="bfe3b-114">Lauke Papildymo strategija pasirinkite „Įvykis“.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="bfe3b-115">Įvykio strategija naudojama, kad pagal įvykį būtų sukurti perkėlimo „kanban‟.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="bfe3b-116">Vėliau procedūros metu perkėlimo „kanban“ suaktyvinsite naudodami atsargų papildymą.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="bfe3b-117">Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="bfe3b-118">Įveskite arba pasirinkite ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="bfe3b-119">Šios perkėlimo veiklos gavimo (išeigos) sandėlis ir vieta yra 12 – tai reiškia, kad medžiagos bus perkeltos į 12-ojo sandėlio 12-ąją vietą.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="bfe3b-120">Išplėskite skyrių Išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-120">Expand the Details section.</span></span>
7. <span data-ttu-id="bfe3b-121">Lauke Produktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="bfe3b-122">Pažymėkite M0007.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-122">Select M0007.</span></span>  
8. <span data-ttu-id="bfe3b-123">Išplėskite skyrių Įvykiai.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-123">Expand the Events section.</span></span>
9. <span data-ttu-id="bfe3b-124">Lauke Atsargų papildymo įvykis pasirinkite Paketas.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="bfe3b-125">Taip sukuriamas „kanban“, siekiant medžiagų poreikius susijusioje vietoje patenkinti iškvietimo įvykių apdorojimo metu.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="bfe3b-126">Nustatyti mažiausią galimą prekės kiekį</span><span class="sxs-lookup"><span data-stu-id="bfe3b-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="bfe3b-127">Lauke Produktas spustelėkite saitą.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="bfe3b-128">Spustelėkite, kad būtumėte nukreipti pagal saitą lauke Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="bfe3b-129">Išplėskite „FactBox“ Produkto vaizdas.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="bfe3b-130">Veiksmų srityje spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="bfe3b-131">Spustelėkite Prekės padengimas.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-131">Click Item coverage.</span></span>
6. <span data-ttu-id="bfe3b-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-132">Click New.</span></span>
7. <span data-ttu-id="bfe3b-133">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="bfe3b-134">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="bfe3b-135">Nustatykite pasirinkties Sandėlis reikšmę 12.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="bfe3b-136">Nustatyti lauko Mažiausias kiekis reikšmę į 200.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="bfe3b-137">Paleisti paketinę įvykio kūrimo užduotį</span><span class="sxs-lookup"><span data-stu-id="bfe3b-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="bfe3b-138">Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ užduoties paketinis apdorojimas > Iškvietimo įvykių apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="bfe3b-139">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-139">Click OK.</span></span>
3. <span data-ttu-id="bfe3b-140">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="bfe3b-141">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bfe3b-142">Pasirinkite anksčiau sukurtą „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="bfe3b-143">Išplėskite skyrių „Kanbans“.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="bfe3b-144">Atkreipkite dėmesį, kad „kanban“ buvo sukurtas, siekiant reikiamą medžiagą perkelti į 12-ąjį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="bfe3b-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

