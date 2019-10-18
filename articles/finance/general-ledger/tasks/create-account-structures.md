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
ms.openlocfilehash: 8b100d5da6ec26dc386c0c6cb0793245531eb0d8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186261"
---
# <a name="create-account-structures"></a><span data-ttu-id="36076-103">Sukurti sąskaitos struktūras</span><span class="sxs-lookup"><span data-stu-id="36076-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36076-104">Šis užduoties vadovas padeda sukurti sąskaitos struktūrą.</span><span class="sxs-lookup"><span data-stu-id="36076-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="36076-105">Veiksmuose naudojama demonstracinių duomenų įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="36076-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="36076-106">Eikite į **Naršymo sritis > Moduliai > Didžioji knyga > Sąskaitų planas > Struktūros > Konfigūruoti sąskaitų struktūras**.</span><span class="sxs-lookup"><span data-stu-id="36076-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="36076-107">**Veiksmų sritis** spustelėkite **Naujas**, kad atidarytumėte tiesioginio dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="36076-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="36076-108">Lauke **Sąskaitos struktūra** įveskite pavadinimą, aprašantį sąskaitos struktūros tikslą.</span><span class="sxs-lookup"><span data-stu-id="36076-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="36076-109">Lauke **Aprašas** įveskite aprašą, apibūdinantį sąskaitos struktūros tikslą.</span><span class="sxs-lookup"><span data-stu-id="36076-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="36076-110">Spustelėkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="36076-110">Click **Create**.</span></span>
6. <span data-ttu-id="36076-111">**Segmentai ir leidžiamos reikšmės** spustelėkite **Įtraukti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="36076-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="36076-112">Matmenų sąraše pažymėkite į sąskaitos struktūrą įtrauktiną matmenį.</span><span class="sxs-lookup"><span data-stu-id="36076-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="36076-113">Sąrašo pabaigoje spustelėkite **Įtraukti segmentą**.</span><span class="sxs-lookup"><span data-stu-id="36076-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="36076-114">Jei reikia, pakartokite 6–9 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="36076-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="36076-115">Skyriuje **Leidžiamos reikšmės išsami informacija** pažymėkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="36076-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="36076-116">Pavyzdžiui, spustelėkite lauką **Pagrindinė sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="36076-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="36076-117">Lauke **Operatorius** pasirinkite parinktį, pvz., „yra tarp“ ir „apima“.</span><span class="sxs-lookup"><span data-stu-id="36076-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="36076-118">Lauke **Reikšmė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36076-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="36076-119">Pavyzdžiui, 600000.</span><span class="sxs-lookup"><span data-stu-id="36076-119">For example, 600000.</span></span>  
13. <span data-ttu-id="36076-120">Lauke **per** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36076-120">In the **through** field, type a value.</span></span> <span data-ttu-id="36076-121">Pavyzdžiui, 699999.</span><span class="sxs-lookup"><span data-stu-id="36076-121">For example, 699999.</span></span>  
14. <span data-ttu-id="36076-122">Skyriuje **Leidžiamos reikšmės išsami informacija** spustelėkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="36076-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="36076-123">Jei reikia, pakartokite 10–15 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="36076-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="36076-124">Skyriuje **Leidžiamos reikšmės išsami informacija** spustelėkite **Įtraukti naujus kriterijus**.</span><span class="sxs-lookup"><span data-stu-id="36076-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="36076-125">Lauke Operatorius, pasirinkite parinktį, pvz., „yra tarp“ ir „apima“.</span><span class="sxs-lookup"><span data-stu-id="36076-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="36076-126">Lauke **Reikšmė** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36076-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="36076-127">Pavyzdžiui, 033.</span><span class="sxs-lookup"><span data-stu-id="36076-127">For example, 033.</span></span>  
19. <span data-ttu-id="36076-128">Lauke **per** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36076-128">In the **through** field, type a value.</span></span> <span data-ttu-id="36076-129">Pavyzdžiui, 034.</span><span class="sxs-lookup"><span data-stu-id="36076-129">For example, 034.</span></span>  
20. <span data-ttu-id="36076-130">Spustelėkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="36076-130">Click **Apply**.</span></span>
21. <span data-ttu-id="36076-131">Tinklelyje pasirinkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="36076-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="36076-132">Pavyzdžiui, Išlaidų centras.</span><span class="sxs-lookup"><span data-stu-id="36076-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="36076-133">Lauke **CostCenter laukas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36076-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="36076-134">Pavyzdžiui, 007..021.</span><span class="sxs-lookup"><span data-stu-id="36076-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="36076-135">**Segmentai ir leidžiamos reikšmės** spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="36076-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="36076-136">Lauke **MainAccount** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36076-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="36076-137">Pavyzdžiui, 600000..699999</span><span class="sxs-lookup"><span data-stu-id="36076-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="36076-138">Tinklelyje pasirinkite segmentą, kad galėtumėte redaguoti leidžiamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="36076-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="36076-139">Pavyzdžiui, Padalinys.</span><span class="sxs-lookup"><span data-stu-id="36076-139">For example, Department.</span></span>  
26. <span data-ttu-id="36076-140">Lauke Padalinys įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36076-140">In the Department field, type a value.</span></span> <span data-ttu-id="36076-141">Pavyzdžiui, 032.</span><span class="sxs-lookup"><span data-stu-id="36076-141">For example, 032.</span></span>  
27. <span data-ttu-id="36076-142">Lauke Išlaidų centras įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="36076-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="36076-143">Pavyzdžiui, 086.</span><span class="sxs-lookup"><span data-stu-id="36076-143">For example, 086.</span></span>  
28. <span data-ttu-id="36076-144">**Veiksmų sritis** spustelėkite **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="36076-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="36076-145">**Veiksmų sritis** spustelėkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="36076-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="36076-146">Spustelėkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="36076-146">Click **Activate**.</span></span>

