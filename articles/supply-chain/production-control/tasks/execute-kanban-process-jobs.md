---
title: Vykdyti „kanban“ proceso užduotis
description: Šioje procedūroje parodyta, kaip vykdyti „kanban“ proceso užduotis.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9da49ae17d6c25166f6b0e05e3c45fc991c9a54d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994159"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="77fb2-103">Vykdyti „kanban“ proceso užduotis</span><span class="sxs-lookup"><span data-stu-id="77fb2-103">Execute kanban process jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77fb2-104">Šioje procedūroje parodyta, kaip vykdyti „kanban“ proceso užduotis.</span><span class="sxs-lookup"><span data-stu-id="77fb2-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="77fb2-105">Pirmoji užduotis baigta su numatytu kiekiu ir be klaidų.</span><span class="sxs-lookup"><span data-stu-id="77fb2-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="77fb2-106">Antroji užduotis baigta su klaidomis.</span><span class="sxs-lookup"><span data-stu-id="77fb2-106">The second job is completed with errors.</span></span> <span data-ttu-id="77fb2-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="77fb2-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="77fb2-108">Ši procedūra skirta mašinos operatoriui.</span><span class="sxs-lookup"><span data-stu-id="77fb2-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="77fb2-109">„Kanban‟ užduoties pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="77fb2-109">Select a kanban job</span></span>
1. <span data-ttu-id="77fb2-110">Pasirinkite Gamybos kontrolė > „Kanban“ > „Kanban“ sritis proceso užduotims.</span><span class="sxs-lookup"><span data-stu-id="77fb2-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="77fb2-111">Lauke Darbo elementas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="77fb2-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="77fb2-112">Spustelėkite eilutę su 1250 išteklių grupe.</span><span class="sxs-lookup"><span data-stu-id="77fb2-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="77fb2-113">Užduočių sąrašas filtruojamas, kad būtų rodomos tik 1250 darbo elemento užduotys.</span><span class="sxs-lookup"><span data-stu-id="77fb2-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="77fb2-114">Pažymėkite eilutę, kurios būsena – Suplanuota užduotis.</span><span class="sxs-lookup"><span data-stu-id="77fb2-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="77fb2-115">Užduoties baigimas su numatytu kiekiu</span><span class="sxs-lookup"><span data-stu-id="77fb2-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="77fb2-116">Išplėskite arba sutraukite sekciją Informacija.</span><span class="sxs-lookup"><span data-stu-id="77fb2-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="77fb2-117">Šioje dalyje rodoma svarbi informacija apie kortelės numerį, prekės numerį, užsakytą kiekį ir veiklos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="77fb2-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="77fb2-118">Išplėskite arba sutraukite dalį Gamybos instrukcijos.</span><span class="sxs-lookup"><span data-stu-id="77fb2-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="77fb2-119">Šioje dalyje rodomos veiklos gamybos instrukcijos.</span><span class="sxs-lookup"><span data-stu-id="77fb2-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="77fb2-120">Instrukcijos gali būti tekstas, paveikslėliai, eskizai ir kiti dokumentai.</span><span class="sxs-lookup"><span data-stu-id="77fb2-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="77fb2-121">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="77fb2-121">Click Start.</span></span>
    * <span data-ttu-id="77fb2-122">Pasirinkite nepabaigtą užduotį.</span><span class="sxs-lookup"><span data-stu-id="77fb2-122">Select a job that is not completed.</span></span> <span data-ttu-id="77fb2-123">Naudokite būsenos piktogramas lauke Užduoties būsena, kad peržiūrėtumėte užduoties būseną.</span><span class="sxs-lookup"><span data-stu-id="77fb2-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="77fb2-124">Spustelėkite Baigti.</span><span class="sxs-lookup"><span data-stu-id="77fb2-124">Click Complete.</span></span>
    * <span data-ttu-id="77fb2-125">Užduotis baigta, jos kokybė numatyta.</span><span class="sxs-lookup"><span data-stu-id="77fb2-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="77fb2-126">Užduoties baigimas su klaidomis</span><span class="sxs-lookup"><span data-stu-id="77fb2-126">Complete a job with errors</span></span>
1. <span data-ttu-id="77fb2-127">Spustelėkite Pradėti.</span><span class="sxs-lookup"><span data-stu-id="77fb2-127">Click Start.</span></span>
    * <span data-ttu-id="77fb2-128">Kai užduotis baigiama, automatiškai pasirenkama kita sąrašo užduotis.</span><span class="sxs-lookup"><span data-stu-id="77fb2-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="77fb2-129">Todėl, prieš spustelėjant Pradėti, nereikia pasirinkti užduoties.</span><span class="sxs-lookup"><span data-stu-id="77fb2-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="77fb2-130">Veiksmų srityje spustelėkite Gamyba.</span><span class="sxs-lookup"><span data-stu-id="77fb2-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="77fb2-131">Spustelėkite Užbaigti (informacija).</span><span class="sxs-lookup"><span data-stu-id="77fb2-131">Click Complete (details).</span></span>
4. <span data-ttu-id="77fb2-132">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="77fb2-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="77fb2-133">Lauke Klaidų kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="77fb2-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="77fb2-134">Lauke Tinkamas kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="77fb2-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="77fb2-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="77fb2-135">Click OK.</span></span>

