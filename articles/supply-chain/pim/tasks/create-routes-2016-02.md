---
title: Kurti maršrutus (2016 m. vasario mėn.)
description: Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų gamybos maršrutus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567865"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="428ca-103">Kurti maršrutus (2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="428ca-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="428ca-104">Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų gamybos maršrutus.</span><span class="sxs-lookup"><span data-stu-id="428ca-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="428ca-105">Tai penktoji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="428ca-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="428ca-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="428ca-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="428ca-107">Kurti pusiau baigto produkto maršrutą</span><span class="sxs-lookup"><span data-stu-id="428ca-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="428ca-108">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="428ca-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="428ca-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="428ca-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="428ca-110">Pasirinkite prekės numerį BOM_2.</span><span class="sxs-lookup"><span data-stu-id="428ca-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="428ca-111">Veiksmų srityje spustelėkite Inžinierius.</span><span class="sxs-lookup"><span data-stu-id="428ca-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="428ca-112">Spustelėkite Maršrutas.</span><span class="sxs-lookup"><span data-stu-id="428ca-112">Click Route.</span></span>
5. <span data-ttu-id="428ca-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="428ca-113">Click New.</span></span>
6. <span data-ttu-id="428ca-114">Spustelėkite Maršrutas ir maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="428ca-114">Click Route and route version.</span></span>
7. <span data-ttu-id="428ca-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="428ca-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="428ca-116">Pavyzdžiui, įveskite ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="428ca-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="428ca-117">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="428ca-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="428ca-118">Šiame pavyzdyje įveskite arba pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="428ca-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="428ca-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="428ca-119">Click OK.</span></span>
10. <span data-ttu-id="428ca-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="428ca-120">Click New.</span></span>
11. <span data-ttu-id="428ca-121">Lauke Operacija įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="428ca-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="428ca-122">Šiame pavyzdyje pasirinkite Surinkimas.</span><span class="sxs-lookup"><span data-stu-id="428ca-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="428ca-123">Lauke Vykdymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="428ca-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="428ca-124">Pavyzdžiui, įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="428ca-124">For example, type 1.</span></span> <span data-ttu-id="428ca-125">Vykdymo laikas dažnai yra apskaičiuotos prekės kainos dalis.</span><span class="sxs-lookup"><span data-stu-id="428ca-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="428ca-126">Lauke Maršruto grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="428ca-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="428ca-127">Šiame pavyzdyje pasirinkite Std.</span><span class="sxs-lookup"><span data-stu-id="428ca-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="428ca-128">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="428ca-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="428ca-129">Lauke Nustatymų kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="428ca-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="428ca-130">Šiame pavyzdyje pasirinkite Surinkimas.</span><span class="sxs-lookup"><span data-stu-id="428ca-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="428ca-131">Spustelėkite skirtuką Laikas.</span><span class="sxs-lookup"><span data-stu-id="428ca-131">Click the Times tab.</span></span>
17. <span data-ttu-id="428ca-132">Lauke Nustatymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="428ca-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="428ca-133">Šiame pavyzdyje įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="428ca-133">For this example, type 1.</span></span> <span data-ttu-id="428ca-134">Nustatymo laikas dažnai yra apskaičiuotos prekės kainos dalis.</span><span class="sxs-lookup"><span data-stu-id="428ca-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="428ca-135">Veiksmų srityje spustelėkite Maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="428ca-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="428ca-136">Spustelėkite „Patvirtinti“.</span><span class="sxs-lookup"><span data-stu-id="428ca-136">Click Approve.</span></span>
20. <span data-ttu-id="428ca-137">Lange Ar norite patvirtinti ir maršrutą? pasirinkite Taip. nurodytas operacijos numeris.</span><span class="sxs-lookup"><span data-stu-id="428ca-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="428ca-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="428ca-138">Click OK.</span></span>
22. <span data-ttu-id="428ca-139">Veiksmų srityje spustelėkite Maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="428ca-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="428ca-140">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="428ca-140">Click Activate.</span></span>
24. <span data-ttu-id="428ca-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="428ca-141">Close the page.</span></span>
25. <span data-ttu-id="428ca-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="428ca-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="428ca-143">Kurti galutinio produkto maršrutą</span><span class="sxs-lookup"><span data-stu-id="428ca-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="428ca-144">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="428ca-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="428ca-145">Pasirinkite prekės numerį BOM_1.</span><span class="sxs-lookup"><span data-stu-id="428ca-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="428ca-146">Veiksmų srityje spustelėkite Inžinierius.</span><span class="sxs-lookup"><span data-stu-id="428ca-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="428ca-147">Spustelėkite Maršrutas.</span><span class="sxs-lookup"><span data-stu-id="428ca-147">Click Route.</span></span>
4. <span data-ttu-id="428ca-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="428ca-148">Click New.</span></span>
5. <span data-ttu-id="428ca-149">Spustelėkite Maršrutas ir maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="428ca-149">Click Route and route version.</span></span>
6. <span data-ttu-id="428ca-150">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="428ca-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="428ca-151">Šiame pavyzdyje įveskite ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="428ca-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="428ca-152">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="428ca-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="428ca-153">Šiame pavyzdyje įveskite arba pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="428ca-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="428ca-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="428ca-154">Click OK.</span></span>
9. <span data-ttu-id="428ca-155">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="428ca-155">Click New.</span></span>
10. <span data-ttu-id="428ca-156">Lauke Operacija įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="428ca-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="428ca-157">Šiame pavyzdyje pasirinkite Pakavimas.</span><span class="sxs-lookup"><span data-stu-id="428ca-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="428ca-158">Lauke Vykdymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="428ca-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="428ca-159">Šiame pavyzdyje įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="428ca-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="428ca-160">Lauke Maršruto grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="428ca-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="428ca-161">Šiame pavyzdyje pasirinkite Std.</span><span class="sxs-lookup"><span data-stu-id="428ca-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="428ca-162">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="428ca-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="428ca-163">Lauke Nustatymų kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="428ca-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="428ca-164">Šiame pavyzdyje pasirinkite Pakavimas.</span><span class="sxs-lookup"><span data-stu-id="428ca-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="428ca-165">Spustelėkite skirtuką Laikas.</span><span class="sxs-lookup"><span data-stu-id="428ca-165">Click the Times tab.</span></span>
16. <span data-ttu-id="428ca-166">Lauke Nustatymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="428ca-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="428ca-167">Šiame pavyzdyje įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="428ca-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="428ca-168">Veiksmų srityje spustelėkite Maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="428ca-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="428ca-169">Spustelėkite „Patvirtinti“.</span><span class="sxs-lookup"><span data-stu-id="428ca-169">Click Approve.</span></span>
19. <span data-ttu-id="428ca-170">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="428ca-170">Click OK.</span></span>
20. <span data-ttu-id="428ca-171">Veiksmų srityje spustelėkite Maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="428ca-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="428ca-172">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="428ca-172">Click Activate.</span></span>
22. <span data-ttu-id="428ca-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="428ca-173">Close the page.</span></span>
23. <span data-ttu-id="428ca-174">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="428ca-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="428ca-175">Įgalinti automatinį nustatymo laiko suvartojimą</span><span class="sxs-lookup"><span data-stu-id="428ca-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="428ca-176">Eikite į Gamybos kontrolė > Sąranka > Maršrutai > Maršrutų grupės.</span><span class="sxs-lookup"><span data-stu-id="428ca-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="428ca-177">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="428ca-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="428ca-178">Sąraše pasirinkite Std.</span><span class="sxs-lookup"><span data-stu-id="428ca-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="428ca-179">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="428ca-179">Click Edit.</span></span>
4. <span data-ttu-id="428ca-180">Lauke Nustatymo laikas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="428ca-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="428ca-181">Nustatymo laikas dažnai yra apskaičiuotos prekės kainos dalis.</span><span class="sxs-lookup"><span data-stu-id="428ca-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="428ca-182">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="428ca-182">Click Save.</span></span>
6. <span data-ttu-id="428ca-183">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="428ca-183">Close the page.</span></span>

