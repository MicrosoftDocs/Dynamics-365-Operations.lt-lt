---
title: Produktų informacijos puslapių apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792224"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="2f62d-103">Produkto informacijos puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="2f62d-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f62d-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.</span><span class="sxs-lookup"><span data-stu-id="2f62d-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2f62d-105">PDP pateikiama išsami informacija apie produktą ir juose klientai gal pasirinkti produkto parinktis, pvz., dydį, stilių ir spalvą.</span><span class="sxs-lookup"><span data-stu-id="2f62d-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="2f62d-106">PDP turi parodyti visą informaciją apie produktą, kurios klientui reikia pirkimo sprendimui priimti.</span><span class="sxs-lookup"><span data-stu-id="2f62d-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="2f62d-107">Toliau pateikiamoje iliustracijoje vaizduojamas PDP pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="2f62d-107">The following illustration shows an example of a PDP.</span></span>

![Produkto informacijos puslapio pavyzdys](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="2f62d-109">Antraštės ir poraštės moduliai</span><span class="sxs-lookup"><span data-stu-id="2f62d-109">Header and footer modules</span></span>

<span data-ttu-id="2f62d-110">PDP viršuje yra antraštė, rodanti visas produktų kategorijas ir kitus puslapius, kuriuose pardavėjas norėtų, kad klientai naršytų.</span><span class="sxs-lookup"><span data-stu-id="2f62d-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="2f62d-111">Puslapio apačioje yra poraštė, kurioje yra spartieji saitai su įvairiomis temomis, kurios gali sudominti klientus.</span><span class="sxs-lookup"><span data-stu-id="2f62d-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="2f62d-112">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="2f62d-112">Buy box module</span></span>

<span data-ttu-id="2f62d-113">Svarbiausias PDP modulis yra pirkimo langelio modulis, kuris pasirodo kaip pirmasis elementas pagrindinėje puslapio dalyje.</span><span class="sxs-lookup"><span data-stu-id="2f62d-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="2f62d-114">Pirkimo langelių modulyje rodoma svarbi informacija apie produktą, kaip pavyzdžiui, produkto pavadinimas, produkto aprašymas, produkto kaina, produkto nuotraukos ir produkto įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="2f62d-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="2f62d-115">Pirkimo langelių modulis leidžia klientui pasirinkti produkto parinktis (pavyzdžiui, dydžio, stiliaus ir spalvos) ir įtraukti produktą į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="2f62d-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="2f62d-116">Be to, juo klientas gali pirkti produktą internetu ir atsiimti jį parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="2f62d-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="2f62d-117">Pirkimo internetu ir atsiėmimo parduotuvėje modulis naudoja integravimą su „Bing“ žemėlapių programos programavimo sąsajomis (API), kad būtų galima rasti netoliese esančių parduotuvių arba parduotuvių kitoje vietoje, kurią nurodo klientas.</span><span class="sxs-lookup"><span data-stu-id="2f62d-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="2f62d-118">Pirkimo langelių moduliui reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="2f62d-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="2f62d-119">Šis ID išvestas iš puslapio konteksto.</span><span class="sxs-lookup"><span data-stu-id="2f62d-119">This ID is derived from the page context.</span></span> <span data-ttu-id="2f62d-120">Jei pirkimo langelių modulis yra įtrauktas į puslapį, kurio puslapio kontekste nėra produkto ID, jis tinkamai negeneruos informacijos.</span><span class="sxs-lookup"><span data-stu-id="2f62d-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="2f62d-121">Produkto specifikacijų modulis</span><span class="sxs-lookup"><span data-stu-id="2f62d-121">Product specifications module</span></span>

<span data-ttu-id="2f62d-122">Produkto specifikacijų modulį galima naudoti norint parodyti papildomą produkto informaciją.</span><span class="sxs-lookup"><span data-stu-id="2f62d-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="2f62d-123">Ši informacija yra paimta iš produkto atributų, esančių „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="2f62d-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="2f62d-124">Produkto specifikacijų modulyje nurodomas kiekvienas atributas, kurio **matoma** ypatybė nustatyta kaip **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="2f62d-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="2f62d-125">Jis reikalauja, kad produkto ID gautų produkto atributus.</span><span class="sxs-lookup"><span data-stu-id="2f62d-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="2f62d-126">Rekomendacijų modulis</span><span class="sxs-lookup"><span data-stu-id="2f62d-126">Recommendations module</span></span>

<span data-ttu-id="2f62d-127">Rekomendacijų modulis yra svarbus PDP modulis.</span><span class="sxs-lookup"><span data-stu-id="2f62d-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="2f62d-128">Vartotojams naršant produktus, turi būti pateikiama daugiau produktų, kad jie galėtų rasti tinkamą produktą ir atlikti pirkimą.</span><span class="sxs-lookup"><span data-stu-id="2f62d-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="2f62d-129">Rekomendacijos padeda klientams lengvai atrasti susijusį turinį ir tęsti apsipirkimą.</span><span class="sxs-lookup"><span data-stu-id="2f62d-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="2f62d-130">Galimi skirtingi rekomendacijų sąrašų tipai:</span><span class="sxs-lookup"><span data-stu-id="2f62d-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="2f62d-131">**Žmonėms taip pat patiko** sąrašas pagrįstas mašininiu mokymu.</span><span class="sxs-lookup"><span data-stu-id="2f62d-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="2f62d-132">Jam naudojama kitų klientų operacijų retrospektyvą pateikti rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="2f62d-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="2f62d-133">Šį sąrašą generuoja rekomendacijų tarnyba ir primena sąrašus „Klientai, kurie pirko, taip pat pirko...“.</span><span class="sxs-lookup"><span data-stu-id="2f62d-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="2f62d-134">Šiam sąrašui generuoti reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="2f62d-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="2f62d-135">**„Susiję“** sąrašą galima sukonfigūruoti „Commerce“ produktui.</span><span class="sxs-lookup"><span data-stu-id="2f62d-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="2f62d-136">Pavyzdžiui, rudos odos kelioninei rankinei gali būti konfigūruojama susijusiame sąraše daugiau rankinių, kurios yra iš odos arba skirtos kelionėms.</span><span class="sxs-lookup"><span data-stu-id="2f62d-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="2f62d-137">Kitų tipų susijusius sąrašus, tokius kaip **Aksesuarai** ir **Daugiau panašių**, taip pat galima sukonfigūruoti „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="2f62d-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="2f62d-138">Šiam sąrašui generuoti reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="2f62d-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="2f62d-139">Todėl, jei jis pridėtas prie pagrindinio puslapio, kuriame puslapio kontekste nėra produkto ID, sąrašas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="2f62d-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="2f62d-140">Algoritmiškai sugeneruoti rekomendacijų sąrašai, pvz. **Populiaru**, **Perkamiausi** ir **Nauja**, galima naudoti PDP.</span><span class="sxs-lookup"><span data-stu-id="2f62d-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="2f62d-141">Nors šie sąrašai gali būti tiesiogiai nesusiję su PDP produktu, jie yra dar vienas būdas padėti klientams rasti produktus, kurie gali juos dominti.</span><span class="sxs-lookup"><span data-stu-id="2f62d-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="2f62d-142">Šie sąrašų tipai nereikalauja produkto ID.</span><span class="sxs-lookup"><span data-stu-id="2f62d-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="2f62d-143">Jie yra bendri sąrašai, sugeneruoti pagal pirkimo tendencijas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="2f62d-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="2f62d-144">Redakciniai sąrašai yra neautomatiniu būdu kuruoti sąrašai.</span><span class="sxs-lookup"><span data-stu-id="2f62d-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="2f62d-145">Pavyzdžiui, pardavėjas gali nuspręsti neautomatiniu būdu kuruoti produktų, kuriuos norima rodyti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="2f62d-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="2f62d-146">Įvertinimų ir apžvalgų moduliai</span><span class="sxs-lookup"><span data-stu-id="2f62d-146">Ratings and reviews modules</span></span>

<span data-ttu-id="2f62d-147">Norint parodyti ir pridėti apžvalgas, gali būti naudojami trys moduliai.</span><span class="sxs-lookup"><span data-stu-id="2f62d-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="2f62d-148">**Apžvalgos** – šiame modulyje pateikiami įvertinimai ir apžvalgos, kuriuos pateikė kiti klientai.</span><span class="sxs-lookup"><span data-stu-id="2f62d-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="2f62d-149">Klientai gali rūšiuoti ir filtruoti apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="2f62d-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="2f62d-150">Šis modulis taip pat leidžia klientams pamėgti ar nepamėgti apžvalgas ir pranešti apie problemas.</span><span class="sxs-lookup"><span data-stu-id="2f62d-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="2f62d-151">**Rašyti apžvalgą** – šis modulis leidžia klientams parašyti savo apžvalgą apie produktą.</span><span class="sxs-lookup"><span data-stu-id="2f62d-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="2f62d-152">**Įvertinimo histograma** – šiame modulyje yra histograma, rodanti produkto įvertinimo tendencijas.</span><span class="sxs-lookup"><span data-stu-id="2f62d-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="2f62d-153">Daugiau informacijos žr. [Įvertinimų ir apžvalgų apžvalga](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2f62d-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="2f62d-154">Rinkodaros moduliai</span><span class="sxs-lookup"><span data-stu-id="2f62d-154">Marketing modules</span></span>

<span data-ttu-id="2f62d-155">Jeigu rinkodaros turinys yra unikalus konkrečiam produktui, bet koks rinkodaros modulis gali būti pridėtas prie PDP.</span><span class="sxs-lookup"><span data-stu-id="2f62d-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="2f62d-156">Galite įtraukti rinkodaros modulius į PDP, naudodami puslapio „papildymą“.</span><span class="sxs-lookup"><span data-stu-id="2f62d-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="2f62d-157">Norėdami gauti išsamesnės informacijos, žr. [„Papildyti produkto puslapį“](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="2f62d-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f62d-158">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2f62d-158">Additional resources</span></span>

[<span data-ttu-id="2f62d-159">Pagrindinio puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="2f62d-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="2f62d-160">Krepšelio ir pirkimo užbaigimo puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="2f62d-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="2f62d-161">Paskyrų tvarkymo puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="2f62d-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="2f62d-162">„Papildyti produkto aprašymo puslapį“.</span><span class="sxs-lookup"><span data-stu-id="2f62d-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
