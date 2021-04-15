---
title: Patikrinti puslapio turinio pritaikymą neįgaliesiems
description: Šioje temoje aprašoma, kaip patikrinti „Microsoft Dynamics 365 Commerce“ puslapių turinio pritaikymą neįgaliesiems.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791636"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="413df-103">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="413df-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="413df-104">Šioje temoje aprašoma, kaip patikrinti „Microsoft Dynamics 365 Commerce“ puslapių turinio pritaikymą neįgaliesiems.</span><span class="sxs-lookup"><span data-stu-id="413df-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="413df-105">Baigę keisti puslapį, turėtumėte įsitikinti, kad turinys pasiekiamas visiems žiniatinklio vartotojams.</span><span class="sxs-lookup"><span data-stu-id="413df-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="413df-106">Naudodami „Commerce“ kūrimo įrankius, galite lengvai patikrinti puslapio turinio pritaikymą neįgaliesiems integruotoje paslaugoje [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="413df-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="413df-107">Ši paslauga patikrina jūsų puslapio turinį pagal naujausias [Žiniatinklio konsorciumo W3C pritaikymo neįgaliesiems](https://www.w3.org/standards/webdesign/accessibility) gaires.</span><span class="sxs-lookup"><span data-stu-id="413df-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="413df-108">Prieš naudojant paslaugą [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/), nuomotojo arba svetainės lygiu reikia įjungti jos integravimą.</span><span class="sxs-lookup"><span data-stu-id="413df-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="413df-109">Paslaugos „Microsoft Accessibility Insights“ įjungimas visose nuomotojo svetainėse</span><span class="sxs-lookup"><span data-stu-id="413df-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="413df-110">Norėdami įjungti paslaugos [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/) integravimą visose nuomotojo „Commerce“ svetainėse, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="413df-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="413df-111">Norėdami pasiekti nuomotojo parametrus, turite būti prisijungę prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="413df-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="413df-112">Prisijunkite prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="413df-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="413df-113">Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="413df-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="413df-114">Dalyje **Nuomotojo parametrai** pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="413df-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="413df-115">Nustatykite parinkties **Pritaikymo neįgaliesiems tikrinimas** vertę **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="413df-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="413df-116">Paslaugos „Microsoft Accessibility Insights“ įjungimas vienoje svetainėje</span><span class="sxs-lookup"><span data-stu-id="413df-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="413df-117">Norėdami įjungti paslaugos [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/) integravimą vienoje „Commerce“ svetainėje, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="413df-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="413df-118">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="413df-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="413df-119">Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="413df-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="413df-120">Dalyje **Svetainės parametrai** pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="413df-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="413df-121">Nustatykite parinkties **Pritaikymo neįgaliesiems tikrinimas** vertę **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="413df-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="413df-122">Pagrindinio puslapio turinio pritaikymo neįgaliesiems patikrinimas</span><span class="sxs-lookup"><span data-stu-id="413df-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="413df-123">Norėdami naudoti integruotą paslaugą [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/), kad nuskaitytumėte ir patikrintumėte pagrindinio „Commerce“ puslapio turinį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="413df-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="413df-124">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="413df-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="413df-125">Kairiojoje naršymo srityje pasirinkite **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="413df-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="413df-126">Raskite ir pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="413df-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="413df-127">Komandų juostoje pasirinkite **Tikrinti pritaikymą neįgaliesiems**.</span><span class="sxs-lookup"><span data-stu-id="413df-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="413df-128">Atidaromas puslapis **Tikrinti pritaikymą neįgaliesiems**.</span><span class="sxs-lookup"><span data-stu-id="413df-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="413df-129">Nuskaitymui pasibaigus, peržiūrėkite ataskaitos turinį.</span><span class="sxs-lookup"><span data-stu-id="413df-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="413df-130">Jei kurių nors patikrinimų rezultatas neigiamas, pasirinkite elementus, kurių tikrinimo rezultatai neigiami, kad išplėstumėte elementus ir pamatytumėte daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="413df-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="413df-131">Norėdami uždaryti ataskaitą ją peržiūrėję, slinkite į puslapio **Tikrinti pritaikymą neįgaliesiems** apačią ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="413df-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="413df-132">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="413df-132">Additional resources</span></span>

[<span data-ttu-id="413df-133">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="413df-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="413df-134">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="413df-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="413df-135">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="413df-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="413df-136">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="413df-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="413df-137">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="413df-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="413df-138">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="413df-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="413df-139">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="413df-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="413df-140">Sukurti dinaminius e-komercijos puslapius pagal URL parametrus</span><span class="sxs-lookup"><span data-stu-id="413df-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
