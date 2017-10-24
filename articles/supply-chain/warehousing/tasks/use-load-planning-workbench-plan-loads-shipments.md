--- 
title: "Planuoti krovinius ir siuntas naudojant krovinio planavimo darbo sritį"
description: "Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="7729a-103">Planuoti krovinius ir siuntas naudojant krovinio planavimo darbo sritį</span><span class="sxs-lookup"><span data-stu-id="7729a-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7729a-104">Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="7729a-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="7729a-105">Būtina sąlyga – pirmiausia turime sukurti pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="7729a-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="7729a-106">Ši procedūra yra dalis transportavimo koordinatoriaus kasdienio darbo.</span><span class="sxs-lookup"><span data-stu-id="7729a-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="7729a-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="7729a-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="7729a-108">Kurti pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="7729a-108">Create a sales order</span></span>
1. <span data-ttu-id="7729a-109">Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="7729a-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7729a-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="7729a-110">Click New.</span></span>
3. <span data-ttu-id="7729a-111">Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="7729a-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7729a-112">Pasirinkite sąskaitą US-004.</span><span class="sxs-lookup"><span data-stu-id="7729a-112">Select account US-004.</span></span>
5. <span data-ttu-id="7729a-113">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="7729a-113">Click OK.</span></span>
6. <span data-ttu-id="7729a-114">Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="7729a-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="7729a-115">Pasirinkite prekę A0001.</span><span class="sxs-lookup"><span data-stu-id="7729a-115">Select item A0001.</span></span>
    * <span data-ttu-id="7729a-116">A0001 parengta naudoti transportavimo valdymui.</span><span class="sxs-lookup"><span data-stu-id="7729a-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="7729a-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7729a-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="7729a-118">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7729a-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="7729a-119">Lauke „Sandėlis“ įveskite „24“.</span><span class="sxs-lookup"><span data-stu-id="7729a-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="7729a-120">Šiame pavyzdyje pasirinkite 24 sandėlį.</span><span class="sxs-lookup"><span data-stu-id="7729a-120">In this example select warehouse 24.</span></span> <span data-ttu-id="7729a-121">Šis sandėlis parengtas naudoti transportavimo valdymui ir patobulintam sandėlio valdymui.</span><span class="sxs-lookup"><span data-stu-id="7729a-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="7729a-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="7729a-122">Click Save.</span></span>
12. <span data-ttu-id="7729a-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7729a-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="7729a-124">Sukurti naują krovinį</span><span class="sxs-lookup"><span data-stu-id="7729a-124">Create a new load</span></span>
1. <span data-ttu-id="7729a-125">Pasirinkite Transportavimo valdymas > Planavimas > Krovinio planavimo darbo sritis.</span><span class="sxs-lookup"><span data-stu-id="7729a-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="7729a-126">Spustelėkite skirtuką „Pardavimo eilutės“.</span><span class="sxs-lookup"><span data-stu-id="7729a-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="7729a-127">Dabar sudarysite krovinį pardavimo užsakymui, kurį ką tik sukūrėte.</span><span class="sxs-lookup"><span data-stu-id="7729a-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="7729a-128">Krovinius galima sudaryti remiantis pirkimo užsakymų, perkėlimo užsakymų ir pardavimo užsakymų sukuriama pasiūla ir paklausa.</span><span class="sxs-lookup"><span data-stu-id="7729a-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="7729a-129">Veiksmų srityje spustelėkite „Pasiūla ir paklausa“.</span><span class="sxs-lookup"><span data-stu-id="7729a-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="7729a-130">Spustelėkite „Į naują krovin“.</span><span class="sxs-lookup"><span data-stu-id="7729a-130">Click To new load.</span></span>
5. <span data-ttu-id="7729a-131">Lauke „Krovinio šablono ID“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="7729a-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7729a-132">Krovinio šablonas apibrėžia didžiausią viso krovinio svorį ir tūrį.</span><span class="sxs-lookup"><span data-stu-id="7729a-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="7729a-133">Pvz., krovinio šablonas gali atitikti sunkvežimio ar konteinerio dydį.</span><span class="sxs-lookup"><span data-stu-id="7729a-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="7729a-134">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="7729a-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7729a-135">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="7729a-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="7729a-136">Nustatyti krovinio tarifą ir maršrutą</span><span class="sxs-lookup"><span data-stu-id="7729a-136">Rate and route the load</span></span>
1. <span data-ttu-id="7729a-137">Spustelėkite „Tarifo ir maršruto planavimas“.</span><span class="sxs-lookup"><span data-stu-id="7729a-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="7729a-138">Spustelėkite „Tarifo maršruto darbo sritis“.</span><span class="sxs-lookup"><span data-stu-id="7729a-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="7729a-139">Spustelėkite „Tarifo skyrius“.</span><span class="sxs-lookup"><span data-stu-id="7729a-139">Click Rate shop.</span></span>
4. <span data-ttu-id="7729a-140">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="7729a-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7729a-141">Spustelėkite „Priskirti“.</span><span class="sxs-lookup"><span data-stu-id="7729a-141">Click Assign.</span></span>
6. <span data-ttu-id="7729a-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7729a-142">Close the page.</span></span>
7. <span data-ttu-id="7729a-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7729a-143">Close the page.</span></span>


