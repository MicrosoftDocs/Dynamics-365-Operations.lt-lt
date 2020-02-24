---
title: Įvertinimų ir atsiliepimų konfigūravimas
description: Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002202"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="ab875-103">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ab875-103">Configure ratings and reviews</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ab875-104">Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.</span><span class="sxs-lookup"><span data-stu-id="ab875-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ab875-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="ab875-105">Overview</span></span>

<span data-ttu-id="ab875-106">El. prekybos svetainėse nurodyti įverčiai ir apžvalgos klientams padeda sužinoti apie produktus prieš priimant pirkimo sprendimą, nes jiems parodo, ką apie tuos produktus mano kiti klientai.</span><span class="sxs-lookup"><span data-stu-id="ab875-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="ab875-107">El. prekybos svetainėse įverčiai ir apžvalgos taip pat yra mechanizmas klientų atsiliepimams apie produktus rinkti.</span><span class="sxs-lookup"><span data-stu-id="ab875-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="ab875-108">Įverčiai rodomi produktų sąrašų puslapiuose, kategorijų sąrašų puslapiuose, ieškos rezultatų puslapiuose ir kituose svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="ab875-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="ab875-109">Įverčių histogramos ir produktų apžvalgos rodomos produktų išsamios informacijos puslapiuose (PIIP).</span><span class="sxs-lookup"><span data-stu-id="ab875-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="ab875-110">Klientai pateikti produkto įverčius ir apžvalgas gali naudodami mygtuką **Rašyti apžvalgą**.</span><span class="sxs-lookup"><span data-stu-id="ab875-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="ab875-111">Įverčių ir apžvalgų moduliai PIIP puslapiuose</span><span class="sxs-lookup"><span data-stu-id="ab875-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="ab875-112">PIIP puslapiuose įverčių ir apžvalgų suvestinę rodo tolesni trys moduliai.</span><span class="sxs-lookup"><span data-stu-id="ab875-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="ab875-113">Apžvalgų rašymo modulis</span><span class="sxs-lookup"><span data-stu-id="ab875-113">Write review module</span></span>
- <span data-ttu-id="ab875-114">Produktų apžvalgų sąrašo modulis</span><span class="sxs-lookup"><span data-stu-id="ab875-114">Product reviews list module</span></span>
- <span data-ttu-id="ab875-115">Įverčių histogramų modulis</span><span class="sxs-lookup"><span data-stu-id="ab875-115">Ratings histogram module</span></span>
 
<span data-ttu-id="ab875-116">Toliau pateiktoje iliustracijoje rodoma, kaip PIIP puslapyje atrodo įverčių ir apžvalgų moduliai.</span><span class="sxs-lookup"><span data-stu-id="ab875-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Įverčių ir apžvalgų moduliai PIIP puslapyje](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="ab875-118">Norėdami gauti informacijos apie tai, kaip optimizuoti PIIP šablonus ir maketus, kad įverčių ir apžvalgų modulių konfigūracijas galėtumėte bendrai naudoti keliuose el. prekybos svetainės PIIP, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ab875-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="ab875-119">Tolesnėje iliustracijoje parodyta, kaip „Dynamics 365 Commerce“ dialogo lange **Modulio įtraukimas** pateikiami įverčių ir apžvalgų moduliai.</span><span class="sxs-lookup"><span data-stu-id="ab875-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Dialogo langas Modulio įtraukimas](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="ab875-121">Apžvalgų rašymo modulis</span><span class="sxs-lookup"><span data-stu-id="ab875-121">Write review module</span></span>

<span data-ttu-id="ab875-122">Apžvalgų rašymo modulyje yra mygtukas **Rašyti apžvalgą**, kurį naudodami vartotojai gali prisijungti, priskirti įvertį ir parašyti produkto apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="ab875-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="ab875-123">Naudodami šį modulį vartotojai taip pat gali redaguoti įvertį arba peržiūrėti, ką pateikė anksčiau.</span><span class="sxs-lookup"><span data-stu-id="ab875-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="ab875-124">Šis modulis PIIP puslapyje paprastai rodomas virš įverčių histogramų ir produktų apžvalgų sąrašo modulių.</span><span class="sxs-lookup"><span data-stu-id="ab875-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="ab875-125">Tolesnėje iliustracijoje parodytas dialogo langas **Apžvalgos rašymas**, rodomas klientui pasirinkus **Rašyti apžvalgą**.</span><span class="sxs-lookup"><span data-stu-id="ab875-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="ab875-126">Šiame dialogo lange klientas gali pateikti įvertį ir apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="ab875-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Dialogo langas Apžvalgos rašymas](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="ab875-128">Tolesnėje lentelėje parodyta apžvalgų rašymo modulio ypatybė, kurią reikia sukonfigūruoti kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="ab875-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="ab875-129">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ab875-129">Property name</span></span> | <span data-ttu-id="ab875-130">Vertė</span><span class="sxs-lookup"><span data-stu-id="ab875-130">Value</span></span>        | <span data-ttu-id="ab875-131">Ypatybės aprašas</span><span class="sxs-lookup"><span data-stu-id="ab875-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="ab875-132">Vardas ir pavardė</span><span class="sxs-lookup"><span data-stu-id="ab875-132">Name</span></span>          | <span data-ttu-id="ab875-133">Rašyti apžvalgą</span><span class="sxs-lookup"><span data-stu-id="ab875-133">Write review</span></span> | <span data-ttu-id="ab875-134">Apžvalgų rašymo modulio pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="ab875-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="ab875-135">Įverčių histogramų modulis</span><span class="sxs-lookup"><span data-stu-id="ab875-135">Ratings histogram module</span></span>

<span data-ttu-id="ab875-136">Įverčių histogramų modulyje rodoma įverčių histograma.</span><span class="sxs-lookup"><span data-stu-id="ab875-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="ab875-137">Šis modulis PIIP puslapyje paprastai rodomas tarp apžvalgų rašymo modulio ir produktų apžvalgų sąrašo modulio.</span><span class="sxs-lookup"><span data-stu-id="ab875-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="ab875-138">Įverčių histogramų modulio konfigūruoti nereikia.</span><span class="sxs-lookup"><span data-stu-id="ab875-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="ab875-139">Tereikia modulį įtraukti į PIIP šabloną.</span><span class="sxs-lookup"><span data-stu-id="ab875-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="ab875-140">Tolesnėse iliustacijose parodyta, kaip programoje „Dynamics 365 Commerce“ atrodo PIIP šablonas, kai sukonfigūruota PIIP puslapiuose rodyti įverčių ir apžvalgų modulius.</span><span class="sxs-lookup"><span data-stu-id="ab875-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PIIP šablonas, kai sukonfigūruota PIIP puslapiuose rodyti įverčius ir apžvalgas](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="ab875-142">Produktų apžvalgų sąrašo modulis</span><span class="sxs-lookup"><span data-stu-id="ab875-142">Product reviews list module</span></span>

<span data-ttu-id="ab875-143">Produktų apžvalgų sąrašo modulyje rodomas produktų apžvalgų sąrašas su rikiavimo, filtravimo ir skaidymo į puslapius parinktimis.</span><span class="sxs-lookup"><span data-stu-id="ab875-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="ab875-144">Šis modulis PIIP puslapyje paprastai rodomas už įverčių histogramų modulio.</span><span class="sxs-lookup"><span data-stu-id="ab875-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="ab875-145">Tolesnėje lentelėje parodytos produktų apžvalgų sąrašo modulio ypatybės, kurias reikia sukonfigūruoti kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="ab875-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="ab875-146">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ab875-146">Property name</span></span>              | <span data-ttu-id="ab875-147">Vertė</span><span class="sxs-lookup"><span data-stu-id="ab875-147">Value</span></span> | <span data-ttu-id="ab875-148">Ypatybės aprašas</span><span class="sxs-lookup"><span data-stu-id="ab875-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="ab875-149">Kiekviename puslapyje rodomos apžvalgos</span><span class="sxs-lookup"><span data-stu-id="ab875-149">Reviews shown on each page</span></span> | <span data-ttu-id="ab875-150">10</span><span class="sxs-lookup"><span data-stu-id="ab875-150">10</span></span>    | <span data-ttu-id="ab875-151">Apžvalgų skaičius, kuris vienu metu turi būti rodomas PIIP puslapyje.</span><span class="sxs-lookup"><span data-stu-id="ab875-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="ab875-152">Pateikti mygtukai **Kitas** ir **Ankstesnis**, kad vartotojai galėtų pereiti per apžvalgų puslapius.</span><span class="sxs-lookup"><span data-stu-id="ab875-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="ab875-153">Įverčių histograma – suvestinės rodinys</span><span class="sxs-lookup"><span data-stu-id="ab875-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="ab875-154">Produktų apžvalgų sąrašo modulyje yra vieta, kurioje galite įtraukti įverčių histogramų modulį.</span><span class="sxs-lookup"><span data-stu-id="ab875-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="ab875-155">Toliau pateiktoje iliustracijoje parodyta, kaip programoje „Dynamics 365 Commerce“ į produktų apžvalgų sąrašo modulį galite įtraukti įverčių histogramų modulį.</span><span class="sxs-lookup"><span data-stu-id="ab875-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Įverčių histogramų modulio įtraukimas į produktų apžvalgų sąrašo modulį](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="ab875-157">Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos</span><span class="sxs-lookup"><span data-stu-id="ab875-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="ab875-158">Įverčių ir apžvalgų konfigūravimo reikšmės, pvz., nuomotojo ID, apžvalgos teksto ilgis ir apžvalgos pavadinimo ilgis, konfigūruojamos svetainės lygiu.</span><span class="sxs-lookup"><span data-stu-id="ab875-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="ab875-159">Norėdami sukonfigūruoti svetainę, kad būtų rodomi įverčiai ir apžvalgos, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab875-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="ab875-160">Nueikite į **Pradžia \> Svetainės**.</span><span class="sxs-lookup"><span data-stu-id="ab875-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="ab875-161">Pasirinkite savo svetainės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ab875-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="ab875-162">Nueikite į **Svetainės valdymas \> Išplečiamumas**.</span><span class="sxs-lookup"><span data-stu-id="ab875-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="ab875-163">Lauke **Maks. apžvalgos teksto ilgis** įveskite maksimalų galimą apžvalgos teksto simbolių skaičių (pavyzdžiui, **1000**).</span><span class="sxs-lookup"><span data-stu-id="ab875-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="ab875-164">Lauke **Maks. apžvalgos pavadinimo ilgis** įveskite maksimalų galimą apžvalgos pavadinimų simbolių skaičių (pavyzdžiui, **55**).</span><span class="sxs-lookup"><span data-stu-id="ab875-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="ab875-165">Pasirinkite **Įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="ab875-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="ab875-166">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ab875-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="ab875-168">Produkto įverčio susiejimas su PIIP skyriumi Apžvalgos</span><span class="sxs-lookup"><span data-stu-id="ab875-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="ab875-169">Produkto įvertis rodomas po produkto pavadinimu PIIP viršuje.</span><span class="sxs-lookup"><span data-stu-id="ab875-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="ab875-170">Galima sukonfigūruoti, kad produkto įvertis būtų susietas su to paties PIIP skyriumi **Apžvalgos**.</span><span class="sxs-lookup"><span data-stu-id="ab875-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="ab875-171">Norėdami produkto įvertį susieti su PIIP skyriumi **Apžvalgos**, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab875-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="ab875-172">Atidarykite PIIP šabloną.</span><span class="sxs-lookup"><span data-stu-id="ab875-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="ab875-173">Nueikite į **Pirkimo langelio konteinerio modulių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ab875-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="ab875-174">Dalyje **Pirkimo langelis** pasirinkite **Produktų įverčiai**, tada pažymėkite žymės langelį **Spustelėjimą susieti su visų apžvalgų moduliu**.</span><span class="sxs-lookup"><span data-stu-id="ab875-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="ab875-175">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ab875-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Produkto įverčio susiejimas su PIIP skyriumi Apžvalgos](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="ab875-177">Privatumo ir strategijų puslapio saito konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ab875-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="ab875-178">Norėdami sukonfigūruoti privatumo ir strategijų puslapio saitą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab875-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="ab875-179">Nueikite į **Pradžia \> Svetainės**.</span><span class="sxs-lookup"><span data-stu-id="ab875-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="ab875-180">Pasirinkite savo svetainės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ab875-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="ab875-181">Nueikite į **Svetainės valdymas \> Išplečiamumas**</span><span class="sxs-lookup"><span data-stu-id="ab875-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="ab875-182">Skirtuko **Maršrutai** dalyje **RNR privatumas ir strategija** pasirinkite **Įtraukti saitą**.</span><span class="sxs-lookup"><span data-stu-id="ab875-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="ab875-183">Jei saitas jau įvestas ir norite jį pakeisti, jį pasirinkite.</span><span class="sxs-lookup"><span data-stu-id="ab875-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="ab875-184">Dialogo lange **Saito įtraukimas** pasirinkite privatumo ir strategijos puslapio saitą ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ab875-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="ab875-185">Pasirinkite **Įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="ab875-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="ab875-186">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ab875-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Privatumo ir strategijų puslapio saito konfigūravimas](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="ab875-188">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ab875-188">Additional resources</span></span>

[<span data-ttu-id="ab875-189">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="ab875-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="ab875-190">Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus</span><span class="sxs-lookup"><span data-stu-id="ab875-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="ab875-191">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="ab875-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="ab875-192">Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“</span><span class="sxs-lookup"><span data-stu-id="ab875-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
