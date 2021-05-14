---
title: Sudėtinių produktų medžiagų plano kūrimas
description: Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920734"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0c890-103">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="0c890-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c890-104">Gamybos planuotojas planuoja medžiagų poreikius prekėms, kurios yra formulės sudėtiniai produktai.</span><span class="sxs-lookup"><span data-stu-id="0c890-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="0c890-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USP2.</span><span class="sxs-lookup"><span data-stu-id="0c890-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="0c890-106">Kurti sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="0c890-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="0c890-107">Eikite **į pardavimo ir rinkodaros darbo sričių pardavimo užsakymo \> \> apdorojimą ir užklausą**.</span><span class="sxs-lookup"><span data-stu-id="0c890-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="0c890-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0c890-108">Select **New**.</span></span>
1. <span data-ttu-id="0c890-109">Pasirinkite **Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="0c890-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="0c890-110">Lauke **Kliento sąskaita** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c890-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="0c890-111">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="0c890-111">Example: US-001</span></span>  
1. <span data-ttu-id="0c890-112">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-112">Select **OK**.</span></span>
1. <span data-ttu-id="0c890-113">Lauke **Prekės numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="0c890-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="0c890-114">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="0c890-114">Example: P6003</span></span>  
1. <span data-ttu-id="0c890-115">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0c890-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="0c890-116">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="0c890-116">Example: 50000</span></span>  
1. <span data-ttu-id="0c890-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0c890-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0c890-118">Sudėtinių produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="0c890-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="0c890-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c890-119">Close the page.</span></span>
1. <span data-ttu-id="0c890-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c890-120">Close the page.</span></span>
1. <span data-ttu-id="0c890-121">Pasirinkite **Bendrasis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="0c890-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="0c890-122">Lauke **Planas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0c890-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="0c890-123">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0c890-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="0c890-124">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="0c890-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="0c890-125">Pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="0c890-125">Select **Run**.</span></span>
1. <span data-ttu-id="0c890-126">Išplėskite arba sutraukite dalį **įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="0c890-127">Pasirinkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="0c890-127">Select **Filter**.</span></span>
1. <span data-ttu-id="0c890-128">Sąraše pasirinkite lauko eilutę **Laukelis** = *Elemento numeris*.</span><span class="sxs-lookup"><span data-stu-id="0c890-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="0c890-129">Lauke **Kriterijai** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c890-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="0c890-130">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="0c890-130">Example: P6003</span></span>  
1. <span data-ttu-id="0c890-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-131">Select **OK**.</span></span>
1. <span data-ttu-id="0c890-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-132">Select **OK**.</span></span>
1. <span data-ttu-id="0c890-133">Pažymėkite **Suplanuoti užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="0c890-134">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="0c890-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0c890-135">Pvz., filtruokite lauką **Prekės numeris** reikšme 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="0c890-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="0c890-136">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="0c890-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="0c890-137">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0c890-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0c890-138">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="0c890-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="0c890-139">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0c890-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="0c890-140">Išplėskite skyrių **Susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="0c890-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="0c890-141">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0c890-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="0c890-142">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="0c890-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="0c890-143">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c890-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="0c890-144">Kurti antrą sudėtinio produkto poreikį</span><span class="sxs-lookup"><span data-stu-id="0c890-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="0c890-145">Eikite **į pardavimo ir rinkodaros darbo sričių pardavimo užsakymo \> \> apdorojimą ir užklausą**.</span><span class="sxs-lookup"><span data-stu-id="0c890-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="0c890-146">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0c890-146">Select **New**.</span></span>
1. <span data-ttu-id="0c890-147">Pasirinkite **Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="0c890-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="0c890-148">Lauke **Kliento sąskaita** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c890-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="0c890-149">Pavyzdys: US-001</span><span class="sxs-lookup"><span data-stu-id="0c890-149">Example: US-001</span></span>  
1. <span data-ttu-id="0c890-150">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-150">Select **OK**.</span></span>
1. <span data-ttu-id="0c890-151">Lauke **Prekės numeris** įveskite vertę.</span><span class="sxs-lookup"><span data-stu-id="0c890-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="0c890-152">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="0c890-152">Example: P6003</span></span>  
1. <span data-ttu-id="0c890-153">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0c890-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="0c890-154">Pavyzdys: 50000</span><span class="sxs-lookup"><span data-stu-id="0c890-154">Example: 50000</span></span>  
1. <span data-ttu-id="0c890-155">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0c890-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="0c890-156">Sudėtinių antrų produktų medžiagų plano kūrimas</span><span class="sxs-lookup"><span data-stu-id="0c890-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="0c890-157">Lauke **Planas** pasirinkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="0c890-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="0c890-158">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0c890-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="0c890-159">Pavyzdys: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="0c890-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="0c890-160">Pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="0c890-160">Select **Run**.</span></span>
4. <span data-ttu-id="0c890-161">Išplėskite arba sutraukite dalį **įtrauktini įrašai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="0c890-162">Pasirinkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="0c890-162">Select **Filter**.</span></span>
6. <span data-ttu-id="0c890-163">Sąraše pasirinkite lauko eilutę **Laukelis** = *Elemento numeris*.</span><span class="sxs-lookup"><span data-stu-id="0c890-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="0c890-164">Lauke *Kriterijai* įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c890-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="0c890-165">Pavyzdys: P6003</span><span class="sxs-lookup"><span data-stu-id="0c890-165">Example: P6003</span></span>  
8. <span data-ttu-id="0c890-166">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-166">Select **OK**.</span></span>
9. <span data-ttu-id="0c890-167">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-167">Select **OK**.</span></span>
10. <span data-ttu-id="0c890-168">Pažymėkite **Suplanuoti užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="0c890-169">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="0c890-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0c890-170">Pvz., filtruokite lauką **Prekės numeris** reikšme 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="0c890-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="0c890-171">Filtruokite pagal sudėtinę prekę, kuri turi prekės, kuriai sukūrėte pardavimo užsakymą, sudėtinį produktą.</span><span class="sxs-lookup"><span data-stu-id="0c890-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="0c890-172">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0c890-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0c890-173">Pasirinkite vieną iš filtro pateiktų eilučių.</span><span class="sxs-lookup"><span data-stu-id="0c890-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="0c890-174">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0c890-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="0c890-175">Išplėskite arba sutraukite skyrių **Susiejimas**.</span><span class="sxs-lookup"><span data-stu-id="0c890-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="0c890-176">Šiame sąraše pasirinkite nuorodą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0c890-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="0c890-177">Suplanuotas užsakymas yra susietas su sudėtinio produkto pardavimo užsakymu.</span><span class="sxs-lookup"><span data-stu-id="0c890-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="0c890-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c890-178">Close the page.</span></span>
17. <span data-ttu-id="0c890-179">Pasirinkite **Bendrasis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="0c890-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="0c890-180">Eikite į **Bendrasis planavimas \> Sąranka \> Bendrojo planavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="0c890-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="0c890-181">Rinkitės *Ne* lauke **Išjungti visus planavimo procesus**.</span><span class="sxs-lookup"><span data-stu-id="0c890-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="0c890-182">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c890-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]