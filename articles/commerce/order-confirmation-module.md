---
title: Užsakymo patvirtinimo modulis
description: Šioje temoje aprašomi užsakymo patvirtinimo modeliai ir jis aprašo, kaip juos naudoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 407fc2724d4b589ef5f611974f9358e879dba7ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257152"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="b858c-103">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b858c-104">Šioje temoje aprašomi užsakymo patvirtinimo modeliai ir jis aprašo, kaip juos naudoti „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="b858c-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b858c-105">Užsakymo patvirtinimo modulis yra naudojamas siekiant parodyti užsakymo patvirtinimo išsamią informaciją padarius užsakymą.</span><span class="sxs-lookup"><span data-stu-id="b858c-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="b858c-106">Jis rodo užsakymo patvirtinimo ID, užsakymo kontaktinę informaciją ir kitą išsamią užsakymo informaciją, tokią kaip įsigytos prekės, mokėjimo informacijas, paėmimo parinktys ir siuntimo metodas.</span><span class="sxs-lookup"><span data-stu-id="b858c-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="b858c-107">Užsakymo patvirtinimo modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="b858c-107">Order confirmation module properties</span></span>

| <span data-ttu-id="b858c-108">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="b858c-108">Property name</span></span>  | <span data-ttu-id="b858c-109">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="b858c-109">Values</span></span> | <span data-ttu-id="b858c-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="b858c-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b858c-111">Antraštė</span><span class="sxs-lookup"><span data-stu-id="b858c-111">Heading</span></span>        | <span data-ttu-id="b858c-112">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**)</span><span class="sxs-lookup"><span data-stu-id="b858c-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b858c-113">Užsakymo patvirtinimo modulyje gali būti antraštė.</span><span class="sxs-lookup"><span data-stu-id="b858c-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="b858c-114">Numatyta, kad naudojama antrašės žymė **H2**.</span><span class="sxs-lookup"><span data-stu-id="b858c-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="b858c-115">Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="b858c-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="b858c-116">Kontaktinis numeris</span><span class="sxs-lookup"><span data-stu-id="b858c-116">Contact number</span></span> | <span data-ttu-id="b858c-117">Tekstas</span><span class="sxs-lookup"><span data-stu-id="b858c-117">Text</span></span> | <span data-ttu-id="b858c-118">Galite pateikti su užsakymais susijusių klausimų kontaktinį numerį.</span><span class="sxs-lookup"><span data-stu-id="b858c-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="b858c-119">Rodyti paėmimo laiko vietos informaciją</span><span class="sxs-lookup"><span data-stu-id="b858c-119">Show pickup timeslot information</span></span> | <span data-ttu-id="b858c-120">Teisinga arba klaidinga</span><span class="sxs-lookup"><span data-stu-id="b858c-120">True or False</span></span> | <span data-ttu-id="b858c-121">Ši ypatybės yra prieinama „Dynamics 365 Commerce“ 10.0.15 ir vėlesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="b858c-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="b858c-122">Kai jis teisingas, jis rodo paėmimo laiko vietos informaciją, jei pateikta paėmimo prekei</span><span class="sxs-lookup"><span data-stu-id="b858c-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="b858c-123">Moduliai gali būti naudojami užsakymo patvirtinimo puslapyje</span><span class="sxs-lookup"><span data-stu-id="b858c-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="b858c-124">Jums sukūrus užsakymo patvirtinimo puslapį, galite įtraukti kitus būtinus modulius kartu su užsakymo patvirtinimo moduliu.</span><span class="sxs-lookup"><span data-stu-id="b858c-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="b858c-125">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="b858c-125">Here are some examples:</span></span>

- <span data-ttu-id="b858c-126">**Rekomendacijų modulis** – Rekomendacijų modulis gali būti įtrauktas į užsakymo patvirtinimo puslapį siekiant patarti kitus produktus klientui.</span><span class="sxs-lookup"><span data-stu-id="b858c-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="b858c-127">**Reklamos moduliai** – Bet kuris reklamos modulis gali būti įtrauktas į užsakymo patvirtinimo puslapį, kad rodytų reklamos turinį.</span><span class="sxs-lookup"><span data-stu-id="b858c-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="b858c-128">Įtraukti užsakymo patvirtinimo modulį į puslapį</span><span class="sxs-lookup"><span data-stu-id="b858c-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="b858c-129">Norėdami įtraukti užsakymo patvirtinimo modulį į naują puslapį ir nustatyti reikiamas ypatybes, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="b858c-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b858c-130">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="b858c-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b858c-131">Teksto laukelyje **Naujas šablonas** skyriuje **Šablono pavadinimas**, įtveskite pavadinimą **Užsakymo patvirtinimo šablonas** ir tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b858c-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="b858c-132">Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="b858c-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b858c-133">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b858c-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b858c-134">Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="b858c-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b858c-135">Teksto laukelyje **Įtraukite modulį** pasirinkite **Užsakymo patvirtinimo** modulis ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b858c-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b858c-136">Pasirinkite **Įrašyti** ir tada pasirinkite **Peržiūrėti**, kad peržiūrėtumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="b858c-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="b858c-137">Užsakymo patvirtinimo modulis nebus sukurtas, nes jam reikia užsakymo patvirtinimo skaičiaus konteksto.</span><span class="sxs-lookup"><span data-stu-id="b858c-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="b858c-138">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="b858c-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b858c-139">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="b858c-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b858c-140">Teksto laukelyje **Pasirinkti šabloną** rinkitės **Užsakymo patvirtinimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="b858c-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="b858c-141">Skyriuje **Puslapio pavadinimas**, įveskite **Užsakymo patvirtinimo puslapis** ir tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b858c-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="b858c-142">Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="b858c-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b858c-143">Teksto laukelyje **Įtraukite modulį** pasirinkite **Užsakymo patvirtinimo** modulis ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b858c-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b858c-144">Ypatybių juostoje užsakymo patvirtinimo moduliui, pasirinkite **Antraštė** šalia pieštuko simbolio.</span><span class="sxs-lookup"><span data-stu-id="b858c-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="b858c-145">Laukelyje **Antraštės tekstas** skyriuje **Antraštės** teksto laukelyje, įtveskite antraštės tekstą **Užsakymo patvirtinimas** ir tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="b858c-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="b858c-146">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="b858c-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="b858c-147">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="b858c-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b858c-148">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b858c-148">Additional resources</span></span>

[<span data-ttu-id="b858c-149">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b858c-150">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b858c-151">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b858c-152">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b858c-153">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b858c-154">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b858c-155">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b858c-156">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="b858c-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]