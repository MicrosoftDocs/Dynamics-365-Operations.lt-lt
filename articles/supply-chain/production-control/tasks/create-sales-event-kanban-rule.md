--- 
title: "Kurti pardavimo įvykio „kanban“ taisyklę"
description: "Šia procedūra sutelkiamas dėmesys į nustatymus, reikalingus norint sukurti „kanban“ taisyklę, kuri veikia kuriant pardavimo užsakymą."
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 67dc36565739b8e902334d9a55af226a0cef5b85
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="72ea6-103">Kurti pardavimo įvykio „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="72ea6-103">Create a sales event kanban rule</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72ea6-104">Šia procedūra sutelkiamas dėmesys į nustatymus, reikalingus norint sukurti „kanban“ taisyklę, kuri veikia kuriant pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="72ea6-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="72ea6-105">Įvykio „kanban“ taisyklė papildo reikalavimus, kylančius iš pardavimo užsakymo eilučių.</span><span class="sxs-lookup"><span data-stu-id="72ea6-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="72ea6-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="72ea6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="72ea6-107">Ji skirta proceso inžinieriui arba vertės srauto vadybininkui, nes jie parengia naujos arba pakeistos prekės gamybą.</span><span class="sxs-lookup"><span data-stu-id="72ea6-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="72ea6-108">Kurti naują „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="72ea6-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="72ea6-109">Eikite į „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="72ea6-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="72ea6-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="72ea6-110">Click New.</span></span>
3. <span data-ttu-id="72ea6-111">Lauke Papildymo strategija pasirinkite „Įvykis“.</span><span class="sxs-lookup"><span data-stu-id="72ea6-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="72ea6-112">Pasirinkus Įvykis reiškia, kad „kanban“ taisyklę nulemia įvykis, pvz., pardavimo užsakymo eilutės kūrimas.</span><span class="sxs-lookup"><span data-stu-id="72ea6-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="72ea6-113">Tai taikoma toms sritims, kuriose kiekvienas „kanban“ turėtų patenkinti tam tikrus poreikius.</span><span class="sxs-lookup"><span data-stu-id="72ea6-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="72ea6-114">Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="72ea6-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="72ea6-115">Pasirinkite Galutinis surinkimas.</span><span class="sxs-lookup"><span data-stu-id="72ea6-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="72ea6-116">Išplėskite skyrių Išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="72ea6-116">Expand the Details section.</span></span>
6. <span data-ttu-id="72ea6-117">Lauke Produktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="72ea6-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="72ea6-118">Pažymėkite L0050.</span><span class="sxs-lookup"><span data-stu-id="72ea6-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="72ea6-119">Įvykio apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="72ea6-119">Define an event</span></span>
1. <span data-ttu-id="72ea6-120">Išplėskite skyrių Įvykiai.</span><span class="sxs-lookup"><span data-stu-id="72ea6-120">Expand the Events section.</span></span>
2. <span data-ttu-id="72ea6-121">Lauke Pardavimo įvykis pasirinkite „Automatinis“.</span><span class="sxs-lookup"><span data-stu-id="72ea6-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="72ea6-122">Pasirinkus pardavimo įvykį Automatinis, kai pardavimo eilutė sutaps su produkto ir gavimo vieta, ši „kanban“ taisyklė bus paleidžiama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="72ea6-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="72ea6-123">Šioje procedūroje tai produktas L0050 13 sandėlyje.</span><span class="sxs-lookup"><span data-stu-id="72ea6-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="72ea6-124">Nustatykite pasirinkties Mažiausias įvykio kiekis reikšmę „50“.</span><span class="sxs-lookup"><span data-stu-id="72ea6-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="72ea6-125">Kai Mažiausias įvykio kiekis yra 50, „kanban“ taisyklę naudos tik tie įvykiai, kurių kiekis yra 50 arba didesnis.</span><span class="sxs-lookup"><span data-stu-id="72ea6-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="72ea6-126">Išplėskite skyrių Gamybos eiga.</span><span class="sxs-lookup"><span data-stu-id="72ea6-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="72ea6-127">Atkreipkite dėmesį, kad Gavimo vieta yra 13 sandėlis.</span><span class="sxs-lookup"><span data-stu-id="72ea6-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="72ea6-128">Tai reiškia, kad ši „kanban“ taisyklė bus taikoma šiai vietai.</span><span class="sxs-lookup"><span data-stu-id="72ea6-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="72ea6-129">Šiame pavyzdyje šią „kanban“ taisyklę paleis produkto pardavimo eilutė L0050, kurioje nurodytas 13 sandėlio kiekis yra 50 arba didesnis.</span><span class="sxs-lookup"><span data-stu-id="72ea6-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="72ea6-130">Pardavimo eilutės kūrimas ir įvykio „kanban“ taisyklės paleidimas</span><span class="sxs-lookup"><span data-stu-id="72ea6-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="72ea6-131">Eikite į Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="72ea6-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="72ea6-132">Įrašius „kanban“ taisyklę rodomas įspėjimas, o tai reiškia, kad „kanbans“ bus sukurti realiuoju laiku kuriant pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="72ea6-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="72ea6-133">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="72ea6-133">Click New.</span></span>
3. <span data-ttu-id="72ea6-134">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="72ea6-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="72ea6-135">Pavyzdžiui, pasirinkite US-003.</span><span class="sxs-lookup"><span data-stu-id="72ea6-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="72ea6-136">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="72ea6-136">Click OK.</span></span>
5. <span data-ttu-id="72ea6-137">Lauke „Prekės numeris“ įveskite „L0050“.</span><span class="sxs-lookup"><span data-stu-id="72ea6-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="72ea6-138">Lauke Vieta įveskite „1“.</span><span class="sxs-lookup"><span data-stu-id="72ea6-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="72ea6-139">Pasirinkite 1 vietą, nes 13 sandėlis yra 1 vietoje.</span><span class="sxs-lookup"><span data-stu-id="72ea6-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="72ea6-140">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="72ea6-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="72ea6-141">Nustatykite pasirinkties Sandėlis reikšmę 13.</span><span class="sxs-lookup"><span data-stu-id="72ea6-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="72ea6-142">Nustatykite kiekį – 75.</span><span class="sxs-lookup"><span data-stu-id="72ea6-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="72ea6-143">Įveskite kiekį 50 arba didesnį, kad paleistumėte „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="72ea6-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="72ea6-144">Patikrinkite, ar „kanban“ sukurtas</span><span class="sxs-lookup"><span data-stu-id="72ea6-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="72ea6-145">Spustelėkite Produktas ir tiekimas.</span><span class="sxs-lookup"><span data-stu-id="72ea6-145">Click Product and supply.</span></span>
2. <span data-ttu-id="72ea6-146">Spustelėkite Peržiūrėti iškvietimo medį.</span><span class="sxs-lookup"><span data-stu-id="72ea6-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="72ea6-147">Atkreipkite dėmesį, kad sukuriamas „kanban“, kurio kiekis toks pat, kaip pardavimo eilutė.</span><span class="sxs-lookup"><span data-stu-id="72ea6-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="72ea6-148">Taip pat galite matyti, kokios medžiagos turi būti išduotos norint pagaminti L0050.</span><span class="sxs-lookup"><span data-stu-id="72ea6-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="72ea6-149">Tai yra paskutinis šios procedūros veiksmas.</span><span class="sxs-lookup"><span data-stu-id="72ea6-149">This is the last step in this procedure.</span></span>  


