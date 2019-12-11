---
title: Įtraukti naują svetainės puslapį
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ įtraukti naują svetainės puslapį.
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
ms.openlocfilehash: d5ab90343220e427a80cc4dde17c628ba64ac69e
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696743"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="d3847-103">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="d3847-103">Add a new site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d3847-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ įtraukti naują svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="d3847-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d3847-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="d3847-105">Overview</span></span>

<span data-ttu-id="d3847-106">Svetainei sukūrus šablonų ir fragmentų, kitas veiksmas yra pradėti kurti puslapius, kuriuose jie naudojami.</span><span class="sxs-lookup"><span data-stu-id="d3847-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="d3847-107">Norėdami pradėti, turite pasirinkti šabloną arba maketą, puslapio pavadinimą ir puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="d3847-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="d3847-108">Šablonas arba maketas</span><span class="sxs-lookup"><span data-stu-id="d3847-108">Template or layout</span></span>

<span data-ttu-id="d3847-109">Naujam puslapiui galite naudoti šabloną arba maketą.</span><span class="sxs-lookup"><span data-stu-id="d3847-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="d3847-110">Norėdami gauti daugiau informacijos, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d3847-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="d3847-111">Puslapio pavadinimas</span><span class="sxs-lookup"><span data-stu-id="d3847-111">Page name</span></span>

<span data-ttu-id="d3847-112">Jūsų puslapio pavadinimas turi būti unikalus.</span><span class="sxs-lookup"><span data-stu-id="d3847-112">The page name must be unique to your page.</span></span> <span data-ttu-id="d3847-113">Jis turi būti aprašomasis, kad galėtumėte lengvai jį rasti ir kiti žmonės žinotų, kam puslapis skirtas.</span><span class="sxs-lookup"><span data-stu-id="d3847-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="d3847-114">Puslapio pavadinimą pasirinkite atidžiai, nes jo negalima pakeisti vėliau.</span><span class="sxs-lookup"><span data-stu-id="d3847-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="d3847-115">Puslapio URL</span><span class="sxs-lookup"><span data-stu-id="d3847-115">Page URL</span></span>

<span data-ttu-id="d3847-116">Galite pasirinkti, kad būtų galima įvesti naujo puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="d3847-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="d3847-117">Sukūrę puslapį, galite įvesti eilutę, kuri bus naudojama visam URL sudaryti.</span><span class="sxs-lookup"><span data-stu-id="d3847-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="d3847-118">Ši eilutė vadinama santykiniu URL arba kintamaisiais URL duomenimis.</span><span class="sxs-lookup"><span data-stu-id="d3847-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="d3847-119">Tada pagal kintamuosius URL duomenis sugeneruojamas visas URL ir jam priskiriamas naujasis puslapis.</span><span class="sxs-lookup"><span data-stu-id="d3847-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="d3847-120">Kintamuosius URL duomenis galite pakeisti vėliau, prieš publikuodami puslapį.</span><span class="sxs-lookup"><span data-stu-id="d3847-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="d3847-121">Norėdami gauti daugiau informacijos, žr. [Puslapio URL sukūrimas](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="d3847-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d3847-122">„Dynamics 365 Commerce“ atsieja URL adresus ir turinį.</span><span class="sxs-lookup"><span data-stu-id="d3847-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="d3847-123">Kitaip tariant, galima sukurti puslapį, kuris nėra susietas su URL, ir URL, kuris nėra susietas su puslapiu.</span><span class="sxs-lookup"><span data-stu-id="d3847-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="d3847-124">Todėl galima sukeisti URL turinį be prastovos ir lengviau valdyti peradresavimą.</span><span class="sxs-lookup"><span data-stu-id="d3847-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="d3847-125">Naujo puslapio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="d3847-125">Add a new page</span></span>

<span data-ttu-id="d3847-126">Norėdami į savo svetainę įtraukti naują puslapį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d3847-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="d3847-127">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="d3847-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d3847-128">Pasirinkite **Naujas puslapis**.</span><span class="sxs-lookup"><span data-stu-id="d3847-128">Select **New Page**.</span></span>
1. <span data-ttu-id="d3847-129">Dialogo lange **Naujas puslapis** pasirinkite šabloną ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3847-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="d3847-130">Lauke **Puslapio pavadinimas** įveskite puslapio pavadinimą, (pavyzdžiui, **Mano naujas puslapis**).</span><span class="sxs-lookup"><span data-stu-id="d3847-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="d3847-131">Lauke **URL** įveskite eilutę (kintamuosius URL duomenis), kad būtų įvestas visas URL (pavyzdžiui, **manonaujaspuslapis**).</span><span class="sxs-lookup"><span data-stu-id="d3847-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="d3847-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3847-132">Select **OK**.</span></span> <span data-ttu-id="d3847-133">Atidaroma puslapio rengyklė.</span><span class="sxs-lookup"><span data-stu-id="d3847-133">The page editor appears.</span></span> <span data-ttu-id="d3847-134">Atkreipkite dėmesį, kad pagal jūsų pasirinktą šabloną antraštė ir poraštė yra automatiškai įtrauktos į puslapį.</span><span class="sxs-lookup"><span data-stu-id="d3847-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="d3847-135">Puslapio struktūroje pasirinkite vietą **Pagrindinis**, pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d3847-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3847-136">Pasirinkite **Konteineris**, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3847-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="d3847-137">Pasirinkite **Paslankusis konteineris**, tada – daugtaškio mygtuką ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d3847-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3847-138">Pasirinkite **Raiškiojo turinio blokas** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3847-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="d3847-139">Pasirinkite **Raiškiojo turinio blokas**, tada – daugtaškio mygtuką ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d3847-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="d3847-140">Pasirinkite **Raiškiojo turinio bloko elementas** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3847-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="d3847-141">Dešinėje esančioje ypatybių srityje pasirinkite **Pastraipa**, tada lauke įveskite **Mano testinis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="d3847-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="d3847-142">Pasirinkite **Įrašyti**, tada – **Įrašyti ir atrakinti**.</span><span class="sxs-lookup"><span data-stu-id="d3847-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="d3847-143">Lauke **Komentarai** įveskite **Įtrauktas naujas puslapis** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d3847-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="d3847-144">Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="d3847-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="d3847-145">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="d3847-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="d3847-146">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="d3847-146">Select **Publish**.</span></span>
1. <span data-ttu-id="d3847-147">Naršymo kelyje (kelio nuorodose) pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="d3847-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d3847-148">Kairėje esančioje naršymo srityje pasirinkite **URL adresai**.</span><span class="sxs-lookup"><span data-stu-id="d3847-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="d3847-149">Sąraše raskite ir pasirinkite savo URL (**manonaujaspuslapis**).</span><span class="sxs-lookup"><span data-stu-id="d3847-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="d3847-150">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="d3847-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3847-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d3847-151">Additional resources</span></span>

[<span data-ttu-id="d3847-152">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="d3847-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="d3847-153">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="d3847-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d3847-154">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="d3847-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="d3847-155">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="d3847-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d3847-156">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="d3847-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d3847-157">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="d3847-157">Enrich a category landing page</span></span>](enrich-category-page.md)

