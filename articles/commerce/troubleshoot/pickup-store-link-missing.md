---
title: Parinktis „Paimti” neatsiranda krepšelio arba produkto informacijos puslapyje
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai paėmimo iš parduotuvės parinktis neatsiranda krepšelio arba produkto informacijos puslapyje.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585444"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="e1abb-103">Parinktis „Paimti” neatsiranda krepšelio arba produkto informacijos puslapyje</span><span class="sxs-lookup"><span data-stu-id="e1abb-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1abb-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai paėmimo iš parduotuvės parinktis neatsiranda krepšelio arba produkto informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e1abb-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="e1abb-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="e1abb-105">Description</span></span>

<span data-ttu-id="e1abb-106">Mygtukas **Paimti** neatsiranda krepšelio arba produkto informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e1abb-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="e1abb-107">Šioje iliustracijoje pateikiamas puslapio, kuriame yra mygtukas **Paimti**, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e1abb-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Mygtukas Paimti](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="e1abb-109">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="e1abb-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="e1abb-110">Įgalinti BOPIS plėtinį „Commerce” svetainių daryklėje</span><span class="sxs-lookup"><span data-stu-id="e1abb-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="e1abb-111">Norėdami įgalinti plėtinį „Pirkti internetu, paimti parduotuvėje” (BOPIS) „Commerce” svetainių daryklėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e1abb-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="e1abb-112">Pasirinkite jūsų svetainę.</span><span class="sxs-lookup"><span data-stu-id="e1abb-112">Select your site.</span></span>
1. <span data-ttu-id="e1abb-113">Pasirinkite **Svetainės parametrai**, tada – **Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="e1abb-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="e1abb-114">Įsitikinkite, kad parinktis **Išjungti BOPIS** išvalyta.</span><span class="sxs-lookup"><span data-stu-id="e1abb-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="e1abb-115">Pristatymo būdų konfigūravimas „Commerce Headquarters”</span><span class="sxs-lookup"><span data-stu-id="e1abb-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="e1abb-116">Norėdami konfigūruoti pristatymo būdus „Commerce Headquarters“, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="e1abb-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e1abb-117">Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Pristatymo būdai**.</span><span class="sxs-lookup"><span data-stu-id="e1abb-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="e1abb-118">Įsitikinkite, kad sukurtas pristatymo būdas **Kliento paėmimas** ir jam priskirti produktai bei adresai.</span><span class="sxs-lookup"><span data-stu-id="e1abb-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="e1abb-119">Eikite į **„Retail” ir „Commerce” \> „Headquarters” sąranka \> Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e1abb-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="e1abb-120">Kairiojoje naršymo srityje pasirinkite **Kliento užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="e1abb-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="e1abb-121">Įsitikinkite, kad **Pristatymo paėmimo būdas** tinkamai sukonfigūruotas.</span><span class="sxs-lookup"><span data-stu-id="e1abb-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="e1abb-122">Kliento užsakymų mokėjimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e1abb-122">Configure customer orders payments</span></span>

<span data-ttu-id="e1abb-123">Norėdami konfigūruoti kliento užsakymų mokėjimus „Commerce Headquarters“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e1abb-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e1abb-124">Eikite į **„Retail” ir „Commerce” \> „Headquarters” sąranka \> Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e1abb-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="e1abb-125">Kairiojoje naršymo srityje pasirinkite **Kliento užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="e1abb-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="e1abb-126">„FastTab” **Mokėjimai** įsitikinkite, kad laukai **Mokėjimo sąlygos** ir **Mokėjimo būdas** nustatyti teisingai.</span><span class="sxs-lookup"><span data-stu-id="e1abb-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1abb-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e1abb-127">Additional resources</span></span>

[<span data-ttu-id="e1abb-128">BOPIS konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e1abb-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="e1abb-129">Įjungti keletą paėmimo pristatymo režimų kliento užsakymams</span><span class="sxs-lookup"><span data-stu-id="e1abb-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="e1abb-130">Daugiakanaliai „Commerce“ užsakymų mokėjimai</span><span class="sxs-lookup"><span data-stu-id="e1abb-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="e1abb-131">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="e1abb-131">Store selector module</span></span>](../store-selector.md)
