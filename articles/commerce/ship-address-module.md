---
title: Siuntimo adreso modulis
description: Ši tema paaiškina siuntimo adreso modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: 7233b23020e6c82f39981d530095642902461807
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818403"
---
# <a name="shipping-address-module"></a><span data-ttu-id="f214f-103">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="f214f-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f214f-104">Ši tema aprašo siuntimo adreso modulį ir tai, kaip jį sukonfigūruoti „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="f214f-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f214f-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="f214f-105">Overview</span></span>

<span data-ttu-id="f214f-106">Siuntimo adreso modulis leidžia klientams įtraukti ar pasirinkti siuntimo adresą užsakymui išsiregistravimo srauto metu.</span><span class="sxs-lookup"><span data-stu-id="f214f-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="f214f-107">Jei klientas yra prisijungęs, visi anksčiau tam klientui įrašyti adresai bus rodomi, o klientas galės iš jų pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="f214f-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="f214f-108">Klientas taip pat gali įtraukti naują adresą.</span><span class="sxs-lookup"><span data-stu-id="f214f-108">The customer can also add a new address.</span></span> <span data-ttu-id="f214f-109">Siuntimo adreso modulis yra naudojamas visoms užsakymo prekėms, kuriems reikalingas siuntimas.</span><span class="sxs-lookup"><span data-stu-id="f214f-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="f214f-110">Siuntimo adreso formatai gali būti nustatyti komercijos štabe kiekvienai šaliai ar regionui, o siuntimo adreso modulis tuomet įjungia valstybei/regionui priklausančias taisykles.</span><span class="sxs-lookup"><span data-stu-id="f214f-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="f214f-111">Kai klientai įveda siuntimo adresą išsiregistravimo sraute, jie turi pasirinkimą įrašyti adresą kaip pirminį.</span><span class="sxs-lookup"><span data-stu-id="f214f-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="f214f-112">Ši parinktis rodoma tik klientui prisijungus.</span><span class="sxs-lookup"><span data-stu-id="f214f-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="f214f-113">Nepaisant to, kad siuntimo adreso modulis neleidžia patvirtinti adreso, ši funkcija gali būti įgyvendinta tinkinimo metu.</span><span class="sxs-lookup"><span data-stu-id="f214f-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="f214f-114">Tolesnis paveikslėlis rodo naujo siuntimo adreso modulio pavyzdį išsiregistravimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f214f-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Siuntimo adreso pavyzdžio modulis išsiregistravimo puslapyje](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="f214f-116">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="f214f-116">Module properties</span></span>

| <span data-ttu-id="f214f-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f214f-117">Property name</span></span> | <span data-ttu-id="f214f-118">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="f214f-118">Values</span></span> | <span data-ttu-id="f214f-119">aprašymas</span><span class="sxs-lookup"><span data-stu-id="f214f-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f214f-120">Antraštė</span><span class="sxs-lookup"><span data-stu-id="f214f-120">Heading</span></span> | <span data-ttu-id="f214f-121">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**)</span><span class="sxs-lookup"><span data-stu-id="f214f-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="f214f-122">Pasirenkama antraštė siuntimo adreso moduliui.</span><span class="sxs-lookup"><span data-stu-id="f214f-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="f214f-123">Rodyti adreso tipą</span><span class="sxs-lookup"><span data-stu-id="f214f-123">Show address type</span></span> | <span data-ttu-id="f214f-124">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="f214f-124">**True** or **False**</span></span> | <span data-ttu-id="f214f-125">Jei šios pasirenkamos ypatybės yra nustatytos į **Teisingos**, bus rodomas adreso tipas, toks kaip **Namų** ar **Įmonės**.</span><span class="sxs-lookup"><span data-stu-id="f214f-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="f214f-126">Jei nėra nurodyta jokio adreso tipo, adresas automatiškai bus įrašomas kaip **Tipas**=**Kitas**.</span><span class="sxs-lookup"><span data-stu-id="f214f-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="f214f-127">Įtraukite siuntimo adreso modulį į galutinį puslapį ir nustatykite reikiamas ypatybes</span><span class="sxs-lookup"><span data-stu-id="f214f-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="f214f-128">Siuntimo adreso modulis gali būti įtrauktas tik į galutinį modulį.</span><span class="sxs-lookup"><span data-stu-id="f214f-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="f214f-129">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti siuntimo adreso modulį ir įtraukti jį į galutinį puslapį, žr. [Galutinis modulis](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f214f-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f214f-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f214f-130">Additional resources</span></span>

[<span data-ttu-id="f214f-131">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="f214f-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f214f-132">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="f214f-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="f214f-133">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="f214f-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f214f-134">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="f214f-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="f214f-135">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="f214f-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="f214f-136">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="f214f-136">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f214f-137">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="f214f-137">Gift card module</span></span>](add-giftcard.md)