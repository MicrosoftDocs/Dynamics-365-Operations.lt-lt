---
title: Kurti organizacijos ataskaitų hierarchija
description: Naudokite šią procedūrą, norėdami sukurti ataskaitų hierarchiją organizacijos ataskaitoms.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3db8465c462caffeaf6bd12d17c4b61355ed8eed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208756"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="1ffa6-103">Kurti organizacijos ataskaitų hierarchija</span><span class="sxs-lookup"><span data-stu-id="1ffa6-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ffa6-104">Naudokite šią procedūrą, norėdami sukurti ataskaitų hierarchiją organizacijos ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="1ffa6-105">Šio įrašo paskirtis yra padėti jums dimensijų hierarchijoje, kad jūs galėtumėte tęsti, kol visos organizacijos ataskaitų struktūra bus sukurta.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="1ffa6-106">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="1ffa6-107">Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="1ffa6-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-108">Click New.</span></span>
3. <span data-ttu-id="1ffa6-109">Lauke HierarchyTypeComboBox pasirinkite „Dimensijų klasifikacijos hierarchija“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="1ffa6-110">Pasirinkite Dimensijų klasifikacijos hierarchija.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="1ffa6-111">Tipas Dimensijų klasifikacijos hierarchija naudojamas norint apibrėžti taisykles ir ataskaitų rengimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="1ffa6-112">Jis palaiko visas dimensijas, pavyzdžiui, išlaidų objektus, išlaidų elementus ir statistines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="1ffa6-113">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-113">Click Create.</span></span>
5. <span data-ttu-id="1ffa6-114">Lauke Dimensijų hierarchijos pavadinimas įrašykite „Organizacija USP2“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="1ffa6-115">Lauke Dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="1ffa6-116">Pasirinkite Išlaidų centrai.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="1ffa6-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-117">Click Save.</span></span>
8. <span data-ttu-id="1ffa6-118">Spustelėkite Peržiūrėti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="1ffa6-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-119">Click New.</span></span>
10. <span data-ttu-id="1ffa6-120">Lauke Mazgo pavadinimas įrašykite „CEO“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="1ffa6-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-121">Click Save.</span></span>
12. <span data-ttu-id="1ffa6-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-122">Click New.</span></span>
13. <span data-ttu-id="1ffa6-123">Lauke Mazgo pavadinimas įrašykite „CEO“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="1ffa6-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-124">Click Save.</span></span>
15. <span data-ttu-id="1ffa6-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-125">Click New.</span></span>
16. <span data-ttu-id="1ffa6-126">Lauke Mazgo pavadinimas įrašykite „Rytų regionas“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="1ffa6-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-127">Click Save.</span></span>
18. <span data-ttu-id="1ffa6-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-128">Click New.</span></span>
19. <span data-ttu-id="1ffa6-129">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="1ffa6-130">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1ffa6-131">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="1ffa6-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-132">Click Save.</span></span>
22. <span data-ttu-id="1ffa6-133">Medyje pasirinkite „Oganization USP2\CEO\CEO cost centers“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="1ffa6-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-134">Click New.</span></span>
24. <span data-ttu-id="1ffa6-135">Lauke Mazgo pavadinimas įrašykite „Vakarų regionas“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="1ffa6-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-136">Click Save.</span></span>
26. <span data-ttu-id="1ffa6-137">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-137">Click New.</span></span>
27. <span data-ttu-id="1ffa6-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="1ffa6-139">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1ffa6-140">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="1ffa6-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-141">Click Save.</span></span>
30. <span data-ttu-id="1ffa6-142">Medyje pasirinkite „Oganization USP2\CEO“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="1ffa6-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-143">Click New.</span></span>
32. <span data-ttu-id="1ffa6-144">Lauke Mazgo pavadinimas įrašykite „CFO išlaidų centrai“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="1ffa6-145">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-145">Click Save.</span></span>
34. <span data-ttu-id="1ffa6-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-146">Click New.</span></span>
35. <span data-ttu-id="1ffa6-147">Lauke Mazgo pavadinimas įrašykite „Rinkodaros kampa.“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="1ffa6-148">Lauke Mazgo pavadinimas įrašykite „Rinkodaros kampanija“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="1ffa6-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-149">Click Save.</span></span>
38. <span data-ttu-id="1ffa6-150">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-150">Click New.</span></span>
39. <span data-ttu-id="1ffa6-151">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="1ffa6-152">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1ffa6-153">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="1ffa6-154">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-154">Click Save.</span></span>
42. <span data-ttu-id="1ffa6-155">Medyje pasirinkite „Organization USP2\CEO\CFO cost centers“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="1ffa6-156">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-156">Click New.</span></span>
44. <span data-ttu-id="1ffa6-157">Lauke Mazgo pavadinimas įrašykite „Prekybos mugės“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="1ffa6-158">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-158">Click Save.</span></span>
46. <span data-ttu-id="1ffa6-159">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-159">Click New.</span></span>
47. <span data-ttu-id="1ffa6-160">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="1ffa6-161">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1ffa6-162">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="1ffa6-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-163">Click Save.</span></span>
50. <span data-ttu-id="1ffa6-164">Medyje pasirinkite „Oganization USP2\CEO“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="1ffa6-165">Lauke Mazgo pavadinimas įrašykite „CIO išlaidų centrai“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="1ffa6-166">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-166">Click Save.</span></span>
53. <span data-ttu-id="1ffa6-167">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-167">Click New.</span></span>
54. <span data-ttu-id="1ffa6-168">Lauke Mazgo pavadinimas įrašykite „Skambučių centrai“.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="1ffa6-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-169">Click Save.</span></span>
56. <span data-ttu-id="1ffa6-170">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-170">Click New.</span></span>
57. <span data-ttu-id="1ffa6-171">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="1ffa6-172">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1ffa6-173">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="1ffa6-174">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1ffa6-174">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]