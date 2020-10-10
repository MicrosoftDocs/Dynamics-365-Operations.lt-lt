---
title: Mokėjimo modulis
description: Ši tema paaiškina mokėjimo modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4267391edaf70ec645933b2c5c08a72735f52894
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818331"
---
# <a name="payment-module"></a><span data-ttu-id="54a7a-103">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="54a7a-103">Payment module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="54a7a-104">Ši tema paaiškina mokėjimo modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="54a7a-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="54a7a-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="54a7a-105">Overview</span></span>

<span data-ttu-id="54a7a-106">Mokėjimo modulis leidžia klientui sumokėti už užsakymus naudojant kredito ar debeto korteles.</span><span class="sxs-lookup"><span data-stu-id="54a7a-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="54a7a-107">Mokėjimo papildymas šiam moduliui yra pateiktas „Dynamics 365 Payment Connector“ „Adyen“.</span><span class="sxs-lookup"><span data-stu-id="54a7a-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="54a7a-108">Dėl išsamesnės informacijos, kaip nustatyti ir konfigūruoti mokėjimo jungtį, žr. [„Dynamics 365 Payment Connector“ „Adyen“](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="54a7a-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="54a7a-109">Mokėjimo modulis talpina mokėjimo informaciją, kuri yra laikoma per „Ayden“ HTML vidaus rėmuose (iframe).</span><span class="sxs-lookup"><span data-stu-id="54a7a-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="54a7a-110">Mokėjimo modulis sąveikauja su „Commerce Scale Unit“ tam, kad gautų „Adyen“ mokėjimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="54a7a-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="54a7a-111">Kaip dalis sąveikos su „Commerce Scale Unit”, mokėjimo modulis gali leisti, kad sąskaitos adreso informacija būtų naudojama kaip „iframe“ arba atskiras modulis.</span><span class="sxs-lookup"><span data-stu-id="54a7a-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="54a7a-112">„Fabrikam“ temoje mokėjimo adresas yra rodomas atskirame modulyje.</span><span class="sxs-lookup"><span data-stu-id="54a7a-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="54a7a-113">Ši prieiga leidžia lanksčiau formatuoti, nes adreso eilutės gali būti sukurtos taip, kad atspindetų siuntimo adreso eilutes.</span><span class="sxs-lookup"><span data-stu-id="54a7a-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="54a7a-114">Mokėjimo modulis taip pat leidžia prisijungusiems klientams įrašyti jų mokėjimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="54a7a-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="54a7a-115">Mokėjimo informacija ir sąskaitų adresai yra įrašomi ir valdomi per „Adyen“ mokėjimo jungtį.</span><span class="sxs-lookup"><span data-stu-id="54a7a-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="54a7a-116">Mokėjimo modulis apima visus mokesčius, kurie nėra apimti lojalumo taškų ar dovanų kortelės.</span><span class="sxs-lookup"><span data-stu-id="54a7a-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="54a7a-117">Jei bendra užsakymo suuma yra visiškai padengiama lojalumo taškais ar dovanų kortelės kreditu, mokėjimo modulis bus paslėptas ir klientas galės be jo pateikti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="54a7a-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="54a7a-118">„Adyen“ mokėjimo jungtis taip pat palaiko stiprią kliento autentifikaciją (SCA).</span><span class="sxs-lookup"><span data-stu-id="54a7a-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="54a7a-119">Europos Sąjungos (ES) mokėjimų paslaugų direktyvos 2.0 (PSD2.0) dalis reikalauja, kad interneto pirkėjai būtų autentifikuojami ne jų interneto apsipirkimo patirtyje jiems naudojant elektroninio apmokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="54a7a-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="54a7a-120">Išsiregistravimo srauto metu, klientai yra nukreipiama į jų banko svetainę.</span><span class="sxs-lookup"><span data-stu-id="54a7a-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="54a7a-121">Tuomet, po autentifikavimo, jie yra nukreipiami atgal į prekybos išsiregistravimo srautą.</span><span class="sxs-lookup"><span data-stu-id="54a7a-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="54a7a-122">Šio nukreipimo metu, informacija, kad klientas įvedė išsiregistravimo srautą (pavyzdžiui, siuntimo adresą, pristatymo parinktis, dovanų kortelės informaciją ir lojalumo informaciją) išliks.</span><span class="sxs-lookup"><span data-stu-id="54a7a-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="54a7a-123">Prie jums įjungiant šią funkciją, mokėjimo jungtis turi būti sukonfigūruota SCA prekybos štabe.</span><span class="sxs-lookup"><span data-stu-id="54a7a-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="54a7a-124">Dėl išsamesnės informacijos, žr. [Stipri kliento autentifikacija naudojant „Adyen“](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="54a7a-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="54a7a-125">Tolesnis paveikslėlis rodo dovanų kortelės lojalumo taškų pavyzdį ir mokėjimo modulius išsiregistravimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="54a7a-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Dovanų kortelės taškų pavyzdys ir mokėjimo moduliai užbaigimo puslapyje.](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="54a7a-127">Mokėjimo modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="54a7a-127">Payment module properties</span></span>

| <span data-ttu-id="54a7a-128">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="54a7a-128">Property name</span></span> | <span data-ttu-id="54a7a-129">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="54a7a-129">Values</span></span> | <span data-ttu-id="54a7a-130">aprašymas</span><span class="sxs-lookup"><span data-stu-id="54a7a-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="54a7a-131">Antraštė</span><span class="sxs-lookup"><span data-stu-id="54a7a-131">Heading</span></span> | <span data-ttu-id="54a7a-132">Antraštės tekstas</span><span class="sxs-lookup"><span data-stu-id="54a7a-132">Heading text</span></span> | <span data-ttu-id="54a7a-133">Pasirenkama antraštė mokėjimo moduliui.</span><span class="sxs-lookup"><span data-stu-id="54a7a-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="54a7a-134">„iframe“ aukštis</span><span class="sxs-lookup"><span data-stu-id="54a7a-134">Height of the iframe</span></span> | <span data-ttu-id="54a7a-135">Pikseliai</span><span class="sxs-lookup"><span data-stu-id="54a7a-135">Pixels</span></span> | <span data-ttu-id="54a7a-136">„iframe“ aukštis pikseliais.</span><span class="sxs-lookup"><span data-stu-id="54a7a-136">The iframe height, in pixels.</span></span> <span data-ttu-id="54a7a-137">Aukštis gali būti reguliuojamas, kaip būtina.</span><span class="sxs-lookup"><span data-stu-id="54a7a-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="54a7a-138">Rodyti sąskaitų siuntimo adresą</span><span class="sxs-lookup"><span data-stu-id="54a7a-138">Show billing address</span></span> | <span data-ttu-id="54a7a-139">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="54a7a-139">**True** or **False**</span></span> | <span data-ttu-id="54a7a-140">Jei ši ypatybė yra nustatyta į **Teisingą**, mokėjimo adresas bus pateiktas „Adyen“ mokėjimo modulio „iframe“ viduje.</span><span class="sxs-lookup"><span data-stu-id="54a7a-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="54a7a-141">Jei jis nustatytas į **Neteisingas**, mokėjimo adreso „Adyen“ neteiks ir prekybos vartotojas turės sukonfigūruoti modulį tam, kad rodytų mokėjimo adresą išsiregistravimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="54a7a-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="54a7a-142">Mokėjimo stiliaus nepaisymas</span><span class="sxs-lookup"><span data-stu-id="54a7a-142">Payment style override</span></span> | <span data-ttu-id="54a7a-143">Kaskadinio stiliaus lapų (CSS) kodai</span><span class="sxs-lookup"><span data-stu-id="54a7a-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="54a7a-144">Kadangi mokėjimo modulis yra palaikomas „iframe“, esama apriboto stiliaus pajėgumo.</span><span class="sxs-lookup"><span data-stu-id="54a7a-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="54a7a-145">Galite pasiekti tam tikrą stilių naudodami šią ypatybę.</span><span class="sxs-lookup"><span data-stu-id="54a7a-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="54a7a-146">Vietos stiliaus viršijimui, turite įkelti CSS kodą kaip šios ypatybės vertę.</span><span class="sxs-lookup"><span data-stu-id="54a7a-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="54a7a-147">Vietos kūrimo įrankis CSS viršija ir stiliai nėra taikomi šiam moduliui.</span><span class="sxs-lookup"><span data-stu-id="54a7a-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="54a7a-148">Sąskaitų siuntimo adresas</span><span class="sxs-lookup"><span data-stu-id="54a7a-148">Billing address</span></span>

<span data-ttu-id="54a7a-149">Mokėjimo modulis taip pat leidžia klientams pateikti sąskaitos adresą jų mokėjimo informacijai.</span><span class="sxs-lookup"><span data-stu-id="54a7a-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="54a7a-150">Jis taip pat leidžia jiems naudoti jų siuntimo adresą kaip mokėjimo adresą siekiant supaprastinti ir pagreitinti išsiregistravimo srautą.</span><span class="sxs-lookup"><span data-stu-id="54a7a-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="54a7a-151">Jei **Rodyti mokėjimo adresą** ypatybė yra nustatyta į **Netikrą**, mokėjimo modulis turi būti konfigūruotas išsiregistravimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="54a7a-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="54a7a-152">Įtraukite mokėjimo modulį į galutinį puslapį ir nustatykite reikiamas ypatybes</span><span class="sxs-lookup"><span data-stu-id="54a7a-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="54a7a-153">Mokėjimo modulis gali būti įtrauktas tik į galutinį modulį.</span><span class="sxs-lookup"><span data-stu-id="54a7a-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="54a7a-154">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti mokėjimo modulį išsiregistravimo puslapis, žr. [Galutinis modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="54a7a-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54a7a-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="54a7a-155">Additional resources</span></span>

[<span data-ttu-id="54a7a-156">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="54a7a-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="54a7a-157">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="54a7a-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="54a7a-158">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="54a7a-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="54a7a-159">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="54a7a-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="54a7a-160">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="54a7a-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="54a7a-161">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="54a7a-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="54a7a-162">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="54a7a-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="54a7a-163">„Dynamics 365“ mokėjimo jungtis, skirta sprendimui „Adyen“</span><span class="sxs-lookup"><span data-stu-id="54a7a-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="54a7a-164">Stipri kliento autentifikacija naudojant „Adyen“</span><span class="sxs-lookup"><span data-stu-id="54a7a-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
