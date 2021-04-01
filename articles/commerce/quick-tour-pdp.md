---
title: Produktų informacijos puslapių apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 020c2a72515eb112adb33c6b58e3a5084339d040
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243844"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="bac1b-103">Produkto informacijos puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="bac1b-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bac1b-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.</span><span class="sxs-lookup"><span data-stu-id="bac1b-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bac1b-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="bac1b-105">Overview</span></span>

<span data-ttu-id="bac1b-106">PDP pateikiama išsami informacija apie produktą ir juose klientai gal pasirinkti produkto parinktis, pvz., dydį, stilių ir spalvą.</span><span class="sxs-lookup"><span data-stu-id="bac1b-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="bac1b-107">PDP turi parodyti visą informaciją apie produktą, kurios klientui reikia pirkimo sprendimui priimti.</span><span class="sxs-lookup"><span data-stu-id="bac1b-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="bac1b-108">Toliau pateikiamoje iliustracijoje vaizduojamas PDP pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="bac1b-108">The following illustration shows an example of a PDP.</span></span>

![Produkto informacijos puslapio pavyzdys](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="bac1b-110">Antraštės ir poraštės moduliai</span><span class="sxs-lookup"><span data-stu-id="bac1b-110">Header and footer modules</span></span>

<span data-ttu-id="bac1b-111">PDP viršuje yra antraštė, rodanti visas produktų kategorijas ir kitus puslapius, kuriuose pardavėjas norėtų, kad klientai naršytų.</span><span class="sxs-lookup"><span data-stu-id="bac1b-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="bac1b-112">Puslapio apačioje yra poraštė, kurioje yra spartieji saitai su įvairiomis temomis, kurios gali sudominti klientus.</span><span class="sxs-lookup"><span data-stu-id="bac1b-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="bac1b-113">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="bac1b-113">Buy box module</span></span>

<span data-ttu-id="bac1b-114">Svarbiausias PDP modulis yra pirkimo langelio modulis, kuris pasirodo kaip pirmasis elementas pagrindinėje puslapio dalyje.</span><span class="sxs-lookup"><span data-stu-id="bac1b-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="bac1b-115">Pirkimo langelių modulyje rodoma svarbi informacija apie produktą, kaip pavyzdžiui, produkto pavadinimas, produkto aprašymas, produkto kaina, produkto nuotraukos ir produkto įvertinimas.</span><span class="sxs-lookup"><span data-stu-id="bac1b-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="bac1b-116">Pirkimo langelių modulis leidžia klientui pasirinkti produkto parinktis (pavyzdžiui, dydžio, stiliaus ir spalvos) ir įtraukti produktą į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="bac1b-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="bac1b-117">Be to, juo klientas gali pirkti produktą internetu ir atsiimti jį parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="bac1b-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="bac1b-118">Pirkimo internetu ir atsiėmimo parduotuvėje modulis naudoja integravimą su „Bing“ žemėlapių programos programavimo sąsajomis (API), kad būtų galima rasti netoliese esančių parduotuvių arba parduotuvių kitoje vietoje, kurią nurodo klientas.</span><span class="sxs-lookup"><span data-stu-id="bac1b-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="bac1b-119">Pirkimo langelių moduliui reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="bac1b-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="bac1b-120">Šis ID išvestas iš puslapio konteksto.</span><span class="sxs-lookup"><span data-stu-id="bac1b-120">This ID is derived from the page context.</span></span> <span data-ttu-id="bac1b-121">Jei pirkimo langelių modulis yra įtrauktas į puslapį, kurio puslapio kontekste nėra produkto ID, jis tinkamai negeneruos informacijos.</span><span class="sxs-lookup"><span data-stu-id="bac1b-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="bac1b-122">Produkto specifikacijų modulis</span><span class="sxs-lookup"><span data-stu-id="bac1b-122">Product specifications module</span></span>

<span data-ttu-id="bac1b-123">Produkto specifikacijų modulį galima naudoti norint parodyti papildomą produkto informaciją.</span><span class="sxs-lookup"><span data-stu-id="bac1b-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="bac1b-124">Ši informacija yra paimta iš produkto atributų, esančių „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="bac1b-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="bac1b-125">Produkto specifikacijų modulyje nurodomas kiekvienas atributas, kurio **matoma** ypatybė nustatyta kaip **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="bac1b-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="bac1b-126">Jis reikalauja, kad produkto ID gautų produkto atributus.</span><span class="sxs-lookup"><span data-stu-id="bac1b-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="bac1b-127">Rekomendacijų modulis</span><span class="sxs-lookup"><span data-stu-id="bac1b-127">Recommendations module</span></span>

<span data-ttu-id="bac1b-128">Rekomendacijų modulis yra svarbus PDP modulis.</span><span class="sxs-lookup"><span data-stu-id="bac1b-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="bac1b-129">Vartotojams naršant produktus, turi būti pateikiama daugiau produktų, kad jie galėtų rasti tinkamą produktą ir atlikti pirkimą.</span><span class="sxs-lookup"><span data-stu-id="bac1b-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="bac1b-130">Rekomendacijos padeda klientams lengvai atrasti susijusį turinį ir tęsti apsipirkimą.</span><span class="sxs-lookup"><span data-stu-id="bac1b-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="bac1b-131">Galimi skirtingi rekomendacijų sąrašų tipai:</span><span class="sxs-lookup"><span data-stu-id="bac1b-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="bac1b-132">**Žmonėms taip pat patiko** sąrašas pagrįstas mašininiu mokymu.</span><span class="sxs-lookup"><span data-stu-id="bac1b-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="bac1b-133">Jam naudojama kitų klientų operacijų retrospektyvą pateikti rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="bac1b-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="bac1b-134">Šį sąrašą generuoja rekomendacijų tarnyba ir primena sąrašus „Klientai, kurie pirko, taip pat pirko...“.</span><span class="sxs-lookup"><span data-stu-id="bac1b-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="bac1b-135">Šiam sąrašui generuoti reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="bac1b-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="bac1b-136">**„Susiję“** sąrašą galima sukonfigūruoti „Commerce“ produktui.</span><span class="sxs-lookup"><span data-stu-id="bac1b-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="bac1b-137">Pavyzdžiui, rudos odos kelioninei rankinei gali būti konfigūruojama susijusiame sąraše daugiau rankinių, kurios yra iš odos arba skirtos kelionėms.</span><span class="sxs-lookup"><span data-stu-id="bac1b-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="bac1b-138">Kitų tipų susijusius sąrašus, tokius kaip **Aksesuarai** ir **Daugiau panašių**, taip pat galima sukonfigūruoti „Commerce“.</span><span class="sxs-lookup"><span data-stu-id="bac1b-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="bac1b-139">Šiam sąrašui generuoti reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="bac1b-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="bac1b-140">Todėl, jei jis pridėtas prie pagrindinio puslapio, kuriame puslapio kontekste nėra produkto ID, sąrašas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="bac1b-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="bac1b-141">Algoritmiškai sugeneruoti rekomendacijų sąrašai, pvz. **Populiaru**, **Perkamiausi** ir **Nauja**, galima naudoti PDP.</span><span class="sxs-lookup"><span data-stu-id="bac1b-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="bac1b-142">Nors šie sąrašai gali būti tiesiogiai nesusiję su PDP produktu, jie yra dar vienas būdas padėti klientams rasti produktus, kurie gali juos dominti.</span><span class="sxs-lookup"><span data-stu-id="bac1b-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="bac1b-143">Šie sąrašų tipai nereikalauja produkto ID.</span><span class="sxs-lookup"><span data-stu-id="bac1b-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="bac1b-144">Jie yra bendri sąrašai, sugeneruoti pagal pirkimo tendencijas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="bac1b-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="bac1b-145">Redakciniai sąrašai yra neautomatiniu būdu kuruoti sąrašai.</span><span class="sxs-lookup"><span data-stu-id="bac1b-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="bac1b-146">Pavyzdžiui, pardavėjas gali nuspręsti neautomatiniu būdu kuruoti produktų, kuriuos norima rodyti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="bac1b-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="bac1b-147">Įvertinimų ir apžvalgų moduliai</span><span class="sxs-lookup"><span data-stu-id="bac1b-147">Ratings and reviews modules</span></span>

<span data-ttu-id="bac1b-148">Norint parodyti ir pridėti apžvalgas, gali būti naudojami trys moduliai.</span><span class="sxs-lookup"><span data-stu-id="bac1b-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="bac1b-149">**Apžvalgos** – šiame modulyje pateikiami įvertinimai ir apžvalgos, kuriuos pateikė kiti klientai.</span><span class="sxs-lookup"><span data-stu-id="bac1b-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="bac1b-150">Klientai gali rūšiuoti ir filtruoti apžvalgas.</span><span class="sxs-lookup"><span data-stu-id="bac1b-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="bac1b-151">Šis modulis taip pat leidžia klientams pamėgti ar nepamėgti apžvalgas ir pranešti apie problemas.</span><span class="sxs-lookup"><span data-stu-id="bac1b-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="bac1b-152">**Rašyti apžvalgą** – šis modulis leidžia klientams parašyti savo apžvalgą apie produktą.</span><span class="sxs-lookup"><span data-stu-id="bac1b-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="bac1b-153">**Įvertinimo histograma** – šiame modulyje yra histograma, rodanti produkto įvertinimo tendencijas.</span><span class="sxs-lookup"><span data-stu-id="bac1b-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="bac1b-154">Daugiau informacijos žr. [Įvertinimų ir apžvalgų apžvalga](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bac1b-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="bac1b-155">Rinkodaros moduliai</span><span class="sxs-lookup"><span data-stu-id="bac1b-155">Marketing modules</span></span>

<span data-ttu-id="bac1b-156">Jeigu rinkodaros turinys yra unikalus konkrečiam produktui, bet koks rinkodaros modulis gali būti pridėtas prie PDP.</span><span class="sxs-lookup"><span data-stu-id="bac1b-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="bac1b-157">Galite įtraukti rinkodaros modulius į PDP, naudodami puslapio „papildymą“.</span><span class="sxs-lookup"><span data-stu-id="bac1b-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="bac1b-158">Norėdami gauti išsamesnės informacijos, žr. [„Papildyti produkto puslapį“](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="bac1b-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bac1b-159">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bac1b-159">Additional resources</span></span>

[<span data-ttu-id="bac1b-160">Pagrindinio puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="bac1b-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="bac1b-161">Krepšelio ir pirkimo užbaigimo puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="bac1b-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="bac1b-162">Paskyrų tvarkymo puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="bac1b-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="bac1b-163">„Papildyti produkto aprašymo puslapį“.</span><span class="sxs-lookup"><span data-stu-id="bac1b-163">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]