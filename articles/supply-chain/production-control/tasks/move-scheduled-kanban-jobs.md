--- 
title: "Perkelti suplanuotas „kanban“ užduotis"
description: "Šia procedūra dėmesys skiriamas suplanuotų „kanban‟ apdorojimo užduočių perkėlimui į kitą laikotarpį."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ae6ea66f0e0ce03008882e59140ad7a0d89f0e30
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="91050-103">Perkelti suplanuotas „kanban“ užduotis</span><span class="sxs-lookup"><span data-stu-id="91050-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="91050-104">Šia procedūra dėmesys skiriamas suplanuotų „kanban‟ apdorojimo užduočių perkėlimui į kitą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="91050-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="91050-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="91050-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="91050-106">Ši procedūra yra skirta darbo laiko prižiūrėtojui arba gamybos planuotojui, dirbančiam su „kanban‟.</span><span class="sxs-lookup"><span data-stu-id="91050-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="91050-107">Pasirinkti suplanuotas „kanban“ užduotis</span><span class="sxs-lookup"><span data-stu-id="91050-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="91050-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="91050-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="91050-109">!MtCMR!Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="91050-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="91050-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="91050-110">áçêìõý !</span></span>
3. <span data-ttu-id="91050-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="91050-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="91050-112">Pasirinkite 1250 darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="91050-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="91050-113">Klik på Select.</span><span class="sxs-lookup"><span data-stu-id="91050-113">Klik på Select.</span></span>
5. <span data-ttu-id="91050-114">Vælg 'Planlagt' i feltet Display job status.</span><span class="sxs-lookup"><span data-stu-id="91050-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="91050-115">Filtruojamas užduočių sąrašas, kad būtų rodomos tik suplanuotos „kanban‟ užduotys.</span><span class="sxs-lookup"><span data-stu-id="91050-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="91050-116">Perkelti „kanban‟ užduotis į kitą laikotarpį</span><span class="sxs-lookup"><span data-stu-id="91050-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="91050-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="91050-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="91050-118">Pasirinkite užduotį, kurios būsena yra Suplanuota, pvz., suplanuotą 2012 m. gruodžio 20 d. lauke Suplanuotas laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="91050-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="91050-119">Tada užduotį perkelkite į ankstesnį laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="91050-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="91050-120">Klik på Previous period.</span><span class="sxs-lookup"><span data-stu-id="91050-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="91050-121">Klik på End.</span><span class="sxs-lookup"><span data-stu-id="91050-121">Klik på End.</span></span>
    * <span data-ttu-id="91050-122">Užduotis bus perkelta į užduočių sąrašo pabaigą kaip paskutinė ankstesnio laikotarpio užduotis.</span><span class="sxs-lookup"><span data-stu-id="91050-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="91050-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="91050-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="91050-124">Pasirinkite užduotį, kurios būsena yra Suplanuota, pvz., suplanuotą 2012 m. gruodžio 18 d. lauke Suplanuotas laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="91050-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="91050-125">Tada užduotį perkelkite į kitą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="91050-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="91050-126">Klik på Next period.</span><span class="sxs-lookup"><span data-stu-id="91050-126">Klik på Next period.</span></span>
6. <span data-ttu-id="91050-127">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="91050-127">Klik på Start.</span></span>
    * <span data-ttu-id="91050-128">Užduotis bus perkelta į užduočių sąrašo pradžą kaip pirmoji ankstesnio laikotarpio užduotis.</span><span class="sxs-lookup"><span data-stu-id="91050-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="91050-129">Užduotis: perkelti užduotį laikotarpyje</span><span class="sxs-lookup"><span data-stu-id="91050-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="91050-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="91050-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="91050-131">Pasirinkite užduotį, kurios būsena yra Suplanuota, pvz., antrąją užduotį, suplanuotą 2012 m. gruodžio 19 d. lauke Suplanuotas laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="91050-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="91050-132">Tada užduotį perkelkite į suplanuotą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="91050-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="91050-133">Klik på Forward.</span><span class="sxs-lookup"><span data-stu-id="91050-133">Klik på Forward.</span></span>
    * <span data-ttu-id="91050-134">Atkreipkite dėmesį, kad užduotis sąraše perkeliama viena eilute žemyn.</span><span class="sxs-lookup"><span data-stu-id="91050-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="91050-135">Klik på Backward.</span><span class="sxs-lookup"><span data-stu-id="91050-135">Klik på Backward.</span></span>
    * <span data-ttu-id="91050-136">Atkreipkite dėmesį, kad užduotis sąraše perkeliama viena eilute aukštyn.</span><span class="sxs-lookup"><span data-stu-id="91050-136">Notice that the job is moved one line up on the list.</span></span>  


