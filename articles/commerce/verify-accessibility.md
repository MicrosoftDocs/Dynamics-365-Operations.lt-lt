---
title: Patikrinti puslapio turinio pritaikymą neįgaliesiems
description: Šioje temoje aprašoma, kaip patikrinti „Microsoft Dynamics 365 Commerce“ puslapių turinio pritaikymą neįgaliesiems.
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 70604ed16d72e519724aeb2c33bd4a91a8b26c8c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946051"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="2ee6b-103">Patikrinti puslapio turinio pritaikymą neįgaliesiems</span><span class="sxs-lookup"><span data-stu-id="2ee6b-103">Verify page content accessibility</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2ee6b-104">Šioje temoje aprašoma, kaip patikrinti „Microsoft Dynamics 365 Commerce“ puslapių turinio pritaikymą neįgaliesiems.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2ee6b-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="2ee6b-105">Overview</span></span>

<span data-ttu-id="2ee6b-106">Baigę keisti puslapį, turėtumėte įsitikinti, kad turinys pasiekiamas visiems žiniatinklio vartotojams.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="2ee6b-107">Naudodami „Commerce“ kūrimo įrankius, galite lengvai patikrinti puslapio turinio pritaikymą neįgaliesiems integruotoje paslaugoje [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="2ee6b-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="2ee6b-108">Ši paslauga patikrina jūsų puslapio turinį pagal naujausias [Žiniatinklio konsorciumo W3C pritaikymo neįgaliesiems](https://www.w3.org/standards/webdesign/accessibility) gaires.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="2ee6b-109">Prieš naudojant paslaugą [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/), nuomotojo arba svetainės lygiu reikia įjungti jos integravimą.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="2ee6b-110">Paslaugos „Microsoft Accessibility Insights“ įjungimas visose nuomotojo svetainėse</span><span class="sxs-lookup"><span data-stu-id="2ee6b-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="2ee6b-111">Norėdami įjungti paslaugos [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/) integravimą visose nuomotojo „Commerce“ svetainėse, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="2ee6b-112">Norėdami pasiekti nuomotojo parametrus, turite būti prisijungę prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="2ee6b-113">Prisijunkite prie „Commerce“ kaip sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="2ee6b-114">Kairiojoje naršymo srityje pasirinkite **Nuomotojo parametrai** (šalia krumpliaračio simbolio), kad juos išplėstumėte.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="2ee6b-115">Dalyje **Nuomotojo parametrai** pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="2ee6b-116">Nustatykite parinkties **Pritaikymo neįgaliesiems tikrinimas** vertę **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="2ee6b-117">Paslaugos „Microsoft Accessibility Insights“ įjungimas vienoje svetainėje</span><span class="sxs-lookup"><span data-stu-id="2ee6b-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="2ee6b-118">Norėdami įjungti paslaugos [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/) integravimą vienoje „Commerce“ svetainėje, atlikite toliau pateikiamus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="2ee6b-119">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="2ee6b-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2ee6b-120">Kairiojoje naršymo srityje pasirinkite ir išskleiskite **Svetainės parametrai**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="2ee6b-121">Dalyje **Svetainės parametrai** pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="2ee6b-122">Nustatykite parinkties **Pritaikymo neįgaliesiems tikrinimas** vertę **Įjungta**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="2ee6b-123">Pagrindinio puslapio turinio pritaikymo neįgaliesiems patikrinimas</span><span class="sxs-lookup"><span data-stu-id="2ee6b-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="2ee6b-124">Norėdami naudoti integruotą paslaugą [„Microsoft Accessibility Insights“](https://accessibilityinsights.io/), kad nuskaitytumėte ir patikrintumėte pagrindinio „Commerce“ puslapio turinį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2ee6b-125">Dalyje **Svetainės** pasirinkite **„Fabrikam“** (arba savo svetainės pavadinimą).</span><span class="sxs-lookup"><span data-stu-id="2ee6b-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2ee6b-126">Kairiojoje naršymo srityje pasirinkite **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="2ee6b-127">Raskite ir pasirinkite pagrindinį puslapį, kad jis būtų atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="2ee6b-128">Komandų juostoje pasirinkite **Tikrinti pritaikymą neįgaliesiems**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="2ee6b-129">Atidaromas puslapis **Tikrinti pritaikymą neįgaliesiems**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="2ee6b-130">Nuskaitymui pasibaigus, peržiūrėkite ataskaitos turinį.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="2ee6b-131">Jei kurių nors patikrinimų rezultatas neigiamas, pasirinkite elementus, kurių tikrinimo rezultatai neigiami, kad išplėstumėte elementus ir pamatytumėte daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="2ee6b-132">Norėdami uždaryti ataskaitą ją peržiūrėję, slinkite į puslapio **Tikrinti pritaikymą neįgaliesiems** apačią ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2ee6b-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ee6b-133">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="2ee6b-133">Additional resources</span></span>

[<span data-ttu-id="2ee6b-134">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="2ee6b-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="2ee6b-135">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="2ee6b-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2ee6b-136">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="2ee6b-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2ee6b-137">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="2ee6b-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="2ee6b-138">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="2ee6b-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2ee6b-139">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="2ee6b-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="2ee6b-140">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="2ee6b-140">Enrich a category landing page</span></span>](enrich-category-page.md)
