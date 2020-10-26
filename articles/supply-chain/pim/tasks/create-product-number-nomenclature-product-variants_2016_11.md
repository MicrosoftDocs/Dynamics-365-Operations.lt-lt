---
title: Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas
description: Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5f75d7e493255b9c09c10b121f388854861cb0fc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986004"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="25ae7-103">Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="25ae7-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25ae7-104">Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto.</span><span class="sxs-lookup"><span data-stu-id="25ae7-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="25ae7-105">Šioje procedūroje taip pat parodoma, kaip galima kurti konfigūravimo nomenklatūrą, skirtą produkto konfigūravimo modelio komponentui.</span><span class="sxs-lookup"><span data-stu-id="25ae7-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="25ae7-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="25ae7-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="25ae7-107">Nauja produkto numerių nomenklatūrą yra priskiriama bendrajam produktui D0004.</span><span class="sxs-lookup"><span data-stu-id="25ae7-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="25ae7-108">Paprastai šią užduotį atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="25ae7-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="25ae7-109">Produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="25ae7-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="25ae7-110">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="25ae7-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="25ae7-111">Spustelėkite Produkto nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="25ae7-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="25ae7-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="25ae7-112">Click New.</span></span>
4. <span data-ttu-id="25ae7-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="25ae7-114">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="25ae7-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-115">Click Add.</span></span>
7. <span data-ttu-id="25ae7-116">Spustelėkite Bendrojo produkto numeris.</span><span class="sxs-lookup"><span data-stu-id="25ae7-116">Click Product master number.</span></span>
8. <span data-ttu-id="25ae7-117">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-117">Click Add.</span></span>
9. <span data-ttu-id="25ae7-118">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="25ae7-118">Click Text constant.</span></span>
10. <span data-ttu-id="25ae7-119">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="25ae7-120">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="25ae7-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-121">Click Add.</span></span>
13. <span data-ttu-id="25ae7-122">Spustelėkite Konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="25ae7-122">Click Configuration.</span></span>
14. <span data-ttu-id="25ae7-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25ae7-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="25ae7-124">Produkto numerių nomenklatūros priskyrimas bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="25ae7-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="25ae7-125">Spustelėkite Bendrieji produktai.</span><span class="sxs-lookup"><span data-stu-id="25ae7-125">Click Product masters.</span></span>
2. <span data-ttu-id="25ae7-126">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="25ae7-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="25ae7-127">Pvz., filtruokite lauką Produkto numeris naudodami reikšmę D.</span><span class="sxs-lookup"><span data-stu-id="25ae7-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="25ae7-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="25ae7-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="25ae7-129">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-129">Click Edit.</span></span>
5. <span data-ttu-id="25ae7-130">Lauke Naudoti nomenklatūrą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="25ae7-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="25ae7-131">Lauke Produkto varianto numerių nomenklatūra įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="25ae7-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25ae7-132">Close the page.</span></span>
8. <span data-ttu-id="25ae7-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25ae7-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="25ae7-134">Produkto konfigūracijos modelio komponento nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="25ae7-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="25ae7-135">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="25ae7-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="25ae7-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="25ae7-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="25ae7-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="25ae7-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="25ae7-138">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-138">Click Edit.</span></span>
5. <span data-ttu-id="25ae7-139">Lauke Naudoti konfigūracijos nomenklatūrą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="25ae7-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="25ae7-140">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-140">Click Add.</span></span>
7. <span data-ttu-id="25ae7-141">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="25ae7-141">Click Attribute value.</span></span>
8. <span data-ttu-id="25ae7-142">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="25ae7-143">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="25ae7-144">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-144">Click Add.</span></span>
11. <span data-ttu-id="25ae7-145">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="25ae7-145">Click Text constant.</span></span>
12. <span data-ttu-id="25ae7-146">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="25ae7-147">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="25ae7-148">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-148">Click Add.</span></span>
15. <span data-ttu-id="25ae7-149">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="25ae7-149">Click Attribute value.</span></span>
16. <span data-ttu-id="25ae7-150">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="25ae7-151">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="25ae7-152">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-152">Click Add.</span></span>
19. <span data-ttu-id="25ae7-153">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="25ae7-153">Click Text constant.</span></span>
20. <span data-ttu-id="25ae7-154">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="25ae7-155">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="25ae7-156">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-156">Click Add.</span></span>
23. <span data-ttu-id="25ae7-157">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="25ae7-157">Click Attribute value.</span></span>
24. <span data-ttu-id="25ae7-158">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="25ae7-159">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="25ae7-160">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-160">Click Add.</span></span>
27. <span data-ttu-id="25ae7-161">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="25ae7-161">Click Text constant.</span></span>
28. <span data-ttu-id="25ae7-162">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="25ae7-163">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="25ae7-164">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-164">Click Add.</span></span>
31. <span data-ttu-id="25ae7-165">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="25ae7-165">Click Attribute value.</span></span>
32. <span data-ttu-id="25ae7-166">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="25ae7-167">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="25ae7-168">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-168">Click Add.</span></span>
35. <span data-ttu-id="25ae7-169">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="25ae7-169">Click Text constant.</span></span>
36. <span data-ttu-id="25ae7-170">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="25ae7-171">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="25ae7-172">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="25ae7-172">Click Add.</span></span>
39. <span data-ttu-id="25ae7-173">Spustelėkite Numeracijos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="25ae7-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="25ae7-174">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="25ae7-175">Lauke Numeracija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="25ae7-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="25ae7-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25ae7-176">Close the page.</span></span>
43. <span data-ttu-id="25ae7-177">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25ae7-177">Close the page.</span></span>
44. <span data-ttu-id="25ae7-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="25ae7-178">Close the page.</span></span>

