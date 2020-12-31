---
title: Sukurti sąskaitos struktūras
description: Šis užduoties vadovas padeda sukurti sąskaitos struktūrą.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b75ee76a1fb874652415a2174441f629955d763a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446071"
---
# <a name="create-account-structures"></a><span data-ttu-id="10621-103">Sukurti sąskaitos struktūras</span><span class="sxs-lookup"><span data-stu-id="10621-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10621-104">Šis užduoties vadovas padeda sukurti sąskaitos struktūrą.</span><span class="sxs-lookup"><span data-stu-id="10621-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="10621-105">Veiksmuose naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="10621-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="10621-106">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Konfigūruoti sąskaitų struktūras**.</span><span class="sxs-lookup"><span data-stu-id="10621-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="10621-107">**Veiksmų sritis** spustelėkite **Naujas**, kad atidarytumėte tiesioginio dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="10621-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="10621-108">Lauke **Sąskaitos struktūra** įveskite pavadinimą, aprašantį sąskaitos struktūros tikslą.</span><span class="sxs-lookup"><span data-stu-id="10621-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="10621-109">Lauke **Aprašas** įveskite aprašą, apibūdinantį sąskaitos struktūros tikslą.</span><span class="sxs-lookup"><span data-stu-id="10621-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="10621-110">Spustelėkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="10621-110">Click **Create**.</span></span>
6. <span data-ttu-id="10621-111">**Segmentai ir leidžiamos reikšmės** spustelėkite **Įtraukti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="10621-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="10621-112">Matmenų sąraše pažymėkite į sąskaitos struktūrą įtrauktiną matmenį.</span><span class="sxs-lookup"><span data-stu-id="10621-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="10621-113">Sąrašo pabaigoje spustelėkite **Įtraukti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="10621-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="10621-114">Jei reikia, pakartokite 6–9 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="10621-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="10621-115">Skyriuje **Leidžiamos reikšmės išsami informacija** pažymėkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="10621-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="10621-116">Pavyzdžiui, spustelėkite lauką **Pagrindinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="10621-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="10621-117">Lauke **Operatorius** pasirinkite parinktį, pvz., „yra tarp“ ir „apima“.</span><span class="sxs-lookup"><span data-stu-id="10621-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="10621-118">Lauke **Reikšmė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10621-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="10621-119">Pavyzdžiui, 600000.</span><span class="sxs-lookup"><span data-stu-id="10621-119">For example, 600000.</span></span>  
13. <span data-ttu-id="10621-120">Lauke **per** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10621-120">In the **through** field, type a value.</span></span> <span data-ttu-id="10621-121">Pavyzdžiui, 699999.</span><span class="sxs-lookup"><span data-stu-id="10621-121">For example, 699999.</span></span>  
14. <span data-ttu-id="10621-122">Skyriuje **Leidžiamos reikšmės išsami informacija** spustelėkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="10621-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="10621-123">Jei reikia, pakartokite 10–15 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="10621-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="10621-124">Skyriuje **Leidžiamos reikšmės išsami informacija** spustelėkite **Įtraukti naujus kriterijus**.</span><span class="sxs-lookup"><span data-stu-id="10621-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="10621-125">Lauke Operatorius, pasirinkite parinktį, pvz., „yra tarp“ ir „apima“.</span><span class="sxs-lookup"><span data-stu-id="10621-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="10621-126">Lauke **Reikšmė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10621-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="10621-127">Pavyzdžiui, 033.</span><span class="sxs-lookup"><span data-stu-id="10621-127">For example, 033.</span></span>  
19. <span data-ttu-id="10621-128">Lauke **per** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10621-128">In the **through** field, type a value.</span></span> <span data-ttu-id="10621-129">Pavyzdžiui, 034.</span><span class="sxs-lookup"><span data-stu-id="10621-129">For example, 034.</span></span>  
20. <span data-ttu-id="10621-130">Spustelėkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="10621-130">Click **Apply**.</span></span>
21. <span data-ttu-id="10621-131">Tinklelyje pasirinkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="10621-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="10621-132">Pavyzdžiui, Išlaidų centras.</span><span class="sxs-lookup"><span data-stu-id="10621-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="10621-133">Lauke **CostCenter laukas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10621-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="10621-134">Pavyzdžiui, 007..021.</span><span class="sxs-lookup"><span data-stu-id="10621-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="10621-135">**Segmentai ir leidžiamos reikšmės** spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="10621-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="10621-136">Lauke **MainAccount** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10621-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="10621-137">Pavyzdžiui, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="10621-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="10621-138">Tinklelyje pasirinkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="10621-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="10621-139">Pavyzdžiui, Padalinys.</span><span class="sxs-lookup"><span data-stu-id="10621-139">For example, Department.</span></span>  
26. <span data-ttu-id="10621-140">Lauke Padalinys įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10621-140">In the Department field, type a value.</span></span> <span data-ttu-id="10621-141">Pavyzdžiui, 032.</span><span class="sxs-lookup"><span data-stu-id="10621-141">For example, 032.</span></span>  
27. <span data-ttu-id="10621-142">Lauke Išlaidų centras įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="10621-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="10621-143">Pavyzdžiui, 086.</span><span class="sxs-lookup"><span data-stu-id="10621-143">For example, 086.</span></span>  
28. <span data-ttu-id="10621-144">**Veiksmų sritis** spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="10621-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="10621-145">**Veiksmų sritis** spustelėkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="10621-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="10621-146">Spustelėkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="10621-146">Click **Activate**.</span></span>

