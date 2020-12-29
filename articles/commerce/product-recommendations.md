---
title: Produktų rekomendacijų apžvalga
description: Šioje temoje pateikta bendra informacija apie produkto rekomendacijas. Produktų rekomendacijos leidžia vartotojams lengvai ir greitai rasti norimus produktus ir netgi produktų, kurių jie neketina pirkti.
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5aa7db8e53906f9e1416b912fe2c3b70d5430258
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414220"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="34068-104">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="34068-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="34068-105">„Microsoft Dynamics 365 Commerce“ gali būti naudojama rodyti produkto rekomendacijas „e-Commerce“ svetainėje ir elektroninio kasos aparato (EKA) įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="34068-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="34068-106">Produkto rekomendacijos – tai prekės, kurios gali sudominti klientą.</span><span class="sxs-lookup"><span data-stu-id="34068-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="34068-107">Rekomendacijos yra paremtos kitų klientų pirkimo tendencijomis internetinėse ir fizinėse parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="34068-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="34068-108">Pasitelkdami produktų rekomendacijomis vartotojai gali lengvai ir greitai rasti norimų produktų, tad ši funkcija jiems labai naudinga.</span><span class="sxs-lookup"><span data-stu-id="34068-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="34068-109">Kryžminis pardavimas ir papildomas pardavimas gali būti naudojami netgi siekiant padėti klientams surasti papildomų produktų, kurių iš pradžių jie net neketino pirkti.</span><span class="sxs-lookup"><span data-stu-id="34068-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="34068-110">Kai rekomendacijos yra naudojamos siekiant pagerinti produkto atradimą, atsiranda daugiau konversijos padidinimo galimybių, išauga pardavimo įplaukos, netgi pagerėja klientų pasitenkinimas ir tokiu būdu jie išsaugomi.</span><span class="sxs-lookup"><span data-stu-id="34068-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="34068-111">„e-Commerce“ produktų rekomendacijoms plačiai naudojama „Microsoft“ rekomendacijų mašininio mokymo technologijų platforma.</span><span class="sxs-lookup"><span data-stu-id="34068-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="34068-112">Rekomendacijų paslauga</span><span class="sxs-lookup"><span data-stu-id="34068-112">Recommendation service</span></span>

<span data-ttu-id="34068-113">Produkto rekomendacijų paslauga naudoja dirbtinio intelekto ir mašininio mokymosi (AI-ML) technologijas toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="34068-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="34068-114">Rekomendavimo paslaugai reikiamu formatu pateikti duomenys ištraukiami iš „Commerce“ operacinės duomenų bazės ir siunčiami į Azure Data Lake Storage arba objekto parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="34068-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="34068-115">Rekomendacijų paslaugai naudojami išsaugoti duomenys, skirti mokyti rekomendavimo modelius sąrašams **Žmonėms taip pat patiko**, **Dažnai kartu perkama**, **Nauja**, **Perkamiausi** ir **Populiaru**.</span><span class="sxs-lookup"><span data-stu-id="34068-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="34068-116">Scenarijai</span><span class="sxs-lookup"><span data-stu-id="34068-116">Scenarios</span></span>

<span data-ttu-id="34068-117">Produktų rekomendacijos pasiekiamos toliau nurodytais scenarijais:</span><span class="sxs-lookup"><span data-stu-id="34068-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="34068-118">**Bet kuriame parduotuvės naršymo puslapyje ar nukreipimo puslapyje el. prekyboje:** Jei klientai arba parduotuvės partneriai lankosi parduotuvės puslapyje, rekomendacijų mechanizmas gali siūlyti produktus iš sąrašų **Nauja**, **Perkamiausi** ir **Populiaru**.</span><span class="sxs-lookup"><span data-stu-id="34068-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="34068-119">**Produkto išsamios informacijos puslapyje:** Jei klientai ar parduotuvės partneriai apsilanko puslapyje **Produkto išsami informacija**, rekomendacijos mechanizmas pasiūlys papildomas prekes, kurios taip pat gali būti perkamos.</span><span class="sxs-lookup"><span data-stu-id="34068-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="34068-120">Šie elementai rodomi sąraše **Žmonėms taip pat patiko**.</span><span class="sxs-lookup"><span data-stu-id="34068-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="34068-121">**Operacijų puslapyje arba pirkimo užbaigimo puslapyje:** rekomendacijų mechanizmas siūlo prekių pagal visų prekių krepšelyje sąrašą.</span><span class="sxs-lookup"><span data-stu-id="34068-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="34068-122">Šios prekės rodomos sąraše **Dažnai kartu perkama**.</span><span class="sxs-lookup"><span data-stu-id="34068-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="34068-123">**Pagal asmeninius poreikius pritaikytos rekomendacijos:** prekybininkai gali pateikti prisijungusiems klientams asmeninius sąrašus **Parinkta jums**, be naujų funkcijų, leidžiančių esamus sąrašo scenarijus pritaikyti pagal asmeninius poreikius ir atsižvelgiant į konkretų klientą.</span><span class="sxs-lookup"><span data-stu-id="34068-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="34068-124">Norėdami sužinoti daugiau, žr. [Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="34068-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="34068-125">Produktų rekomendacijų tipai</span><span class="sxs-lookup"><span data-stu-id="34068-125">Types of product recommendations</span></span>

<span data-ttu-id="34068-126">Šioje lentelėje aprašytos įvairių tipų automatizuotos produktų rekomendacijos, kurias mažmenininkai gali naudoti „Dynamics 365 Commerce“ per [produktų rinkinio modulį](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="34068-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="34068-127">Mažmenininkai taip pat gali šiame sąraše prisiregistravusiam vartotojui pateikti personalizuotus rezultatus, jei svetainės autorius nustato atitinkamą parinktį.</span><span class="sxs-lookup"><span data-stu-id="34068-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="34068-128">Produktų atsiėmimo modulis</span><span class="sxs-lookup"><span data-stu-id="34068-128">Product collection module</span></span>  | <span data-ttu-id="34068-129">Tipas</span><span class="sxs-lookup"><span data-stu-id="34068-129">Type</span></span> | <span data-ttu-id="34068-130">aprašymas</span><span class="sxs-lookup"><span data-stu-id="34068-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="34068-131">Naujos</span><span class="sxs-lookup"><span data-stu-id="34068-131">New</span></span>                        | <span data-ttu-id="34068-132">Algoritminis</span><span class="sxs-lookup"><span data-stu-id="34068-132">Algorithmic</span></span> | <span data-ttu-id="34068-133">Šiame modulyje rodomas naujausių produktų, kurie buvo neseniai atrinkti į kanalus ir katalogus, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="34068-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="34068-134">Perkamiausia</span><span class="sxs-lookup"><span data-stu-id="34068-134">Best selling</span></span>               | <span data-ttu-id="34068-135">Algoritminis</span><span class="sxs-lookup"><span data-stu-id="34068-135">Algorithmic</span></span> | <span data-ttu-id="34068-136">Šiame modulyje rodomas produktų, kurie išdėstyti pagal didžiausią pardavimo skaičių, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="34068-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="34068-137">Populiaru</span><span class="sxs-lookup"><span data-stu-id="34068-137">Trending</span></span>                   | <span data-ttu-id="34068-138">Algoritminis</span><span class="sxs-lookup"><span data-stu-id="34068-138">Algorithmic</span></span> | <span data-ttu-id="34068-139">Šis modulis pateikia tam tikro laikotarpio labiausiai parduodamų produktų sąrašą pagal didžiausią pardavimų skaičių.</span><span class="sxs-lookup"><span data-stu-id="34068-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="34068-140">Dažnai perkama kartu</span><span class="sxs-lookup"><span data-stu-id="34068-140">Frequently bought together</span></span> | <span data-ttu-id="34068-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="34068-141">AI-ML</span></span> | <span data-ttu-id="34068-142">Šiame modulyje rekomenduojami produktai, kurie dažniausiai perkami kartu su dabartinio vartotojo krepšelio turiniu.</span><span class="sxs-lookup"><span data-stu-id="34068-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="34068-143">Žmonėms taip pat patinka</span><span class="sxs-lookup"><span data-stu-id="34068-143">People also like</span></span>           | <span data-ttu-id="34068-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="34068-144">AI-ML</span></span> | <span data-ttu-id="34068-145">Šiame modulyje rekomenduojami tam tikro pradinio gaminio produktai, atsižvelgiant į vartotojų pirkimo tendencijas.</span><span class="sxs-lookup"><span data-stu-id="34068-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="34068-146">Parinkta jums</span><span class="sxs-lookup"><span data-stu-id="34068-146">Picks for you</span></span>              | <span data-ttu-id="34068-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="34068-147">AI-ML</span></span> | <span data-ttu-id="34068-148">Šiame modulyje rekomenduojamas asmeniniams poreikiams pritaikytų produktų sąrašas, atsižvelgiant į prisiregistravusio vartotojo pirkimo tendencijas.</span><span class="sxs-lookup"><span data-stu-id="34068-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="34068-149">Vartotojui svečiui bus rodomas sutrauktas sąrašas.</span><span class="sxs-lookup"><span data-stu-id="34068-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="34068-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="34068-150">Additional resources</span></span>

[<span data-ttu-id="34068-151">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="34068-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="34068-152">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="34068-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="34068-153">Personalizuotų rekomendacijų įjungimas</span><span class="sxs-lookup"><span data-stu-id="34068-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="34068-154">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="34068-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="34068-155">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="34068-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="34068-156">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="34068-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="34068-157">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="34068-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="34068-158">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="34068-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="34068-159">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="34068-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="34068-160">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="34068-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="34068-161">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="34068-161">Product recommendations FAQ</span></span>](faq-recommendations.md)
