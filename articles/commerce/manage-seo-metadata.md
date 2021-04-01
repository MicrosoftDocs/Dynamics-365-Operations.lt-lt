---
title: Tvarkyti SEO metaduomenis
description: Šioje temoje aprašoma, kaip valdyti ieškos modulio optimizavimo (SEO) metaduomenis programoje „Microsoft Dynamics 365 Commerce“.
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
ms.openlocfilehash: 00942befef9f9b6a878766bbbb5341426e31db2c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252611"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="e208f-103">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="e208f-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e208f-104">Šioje temoje aprašoma, kaip valdyti ieškos modulio optimizavimo (SEO) metaduomenis programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="e208f-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e208f-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="e208f-105">Overview</span></span>

<span data-ttu-id="e208f-106">Svetainės SEO metaduomenys gali būti valdomi naudojant svetainės struktūromis ir puslapio metaduomenimis.</span><span class="sxs-lookup"><span data-stu-id="e208f-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="e208f-107">Svetainės struktūros</span><span class="sxs-lookup"><span data-stu-id="e208f-107">Site maps</span></span>

<span data-ttu-id="e208f-108">Svetainės struktūra yra žiniatinklio svetainės puslapių XML formatu kompiuterio skaitomas sąrašas.</span><span class="sxs-lookup"><span data-stu-id="e208f-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="e208f-109">Jis skirtas vartoti ieškos moduliuose, kad jie galėtų pateikti geresnius ieškos rezultatus jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="e208f-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="e208f-110">Gali būti, kad svetainės struktūros neautomatiniu būdu parenkamos ieškos moduliui vartoti arba publikuojamos faile robots.txt.</span><span class="sxs-lookup"><span data-stu-id="e208f-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="e208f-111">„Dynamics 365 Commerce“ palaiko automatinį svetainės struktūrų generavimą.</span><span class="sxs-lookup"><span data-stu-id="e208f-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="e208f-112">Svetainės struktūros atnaujinamos automatiškai, kai puslapiai publikuojami ar jų publikavimas atšaukiamas.</span><span class="sxs-lookup"><span data-stu-id="e208f-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="e208f-113">Svetainės struktūros generavimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="e208f-113">Turn on site map generation</span></span>

1. <span data-ttu-id="e208f-114">Prisijunkite prie turinio kūrimo įrankio.</span><span class="sxs-lookup"><span data-stu-id="e208f-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="e208f-115">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="e208f-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e208f-116">Kairėje naršymo srityje pasirinkite **Svetainės valdymas**.</span><span class="sxs-lookup"><span data-stu-id="e208f-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="e208f-117">Įsitikinkite, kad įjungta parinktis **Svetainės struktūros įgalintos**.</span><span class="sxs-lookup"><span data-stu-id="e208f-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="e208f-118">Puslapio metaduomenys</span><span class="sxs-lookup"><span data-stu-id="e208f-118">Page metadata</span></span>

<span data-ttu-id="e208f-119">„Dynamics 365 Commerce“ galite tvarkyti atskirų puslapių SEO metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="e208f-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="e208f-120">Šią informaciją galite peržiūrėti ir modifikuoti puslapio konteinerio skyriuje **SEO ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="e208f-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="e208f-121">Toliau nurodytos SEO metaduomenų ypatybės yra palaikomos:</span><span class="sxs-lookup"><span data-stu-id="e208f-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="e208f-122">Pareigos</span><span class="sxs-lookup"><span data-stu-id="e208f-122">Title</span></span>
- <span data-ttu-id="e208f-123">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="e208f-123">Description</span></span>
- <span data-ttu-id="e208f-124">SEO raktažodžiai</span><span class="sxs-lookup"><span data-stu-id="e208f-124">SEO keywords</span></span>
- <span data-ttu-id="e208f-125">„Aria“ žymos</span><span class="sxs-lookup"><span data-stu-id="e208f-125">Aria labels</span></span>
- <span data-ttu-id="e208f-126">noindex</span><span class="sxs-lookup"><span data-stu-id="e208f-126">noindex</span></span>
- <span data-ttu-id="e208f-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="e208f-127">nofollow</span></span>
- <span data-ttu-id="e208f-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="e208f-128">noarchive</span></span>
- <span data-ttu-id="e208f-129">nocache</span><span class="sxs-lookup"><span data-stu-id="e208f-129">nocache</span></span>
- <span data-ttu-id="e208f-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="e208f-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="e208f-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="e208f-131">nosnippet</span></span>
- <span data-ttu-id="e208f-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="e208f-132">noImageIndex</span></span>
- <span data-ttu-id="e208f-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="e208f-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="e208f-134">Puslapio metaduomenų modifikavimas</span><span class="sxs-lookup"><span data-stu-id="e208f-134">Modify page metadata</span></span>

<span data-ttu-id="e208f-135">Norėdami modifikuoti metaduomenis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e208f-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="e208f-136">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="e208f-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e208f-137">Kairėje naršymo srityje pasirinkite **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="e208f-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="e208f-138">Pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="e208f-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="e208f-139">Komandų juostoje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e208f-139">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="e208f-140">Dešiniojoje ypatybių srityje išplėskite **Numatytosios metažymės**.</span><span class="sxs-lookup"><span data-stu-id="e208f-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="e208f-141">Norėdami įtraukti naują metažymę, pasirinkite **Įtraukti** ir lauke įveskite žymę.</span><span class="sxs-lookup"><span data-stu-id="e208f-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="e208f-142">Norėdami pašalinti esamą metažymę, pasirinkite šiukšliadėžės simbolį jos dešinėje.</span><span class="sxs-lookup"><span data-stu-id="e208f-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="e208f-143">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="e208f-143">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e208f-144">Lauke **Komentarai** įveskite **Atnaujintos metažymės** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e208f-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="e208f-145">Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="e208f-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="e208f-146">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="e208f-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="e208f-147">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="e208f-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e208f-148">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e208f-148">Additional resources</span></span>

[<span data-ttu-id="e208f-149">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="e208f-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e208f-150">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="e208f-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e208f-151">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="e208f-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e208f-152">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="e208f-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="e208f-153">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="e208f-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="e208f-154">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="e208f-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="e208f-155">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="e208f-155">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="e208f-156">Sukurti dinaminius e-komercijos puslapius pagal URL parameterus</span><span class="sxs-lookup"><span data-stu-id="e208f-156">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]