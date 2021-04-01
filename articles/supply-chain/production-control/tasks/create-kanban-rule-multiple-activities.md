---
title: Kurti kelių veiklos rūšių „kanban“ taisykles
description: Šioje procedūroje parodoma, kaip kurti „kanban“ taisyklę, kuri apima kelias gamybos eigos veiklas.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcf507611d7f85800b2012e8372d5f91bbc8d724
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255186"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="82ddc-103">Kurti kelių veiklos rūšių „kanban“ taisykles</span><span class="sxs-lookup"><span data-stu-id="82ddc-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82ddc-104">Šioje procedūroje parodoma, kaip kurti „kanban“ taisyklę, kuri apima kelias gamybos eigos veiklas.</span><span class="sxs-lookup"><span data-stu-id="82ddc-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="82ddc-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="82ddc-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="82ddc-106">Ši užduotis skirta proceso inžinieriui arba vertės srauto vadovui, nes jie parengia naujos arba pakeistos prekės gamybą „lean“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="82ddc-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="82ddc-107">Kurti naują „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="82ddc-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="82ddc-108">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="82ddc-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="82ddc-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="82ddc-109">Click New.</span></span>
3. <span data-ttu-id="82ddc-110">Lauke Papildymo strategija pasirinkite Suplanuota.</span><span class="sxs-lookup"><span data-stu-id="82ddc-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="82ddc-111">Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="82ddc-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="82ddc-112">Pasirinkite SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="82ddc-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="82ddc-113">Pasirinkite žymės langelį Kelios veiklos.</span><span class="sxs-lookup"><span data-stu-id="82ddc-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="82ddc-114">Tikslas yra į „kanban“ taisyklę įtraukti daugiau nei vieną veiklą.</span><span class="sxs-lookup"><span data-stu-id="82ddc-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="82ddc-115">Gamybos eigos kelias pasirenkamas, kai pasirenkama paskutiniojo plano veikla.</span><span class="sxs-lookup"><span data-stu-id="82ddc-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="82ddc-116">Lauke Paskutinioji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="82ddc-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="82ddc-117">Pasirinkite SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="82ddc-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="82ddc-118">Pasirinkus reikšmę automatiškai atidaromas puslapis.</span><span class="sxs-lookup"><span data-stu-id="82ddc-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="82ddc-119">Pasirinkite „kanban“ srauto SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="82ddc-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="82ddc-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="82ddc-120">Click OK.</span></span>  
7. <span data-ttu-id="82ddc-121">Išplėskite skyrių Išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="82ddc-121">Expand the Details section.</span></span>
8. <span data-ttu-id="82ddc-122">Lauke Produktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="82ddc-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="82ddc-123">Pasirinkite prekę L0006.</span><span class="sxs-lookup"><span data-stu-id="82ddc-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="82ddc-124">Kurti „kanban“ ir peržiūrėti užduotis</span><span class="sxs-lookup"><span data-stu-id="82ddc-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="82ddc-125">Išplėskite skyrių „Kanbans“.</span><span class="sxs-lookup"><span data-stu-id="82ddc-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="82ddc-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="82ddc-126">Click Add.</span></span>
3. <span data-ttu-id="82ddc-127">Lauke Naujų „kanban“ skaičius įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="82ddc-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="82ddc-128">Taip sukursite vieną „kanban“.</span><span class="sxs-lookup"><span data-stu-id="82ddc-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="82ddc-129">Nustatykite produkto kiekio reikšmę „3“.</span><span class="sxs-lookup"><span data-stu-id="82ddc-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="82ddc-130">„Kanban“ apdoros 3 produktus.</span><span class="sxs-lookup"><span data-stu-id="82ddc-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="82ddc-131">Lauke Termino data / laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="82ddc-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="82ddc-132">Galite įvesti Šiandien.</span><span class="sxs-lookup"><span data-stu-id="82ddc-132">You can enter Today.</span></span>  
6. <span data-ttu-id="82ddc-133">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="82ddc-133">Click Create.</span></span>
7. <span data-ttu-id="82ddc-134">Spustelėkite Informacija.</span><span class="sxs-lookup"><span data-stu-id="82ddc-134">Click Details.</span></span>
    * <span data-ttu-id="82ddc-135">Atkreipkite dėmesį, kad „kanban“ priskirtos dvi gamybos eigos proceso užduotys.</span><span class="sxs-lookup"><span data-stu-id="82ddc-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="82ddc-136">Pirmoji yra SpeakerAssemblyAndPolish, o antroji – SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="82ddc-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="82ddc-137">Tai paskutinis veiksmas!</span><span class="sxs-lookup"><span data-stu-id="82ddc-137">This is the last step!</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]