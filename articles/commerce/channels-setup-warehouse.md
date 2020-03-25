---
title: Sandėlio nustatymas
description: Šioje temoje aprašoma, kaip nustatyti sandėlį, kurį reikia naudoti su nauju „Microsoft Dynamics 365 Commerce“ kanalu.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113764"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="ddc10-103">Sandėlio nustatymas</span><span class="sxs-lookup"><span data-stu-id="ddc10-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ddc10-104">Šioje temoje aprašoma, kaip nustatyti sandėlį, kurį reikia naudoti su nauju „Microsoft Dynamics 365 Commerce“ kanalu.</span><span class="sxs-lookup"><span data-stu-id="ddc10-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ddc10-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="ddc10-105">Overview</span></span>

<span data-ttu-id="ddc10-106">Kiekvieną „Commerce“ kanalą reikia susieti su sukonfigūruotu sandėliu.</span><span class="sxs-lookup"><span data-stu-id="ddc10-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="ddc10-107">Toliau pateiktos procedūros yra minimalios konfigūracijos, kurias reikia atlikti norint nustatyti „Commerce“ kanalo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="ddc10-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="ddc10-108">Daugiau informacijos apie sandėlio nustatymą žr. [Sandėlio valdymo peržiūra](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ddc10-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="ddc10-109">Sandėlis vietos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ddc10-109">Configure a warehouse site</span></span>

<span data-ttu-id="ddc10-110">Prieš nustatydami sandėlį, turite sukonfigūruoti sandėlio vietą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="ddc10-111">Norėdami sukonfigūruoti sandėlio vietą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ddc10-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="ddc10-112">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Vietos**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="ddc10-113">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ddc10-114">Lauke **Vieta** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ddc10-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="ddc10-115">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ddc10-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="ddc10-116">Skyriuje **Bendra** nustatykite reikiamą **Laiko juosta**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="ddc10-117">Skyriuje **Adresai** įveskite adresą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="ddc10-118">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ddc10-119">Toliau pateiktame vaizde parodytas sandėlio vietos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="ddc10-119">The following image shows an example warehouse site.</span></span>

![Sandėlio vietos pavyzdys](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="ddc10-121">Sandėlio nustatymas</span><span class="sxs-lookup"><span data-stu-id="ddc10-121">Set up a warehouse</span></span>

<span data-ttu-id="ddc10-122">Norėdami nustatyti sandėlį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ddc10-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="ddc10-123">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="ddc10-124">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ddc10-125">Lauke **Sandėlis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ddc10-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="ddc10-126">Jei tai yra 1:1 parduotuvės susiejimas, apsvarstykite parduotuvės pavadinimo arba regiono platintojo centro pavadinimo naudojimą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="ddc10-127">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ddc10-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="ddc10-128">Išplečiamajame sąraše **Vieta** pasirinkite anksčiau sukurtą sandėlio vietą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="ddc10-129">Lauke **Tipas** pasirinkite **Numatytasis**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="ddc10-130">Jei norite nustatyti **Sulaikymo sandėlis**, pirmiausia turite atlikti šiuos veiksmus, kad sukurtumėte papildomą sandėlį, kur **Tipas** nustatytas kaip **Sulaikymas**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="ddc10-131">Jei norite nustatyti **Tranzito sandėlis**, pirmiausia turite atlikti šiuos veiksmus, kad sukurtumėte papildomą sandėlį, kur **Tipas** nustatytas kaip **Tranzitas**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="ddc10-132">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="ddc10-133">Nustatyti atsargų perėjimus</span><span class="sxs-lookup"><span data-stu-id="ddc10-133">Set up inventory aisles</span></span>

<span data-ttu-id="ddc10-134">Norėdami nustatyti atsargų perėjimus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ddc10-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="ddc10-135">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Vietos sąranka \> Atsargų perėjimas**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="ddc10-136">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ddc10-137">Išplečiamajame sąraše **Sandėlis** pasirinkite anksčiau sukurtą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="ddc10-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="ddc10-138">Lauke **Perėjimas** įveskite pavadinimą (pavyzdžiui, „Def“).</span><span class="sxs-lookup"><span data-stu-id="ddc10-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="ddc10-139">Lauke **Pavadinimas** įveskite pavadinimą (pavyzdžiui, „Numatytasis perėjimas“).</span><span class="sxs-lookup"><span data-stu-id="ddc10-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="ddc10-140">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="ddc10-141">Sandėlio atsargų vietų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ddc10-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="ddc10-142">Norėdami nustatyti standartinių, pažeistų ar grąžintų sandėlio atsargų vietas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ddc10-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="ddc10-143">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="ddc10-144">Pasirinkite sandėlį, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="ddc10-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="ddc10-145">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="ddc10-146">Veiksmų srityje pasirinkite **Sandėlis**, tada pasirinkite **Atsargų vieta**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="ddc10-147">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-147">On the action pane, select **New**.</span></span> <span data-ttu-id="ddc10-148">Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.</span><span class="sxs-lookup"><span data-stu-id="ddc10-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="ddc10-149">Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="ddc10-150">Nustatykite **Rankinis naujinimas** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="ddc10-151">Lauke **Vieta** įveskite sandėlio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="ddc10-152">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="ddc10-153">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="ddc10-154">Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.</span><span class="sxs-lookup"><span data-stu-id="ddc10-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="ddc10-155">Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="ddc10-156">Nustatykite **Rankinis naujinimas** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="ddc10-157">Lauke **Vieta** įveskite „Sugadintos“.</span><span class="sxs-lookup"><span data-stu-id="ddc10-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="ddc10-158">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="ddc10-159">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="ddc10-160">Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.</span><span class="sxs-lookup"><span data-stu-id="ddc10-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="ddc10-161">Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="ddc10-162">Nustatykite **Rankinis naujinimas** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="ddc10-163">Lauke **Vieta** įveskite „Grąžintos“.</span><span class="sxs-lookup"><span data-stu-id="ddc10-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="ddc10-164">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="ddc10-165">Toliau pateiktame paveiksle parodytas San Francisko sandėlio atsargų vietos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="ddc10-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Atsargų vietos nustatymo pavyzdys](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="ddc10-167">Sandėlio sąrankos užbaigimas</span><span class="sxs-lookup"><span data-stu-id="ddc10-167">Complete warehouse setup</span></span>

<span data-ttu-id="ddc10-168">Norėdami užbaigti sandėlio sąranką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ddc10-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="ddc10-169">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="ddc10-170">Pasirinkite sandėlį, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="ddc10-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="ddc10-171">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="ddc10-172">Dalyje **Atsargų ir sandėlio valdymas**:</span><span class="sxs-lookup"><span data-stu-id="ddc10-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="ddc10-173">Nustatykite **Numatytoji gavimo vieta** į anksčiau sukurtą numatytąją vietą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="ddc10-174">Pasirinkite **Numatytoji išdavimo vieta** į anksčiau sukurtą numatytąją vietą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="ddc10-175">Skyriuje **Adresai** įveskite sandėlio adresą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="ddc10-176">Skyriuje **Mažmeninė prekyba**:</span><span class="sxs-lookup"><span data-stu-id="ddc10-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="ddc10-177">Lauke **Numatytoji grąžinimo vieta** įveskite anksčiau sukurtą grąžinimo vietą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="ddc10-178">Nustatykite **Saugoti** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="ddc10-179">Nustatykite **Svoris** į **1,00**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="ddc10-180">Lauke **Saugojimo matmenys** įveskite anksčiau sukurtą numatytąją vietą.</span><span class="sxs-lookup"><span data-stu-id="ddc10-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="ddc10-181">Skyriuje **Sandėlis** nustatykite **Faktinės neigiamos atsargos** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="ddc10-182">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ddc10-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ddc10-183">Toliau pateiktame vaizde rodoma išsami informacija apie sukonfigūruotą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="ddc10-183">The following image shows details for a configured warehouse.</span></span>

![Sukonfigūruoto sandėlio pavyzdys](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="ddc10-185">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ddc10-185">Additional resources</span></span>

[<span data-ttu-id="ddc10-186">Sandėlio valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="ddc10-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="ddc10-187">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ddc10-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ddc10-188">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="ddc10-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ddc10-189">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ddc10-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="ddc10-190">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ddc10-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="ddc10-191">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ddc10-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





