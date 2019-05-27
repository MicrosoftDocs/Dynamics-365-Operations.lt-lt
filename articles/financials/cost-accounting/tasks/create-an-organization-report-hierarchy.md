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
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a06a67f851e4a73df90f999683d5ea27f38e66
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543938"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="ca0f4-103">Kurti organizacijos ataskaitų hierarchija</span><span class="sxs-lookup"><span data-stu-id="ca0f4-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca0f4-104">Naudokite šią procedūrą, norėdami sukurti ataskaitų hierarchiją organizacijos ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="ca0f4-105">Šio įrašo paskirtis yra padėti jums dimensijų hierarchijoje, kad jūs galėtumėte tęsti, kol visos organizacijos ataskaitų struktūra bus sukurta.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="ca0f4-106">Šiame įraše naudojama demonstracinių duomenų įmonė USP2.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="ca0f4-107">Eikite į Išlaidų apskaita > Dimensijos > Dimensijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="ca0f4-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-108">Click New.</span></span>
3. <span data-ttu-id="ca0f4-109">Lauke HierarchyTypeComboBox pasirinkite „Dimensijų klasifikacijos hierarchija“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="ca0f4-110">Pasirinkite Dimensijų klasifikacijos hierarchija.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="ca0f4-111">Tipas Dimensijų klasifikacijos hierarchija naudojamas norint apibrėžti taisykles ir ataskaitų rengimo tikslais.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="ca0f4-112">Jis palaiko visas dimensijas, pavyzdžiui, išlaidų objektus, išlaidų elementus ir statistines dimensijas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="ca0f4-113">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-113">Click Create.</span></span>
5. <span data-ttu-id="ca0f4-114">Lauke Dimensijų hierarchijos pavadinimas įrašykite „Organizacija USP2“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="ca0f4-115">Lauke Dimensija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="ca0f4-116">Pasirinkite Išlaidų centrai.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="ca0f4-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-117">Click Save.</span></span>
8. <span data-ttu-id="ca0f4-118">Spustelėkite Peržiūrėti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="ca0f4-119">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-119">Click New.</span></span>
10. <span data-ttu-id="ca0f4-120">Lauke Mazgo pavadinimas įrašykite „CEO“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="ca0f4-121">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-121">Click Save.</span></span>
12. <span data-ttu-id="ca0f4-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-122">Click New.</span></span>
13. <span data-ttu-id="ca0f4-123">Lauke Mazgo pavadinimas įrašykite „CEO“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="ca0f4-124">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-124">Click Save.</span></span>
15. <span data-ttu-id="ca0f4-125">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-125">Click New.</span></span>
16. <span data-ttu-id="ca0f4-126">Lauke Mazgo pavadinimas įrašykite „Rytų regionas“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="ca0f4-127">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-127">Click Save.</span></span>
18. <span data-ttu-id="ca0f4-128">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-128">Click New.</span></span>
19. <span data-ttu-id="ca0f4-129">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="ca0f4-130">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ca0f4-131">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="ca0f4-132">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-132">Click Save.</span></span>
22. <span data-ttu-id="ca0f4-133">Medyje pasirinkite „Oganization USP2\CEO\CEO cost centers“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="ca0f4-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-134">Click New.</span></span>
24. <span data-ttu-id="ca0f4-135">Lauke Mazgo pavadinimas įrašykite „Vakarų regionas“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="ca0f4-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-136">Click Save.</span></span>
26. <span data-ttu-id="ca0f4-137">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-137">Click New.</span></span>
27. <span data-ttu-id="ca0f4-138">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="ca0f4-139">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ca0f4-140">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="ca0f4-141">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-141">Click Save.</span></span>
30. <span data-ttu-id="ca0f4-142">Medyje pasirinkite „Oganization USP2\CEO“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="ca0f4-143">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-143">Click New.</span></span>
32. <span data-ttu-id="ca0f4-144">Lauke Mazgo pavadinimas įrašykite „CFO išlaidų centrai“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="ca0f4-145">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-145">Click Save.</span></span>
34. <span data-ttu-id="ca0f4-146">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-146">Click New.</span></span>
35. <span data-ttu-id="ca0f4-147">Lauke Mazgo pavadinimas įrašykite „Rinkodaros kampa.“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="ca0f4-148">Lauke Mazgo pavadinimas įrašykite „Rinkodaros kampanija“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="ca0f4-149">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-149">Click Save.</span></span>
38. <span data-ttu-id="ca0f4-150">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-150">Click New.</span></span>
39. <span data-ttu-id="ca0f4-151">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="ca0f4-152">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ca0f4-153">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="ca0f4-154">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-154">Click Save.</span></span>
42. <span data-ttu-id="ca0f4-155">Medyje pasirinkite „Organization USP2\CEO\CFO cost centers“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="ca0f4-156">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-156">Click New.</span></span>
44. <span data-ttu-id="ca0f4-157">Lauke Mazgo pavadinimas įrašykite „Prekybos mugės“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="ca0f4-158">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-158">Click Save.</span></span>
46. <span data-ttu-id="ca0f4-159">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-159">Click New.</span></span>
47. <span data-ttu-id="ca0f4-160">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="ca0f4-161">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ca0f4-162">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="ca0f4-163">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-163">Click Save.</span></span>
50. <span data-ttu-id="ca0f4-164">Medyje pasirinkite „Oganization USP2\CEO“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="ca0f4-165">Lauke Mazgo pavadinimas įrašykite „CIO išlaidų centrai“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="ca0f4-166">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-166">Click Save.</span></span>
53. <span data-ttu-id="ca0f4-167">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-167">Click New.</span></span>
54. <span data-ttu-id="ca0f4-168">Lauke Mazgo pavadinimas įrašykite „Skambučių centrai“.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="ca0f4-169">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-169">Click Save.</span></span>
56. <span data-ttu-id="ca0f4-170">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-170">Click New.</span></span>
57. <span data-ttu-id="ca0f4-171">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="ca0f4-172">Lauke Iš dimensijų nario įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="ca0f4-173">Pasirinkite dimensijos narį, atitinkantį mazgą.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="ca0f4-174">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ca0f4-174">Click Save.</span></span>

