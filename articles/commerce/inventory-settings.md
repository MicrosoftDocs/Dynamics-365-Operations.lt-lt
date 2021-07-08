---
title: Atsargų parametrų taikymas
description: Šioje temoje aptariami atsargų parametrai ir aprašoma, kaip juos taikyti programoje „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3da447c298993794afa49a0fbaddb1c21cf6231a
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271310"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="5b491-103">Atsargų parametrų taikymas</span><span class="sxs-lookup"><span data-stu-id="5b491-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5b491-104">Šioje temoje aptariami atsargų parametrai ir aprašoma, kaip juos taikyti programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="5b491-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5b491-105">Atsargų parametrai nurodo, ar atsargos turi būti patikrintos prieš įtraukiant produktus į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="5b491-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="5b491-106">Jie taip pat apibrėžia su atsargomis susijusius prekybos pranešimus, pvz., „Sandėlyje“ ir „Liko vos keli“.</span><span class="sxs-lookup"><span data-stu-id="5b491-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="5b491-107">Šie parametrai užtikrina, kad produkto nepavyktų įsigyti, jei jo atsargos pasibaigė.</span><span class="sxs-lookup"><span data-stu-id="5b491-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="5b491-108">„Dynamics 365 Commerce“ pateikiamas turimų produktų atsargų kiekis.</span><span class="sxs-lookup"><span data-stu-id="5b491-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="5b491-109">Norėdami gauti daugiau informacijos apie tai, kaip apskaičiuojamas turimų atsargų pasiekiamumas, žr. [Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="5b491-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="5b491-110">Svetainės kūrimo priemonėje „Commerce“ galima nustatyti produkto ar kategorijos atsargų ribines vertes ir diapazonus.</span><span class="sxs-lookup"><span data-stu-id="5b491-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="5b491-111">Jos nustato, ar atsargos gali būti klasifikuojamos kaip „yra atsargų“, „mažai atsargų“ arba „nebėra atsargų“.</span><span class="sxs-lookup"><span data-stu-id="5b491-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="5b491-112">Jei reikia išsamios informacijos, žr. [Atsargų buferių ir atsargų lygių konfigūravimas](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="5b491-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5b491-113">Atsargų ribų ir diapazonų palaikymas yra prieinamas „Dynamics 365 Commerce“ 10.0.12 leidime.</span><span class="sxs-lookup"><span data-stu-id="5b491-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="5b491-114">Atsargų parametrai</span><span class="sxs-lookup"><span data-stu-id="5b491-114">Inventory settings</span></span>

<span data-ttu-id="5b491-115">Programoje „Commerce“ atsargų parametrai apibrėžiami **Svetainės parametrai \> Plėtiniai \> Atsargų valdymas** svetainės kūrimo priemonėje.</span><span class="sxs-lookup"><span data-stu-id="5b491-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="5b491-116">Yra penki atsargų parametrai, iš kurių vienas yra pasenęs (nerekomenduojamas):</span><span class="sxs-lookup"><span data-stu-id="5b491-116">There are five inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="5b491-117">**Įjungti atsargų tikrinimą programoje** – Šis nustatymas įjungia gaminio inventoriaus patikrinimą.</span><span class="sxs-lookup"><span data-stu-id="5b491-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="5b491-118">Tada pirkimo langelio, krepšelio ir atsiėmimo parduotuvėje moduliai patikrina produkto atsargas ir leidžia įtraukti produktą į krepšelį, tik jei yra atsargų.</span><span class="sxs-lookup"><span data-stu-id="5b491-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="5b491-119">**Atsargų lygio pagrindas** – šis parametras nurodo, kaip apskaičiuojamas atsargų lygis.</span><span class="sxs-lookup"><span data-stu-id="5b491-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="5b491-120">Galimos reikšmės: **Iš viso pasiekiama**, **Fiziškai pasiekiama** ir **Pasibaigusių atsargų slenkstis**.</span><span class="sxs-lookup"><span data-stu-id="5b491-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="5b491-121">Programoje „Commerce“ galima nustatyti kiekvieno produkto ir kategorijos atsargų ribinę vertę ir diapazonus.</span><span class="sxs-lookup"><span data-stu-id="5b491-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="5b491-122">Atsargų API pateikia produkto atsargų informaciją, skirtą ypatybėms **Iš viso pasiekiama** ir **Fiziškai pasiekiama**.</span><span class="sxs-lookup"><span data-stu-id="5b491-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="5b491-123">Mažmenininkas sprendžia, ar **Iš viso pasiekiama** arba **Fiziškai pasiekiama** reikšmės turėtų būti naudojamos atsargų kiekiui ir atitinkamiems diapazonams esančių ir nesančių atsargų būsenai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="5b491-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="5b491-124">Parametro **Atsargų lygio pagrindas** reikšmė **Pasibaigusių atsargų slenkstis** yra pasenusi (senstelėjusi), nebenaudojama reikšmė.</span><span class="sxs-lookup"><span data-stu-id="5b491-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="5b491-125">Ją pasirinkus, atsargų skaičius nustatomas pagal reikšmės **Iš viso pasiekiama** rezultatus, bet slenkstį apibrėžia toliau aprašytas skaitinis parametras **Pasibaigusių atsargų slenkstis**.</span><span class="sxs-lookup"><span data-stu-id="5b491-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="5b491-126">Šis slenksčio nustatymas taikomas visiems produktams visame e-komercijos saite.</span><span class="sxs-lookup"><span data-stu-id="5b491-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="5b491-127">Jei atsargos mažesnės už ribinę vertę, laikoma, kad produkto atsargos pasibaigusios.</span><span class="sxs-lookup"><span data-stu-id="5b491-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="5b491-128">Priešingu atveju laikoma, kad jo atsargų yra.</span><span class="sxs-lookup"><span data-stu-id="5b491-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="5b491-129">Reikšmės **Pasibaigusių atsargų slenkstis** galimybės yra ribotos ir nerekomenduojame jų naudoti 10.0.12 ir naujesnėje versijoje.</span><span class="sxs-lookup"><span data-stu-id="5b491-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="5b491-130">**Kelių sandėlių atsargų lygis – šis parametras leidžia apskaičiuoti atsargų lygį pagal numatytąjį** sandėlį arba kelis sandėlius.</span><span class="sxs-lookup"><span data-stu-id="5b491-130">**Inventory level for multiple warehouses** – This setting enables the inventory level to be calculated against the default warehouse or multiple warehouses.</span></span> <span data-ttu-id="5b491-131">Pasirinktis **Pagal atskirą** sandėlį apskaičiuos atsargų lygius pagal numatytąjį sandėlį.</span><span class="sxs-lookup"><span data-stu-id="5b491-131">The **Based on individual warehouse** option will calculate inventory levels based on the default warehouse.</span></span> <span data-ttu-id="5b491-132">Arba el. komercijos svetainė gali nurodyti kelis sandėlius, kad būtų lengviau įvykdyti.</span><span class="sxs-lookup"><span data-stu-id="5b491-132">Alternatively, an e-commerce site can point to multiple warehouses to facilitate fulfillment.</span></span> <span data-ttu-id="5b491-133">Tokiu atveju **parinktis Pagal siuntimo ir paėmimo sandėlių suvestinę** naudojama nurodant atsargas.</span><span class="sxs-lookup"><span data-stu-id="5b491-133">In that case, the **Based on aggregate for Shipping and Pickup warehouses** option is used to indicate stock availability.</span></span> <span data-ttu-id="5b491-134">Pavyzdžiui, kai klientas perka prekę ir kaip pristatymo būdą pasirenka "siuntimas", prekę galima siųsti iš bet kurio įvykdymo grupės sandėlio, turimo atsargų.</span><span class="sxs-lookup"><span data-stu-id="5b491-134">For example, when a customer purchases an item and selects "shipping" as the delivery mode, the item can be shipped from any warehouse in the fulfillment group that has available inventory.</span></span> <span data-ttu-id="5b491-135">Produkto informacijos puslapyje (PDP) bus rodomas pranešimas "Atsargose", skirtas siuntai, jei įvykdymo grupėje yra siuntimo sandėlių atsargų.</span><span class="sxs-lookup"><span data-stu-id="5b491-135">The product details page (PDP) will show an "In stock" message for shipping if any available shipping warehouse in the fulfillment group has inventory.</span></span> 

> [!IMPORTANT] 
> <span data-ttu-id="5b491-136">Kelių **sandėlių parametrų atsargų lygis** pasiekiamas naudojant „Commerce" 10.0.19 versiją.</span><span class="sxs-lookup"><span data-stu-id="5b491-136">The **Inventory level for multiple warehouses** setting is available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="5b491-137">Jei atnaujinate iš senesnės „Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="5b491-137">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="5b491-138">Dėl nurodymų, žr. [SDK ir modulio bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="5b491-138">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

- <span data-ttu-id="5b491-139">**Atsargų diapazonai** – šis parametras apibrėžia atsargų diapazonus, kurie bus rodomi dėl svetainės moduliuose.</span><span class="sxs-lookup"><span data-stu-id="5b491-139">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="5b491-140">Jis taikomas tik tuo atveju, jei reikšmės **Iš viso pasiekiama** arba **Fiziškai pasiekiama** pasirinktos parametrui **Atsargų lygio pagrindas**.</span><span class="sxs-lookup"><span data-stu-id="5b491-140">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="5b491-141">Galimos vertės yra **Visos**, **Mažai ir nebėra** ir **Nebėra**.</span><span class="sxs-lookup"><span data-stu-id="5b491-141">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="5b491-142">Pasirinkus **Visos** bus rodomi pranešimai apie visus atsargų diapazonus nuo „yra atsargų“ (pranešimas „Yra“) iki „nebėra atsargų“ (pranešimas „nebėra atsargų“).</span><span class="sxs-lookup"><span data-stu-id="5b491-142">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="5b491-143">Pasirinkus **Mažai ir nebėra** bus rodomi pranešimai apie visus atsargų diapazonus, išskyrus „yra atsargų“ (pranešimas „Yra“).</span><span class="sxs-lookup"><span data-stu-id="5b491-143">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="5b491-144">Pasirinkus **Nėra atsargų**, bus rodomas tik pranešimas „Nėra atsargų“.</span><span class="sxs-lookup"><span data-stu-id="5b491-144">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="5b491-145">**Pasibaigusių atsargų slenkstis** – Šis senas skaitinis parametras įsigalios tik tada, jei reikšmė **Pasibaigusių atsargų slenkstis** pasirenkama parametrui **Atsargų lygio pagrindas**.</span><span class="sxs-lookup"><span data-stu-id="5b491-145">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="5b491-146">Šie parametrai galimi „Dynamics 365 Commerce” 10.0.12 leidime.</span><span class="sxs-lookup"><span data-stu-id="5b491-146">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="5b491-147">Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="5b491-147">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="5b491-148">Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="5b491-148">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="5b491-149">Moduliai, kurie naudoja atsargų parametrus</span><span class="sxs-lookup"><span data-stu-id="5b491-149">Modules that use inventory settings</span></span>

<span data-ttu-id="5b491-150">Pirkimo langelis, pageidavimų sąrašas, parduotuvės parinkiklis, krepšelis ir krepšelio piktogramos moduliai naudoja atsargų parametrus, kad būtų rodomi atsargų diapazonai ir pranešimai.</span><span class="sxs-lookup"><span data-stu-id="5b491-150">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="5b491-151">Šiame pavyzdyje PDP rodo atsargų („Turima") pranešimą.</span><span class="sxs-lookup"><span data-stu-id="5b491-151">In the example in the following illustration, a PDP is showing an in-stock ("Available") message.</span></span>

![PDP modulio su atsargų pranešimu, pavyzdys](./media/pdp-InStock.png)

<span data-ttu-id="5b491-153&quot;>Šiame pavyzdyje PDP rodo atsargų („Pasibaigė") pranešimą.</span><span class="sxs-lookup"><span data-stu-id="5b491-153">In the example in the following illustration, a PDP is showing an "Out of stock" message.</span></span>

![PDP modulio su pasibaigusių atsargų pranešimu, pavyzdys](./media/pdp-outofstock.png)

<span data-ttu-id="5b491-155&quot;>Šiame pavyzdyje vežimėlis rodo atsargų („Turima") pranešimą.</span><span class="sxs-lookup"><span data-stu-id="5b491-155">In the example in the following illustration, a cart is showing an in-stock ("Available") message.</span></span>

![Krepšelio modulio su atsargų pranešimu, pavyzdys](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="5b491-157">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5b491-157">Additional resources</span></span>

[<span data-ttu-id="5b491-158">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="5b491-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5b491-159">Atsargų buferių ir atsargų lygių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="5b491-159">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="5b491-160">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="5b491-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5b491-161">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="5b491-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5b491-162">Sąskaitos valdymo puslapiai ir moduliai</span><span class="sxs-lookup"><span data-stu-id="5b491-162">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="5b491-163">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="5b491-163">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="5b491-164">SDK ir modulių bibliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="5b491-164">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
