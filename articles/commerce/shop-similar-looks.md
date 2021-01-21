---
title: Įjungti „apsipirkti panašia mada“ rekomendacijas
description: Šis skyrius aprašo, kaip įjungti „apsipirkti panašia mada“ produkto rekomendacijas „Microsoft Dynamics 365 Commerce“.
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818379"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="d14ab-103">Įjungti „apsipirkti panašia mada“ rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d14ab-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d14ab-104">Šis skyrius aprašo, kaip įjungti „apsipirkti panašia mada“ produkto rekomendacijas „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="d14ab-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d14ab-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="d14ab-105">Overview</span></span>

<span data-ttu-id="d14ab-106">„Apsipirkti panašia mada“ rekomendacijų funkcija „Dynamics 365 Commerce“ naudoja dirbtinio intelekto galias ir mašinos mokymosi (AI-ML) tam, kad klientams pristatytų vizualiai panašių produktų rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="d14ab-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="d14ab-107">Įjungus „apsipirkti panašia mada“ rekomendacijas prieinamas visiems mažmeniniams kanalams prekyboje, pardavėjai gali padidinti klientų pasitenkinimą padėdami jiems paprasčiau surasti jų norimas prekes.</span><span class="sxs-lookup"><span data-stu-id="d14ab-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="d14ab-108">„Apsipirkti panašia mada“ funkcijos rekomendacijos naudoja pagrindinių produkto variantų produkto paveiksėlius tam, kad surastų ir rekomenduotų vizualiai panašius produktus iš prekybininko produkto katalogo.</span><span class="sxs-lookup"><span data-stu-id="d14ab-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="d14ab-109">„Apsipirkti panašia mada“ rekomendacijos yra prieinamas tiek prekybos vietoje (POS), tiek ir el. prekybos patirtyse.</span><span class="sxs-lookup"><span data-stu-id="d14ab-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="d14ab-110">Scenarijų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="d14ab-110">Example scenarios</span></span>

- <span data-ttu-id="d14ab-111">Klientas peržiūri juodą dryžuotą megztinį ir gauna panašaus raudono megztinio rekomendaciją.</span><span class="sxs-lookup"><span data-stu-id="d14ab-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="d14ab-112">Klientas pasirenka rekomenduojamą produktą, o ne originaliai peržiūrėtą produktą ir tuomet gauna panašių raudonų produktų rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="d14ab-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="d14ab-113">Klientas naudoja „apsipirkti panašia mada“ rekomendacijas tam, kad atrastų prie žiedo tinkančius auskarus, kuriuos jis nori įsigyti.</span><span class="sxs-lookup"><span data-stu-id="d14ab-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="d14ab-114">Įjungti „apsipirkti panašia mada“ rekomendacijas prekybos štabe</span><span class="sxs-lookup"><span data-stu-id="d14ab-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="d14ab-115">Produkto rekomendacijas palaiko tik prekybos vartotojai, kurie perkėlė savo atsargas į „Azure Data Lake Gen2“.</span><span class="sxs-lookup"><span data-stu-id="d14ab-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="d14ab-116">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="d14ab-116">Prerequisites</span></span>

<span data-ttu-id="d14ab-117">Prieš tai, kai pardavėjai gali pradėti rodyti „apsipirkti panašia mada“ rekomendacijas klientams, jie turi atlikti du išankstinių sąlygų žingsnius:</span><span class="sxs-lookup"><span data-stu-id="d14ab-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="d14ab-118">[Įjungti produkto rekomendacijas](enable-product-recommendations.md) prekybos štabe.</span><span class="sxs-lookup"><span data-stu-id="d14ab-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="d14ab-119">Patvirtinti, kad medijos serveris palaiko HTTPS skambučius.</span><span class="sxs-lookup"><span data-stu-id="d14ab-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="d14ab-120">Rekmendacijos variklio prieigai prie produkto paveikslėlių, prekybininkai turi sukurti produkto URL.</span><span class="sxs-lookup"><span data-stu-id="d14ab-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="d14ab-121">Produkto URL sukūrimui prekybos štabe, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="d14ab-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d14ab-122">Eikite į **Produkto paveikslėlius**.</span><span class="sxs-lookup"><span data-stu-id="d14ab-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="d14ab-123">Veiksmų juostoje pasirinkite **Nustatyti medijos šabloną**.</span><span class="sxs-lookup"><span data-stu-id="d14ab-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="d14ab-124">**Nustatyti medijso šabloną** ypatybių juostoje, **Medijos URL** pasirinkite **Kurti URL**.</span><span class="sxs-lookup"><span data-stu-id="d14ab-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="d14ab-125">Jums įjungiant „apsipirkti panašia mada“ rekomendacijos funkciją, pradedamas produkto rekomendacijų sąrašo kūrimas.</span><span class="sxs-lookup"><span data-stu-id="d14ab-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="d14ab-126">Gali reikėti atnaujinti prieš tai, kai šie sąrašai bus prieinami ir matomi internete bei POS terminaluose.</span><span class="sxs-lookup"><span data-stu-id="d14ab-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="d14ab-127">Tam, kad įjungtumėte „apsipirkti panašia mada“ rekomendacijas prekybos štabe, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="d14ab-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d14ab-128">Eikite į **Funkcijos valdymą**.</span><span class="sxs-lookup"><span data-stu-id="d14ab-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="d14ab-129">Prieinamų funkcijų sąraše ieškokite ir pasirinkite **Apsipirkti panašia mada**.</span><span class="sxs-lookup"><span data-stu-id="d14ab-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="d14ab-130">Dešinėje juostoje pasirinkite **Įjungti** tam, kad įjungtumėte paslaugą.</span><span class="sxs-lookup"><span data-stu-id="d14ab-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="d14ab-131">Tolesnis paveikslėlis rodo **Apsipirkti panšia mada** funkciją **Funkcijų valdymo** puslapyje prekybos štabe.</span><span class="sxs-lookup"><span data-stu-id="d14ab-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Apsipirkti panašia mada funkcija funkcijų valdymo puslapyje prekybos štabe](./media/enableshopsimilarlooks.png)

<span data-ttu-id="d14ab-133">Užbaigus prieš tai aprašytus veiksmus, POS terminalai automatiškai praplečiami su teksto **Apsipirkti panašia mada** juosta.</span><span class="sxs-lookup"><span data-stu-id="d14ab-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="d14ab-134">Pasirinkę **Matyti daugiau**, POS terminalo vartotojai gali būti nuvest į paskirtą „apsipirkti panašia mada“ puslapį, kuris gali būti filtruojamas toliau.</span><span class="sxs-lookup"><span data-stu-id="d14ab-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="d14ab-135">Jei išjungiate „apsipirkti panašia mada“ rekomendacijų funkciją, jokie kiti produkto rekomendacijų tipai nebus paveikti.</span><span class="sxs-lookup"><span data-stu-id="d14ab-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="d14ab-136">Dėl išsamesnės informacijos apie produkto rekomendacijas, žr. [Produkto rekomendacijų apžvalga](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d14ab-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="d14ab-137">Įtraukite apsipirkti panašia mada mygtuką į produkto išsamios informacijos puslapį naudodami komercijos vietos kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="d14ab-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="d14ab-138">Jums įjungus „apsipirkti panašia mada“ rekomendacijų funkciją prekybos štabe, prekybos vietos kūrimo įrankio parinktis leidžia prekybininkui įtraukti **Apsipirkti panašia mada** mygtuką į įsigijimo laukelį bet kurio produkto išsamios informacijos puslapyje (PDP).</span><span class="sxs-lookup"><span data-stu-id="d14ab-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="d14ab-139">Klientas nustatęs šį mygtuką yra nuvedamas į paskirtą „apsipirkti panašia mada“ puslapį, kuris grįžta prie vizualiai panašių produktų.</span><span class="sxs-lookup"><span data-stu-id="d14ab-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="d14ab-140">Ten klientas gali naudoti selektorius tolesniam produktų filtravimui.</span><span class="sxs-lookup"><span data-stu-id="d14ab-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="d14ab-141">Tam, kad įtrauktumėte **Apsipirkti panašia mada** mygtuką į PDP naudodami prekybos vietos kūrimo įrankį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d14ab-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d14ab-142">Atverkite esantį vietos kūrimo įrankio puslapį, turintį įsigijimo laukelio modulį.</span><span class="sxs-lookup"><span data-stu-id="d14ab-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="d14ab-143">Kairėje naršymo juostoje pasirinkite įsigijimo laukelio modulį.</span><span class="sxs-lookup"><span data-stu-id="d14ab-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="d14ab-144">Dešinėje naršymo juostoje, pasirinkite **Įjungti apsipirkimą panašia mada nuroodą** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="d14ab-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="d14ab-145">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="d14ab-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="d14ab-146">Po to, kai puslapis yra išpublikuotas, PDP apims **Apsipirkti panašia mada** mygtuką.</span><span class="sxs-lookup"><span data-stu-id="d14ab-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="d14ab-147">Toliau pateiktas paveikslėlis rodo **Apsipirkti panašia mada nuorodos įjungimo** žymimą laukelį ir **Apsipirkti panašia mada** mygtuką PDP pavyzdyje vietos kūrimo įrankyje.</span><span class="sxs-lookup"><span data-stu-id="d14ab-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![Apsipirkti panašia mada nuorodos žymimas laukelis ir apsipirkti panašia mada mygtukas PDP vietos kūrimo įrankyje](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="d14ab-149">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d14ab-149">Additional resources</span></span>

[<span data-ttu-id="d14ab-150">Produktų rekomendacijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="d14ab-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d14ab-151">„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="d14ab-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d14ab-152">Įjungti produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d14ab-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d14ab-153">Personalizuotų rekomendacijų atsisakymas</span><span class="sxs-lookup"><span data-stu-id="d14ab-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d14ab-154">Produktų rekomendacijų įtraukimas į EKA</span><span class="sxs-lookup"><span data-stu-id="d14ab-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d14ab-155">Rekomendacijų įtraukimas į operacijų ekraną</span><span class="sxs-lookup"><span data-stu-id="d14ab-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d14ab-156">AI-ML rekomendacijų rezultatų koregavimas</span><span class="sxs-lookup"><span data-stu-id="d14ab-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d14ab-157">Kuruojamų rekomendacijų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="d14ab-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d14ab-158">Rekomendacijų su demonstraciniais duomenimis kūrimas</span><span class="sxs-lookup"><span data-stu-id="d14ab-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d14ab-159">DUK apie produktų rekomendacijas</span><span class="sxs-lookup"><span data-stu-id="d14ab-159">Product recommendations FAQ</span></span>](faq-recommendations.md)