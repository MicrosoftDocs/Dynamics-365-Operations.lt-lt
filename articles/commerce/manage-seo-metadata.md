---
title: Tvarkyti SEO metaduomenis
description: Šioje temoje aprašoma, kaip valdyti ieškos modulio optimizavimo (SEO) metaduomenis programoje „Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794216"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="637fb-103">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="637fb-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="637fb-104">Šioje temoje aprašoma, kaip valdyti ieškos modulio optimizavimo (SEO) metaduomenis programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="637fb-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="637fb-105">Svetainės SEO metaduomenys gali būti valdomi naudojant svetainės struktūromis ir puslapio metaduomenimis.</span><span class="sxs-lookup"><span data-stu-id="637fb-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="637fb-106">Svetainės struktūros</span><span class="sxs-lookup"><span data-stu-id="637fb-106">Site maps</span></span>

<span data-ttu-id="637fb-107">Svetainės struktūra yra žiniatinklio svetainės puslapių XML formatu kompiuterio skaitomas sąrašas.</span><span class="sxs-lookup"><span data-stu-id="637fb-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="637fb-108">Jis skirtas vartoti ieškos moduliuose, kad jie galėtų pateikti geresnius ieškos rezultatus jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="637fb-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="637fb-109">Gali būti, kad svetainės struktūros neautomatiniu būdu parenkamos ieškos moduliui vartoti arba publikuojamos faile robots.txt.</span><span class="sxs-lookup"><span data-stu-id="637fb-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="637fb-110">„Dynamics 365 Commerce“ palaiko automatinį svetainės struktūrų generavimą.</span><span class="sxs-lookup"><span data-stu-id="637fb-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="637fb-111">Svetainės struktūros atnaujinamos automatiškai, kai puslapiai publikuojami ar jų publikavimas atšaukiamas.</span><span class="sxs-lookup"><span data-stu-id="637fb-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="637fb-112">Svetainės struktūros generavimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="637fb-112">Turn on site map generation</span></span>

1. <span data-ttu-id="637fb-113">Prisijunkite prie turinio kūrimo įrankio.</span><span class="sxs-lookup"><span data-stu-id="637fb-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="637fb-114">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="637fb-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="637fb-115">Kairėje naršymo srityje pasirinkite **Svetainės valdymas**.</span><span class="sxs-lookup"><span data-stu-id="637fb-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="637fb-116">Įsitikinkite, kad įjungta parinktis **Svetainės struktūros įgalintos**.</span><span class="sxs-lookup"><span data-stu-id="637fb-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="637fb-117">Puslapio metaduomenys</span><span class="sxs-lookup"><span data-stu-id="637fb-117">Page metadata</span></span>

<span data-ttu-id="637fb-118">„Dynamics 365 Commerce“ galite tvarkyti atskirų puslapių SEO metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="637fb-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="637fb-119">Šią informaciją galite peržiūrėti ir modifikuoti puslapio konteinerio skyriuje **SEO ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="637fb-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="637fb-120">Toliau nurodytos SEO metaduomenų ypatybės yra palaikomos:</span><span class="sxs-lookup"><span data-stu-id="637fb-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="637fb-121">Pareigos</span><span class="sxs-lookup"><span data-stu-id="637fb-121">Title</span></span>
- <span data-ttu-id="637fb-122">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="637fb-122">Description</span></span>
- <span data-ttu-id="637fb-123">SEO raktažodžiai</span><span class="sxs-lookup"><span data-stu-id="637fb-123">SEO keywords</span></span>
- <span data-ttu-id="637fb-124">„Aria“ žymos</span><span class="sxs-lookup"><span data-stu-id="637fb-124">Aria labels</span></span>
- <span data-ttu-id="637fb-125">noindex</span><span class="sxs-lookup"><span data-stu-id="637fb-125">noindex</span></span>
- <span data-ttu-id="637fb-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="637fb-126">nofollow</span></span>
- <span data-ttu-id="637fb-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="637fb-127">noarchive</span></span>
- <span data-ttu-id="637fb-128">nocache</span><span class="sxs-lookup"><span data-stu-id="637fb-128">nocache</span></span>
- <span data-ttu-id="637fb-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="637fb-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="637fb-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="637fb-130">nosnippet</span></span>
- <span data-ttu-id="637fb-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="637fb-131">noImageIndex</span></span>
- <span data-ttu-id="637fb-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="637fb-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="637fb-133">Puslapio metaduomenų modifikavimas</span><span class="sxs-lookup"><span data-stu-id="637fb-133">Modify page metadata</span></span>

<span data-ttu-id="637fb-134">Norėdami modifikuoti metaduomenis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="637fb-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="637fb-135">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="637fb-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="637fb-136">Kairėje naršymo srityje pasirinkite **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="637fb-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="637fb-137">Pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="637fb-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="637fb-138">Komandų juostoje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="637fb-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="637fb-139">Dešiniojoje ypatybių srityje išplėskite **Numatytosios metažymės**.</span><span class="sxs-lookup"><span data-stu-id="637fb-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="637fb-140">Norėdami įtraukti naują metažymę, pasirinkite **Įtraukti** ir lauke įveskite žymę.</span><span class="sxs-lookup"><span data-stu-id="637fb-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="637fb-141">Norėdami pašalinti esamą metažymę, pasirinkite šiukšliadėžės simbolį jos dešinėje.</span><span class="sxs-lookup"><span data-stu-id="637fb-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="637fb-142">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="637fb-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="637fb-143">Lauke **Komentarai** įveskite **Atnaujintos metažymės** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="637fb-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="637fb-144">Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="637fb-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="637fb-145">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="637fb-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="637fb-146">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="637fb-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="637fb-147">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="637fb-147">Additional resources</span></span>

[<span data-ttu-id="637fb-148">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="637fb-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="637fb-149">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="637fb-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="637fb-150">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="637fb-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="637fb-151">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="637fb-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="637fb-152">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="637fb-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="637fb-153">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="637fb-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="637fb-154">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="637fb-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="637fb-155">Sukurti dinaminius e-komercijos puslapius pagal URL parametrus</span><span class="sxs-lookup"><span data-stu-id="637fb-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
