---
title: KS eilutės „kanban“ taisyklės kūrimas
description: Šioje užduotyje parodoma, ką ir kaip reikia nustatyti, norint sukurti įvykio „kanban“ taisyklę, siekiant užtikrinti gamybos KS eilučių tiekimą mišrioje „lean‟ ir klasikinėje gamybos aplinkoje.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6df9632d6e2798fad2b3462055a9495394583f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255282"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="c6c45-103">KS eilutės „kanban“ taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="c6c45-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6c45-104">Šioje užduotyje parodoma, ką ir kaip reikia nustatyti, norint sukurti įvykio „kanban“ taisyklę, siekiant užtikrinti gamybos KS eilučių tiekimą mišrioje „lean‟ ir klasikinėje gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="c6c45-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="c6c45-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="c6c45-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c6c45-106">Ši užduotis skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia naujos arba pakeistos prekės gamybą.</span><span class="sxs-lookup"><span data-stu-id="c6c45-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="c6c45-107">Kurti naują „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="c6c45-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="c6c45-108">Pasirinkite Gamybos kontrolė > Periodinės užduotys > „Kanban“ kiekio skaičiavimas > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="c6c45-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="c6c45-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="c6c45-109">Click New.</span></span>
3. <span data-ttu-id="c6c45-110">Lauke Tipas pasirinkite Išėmimas.</span><span class="sxs-lookup"><span data-stu-id="c6c45-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="c6c45-111">Tipas Išėmimas naudojamas kurti perkėlimo „kanban‟ signalams.</span><span class="sxs-lookup"><span data-stu-id="c6c45-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="c6c45-112">Lauke Papildymo strategija pasirinkite „Įvykis“.</span><span class="sxs-lookup"><span data-stu-id="c6c45-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="c6c45-113">Įvykio strategija pasirenkama, kad pagal įvykį būtų sukurtas „kanban‟ signalų perkėlimas.</span><span class="sxs-lookup"><span data-stu-id="c6c45-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="c6c45-114">Vėliau šiame užduoties vadove ją paleisime įvertindami gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c6c45-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="c6c45-115">Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c6c45-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c6c45-116">Įveskite arba pasirinkite ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="c6c45-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="c6c45-117">Šios perkėlimo veiklos gavimo (išeigos) sandėlis ir vieta yra 12 – tai reiškia, kad medžiaga bus perkelta į 12-ojo sandėlio 12-ąją vietą.</span><span class="sxs-lookup"><span data-stu-id="c6c45-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="c6c45-118">Išplėskite skyrių Išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="c6c45-118">Expand the Details section.</span></span>
7. <span data-ttu-id="c6c45-119">Lauke Produktas įveskite arba pasirinkite M0001.</span><span class="sxs-lookup"><span data-stu-id="c6c45-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="c6c45-120">Išplėskite skyrių Įvykiai.</span><span class="sxs-lookup"><span data-stu-id="c6c45-120">Expand the Events section.</span></span>
9. <span data-ttu-id="c6c45-121">Lauke KS eilutės įvykis pasirinkite Automatinis.</span><span class="sxs-lookup"><span data-stu-id="c6c45-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="c6c45-122">Kai laukas KS eilutės įvykis nustatytas į Automatinis, tenkinti gamybos užsakymo KS eilučių medžiagų poreikiams bus sukurtas „kanban“.</span><span class="sxs-lookup"><span data-stu-id="c6c45-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="c6c45-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c6c45-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="c6c45-124">Naujo gamybos užsakymo kūrimas ir modifikavimas</span><span class="sxs-lookup"><span data-stu-id="c6c45-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="c6c45-125">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="c6c45-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="c6c45-126">Spustelėkite Naujas gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="c6c45-126">Click New production order.</span></span>
3. <span data-ttu-id="c6c45-127">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c6c45-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="c6c45-128">Įveskite arba pasirinkite L0001.</span><span class="sxs-lookup"><span data-stu-id="c6c45-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="c6c45-129">Naudojame prekę L0001, nes prekė M0001 yra įtraukta į prekės L0001 KS.</span><span class="sxs-lookup"><span data-stu-id="c6c45-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="c6c45-130">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="c6c45-130">Click Create.</span></span>
5. <span data-ttu-id="c6c45-131">Sąraše spustelėkite saitą L0001 eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c6c45-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="c6c45-132">Spustelėkite KS.</span><span class="sxs-lookup"><span data-stu-id="c6c45-132">Click BOM.</span></span>
7. <span data-ttu-id="c6c45-133">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c6c45-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c6c45-134">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="c6c45-134">Click Edit.</span></span>
9. <span data-ttu-id="c6c45-135">Lauke Eilutės tipas pasirinkite Iškviestas tiekimas.</span><span class="sxs-lookup"><span data-stu-id="c6c45-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="c6c45-136">Pasirenkamas iškviestas tiekimas, kad būtų suaktyvintas „kanban‟ tiekimo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="c6c45-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="c6c45-137">Lauke Išteklių suvartojimas pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="c6c45-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="c6c45-138">Išvalius žymės langelį Išteklių suvartojimas, galima pakeisti sandėlį</span><span class="sxs-lookup"><span data-stu-id="c6c45-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="c6c45-139">Išplėskite dalį Atsargų dimensijos.</span><span class="sxs-lookup"><span data-stu-id="c6c45-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="c6c45-140">Lauke „Sandėlis“ įveskite „12“.</span><span class="sxs-lookup"><span data-stu-id="c6c45-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="c6c45-141">Sandėlis nustatytas į 12, nes jis yra išėmimo veiklos išeigos sandėlis.</span><span class="sxs-lookup"><span data-stu-id="c6c45-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="c6c45-142">Lauke Vieta įveskite „12“.</span><span class="sxs-lookup"><span data-stu-id="c6c45-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="c6c45-143">Vieta nustatyta į 12, nes ji yra išėmimo veiklos išeigos vieta.</span><span class="sxs-lookup"><span data-stu-id="c6c45-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="c6c45-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c6c45-144">Close the page.</span></span>
15. <span data-ttu-id="c6c45-145">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c6c45-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="c6c45-146">Gamybos užsakymo įvertinimas ir sukurto „kanban“ peržiūra</span><span class="sxs-lookup"><span data-stu-id="c6c45-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="c6c45-147">Spustelėkite Įvertinti.</span><span class="sxs-lookup"><span data-stu-id="c6c45-147">Click Estimate.</span></span>
    * <span data-ttu-id="c6c45-148">Įvertinus gamybos užsakymą bus suaktyvintas susijusio „kanban‟ kūrimas, kad būtų galima tiekti prekę M0001.</span><span class="sxs-lookup"><span data-stu-id="c6c45-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="c6c45-149">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c6c45-149">Click OK.</span></span>
3. <span data-ttu-id="c6c45-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c6c45-150">Close the page.</span></span>
4. <span data-ttu-id="c6c45-151">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="c6c45-151">Close the page.</span></span>
5. <span data-ttu-id="c6c45-152">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="c6c45-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="c6c45-153">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="c6c45-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c6c45-154">Pasirinkite sukurtą prekės M0001 įvykio „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="c6c45-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="c6c45-155">Išplėskite skyrių „Kanbans“.</span><span class="sxs-lookup"><span data-stu-id="c6c45-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="c6c45-156">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="c6c45-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c6c45-157">Atkreipkite dėmesį į „kanban‟, sukurtą, kad būtų galima tiekti M0001 įvertintam gamybos užsakymui.</span><span class="sxs-lookup"><span data-stu-id="c6c45-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="c6c45-158">Tai paskutinis veiksmas!</span><span class="sxs-lookup"><span data-stu-id="c6c45-158">This is the last step!</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]