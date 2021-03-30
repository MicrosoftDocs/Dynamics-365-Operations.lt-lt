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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a87935f8f30d909f1a6a62ed7be00c83476a36a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214375"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="bf0ab-103">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="bf0ab-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf0ab-104">Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="bf0ab-105">Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USP2.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="bf0ab-106">Kurti sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="bf0ab-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="bf0ab-107">Eikite į Numatytoji ataskaitų sritis.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="bf0ab-108">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="bf0ab-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-109">Click New.</span></span>
4. <span data-ttu-id="bf0ab-110">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-110">Click Sales order.</span></span>
5. <span data-ttu-id="bf0ab-111">Lauke Kliento sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="bf0ab-112">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="bf0ab-112">Example: US-001</span></span>  
6. <span data-ttu-id="bf0ab-113">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-113">Click OK.</span></span>
7. <span data-ttu-id="bf0ab-114">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="bf0ab-115">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="bf0ab-115">Example: P6003</span></span>  
8. <span data-ttu-id="bf0ab-116">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bf0ab-117">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="bf0ab-117">Example: 50000</span></span>  
9. <span data-ttu-id="bf0ab-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="bf0ab-119">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="bf0ab-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="bf0ab-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-120">Close the page.</span></span>
2. <span data-ttu-id="bf0ab-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-121">Close the page.</span></span>
3. <span data-ttu-id="bf0ab-122">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-122">Click Master planning.</span></span>
4. <span data-ttu-id="bf0ab-123">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bf0ab-124">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bf0ab-125">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="bf0ab-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="bf0ab-126">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-126">Click Run.</span></span>
7. <span data-ttu-id="bf0ab-127">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="bf0ab-128">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-128">Click Filter.</span></span>
9. <span data-ttu-id="bf0ab-129">Sąraše pasirinkite lauko eilutę =Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="bf0ab-130">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="bf0ab-131">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="bf0ab-131">Example: P6003</span></span>  
11. <span data-ttu-id="bf0ab-132">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-132">Click OK.</span></span>
12. <span data-ttu-id="bf0ab-133">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-133">Click OK.</span></span>
13. <span data-ttu-id="bf0ab-134">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-134">Click Planned orders.</span></span>
14. <span data-ttu-id="bf0ab-135">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bf0ab-136">Pvz., filtruokite lauką Prekės numeris reikšme „P6000 “.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="bf0ab-137">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="bf0ab-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bf0ab-139">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="bf0ab-140">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="bf0ab-141">Išplėskite arba sutraukite skyrių „Iškvietimas“.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="bf0ab-142">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bf0ab-143">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="bf0ab-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="bf0ab-145">Kurti sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="bf0ab-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="bf0ab-146">Eikite į Numatytoji ataskaitų sritis.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="bf0ab-147">Spustelėkite Pardavimo užsakymo apdorojimas ir užklausa.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="bf0ab-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-148">Click New.</span></span>
4. <span data-ttu-id="bf0ab-149">Spustelėkite Pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-149">Click Sales order.</span></span>
5. <span data-ttu-id="bf0ab-150">Lauke Kliento sąskaita surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="bf0ab-151">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="bf0ab-151">Example: US-001</span></span>  
6. <span data-ttu-id="bf0ab-152">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-152">Click OK.</span></span>
7. <span data-ttu-id="bf0ab-153">Lauke Prekės numeris surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="bf0ab-154">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="bf0ab-154">Example: P6003</span></span>  
8. <span data-ttu-id="bf0ab-155">Lauke Kiekis įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="bf0ab-156">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="bf0ab-156">Example: 50000</span></span>  
9. <span data-ttu-id="bf0ab-157">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="bf0ab-158">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="bf0ab-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="bf0ab-159">Lauke Planas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="bf0ab-160">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bf0ab-161">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="bf0ab-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="bf0ab-162">Spustelėkite Vykdyti.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-162">Click Run.</span></span>
4. <span data-ttu-id="bf0ab-163">Išplėskite arba sutraukite dalį Įtrauktini įrašai.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="bf0ab-164">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-164">Click Filter.</span></span>
6. <span data-ttu-id="bf0ab-165">Sąraše pasirinkite lauko eilutę =Prekės numeris.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="bf0ab-166">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="bf0ab-167">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="bf0ab-167">Example: P6003</span></span>  
8. <span data-ttu-id="bf0ab-168">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-168">Click OK.</span></span>
9. <span data-ttu-id="bf0ab-169">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-169">Click OK.</span></span>
10. <span data-ttu-id="bf0ab-170">Spustelėkite Suplanuoti užsakymai.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-170">Click Planned orders.</span></span>
11. <span data-ttu-id="bf0ab-171">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bf0ab-172">Pvz., filtruokite lauką Prekės numeris reikšme „P6000 “.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="bf0ab-173">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="bf0ab-174">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bf0ab-175">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="bf0ab-176">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="bf0ab-177">Išplėskite arba sutraukite skyrių „Iškvietimas“.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="bf0ab-178">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bf0ab-179">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="bf0ab-180">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-180">Close the page.</span></span>
17. <span data-ttu-id="bf0ab-181">Spustelėkite Bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-181">Click Master planning.</span></span>
18. <span data-ttu-id="bf0ab-182">Eikite į Bendrasis planavimas > Sąranka > Bendrojo planavimo parametrai.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="bf0ab-183">Lauke Išjungti visus planavimo procesus pasirinkite Ne.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="bf0ab-184">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-184">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]