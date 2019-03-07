---
title: Kurti pusgaminį (tik 2016 m. vasario mėn.)
description: Šios užduoties tikslas yra sukurti pusiau baigtą produktą.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
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
ms.openlocfilehash: 76fcba3732879f85c9bf0faa6d2481b9c5313a17
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "358950"
---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="0c9f4-103">Kurti pusgaminį (tik 2016 m. vasario mėn.)</span><span class="sxs-lookup"><span data-stu-id="0c9f4-103">Create a semi-finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c9f4-104">Šios užduoties tikslas yra sukurti pusiau baigtą produktą.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="0c9f4-105">Tai antroji KS skaičiavimo sekų užduotis.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="0c9f4-106">Kuriant šią užduotį naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="0c9f4-107">Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0c9f4-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-108">Click New.</span></span>
3. <span data-ttu-id="0c9f4-109">Lauke „Produkto numeris“ įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="0c9f4-110">Šiame pavyzdyje įveskite BOM_2.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="0c9f4-111">Lauke Prekės modelių grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-112">Pažymėkite STD.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-112">Select STD.</span></span> <span data-ttu-id="0c9f4-113">STD – standartinė savikaina yra dažniausiai naudojamas modelis skaičiuojant išlaidas.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="0c9f4-114">Lauke Prekių grupė įveskite arba pasirinkite vertę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-115">Pavyzdžiui, pasirinkite Garso įrašas.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-115">For example, select Audio.</span></span> <span data-ttu-id="0c9f4-116">Išlaidų skaičiavimams tai neturi įtakos.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="0c9f4-117">Lauke Saugojimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-118">Pasirinkite SiteWH.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-118">Select SiteWH.</span></span> <span data-ttu-id="0c9f4-119">Šiame pavyzdyje bus naudojama tik teritorija ir sandėlis.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="0c9f4-120">Lauke Sekimo dimensijų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-121">Šiame pavyzdyje sekimo dimensijos nenaudojamos; pasirinkite Nėra.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="0c9f4-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-122">Click OK.</span></span>
9. <span data-ttu-id="0c9f4-123">Veiksmų srityje spustelėkite Valdyti atsargas.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="0c9f4-124">Spustelėkite Numatytosios užsakymo nuostatos.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-124">Click Default order settings.</span></span>
11. <span data-ttu-id="0c9f4-125">Lauke „Numatytasis užsakymo tipas” pasirinkite „Gamyba”.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="0c9f4-126">Kadangi tai pusiau baigtas produktas, kuris bus gaminamas, pasirinkite Gamyba.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="0c9f4-127">Lauke Pirkimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-128">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="0c9f4-129">Lauke Atsargų vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-130">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="0c9f4-131">Lauke Pardavimo vieta įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-132">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="0c9f4-133">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-133">Close the page.</span></span>
16. <span data-ttu-id="0c9f4-134">Veiksmų srityje spustelėkite Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="0c9f4-135">Spustelėkite Prekės kaina.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-135">Click Item price.</span></span>
18. <span data-ttu-id="0c9f4-136">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-136">Click New.</span></span>
19. <span data-ttu-id="0c9f4-137">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="0c9f4-138">Lauke Versija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-139">Šiame pavyzdyje pasirinkite 10 versiją.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="0c9f4-140">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-141">Šiame pavyzdyje pasirinkite 1 vietą.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="0c9f4-142">Nustatykite Kainą „10”.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="0c9f4-143">Šiame pavyzdyje įveskite savikainą 10.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="0c9f4-144">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-144">Click Save.</span></span>
24. <span data-ttu-id="0c9f4-145">Spustelėkite Suaktyvinti laukiančią kainą (-as).</span><span class="sxs-lookup"><span data-stu-id="0c9f4-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="0c9f4-146">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-146">Close the page.</span></span>
26. <span data-ttu-id="0c9f4-147">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-147">Close the page.</span></span>
27. <span data-ttu-id="0c9f4-148">Spustelėkite BOM_2, kad ją atidarytumėte.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="0c9f4-149">Išplėskite dalį Valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="0c9f4-150">Lauke Išlaidų grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="0c9f4-151">Šiame pavyzdyje pasirinkite Išlaidų grupė M1.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="0c9f4-152">Norėdami įrašyti įrašą, naudokite nuorodą.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="0c9f4-153">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0c9f4-153">Close the page.</span></span>

