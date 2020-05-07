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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 74229628e48ffb8ac974acd868e325eeca77d91e
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/17/2020
ms.locfileid: "3270055"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="198c7-103">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="198c7-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="198c7-104">Šioje temoje aprašoma, kaip valdyti ieškos modulio optimizavimo (SEO) metaduomenis programoje „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="198c7-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="198c7-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="198c7-105">Overview</span></span>

<span data-ttu-id="198c7-106">Svetainės SEO metaduomenys gali būti valdomi naudojant svetainės struktūromis ir puslapio metaduomenimis.</span><span class="sxs-lookup"><span data-stu-id="198c7-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="198c7-107">Svetainės struktūros</span><span class="sxs-lookup"><span data-stu-id="198c7-107">Site maps</span></span>

<span data-ttu-id="198c7-108">Svetainės struktūra yra žiniatinklio svetainės puslapių XML formatu kompiuterio skaitomas sąrašas.</span><span class="sxs-lookup"><span data-stu-id="198c7-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="198c7-109">Jis skirtas vartoti ieškos moduliuose, kad jie galėtų pateikti geresnius ieškos rezultatus jūsų svetainėje.</span><span class="sxs-lookup"><span data-stu-id="198c7-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="198c7-110">Gali būti, kad svetainės struktūros neautomatiniu būdu parenkamos ieškos moduliui vartoti arba publikuojamos faile robots.txt.</span><span class="sxs-lookup"><span data-stu-id="198c7-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="198c7-111">„Dynamics 365 Commerce“ palaiko automatinį svetainės struktūrų generavimą.</span><span class="sxs-lookup"><span data-stu-id="198c7-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="198c7-112">Svetainės struktūros atnaujinamos automatiškai, kai puslapiai publikuojami ar jų publikavimas atšaukiamas.</span><span class="sxs-lookup"><span data-stu-id="198c7-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="198c7-113">Svetainės struktūros generavimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="198c7-113">Turn on site map generation</span></span>

1. <span data-ttu-id="198c7-114">Prisijunkite prie turinio kūrimo įrankio.</span><span class="sxs-lookup"><span data-stu-id="198c7-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="198c7-115">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="198c7-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="198c7-116">Kairėje naršymo srityje pasirinkite **Svetainės valdymas**.</span><span class="sxs-lookup"><span data-stu-id="198c7-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="198c7-117">Įsitikinkite, kad įjungta parinktis **Svetainės struktūros įgalintos**.</span><span class="sxs-lookup"><span data-stu-id="198c7-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="198c7-118">Puslapio metaduomenys</span><span class="sxs-lookup"><span data-stu-id="198c7-118">Page metadata</span></span>

<span data-ttu-id="198c7-119">„Dynamics 365 Commerce“ galite tvarkyti atskirų puslapių SEO metaduomenis.</span><span class="sxs-lookup"><span data-stu-id="198c7-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="198c7-120">Šią informaciją galite peržiūrėti ir modifikuoti puslapio konteinerio skyriuje **SEO ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="198c7-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="198c7-121">Toliau nurodytos SEO metaduomenų ypatybės yra palaikomos:</span><span class="sxs-lookup"><span data-stu-id="198c7-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="198c7-122">Pareigos</span><span class="sxs-lookup"><span data-stu-id="198c7-122">Title</span></span>
- <span data-ttu-id="198c7-123">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="198c7-123">Description</span></span>
- <span data-ttu-id="198c7-124">SEO raktažodžiai</span><span class="sxs-lookup"><span data-stu-id="198c7-124">SEO keywords</span></span>
- <span data-ttu-id="198c7-125">„Aria“ žymos</span><span class="sxs-lookup"><span data-stu-id="198c7-125">Aria labels</span></span>
- <span data-ttu-id="198c7-126">noindex</span><span class="sxs-lookup"><span data-stu-id="198c7-126">noindex</span></span>
- <span data-ttu-id="198c7-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="198c7-127">nofollow</span></span>
- <span data-ttu-id="198c7-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="198c7-128">noarchive</span></span>
- <span data-ttu-id="198c7-129">nocache</span><span class="sxs-lookup"><span data-stu-id="198c7-129">nocache</span></span>
- <span data-ttu-id="198c7-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="198c7-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="198c7-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="198c7-131">nosnippet</span></span>
- <span data-ttu-id="198c7-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="198c7-132">noImageIndex</span></span>
- <span data-ttu-id="198c7-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="198c7-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="198c7-134">Puslapio metaduomenų modifikavimas</span><span class="sxs-lookup"><span data-stu-id="198c7-134">Modify page metadata</span></span>

<span data-ttu-id="198c7-135">Norėdami modifikuoti metaduomenis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="198c7-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="198c7-136">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="198c7-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="198c7-137">Kairėje naršymo srityje pasirinkite **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="198c7-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="198c7-138">Pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="198c7-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="198c7-139">Komandų juostoje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="198c7-139">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="198c7-140">Dešiniojoje ypatybių srityje išplėskite **Numatytosios metažymės**.</span><span class="sxs-lookup"><span data-stu-id="198c7-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="198c7-141">Norėdami įtraukti naują metažymę, pasirinkite **Įtraukti** ir lauke įveskite žymę.</span><span class="sxs-lookup"><span data-stu-id="198c7-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="198c7-142">Norėdami pašalinti esamą metažymę, pasirinkite šiukšliadėžės simbolį jos dešinėje.</span><span class="sxs-lookup"><span data-stu-id="198c7-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="198c7-143">Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="198c7-143">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="198c7-144">Lauke **Komentarai** įveskite **Atnaujintos metažymės** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="198c7-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="198c7-145">Norėdami peržiūrėti puslapį, pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="198c7-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="198c7-146">Baigę uždarykite peržiūros skirtuką – grįšite į kūrimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="198c7-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="198c7-147">Pasirinkite **Publikuoti**.</span><span class="sxs-lookup"><span data-stu-id="198c7-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="198c7-148">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="198c7-148">Additional resources</span></span>

[<span data-ttu-id="198c7-149">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="198c7-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="198c7-150">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="198c7-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="198c7-151">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="198c7-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="198c7-152">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="198c7-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="198c7-153">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="198c7-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="198c7-154">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="198c7-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="198c7-155">Puslapio turinio pritaikymo neįgaliesiems patikra</span><span class="sxs-lookup"><span data-stu-id="198c7-155">Verify page content accessibility</span></span>](verify-accessibility.md)
