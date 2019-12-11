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
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770052"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="6f5f8-104">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="6f5f8-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="6f5f8-105">„Microsoft Dynamics 365 Commerce“ gali būti naudojama rodyti produkto rekomendacijas „e-Commerce“ svetainėje ir elektroninio kasos aparato (EKA) įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="6f5f8-106">Produkto rekomendacijos – tai prekės, kurios gali sudominti klientą.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="6f5f8-107">Rekomendacijos yra paremtos kitų klientų pirkimo tendencijomis internetinėse ir fizinėse parduotuvėse.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="6f5f8-108">Pasitelkdami produktų rekomendacijas vartotojai gali lengvai ir greitai rasti norimų produktų, tad ši funkcija jiems labai naudinga.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="6f5f8-109">Kryžminis pardavimas ir papildomas pardavimas netgi gali būti naudojami siekiant padėti klientams surasti papildomų produktų, kurių iš pradžių jie net neketino pirkti.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="6f5f8-110">Naudojant rekomendacijas padėti aptikti produktų, jomis galima sukurti daugiau konvertavimo galimybių, padėti padidinti įplaukas ir netgi padėti padidinti klientų pasitenkinimą bei išsaugojimą.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="6f5f8-111">„Commerce“ produktų rekomendacijoms plačiai naudojama „Microsoft“ rekomendacijų mašininio mokymo technologijų platforma.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="6f5f8-112">Scenarijai</span><span class="sxs-lookup"><span data-stu-id="6f5f8-112">Scenarios</span></span>

<span data-ttu-id="6f5f8-113">Produktų rekomendacijos pasiekiamos toliau nurodytais scenarijais:</span><span class="sxs-lookup"><span data-stu-id="6f5f8-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="6f5f8-114">**Bet kuriame parduotuvės naršymo puslapyje ar nukreipimo puslapyje el. prekyboje:** Jei klientai arba parduotuvės partneriai lankosi parduotuvės puslapyje, rekomendacijų mechanizmas gali siūlyti produktus iš sąrašų **Nauja**, **Perkamiausi** ir **Populiaru**.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="6f5f8-115">**Produkto išsamios informacijos puslapyje:** Jei klientai ar parduotuvės partneriai apsilanko puslapyje **Produkto išsami informacija**, rekomendacijos mechanizmas pasiūlys papildomas prekes, kurios taip pat gali būti perkamos.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="6f5f8-116">Šie elementai rodomi sąraše **Žmonėms taip pat patiko**.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="6f5f8-117">**Operacijų puslapyje arba pirkimo užbaigimo puslapyje:** rekomendacijų mechanizmas siūlo prekių pagal visų prekių krepšelyje sąrašą.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="6f5f8-118">Šios prekės rodomos sąraše **Dažnai kartu perkama**.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="6f5f8-119">Rekomendacijų paslauga</span><span class="sxs-lookup"><span data-stu-id="6f5f8-119">Recommendation service</span></span>

<span data-ttu-id="6f5f8-120">Produktų rekomendacijoms naudojamos rekomendacijų mašininio mokymo technologijos šiais būdais:</span><span class="sxs-lookup"><span data-stu-id="6f5f8-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="6f5f8-121">Rekomendavimo paslaugai reikiamu formatu pateikti duomenys ištraukiami iš „Commerce“ operacinės duomenų bazės ir siunčiami į objekto parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="6f5f8-122">Rekomendavimo paslaugai naudojami duomenys, skirti mokyti rekomendavimo modelius sąrašams **Žmonėms taip pat patiko**, **Dažnai kartu perkama**, **Nauja**, **Perkamiausi** ir **Populiaru**.</span><span class="sxs-lookup"><span data-stu-id="6f5f8-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f5f8-123">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6f5f8-123">Additional resources</span></span>

[<span data-ttu-id="6f5f8-124">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="6f5f8-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6f5f8-125">Kurti kuruojamus produktų rekomendacijų sąrašus</span><span class="sxs-lookup"><span data-stu-id="6f5f8-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="6f5f8-126">Tvarkyti AI-ML pagrįstų produktų rekomendacijų rezultatus</span><span class="sxs-lookup"><span data-stu-id="6f5f8-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="6f5f8-127">ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius</span><span class="sxs-lookup"><span data-stu-id="6f5f8-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
