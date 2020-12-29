---
title: Atsargų parametrų taikymas
description: Šioje temoje aptariami atsargų parametrai ir aprašoma, kaip juos taikyti programoje „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfa8b2bdc03e3698feda26932db757421097140d
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517069"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="f6ad1-103">Atsargų parametrų taikymas</span><span class="sxs-lookup"><span data-stu-id="f6ad1-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f6ad1-104">Šioje temoje aptariami atsargų parametrai ir aprašoma, kaip juos taikyti programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f6ad1-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="f6ad1-105">Overview</span></span>

<span data-ttu-id="f6ad1-106">Atsargų parametrai nurodo, ar atsargos turi būti patikrintos prieš įtraukiant produktus į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-106">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="f6ad1-107">Jie taip pat apibrėžia su atsargomis susijusius prekybos pranešimus, pvz., „Sandėlyje“ ir „Liko vos keli“.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-107">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="f6ad1-108">Šie parametrai užtikrina, kad produkto nepavyktų įsigyti, jei jo atsargos pasibaigė.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-108">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="f6ad1-109">„Dynamics 365 Commerce“ pateikiamas turimų produktų atsargų kiekis.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-109">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="f6ad1-110">Norėdami gauti daugiau informacijos apie tai, kaip apskaičiuojamas turimų atsargų pasiekiamumas, žr [Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="f6ad1-110">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="f6ad1-111">Svetainės kūrimo priemonėje „Commerce“ galima nustatyti produkto ar kategorijos atsargų ribines vertes ir diapazonus.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-111">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="f6ad1-112">Jos nustato, ar atsargos gali būti klasifikuojamos kaip „yra atsargų“, „mažai atsargų“ arba „nebėra atsargų“.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-112">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="f6ad1-113">Jei reikia išsamios informacijos, žr. [Atsargų buferių ir atsargų lygių konfigūravimas](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f6ad1-113">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f6ad1-114">Atsargų ribų ir diapazonų palaikymas yra prieinamas „Dynamics 365 Commerce“ 10.0.12 leidime.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-114">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="f6ad1-115">Atsargų parametrai</span><span class="sxs-lookup"><span data-stu-id="f6ad1-115">Inventory settings</span></span>

<span data-ttu-id="f6ad1-116">Programoje „Commerce“ atsargų parametrai apibrėžiami **Svetainės parametrai \> Plėtiniai \> Atsargų valdymas** svetainės kūrimo priemonėje.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-116">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="f6ad1-117">Yra keturi atsargų parametrai, iš kurių vienas yra pasenęs (nerekomenduojamas):</span><span class="sxs-lookup"><span data-stu-id="f6ad1-117">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="f6ad1-118">**Įjungti atsargų tikrinimą programoje** – Šis nustatymas įjungia gaminio inventoriaus patikrinimą.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-118">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="f6ad1-119">Tada pirkimo langelio, krepšelio ir atsiėmimo parduotuvėje moduliai patikrina produkto atsargas ir leidžia įtraukti produktą į krepšelį, tik jei yra atsargų.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-119">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="f6ad1-120">**Atsargų lygio pagrindas** – šis parametras nurodo, kaip apskaičiuojamas atsargų lygis.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-120">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="f6ad1-121">Galimos reikšmės: **Iš viso pasiekiama**, **Fiziškai pasiekiama** ir **Pasibaigusių atsargų slenkstis**.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-121">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="f6ad1-122">Programoje „Commerce“ galima nustatyti kiekvieno produkto ir kategorijos atsargų ribinę vertę ir diapazonus.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-122">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="f6ad1-123">Atsargų API pateikia produkto atsargų informaciją, skirtą ypatybėms **Iš viso pasiekiama** ir **Fiziškai pasiekiama**.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-123">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="f6ad1-124">Mažmenininkas sprendžia, ar **Iš viso pasiekiama** arba **Fiziškai pasiekiama** reikšmės turėtų būti naudojamos atsargų kiekiui ir atitinkamiems diapazonams esančių ir nesančių atsargų būsenai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-124">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="f6ad1-125">Parametro **Atsargų lygio pagrindas** reikšmė **Pasibaigusių atsargų slenkstis** yra pasenusi (senstelėjusi), nebenaudojama reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-125">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="f6ad1-126">Ją pasirinkus, atsargų skaičius nustatomas pagal reikšmės **Iš viso pasiekiama** rezultatus, bet slenkstį apibrėžia toliau aprašytas skaitinis parametras **Pasibaigusių atsargų slenkstis**.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-126">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="f6ad1-127">Šis slenksčio nustatymas taikomas visiems produktams visame e-komercijos saite.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-127">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="f6ad1-128">Jei atsargos mažesnės už ribinę vertę, laikoma, kad produkto atsargos pasibaigusios.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-128">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="f6ad1-129">Priešingu atveju laikoma, kad jo atsargų yra.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-129">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="f6ad1-130">Reikšmės **Pasibaigusių atsargų slenkstis** galimybės yra ribotos ir nerekomenduojame jų naudoti 10.0.12 ir naujesnėje versijoje.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-130">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="f6ad1-131">**Atsargų diapazonai** – šis parametras apibrėžia atsargų diapazonus, kurie bus rodomi dėl svetainės moduliuose.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-131">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="f6ad1-132">Jis taikomas tik tuo atveju, jei reikšmės **Iš viso pasiekiama** arba **Fiziškai pasiekiama** pasirinktos parametrui **Atsargų lygio pagrindas**.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-132">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="f6ad1-133">Galimos vertės yra **Visos**, **Mažai ir nebėra** ir **Nebėra**.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-133">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="f6ad1-134">Pasirinkus **Visos** bus rodomi pranešimai apie visus atsargų diapazonus nuo „yra atsargų“ (pranešimas „Yra“) iki „nebėra atsargų“ (pranešimas „nebėra atsargų“).</span><span class="sxs-lookup"><span data-stu-id="f6ad1-134">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="f6ad1-135">Pasirinkus **Mažai ir nebėra** bus rodomi pranešimai apie visus atsargų diapazonus, išskyrus „yra atsargų“ (pranešimas „Yra“).</span><span class="sxs-lookup"><span data-stu-id="f6ad1-135">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="f6ad1-136">Pasirinkus **Nėra atsargų**, bus rodomas tik pranešimas „Nėra atsargų“.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-136">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="f6ad1-137">**Pasibaigusių atsargų slenkstis** – Šis senas skaitinis parametras įsigalios tik tada, jei reikšmė **Pasibaigusių atsargų slenkstis** pasirenkama parametrui **Atsargų lygio pagrindas**.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-137">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="f6ad1-138">Šie parametrai galimi „Dynamics 365 Commerce” 10.0.12 leidime.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-138">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="f6ad1-139">Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-139">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="f6ad1-140">Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="f6ad1-140">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="f6ad1-141">Moduliai, kurie naudoja atsargų parametrus</span><span class="sxs-lookup"><span data-stu-id="f6ad1-141">Modules that use inventory settings</span></span>

<span data-ttu-id="f6ad1-142">Pirkimo langelis, pageidavimų sąrašas, parduotuvės parinkiklis, krepšelis ir krepšelio piktogramos moduliai naudoja atsargų parametrus, kad būtų rodomi atsargų diapazonai ir pranešimai.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-142">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="f6ad1-143">Toliau pateiktame paveikslėlyje parodytas produkto informacijos puslapis (PDP), kuriame pateikiamas pranešimas, kad atsargų yra („Yra“).</span><span class="sxs-lookup"><span data-stu-id="f6ad1-143">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![PDP modulio su atsargų pranešimu, pavyzdys](./media/pdp-InStock.png)

<span data-ttu-id="f6ad1-145">Toliau pateiktame paveikslėlyje rodomas PDP puslapis, kuriame pateikiamas pranešimas „Nėra atsargų“.</span><span class="sxs-lookup"><span data-stu-id="f6ad1-145">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![PDP modulio su pasibaigusių atsargų pranešimu, pavyzdys](./media/pdp-outofstock.png)

<span data-ttu-id="f6ad1-147">Toliau pateiktame paveikslėlyje rodomas krepšelis, kuriame pateikiamas pranešimas, kad atsargų yra („Yra“).</span><span class="sxs-lookup"><span data-stu-id="f6ad1-147">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Krepšelio modulio su atsargų pranešimu, pavyzdys](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="f6ad1-149">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f6ad1-149">Additional resources</span></span>

[<span data-ttu-id="f6ad1-150">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="f6ad1-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f6ad1-151">Atsargų buferių ir atsargų lygių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f6ad1-151">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="f6ad1-152">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="f6ad1-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f6ad1-153">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="f6ad1-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f6ad1-154">Sąskaitos valdymo puslapiai ir moduliai</span><span class="sxs-lookup"><span data-stu-id="f6ad1-154">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="f6ad1-155">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="f6ad1-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="f6ad1-156">SDK ir modulių bibliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="f6ad1-156">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
