---
title: Produkto informacijos puslapių apžvalga
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697870"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="1b8b9-103">Produkto informacijos puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="1b8b9-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1b8b9-104">Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų išsamios informacijos puslapių (PDP) apžvalga.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1b8b9-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="1b8b9-105">Overview</span></span>

<span data-ttu-id="1b8b9-106">PDP pateikiama išsami informacija apie produktą ir juose klientai gal pasirinkti produkto parinktis, pvz., dydį, stilių ir spalvą.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="1b8b9-107">PDP turi parodyti visą informaciją apie produktą, kurios klientui reikia pirkimo sprendimui priimti.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="1b8b9-108">Toliau pateikiamoje iliustracijoje vaizduojamas PDP pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-108">The following illustration shows an example of a PDP.</span></span>

![Produkto informacijos puslapio pavyzdys](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="1b8b9-110">Antraštės ir poraštės moduliai</span><span class="sxs-lookup"><span data-stu-id="1b8b9-110">Header and footer modules</span></span>

<span data-ttu-id="1b8b9-111">PDP viršuje yra antraštė, rodanti visas produktų kategorijas ir kitus puslapius, kuriuose pardavėjas norėtų, kad klientai naršytų.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="1b8b9-112">Puslapio apačioje yra poraštė, kurioje yra spartieji saitai su įvairiomis temomis, kurios gali sudominti klientus.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="1b8b9-113">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="1b8b9-113">Buy box module</span></span>

<span data-ttu-id="1b8b9-114">Svarbiausias PDP modulis yra pirkimo langelių modulis.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="1b8b9-115">Todėl jis yra pirmas pagrindinės puslapio dalies elementas.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="1b8b9-116">Pirkimo langelių modulis yra konteinerio modulis ir jame saugomi keli moduliai, kuriuose yra svarbiausia informacija apie produktą.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="1b8b9-117">Į šią informaciją įeina produkto pavadinimas, produkto atvaizdai, aprašas, kaina ir produktų įvertinimai.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="1b8b9-118">Pirkimo langelių modulis leidžia klientui pasirinkti produkto parinktis (pavyzdžiui, dydžio, stiliaus ir spalvos) ir įtraukti produktą į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="1b8b9-119">Be to, juo klientas gali pirkti produktą internetu ir atsiimti jį parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="1b8b9-120">Pirkimo internetu ir atsiėmimo parduotuvėje modulis naudoja integravimą su „Bing“ žemėlapių programos programavimo sąsajomis (API), kad būtų galima rasti netoliese esančių parduotuvių arba parduotuvių kitoje vietoje, kurią nurodo klientas.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="1b8b9-121">Pirkimo langelių moduliui reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="1b8b9-122">Šis ID išvestas iš puslapio konteksto.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-122">This ID is derived from the page context.</span></span> <span data-ttu-id="1b8b9-123">Jei pirkimo langelių modulis yra įtrauktas į puslapį, kurio puslapio kontekste nėra produkto ID, jis tinkamai negeneruos informacijos.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="1b8b9-124">Produkto specifikacijų modulis</span><span class="sxs-lookup"><span data-stu-id="1b8b9-124">Product specifications module</span></span>

<span data-ttu-id="1b8b9-125">Produkto specifikacijų modulį galima naudoti norint parodyti papildomą produkto informaciją.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="1b8b9-126">Ši išsami informacija paimama iš produkto atributų, esančių „Dynamics 365 Retail“.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="1b8b9-127">Produkto specifikacijų modulyje nurodomas kiekvienas atributas, kurio **matoma** ypatybė nustatyta kaip **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="1b8b9-128">Jis reikalauja, kad produkto ID gautų produkto atributus.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="1b8b9-129">Rekomendacijų modulis</span><span class="sxs-lookup"><span data-stu-id="1b8b9-129">Recommendations module</span></span>

<span data-ttu-id="1b8b9-130">Rekomendacijų modulis yra svarbus PDP modulis.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="1b8b9-131">Vartotojams naršant produktus, turi būti pateikiama daugiau produktų, kad jie galėtų rasti tinkamą produktą ir atlikti pirkimą.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="1b8b9-132">Rekomendacijos padeda klientams lengvai atrasti susijusį turinį ir tęsti apsipirkimą.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="1b8b9-133">Galimi skirtingi rekomendacijų sąrašų tipai:</span><span class="sxs-lookup"><span data-stu-id="1b8b9-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="1b8b9-134">**Žmonėms taip pat patiko** sąrašas pagrįstas mašininiu mokymu.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="1b8b9-135">Jam naudojama kitų klientų operacijų retrospektyvą pateikti rekomendacijų.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="1b8b9-136">Šį sąrašą generuoja rekomendacijų tarnyba ir primena sąrašus „Klientai, kurie pirko, taip pat pirko...“.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="1b8b9-137">Šiam sąrašui generuoti reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="1b8b9-138">**Susiję** sąrašą galima konfigūruoti produktui „Retail“ programoje.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="1b8b9-139">Pavyzdžiui, rudos odos kelioninei rankinei gali būti konfigūruojama susijusiame sąraše daugiau rankinių, kurios yra iš odos arba skirtos kelionėms.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="1b8b9-140">Kiti susiję sąrašai, pvz. **Papuošalai** ir **Daugiau panašių**, taip pat gali būti sukonfigūruoti „Retail“ programoje.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="1b8b9-141">Šiam sąrašui generuoti reikia produkto ID.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="1b8b9-142">Todėl, jei jis pridėtas prie pagrindinio puslapio, kuriame puslapio kontekste nėra produkto ID, sąrašas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="1b8b9-143">Algoritmiškai sugeneruoti rekomendacijų sąrašai, pvz. **Populiaru**, **Perkamiausi** ir **Nauja**, galima naudoti PDP.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="1b8b9-144">Nors šie sąrašai gali būti tiesiogiai nesusiję su PDP produktu, jie yra dar vienas būdas padėti klientams rasti produktus, kurie gali juos dominti.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="1b8b9-145">Šie sąrašų tipai nereikalauja produkto ID.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="1b8b9-146">Jie yra bendri sąrašai, sugeneruoti pagal pirkimo tendencijas svetainėje.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="1b8b9-147">Redakciniai sąrašai yra neautomatiniu būdu kuruoti sąrašai.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="1b8b9-148">Pavyzdžiui, pardavėjas gali nuspręsti neautomatiniu būdu kuruoti produktų, kuriuos norima rodyti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="1b8b9-149">Įvertinimų ir apžvalgų modulis</span><span class="sxs-lookup"><span data-stu-id="1b8b9-149">Ratings and reviews module</span></span>

<span data-ttu-id="1b8b9-150">Modulyje įvertinimai ir apžvalgos pateikiami įvertinimai ir apžvalgos, kuriuos pateikė kiti klientai.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="1b8b9-151">Jame klientai taip pat gali parašyti produkto apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="1b8b9-152">Be to, jame yra histograma, rodanti produkto įvertinimų tendenciją.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="1b8b9-153">Daugiau informacijos žr. [Įvertinimų ir apžvalgų apžvalga](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1b8b9-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="1b8b9-154">Rinkodaros moduliai</span><span class="sxs-lookup"><span data-stu-id="1b8b9-154">Marketing modules</span></span>

<span data-ttu-id="1b8b9-155">Jeigu rinkodaros turinys yra unikalus konkrečiam produktui, bet koks rinkodaros modulis gali būti pridėtas prie PDP.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="1b8b9-156">Galite įtraukti rinkodaros modulius į PDP, naudodami puslapio „papildymą“.</span><span class="sxs-lookup"><span data-stu-id="1b8b9-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="1b8b9-157">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1b8b9-157">Additional resources</span></span>

[<span data-ttu-id="1b8b9-158">Pagrindinio puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="1b8b9-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="1b8b9-159">Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="1b8b9-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="1b8b9-160">Krepšelio ir pirkimo užbaigimo puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="1b8b9-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="1b8b9-161">Paskyros valdymo puslapių apžvalga</span><span class="sxs-lookup"><span data-stu-id="1b8b9-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
