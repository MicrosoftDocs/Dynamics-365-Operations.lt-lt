--- 
title: "Kurti sudėtinių produktų medžiagų planą"
description: "Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1373a-103">Kurti sudėtinių produktų medžiagų planą</span><span class="sxs-lookup"><span data-stu-id="1373a-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1373a-104">Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="1373a-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="1373a-105">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USP2.</span><span class="sxs-lookup"><span data-stu-id="1373a-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="1373a-106">Kurti sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="1373a-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="1373a-107">Eikite į Numatytoji ataskaitų sritis.</span><span class="sxs-lookup"><span data-stu-id="1373a-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="1373a-108">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="1373a-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="1373a-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1373a-109">Click New.</span></span>
4. <span data-ttu-id="1373a-110">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="1373a-110">Click Sales order.</span></span>
5. <span data-ttu-id="1373a-111">Lauke Kliento sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1373a-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="1373a-112">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="1373a-112">Example: US-001</span></span>  
6. <span data-ttu-id="1373a-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1373a-113">Click OK.</span></span>
7. <span data-ttu-id="1373a-114">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1373a-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1373a-115">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="1373a-115">Example: P6003</span></span>  
8. <span data-ttu-id="1373a-116">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="1373a-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="1373a-117">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="1373a-117">Example: 50000</span></span>  
9. <span data-ttu-id="1373a-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1373a-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="1373a-119">Kurti sudėtinių produktų medžiagų planą</span><span class="sxs-lookup"><span data-stu-id="1373a-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="1373a-120">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="1373a-120">Click Master planning.</span></span>
2. <span data-ttu-id="1373a-121">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="1373a-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="1373a-122">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1373a-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1373a-123">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="1373a-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="1373a-124">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="1373a-124">Click Run.</span></span>
5. <span data-ttu-id="1373a-125">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="1373a-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="1373a-126">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="1373a-126">Click Filter.</span></span>
7. <span data-ttu-id="1373a-127">Sąraše pasirinkite lauko eilutę =Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="1373a-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="1373a-128">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1373a-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="1373a-129">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="1373a-129">Example: P6003</span></span>  
9. <span data-ttu-id="1373a-130">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1373a-130">Click OK.</span></span>
10. <span data-ttu-id="1373a-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="1373a-131">Click OK.</span></span>
11. <span data-ttu-id="1373a-132">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="1373a-132">Click Planned orders.</span></span>
12. <span data-ttu-id="1373a-133">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="1373a-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1373a-134">Pvz., filtruokite lauką Prekės numeris reikšme „P6000 “.</span><span class="sxs-lookup"><span data-stu-id="1373a-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="1373a-135">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="1373a-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="1373a-136">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1373a-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1373a-137">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="1373a-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="1373a-138">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1373a-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="1373a-139">Išplėskite arba sutraukite skyrių „Iškvietimas“.</span><span class="sxs-lookup"><span data-stu-id="1373a-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="1373a-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1373a-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1373a-141">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="1373a-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="1373a-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="1373a-142">Close the page.</span></span>


