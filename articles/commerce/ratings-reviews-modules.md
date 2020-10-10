---
title: Įvertinimų ir apžvalgų moduliai
description: Šioje temoje aptariami įvertinimų ir apžvalgų moduliai, naudojami produkto informacijos puslapiuose programoje „Microsoft Dynamics 365 Commerce“.
author: gvrmohanreddy
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 85fb1272103eed7d6e44635b7c20438471d96b34
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817735"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="3caea-103">Įvertinimų ir apžvalgų moduliai</span><span class="sxs-lookup"><span data-stu-id="3caea-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3caea-104">Šioje temoje aptariami įvertinimų ir apžvalgų moduliai, naudojami produkto informacijos puslapiuose (PDP) programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="3caea-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3caea-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="3caea-105">Overview</span></span>

<span data-ttu-id="3caea-106">El. prekybos svetainėse nurodyti įverčiai ir apžvalgos klientams padeda sužinoti apie produktus prieš priimant pirkimo sprendimą, taip pat tai yra mechanizmas, skirtas klientų atsiliepimams apie produktus surinkti.</span><span class="sxs-lookup"><span data-stu-id="3caea-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="3caea-107">Įverčiai rodomi produktų sąrašų puslapiuose, kategorijų sąrašų puslapiuose, ieškos rezultatų puslapiuose ir kituose svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="3caea-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="3caea-108">Įverčių histogramos ir produktų apžvalgos rodomos produktų informacijos puslapiuose (PDP).</span><span class="sxs-lookup"><span data-stu-id="3caea-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="3caea-109">Klientai pateikti produkto įverčius ir apžvalgas gali naudodami mygtuką **Rašyti apžvalgą**.</span><span class="sxs-lookup"><span data-stu-id="3caea-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="3caea-110">Šios PDP funkcijos yra valdomos naudojant įverčių ir apžvalgų modulius.</span><span class="sxs-lookup"><span data-stu-id="3caea-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="3caea-111">Įverčių ir apžvalgų moduliai PIIP puslapiuose</span><span class="sxs-lookup"><span data-stu-id="3caea-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="3caea-112">PIIP puslapiuose įverčių ir apžvalgų suvestinę rodo tolesni trys moduliai.</span><span class="sxs-lookup"><span data-stu-id="3caea-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="3caea-113">Apžvalgų rašymo modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-113">Write review module</span></span>
- <span data-ttu-id="3caea-114">Produktų apžvalgų sąrašo modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-114">Product reviews list module</span></span>
- <span data-ttu-id="3caea-115">Įverčių histogramų modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-115">Ratings histogram module</span></span>
 
<span data-ttu-id="3caea-116">Toliau pateiktoje iliustracijoje rodoma, kaip PIIP puslapyje atrodo įverčių ir apžvalgų moduliai.</span><span class="sxs-lookup"><span data-stu-id="3caea-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Įverčių ir apžvalgų moduliai PIIP puslapyje](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="3caea-118">Norėdami gauti informacijos apie tai, kaip optimizuoti PIIP šablonus ir maketus, kad įverčių ir apžvalgų modulių konfigūracijas galėtumėte bendrai naudoti keliuose el. prekybos svetainės PIIP, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3caea-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="3caea-119">Tolesnėje iliustracijoje parodyta, kaip „Dynamics 365 Commerce“ dialogo lange **Modulio įtraukimas** pateikiami įverčių ir apžvalgų moduliai.</span><span class="sxs-lookup"><span data-stu-id="3caea-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="3caea-120">![Dialogo langas Modulio įtraukimas](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="3caea-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="3caea-121">Apžvalgų rašymo modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-121">Write review module</span></span>

<span data-ttu-id="3caea-122">Apžvalgų rašymo modulyje yra mygtukas **Rašyti apžvalgą**, kurį naudodami vartotojai gali prisijungti, priskirti įvertį ir parašyti produkto apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="3caea-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="3caea-123">Naudodami šį modulį vartotojai taip pat gali redaguoti įvertį arba peržiūrėti, ką pateikė anksčiau.</span><span class="sxs-lookup"><span data-stu-id="3caea-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="3caea-124">Šis modulis PIIP puslapyje paprastai rodomas virš įverčių histogramų ir produktų apžvalgų sąrašo modulių.</span><span class="sxs-lookup"><span data-stu-id="3caea-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="3caea-125">Tolesnėje iliustracijoje parodytas dialogo langas **Apžvalgos rašymas**, rodomas klientui pasirinkus **Rašyti apžvalgą**.</span><span class="sxs-lookup"><span data-stu-id="3caea-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="3caea-126">Šiame dialogo lange klientas gali pateikti įvertį ir apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="3caea-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="3caea-127">![Apžvalgų rašymo dialogo langas](media/rnr-eCommerce-write-review-module.png) Tolesnėje lentelėje parodyta apžvalgų rašymo modulio ypatybė, kurią reikia sukonfigūruoti kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="3caea-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="3caea-128">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3caea-128">Property name</span></span> | <span data-ttu-id="3caea-129">Vertė</span><span class="sxs-lookup"><span data-stu-id="3caea-129">Value</span></span>        | <span data-ttu-id="3caea-130">Ypatybės aprašas</span><span class="sxs-lookup"><span data-stu-id="3caea-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="3caea-131">Vardas ir pavardė</span><span class="sxs-lookup"><span data-stu-id="3caea-131">Name</span></span>          | <span data-ttu-id="3caea-132">Rašyti apžvalgą</span><span class="sxs-lookup"><span data-stu-id="3caea-132">Write review</span></span> | <span data-ttu-id="3caea-133">Apžvalgų rašymo modulio pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="3caea-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="3caea-134">Įverčių histogramų modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-134">Ratings histogram module</span></span>

<span data-ttu-id="3caea-135">Įverčių histogramų modulyje rodoma įverčių histograma.</span><span class="sxs-lookup"><span data-stu-id="3caea-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="3caea-136">Šis modulis PIIP puslapyje paprastai rodomas tarp apžvalgų rašymo modulio ir produktų apžvalgų sąrašo modulio.</span><span class="sxs-lookup"><span data-stu-id="3caea-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="3caea-137">Įverčių histogramų modulio konfigūruoti nereikia.</span><span class="sxs-lookup"><span data-stu-id="3caea-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="3caea-138">Tereikia modulį įtraukti į PIIP šabloną.</span><span class="sxs-lookup"><span data-stu-id="3caea-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="3caea-139">Tolesnėse iliustacijose parodyta, kaip programoje „Dynamics 365 Commerce“ atrodo PIIP šablonas, kai sukonfigūruota PIIP puslapiuose rodyti įverčių ir apžvalgų modulius.</span><span class="sxs-lookup"><span data-stu-id="3caea-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="3caea-140">![PIIP šablonas, kai sukonfigūruota PIIP puslapiuose rodyti įverčius ir apžvalgas](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="3caea-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="3caea-141">Produktų apžvalgų sąrašo modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-141">Product reviews list module</span></span>

<span data-ttu-id="3caea-142">Produktų apžvalgų sąrašo modulyje rodomas produktų apžvalgų sąrašas su rikiavimo, filtravimo ir skaidymo į puslapius parinktimis.</span><span class="sxs-lookup"><span data-stu-id="3caea-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="3caea-143">Šis modulis PIIP puslapyje paprastai rodomas už įverčių histogramų modulio.</span><span class="sxs-lookup"><span data-stu-id="3caea-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="3caea-144">Tolesnėje lentelėje parodytos produktų apžvalgų sąrašo modulio ypatybės, kurias reikia sukonfigūruoti kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="3caea-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="3caea-145">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3caea-145">Property name</span></span>              | <span data-ttu-id="3caea-146">Vertė</span><span class="sxs-lookup"><span data-stu-id="3caea-146">Value</span></span> | <span data-ttu-id="3caea-147">Ypatybės aprašas</span><span class="sxs-lookup"><span data-stu-id="3caea-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="3caea-148">Kiekviename puslapyje rodomos apžvalgos</span><span class="sxs-lookup"><span data-stu-id="3caea-148">Reviews shown on each page</span></span> | <span data-ttu-id="3caea-149">10</span><span class="sxs-lookup"><span data-stu-id="3caea-149">10</span></span>    | <span data-ttu-id="3caea-150">Apžvalgų skaičius, kuris vienu metu turi būti rodomas PIIP puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3caea-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="3caea-151">Pateikti mygtukai **Kitas** ir **Ankstesnis**, kad vartotojai galėtų pereiti per apžvalgų puslapius.</span><span class="sxs-lookup"><span data-stu-id="3caea-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="3caea-152">Įverčių histograma – suvestinės rodinys</span><span class="sxs-lookup"><span data-stu-id="3caea-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="3caea-153">Produktų apžvalgų sąrašo modulyje yra vieta, kurioje galite įtraukti įverčių histogramų modulį.</span><span class="sxs-lookup"><span data-stu-id="3caea-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="3caea-154">Toliau pateiktoje iliustracijoje parodyta, kaip programoje „Dynamics 365 Commerce“ į produktų apžvalgų sąrašo modulį galite įtraukti įverčių histogramų modulį.</span><span class="sxs-lookup"><span data-stu-id="3caea-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Įverčių histogramų modulio įtraukimas į produktų apžvalgų sąrašo modulį](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="3caea-156">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3caea-156">Additional resources</span></span>

[<span data-ttu-id="3caea-157">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="3caea-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3caea-158">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3caea-159">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3caea-160">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3caea-161">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3caea-162">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3caea-163">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="3caea-163">Footer module</span></span>](author-footer-module.md)
