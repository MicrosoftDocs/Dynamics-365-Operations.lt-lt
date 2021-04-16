---
title: Papildyti produkto puslapį
description: Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ papildyti produkto puslapį.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799054"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="3b29a-103">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="3b29a-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3b29a-104">Šioje temoje aprašoma, kaip „Microsoft Dynamics 365 Commerce“ papildyti produkto puslapį.</span><span class="sxs-lookup"><span data-stu-id="3b29a-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3b29a-105">Pagal numatytuosius parametrus, jūsų svetainė naudoja bendrąjį puslapį, kad būtų rodomi produkto duomenys.</span><span class="sxs-lookup"><span data-stu-id="3b29a-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="3b29a-106">Šiame puslapyje yra pagrindinė informacija apie produktą ir valdiklius, kurie reikalingi tą produktą parduoti.</span><span class="sxs-lookup"><span data-stu-id="3b29a-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="3b29a-107">Tačiau galite papildyti informaciją, kuri gaunama iš „Commerce Scale Unit“, papildomais konkretaus produkto paveikslėliais arba tekstu.</span><span class="sxs-lookup"><span data-stu-id="3b29a-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="3b29a-108">Šis procesas žinomas kaip produkto puslapio papildymas.</span><span class="sxs-lookup"><span data-stu-id="3b29a-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="3b29a-109">Daugeliu atvejų, norėsite naudoti konkretų papildomą turinį savo produktams.</span><span class="sxs-lookup"><span data-stu-id="3b29a-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="3b29a-110">Nuėję į **„Retail“ ir „Commerce“** kūrimo įrankyje, matysite produktų sąrašą iš kanalo, kuris priskirtas svetainei.</span><span class="sxs-lookup"><span data-stu-id="3b29a-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="3b29a-111">Šiame sąraše, stulpelis **Papildyta** nurodo, ar buvo papildytas produkto puslapis.</span><span class="sxs-lookup"><span data-stu-id="3b29a-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="3b29a-112">Jei stulpelyje atsiranda varnelė, to produkto puslapis buvo papildytas.</span><span class="sxs-lookup"><span data-stu-id="3b29a-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="3b29a-113">Jei varnelė atsiranda, produktui naudojamas numatytasis produkto puslapis ir turinys.</span><span class="sxs-lookup"><span data-stu-id="3b29a-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="3b29a-114">Galite peržiūrėti ir papildytų, ir nepapildytų produkto puslapių, pasirinkdami produkto pavadinimą sąraše.</span><span class="sxs-lookup"><span data-stu-id="3b29a-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="3b29a-115">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="3b29a-115">Enrich a product page</span></span>

<span data-ttu-id="3b29a-116">Norėdami papildyti produkto puslapį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3b29a-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="3b29a-117">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="3b29a-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="3b29a-118">Kairėje naršymo srityje pasirinkite **Produktai**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="3b29a-119">Pasirinkite bet kokį produktą, kuris neturi papildyto produkto puslapio.</span><span class="sxs-lookup"><span data-stu-id="3b29a-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="3b29a-120">Veiksmų srityje spustelėkite **Papildyti produkto puslapį**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="3b29a-121">Pasirinkite **PDP šablonas**, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b29a-122">Puslapio struktūros medyje kairėje išplėskite atkarpą **Pagrindinis**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="3b29a-123">Pasirinkite prie atkarpos **Pagrindinis** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="3b29a-124">Pasirinkite **Konteineris 2**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b29a-125">Pasirinkite daugtaškio mygtuką dalyje **Konteineris 2** ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="3b29a-126">Pasirinkite **Funkcija**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b29a-127">Dešinėje, srityje Ypatybės, lauke **Raiškusis tekstas**, įveskite atnaujintą produkto aprašą.</span><span class="sxs-lookup"><span data-stu-id="3b29a-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="3b29a-128">Lauke **Antraštė** įveskite antraštės tekstą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="3b29a-129">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="3b29a-130">Lauke **Komentarai** įveskite **Papildyti produktą** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="3b29a-131">Norėdami peržiūrėti papildytą produkto puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="3b29a-132">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="3b29a-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="3b29a-133">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="3b29a-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b29a-134">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3b29a-134">Additional resources</span></span>

[<span data-ttu-id="3b29a-135">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="3b29a-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="3b29a-136">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="3b29a-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="3b29a-137">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="3b29a-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="3b29a-138">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="3b29a-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="3b29a-139">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="3b29a-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="3b29a-140">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="3b29a-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="3b29a-141">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="3b29a-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="3b29a-142">Sukurti dinaminius e-komercijos puslapius pagal URL parametrus</span><span class="sxs-lookup"><span data-stu-id="3b29a-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
