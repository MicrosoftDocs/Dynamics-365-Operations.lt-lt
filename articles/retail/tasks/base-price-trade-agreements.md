---
title: " Bazinė kaina ir prekybos sutartys"
description: Ši procedūra padeda kurti konkretaus kanalo pardavimo kainos prekybos sutartis.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45d3d962958d0487c9e65910a2dce24097a83773
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017763"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="b10d6-103"> Bazinė kaina ir prekybos sutartys</span><span class="sxs-lookup"><span data-stu-id="b10d6-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="b10d6-104">Ši procedūra padeda kurti konkretaus kanalo pardavimo kainos prekybos sutartis.</span><span class="sxs-lookup"><span data-stu-id="b10d6-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="b10d6-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="b10d6-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="b10d6-106">**Naršymo sritis** eikite į **Moduliai > Mažmena ir komercija > Kainodaros ir nuolaidų valdymas > Kainų grupės > Visos kainų grupės**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-106">In the **Navigation pane**, go to **Modules > Retail and commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="b10d6-107">Naudojant kainų grupes, prekybos sutartys priskiriamos konkretiems kanalams.</span><span class="sxs-lookup"><span data-stu-id="b10d6-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="b10d6-108">Naudojant kainų grupes prekybos sutartims kanalui priskirti, galima nustatyti konkretaus kanalo kainas.</span><span class="sxs-lookup"><span data-stu-id="b10d6-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="b10d6-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-109">Click **New**.</span></span>
3. <span data-ttu-id="b10d6-110">Lauke **Kainų grupės** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b10d6-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="b10d6-111">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b10d6-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="b10d6-112">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-112">Click **Save**.</span></span>
6. <span data-ttu-id="b10d6-113">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b10d6-113">Close the page.</span></span>
7. <span data-ttu-id="b10d6-114">**Naršymo sritis** eikite į **Moduliai > Mažmena ir komercija > Kanalai > Parduotuvės > Visos parduotuvės**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-114">In the **Navigation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
8. <span data-ttu-id="b10d6-115">Sąraše pasirinkite „Niujorkas“.</span><span class="sxs-lookup"><span data-stu-id="b10d6-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="b10d6-116">Veiksmų srityje spustelėkite **Parduotuvė**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="b10d6-117">Spustelėkite **Kainų grupės**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="b10d6-118">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-118">Click **New**.</span></span>
12. <span data-ttu-id="b10d6-119">Lauke **Kainų grupės** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b10d6-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="b10d6-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b10d6-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b10d6-121">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-121">Click **Save**.</span></span>
15. <span data-ttu-id="b10d6-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b10d6-122">Close the page.</span></span>
16. <span data-ttu-id="b10d6-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b10d6-123">Close the page.</span></span>
17. <span data-ttu-id="b10d6-124">**Naršymo sritis** eikite į **Moduliai > Mažmena ir komercija > Kanalai > Produktai ir kategorijos > Išleisti produktai pagal kategoriją**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-124">In the **Navigation pane**, go to **Modules > Retail and commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="b10d6-125">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b10d6-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="b10d6-126">Spustelėkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-126">Click **Edit**.</span></span>
20. <span data-ttu-id="b10d6-127">Išplėskite „fastTab“ **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="b10d6-128">Lauke **Kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b10d6-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="b10d6-129">Ši kaina naudojama, jei nerasta jokių taikomų prekybos sutarčių.</span><span class="sxs-lookup"><span data-stu-id="b10d6-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="b10d6-130">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-130">Click **Save**.</span></span>
23. <span data-ttu-id="b10d6-131">**Veiksmų srityje** spustelėkite **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="b10d6-132">Spustelėkite **Kurti prekybos sutartis**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="b10d6-133">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-133">Click **New**.</span></span>
26. <span data-ttu-id="b10d6-134">Lauke **Pavadinimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b10d6-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="b10d6-135">Sąraše pasirinkite **Mažmeninė prekyba**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-135">In the list, select **Retail**.</span></span> <span data-ttu-id="b10d6-136">Demonstraciniuose duomenyse žurnalo pavadinimo **Mažmeninė prekyba** numatytasis ryšys yra **Prekė (pardavimas)**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-136">In the demo data, the **Retail** journal name has the default relation of **Price (sales)**.</span></span> <span data-ttu-id="b10d6-137">Tai reiškia, kad visos naujos sukurtos eilutės bus taikomos pardavimo kainos prekybos sutartims kaip numatytosios.</span><span class="sxs-lookup"><span data-stu-id="b10d6-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="b10d6-138">**Veiksmų srityje** spustelėkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="b10d6-139">Lauke **Kliento kodas** pažymėkite Grupė.</span><span class="sxs-lookup"><span data-stu-id="b10d6-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="b10d6-140">Lauke **Sąskaitos pasirinkimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="b10d6-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="b10d6-141">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="b10d6-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="b10d6-142">Tokiu būdu bus baigtas kanalo susiejimas su kainų grupe arba prekybos sutartimi.</span><span class="sxs-lookup"><span data-stu-id="b10d6-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="b10d6-143">Lauke **Elemento ryšiai** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="b10d6-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="b10d6-144">Lauke **Sumos valiuta** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="b10d6-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="b10d6-145">„fastTab“ **Išsami informacija** pažymėkite arba atžymėkite žymės langelį **Surasti kitą**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="b10d6-146">Kai **Surasti kitą** nustatytas kaip Taip, kainodaros modulis toliau ieškos taikytinų prekybos sutarčių su mažesne pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="b10d6-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="b10d6-147">Kai **Surasti kitą** nustatytas kaip Ne, kainodaros modulis nebeieško ir naudoja prekybos sutartį.</span><span class="sxs-lookup"><span data-stu-id="b10d6-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="b10d6-148">Spustelėkite **Registruoti.**</span><span class="sxs-lookup"><span data-stu-id="b10d6-148">Click **Post**.</span></span>
36. <span data-ttu-id="b10d6-149">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-149">Click **OK**.</span></span>
37. <span data-ttu-id="b10d6-150">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b10d6-150">Close the page.</span></span>
38. <span data-ttu-id="b10d6-151">**Veiksmų sritis** spustelėkite Parduoti.</span><span class="sxs-lookup"><span data-stu-id="b10d6-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="b10d6-152">Spustelėkite **Pardavimo kaina**.</span><span class="sxs-lookup"><span data-stu-id="b10d6-152">Click **Sales price**.</span></span>

