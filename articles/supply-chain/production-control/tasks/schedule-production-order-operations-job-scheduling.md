---
title: Gamybos užsakymo planavimas naudojant operacijų ir užduočių planavimą
description: Šioje temoje aprašyta, kaip planuoti gamybos užsakymą naudojant operacijų ir užduočių planavimą.
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ace204f1ec79cc8f9ce10ebfdc3606879e40d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215846"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="de740-103">Gamybos užsakymo planavimas naudojant operacijų ir užduočių planavimą</span><span class="sxs-lookup"><span data-stu-id="de740-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de740-104">Šioje temoje aprašyta, kaip planuoti gamybos užsakymą naudojant operacijų ir užduočių planavimą.</span><span class="sxs-lookup"><span data-stu-id="de740-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="de740-105">Užduotys nekuriamos naudojant operacijų planavimą, tačiau užduotys kuriamos naudojant užduočių planavimą.</span><span class="sxs-lookup"><span data-stu-id="de740-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="de740-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="de740-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="de740-107">Ši procedūra skirta gamybos vadovui, gamybos planuotojui ar darbo laiko prižiūrėtojui, dirbančiam atskiros gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="de740-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="de740-108">Gamybos užsakymo kūrimas</span><span class="sxs-lookup"><span data-stu-id="de740-108">Create a production order</span></span>
1. <span data-ttu-id="de740-109">Naršymo srityje eikite į **Moduliai > Gamybos kontrolė > Gamybos užsakymai > Visi gamybos užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="de740-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="de740-110">Pasirinkite **Naujas gamybos užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="de740-110">Select **New production order**.</span></span>
3. <span data-ttu-id="de740-111">Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="de740-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="de740-112">Pasirinkite prekės numerį **D0001**.</span><span class="sxs-lookup"><span data-stu-id="de740-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="de740-113">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="de740-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="de740-114">Gamybos užsakymo operacijų planavimas</span><span class="sxs-lookup"><span data-stu-id="de740-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="de740-115">Pažymėkite naujai sukurtą eilutę.</span><span class="sxs-lookup"><span data-stu-id="de740-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="de740-116">Veiksmų srityje pasirinkite **Planavimas**.</span><span class="sxs-lookup"><span data-stu-id="de740-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="de740-117">Pasirinkite **Planuoti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="de740-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="de740-118">Lauke **Planavimo kryptis** pasirinkite **Pirmyn nuo planavimo datos**.</span><span class="sxs-lookup"><span data-stu-id="de740-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="de740-119">Lauke **Planavimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="de740-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="de740-120">Pasirinkite tam tikrą dieną ateityje, pvz., dieną, kuri bus po savaitės.</span><span class="sxs-lookup"><span data-stu-id="de740-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="de740-121">Jei pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo šios datos.</span><span class="sxs-lookup"><span data-stu-id="de740-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="de740-122">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="de740-122">Select **OK**.</span></span>
7. <span data-ttu-id="de740-123">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="de740-123">In the list, mark the selected row.</span></span> <span data-ttu-id="de740-124">Atkreipkite dėmesį, kad būsena pakeičiama į **Suplanuotas**.</span><span class="sxs-lookup"><span data-stu-id="de740-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="de740-125">Pasirinkite **Visos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="de740-125">Select **All jobs**.</span></span> <span data-ttu-id="de740-126">Atminkite, kad nėra užduočių, sukurtų naudojant operacijų planavimą.</span><span class="sxs-lookup"><span data-stu-id="de740-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="de740-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="de740-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="de740-128">Gamybos užsakymo užduočių planavimas</span><span class="sxs-lookup"><span data-stu-id="de740-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="de740-129">Veiksmų srityje pasirinkite **Planavimas**.</span><span class="sxs-lookup"><span data-stu-id="de740-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="de740-130">Pasirinkite **Planuoti užduotis**.</span><span class="sxs-lookup"><span data-stu-id="de740-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="de740-131">Lauke **Planavimo kryptis** pasirinkite **Pirmyn nuo planavimo datos**.</span><span class="sxs-lookup"><span data-stu-id="de740-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="de740-132">Lauke **Planavimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="de740-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="de740-133">Pasirinkite tam tikrą dieną ateityje, pvz., dieną, kuri bus po savaitės.</span><span class="sxs-lookup"><span data-stu-id="de740-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="de740-134">Jei pasirenkate šią planavimo kryptį, gamybos užsakymas bus planuojamas pirmyn nuo šios datos.</span><span class="sxs-lookup"><span data-stu-id="de740-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="de740-135">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="de740-135">Select **OK**.</span></span>
6. <span data-ttu-id="de740-136">Veiksmų srityje pasirinkite **Gamybos užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="de740-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="de740-137">Pasirinkite **Visos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="de740-137">Select **All jobs**.</span></span> <span data-ttu-id="de740-138">Atminkite, kad remiantis aktyviu maršrutu 5 užduotys sukuriamos naudojant užduočių planavimą.</span><span class="sxs-lookup"><span data-stu-id="de740-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]