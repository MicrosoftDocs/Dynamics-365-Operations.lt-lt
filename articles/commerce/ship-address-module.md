---
title: Siuntimo adreso modulis
description: Ši tema paaiškina siuntimo adreso modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
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
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234418"
---
# <a name="shipping-address-module"></a><span data-ttu-id="92497-103">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="92497-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="92497-104">Ši tema paaiškina siuntimo adreso modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="92497-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="92497-105">Siuntimo adreso modulis leidžia klientams įtraukti ar pasirinkti siuntimo adresą užsakymui išsiregistravimo srauto metu.</span><span class="sxs-lookup"><span data-stu-id="92497-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="92497-106">Jei klientas yra prisijungęs, visi anksčiau tam klientui įrašyti adresai bus rodomi, o klientas galės iš jų pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="92497-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="92497-107">Klientas taip pat gali įtraukti naują adresą.</span><span class="sxs-lookup"><span data-stu-id="92497-107">The customer can also add a new address.</span></span> <span data-ttu-id="92497-108">Siuntimo adreso modulis yra naudojamas visoms užsakymo prekėms, kuriems reikalingas siuntimas.</span><span class="sxs-lookup"><span data-stu-id="92497-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="92497-109">Siuntimo adreso formatai gali būti nustatyti komercijos štabe kiekvienai šaliai ar regionui, o siuntimo adreso modulis tuomet įjungia valstybei/regionui priklausančias taisykles.</span><span class="sxs-lookup"><span data-stu-id="92497-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="92497-110">Kai klientai įveda siuntimo adresą išsiregistravimo sraute, jie turi pasirinkimą įrašyti adresą kaip pirminį.</span><span class="sxs-lookup"><span data-stu-id="92497-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="92497-111">Ši parinktis rodoma tik klientui prisijungus.</span><span class="sxs-lookup"><span data-stu-id="92497-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="92497-112">Nepaisant to, kad siuntimo adreso modulis neleidžia patvirtinti adreso, ši funkcija gali būti įgyvendinta tinkinimo metu.</span><span class="sxs-lookup"><span data-stu-id="92497-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="92497-113">Tolesnis paveikslėlis rodo naujo siuntimo adreso modulio pavyzdį išsiregistravimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="92497-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Siuntimo adreso pavyzdžio modulis išsiregistravimo puslapyje](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="92497-115">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="92497-115">Module properties</span></span>

| <span data-ttu-id="92497-116">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="92497-116">Property name</span></span> | <span data-ttu-id="92497-117">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="92497-117">Values</span></span> | <span data-ttu-id="92497-118">aprašymas</span><span class="sxs-lookup"><span data-stu-id="92497-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="92497-119">Antraštė</span><span class="sxs-lookup"><span data-stu-id="92497-119">Heading</span></span> | <span data-ttu-id="92497-120">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**)</span><span class="sxs-lookup"><span data-stu-id="92497-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="92497-121">Pasirenkama antraštė siuntimo adreso moduliui.</span><span class="sxs-lookup"><span data-stu-id="92497-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="92497-122">Rodyti adreso tipą</span><span class="sxs-lookup"><span data-stu-id="92497-122">Show address type</span></span> | <span data-ttu-id="92497-123">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="92497-123">**True** or **False**</span></span> | <span data-ttu-id="92497-124">Jei šios pasirenkamos ypatybės yra nustatytos į **Teisingos**, bus rodomas adreso tipas, toks kaip **Namų** ar **Įmonės**.</span><span class="sxs-lookup"><span data-stu-id="92497-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="92497-125">Jei nėra nurodyta jokio adreso tipo, adresas automatiškai bus įrašomas kaip **Tipas**=**Kitas**.</span><span class="sxs-lookup"><span data-stu-id="92497-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="92497-126">Įjungti automatinį pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="92497-126">Enable auto suggestion</span></span>| <span data-ttu-id="92497-127">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="92497-127">**True** or **False**</span></span> | <span data-ttu-id="92497-128">Jei ši pasirinktinė ypatybė nustatyta į **Teisinga**, bus pateikiami automatiniai adreso pasiūlymai.</span><span class="sxs-lookup"><span data-stu-id="92497-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="92497-129">Šiuos pasiūlymus teikia „Bing” žemėlapiai.</span><span class="sxs-lookup"><span data-stu-id="92497-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="92497-130">Daugiau informacijos, kaip nustatyti „Bing” žemėlapių integravimą jūsų svetainėje, žr. [Parduotuvės išrinkiklio modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="92497-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="92497-131">Ši funkcija yra prieinama „Commerce“ versijos 10.0.15 leidime.</span><span class="sxs-lookup"><span data-stu-id="92497-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="92497-132">Automatinio pasiūlymo parinktys</span><span class="sxs-lookup"><span data-stu-id="92497-132">Auto suggest options</span></span>| <span data-ttu-id="92497-133">Skaičius</span><span class="sxs-lookup"><span data-stu-id="92497-133">A number</span></span>| <span data-ttu-id="92497-134">Jei automatiniai adreso pasiūlymai įgalinti, galite nurodyti papildomas parinktis, pvz., didžiausią pasiūlymų, kuriuos reikia pateikti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="92497-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="92497-135">Įtraukite siuntimo adreso modulį į galutinį puslapį ir nustatykite reikiamas ypatybes</span><span class="sxs-lookup"><span data-stu-id="92497-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="92497-136">Siuntimo adreso modulis gali būti įtrauktas tik į galutinį modulį.</span><span class="sxs-lookup"><span data-stu-id="92497-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="92497-137">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti siuntimo adreso modulį ir įtraukti jį į galutinį puslapį, žr. [Galutinis modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="92497-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="92497-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="92497-138">Additional resources</span></span>

[<span data-ttu-id="92497-139">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="92497-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="92497-140">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="92497-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="92497-141">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="92497-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="92497-142">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="92497-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="92497-143">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="92497-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="92497-144">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="92497-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="92497-145">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="92497-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="92497-146">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="92497-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="92497-147">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="92497-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]