---
title: Pristatymo parinkčių modulis
description: Ši tema paaiškina pristatymo parinkčių modulius ir tai, kaip juos sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 9d8945348cbe3255ecc497f129d125ad11e9ceab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000854"
---
# <a name="delivery-options-module"></a><span data-ttu-id="5487f-103">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="5487f-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5487f-104">Ši tema paaiškina pristatymo parinkčių modulius ir tai, kaip juos sukonfigūruoti „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="5487f-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5487f-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="5487f-105">Overview</span></span>

<span data-ttu-id="5487f-106">Pristatymo parinkčių moduliai leidžia klientams pasirinkti pristatymo būdą, tokį kaip siuntimas ar paėmimas pagal jų interneto užsakymą.</span><span class="sxs-lookup"><span data-stu-id="5487f-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="5487f-107">Siuntimo adresas būtinas siekiant nustatyti pristatymo būdą.</span><span class="sxs-lookup"><span data-stu-id="5487f-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="5487f-108">Jei siuntimo adresas pasikeitė, pristatymo parinktys turi būti dar kartą gautos.</span><span class="sxs-lookup"><span data-stu-id="5487f-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="5487f-109">Jei užsakyme yra tik prekės pakuojamos parduotuvėje, šis modulis yra automatiškai paslepiamas.</span><span class="sxs-lookup"><span data-stu-id="5487f-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="5487f-110">Dėl informacijos apie tai, kaip sukonfigūruoti pristatymo būdus, žr. [Interneto kanalo nustatymai](channel-setup-online.md) ir [Pristatymo būdų nustatymas](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="5487f-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="5487f-111">Visi pristatymo būdai gali turėti susietą mokestį.</span><span class="sxs-lookup"><span data-stu-id="5487f-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="5487f-112">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti mokesčius interneto parduotuvėje, žr. [Omni kanalo papildomi automatiniai mokesčiai](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="5487f-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="5487f-113">10.0.13 komercijos versijoje pristatymo parinkčių modulis buvo atnaujintas taip, kad palaikytų **Antraštės mokesčiai be paskirstymo** ir **Siuntimas kaip eilutės mokestis** funkcijas.</span><span class="sxs-lookup"><span data-stu-id="5487f-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="5487f-114">Jei paskirstymas yra išjungtas, tikimasi, kad el. prekybos darbo srautas neleis maišyti pristatymo būdo prekėms vežimėlyje (tai yra, kai kurios prekės yra pasirinktos siuntimui, tačiau kitos yra pasirinktos paėmimui).</span><span class="sxs-lookup"><span data-stu-id="5487f-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="5487f-115">**Antraštės mokesčio paskirstymo** funkcija reikalauja, kad **Nuolatinio pristatymo būdo tvarkymo kanale įjungimas** vėliava būtų įjungta prekybos štabe.</span><span class="sxs-lookup"><span data-stu-id="5487f-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="5487f-116">Kai ta vėliava yra įjungta, siuntimo mokesčiai bus taikomi bet kuriame antraštės lygyje arba eilutės lygyje priklausomai nuo prekybos štabo konfigūravimo.</span><span class="sxs-lookup"><span data-stu-id="5487f-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="5487f-117">„Fabrikam“ tema palaiko maišytą pristatymo būdą, kai kai kurios prekės yra parinktos siuntimui, o kitos parinktos paėmimui.</span><span class="sxs-lookup"><span data-stu-id="5487f-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="5487f-118">Šiame būde, siuntimo mokesčiai bus paskirstyti visoms prekėms, kurios yra parinktos siuntimo pristatymo būdui.</span><span class="sxs-lookup"><span data-stu-id="5487f-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="5487f-119">Maišytam pristatymo į darbą būdui, pirmiausia turite sukonfigūruoti **Antraštės mokesčiai su paskirstymu** funkciją komercijos štabe.</span><span class="sxs-lookup"><span data-stu-id="5487f-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="5487f-120">Dėl platesnės informacijos apie šį konfigūravimą, žr. [Atidėti antraštės mokesčius sutikimuis su prekybos eilutėmis](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="5487f-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="5487f-121">Jei siuntimo mokesčiai taikomi eilutės prekėms, jos gali būti rodomos kiekvienos prekės vežimėlio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="5487f-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="5487f-122">Ši funkcija reikalauja, kad **Rodyti siuntimo mokesčius eilutės prekei** ypatybė būtų įjungti tiek vežimėlio moduliui tik ir galutiniam moduliui.</span><span class="sxs-lookup"><span data-stu-id="5487f-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="5487f-123">Dėl platesnės informacijos, žr. [Vežimėlio modulis](add-cart-module.md) ir [Galutinis modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="5487f-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="5487f-124">Tolesnis paveikslėlis rodo pristatymo parinkčių modulį galutiniame puslapyje pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="5487f-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Pristatymo parinkčių modulio galutiniame puslapyje pavyzdys.](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="5487f-126">Pristatymo parinkčių modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="5487f-126">Delivery options module properties</span></span>

| <span data-ttu-id="5487f-127">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="5487f-127">Property</span></span> | <span data-ttu-id="5487f-128">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="5487f-128">Values</span></span> | <span data-ttu-id="5487f-129">aprašymas</span><span class="sxs-lookup"><span data-stu-id="5487f-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="5487f-130">Antraštė</span><span class="sxs-lookup"><span data-stu-id="5487f-130">Heading</span></span> | <span data-ttu-id="5487f-131">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**)</span><span class="sxs-lookup"><span data-stu-id="5487f-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="5487f-132">Pasirenkama antraštė pristatymo parinkčių moduliui.</span><span class="sxs-lookup"><span data-stu-id="5487f-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="5487f-133">Pasirinktinis CSS klasės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="5487f-133">Custom CSS class name</span></span> | <span data-ttu-id="5487f-134">Tekstas</span><span class="sxs-lookup"><span data-stu-id="5487f-134">Text</span></span> | <span data-ttu-id="5487f-135">Tinkinto kaskadinio stiliaus lapų (CSS) klasės pavadinimas, kuris bus naudojamas šio modulio sukūrimui, jei taikomas.</span><span class="sxs-lookup"><span data-stu-id="5487f-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="5487f-136">Pristatymo būdo filtro parinktis</span><span class="sxs-lookup"><span data-stu-id="5487f-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="5487f-137">**Nefiltruoti** ar **Nesiųsti būdai**</span><span class="sxs-lookup"><span data-stu-id="5487f-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="5487f-138">Vertė, kuri nurodo, ar pristatymo parinkčių modulis turėtų filtruoti visus nesiunčiamus pristatymo būdus.</span><span class="sxs-lookup"><span data-stu-id="5487f-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="5487f-139">Įtraukite pristatymo parinkčių modulį į galutinį puslapį ir nustatykite reikiamas ypatybes</span><span class="sxs-lookup"><span data-stu-id="5487f-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="5487f-140">Pristatymo parinkčių modulis gali būti įtrauktas tik į galutinį modulį.</span><span class="sxs-lookup"><span data-stu-id="5487f-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="5487f-141">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti pristatymo parinkčių modulį ir įtraukti jį į galutinį puslapį, žr. [Galutinis modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="5487f-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5487f-142">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5487f-142">Additional resources</span></span>

[<span data-ttu-id="5487f-143">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="5487f-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5487f-144">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="5487f-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5487f-145">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="5487f-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="5487f-146">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="5487f-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="5487f-147">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="5487f-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="5487f-148">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="5487f-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5487f-149">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="5487f-149">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="5487f-150">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="5487f-150">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="5487f-151">Omni kanalo papildomi automatiniai mokesčiai</span><span class="sxs-lookup"><span data-stu-id="5487f-151">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="5487f-152">Paskirstyti antraštės mokesčius tam, kad jie atitiktų prekybos eilutes</span><span class="sxs-lookup"><span data-stu-id="5487f-152">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="5487f-153">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="5487f-153">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
