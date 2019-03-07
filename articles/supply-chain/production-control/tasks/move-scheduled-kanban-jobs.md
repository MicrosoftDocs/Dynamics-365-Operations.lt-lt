---
title: Perkelti suplanuotas „kanban“ užduotis
description: Šia procedūra dėmesys skiriamas suplanuotų „kanban‟ apdorojimo užduočių perkėlimui į kitą laikotarpį.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f791c9048ef6efe1585c991f998099cd1fc12df7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "310857"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="16852-103">Perkelti suplanuotas „kanban“ užduotis</span><span class="sxs-lookup"><span data-stu-id="16852-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16852-104">Šia procedūra dėmesys skiriamas suplanuotų „kanban‟ apdorojimo užduočių perkėlimui į kitą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="16852-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="16852-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="16852-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="16852-106">Ši procedūra yra skirta darbo laiko prižiūrėtojui arba gamybos planuotojui, dirbančiam su „kanban‟.</span><span class="sxs-lookup"><span data-stu-id="16852-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="16852-107">Pasirinkite suplanuotas „kanban“ užduotis.</span><span class="sxs-lookup"><span data-stu-id="16852-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="16852-108">Eikite į **Gamybos kontrolė > „Kanban“ > „Kanban“ užduočių planavimas**.</span><span class="sxs-lookup"><span data-stu-id="16852-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="16852-109">Lauke **Darbo elementas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="16852-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="16852-110">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="16852-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="16852-111">Pasirinkite 1250 darbo elementą.</span><span class="sxs-lookup"><span data-stu-id="16852-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="16852-112">Spustelėkite **Pažymėti**.</span><span class="sxs-lookup"><span data-stu-id="16852-112">Click **Select**.</span></span> 

5. <span data-ttu-id="16852-113">Lauke **Rodyti užduoties būseną** pasirinkite **Suplanuota**.</span><span class="sxs-lookup"><span data-stu-id="16852-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="16852-114">Filtruojamas užduočių sąrašas, kad būtų rodomos tik suplanuotos „kanban‟ užduotys.</span><span class="sxs-lookup"><span data-stu-id="16852-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="16852-115">Perkelkite „kanban‟ užduotis į kitą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="16852-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="16852-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="16852-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="16852-117">Lauke **Suplanuotas laikotarpis** pasirinkite užduotį, kurios būsena yra **Suplanuota**, pvz., 2012 m. gruodžio 20 d. suplanuotą užduotį.</span><span class="sxs-lookup"><span data-stu-id="16852-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="16852-118">Tada užduotį perkelkite į ankstesnį laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="16852-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="16852-119">Spustelėkite **Ankstesnis laikotarpis**.</span><span class="sxs-lookup"><span data-stu-id="16852-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="16852-120">Spustelėkite **Pabaiga**, kad užduotį į užduočių sąrašo pabaigą perkeltumėte kaip paskutinę ankstesnio laikotarpio užduotį.</span><span class="sxs-lookup"><span data-stu-id="16852-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="16852-121">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="16852-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="16852-122">Lauke **Suplanuotas laikotarpis** pasirinkite užduotį, kurios būsena yra **Suplanuota**, pvz., 2012 m. gruodžio 18 d. suplanuotą užduotį.</span><span class="sxs-lookup"><span data-stu-id="16852-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="16852-123">Tada užduotį perkelkite į kitą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="16852-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="16852-124">Spustelėkite **Kitas laikotarpis**.</span><span class="sxs-lookup"><span data-stu-id="16852-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="16852-125">Spustelėkite **Pradžia**, kad užduotį į užduočių sąrašo pradžią perkeltumėte kaip pirmą ankstesnio laikotarpio užduotį.</span><span class="sxs-lookup"><span data-stu-id="16852-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="16852-126">Perkelkite užduotį laikotarpyje.</span><span class="sxs-lookup"><span data-stu-id="16852-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="16852-127">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="16852-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="16852-128">Lauke **Suplanuotas laikotarpis** pasirinkite užduotį, kurios būsena yra Suplanuota, pvz., antrąją užduotį, suplanuotą 2012 m. gruodžio 19 d.</span><span class="sxs-lookup"><span data-stu-id="16852-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="16852-129">Tada užduotį perkelkite į suplanuotą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="16852-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="16852-130">Spustelėkite **Pirmyn**.</span><span class="sxs-lookup"><span data-stu-id="16852-130">Click **Forward**.</span></span> <span data-ttu-id="16852-131">Atkreipkite dėmesį, kad užduotis sąraše perkeliama viena eilute žemyn.</span><span class="sxs-lookup"><span data-stu-id="16852-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="16852-132">Spustelėkite **Atgal**.</span><span class="sxs-lookup"><span data-stu-id="16852-132">Click **Backward**.</span></span> <span data-ttu-id="16852-133">Atkreipkite dėmesį, kad užduotis sąraše perkeliama viena eilute aukštyn.</span><span class="sxs-lookup"><span data-stu-id="16852-133">Notice that the job is moved one line up on the list.</span></span>
