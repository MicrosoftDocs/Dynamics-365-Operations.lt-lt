---
title: Sudėtinių produktų medžiagų plano kūrimas
description: Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714f0c5f014aac1f006b8356de8570ad7d7e0d47
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148083"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="db36e-103">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="db36e-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db36e-104">Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="db36e-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="db36e-105">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USP2.</span><span class="sxs-lookup"><span data-stu-id="db36e-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="db36e-106">Kurti sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="db36e-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="db36e-107">Eikite į Numatytoji ataskaitų sritis.</span><span class="sxs-lookup"><span data-stu-id="db36e-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="db36e-108">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="db36e-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="db36e-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="db36e-109">Click New.</span></span>
4. <span data-ttu-id="db36e-110">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="db36e-110">Click Sales order.</span></span>
5. <span data-ttu-id="db36e-111">Lauke Kliento sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db36e-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="db36e-112">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="db36e-112">Example: US-001</span></span>  
6. <span data-ttu-id="db36e-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="db36e-113">Click OK.</span></span>
7. <span data-ttu-id="db36e-114">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db36e-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="db36e-115">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="db36e-115">Example: P6003</span></span>  
8. <span data-ttu-id="db36e-116">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="db36e-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="db36e-117">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="db36e-117">Example: 50000</span></span>  
9. <span data-ttu-id="db36e-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="db36e-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="db36e-119">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="db36e-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="db36e-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db36e-120">Close the page.</span></span>
2. <span data-ttu-id="db36e-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db36e-121">Close the page.</span></span>
3. <span data-ttu-id="db36e-122">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="db36e-122">Click Master planning.</span></span>
4. <span data-ttu-id="db36e-123">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="db36e-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="db36e-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="db36e-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="db36e-125">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="db36e-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="db36e-126">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="db36e-126">Click Run.</span></span>
7. <span data-ttu-id="db36e-127">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="db36e-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="db36e-128">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="db36e-128">Click Filter.</span></span>
9. <span data-ttu-id="db36e-129">Sąraše pasirinkite lauko eilutę =Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="db36e-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="db36e-130">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db36e-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="db36e-131">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="db36e-131">Example: P6003</span></span>  
11. <span data-ttu-id="db36e-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="db36e-132">Click OK.</span></span>
12. <span data-ttu-id="db36e-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="db36e-133">Click OK.</span></span>
13. <span data-ttu-id="db36e-134">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="db36e-134">Click Planned orders.</span></span>
14. <span data-ttu-id="db36e-135">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="db36e-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="db36e-136">Pvz., filtruokite lauką Prekės numeris reikšme „P6000 “.</span><span class="sxs-lookup"><span data-stu-id="db36e-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="db36e-137">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="db36e-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="db36e-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="db36e-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="db36e-139">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="db36e-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="db36e-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="db36e-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="db36e-141">Išplėskite arba sutraukite skyrių „Iškvietimas“.</span><span class="sxs-lookup"><span data-stu-id="db36e-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="db36e-142">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="db36e-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="db36e-143">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="db36e-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="db36e-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db36e-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="db36e-145">Kurti sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="db36e-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="db36e-146">Eikite į Numatytoji ataskaitų sritis.</span><span class="sxs-lookup"><span data-stu-id="db36e-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="db36e-147">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="db36e-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="db36e-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="db36e-148">Click New.</span></span>
4. <span data-ttu-id="db36e-149">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="db36e-149">Click Sales order.</span></span>
5. <span data-ttu-id="db36e-150">Lauke Kliento sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db36e-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="db36e-151">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="db36e-151">Example: US-001</span></span>  
6. <span data-ttu-id="db36e-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="db36e-152">Click OK.</span></span>
7. <span data-ttu-id="db36e-153">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db36e-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="db36e-154">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="db36e-154">Example: P6003</span></span>  
8. <span data-ttu-id="db36e-155">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="db36e-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="db36e-156">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="db36e-156">Example: 50000</span></span>  
9. <span data-ttu-id="db36e-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="db36e-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="db36e-158">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="db36e-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="db36e-159">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="db36e-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="db36e-160">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="db36e-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="db36e-161">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="db36e-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="db36e-162">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="db36e-162">Click Run.</span></span>
4. <span data-ttu-id="db36e-163">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="db36e-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="db36e-164">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="db36e-164">Click Filter.</span></span>
6. <span data-ttu-id="db36e-165">Sąraše pasirinkite lauko eilutę =Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="db36e-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="db36e-166">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="db36e-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="db36e-167">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="db36e-167">Example: P6003</span></span>  
8. <span data-ttu-id="db36e-168">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="db36e-168">Click OK.</span></span>
9. <span data-ttu-id="db36e-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="db36e-169">Click OK.</span></span>
10. <span data-ttu-id="db36e-170">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="db36e-170">Click Planned orders.</span></span>
11. <span data-ttu-id="db36e-171">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="db36e-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="db36e-172">Pvz., filtruokite lauką Prekės numeris reikšme „P6000 “.</span><span class="sxs-lookup"><span data-stu-id="db36e-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="db36e-173">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="db36e-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="db36e-174">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="db36e-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="db36e-175">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="db36e-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="db36e-176">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="db36e-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="db36e-177">Išplėskite arba sutraukite skyrių „Iškvietimas“.</span><span class="sxs-lookup"><span data-stu-id="db36e-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="db36e-178">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="db36e-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="db36e-179">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="db36e-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="db36e-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db36e-180">Close the page.</span></span>
17. <span data-ttu-id="db36e-181">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="db36e-181">Click Master planning.</span></span>
18. <span data-ttu-id="db36e-182">Eikite į Bendrasis planavimas > Sąranka > Bendrojo planavimo parametrai.</span><span class="sxs-lookup"><span data-stu-id="db36e-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="db36e-183">Lauke Išjungti visus planavimo procesus pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="db36e-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="db36e-184">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="db36e-184">Close the page.</span></span>

