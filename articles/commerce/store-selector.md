---
title: Parduotuvės parinkiklio modulis
description: Šioje temoje paaiškinamas parduotuvės parinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378213"
---
# <a name="store-selector-module"></a><span data-ttu-id="bf5c9-103">Parduotuvės parinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="bf5c9-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bf5c9-104">Šioje temoje paaiškinamas parduotuvės parinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bf5c9-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="bf5c9-105">Overview</span></span>

<span data-ttu-id="bf5c9-106">Parduotuvės parinkiklio modulis naudojamas „pirkti internetu, atsiimti parduotuvėje“ (angl. BOPIS) kliento scenarijui.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="bf5c9-107">Čia pateikiamas parduotuvių, kuriose galima atsiimti produktą, sąrašas, kiekvienos parduotuvės darbo valandos ir prekių atsargos.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="bf5c9-108">Parduotuvių parinkiklio moduliui reikalingas produkto konteksto ir paieškos vietos įgalinimas, kad jis galėtų rasti parduotuves.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="bf5c9-109">Jei paieškos vietos nėra, ji pagal numatytąsias nuostatas nustato kliento naršyklės vietą, jei klientas duoda tam sutikimą.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="bf5c9-110">Modulyje yra įvesties laukas, kurį naudodamas klientas gali įvesti vietą (pašto kodą, miestą, valstiją) ir ieškoti netoliese esančių parduotuvių.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="bf5c9-111">Parduotuvės parinkiklio modulis yra integruotas su „Bing“ žemėlapių geokodavimo programos programavimo sąsaja (API), kad vieta būtų konvertuojama į platumą ir ilgumą.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="bf5c9-112">Reikalingas „Bing“ žemėlapių programos programavimo sąsajos (API) raktas, kuris turi būti pridėtas prie puslapio „Bendrieji „Commerce“ parametrai“, esančio „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bf5c9-113">Parduotuvės parinkiklio modulis gali būti pridėtas prie pirkimo langelio modulio, esančio išsamios produkto informacijos puslapyje (PDP), kad būtų galima parodyti parduotuves, kuriose galima atsiimti produktą.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="bf5c9-114">Jį taip pat galima pridėti prie krepšelio modulio.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-114">It can also be added to a cart module.</span></span> <span data-ttu-id="bf5c9-115">Kai parduotuvių parinkiklio modulis pridedamas prie krepšelio modulio, rodomos kiekvieno krepšelio eilutės elemento atsiėmimo parinktys.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="bf5c9-116">Be to, su pasirinktiniu kodavimu šį modulį galima pridėti prie kitų puslapių ar modulių plėtiniais ir tinkinimais.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="bf5c9-117">Produktai turi būti sukonfigūruoti su „atsiims klientas“ pristatymo būdu, kad BOPIS scenarijus veiktų.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="bf5c9-118">Priešingu atveju modulis nebus rodomas atitinkamuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="bf5c9-119">Norėdami gauti daugiau informacijos apie tai, kaip sukonfigūruoti pristatymo būdą, žr. [Nustatyti pristatymo būdus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="bf5c9-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="bf5c9-120">Toliau pateiktame paveikslėlyje vaizduojamas išsamios produkto informacijos puslapyje (PDP) naudojamo parduotuvių parinkiklio modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Parduotuvės parinkiklio modulio pavyzdys](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="bf5c9-122">Parduotuvės parinkiklio modulio naudojimas „e-Commerce“</span><span class="sxs-lookup"><span data-stu-id="bf5c9-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="bf5c9-123">Parduotuvės parinkiklio modulis gali būti naudojamas išsamios informacijos apie gaminį puslapyje (PDP), kad būtų galima ieškoti netoliese esančių parduotuvių, kuriose galima atsiimti produktą.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="bf5c9-124">Parduotuvės parinkiklio modulis gali būti naudojamas krepšelio puslapyje, kad būtų galima ieškoti netoliese esančių parduotuvių, kuriose galima atsiimti krepšelyje esantį produktą.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="bf5c9-125">Parduotuvės parinkiklio modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="bf5c9-125">Store selector module properties</span></span>

| <span data-ttu-id="bf5c9-126">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="bf5c9-126">Property name</span></span>             | <span data-ttu-id="bf5c9-127">Vertė</span><span class="sxs-lookup"><span data-stu-id="bf5c9-127">Value</span></span>                 | <span data-ttu-id="bf5c9-128">aprašymas</span><span class="sxs-lookup"><span data-stu-id="bf5c9-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="bf5c9-129">Ieškos spindulys</span><span class="sxs-lookup"><span data-stu-id="bf5c9-129">Search radius</span></span> | <span data-ttu-id="bf5c9-130">Skaičius</span><span class="sxs-lookup"><span data-stu-id="bf5c9-130">Number</span></span> | <span data-ttu-id="bf5c9-131">Apibrėžia parduotuvių ieškos spindulį myliomis.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="bf5c9-132">Jeigu vertė nenurodyta, naudojamas numatytasis 50 mylių ieškos spindulys.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="bf5c9-133">Paslaugos teikimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="bf5c9-133">Terms of Service</span></span> | <span data-ttu-id="bf5c9-134">URL</span><span class="sxs-lookup"><span data-stu-id="bf5c9-134">URL</span></span>    |  <span data-ttu-id="bf5c9-135">Paslaugų teikimo sąlygų URL, kuris reikalingas „Bing“ žemėlapių paslaugai.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="bf5c9-136">Parduotuvės parinkiklio modulio pridėjimas prie puslapio</span><span class="sxs-lookup"><span data-stu-id="bf5c9-136">Add a store selector module to a page</span></span>

<span data-ttu-id="bf5c9-137">Parduotuvės parinkiklio moduliui reikalingas produkto kontekstas, todėl jį galima naudoti tik pirkimo langelio ir krepšelio moduliuose.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="bf5c9-138">Parduotuvės parinkiklio moduliai neveikia be šių modulių.</span><span class="sxs-lookup"><span data-stu-id="bf5c9-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="bf5c9-139">Norėdami gauti informacijos apie tai, kaip pridėti parduotuvės parinkiklio modulį prie pirkimo langelio modulio, žr. [Pirkimo langelio modulis](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="bf5c9-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="bf5c9-140">Norėdami gauti informacijos apie tai, kaip pridėti parduotuvės parinkiklio modulį prie krepšelio modulio, žr. [Krepšelio modulis](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="bf5c9-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bf5c9-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bf5c9-141">Additional resources</span></span>

[<span data-ttu-id="bf5c9-142">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="bf5c9-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bf5c9-143">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="bf5c9-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bf5c9-144">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="bf5c9-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bf5c9-145">Greitai susipažinkite su išsamios produkto informacijos puslapiu (PDP)</span><span class="sxs-lookup"><span data-stu-id="bf5c9-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="bf5c9-146">Greitai susipažinkite su „Krepšelis ir mokėjimas“</span><span class="sxs-lookup"><span data-stu-id="bf5c9-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="bf5c9-147">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="bf5c9-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="bf5c9-148">Jūsų organizacijos „Bing“ žemėlapių valdymas</span><span class="sxs-lookup"><span data-stu-id="bf5c9-148">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)
