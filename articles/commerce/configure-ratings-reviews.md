---
title: Įvertinimų ir atsiliepimų konfigūravimas
description: Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5161755b9e15e93fbb5eeb6404ea0820f7068ea7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796080"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="9a93f-103">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9a93f-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a93f-104">Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.</span><span class="sxs-lookup"><span data-stu-id="9a93f-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9a93f-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="9a93f-105">Overview</span></span>

<span data-ttu-id="9a93f-106">El. prekybos svetainėse nurodyti įverčiai ir apžvalgos klientams padeda sužinoti apie produktus prieš priimant pirkimo sprendimą, nes jiems parodo, ką apie tuos produktus mano kiti klientai.</span><span class="sxs-lookup"><span data-stu-id="9a93f-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="9a93f-107">El. prekybos svetainėse įverčiai ir apžvalgos taip pat yra mechanizmas klientų atsiliepimams apie produktus rinkti.</span><span class="sxs-lookup"><span data-stu-id="9a93f-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="9a93f-108">Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos</span><span class="sxs-lookup"><span data-stu-id="9a93f-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="9a93f-109">Įverčių ir apžvalgų konfigūravimo reikšmės, pvz., nuomotojo ID, apžvalgos teksto ilgis ir apžvalgos pavadinimo ilgis, konfigūruojamos svetainės lygiu.</span><span class="sxs-lookup"><span data-stu-id="9a93f-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="9a93f-110">Norėdami sukonfigūruoti svetainę, kad būtų rodomi įverčiai ir apžvalgos, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9a93f-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="9a93f-111">Nueikite į **Pradžia \> Svetainės**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="9a93f-112">Pasirinkite savo svetainės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9a93f-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="9a93f-113">Eiti į **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="9a93f-114">Lauke **Maks. apžvalgos teksto ilgis** įveskite maksimalų galimą apžvalgos teksto simbolių skaičių (pavyzdžiui, **1000**).</span><span class="sxs-lookup"><span data-stu-id="9a93f-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="9a93f-115">Lauke **Maks. apžvalgos pavadinimo ilgis** įveskite maksimalų galimą apžvalgos pavadinimų simbolių skaičių (pavyzdžiui, **55**).</span><span class="sxs-lookup"><span data-stu-id="9a93f-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="9a93f-116">Pasirinkite **Įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="9a93f-117">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="9a93f-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="9a93f-119">Produkto įverčio susiejimas su PIIP skyriumi Apžvalgos</span><span class="sxs-lookup"><span data-stu-id="9a93f-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="9a93f-120">Produkto įvertis rodomas po produkto pavadinimu PIIP viršuje.</span><span class="sxs-lookup"><span data-stu-id="9a93f-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="9a93f-121">Galima sukonfigūruoti, kad produkto įvertis būtų susietas su to paties PIIP skyriumi **Apžvalgos**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="9a93f-122">Norėdami produkto įvertį susieti su PIIP skyriumi **Apžvalgos**, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9a93f-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="9a93f-123">Atidarykite PIIP šabloną.</span><span class="sxs-lookup"><span data-stu-id="9a93f-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="9a93f-124">Nueikite į **Pirkimo langelio konteinerio modulių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="9a93f-125">Dalyje **Pirkimo langelis** pasirinkite **Produktų įverčiai**, tada pažymėkite žymės langelį **Spustelėjimą susieti su visų apžvalgų moduliu**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="9a93f-126">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="9a93f-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Produkto įverčio susiejimas su PIIP skyriumi Apžvalgos](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="9a93f-128">Privatumo ir strategijų puslapio saito konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9a93f-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="9a93f-129">Norėdami sukonfigūruoti privatumo ir strategijų puslapio saitą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9a93f-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="9a93f-130">Nueikite į **Pradžia \> Svetainės**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="9a93f-131">Pasirinkite savo svetainės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="9a93f-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="9a93f-132">Eiti į **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="9a93f-133">Skirtuko **Maršrutai** dalyje **RNR privatumas ir strategija** pasirinkite **Įtraukti saitą**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="9a93f-134">Jei saitas jau įvestas ir norite jį pakeisti, jį pasirinkite.</span><span class="sxs-lookup"><span data-stu-id="9a93f-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="9a93f-135">Dialogo lange **Saito įtraukimas** pasirinkite privatumo ir strategijos puslapio saitą ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="9a93f-136">Pasirinkite **Įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="9a93f-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="9a93f-137">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="9a93f-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Privatumo ir strategijų puslapio saito konfigūravimas](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="9a93f-139">Įvertinimų ir atsiliepimų modulių produkto informacijos puslapiuose konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9a93f-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="9a93f-140">Informacijos, kaip konfigūruoti įvertinimus ir atsiliepimų modulius produkto informacijos puslapiuose, žr. [Įvertinimų ir atsiliepimų moduliai](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="9a93f-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a93f-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9a93f-141">Additional resources</span></span>

[<span data-ttu-id="9a93f-142">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="9a93f-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="9a93f-143">Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite</span><span class="sxs-lookup"><span data-stu-id="9a93f-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="9a93f-144">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="9a93f-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="9a93f-145">Įvertinimų ir atsiliepimų modulių produkto informacijos puslapiuose konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9a93f-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="9a93f-146">Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“</span><span class="sxs-lookup"><span data-stu-id="9a93f-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]