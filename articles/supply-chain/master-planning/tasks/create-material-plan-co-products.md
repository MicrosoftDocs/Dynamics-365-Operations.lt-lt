---
title: Sudėtinių produktų medžiagų plano kūrimas
description: Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5915dca3af0650883ef5c90dbc50332af5be6cbd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209679"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="08127-103">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="08127-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08127-104">Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="08127-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="08127-105">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USP2.</span><span class="sxs-lookup"><span data-stu-id="08127-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="08127-106">Kurti sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="08127-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="08127-107">Eikite į Numatytoji ataskaitų sritis.</span><span class="sxs-lookup"><span data-stu-id="08127-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="08127-108">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="08127-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="08127-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="08127-109">Click New.</span></span>
4. <span data-ttu-id="08127-110">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="08127-110">Click Sales order.</span></span>
5. <span data-ttu-id="08127-111">Lauke Kliento sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08127-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="08127-112">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="08127-112">Example: US-001</span></span>  
6. <span data-ttu-id="08127-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="08127-113">Click OK.</span></span>
7. <span data-ttu-id="08127-114">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08127-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="08127-115">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="08127-115">Example: P6003</span></span>  
8. <span data-ttu-id="08127-116">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="08127-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="08127-117">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="08127-117">Example: 50000</span></span>  
9. <span data-ttu-id="08127-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="08127-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="08127-119">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="08127-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="08127-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="08127-120">Close the page.</span></span>
2. <span data-ttu-id="08127-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="08127-121">Close the page.</span></span>
3. <span data-ttu-id="08127-122">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="08127-122">Click Master planning.</span></span>
4. <span data-ttu-id="08127-123">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08127-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="08127-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08127-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="08127-125">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="08127-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="08127-126">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="08127-126">Click Run.</span></span>
7. <span data-ttu-id="08127-127">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="08127-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="08127-128">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="08127-128">Click Filter.</span></span>
9. <span data-ttu-id="08127-129">Sąraše pasirinkite lauko eilutę =Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="08127-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="08127-130">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08127-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="08127-131">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="08127-131">Example: P6003</span></span>  
11. <span data-ttu-id="08127-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="08127-132">Click OK.</span></span>
12. <span data-ttu-id="08127-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="08127-133">Click OK.</span></span>
13. <span data-ttu-id="08127-134">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="08127-134">Click Planned orders.</span></span>
14. <span data-ttu-id="08127-135">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="08127-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="08127-136">Pvz., filtruokite lauką Prekės numeris reikšme „P6000 “.</span><span class="sxs-lookup"><span data-stu-id="08127-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="08127-137">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="08127-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="08127-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="08127-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="08127-139">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="08127-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="08127-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08127-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="08127-141">Išplėskite arba sutraukite skyrių „Iškvietimas“.</span><span class="sxs-lookup"><span data-stu-id="08127-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="08127-142">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08127-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="08127-143">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="08127-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="08127-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="08127-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="08127-145">Kurti sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="08127-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="08127-146">Eikite į Numatytoji ataskaitų sritis.</span><span class="sxs-lookup"><span data-stu-id="08127-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="08127-147">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="08127-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="08127-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="08127-148">Click New.</span></span>
4. <span data-ttu-id="08127-149">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="08127-149">Click Sales order.</span></span>
5. <span data-ttu-id="08127-150">Lauke Kliento sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08127-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="08127-151">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="08127-151">Example: US-001</span></span>  
6. <span data-ttu-id="08127-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="08127-152">Click OK.</span></span>
7. <span data-ttu-id="08127-153">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08127-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="08127-154">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="08127-154">Example: P6003</span></span>  
8. <span data-ttu-id="08127-155">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="08127-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="08127-156">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="08127-156">Example: 50000</span></span>  
9. <span data-ttu-id="08127-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="08127-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="08127-158">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="08127-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="08127-159">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="08127-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="08127-160">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08127-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="08127-161">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="08127-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="08127-162">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="08127-162">Click Run.</span></span>
4. <span data-ttu-id="08127-163">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="08127-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="08127-164">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="08127-164">Click Filter.</span></span>
6. <span data-ttu-id="08127-165">Sąraše pasirinkite lauko eilutę =Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="08127-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="08127-166">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="08127-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="08127-167">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="08127-167">Example: P6003</span></span>  
8. <span data-ttu-id="08127-168">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="08127-168">Click OK.</span></span>
9. <span data-ttu-id="08127-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="08127-169">Click OK.</span></span>
10. <span data-ttu-id="08127-170">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="08127-170">Click Planned orders.</span></span>
11. <span data-ttu-id="08127-171">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="08127-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="08127-172">Pvz., filtruokite lauką Prekės numeris reikšme „P6000 “.</span><span class="sxs-lookup"><span data-stu-id="08127-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="08127-173">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="08127-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="08127-174">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="08127-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="08127-175">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="08127-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="08127-176">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08127-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="08127-177">Išplėskite arba sutraukite skyrių „Iškvietimas“.</span><span class="sxs-lookup"><span data-stu-id="08127-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="08127-178">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="08127-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="08127-179">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="08127-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="08127-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="08127-180">Close the page.</span></span>
17. <span data-ttu-id="08127-181">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="08127-181">Click Master planning.</span></span>
18. <span data-ttu-id="08127-182">Eikite į Bendrasis planavimas > Sąranka > Bendrojo planavimo parametrai.</span><span class="sxs-lookup"><span data-stu-id="08127-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="08127-183">Lauke Išjungti visus planavimo procesus pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="08127-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="08127-184">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="08127-184">Close the page.</span></span>

