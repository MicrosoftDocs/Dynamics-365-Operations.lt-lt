---
title: Krovinių ir siuntų planavimas naudojant krovinio planavimo darbo sritį
description: Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4fdff8bdc383a85d604fa6e545c625d5782241f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976818"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="169e7-103">Krovinių ir siuntų planavimas naudojant krovinio planavimo darbo sritį</span><span class="sxs-lookup"><span data-stu-id="169e7-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="169e7-104">Ši procedūra nurodo, kaip naudoti krovinio planavimo darbo sritį norint sukurti krovinį pagal pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="169e7-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="169e7-105">Būtina sąlyga – pirmiausia turime sukurti pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="169e7-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="169e7-106">Ši procedūra yra dalis transportavimo koordinatoriaus kasdienio darbo.</span><span class="sxs-lookup"><span data-stu-id="169e7-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="169e7-107">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="169e7-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="169e7-108">Kurti pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="169e7-108">Create a sales order</span></span>
1. <span data-ttu-id="169e7-109">Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="169e7-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="169e7-110">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="169e7-110">Select **New**.</span></span>
3. <span data-ttu-id="169e7-111">Lauke **Kliento kodas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="169e7-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="169e7-112">Pasirinkite sąskaitą **US-004**.</span><span class="sxs-lookup"><span data-stu-id="169e7-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="169e7-113">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="169e7-113">Select **OK**.</span></span>
6. <span data-ttu-id="169e7-114">Lauke **Prekės numeris** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="169e7-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="169e7-115">Pasirinkti prekę: **A0001**</span><span class="sxs-lookup"><span data-stu-id="169e7-115">Select item **A0001**.</span></span> <span data-ttu-id="169e7-116">**A0001** parengta naudoti transportavimo valdymui.</span><span class="sxs-lookup"><span data-stu-id="169e7-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="169e7-117">Lauke **Puslapis** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą ir tada pasirinkite prekę.</span><span class="sxs-lookup"><span data-stu-id="169e7-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="169e7-118">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="169e7-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="169e7-119">Lauke **Sandėlis** įveskite „24“ šiam pavyzdžiui.</span><span class="sxs-lookup"><span data-stu-id="169e7-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="169e7-120">Šis sandėlis parengtas naudoti transportavimo valdymui ir patobulintam sandėlio valdymui.</span><span class="sxs-lookup"><span data-stu-id="169e7-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="169e7-121">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="169e7-121">Select **Save**.</span></span>
12. <span data-ttu-id="169e7-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="169e7-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="169e7-123">Sukurti naują krovinį</span><span class="sxs-lookup"><span data-stu-id="169e7-123">Create a new load</span></span>
1. <span data-ttu-id="169e7-124">Eikite į **Valdymas skiltį > Moduliai > Transportavimo valdymas > Planavimas > Krovinio planavimo darbo sritis**</span><span class="sxs-lookup"><span data-stu-id="169e7-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="169e7-125">Pasirinkite skirtuką **Pardavimo eilutės**. Dabar sukursite ką tik sukurto pardavimo užsakymo krūvį.</span><span class="sxs-lookup"><span data-stu-id="169e7-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="169e7-126">Krovinius galima sudaryti remiantis pirkimo užsakymų, perkėlimo užsakymų ir pardavimo užsakymų sukuriama pasiūla ir paklausa.</span><span class="sxs-lookup"><span data-stu-id="169e7-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="169e7-127">Veiksmų srityje spauskite **Tiekimas ir poreikis**.</span><span class="sxs-lookup"><span data-stu-id="169e7-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="169e7-128">Pasirinkite **Į naują krovinį**.</span><span class="sxs-lookup"><span data-stu-id="169e7-128">Select **To new load**.</span></span>
5. <span data-ttu-id="169e7-129">Lauke **Krovinio šablono ID** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="169e7-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="169e7-130">Krovinio šablonas apibrėžia didžiausią viso krovinio svorį ir tūrį.</span><span class="sxs-lookup"><span data-stu-id="169e7-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="169e7-131">Pvz., krovinio šablonas gali atitikti sunkvežimio ar konteinerio dydį.</span><span class="sxs-lookup"><span data-stu-id="169e7-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="169e7-132">Pasirinkite prekę.</span><span class="sxs-lookup"><span data-stu-id="169e7-132">Select an item.</span></span>
6. <span data-ttu-id="169e7-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="169e7-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="169e7-134">Nustatyti krovinio tarifą ir maršrutą</span><span class="sxs-lookup"><span data-stu-id="169e7-134">Rate and route the load</span></span>
1. <span data-ttu-id="169e7-135">Pasirinkite **Tarifo ir maršruto planavimas**.</span><span class="sxs-lookup"><span data-stu-id="169e7-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="169e7-136">Pasirinkite **Tarifo ir maršruto darbo sritis**.</span><span class="sxs-lookup"><span data-stu-id="169e7-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="169e7-137">Pasirinkite **Tarifų parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="169e7-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="169e7-138">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="169e7-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="169e7-139">Pasirinkite **Priskirti**.</span><span class="sxs-lookup"><span data-stu-id="169e7-139">Select **Assign**.</span></span>
6. <span data-ttu-id="169e7-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="169e7-140">Close the page.</span></span>

