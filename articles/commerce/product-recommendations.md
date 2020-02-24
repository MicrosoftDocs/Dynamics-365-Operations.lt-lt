---
title: Produktų rekomendacijų apžvalga
description: Šioje temoje pateikta bendra informacija apie produkto rekomendacijas. Produktų rekomendacijos leidžia vartotojams lengvai ir greitai rasti norimus produktus ir netgi produktų, kurių jie neketina pirkti.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024984"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="d182e-104">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="d182e-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d182e-105">„Microsoft Dynamics 365 Commerce“ gali būti naudojama rodyti produkto rekomendacijas „e-Commerce“ svetainėje ir elektroninio kasos aparato (EKA) įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="d182e-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="d182e-106">Produkto rekomendacijos – tai prekės, kurios gali sudominti klientą.</span><span class="sxs-lookup"><span data-stu-id="d182e-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="d182e-107">Rekomendacijos yra paremtos kitų klientų pirkimo tendencijomis internetinėse ir fizinėse parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="d182e-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="d182e-108">Pasitelkdami produktų rekomendacijas vartotojai gali lengvai ir greitai rasti norimų produktų, tad ši funkcija jiems labai naudinga.</span><span class="sxs-lookup"><span data-stu-id="d182e-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="d182e-109">Kryžminis pardavimas ir papildomas pardavimas netgi gali būti naudojami siekiant padėti klientams surasti papildomų produktų, kurių iš pradžių jie net neketino pirkti.</span><span class="sxs-lookup"><span data-stu-id="d182e-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="d182e-110">Naudojant rekomendacijas padėti aptikti produktų, jomis galima sukurti daugiau konvertavimo galimybių, padėti padidinti įplaukas ir netgi padėti padidinti klientų pasitenkinimą bei išsaugojimą.</span><span class="sxs-lookup"><span data-stu-id="d182e-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="d182e-111">„Commerce“ produktų rekomendacijoms plačiai naudojama „Microsoft“ rekomendacijų mašininio mokymo technologijų platforma.</span><span class="sxs-lookup"><span data-stu-id="d182e-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="d182e-112">Scenarijai</span><span class="sxs-lookup"><span data-stu-id="d182e-112">Scenarios</span></span>

<span data-ttu-id="d182e-113">Produktų rekomendacijos pasiekiamos toliau nurodytais scenarijais:</span><span class="sxs-lookup"><span data-stu-id="d182e-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="d182e-114">**Bet kuriame parduotuvės naršymo puslapyje ar nukreipimo puslapyje el. prekyboje:** Jei klientai arba parduotuvės partneriai lankosi parduotuvės puslapyje, rekomendacijų mechanizmas gali siūlyti produktus iš sąrašų **Nauja**, **Perkamiausi** ir **Populiaru**.</span><span class="sxs-lookup"><span data-stu-id="d182e-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="d182e-115">**Produkto išsamios informacijos puslapyje:** Jei klientai ar parduotuvės partneriai apsilanko puslapyje **Produkto išsami informacija**, rekomendacijos mechanizmas pasiūlys papildomas prekes, kurios taip pat gali būti perkamos.</span><span class="sxs-lookup"><span data-stu-id="d182e-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="d182e-116">Šie elementai rodomi sąraše **Žmonėms taip pat patiko**.</span><span class="sxs-lookup"><span data-stu-id="d182e-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="d182e-117">**Operacijų puslapyje arba pirkimo užbaigimo puslapyje:** rekomendacijų mechanizmas siūlo prekių pagal visų prekių krepšelyje sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d182e-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="d182e-118">Šios prekės rodomos sąraše **Dažnai kartu perkama**.</span><span class="sxs-lookup"><span data-stu-id="d182e-118">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="d182e-119">**Pagal asmeninius poreikius pritaikytos rekomendacijos:** prekybininkai gali pateikti prisijungusiems klientams asmeninius sąrašus **Parinkta jums**, be naujų funkcijų, leidžiančių esamus sąrašo scenarijus pritaikyti pagal asmeninius poreikius ir atsižvelgiant į konkretų klientą.</span><span class="sxs-lookup"><span data-stu-id="d182e-119">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="d182e-120">Norėdami sužinoti daugiau, žr. funkcijos dokumentaciją:\[įgalinti pagal asmeninius poreikius pritaikytas rekomendacijas.](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="d182e-120">To learn more, please see the feature documenation: [enable personalized recommedations.](personalized-recommendations.md)</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="d182e-121">Rekomendacijų paslauga</span><span class="sxs-lookup"><span data-stu-id="d182e-121">Recommendation service</span></span>

<span data-ttu-id="d182e-122">Produktų rekomendacijoms naudojamos rekomendacijų mašininio mokymo technologijos šiais būdais:</span><span class="sxs-lookup"><span data-stu-id="d182e-122">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="d182e-123">Rekomendavimo paslaugai reikiamu formatu pateikti duomenys ištraukiami iš „Commerce“ operacinės duomenų bazės ir siunčiami į objekto parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="d182e-123">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="d182e-124">Rekomendavimo paslaugai naudojami duomenys, skirti mokyti rekomendavimo modelius sąrašams **Žmonėms taip pat patiko**, **Dažnai kartu perkama**, **Nauja**, **Perkamiausi** ir **Populiaru**.</span><span class="sxs-lookup"><span data-stu-id="d182e-124">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d182e-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d182e-125">Additional resources</span></span>

[<span data-ttu-id="d182e-126">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d182e-126">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d182e-127">Įgalinti asmeniniams poreikiams pritaikytas rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d182e-127">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d182e-128">Produktų rinkinio modulio peržiūra</span><span class="sxs-lookup"><span data-stu-id="d182e-128">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="d182e-129">Kurti kuruojamus produktų rekomendacijų sąrašus</span><span class="sxs-lookup"><span data-stu-id="d182e-129">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d182e-130">Tvarkyti AI-ML pagrįstų produktų rekomendacijų rezultatus</span><span class="sxs-lookup"><span data-stu-id="d182e-130">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d182e-131">ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius</span><span class="sxs-lookup"><span data-stu-id="d182e-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
