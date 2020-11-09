---
title: Išsamios užsakymo informacijos modulis
description: Šioje temoje aprašomi išsamios užsakymo informacijos moduliai ir jų naudojimas „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015185"
---
# <a name="order-details-module"></a><span data-ttu-id="2180a-103">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="2180a-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2180a-104">Šioje temoje aprašomi išsamios užsakymo informacijos moduliai ir jų naudojimas „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="2180a-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2180a-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="2180a-105">Overview</span></span>

<span data-ttu-id="2180a-106">Išsamios užsakymo informacijos modulis pateikia užsakymo patvirtinimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="2180a-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="2180a-107">Pateikiamas užsakymo patvirtinimo ID, užsakymo kontaktinė informacija ir kita išsami informacija apie užsakymą, kaip pvz., įsigytos prekės, mokėjimo informacija ir pristatymo būdas.</span><span class="sxs-lookup"><span data-stu-id="2180a-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="2180a-108">Užsakymo išsamios informacijos modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="2180a-108">Order details module properties</span></span>

| <span data-ttu-id="2180a-109">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="2180a-109">Property name</span></span>  | <span data-ttu-id="2180a-110">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="2180a-110">Values</span></span> | <span data-ttu-id="2180a-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="2180a-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="2180a-112">Antraštė</span><span class="sxs-lookup"><span data-stu-id="2180a-112">Heading</span></span>        | <span data-ttu-id="2180a-113">Antraštės tekstas ir antraštės žymė ( **H1** , **H2** , **H3** , **H4** , **H5** arba **H6** )</span><span class="sxs-lookup"><span data-stu-id="2180a-113">Heading text and heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="2180a-114">Užsakymo išsamios informacijos modulis gali turėti antraštę.</span><span class="sxs-lookup"><span data-stu-id="2180a-114">The order details module can have a heading.</span></span> <span data-ttu-id="2180a-115">Numatyta, kad naudojama antrašės žymė **H2**.</span><span class="sxs-lookup"><span data-stu-id="2180a-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="2180a-116">Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="2180a-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="2180a-117">Kontaktinis numeris</span><span class="sxs-lookup"><span data-stu-id="2180a-117">Contact number</span></span> | <span data-ttu-id="2180a-118">Tekstas</span><span class="sxs-lookup"><span data-stu-id="2180a-118">Text</span></span> | <span data-ttu-id="2180a-119">Galite pateikti su užsakymais susijusių klausimų kontaktinį numerį.</span><span class="sxs-lookup"><span data-stu-id="2180a-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="2180a-120">Moduliai, kuriuos galima naudoti užsakymo informacijos puslapyje</span><span class="sxs-lookup"><span data-stu-id="2180a-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="2180a-121">Kurdami išsamios užsakymo informacijos puslapį, prie užsakymo informacijos modulio galite pridėti ir kitus svarbius modulius.</span><span class="sxs-lookup"><span data-stu-id="2180a-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="2180a-122">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="2180a-122">Here are some examples:</span></span>

- <span data-ttu-id="2180a-123">**Rekomendacijų modulis** – jis gali būti pridėtas prie išsamios užsakymo informacijos puslapio, kad klientui būtų pasiūlyti kiti produktai.</span><span class="sxs-lookup"><span data-stu-id="2180a-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="2180a-124">**Rinkodaros moduliai** – prie išsamios užsakymo informacijos puslapio galima pridėti bet kurį rinkodaros modulį, kad būtų parodytas rinkodaros turinys.</span><span class="sxs-lookup"><span data-stu-id="2180a-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="2180a-125">Pridėkite užsakymo išsamios informacijos modulį prie puslapio</span><span class="sxs-lookup"><span data-stu-id="2180a-125">Add an order details module to a page</span></span>

<span data-ttu-id="2180a-126">Norėdami pridėti užsakymo išsamios informacijos modulį naujame puslapyje ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2180a-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2180a-127">Eikite į **Šablonai** ir pasirinkite **Naujas** , kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="2180a-127">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2180a-128">**Naujas šablonas** dialogo lange po **Šablono pavadinimas** įveskite pavadinimą **Užsakymo išsamios informacijos šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2180a-128">In the **New Template** dialog box, under **Template name** , enter the name **Order details template** , and then select **OK**.</span></span>
1. <span data-ttu-id="2180a-129">Vietoje **Pagrindinė dalis** pasirinkite daugtaškį ( **...** ), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="2180a-129">In the **Body** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2180a-130">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis** , tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2180a-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2180a-131">Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį ( **...** ) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="2180a-131">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2180a-132">Dialogo lange **Pridėti modulį** pasirinkite **Užsakymo išsami informacija** modulį, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2180a-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2180a-133">Pasirinkite **Įrašyti** ir tada pasirinkite **Peržiūrėti** , kad peržiūrėtumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="2180a-133">Select **Save** , and then select **Preview** to preview the template.</span></span> <span data-ttu-id="2180a-134">Užsakymo informacijos modulis nebus atvaizduotas, nes tam reikalingas užsakymo patvirtinimo numerio kontekstas.</span><span class="sxs-lookup"><span data-stu-id="2180a-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="2180a-135">Pasirinkite **Baigti redagavimą** , kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti** , kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="2180a-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="2180a-136">Eikite į **Puslapiai** ir pasirinkite **Naujas** , kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="2180a-136">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="2180a-137">Dialogo lange **Pasirinkti šabloną** pasirinkite **Užsakymo išsamios informacijos šablonas**.</span><span class="sxs-lookup"><span data-stu-id="2180a-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="2180a-138">Po **Puslapio pavadinimas** įveskite **Užsakymo išsamios informacijos puslapis** , tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2180a-138">Under **Page name** , enter **Order details page** , and then select **OK**.</span></span>
1. <span data-ttu-id="2180a-139">Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį ( **...** ) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="2180a-139">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2180a-140">Dialogo lange **Pridėti modulį** pasirinkite **Užsakymo išsami informacija** modulį, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2180a-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2180a-141">Užsakymo išsamios informacijos modulio ypatybių srityje, šalia pieštuko simbolio, pasirinkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="2180a-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="2180a-142">**Antraštės tekstas** lauke **Antraštė** dialogo lango įveskite antraštės tekstą **Užsakymo išsami informacija** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2180a-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details** , and then select **OK**.</span></span>
1. <span data-ttu-id="2180a-143">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="2180a-143">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="2180a-144">Pasirinkite **Baigti redagavimą** , kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti** , kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="2180a-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2180a-145">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2180a-145">Additional resources</span></span>

[<span data-ttu-id="2180a-146">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="2180a-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2180a-147">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="2180a-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="2180a-148">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="2180a-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2180a-149">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="2180a-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="2180a-150">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="2180a-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="2180a-151">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="2180a-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="2180a-152">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="2180a-152">Gift card module</span></span>](add-giftcard.md)
