---
title: Parinktis „Paimti” neatsiranda krepšelio arba produkto informacijos puslapyje
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai paėmimo iš parduotuvės parinktis neatsiranda krepšelio arba produkto informacijos puslapyje.
author: Reza-Assadi
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
ms.openlocfilehash: 46eeed18bb547035603d7e9a01e8f131a2393f01
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801632"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="dd13e-103">Parinktis „Paimti” neatsiranda krepšelio arba produkto informacijos puslapyje</span><span class="sxs-lookup"><span data-stu-id="dd13e-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd13e-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai paėmimo iš parduotuvės parinktis neatsiranda krepšelio arba produkto informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="dd13e-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="dd13e-105">aprašymas</span><span class="sxs-lookup"><span data-stu-id="dd13e-105">Description</span></span>

<span data-ttu-id="dd13e-106">Mygtukas **Paimti** neatsiranda krepšelio arba produkto informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="dd13e-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="dd13e-107">Šioje iliustracijoje pateikiamas puslapio, kuriame yra mygtukas **Paimti**, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="dd13e-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Mygtukas Paimti](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="dd13e-109">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="dd13e-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="dd13e-110">Įgalinti BOPIS plėtinį „Commerce” svetainių daryklėje</span><span class="sxs-lookup"><span data-stu-id="dd13e-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="dd13e-111">Norėdami įgalinti plėtinį „Pirkti internetu, paimti parduotuvėje” (BOPIS) „Commerce” svetainių daryklėje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dd13e-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="dd13e-112">Pasirinkite jūsų svetainę.</span><span class="sxs-lookup"><span data-stu-id="dd13e-112">Select your site.</span></span>
1. <span data-ttu-id="dd13e-113">Pasirinkite **Svetainės parametrai**, tada – **Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="dd13e-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="dd13e-114">Įsitikinkite, kad parinktis **Išjungti BOPIS** išvalyta.</span><span class="sxs-lookup"><span data-stu-id="dd13e-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="dd13e-115">Pristatymo būdų konfigūravimas „Commerce Headquarters”</span><span class="sxs-lookup"><span data-stu-id="dd13e-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="dd13e-116">Norėdami konfigūruoti pristatymo būdus „Commerce Headquarters“, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="dd13e-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="dd13e-117">Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Sąranka \> Pristatymo būdai**.</span><span class="sxs-lookup"><span data-stu-id="dd13e-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="dd13e-118">Įsitikinkite, kad sukurtas pristatymo būdas **Kliento paėmimas** ir jam priskirti produktai bei adresai.</span><span class="sxs-lookup"><span data-stu-id="dd13e-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="dd13e-119">Eikite į **„Retail” ir „Commerce” \> „Headquarters” sąranka \> Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dd13e-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="dd13e-120">Kairiojoje naršymo srityje pasirinkite **Kliento užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="dd13e-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="dd13e-121">Įsitikinkite, kad **Pristatymo paėmimo būdas** tinkamai sukonfigūruotas.</span><span class="sxs-lookup"><span data-stu-id="dd13e-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="dd13e-122">Kliento užsakymų mokėjimų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="dd13e-122">Configure customer orders payments</span></span>

<span data-ttu-id="dd13e-123">Norėdami konfigūruoti kliento užsakymų mokėjimus „Commerce Headquarters“, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dd13e-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="dd13e-124">Eikite į **„Retail” ir „Commerce” \> „Headquarters” sąranka \> Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="dd13e-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="dd13e-125">Kairiojoje naršymo srityje pasirinkite **Kliento užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="dd13e-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="dd13e-126">„FastTab” **Mokėjimai** įsitikinkite, kad laukai **Mokėjimo sąlygos** ir **Mokėjimo būdas** nustatyti teisingai.</span><span class="sxs-lookup"><span data-stu-id="dd13e-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd13e-127">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dd13e-127">Additional resources</span></span>

[<span data-ttu-id="dd13e-128">BOPIS konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="dd13e-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="dd13e-129">Įjungti keletą paėmimo pristatymo režimų kliento užsakymams</span><span class="sxs-lookup"><span data-stu-id="dd13e-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="dd13e-130">Daugiakanaliai „Commerce“ užsakymų mokėjimai</span><span class="sxs-lookup"><span data-stu-id="dd13e-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="dd13e-131">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="dd13e-131">Store selector module</span></span>](../store-selector.md)
