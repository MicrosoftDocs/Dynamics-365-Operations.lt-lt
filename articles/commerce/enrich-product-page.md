---
title: Papildyti produkto puslapį
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ papildyti produkto puslapį.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9c0f329d21cdda5c36a39a8c602d5925b720f52
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945748"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="ad951-103">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="ad951-103">Enrich a product page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ad951-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ papildyti produkto puslapį.</span><span class="sxs-lookup"><span data-stu-id="ad951-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ad951-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="ad951-105">Overview</span></span>

<span data-ttu-id="ad951-106">Pagal numatytuosius parametrus, jūsų svetainė naudoja bendrąjį puslapį, kad būtų rodomi produkto duomenys.</span><span class="sxs-lookup"><span data-stu-id="ad951-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="ad951-107">Šiame puslapyje yra pagrindinė informacija apie produktą ir valdiklius, kurie reikalingi tą produktą parduoti.</span><span class="sxs-lookup"><span data-stu-id="ad951-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="ad951-108">Tačiau galite papildyti informaciją, kuri gaunama iš „Retail“ serverio su papildomais konkretaus produkto paveikslėliais arba tekstu.</span><span class="sxs-lookup"><span data-stu-id="ad951-108">However, you can supplement the information that comes from the Retail Server with additional images or text for a specific product.</span></span> <span data-ttu-id="ad951-109">Šis procesas žinomas kaip produkto puslapio papildymas.</span><span class="sxs-lookup"><span data-stu-id="ad951-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="ad951-110">Daugeliu atvejų, norėsite naudoti konkretų papildomą turinį savo produktams.</span><span class="sxs-lookup"><span data-stu-id="ad951-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="ad951-111">Nuėję į **„Retail“** kūrimo įrankį, matysite produktų sąrašą iš kanalo, kuris priskirtas svetainei.</span><span class="sxs-lookup"><span data-stu-id="ad951-111">When you go to **Retail** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="ad951-112">Šiame sąraše, stulpelis **Papildyta** nurodo, ar buvo papildytas produkto puslapis.</span><span class="sxs-lookup"><span data-stu-id="ad951-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="ad951-113">Jei stulpelyje atsiranda varnelė, to produkto puslapis buvo papildytas.</span><span class="sxs-lookup"><span data-stu-id="ad951-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="ad951-114">Jei varnelė atsiranda, produktui naudojamas numatytasis produkto puslapis ir turinys.</span><span class="sxs-lookup"><span data-stu-id="ad951-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="ad951-115">Galite peržiūrėti ir papildytų, ir nepapildytų produkto puslapių, pasirinkdami produkto pavadinimą sąraše.</span><span class="sxs-lookup"><span data-stu-id="ad951-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="ad951-116">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="ad951-116">Enrich a product page</span></span>

<span data-ttu-id="ad951-117">Norėdami papildyti produkto puslapį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ad951-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="ad951-118">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="ad951-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ad951-119">Kairėje naršymo srityje pasirinkite **Produktai**.</span><span class="sxs-lookup"><span data-stu-id="ad951-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="ad951-120">Pasirinkite bet kokį produktą, kuris neturi papildyto produkto puslapio.</span><span class="sxs-lookup"><span data-stu-id="ad951-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="ad951-121">Veiksmų srityje spustelėkite **Papildyti produkto puslapį**.</span><span class="sxs-lookup"><span data-stu-id="ad951-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="ad951-122">Pasirinkite **PDP šablonas**, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ad951-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="ad951-123">Puslapio struktūros medyje kairėje išplėskite atkarpą **Pagrindinis**.</span><span class="sxs-lookup"><span data-stu-id="ad951-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="ad951-124">Pasirinkite prie atkarpos **Pagrindinis** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="ad951-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ad951-125">Pasirinkite **Konteineris 2**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ad951-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="ad951-126">Pasirinkite daugtaškio mygtuką dalyje **Konteineris 2** ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="ad951-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ad951-127">Pasirinkite **Funkcija**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ad951-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="ad951-128">Dešinėje, srityje Ypatybės, lauke **Raiškusis tekstas**, įveskite atnaujintą produkto aprašą.</span><span class="sxs-lookup"><span data-stu-id="ad951-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="ad951-129">Lauke **Antraštė** įveskite antraštės tekstą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ad951-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="ad951-130">Pasirinkite **Įrašyti**, tada – **Įrašyti ir atrakinti**.</span><span class="sxs-lookup"><span data-stu-id="ad951-130">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="ad951-131">Lauke **Komentarai** įveskite **Papildyti produktą** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ad951-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="ad951-132">Norėdami peržiūrėti papildytą produkto puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="ad951-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="ad951-133">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="ad951-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="ad951-134">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="ad951-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad951-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ad951-135">Additional resources</span></span>

[<span data-ttu-id="ad951-136">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="ad951-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="ad951-137">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="ad951-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ad951-138">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="ad951-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="ad951-139">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="ad951-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="ad951-140">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="ad951-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="ad951-141">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="ad951-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="ad951-142">Puslapio turinio pritaikymo neįgaliesiems patikra</span><span class="sxs-lookup"><span data-stu-id="ad951-142">Verify page content accessibility</span></span>](verify-accessibility.md)
