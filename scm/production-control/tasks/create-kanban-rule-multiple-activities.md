--- 
title: "Kurti kelių veiklos rūšių „kanban“ taisykles"
description: "Šioje procedūroje parodoma, kaip kurti „kanban“ taisyklę, kuri apima kelias gamybos eigos veiklas."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d6d0c50da3124553124b65f6ba0e1c5ed35e8613
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="09218-103">Kurti kelių veiklos rūšių „kanban“ taisykles</span><span class="sxs-lookup"><span data-stu-id="09218-103">Create a kanban rule for multiple activities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09218-104">Šioje procedūroje parodoma, kaip kurti „kanban“ taisyklę, kuri apima kelias gamybos eigos veiklas.</span><span class="sxs-lookup"><span data-stu-id="09218-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="09218-105">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="09218-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="09218-106">Ši užduotis skirta proceso inžinieriui arba vertės srauto vadovui, nes jie parengia naujos arba pakeistos prekės gamybą „lean“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="09218-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="09218-107">Kurti naują „kanban“ taisyklę</span><span class="sxs-lookup"><span data-stu-id="09218-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="09218-108">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="09218-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="09218-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="09218-109">Click New.</span></span>
3. <span data-ttu-id="09218-110">Lauke Papildymo strategija pasirinkite Suplanuota.</span><span class="sxs-lookup"><span data-stu-id="09218-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="09218-111">Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09218-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="09218-112">Pasirinkite SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="09218-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="09218-113">Pasirinkite žymės langelį Kelios veiklos.</span><span class="sxs-lookup"><span data-stu-id="09218-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="09218-114">Tikslas yra į „kanban“ taisyklę įtraukti daugiau nei vieną veiklą.</span><span class="sxs-lookup"><span data-stu-id="09218-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="09218-115">Gamybos eigos kelias pasirenkamas, kai pasirenkama paskutiniojo plano veikla.</span><span class="sxs-lookup"><span data-stu-id="09218-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="09218-116">Lauke Paskutinioji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09218-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="09218-117">Pasirinkite SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="09218-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="09218-118">Pasirinkus reikšmę automatiškai atidaromas puslapis.</span><span class="sxs-lookup"><span data-stu-id="09218-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="09218-119">Pasirinkite „kanban“ srauto SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="09218-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="09218-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="09218-120">Click OK.</span></span>  
7. <span data-ttu-id="09218-121">Išplėskite skyrių Išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="09218-121">Expand the Details section.</span></span>
8. <span data-ttu-id="09218-122">Lauke Produktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="09218-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="09218-123">Pasirinkite prekę L0006.</span><span class="sxs-lookup"><span data-stu-id="09218-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="09218-124">Kurti „kanban“ ir peržiūrėti užduotis</span><span class="sxs-lookup"><span data-stu-id="09218-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="09218-125">Išplėskite skyrių „Kanbans“.</span><span class="sxs-lookup"><span data-stu-id="09218-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="09218-126">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="09218-126">Click Add.</span></span>
3. <span data-ttu-id="09218-127">Lauke Naujų „kanban“ skaičius įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="09218-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="09218-128">Taip sukursite vieną „kanban“.</span><span class="sxs-lookup"><span data-stu-id="09218-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="09218-129">Nustatykite produkto kiekio reikšmę „3“.</span><span class="sxs-lookup"><span data-stu-id="09218-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="09218-130">„Kanban“ apdoros 3 produktus.</span><span class="sxs-lookup"><span data-stu-id="09218-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="09218-131">Lauke Termino data / laikas įveskite datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="09218-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="09218-132">Galite įvesti Šiandien.</span><span class="sxs-lookup"><span data-stu-id="09218-132">You can enter Today.</span></span>  
6. <span data-ttu-id="09218-133">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="09218-133">Click Create.</span></span>
7. <span data-ttu-id="09218-134">Spustelėkite Informacija.</span><span class="sxs-lookup"><span data-stu-id="09218-134">Click Details.</span></span>
    * <span data-ttu-id="09218-135">Atkreipkite dėmesį, kad „kanban“ priskirtos dvi gamybos eigos proceso užduotys.</span><span class="sxs-lookup"><span data-stu-id="09218-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="09218-136">Pirmoji yra SpeakerAssemblyAndPolish, o antroji – SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="09218-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="09218-137">Tai paskutinis veiksmas!</span><span class="sxs-lookup"><span data-stu-id="09218-137">This is the last step!</span></span>  


