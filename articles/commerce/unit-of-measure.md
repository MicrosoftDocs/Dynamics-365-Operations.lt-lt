---
title: Taikyti matavimo vieneto parametrus
description: Šioje temoje aptariami atsargų matavimo vienetų nustatymai ir aprašoma, kaip juos taikyti programoje „Microsoft Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022379"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="ddf9d-103">Taikyti matavimo vieneto parametrus</span><span class="sxs-lookup"><span data-stu-id="ddf9d-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="ddf9d-104">Šioje temoje aptariami atsargų matavimo vienetų nustatymai ir aprašoma, kaip juos taikyti programoje „Microsoft Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ddf9d-105">Produktą galima parduoti skirtingais vienetais, pvz., „kiekviena," „pora" ir „tuzinas".</span><span class="sxs-lookup"><span data-stu-id="ddf9d-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="ddf9d-106">„Commerce Headquarters" galima nurodyti produkto pardavimo matavimo vienetą, kuris rodomas el. komercijos svetainėje.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="ddf9d-107">Pavyzdžiui, jei mažmenininkas parduoda produktą ir individualiai, ir tuzinais, turimi matavimo vienetai gali būti rodomi kartu su kita informacija apie produktą.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="ddf9d-108">Toliau pateiktame pavyzdyje parodytas produkto pardavimo vienetas pagal matavimo **vienetą** „Commerce Headquarters" konfigūruotas.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Produkto, sukonfigūruotas naudojant matavimo vienetą „Commerce Headquarters", pavyzdys](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="ddf9d-110">Galima naudoti „Commerce" 10.0.19 versijos leidimą, siekiant pritaikyti ir rodyti matavimo vienetą.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="ddf9d-111">Matavimo vieneto parametrai</span><span class="sxs-lookup"><span data-stu-id="ddf9d-111">Unit of measure settings</span></span>

<span data-ttu-id="ddf9d-112">Matavimo vieneto ekrano parametrai apibrėžti „Commerce Site Builder", prie **svetainės \> parametrų \> plėtinių produktų rodymo matavimo vienetas**.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="ddf9d-113">Yra trys palaikomi parametrai:</span><span class="sxs-lookup"><span data-stu-id="ddf9d-113">There are three supported settings:</span></span>

- <span data-ttu-id="ddf9d-114">**Nerodyti** – kai šis parametras pasirinktas, el. komercijos svetainėje nebus rodomas produkto matavimo vienetas.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="ddf9d-115">Tai numatytasis elgesys.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="ddf9d-116">**Rodyti produkto pirkimo patirties puslapyje – pasirinkus šį parametrą, matavimo vienetas rodomas produkto duomenyse, krepšelyje, išregistravimo, užsakymo retrospektyvos ir užsakymo** informacijos puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="ddf9d-117">**Rodyti produktų naršymo ir pirkimo patirtį – pasirinkus šį parametrą, matavimo vienetas rodomas produktų pirkimo patirties puslapiuose ir produktų** naršymo patirties metu.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="ddf9d-118">Kaip šių veiksmų dalis rodoma ieškos rezultatų ir produktų rinkinio moduliuose.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ddf9d-119">Matavimo vienetų rodymo parametrai galimi pagal „Commerce" 10.0.19 versiją.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="ddf9d-120">Jei atnaujinate iš senesnės „Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="ddf9d-121">Dėl nurodymų, žr. [SDK ir modulio bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="ddf9d-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="ddf9d-122">Moduliai, naudojanti matavimo vieneto parametrus</span><span class="sxs-lookup"><span data-stu-id="ddf9d-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="ddf9d-123">Moduliuose, kuriuose naudojami matavimo vienetų parametrai, yra pirkimo dėžės, pageidavimų sąrašo, krepšelio, krepšelio piktogramos, ieškos rezultatų konteinerio, produktų rinkinio, tikrinimo ir užsakymo informacijos moduliai.</span><span class="sxs-lookup"><span data-stu-id="ddf9d-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="ddf9d-124">Toliau pateiktame pavyzdyje produkto informacijos puslapis (PDP) rodo produkto matavimo **vienetą** (lt).</span><span class="sxs-lookup"><span data-stu-id="ddf9d-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![PDP, kuriame rodomas matavimo vienetas, pavyzdys](./media/Productunit-PDP.png)

<span data-ttu-id="ddf9d-126">Toliau pateiktame pavyzdyje produkto surinkimo modulis rodo produkto matavimo **vienetą** (lt).</span><span class="sxs-lookup"><span data-stu-id="ddf9d-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Produkto surinkimo mudlis, kuriame rodomas matavimo vienetas, pavyzdys](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="ddf9d-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ddf9d-128">Additional resources</span></span>

[<span data-ttu-id="ddf9d-129">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="ddf9d-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ddf9d-130">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="ddf9d-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ddf9d-131">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="ddf9d-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ddf9d-132">Sąskaitos valdymo puslapiai ir moduliai</span><span class="sxs-lookup"><span data-stu-id="ddf9d-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="ddf9d-133">SDK ir modulių bibliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="ddf9d-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
