---
title: Sandėlio nustatymas
description: Šioje temoje aprašoma, kaip nustatyti sandėlį, kurį reikia naudoti su nauju „Microsoft Dynamics 365 Commerce“ kanalu.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800500"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="99470-103">Sandėlio nustatymas</span><span class="sxs-lookup"><span data-stu-id="99470-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99470-104">Šioje temoje aprašoma, kaip nustatyti sandėlį, kurį reikia naudoti su nauju „Microsoft Dynamics 365 Commerce“ kanalu.</span><span class="sxs-lookup"><span data-stu-id="99470-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="99470-105">Kiekvieną „Commerce“ kanalą reikia susieti su sukonfigūruotu sandėliu.</span><span class="sxs-lookup"><span data-stu-id="99470-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="99470-106">Toliau pateiktos procedūros yra minimalios konfigūracijos, kurias reikia atlikti norint nustatyti „Commerce“ kanalo sandėlį.</span><span class="sxs-lookup"><span data-stu-id="99470-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="99470-107">Daugiau informacijos apie sandėlio nustatymą žr. [Sandėlio valdymo peržiūra](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="99470-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="99470-108">Sandėlis vietos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="99470-108">Configure a warehouse site</span></span>

<span data-ttu-id="99470-109">Prieš nustatydami sandėlį, turite sukonfigūruoti sandėlio vietą.</span><span class="sxs-lookup"><span data-stu-id="99470-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="99470-110">Norėdami sukonfigūruoti sandėlio vietą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="99470-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="99470-111">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Vietos**.</span><span class="sxs-lookup"><span data-stu-id="99470-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="99470-112">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="99470-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="99470-113">Lauke **Vieta** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="99470-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="99470-114">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="99470-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="99470-115">Skyriuje **Bendra** nustatykite reikiamą **Laiko juosta**.</span><span class="sxs-lookup"><span data-stu-id="99470-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="99470-116">Skyriuje **Adresai** įveskite adresą.</span><span class="sxs-lookup"><span data-stu-id="99470-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="99470-117">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="99470-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="99470-118">Toliau pateiktame vaizde parodytas sandėlio vietos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="99470-118">The following image shows an example warehouse site.</span></span>

![Sandėlio vietos pavyzdys](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="99470-120">Sandėlio nustatymas</span><span class="sxs-lookup"><span data-stu-id="99470-120">Set up a warehouse</span></span>

<span data-ttu-id="99470-121">Norėdami nustatyti sandėlį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="99470-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="99470-122">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="99470-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="99470-123">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="99470-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="99470-124">Lauke **Sandėlis** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="99470-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="99470-125">Jei tai yra 1:1 parduotuvės susiejimas, apsvarstykite parduotuvės pavadinimo arba regiono platintojo centro pavadinimo naudojimą.</span><span class="sxs-lookup"><span data-stu-id="99470-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="99470-126">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="99470-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="99470-127">Išplečiamajame sąraše **Vieta** pasirinkite anksčiau sukurtą sandėlio vietą.</span><span class="sxs-lookup"><span data-stu-id="99470-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="99470-128">Lauke **Tipas** pasirinkite **Numatytasis**.</span><span class="sxs-lookup"><span data-stu-id="99470-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="99470-129">Jei norite nustatyti **Sulaikymo sandėlis**, pirmiausia turite atlikti šiuos veiksmus, kad sukurtumėte papildomą sandėlį, kur **Tipas** nustatytas kaip **Sulaikymas**.</span><span class="sxs-lookup"><span data-stu-id="99470-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="99470-130">Jei norite nustatyti **Tranzito sandėlis**, pirmiausia turite atlikti šiuos veiksmus, kad sukurtumėte papildomą sandėlį, kur **Tipas** nustatytas kaip **Tranzitas**.</span><span class="sxs-lookup"><span data-stu-id="99470-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="99470-131">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="99470-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="99470-132">Nustatyti atsargų perėjimus</span><span class="sxs-lookup"><span data-stu-id="99470-132">Set up inventory aisles</span></span>

<span data-ttu-id="99470-133">Norėdami nustatyti atsargų perėjimus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="99470-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="99470-134">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Vietos sąranka \> Atsargų perėjimas**.</span><span class="sxs-lookup"><span data-stu-id="99470-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="99470-135">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="99470-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="99470-136">Išplečiamajame sąraše **Sandėlis** pasirinkite anksčiau sukurtą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="99470-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="99470-137">Lauke **Perėjimas** įveskite pavadinimą (pavyzdžiui, „Def“).</span><span class="sxs-lookup"><span data-stu-id="99470-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="99470-138">Lauke **Pavadinimas** įveskite pavadinimą (pavyzdžiui, „Numatytasis perėjimas“).</span><span class="sxs-lookup"><span data-stu-id="99470-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="99470-139">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="99470-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="99470-140">Sandėlio atsargų vietų nustatymas</span><span class="sxs-lookup"><span data-stu-id="99470-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="99470-141">Norėdami nustatyti standartinių, pažeistų ar grąžintų sandėlio atsargų vietas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="99470-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="99470-142">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="99470-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="99470-143">Pasirinkite sandėlį, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="99470-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="99470-144">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="99470-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="99470-145">Veiksmų srityje pasirinkite **Sandėlis**, tada pasirinkite **Atsargų vieta**.</span><span class="sxs-lookup"><span data-stu-id="99470-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="99470-146">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="99470-146">On the action pane, select **New**.</span></span> <span data-ttu-id="99470-147">Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.</span><span class="sxs-lookup"><span data-stu-id="99470-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="99470-148">Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="99470-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="99470-149">Nustatykite **Rankinis naujinimas** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99470-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="99470-150">Lauke **Vieta** įveskite sandėlio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="99470-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="99470-151">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="99470-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="99470-152">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="99470-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="99470-153">Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.</span><span class="sxs-lookup"><span data-stu-id="99470-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="99470-154">Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="99470-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="99470-155">Nustatykite **Rankinis naujinimas** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99470-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="99470-156">Lauke **Vieta** įveskite „Sugadintos“.</span><span class="sxs-lookup"><span data-stu-id="99470-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="99470-157">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="99470-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="99470-158">Veiksmų srityje pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="99470-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="99470-159">Išplečiamajame sąraše **Sandėlis** kaip numatytasis turi būti rodomas naujas sandėlis.</span><span class="sxs-lookup"><span data-stu-id="99470-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="99470-160">Lauke **perėjimas** įveskite anksčiau nurodyto perėjimo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="99470-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="99470-161">Nustatykite **Rankinis naujinimas** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99470-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="99470-162">Lauke **Vieta** įveskite „Grąžintos“.</span><span class="sxs-lookup"><span data-stu-id="99470-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="99470-163">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="99470-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="99470-164">Toliau pateiktame paveiksle parodytas San Francisko sandėlio atsargų vietos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="99470-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Atsargų vietos nustatymo pavyzdys](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="99470-166">Sandėlio sąrankos užbaigimas</span><span class="sxs-lookup"><span data-stu-id="99470-166">Complete warehouse setup</span></span>

<span data-ttu-id="99470-167">Norėdami užbaigti sandėlio sąranką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="99470-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="99470-168">Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="99470-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="99470-169">Pasirinkite sandėlį, kurį sukūrėte anksčiau.</span><span class="sxs-lookup"><span data-stu-id="99470-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="99470-170">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="99470-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="99470-171">Dalyje **Atsargų ir sandėlio valdymas**:</span><span class="sxs-lookup"><span data-stu-id="99470-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="99470-172">Nustatykite **Numatytoji gavimo vieta** į anksčiau sukurtą numatytąją vietą.</span><span class="sxs-lookup"><span data-stu-id="99470-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="99470-173">Pasirinkite **Numatytoji išdavimo vieta** į anksčiau sukurtą numatytąją vietą.</span><span class="sxs-lookup"><span data-stu-id="99470-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="99470-174">Skyriuje **Adresai** įveskite sandėlio adresą.</span><span class="sxs-lookup"><span data-stu-id="99470-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="99470-175">Skyriuje **Mažmeninė prekyba**:</span><span class="sxs-lookup"><span data-stu-id="99470-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="99470-176">Lauke **Numatytoji grąžinimo vieta** įveskite anksčiau sukurtą grąžinimo vietą.</span><span class="sxs-lookup"><span data-stu-id="99470-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="99470-177">Nustatykite **Saugoti** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99470-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="99470-178">Nustatykite **Svoris** į **1,00**.</span><span class="sxs-lookup"><span data-stu-id="99470-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="99470-179">Lauke **Saugojimo matmenys** įveskite anksčiau sukurtą numatytąją vietą.</span><span class="sxs-lookup"><span data-stu-id="99470-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="99470-180">Skyriuje **Sandėlis** nustatykite **Faktinės neigiamos atsargos** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="99470-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="99470-181">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="99470-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="99470-182">Toliau pateiktame vaizde rodoma išsami informacija apie sukonfigūruotą sandėlį.</span><span class="sxs-lookup"><span data-stu-id="99470-182">The following image shows details for a configured warehouse.</span></span>

![Sukonfigūruoto sandėlio pavyzdys](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="99470-184">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="99470-184">Additional resources</span></span>

[<span data-ttu-id="99470-185">Sandėlio valdymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="99470-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="99470-186">Kanalų apžvalga</span><span class="sxs-lookup"><span data-stu-id="99470-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="99470-187">Būtinosios kanalo nustatymo sąlygos</span><span class="sxs-lookup"><span data-stu-id="99470-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="99470-188">Mažmeninės prekybos kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="99470-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="99470-189">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="99470-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="99470-190">Skambučių centro kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="99470-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
