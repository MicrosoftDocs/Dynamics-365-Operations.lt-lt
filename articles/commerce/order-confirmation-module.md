---
title: Išsamios užsakymo informacijos modulis
description: Šioje temoje aprašomi išsamios užsakymo informacijos moduliai ir jų naudojimas „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026022"
---
# <a name="order-details-module"></a><span data-ttu-id="52367-103">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="52367-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="52367-104">Šioje temoje aprašomi išsamios užsakymo informacijos moduliai ir jų naudojimas „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="52367-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="52367-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="52367-105">Overview</span></span>

<span data-ttu-id="52367-106">Išsamios užsakymo informacijos modulis pateikia užsakymo patvirtinimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="52367-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="52367-107">Pateikiamas užsakymo patvirtinimo ID, užsakymo kontaktinė informacija ir kita išsami informacija apie užsakymą, kaip pvz., įsigytos prekės, mokėjimo informacija ir pristatymo būdas.</span><span class="sxs-lookup"><span data-stu-id="52367-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="52367-108">Užsakymo patvirtinimo modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="52367-108">Order confirmation module properties</span></span>

| <span data-ttu-id="52367-109">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="52367-109">Property name</span></span>  | <span data-ttu-id="52367-110">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="52367-110">Values</span></span> | <span data-ttu-id="52367-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="52367-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="52367-112">Antraštė</span><span class="sxs-lookup"><span data-stu-id="52367-112">Heading</span></span>        | <span data-ttu-id="52367-113">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**)</span><span class="sxs-lookup"><span data-stu-id="52367-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="52367-114">Užsakymo patvirtinimo modulyje gali būti antraštė.</span><span class="sxs-lookup"><span data-stu-id="52367-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="52367-115">Numatyta, kad naudojama antrašės žymė **H2**.</span><span class="sxs-lookup"><span data-stu-id="52367-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="52367-116">Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="52367-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="52367-117">Kontaktinis numeris</span><span class="sxs-lookup"><span data-stu-id="52367-117">Contact number</span></span> | <span data-ttu-id="52367-118">Tekstas</span><span class="sxs-lookup"><span data-stu-id="52367-118">Text</span></span> | <span data-ttu-id="52367-119">Galite pateikti su užsakymais susijusių klausimų kontaktinį numerį.</span><span class="sxs-lookup"><span data-stu-id="52367-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="52367-120">Moduliai, kuriuos galima naudoti užsakymo informacijos puslapyje</span><span class="sxs-lookup"><span data-stu-id="52367-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="52367-121">Kurdami išsamios užsakymo informacijos puslapį, prie užsakymo informacijos modulio galite pridėti ir kitus svarbius modulius.</span><span class="sxs-lookup"><span data-stu-id="52367-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="52367-122">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="52367-122">Here are some examples:</span></span>

- <span data-ttu-id="52367-123">**Rekomendacijų modulis** – jis gali būti pridėtas prie išsamios užsakymo informacijos puslapio, kad klientui būtų pasiūlyti kiti produktai.</span><span class="sxs-lookup"><span data-stu-id="52367-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="52367-124">**Rinkodaros moduliai** – prie išsamios užsakymo informacijos puslapio galima pridėti bet kurį rinkodaros modulį, kad būtų parodytas rinkodaros turinys.</span><span class="sxs-lookup"><span data-stu-id="52367-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="52367-125">Išsamios užsakymo informacijos puslapio modulio kūrimas</span><span class="sxs-lookup"><span data-stu-id="52367-125">Create an order details page module</span></span>

1. <span data-ttu-id="52367-126">Sukurkite puslapio šabloną pavadinimu **Užsakymo informacijos šablonas**.</span><span class="sxs-lookup"><span data-stu-id="52367-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="52367-127">Prie numatytojo puslapio tarpsnio **Pagrindinis** pridėkite užsakymo informacijos modulį.</span><span class="sxs-lookup"><span data-stu-id="52367-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="52367-128">Prie užsakymo informacijos modulio pridėkite rekomendacijų modulį.</span><span class="sxs-lookup"><span data-stu-id="52367-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="52367-129">Įrašykite ir peržiūrėkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="52367-129">Save and preview the template.</span></span> <span data-ttu-id="52367-130">Užsakymo informacijos modulis nebus atvaizduotas, nes tam reikalingas užsakymo patvirtinimo numerio kontekstas.</span><span class="sxs-lookup"><span data-stu-id="52367-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="52367-131">Baikite šablono redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="52367-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="52367-132">Naudokite ką tik sukurtą užsakymo informacijos šabloną pavadinimu **Užsakymo informacijos puslapis**.</span><span class="sxs-lookup"><span data-stu-id="52367-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="52367-133">Pridėkite numatytąjį puslapį prie puslapio struktūros.</span><span class="sxs-lookup"><span data-stu-id="52367-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="52367-134">Į atkarpą **Antraštė** įtraukite antraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="52367-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="52367-135">Į atkarpą **Poraštė** įtraukite poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="52367-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="52367-136">Prie tarpsnio **Pagrindinis** pridėkite užsakymo informacijos modulį.</span><span class="sxs-lookup"><span data-stu-id="52367-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="52367-137">Prie išsamios užsakymo informacijos modulio ypatybių srities pridėkite antraštę **Užsakymo informacija**.</span><span class="sxs-lookup"><span data-stu-id="52367-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="52367-138">Po užsakymo informacijos moduliu pridėkite rekomendacijų modulį ir sukonfigūruokite jį taip, kad jame būtų naudojami nustatymai **Naujas** ir **Geriausiai parduodami**.</span><span class="sxs-lookup"><span data-stu-id="52367-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="52367-139">Puslapį įrašykite ir peržiūrėkite.</span><span class="sxs-lookup"><span data-stu-id="52367-139">Save and preview the page.</span></span>
1. <span data-ttu-id="52367-140">Baikite puslapio redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="52367-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52367-141">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="52367-141">Additional resources</span></span>

[<span data-ttu-id="52367-142">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="52367-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="52367-143">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="52367-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="52367-144">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="52367-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="52367-145">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="52367-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="52367-146">Pirkimo užbaigimo modulį</span><span class="sxs-lookup"><span data-stu-id="52367-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="52367-147">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="52367-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="52367-148">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="52367-148">Footer module</span></span>](author-footer-module.md)
