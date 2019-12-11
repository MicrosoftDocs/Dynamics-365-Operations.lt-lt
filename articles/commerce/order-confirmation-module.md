---
title: Užsakymo patvirtinimo modulis
description: Ši tema apima užsakymo patvirtinimo modulius ir joje aprašoma, kaip juos sukurti programoje „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698331"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="c7cce-103">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="c7cce-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c7cce-104">Ši tema apima užsakymo patvirtinimo modulius ir joje aprašoma, kaip juos sukurti programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c7cce-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c7cce-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="c7cce-105">Overview</span></span>

<span data-ttu-id="c7cce-106">Užsakymo patvirtinimo modulis naudojamas rodyti patvirtinimo pranešimą užsakymo patvirtinimo puslapyje, kai pateikiamas užsakymas.</span><span class="sxs-lookup"><span data-stu-id="c7cce-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="c7cce-107">Užsakymo patvirtinimo modulis nurodo užsakymo patvirtinimo numerį ir kliento el. pašto adresą, kuris buvo pateiktas užbaigiant pirkimą.</span><span class="sxs-lookup"><span data-stu-id="c7cce-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="c7cce-108">Kai užsakymas pateikiamas užbaigiant pirkimą, užsakymo patvirtinimo numeris ir kliento el. pašto adresas perduodami į užsakymo patvirtinimo puslapį kaip užklausos eilutė, esanti puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="c7cce-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="c7cce-109">Užsakymo patvirtinimo modulis gauna šią informaciją ir užsakymo patvirtinimo puslapyje sugeneruoja užsakymo būseną.</span><span class="sxs-lookup"><span data-stu-id="c7cce-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="c7cce-110">Užsakymo patvirtinimo modulyje reikalingas šio puslapio kontekstas, kad būtų pateikta užsakymo būsena.</span><span class="sxs-lookup"><span data-stu-id="c7cce-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="c7cce-111">Užsakymo patvirtinimo modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="c7cce-111">Order confirmation module properties</span></span>

| <span data-ttu-id="c7cce-112">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c7cce-112">Property name</span></span> | <span data-ttu-id="c7cce-113">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="c7cce-113">Values</span></span> | <span data-ttu-id="c7cce-114">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c7cce-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="c7cce-115">Antraštė</span><span class="sxs-lookup"><span data-stu-id="c7cce-115">Heading</span></span>       | <span data-ttu-id="c7cce-116">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**)</span><span class="sxs-lookup"><span data-stu-id="c7cce-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="c7cce-117">Užsakymo patvirtinimo modulyje gali būti antraštė.</span><span class="sxs-lookup"><span data-stu-id="c7cce-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="c7cce-118">Numatyta, kad naudojama antrašės žymė **H2**.</span><span class="sxs-lookup"><span data-stu-id="c7cce-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="c7cce-119">Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="c7cce-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="c7cce-120">Moduliai, kuriuos galima naudoti užsakymo patvirtinimo puslapio modulyje</span><span class="sxs-lookup"><span data-stu-id="c7cce-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="c7cce-121">**Rekomendacijos** – rekomendacijų modulį galima įtraukti į užsakymo patvirtinimo puslapį, kad klientas galėtų siūlyti kitus produktus.</span><span class="sxs-lookup"><span data-stu-id="c7cce-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="c7cce-122">**Rinkodara** – rinkodaros modulis gali pridėti rinkodaros turinį į užsakymo patvirtinimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="c7cce-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="c7cce-123">Užsakymo patvirtinimo puslapio modulio kūrimas</span><span class="sxs-lookup"><span data-stu-id="c7cce-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="c7cce-124">Sukurkite puslapio šabloną, pavadintą **užsakymo patvirtinimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="c7cce-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="c7cce-125">Numatytojo puslapio atkarpoje **Pagrindinis** įtraukite užsakymo patvirtinimo modulį.</span><span class="sxs-lookup"><span data-stu-id="c7cce-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="c7cce-126">Užsakymo patvirtinimo modulyje pridėkite rekomendacijų modulį.</span><span class="sxs-lookup"><span data-stu-id="c7cce-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="c7cce-127">Įrašykite ir peržiūrėkite šabloną.</span><span class="sxs-lookup"><span data-stu-id="c7cce-127">Save and preview the template.</span></span> <span data-ttu-id="c7cce-128">Užsakymo patvirtinimo modulis negali būti atvaizduotas, nes jam reikia užsakymo patvirtinimo numerio konteksto.</span><span class="sxs-lookup"><span data-stu-id="c7cce-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="c7cce-129">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="c7cce-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="c7cce-130">Naudodami užsakymo patvirtinimo šabloną, sukurkite puslapį, pavadintą **Užsakymo patvirtinimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="c7cce-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="c7cce-131">Pridėkite numatytąjį puslapį prie puslapio struktūros.</span><span class="sxs-lookup"><span data-stu-id="c7cce-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="c7cce-132">Į atkarpą **Antraštė** įtraukite antraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c7cce-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="c7cce-133">Į atkarpą **Poraštė** įtraukite poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="c7cce-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="c7cce-134">Atkarpoje **Pagrindinis** įtraukite užsakymo patvirtinimo modulį.</span><span class="sxs-lookup"><span data-stu-id="c7cce-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="c7cce-135">Užsakymo patvirtinimo modulio ypatybių srityje įtraukite antraštę **Užsakymo patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="c7cce-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="c7cce-136">Po užsakymo patvirtinimo moduliu įtraukite rekomendacijų modulį ir sukonfigūruokite taip, kad jis naudotų parametrus **Nauja** ir **Perkamiausi**.</span><span class="sxs-lookup"><span data-stu-id="c7cce-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="c7cce-137">Puslapį įrašykite ir peržiūrėkite, įrašykite ir atrakinkite bei jį publikuokite.</span><span class="sxs-lookup"><span data-stu-id="c7cce-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7cce-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c7cce-138">Additional resources</span></span>

[<span data-ttu-id="c7cce-139">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="c7cce-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c7cce-140">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="c7cce-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c7cce-141">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="c7cce-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c7cce-142">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="c7cce-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c7cce-143">Pirkimo užbaigimo modulį</span><span class="sxs-lookup"><span data-stu-id="c7cce-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c7cce-144">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="c7cce-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c7cce-145">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="c7cce-145">Footer module</span></span>](author-footer-module.md)
