---
title: Įtraukti naują svetainės puslapį
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ įtraukti naują svetainės puslapį.
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
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797556"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="73466-103">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="73466-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="73466-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ įtraukti naują svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="73466-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="73466-105">Svetainei sukūrus šablonų ir fragmentų, kitas veiksmas yra pradėti kurti puslapius, kuriuose jie naudojami.</span><span class="sxs-lookup"><span data-stu-id="73466-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="73466-106">Norėdami pradėti, turite pasirinkti šabloną arba maketą, puslapio pavadinimą ir puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="73466-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="73466-107">Šablonas arba maketas</span><span class="sxs-lookup"><span data-stu-id="73466-107">Template or layout</span></span>

<span data-ttu-id="73466-108">Naujam puslapiui galite naudoti šabloną arba maketą.</span><span class="sxs-lookup"><span data-stu-id="73466-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="73466-109">Norėdami gauti daugiau informacijos, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="73466-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="73466-110">Puslapio pavadinimas</span><span class="sxs-lookup"><span data-stu-id="73466-110">Page name</span></span>

<span data-ttu-id="73466-111">Jūsų puslapio pavadinimas turi būti unikalus.</span><span class="sxs-lookup"><span data-stu-id="73466-111">The page name must be unique to your page.</span></span> <span data-ttu-id="73466-112">Jis turi būti aprašomasis, kad galėtumėte lengvai jį rasti ir kiti žmonės žinotų, kam puslapis skirtas.</span><span class="sxs-lookup"><span data-stu-id="73466-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="73466-113">Puslapio pavadinimą pasirinkite atidžiai, nes jo negalima pakeisti vėliau.</span><span class="sxs-lookup"><span data-stu-id="73466-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="73466-114">Puslapio URL</span><span class="sxs-lookup"><span data-stu-id="73466-114">Page URL</span></span>

<span data-ttu-id="73466-115">Galite pasirinkti, kad būtų galima įvesti naujo puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="73466-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="73466-116">Sukūrę puslapį, galite įvesti eilutę, kuri bus naudojama visam URL sudaryti.</span><span class="sxs-lookup"><span data-stu-id="73466-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="73466-117">Ši eilutė vadinama santykiniu URL arba kintamaisiais URL duomenimis.</span><span class="sxs-lookup"><span data-stu-id="73466-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="73466-118">Tada pagal kintamuosius URL duomenis sugeneruojamas visas URL ir jam priskiriamas naujasis puslapis.</span><span class="sxs-lookup"><span data-stu-id="73466-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="73466-119">Kintamuosius URL duomenis galite pakeisti vėliau, prieš publikuodami puslapį.</span><span class="sxs-lookup"><span data-stu-id="73466-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="73466-120">Norėdami gauti daugiau informacijos, žr. [Puslapio URL sukūrimas](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="73466-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="73466-121">„Dynamics 365 Commerce“ atsieja URL adresus ir turinį.</span><span class="sxs-lookup"><span data-stu-id="73466-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="73466-122">Kitaip tariant, galima sukurti puslapį, kuris nėra susietas su URL, ir URL, kuris nėra susietas su puslapiu.</span><span class="sxs-lookup"><span data-stu-id="73466-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="73466-123">Todėl galima sukeisti URL turinį be prastovos ir lengviau valdyti peradresavimą.</span><span class="sxs-lookup"><span data-stu-id="73466-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="73466-124">Naujo puslapio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="73466-124">Add a new page</span></span>

<span data-ttu-id="73466-125">Norėdami į savo svetainę įtraukti naują puslapį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="73466-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="73466-126">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="73466-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="73466-127">Pasirinkite **Naujas puslapis**.</span><span class="sxs-lookup"><span data-stu-id="73466-127">Select **New Page**.</span></span>
1. <span data-ttu-id="73466-128">Dialogo lange **Naujas puslapis** pasirinkite šabloną ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="73466-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="73466-129">Lauke **Puslapio pavadinimas** įveskite puslapio pavadinimą, (pavyzdžiui, **Mano naujas puslapis**).</span><span class="sxs-lookup"><span data-stu-id="73466-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="73466-130">Lauke **URL** įveskite eilutę (kintamuosius URL duomenis), kad būtų įvestas visas URL (pavyzdžiui, **manonaujaspuslapis**).</span><span class="sxs-lookup"><span data-stu-id="73466-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="73466-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="73466-131">Select **OK**.</span></span> <span data-ttu-id="73466-132">Atidaroma puslapio rengyklė.</span><span class="sxs-lookup"><span data-stu-id="73466-132">The page editor appears.</span></span> <span data-ttu-id="73466-133">Atkreipkite dėmesį, kad pagal jūsų pasirinktą šabloną antraštė ir poraštė yra automatiškai įtrauktos į puslapį.</span><span class="sxs-lookup"><span data-stu-id="73466-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="73466-134">Puslapio struktūroje pasirinkite vietą **Pagrindinis**, pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="73466-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="73466-135">Pasirinkite **Konteineris**, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="73466-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="73466-136">Pasirinkite **Paslankusis konteineris**, tada – daugtaškio mygtuką ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="73466-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="73466-137">Pasirinkite **Raiškiojo turinio blokas** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="73466-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="73466-138">Pasirinkite **Raiškiojo turinio blokas**, tada – daugtaškio mygtuką ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="73466-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="73466-139">Pasirinkite **Raiškiojo turinio bloko elementas** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="73466-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="73466-140">Dešinėje esančioje ypatybių srityje pasirinkite **Pastraipa**, tada lauke įveskite **Mano bandomasis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="73466-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="73466-141">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="73466-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="73466-142">Lauke **Komentarai** įveskite **Įtrauktas naujas puslapis** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="73466-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="73466-143">Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="73466-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="73466-144">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="73466-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="73466-145">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="73466-145">Select **Publish**.</span></span>
1. <span data-ttu-id="73466-146">Naršymo kelyje (kelio nuorodose) pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="73466-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="73466-147">Kairėje esančioje naršymo srityje pasirinkite **URL adresai**.</span><span class="sxs-lookup"><span data-stu-id="73466-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="73466-148">Sąraše raskite ir pasirinkite savo URL (**manonaujaspuslapis**).</span><span class="sxs-lookup"><span data-stu-id="73466-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="73466-149">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="73466-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73466-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="73466-150">Additional resources</span></span>

[<span data-ttu-id="73466-151">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="73466-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="73466-152">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="73466-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="73466-153">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="73466-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="73466-154">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="73466-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="73466-155">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="73466-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="73466-156">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="73466-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="73466-157">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="73466-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="73466-158">Sukurti dinaminius e-komercijos puslapius pagal URL parametrus</span><span class="sxs-lookup"><span data-stu-id="73466-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
