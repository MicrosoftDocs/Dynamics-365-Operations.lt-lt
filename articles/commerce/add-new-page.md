---
title: Įtraukti naują svetainės puslapį
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ įtraukti naują svetainės puslapį.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 54e690b0dde048b17ce074fcc30cf20a9ff7a4ca
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097134"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="9a6eb-103">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="9a6eb-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9a6eb-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ įtraukti naują svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9a6eb-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="9a6eb-105">Overview</span></span>

<span data-ttu-id="9a6eb-106">Svetainei sukūrus šablonų ir fragmentų, kitas veiksmas yra pradėti kurti puslapius, kuriuose jie naudojami.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="9a6eb-107">Norėdami pradėti, turite pasirinkti šabloną arba maketą, puslapio pavadinimą ir puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="9a6eb-108">Šablonas arba maketas</span><span class="sxs-lookup"><span data-stu-id="9a6eb-108">Template or layout</span></span>

<span data-ttu-id="9a6eb-109">Naujam puslapiui galite naudoti šabloną arba maketą.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="9a6eb-110">Norėdami gauti daugiau informacijos, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9a6eb-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="9a6eb-111">Puslapio pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9a6eb-111">Page name</span></span>

<span data-ttu-id="9a6eb-112">Jūsų puslapio pavadinimas turi būti unikalus.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-112">The page name must be unique to your page.</span></span> <span data-ttu-id="9a6eb-113">Jis turi būti aprašomasis, kad galėtumėte lengvai jį rasti ir kiti žmonės žinotų, kam puslapis skirtas.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="9a6eb-114">Puslapio pavadinimą pasirinkite atidžiai, nes jo negalima pakeisti vėliau.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="9a6eb-115">Puslapio URL</span><span class="sxs-lookup"><span data-stu-id="9a6eb-115">Page URL</span></span>

<span data-ttu-id="9a6eb-116">Galite pasirinkti, kad būtų galima įvesti naujo puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="9a6eb-117">Sukūrę puslapį, galite įvesti eilutę, kuri bus naudojama visam URL sudaryti.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="9a6eb-118">Ši eilutė vadinama santykiniu URL arba kintamaisiais URL duomenimis.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="9a6eb-119">Tada pagal kintamuosius URL duomenis sugeneruojamas visas URL ir jam priskiriamas naujasis puslapis.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="9a6eb-120">Kintamuosius URL duomenis galite pakeisti vėliau, prieš publikuodami puslapį.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="9a6eb-121">Norėdami gauti daugiau informacijos, žr. [Puslapio URL sukūrimas](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="9a6eb-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9a6eb-122">„Dynamics 365 Commerce“ atsieja URL adresus ir turinį.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="9a6eb-123">Kitaip tariant, galima sukurti puslapį, kuris nėra susietas su URL, ir URL, kuris nėra susietas su puslapiu.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="9a6eb-124">Todėl galima sukeisti URL turinį be prastovos ir lengviau valdyti peradresavimą.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="9a6eb-125">Naujo puslapio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="9a6eb-125">Add a new page</span></span>

<span data-ttu-id="9a6eb-126">Norėdami į savo svetainę įtraukti naują puslapį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="9a6eb-127">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="9a6eb-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="9a6eb-128">Pasirinkite **Naujas puslapis**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-128">Select **New Page**.</span></span>
1. <span data-ttu-id="9a6eb-129">Dialogo lange **Naujas puslapis** pasirinkite šabloną ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="9a6eb-130">Lauke **Puslapio pavadinimas** įveskite puslapio pavadinimą, (pavyzdžiui, **Mano naujas puslapis**).</span><span class="sxs-lookup"><span data-stu-id="9a6eb-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="9a6eb-131">Lauke **URL** įveskite eilutę (kintamuosius URL duomenis), kad būtų įvestas visas URL (pavyzdžiui, **manonaujaspuslapis**).</span><span class="sxs-lookup"><span data-stu-id="9a6eb-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="9a6eb-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-132">Select **OK**.</span></span> <span data-ttu-id="9a6eb-133">Atidaroma puslapio rengyklė.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-133">The page editor appears.</span></span> <span data-ttu-id="9a6eb-134">Atkreipkite dėmesį, kad pagal jūsų pasirinktą šabloną antraštė ir poraštė yra automatiškai įtrauktos į puslapį.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="9a6eb-135">Puslapio struktūroje pasirinkite vietą **Pagrindinis**, pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9a6eb-136">Pasirinkite **Konteineris**, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="9a6eb-137">Pasirinkite **Paslankusis konteineris**, tada – daugtaškio mygtuką ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="9a6eb-138">Pasirinkite **Raiškiojo turinio blokas** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="9a6eb-139">Pasirinkite **Raiškiojo turinio blokas**, tada – daugtaškio mygtuką ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="9a6eb-140">Pasirinkite **Raiškiojo turinio bloko elementas** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="9a6eb-141">Dešinėje esančioje ypatybių srityje pasirinkite **Pastraipa**, tada lauke įveskite **Mano testinis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="9a6eb-142">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="9a6eb-143">Lauke **Komentarai** įveskite **Įtrauktas naujas puslapis** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="9a6eb-144">Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="9a6eb-145">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="9a6eb-146">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-146">Select **Publish**.</span></span>
1. <span data-ttu-id="9a6eb-147">Naršymo kelyje (kelio nuorodose) pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="9a6eb-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="9a6eb-148">Kairėje esančioje naršymo srityje pasirinkite **URL adresai**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="9a6eb-149">Sąraše raskite ir pasirinkite savo URL (**manonaujaspuslapis**).</span><span class="sxs-lookup"><span data-stu-id="9a6eb-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="9a6eb-150">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="9a6eb-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a6eb-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9a6eb-151">Additional resources</span></span>

[<span data-ttu-id="9a6eb-152">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="9a6eb-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="9a6eb-153">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="9a6eb-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="9a6eb-154">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="9a6eb-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="9a6eb-155">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="9a6eb-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="9a6eb-156">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="9a6eb-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="9a6eb-157">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="9a6eb-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="9a6eb-158">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="9a6eb-158">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="9a6eb-159">Sukurti dinaminius e-komercijos puslapius pagal URL parameterus</span><span class="sxs-lookup"><span data-stu-id="9a6eb-159">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
