---
title: „Kanban“ užduočių planavimas
description: Šia procedūra dėmesys skiriamas konkretaus darbo elemento „kanban‟ apdorojimo užduočių planavimui.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5170fecf0190591d74f45d35fecc4472e7f5e900
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562166"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="b9ad0-103">„Kanban“ užduočių planavimas</span><span class="sxs-lookup"><span data-stu-id="b9ad0-103">Schedule kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9ad0-104">Šia procedūra dėmesys skiriamas konkretaus darbo elemento „kanban‟ apdorojimo užduočių planavimui.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="b9ad0-105">Būtina šios procedūros sukūrimo sąlyga yra procedūra „Parengti „kanban“ užduoties procesą, kai nėra reikiamų medžiagų“.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="b9ad0-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b9ad0-107">Ši užduotis yra skirta darbo laiko prižiūrėtojui ir gamybos planuotojui, dirbančiam su „kanban‟.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="b9ad0-108">Pasirinkti darbo elemento „kanban‟ užduotis</span><span class="sxs-lookup"><span data-stu-id="b9ad0-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="b9ad0-109">Pasirinkite Gamybos kontrolė > „Kanban“ > „Kanban“ užduočių planavimas.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="b9ad0-110">Išplėsti „FactBox“ Laikotarpio pajėgumas</span><span class="sxs-lookup"><span data-stu-id="b9ad0-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="b9ad0-111">Išplėskite „FactBox“ „Kanban“.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="b9ad0-112">Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b9ad0-113">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b9ad0-114">Pasirinkite 1250 darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-114">Select work cell 1250.</span></span> <span data-ttu-id="b9ad0-115">Rodinys bus filtruojamas, kad būtų rodomos tik 1250 darbo elemento užduotys.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="b9ad0-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b9ad0-117">Spustelėkite Pažymėti.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="b9ad0-118">„Kanban‟ užduotį planuoti pirmajam galimam laikotarpiui</span><span class="sxs-lookup"><span data-stu-id="b9ad0-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="b9ad0-119">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b9ad0-120">Pasirinkite pirmąją eilutę sąraše, kurios būsena yra Nesuplanuota.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="b9ad0-121">Taškinė piktograma lauke Užduoties būsena nurodo nesuplanuotą būseną.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="b9ad0-122">Spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-122">Click Schedule.</span></span>
    * <span data-ttu-id="b9ad0-123">„Kanban‟ užduotis bus suplanuota pirmajam galimam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="b9ad0-124">Atkreipkite dėmesį, kad „kanban“ užduotis perkelta į sąrašo pabaigą, nes ji pridėta į laikotarpį, prasidedantį šiandien.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="b9ad0-125">Jei laikotarpis, prasidedantis šiandien, yra visiškai rezervuotas, užduotis bus perkelta į pirmąjį galimą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="b9ad0-126">Konkrečiai dienai suplanuoti dvi „kanban‟ užduotis</span><span class="sxs-lookup"><span data-stu-id="b9ad0-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="b9ad0-127">Sąraše pasirinkite 1 eilutę.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="b9ad0-128">Turėtumėte matyti, kad pirmosios eilutės lauke Užduoties būsena būsena yra Nesuplanuota.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="b9ad0-129">Sąraše pasirinkite 2 eilutę.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="b9ad0-130">Turėtumėte matyti, kad antrosios eilutės lauke Užduoties būsena būsena yra Nesuplanuota.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="b9ad0-131">Dabar pasirinktos pirmosios dvi užduotys.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="b9ad0-132">Spustelėdami Grafikas nuo datos, atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="b9ad0-133">Pažymėkite arba atžymėkite langelį Perrašyti pajėgumo trūkumo reakciją.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="b9ad0-134">Ši parinktis leidžia nepaisyti numatytosios pajėgumo trūkumo reakcijos.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="b9ad0-135">Lauke Pajėgumo trūkumo reakcija pasirinkite „Įtraukti į reikalaujamą laikotarpį‟.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="b9ad0-136">Ši parinktis užtikrins, kad užduotis būtų pridėta į reikiamą laikotarpį, neatsižvelgiant į tai, kad darbo elementas gali būti perkrautas.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="b9ad0-137">Spustelėkite Planuoti.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-137">Click Schedule.</span></span>
    * <span data-ttu-id="b9ad0-138">Atkreipkite dėmesį, kad abi užduotys pridėtos į norimą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="b9ad0-139">Dalyje Laikotarpio pajėgumas galite matyti kiekvieno laikotarpio apkrovą.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="b9ad0-140">Lauke Suvartojimas rodomas suplanuotas suvartojimas šiuo laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="b9ad0-141">Jei suplanuotas suvartojimas yra didesnis nei galimas pajėgumas per šį laikotarpį, bus pasirinktas perkrautas suvartojimas.</span><span class="sxs-lookup"><span data-stu-id="b9ad0-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

