--- 
title: "Kurti „kanban“ taisyklę naudojant „kanban“ eilutės įvykį"
description: "Šios procedūros metu „kanban“ taisyklė sukuriama naudojant „kanban“ eilutės įvykio parametrą, kad iš proceso veiklos būtų suaktyvintas atgalinis planavimas."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9d2c2fbd223bd2b410e4a5db87ec468eb25dc87f
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="a4483-103">Kurti „kanban“ taisyklę naudojant „kanban“ eilutės įvykį</span><span class="sxs-lookup"><span data-stu-id="a4483-103">Create a kanban rule using a kanban line event</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4483-104">Šios procedūros metu „kanban“ taisyklė sukuriama naudojant „kanban“ eilutės įvykio parametrą, kad iš proceso veiklos būtų suaktyvintas atgalinis planavimas.</span><span class="sxs-lookup"><span data-stu-id="a4483-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="a4483-105">„Kanban“ taisyklę suaktyvina „kanban“ proceso veikla, kurios kiekvienas kiekis yra lygus arba didesnis už 25.</span><span class="sxs-lookup"><span data-stu-id="a4483-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="a4483-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="a4483-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="a4483-107">Ši užduotis skirta proceso inžinieriui arba vertės srauto vadovui, nes jie parengia naujos arba pakeistos prekės gamybą „lean“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="a4483-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="a4483-108">„Kanban“ taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="a4483-108">Create a kanban rule</span></span>
1. <span data-ttu-id="a4483-109">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="a4483-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="a4483-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a4483-110">Click New.</span></span>
3. <span data-ttu-id="a4483-111">Lauke Papildymo strategija pasirinkite „Įvykis“.</span><span class="sxs-lookup"><span data-stu-id="a4483-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="a4483-112">Taip „kanban“ sugeneruojami tiesiogiai pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="a4483-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="a4483-113">Ši parinktis naudojama siekiant nustatyti taisykles, apibrėžiančias gamybos pagal užsakymą scenarijų</span><span class="sxs-lookup"><span data-stu-id="a4483-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="a4483-114">Lauke Pirmoji plano veikla įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4483-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="a4483-115">Įveskite arba pasirinkite SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="a4483-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="a4483-116">Pirmoji gamybos „kanban“ taisyklės veikla yra gamybos eigos proceso veikla.</span><span class="sxs-lookup"><span data-stu-id="a4483-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="a4483-117">Kai pasirenkate veiklą, veiklos galiojimo datos nukopijuojamos į „kanban“ taisyklės galiojimo datas.</span><span class="sxs-lookup"><span data-stu-id="a4483-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="a4483-118">Išplėskite skyrių Išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="a4483-118">Expand the Details section.</span></span>
6. <span data-ttu-id="a4483-119">Lauke Produktas įveskite L0001.</span><span class="sxs-lookup"><span data-stu-id="a4483-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="a4483-120">Išplėskite skyrių Įvykiai.</span><span class="sxs-lookup"><span data-stu-id="a4483-120">Expand the Events section.</span></span>
8. <span data-ttu-id="a4483-121">Lauke „Kanban“ eilutės įvykis pasirinkite Automatinis.</span><span class="sxs-lookup"><span data-stu-id="a4483-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="a4483-122">Taip įvykio „kanban“ sugeneruojami pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="a4483-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="a4483-123">Laukas naudojamas norint konfigūruoti „kanban“ taisykles, papildančias medžiagą, kurios reikia taikomo proceso veiklai.</span><span class="sxs-lookup"><span data-stu-id="a4483-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="a4483-124">Pasirinkus Automatinis, įvykio „kanban“ sukuriami pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="a4483-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="a4483-125">Šį parametrą rekomenduojama naudoti, jei gamybą planuojate vykdyti tą pačią dieną.</span><span class="sxs-lookup"><span data-stu-id="a4483-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="a4483-126">Nustatykite pasirinkties Mažiausias įvykio kiekis reikšmę „25“.</span><span class="sxs-lookup"><span data-stu-id="a4483-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="a4483-127">Įvykio „kanban“ generuojami, kai poreikio kiekis yra lygus šio lauko reikšmei arba už ją didesnis.</span><span class="sxs-lookup"><span data-stu-id="a4483-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="a4483-128">Tai naudinga norint vienoje mašinoje gaminti užsakymo kiekį, mažesnį nei šio lauko reikšmė, ir kitoje mašinoje gaminti užsakymo kiekį, didesnį nei šio lauko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a4483-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="a4483-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a4483-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="a4483-130">Kurti pardavimo užsakymą ir suaktyvinti „kanban“ grandinę</span><span class="sxs-lookup"><span data-stu-id="a4483-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="a4483-131">Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="a4483-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="a4483-132">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a4483-132">Click New.</span></span>
3. <span data-ttu-id="a4483-133">Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4483-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="a4483-134">Pasirinkite Kliento sąskaita US-003, Miškų didmeninė prekyba.</span><span class="sxs-lookup"><span data-stu-id="a4483-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="a4483-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="a4483-135">Click OK.</span></span>
5. <span data-ttu-id="a4483-136">Lauke „Prekės numeris“ įveskite „L0001“.</span><span class="sxs-lookup"><span data-stu-id="a4483-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="a4483-137">L0001 yra prekė, kuriai sukūrėte „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="a4483-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="a4483-138">Nustatykite kiekį – 27.</span><span class="sxs-lookup"><span data-stu-id="a4483-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="a4483-139">Kadangi skaičius 27 yra didesnis nei minimalus „kanban“ taisyklės kiekis 25, bus suaktyvinta įvykio „kanban“.</span><span class="sxs-lookup"><span data-stu-id="a4483-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="a4483-140">Lauke Vieta įveskite „1“.</span><span class="sxs-lookup"><span data-stu-id="a4483-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="a4483-141">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a4483-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a4483-142">Pasirinkite 13 sandėlį.</span><span class="sxs-lookup"><span data-stu-id="a4483-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="a4483-143">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a4483-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="a4483-144">Peržiūrėti „kanban“, kurį sugeneravo „kanban“ taisyklė</span><span class="sxs-lookup"><span data-stu-id="a4483-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="a4483-145">Pasirinkite Produkto informacijos valdymas > „Lean manufacturing“ > „Kanban“ taisyklės.</span><span class="sxs-lookup"><span data-stu-id="a4483-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="a4483-146">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a4483-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a4483-147">Išplėskite skyrių „Kanbans“.</span><span class="sxs-lookup"><span data-stu-id="a4483-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="a4483-148">Atkreipkite dėmesį, kad kiekio 27 „kanban“ buvo sukurtas siekiant apdoroti veiklą pagal sukurtą „kanban“ taisyklę.</span><span class="sxs-lookup"><span data-stu-id="a4483-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="a4483-149">Tai paskutinis veiksmas.</span><span class="sxs-lookup"><span data-stu-id="a4483-149">This is the last step.</span></span>  


