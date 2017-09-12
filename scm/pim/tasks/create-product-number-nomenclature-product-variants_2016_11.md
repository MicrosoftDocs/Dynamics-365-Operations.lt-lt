--- 
title: "Konfigūruotų produkto variantų produkto numerių kūrimas"
description: "Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto."
author: BibiSp
manager: AnnBe
ms.date: 10/25/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e70a5f28635e75a69811085637f7e7431c0f1d40
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-configured-product-variants"></a><span data-ttu-id="8f7ef-103">Konfigūruotų produkto variantų produkto numerių kūrimas</span><span class="sxs-lookup"><span data-stu-id="8f7ef-103">Create a product number for configured product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f7ef-104">Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="8f7ef-105">Šioje procedūroje taip pat parodoma, kaip galima kurti konfigūravimo nomenklatūrą, skirtą produkto konfigūravimo modelio komponentui.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="8f7ef-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8f7ef-107">Nauja produkto numerių nomenklatūrą yra priskiriama bendrajam produktui D0004.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="8f7ef-108">Paprastai šią užduotį atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="8f7ef-109">Produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="8f7ef-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="8f7ef-110">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="8f7ef-111">Spustelėkite Produkto nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="8f7ef-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-112">Click New.</span></span>
4. <span data-ttu-id="8f7ef-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8f7ef-114">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8f7ef-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-115">Click Add.</span></span>
7. <span data-ttu-id="8f7ef-116">Spustelėkite Bendrojo produkto numeris.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-116">Click Product master number.</span></span>
8. <span data-ttu-id="8f7ef-117">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-117">Click Add.</span></span>
9. <span data-ttu-id="8f7ef-118">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-118">Click Text constant.</span></span>
10. <span data-ttu-id="8f7ef-119">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="8f7ef-120">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="8f7ef-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-121">Click Add.</span></span>
13. <span data-ttu-id="8f7ef-122">Spustelėkite Konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-122">Click Configuration.</span></span>
14. <span data-ttu-id="8f7ef-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="8f7ef-124">Produkto numerių nomenklatūros priskyrimas bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="8f7ef-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="8f7ef-125">Spustelėkite Bendrieji produktai.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-125">Click Product masters.</span></span>
2. <span data-ttu-id="8f7ef-126">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8f7ef-127">Pvz., filtruokite lauką Produkto numeris naudodami reikšmę D.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="8f7ef-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8f7ef-129">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-129">Click Edit.</span></span>
5. <span data-ttu-id="8f7ef-130">Lauke Naudoti nomenklatūrą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="8f7ef-131">Lauke Produkto varianto numerių nomenklatūra įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="8f7ef-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-132">Close the page.</span></span>
8. <span data-ttu-id="8f7ef-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="8f7ef-134">Produkto konfigūracijos modelio komponento nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="8f7ef-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="8f7ef-135">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="8f7ef-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8f7ef-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8f7ef-138">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-138">Click Edit.</span></span>
5. <span data-ttu-id="8f7ef-139">Lauke Naudoti konfigūracijos nomenklatūrą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="8f7ef-140">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-140">Click Add.</span></span>
7. <span data-ttu-id="8f7ef-141">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-141">Click Attribute value.</span></span>
8. <span data-ttu-id="8f7ef-142">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="8f7ef-143">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="8f7ef-144">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-144">Click Add.</span></span>
11. <span data-ttu-id="8f7ef-145">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-145">Click Text constant.</span></span>
12. <span data-ttu-id="8f7ef-146">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8f7ef-147">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="8f7ef-148">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-148">Click Add.</span></span>
15. <span data-ttu-id="8f7ef-149">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-149">Click Attribute value.</span></span>
16. <span data-ttu-id="8f7ef-150">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="8f7ef-151">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="8f7ef-152">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-152">Click Add.</span></span>
19. <span data-ttu-id="8f7ef-153">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-153">Click Text constant.</span></span>
20. <span data-ttu-id="8f7ef-154">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="8f7ef-155">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="8f7ef-156">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-156">Click Add.</span></span>
23. <span data-ttu-id="8f7ef-157">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-157">Click Attribute value.</span></span>
24. <span data-ttu-id="8f7ef-158">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="8f7ef-159">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="8f7ef-160">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-160">Click Add.</span></span>
27. <span data-ttu-id="8f7ef-161">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-161">Click Text constant.</span></span>
28. <span data-ttu-id="8f7ef-162">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="8f7ef-163">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="8f7ef-164">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-164">Click Add.</span></span>
31. <span data-ttu-id="8f7ef-165">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-165">Click Attribute value.</span></span>
32. <span data-ttu-id="8f7ef-166">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="8f7ef-167">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="8f7ef-168">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-168">Click Add.</span></span>
35. <span data-ttu-id="8f7ef-169">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-169">Click Text constant.</span></span>
36. <span data-ttu-id="8f7ef-170">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="8f7ef-171">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="8f7ef-172">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-172">Click Add.</span></span>
39. <span data-ttu-id="8f7ef-173">Spustelėkite Numeracijos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="8f7ef-174">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="8f7ef-175">Lauke Numeracija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="8f7ef-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-176">Close the page.</span></span>
43. <span data-ttu-id="8f7ef-177">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-177">Close the page.</span></span>
44. <span data-ttu-id="8f7ef-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8f7ef-178">Close the page.</span></span>


