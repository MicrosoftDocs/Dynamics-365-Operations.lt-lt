--- 
title: "Gamybos užsakymo planavimas, naudojant operacijų planavimą ir užduočių planavimą"
description: "Ši procedūra orientuota į gamybos užsakymo planavimą naudojant operacijų planavimą ir užduočių planavimą."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9fda708858adb3eeed9bf479936bc3539fb64a4
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="0637a-103">Gamybos užsakymo planavimas, naudojant operacijų planavimą ir užduočių planavimą</span><span class="sxs-lookup"><span data-stu-id="0637a-103">Schedule a production order with operations and job scheduling</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0637a-104">Ši procedūra orientuota į gamybos užsakymo planavimą naudojant operacijų planavimą ir užduočių planavimą.</span><span class="sxs-lookup"><span data-stu-id="0637a-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="0637a-105">Užduotys nekuriamos naudojant operacijų planavimą, tačiau užduotys kuriamos naudojant užduočių planavimą.</span><span class="sxs-lookup"><span data-stu-id="0637a-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="0637a-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="0637a-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="0637a-107">Ši procedūra skirta gamybos vadovui, gamybos planuotojui ar darbo laiko prižiūrėtojui, dirbančiam atskiros gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="0637a-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="0637a-108">Kurti gamybos užsakymą</span><span class="sxs-lookup"><span data-stu-id="0637a-108">Create a production order</span></span>
1. <span data-ttu-id="0637a-109">Pasirinkite Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai.</span><span class="sxs-lookup"><span data-stu-id="0637a-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="0637a-110">Spustelėkite Naujas gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="0637a-110">Click New production order.</span></span>
3. <span data-ttu-id="0637a-111">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0637a-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="0637a-112">Pasirinkite prekės numerį D0001.</span><span class="sxs-lookup"><span data-stu-id="0637a-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="0637a-113">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="0637a-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="0637a-114">Gamybos užsakymo operacijų planavimas</span><span class="sxs-lookup"><span data-stu-id="0637a-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="0637a-115">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0637a-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0637a-116">Pasirinkite ką tik sukurtą gamybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="0637a-116">Select the production order that you have just created.</span></span> <span data-ttu-id="0637a-117">Jis turėtų būti sąrašo viršuje.</span><span class="sxs-lookup"><span data-stu-id="0637a-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="0637a-118">Veiksmų srityje spustelėkite Grafikas.</span><span class="sxs-lookup"><span data-stu-id="0637a-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="0637a-119">Spustelėkite Planuoti operacijas.</span><span class="sxs-lookup"><span data-stu-id="0637a-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="0637a-120">Lauke Planavimo kryptis pasirinkite „Pirmyn nuo planavimo datos‟.</span><span class="sxs-lookup"><span data-stu-id="0637a-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="0637a-121">Lauke Planavimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="0637a-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="0637a-122">Pasirinkite tam tikrą dieną ateityje, pvz., dieną, kuri bus po savaitės.</span><span class="sxs-lookup"><span data-stu-id="0637a-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="0637a-123">Jei pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo šios datos.</span><span class="sxs-lookup"><span data-stu-id="0637a-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="0637a-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0637a-124">Click OK.</span></span>
7. <span data-ttu-id="0637a-125">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0637a-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0637a-126">Atminkite, kad būsena pasikeičia į Suplanuota.</span><span class="sxs-lookup"><span data-stu-id="0637a-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="0637a-127">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0637a-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0637a-128">Spustelėkite Visos užduotys.</span><span class="sxs-lookup"><span data-stu-id="0637a-128">Click All jobs.</span></span>
    * <span data-ttu-id="0637a-129">Atminkite, kad nėra užduočių, sukurtų naudojant operacijų planavimą.</span><span class="sxs-lookup"><span data-stu-id="0637a-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="0637a-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0637a-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="0637a-131">Gamybos užsakymo užduočių planavimas</span><span class="sxs-lookup"><span data-stu-id="0637a-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="0637a-132">Veiksmų srityje spustelėkite Grafikas.</span><span class="sxs-lookup"><span data-stu-id="0637a-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="0637a-133">Spustelėkite Planuoti užduotis.</span><span class="sxs-lookup"><span data-stu-id="0637a-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="0637a-134">Lauke Planavimo kryptis pasirinkite „Pirmyn nuo planavimo datos‟.</span><span class="sxs-lookup"><span data-stu-id="0637a-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="0637a-135">Lauke Planavimo data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="0637a-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="0637a-136">Pasirinkite tam tikrą dieną ateityje, pvz., dieną, kuri bus po savaitės.</span><span class="sxs-lookup"><span data-stu-id="0637a-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="0637a-137">Jei pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo šios datos.</span><span class="sxs-lookup"><span data-stu-id="0637a-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="0637a-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0637a-138">Click OK.</span></span>
6. <span data-ttu-id="0637a-139">Veiksmų srityje spustelėkite Gamybos užsakymas.</span><span class="sxs-lookup"><span data-stu-id="0637a-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="0637a-140">Spustelėkite Visos užduotys.</span><span class="sxs-lookup"><span data-stu-id="0637a-140">Click All jobs.</span></span>
    * <span data-ttu-id="0637a-141">Atminkite, kad remiantis aktyviu maršrutu 5 užduotys sukuriamos naudojant užduočių planavimą.</span><span class="sxs-lookup"><span data-stu-id="0637a-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  


