--- 
title: "Kurti maršrutus (tik 2016 m. vasario mėn.)"
description: "Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų gamybos maršrutus."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1c2801af8201865f5ae9233c9729a4d59ef84bcd
ms.openlocfilehash: 2df913543d89a502aecfe7e2fe61265a8a1a121c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="58240-103">Kurti maršrutus (tik 2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="58240-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58240-104">Šios užduoties tikslas yra sukurti galutinių ir pusiau baigtų produktų gamybos maršrutus.</span><span class="sxs-lookup"><span data-stu-id="58240-104">This task focuses on creating the production routes for a finished product and and a semi-finished product.</span></span> <span data-ttu-id="58240-105">Tai penktoji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="58240-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="58240-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="58240-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="58240-107">Kurti pusiau baigto produkto maršrutą</span><span class="sxs-lookup"><span data-stu-id="58240-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="58240-108">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="58240-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="58240-109">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="58240-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="58240-110">Pasirinkite prekės numerį BOM_2.</span><span class="sxs-lookup"><span data-stu-id="58240-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="58240-111">Veiksmų srityje spustelėkite Inžinierius.</span><span class="sxs-lookup"><span data-stu-id="58240-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="58240-112">Spustelėkite Maršrutas.</span><span class="sxs-lookup"><span data-stu-id="58240-112">Click Route.</span></span>
5. <span data-ttu-id="58240-113">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="58240-113">Click New.</span></span>
6. <span data-ttu-id="58240-114">Spustelėkite Maršrutas ir maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="58240-114">Click Route and route version.</span></span>
7. <span data-ttu-id="58240-115">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="58240-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="58240-116">Pavyzdžiui, įveskite ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="58240-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="58240-117">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="58240-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="58240-118">Šiame pavyzdyje įveskite arba pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="58240-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="58240-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="58240-119">Click OK.</span></span>
10. <span data-ttu-id="58240-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="58240-120">Click New.</span></span>
11. <span data-ttu-id="58240-121">Lauke Operacija įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="58240-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="58240-122">Šiame pavyzdyje pasirinkite Surinkimas.</span><span class="sxs-lookup"><span data-stu-id="58240-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="58240-123">Lauke Vykdymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="58240-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="58240-124">Pavyzdžiui, įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="58240-124">For example, type 1.</span></span> <span data-ttu-id="58240-125">Vykdymo laikas dažnai yra apskaičiuotos prekės kainos dalis.</span><span class="sxs-lookup"><span data-stu-id="58240-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="58240-126">Lauke Maršruto grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="58240-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="58240-127">Šiame pavyzdyje pasirinkite Std.</span><span class="sxs-lookup"><span data-stu-id="58240-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="58240-128">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="58240-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="58240-129">Lauke Nustatymų kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="58240-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="58240-130">Šiame pavyzdyje pasirinkite Surinkimas.</span><span class="sxs-lookup"><span data-stu-id="58240-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="58240-131">Spustelėkite skirtuką Laikas.</span><span class="sxs-lookup"><span data-stu-id="58240-131">Click the Times tab.</span></span>
17. <span data-ttu-id="58240-132">Lauke Nustatymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="58240-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="58240-133">Šiame pavyzdyje įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="58240-133">For this example, type 1.</span></span> <span data-ttu-id="58240-134">Nustatymo laikas dažnai yra apskaičiuotos prekės kainos dalis.</span><span class="sxs-lookup"><span data-stu-id="58240-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="58240-135">Veiksmų srityje spustelėkite Maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="58240-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="58240-136">Spustelėkite „Patvirtinti“.</span><span class="sxs-lookup"><span data-stu-id="58240-136">Click Approve.</span></span>
20. <span data-ttu-id="58240-137">Lange Ar norite patvirtinti ir maršrutą? pasirinkite Taip. nurodytas operacijos numeris.</span><span class="sxs-lookup"><span data-stu-id="58240-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="58240-138">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="58240-138">Click OK.</span></span>
22. <span data-ttu-id="58240-139">Veiksmų srityje spustelėkite Maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="58240-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="58240-140">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="58240-140">Click Activate.</span></span>
24. <span data-ttu-id="58240-141">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58240-141">Close the page.</span></span>
25. <span data-ttu-id="58240-142">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58240-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="58240-143">Kurti galutinio produkto maršrutą</span><span class="sxs-lookup"><span data-stu-id="58240-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="58240-144">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="58240-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="58240-145">Pasirinkite prekės numerį BOM_1.</span><span class="sxs-lookup"><span data-stu-id="58240-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="58240-146">Veiksmų srityje spustelėkite Inžinierius.</span><span class="sxs-lookup"><span data-stu-id="58240-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="58240-147">Spustelėkite Maršrutas.</span><span class="sxs-lookup"><span data-stu-id="58240-147">Click Route.</span></span>
4. <span data-ttu-id="58240-148">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="58240-148">Click New.</span></span>
5. <span data-ttu-id="58240-149">Spustelėkite Maršrutas ir maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="58240-149">Click Route and route version.</span></span>
6. <span data-ttu-id="58240-150">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="58240-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="58240-151">Šiame pavyzdyje įveskite ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="58240-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="58240-152">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="58240-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="58240-153">Šiame pavyzdyje įveskite arba pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="58240-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="58240-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="58240-154">Click OK.</span></span>
9. <span data-ttu-id="58240-155">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="58240-155">Click New.</span></span>
10. <span data-ttu-id="58240-156">Lauke Operacija įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="58240-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="58240-157">Šiame pavyzdyje pasirinkite Pakavimas.</span><span class="sxs-lookup"><span data-stu-id="58240-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="58240-158">Lauke Vykdymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="58240-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="58240-159">Šiame pavyzdyje įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="58240-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="58240-160">Lauke Maršruto grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="58240-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="58240-161">Šiame pavyzdyje pasirinkite Std.</span><span class="sxs-lookup"><span data-stu-id="58240-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="58240-162">Spustelėkite skirtuką Nustatymas.</span><span class="sxs-lookup"><span data-stu-id="58240-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="58240-163">Lauke Nustatymų kategorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="58240-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="58240-164">Šiame pavyzdyje pasirinkite Pakavimas.</span><span class="sxs-lookup"><span data-stu-id="58240-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="58240-165">Spustelėkite skirtuką Laikas.</span><span class="sxs-lookup"><span data-stu-id="58240-165">Click the Times tab.</span></span>
16. <span data-ttu-id="58240-166">Lauke Nustatymo laikas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="58240-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="58240-167">Šiame pavyzdyje įveskite 1.</span><span class="sxs-lookup"><span data-stu-id="58240-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="58240-168">Veiksmų srityje spustelėkite Maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="58240-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="58240-169">Spustelėkite „Patvirtinti“.</span><span class="sxs-lookup"><span data-stu-id="58240-169">Click Approve.</span></span>
19. <span data-ttu-id="58240-170">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="58240-170">Click OK.</span></span>
20. <span data-ttu-id="58240-171">Veiksmų srityje spustelėkite Maršruto versija.</span><span class="sxs-lookup"><span data-stu-id="58240-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="58240-172">Spustelėkite Aktyvinti.</span><span class="sxs-lookup"><span data-stu-id="58240-172">Click Activate.</span></span>
22. <span data-ttu-id="58240-173">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58240-173">Close the page.</span></span>
23. <span data-ttu-id="58240-174">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58240-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="58240-175">Įgalinti automatinį nustatymo laiko suvartojimą</span><span class="sxs-lookup"><span data-stu-id="58240-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="58240-176">Eikite į Gamybos kontrolė > Sąranka > Maršrutai > Maršrutų grupės.</span><span class="sxs-lookup"><span data-stu-id="58240-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="58240-177">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="58240-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="58240-178">Sąraše pasirinkite Std.</span><span class="sxs-lookup"><span data-stu-id="58240-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="58240-179">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="58240-179">Click Edit.</span></span>
4. <span data-ttu-id="58240-180">Lauke Nustatymo laikas pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="58240-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="58240-181">Nustatymo laikas dažnai yra apskaičiuotos prekės kainos dalis.</span><span class="sxs-lookup"><span data-stu-id="58240-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="58240-182">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="58240-182">Click Save.</span></span>
6. <span data-ttu-id="58240-183">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="58240-183">Close the page.</span></span>


