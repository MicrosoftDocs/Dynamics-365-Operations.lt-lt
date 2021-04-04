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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07922a20d5c99640f32bb28ddddaffe846440667
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258880"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="a6f7c-103">Sukonfigūruotų produkto variantų produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="a6f7c-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6f7c-104">Šioje procedūroje parodoma, kaip nustatyti sukonfigūruotų produkto variantų produkto numerių nomenklatūrą ir kaip ją galima pridėti prie konfigūruojamo bendrojo produkto.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="a6f7c-105">Šioje procedūroje taip pat parodoma, kaip galima kurti konfigūravimo nomenklatūrą, skirtą produkto konfigūravimo modelio komponentui.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="a6f7c-106">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a6f7c-107">Nauja produkto numerių nomenklatūrą yra priskiriama bendrajam produktui D0004.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="a6f7c-108">Paprastai šią užduotį atlieka produkto kūrėjas.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="a6f7c-109">Produkto numerių nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="a6f7c-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="a6f7c-110">Spustelėkite Produkto varianto modelio aprašą.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a6f7c-111">Spustelėkite Produkto nomenklatūra.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="a6f7c-112">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-112">Click New.</span></span>
4. <span data-ttu-id="a6f7c-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a6f7c-114">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a6f7c-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-115">Click Add.</span></span>
7. <span data-ttu-id="a6f7c-116">Spustelėkite Bendrojo produkto numeris.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-116">Click Product master number.</span></span>
8. <span data-ttu-id="a6f7c-117">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-117">Click Add.</span></span>
9. <span data-ttu-id="a6f7c-118">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-118">Click Text constant.</span></span>
10. <span data-ttu-id="a6f7c-119">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="a6f7c-120">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="a6f7c-121">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-121">Click Add.</span></span>
13. <span data-ttu-id="a6f7c-122">Spustelėkite Konfigūravimas.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-122">Click Configuration.</span></span>
14. <span data-ttu-id="a6f7c-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="a6f7c-124">Produkto numerių nomenklatūros priskyrimas bendrajam produktui</span><span class="sxs-lookup"><span data-stu-id="a6f7c-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="a6f7c-125">Spustelėkite Bendrieji produktai.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-125">Click Product masters.</span></span>
2. <span data-ttu-id="a6f7c-126">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a6f7c-127">Pvz., filtruokite lauką Produkto numeris naudodami reikšmę D.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="a6f7c-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a6f7c-129">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-129">Click Edit.</span></span>
5. <span data-ttu-id="a6f7c-130">Lauke Naudoti nomenklatūrą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="a6f7c-131">Lauke Produkto varianto numerių nomenklatūra įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="a6f7c-132">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-132">Close the page.</span></span>
8. <span data-ttu-id="a6f7c-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="a6f7c-134">Produkto konfigūracijos modelio komponento nomenklatūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="a6f7c-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="a6f7c-135">Spustelėkite Produkto konfigūracijos modeliai.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="a6f7c-136">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a6f7c-137">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a6f7c-138">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-138">Click Edit.</span></span>
5. <span data-ttu-id="a6f7c-139">Lauke Naudoti konfigūracijos nomenklatūrą pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="a6f7c-140">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-140">Click Add.</span></span>
7. <span data-ttu-id="a6f7c-141">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-141">Click Attribute value.</span></span>
8. <span data-ttu-id="a6f7c-142">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="a6f7c-143">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="a6f7c-144">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-144">Click Add.</span></span>
11. <span data-ttu-id="a6f7c-145">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-145">Click Text constant.</span></span>
12. <span data-ttu-id="a6f7c-146">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="a6f7c-147">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="a6f7c-148">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-148">Click Add.</span></span>
15. <span data-ttu-id="a6f7c-149">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-149">Click Attribute value.</span></span>
16. <span data-ttu-id="a6f7c-150">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="a6f7c-151">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="a6f7c-152">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-152">Click Add.</span></span>
19. <span data-ttu-id="a6f7c-153">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-153">Click Text constant.</span></span>
20. <span data-ttu-id="a6f7c-154">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="a6f7c-155">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="a6f7c-156">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-156">Click Add.</span></span>
23. <span data-ttu-id="a6f7c-157">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-157">Click Attribute value.</span></span>
24. <span data-ttu-id="a6f7c-158">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="a6f7c-159">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="a6f7c-160">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-160">Click Add.</span></span>
27. <span data-ttu-id="a6f7c-161">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-161">Click Text constant.</span></span>
28. <span data-ttu-id="a6f7c-162">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="a6f7c-163">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="a6f7c-164">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-164">Click Add.</span></span>
31. <span data-ttu-id="a6f7c-165">Spustelėkite Atributo reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-165">Click Attribute value.</span></span>
32. <span data-ttu-id="a6f7c-166">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="a6f7c-167">Lauke Atributas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="a6f7c-168">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-168">Click Add.</span></span>
35. <span data-ttu-id="a6f7c-169">Spustelėkite Teksto konstanta.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-169">Click Text constant.</span></span>
36. <span data-ttu-id="a6f7c-170">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="a6f7c-171">Lauke „Tekstas“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="a6f7c-172">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-172">Click Add.</span></span>
39. <span data-ttu-id="a6f7c-173">Spustelėkite Numeracijos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="a6f7c-174">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="a6f7c-175">Lauke Numeracija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="a6f7c-176">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-176">Close the page.</span></span>
43. <span data-ttu-id="a6f7c-177">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-177">Close the page.</span></span>
44. <span data-ttu-id="a6f7c-178">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a6f7c-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]