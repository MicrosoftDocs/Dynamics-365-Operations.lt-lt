---
title: Pristatymo parinkčių modulis
description: Ši tema paaiškina pristatymo parinkčių modulius ir tai, kaip juos sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 8342afefa6eeda3a53decb39caddb62d1e4e1963
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270866"
---
# <a name="delivery-options-module"></a><span data-ttu-id="1ac2b-103">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ac2b-104">Ši tema paaiškina pristatymo parinkčių modulius ir tai, kaip juos sukonfigūruoti „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1ac2b-105">Pristatymo parinkčių moduliai leidžia klientams pasirinkti pristatymo būdą, tokį kaip siuntimas ar paėmimas pagal jų interneto užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="1ac2b-106">Siuntimo adresas būtinas siekiant nustatyti pristatymo būdą.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="1ac2b-107">Jei siuntimo adresas pasikeitė, pristatymo parinktys turi būti dar kartą gautos.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="1ac2b-108">Jei užsakyme yra tik prekės pakuojamos parduotuvėje, šis modulis yra automatiškai paslepiamas.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="1ac2b-109">Dėl informacijos apie tai, kaip sukonfigūruoti pristatymo būdus, žr. [Interneto kanalo nustatymai](channel-setup-online.md) ir [Pristatymo būdų nustatymas](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="1ac2b-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="1ac2b-110">Visi pristatymo būdai gali turėti susietą mokestį.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="1ac2b-111">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti mokesčius interneto parduotuvėje, žr. [Omni kanalo papildomi automatiniai mokesčiai](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="1ac2b-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="1ac2b-112">10.0.13 komercijos versijoje pristatymo parinkčių modulis buvo atnaujintas taip, kad palaikytų **Antraštės mokesčiai be paskirstymo** ir **Siuntimas kaip eilutės mokestis** funkcijas.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="1ac2b-113">Jei paskirstymas yra išjungtas, tikimasi, kad el. prekybos darbo srautas neleis maišyti pristatymo būdo prekėms vežimėlyje (tai yra, kai kurios prekės yra pasirinktos siuntimui, tačiau kitos yra pasirinktos paėmimui).</span><span class="sxs-lookup"><span data-stu-id="1ac2b-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="1ac2b-114">**Antraštės mokesčio paskirstymo** funkcija reikalauja, kad **Nuolatinio pristatymo būdo tvarkymo kanale įjungimas** vėliava būtų įjungta prekybos štabe.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="1ac2b-115">Kai vėliavos funkcija yra įjungta, siuntimo mokesčiai bus taikomi antraštės lygmeniu ar eilutės lygmeniu priklausomai nuo „Commerce“ štabo konfigūravimo.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="1ac2b-116">„Fabrikam“ tema palaiko maišytą pristatymo būdą, kai kai kurios prekės yra parinktos siuntimui, o kitos parinktos paėmimui.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="1ac2b-117">Šiame būde, siuntimo mokesčiai bus paskirstyti visoms prekėms, kurios yra parinktos siuntimo pristatymo būdui.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="1ac2b-118">Maišytam pristatymo į darbą būdui, pirmiausia turite sukonfigūruoti **Antraštės mokesčiai su paskirstymu** funkciją komercijos štabe.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="1ac2b-119">Dėl platesnės informacijos apie šį konfigūravimą, žr. [Atidėti antraštės mokesčius atitikimui su prekybos eilutėmis](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="1ac2b-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="1ac2b-120">Jei siuntimo mokesčiai taikomi eilutės prekėms, jos gali būti rodomos kiekvienos prekės vežimėlio eilutėje.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="1ac2b-121">Ši funkcija reikalauja, kad **Rodyti siuntimo mokesčius eilutės prekei** ypatybė būtų įjungti tiek vežimėlio moduliui tik ir galutiniam moduliui.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="1ac2b-122">Dėl platesnės informacijos, žr. [Vežimėlio modulis](add-cart-module.md) ir [Galutinis modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="1ac2b-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="1ac2b-123">Tolesnis paveikslėlis rodo pristatymo parinkčių modulį galutiniame puslapyje pavyzdį.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Pristatymo parinkčių modulio galutiniame puslapyje pavyzdys](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="1ac2b-125">Pristatymo parinkčių modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="1ac2b-125">Delivery options module properties</span></span>

| <span data-ttu-id="1ac2b-126">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="1ac2b-126">Property</span></span> | <span data-ttu-id="1ac2b-127">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="1ac2b-127">Values</span></span> | <span data-ttu-id="1ac2b-128">aprašymas</span><span class="sxs-lookup"><span data-stu-id="1ac2b-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="1ac2b-129">Antraštė</span><span class="sxs-lookup"><span data-stu-id="1ac2b-129">Heading</span></span> | <span data-ttu-id="1ac2b-130">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**)</span><span class="sxs-lookup"><span data-stu-id="1ac2b-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1ac2b-131">Pasirenkama antraštė pristatymo parinkčių moduliui.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="1ac2b-132">Pasirinktinis CSS klasės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="1ac2b-132">Custom CSS class name</span></span> | <span data-ttu-id="1ac2b-133">Tekstas</span><span class="sxs-lookup"><span data-stu-id="1ac2b-133">Text</span></span> | <span data-ttu-id="1ac2b-134">Tinkinto kaskadinio stiliaus lapų (CSS) klasės pavadinimas, kuris bus naudojamas šio modulio sukūrimui, jei taikomas.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="1ac2b-135">Pristatymo būdo filtro parinktis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="1ac2b-136">**Nefiltruoti** ar **Nesiųsti būdai**</span><span class="sxs-lookup"><span data-stu-id="1ac2b-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="1ac2b-137">Vertė, kuri nurodo, ar pristatymo parinkčių modulis turėtų filtruoti visus nesiunčiamus pristatymo būdus.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="1ac2b-138">Automatiškai pasirinkti pristatymo pasirinktį</span><span class="sxs-lookup"><span data-stu-id="1ac2b-138">Auto select a delivery option</span></span> | <span data-ttu-id="1ac2b-139">**Nefiltruoti** , **automatiškai pasirinkti pristatymo parinktį, rodyti suvestinę** arba automatiškai pasirinkti pristatymo parinktį ir **nerodyti suvestinės**</span><span class="sxs-lookup"><span data-stu-id="1ac2b-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="1ac2b-140">Ši ypatybė automatiškai pritaiko pirmą galima pristatymo pasirinktį patikrinti nereikalaujant, kad vartotojas ją pasirinktų.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="1ac2b-141">Jis turėtų būti naudojamas tik tada, jei yra viena galima pristatymo pasirinktis.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="1ac2b-142">Ši ypatybė yra palaikoma nuo „Commerce“ versijos 10.0.19 leidimo.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="1ac2b-143">Įtraukite pristatymo parinkčių modulį į galutinį puslapį ir nustatykite reikiamas ypatybes</span><span class="sxs-lookup"><span data-stu-id="1ac2b-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="1ac2b-144">Pristatymo parinkčių modulis gali būti įtrauktas tik į galutinį modulį.</span><span class="sxs-lookup"><span data-stu-id="1ac2b-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="1ac2b-145">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti pristatymo parinkčių modulį ir įtraukti jį į galutinį puslapį, žr. [Galutinis modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="1ac2b-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ac2b-146">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1ac2b-146">Additional resources</span></span>

[<span data-ttu-id="1ac2b-147">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1ac2b-148">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1ac2b-149">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="1ac2b-150">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="1ac2b-151">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="1ac2b-152">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1ac2b-153">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="1ac2b-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="1ac2b-154">Interneto kanalo nustatymas</span><span class="sxs-lookup"><span data-stu-id="1ac2b-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="1ac2b-155">Omni kanalo papildomi automatiniai mokesčiai</span><span class="sxs-lookup"><span data-stu-id="1ac2b-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="1ac2b-156">Paskirstyti antraštės mokesčius tam, kad jie atitiktų prekybos eilutes</span><span class="sxs-lookup"><span data-stu-id="1ac2b-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="1ac2b-157">Nustatyti pristatymo būdus</span><span class="sxs-lookup"><span data-stu-id="1ac2b-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
