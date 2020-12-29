---
title: Įvertinimų ir atsiliepimų konfigūravimas
description: Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
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
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414249"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="c80b1-103">Įvertinimų ir atsiliepimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c80b1-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c80b1-104">Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.</span><span class="sxs-lookup"><span data-stu-id="c80b1-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c80b1-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="c80b1-105">Overview</span></span>

<span data-ttu-id="c80b1-106">El. prekybos svetainėse nurodyti įverčiai ir apžvalgos klientams padeda sužinoti apie produktus prieš priimant pirkimo sprendimą, nes jiems parodo, ką apie tuos produktus mano kiti klientai.</span><span class="sxs-lookup"><span data-stu-id="c80b1-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="c80b1-107">El. prekybos svetainėse įverčiai ir apžvalgos taip pat yra mechanizmas klientų atsiliepimams apie produktus rinkti.</span><span class="sxs-lookup"><span data-stu-id="c80b1-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="c80b1-108">Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos</span><span class="sxs-lookup"><span data-stu-id="c80b1-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="c80b1-109">Įverčių ir apžvalgų konfigūravimo reikšmės, pvz., nuomotojo ID, apžvalgos teksto ilgis ir apžvalgos pavadinimo ilgis, konfigūruojamos svetainės lygiu.</span><span class="sxs-lookup"><span data-stu-id="c80b1-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="c80b1-110">Norėdami sukonfigūruoti svetainę, kad būtų rodomi įverčiai ir apžvalgos, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c80b1-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="c80b1-111">Nueikite į **Pradžia \> Svetainės**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="c80b1-112">Pasirinkite savo svetainės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c80b1-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="c80b1-113">Eiti į **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="c80b1-114">Lauke **Maks. apžvalgos teksto ilgis** įveskite maksimalų galimą apžvalgos teksto simbolių skaičių (pavyzdžiui, **1000**).</span><span class="sxs-lookup"><span data-stu-id="c80b1-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="c80b1-115">Lauke **Maks. apžvalgos pavadinimo ilgis** įveskite maksimalų galimą apžvalgos pavadinimų simbolių skaičių (pavyzdžiui, **55**).</span><span class="sxs-lookup"><span data-stu-id="c80b1-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="c80b1-116">Pasirinkite **Įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="c80b1-117">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c80b1-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="c80b1-119">Produkto įverčio susiejimas su PIIP skyriumi Apžvalgos</span><span class="sxs-lookup"><span data-stu-id="c80b1-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="c80b1-120">Produkto įvertis rodomas po produkto pavadinimu PIIP viršuje.</span><span class="sxs-lookup"><span data-stu-id="c80b1-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="c80b1-121">Galima sukonfigūruoti, kad produkto įvertis būtų susietas su to paties PIIP skyriumi **Apžvalgos**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="c80b1-122">Norėdami produkto įvertį susieti su PIIP skyriumi **Apžvalgos**, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c80b1-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="c80b1-123">Atidarykite PIIP šabloną.</span><span class="sxs-lookup"><span data-stu-id="c80b1-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="c80b1-124">Nueikite į **Pirkimo langelio konteinerio modulių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="c80b1-125">Dalyje **Pirkimo langelis** pasirinkite **Produktų įverčiai**, tada pažymėkite žymės langelį **Spustelėjimą susieti su visų apžvalgų moduliu**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="c80b1-126">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c80b1-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Produkto įverčio susiejimas su PIIP skyriumi Apžvalgos](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="c80b1-128">Privatumo ir strategijų puslapio saito konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c80b1-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="c80b1-129">Norėdami sukonfigūruoti privatumo ir strategijų puslapio saitą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c80b1-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="c80b1-130">Nueikite į **Pradžia \> Svetainės**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="c80b1-131">Pasirinkite savo svetainės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="c80b1-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="c80b1-132">Eiti į **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="c80b1-133">Skirtuko **Maršrutai** dalyje **RNR privatumas ir strategija** pasirinkite **Įtraukti saitą**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="c80b1-134">Jei saitas jau įvestas ir norite jį pakeisti, jį pasirinkite.</span><span class="sxs-lookup"><span data-stu-id="c80b1-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="c80b1-135">Dialogo lange **Saito įtraukimas** pasirinkite privatumo ir strategijos puslapio saitą ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="c80b1-136">Pasirinkite **Įrašyti ir publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="c80b1-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="c80b1-137">Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c80b1-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Privatumo ir strategijų puslapio saito konfigūravimas](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="c80b1-139">Įvertinimų ir atsiliepimų modulių produkto informacijos puslapiuose konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c80b1-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="c80b1-140">Informacijos, kaip konfigūruoti įvertinimus ir atsiliepimų modulius produkto informacijos puslapiuose, žr. [Įvertinimų ir atsiliepimų moduliai](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="c80b1-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c80b1-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c80b1-141">Additional resources</span></span>

[<span data-ttu-id="c80b1-142">Įvertinimų ir atsiliepimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="c80b1-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="c80b1-143">Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite</span><span class="sxs-lookup"><span data-stu-id="c80b1-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="c80b1-144">Įvertinimų ir atsiliepimų tvarkymas</span><span class="sxs-lookup"><span data-stu-id="c80b1-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="c80b1-145">Įvertinimų ir atsiliepimų modulių produkto informacijos puslapiuose konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="c80b1-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="c80b1-146">Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“</span><span class="sxs-lookup"><span data-stu-id="c80b1-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
