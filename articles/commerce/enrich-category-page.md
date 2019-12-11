---
title: Papildyti kategorijos nukreipimo puslapį
description: Šioje temoje aptariamas kategorijos puslapių papildymas sprendime „Dynamics 365 Commerce“.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8d735b215132b90ca786d6967589496bee73f4d9
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697594"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="21651-103">Papildyti kategorijos nukreipimo puslapį</span><span class="sxs-lookup"><span data-stu-id="21651-103">Enrich a category landing page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="21651-104">Šioje temoje aptariamas kategorijos puslapių papildymas sprendime „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="21651-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="21651-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="21651-105">Overview</span></span>

<span data-ttu-id="21651-106">„Commerce“ pateikiamas numatytasis kategorijos nukreipimo puslapis, kuris naudojamas, kai rodomi kategorijos duomenys.</span><span class="sxs-lookup"><span data-stu-id="21651-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="21651-107">Numatytame kategorijos puslapyje yra būtini elementai, pvz., tikslinimo priemonės, produktų išdėstymas pagal kategorijas, rūšiavimo parinktys, pasirinkimo suvestinė ir skaidymo į puslapius valdikliai.</span><span class="sxs-lookup"><span data-stu-id="21651-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="21651-108">Tačiau užuot naudoję numatytąjį kategorijos puslapį, galbūt norėsite naudoti papildytą kategorijos nukreipimo puslapį, kuriame yra daugiau turinio ir konkretesnių elementų.</span><span class="sxs-lookup"><span data-stu-id="21651-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="21651-109">Tipiškas papildymas gali apimti tam tikros kategorijos rinkodaros turinio įtraukimą į kategorijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="21651-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="21651-110">Į šį turinį gali būti įtraukti kryžminių kategorijų produktų išdėstymas kryžminio pardavimo tikslais, redakcijos sąrašams, atvaizdams, vaizdo įrašams ir kitiems tekstams.</span><span class="sxs-lookup"><span data-stu-id="21651-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="21651-111">Galite modifikuoti numatytąjį kategorijos puslapį arba nustatyti konkrečiai kategorijai kitą kategorijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="21651-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Papildytas kategorijos nukreipimo puslapis](./media/CategoryLandingPages.png)

<span data-ttu-id="21651-113">Kūrimo įrankyje puslapyje **Produktas** yra priskirtų svetainei kanalo kategorijų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="21651-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="21651-114">Jei kategorijos puslapyje pasirinkta būsena **Papildyta**, tas puslapis yra papildytas.</span><span class="sxs-lookup"><span data-stu-id="21651-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="21651-115">Kitu atveju kategorijai naudojami numatytasis kategorijos puslapis ir turinys.</span><span class="sxs-lookup"><span data-stu-id="21651-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="21651-116">Galite peržiūrėti ir papildytų, ir nepapildytų kategorijų puslapių konkrečiai kategorijai, pasirinkdami kategorijos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="21651-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="21651-117">Norėdami papildyti kategorijos puslapį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="21651-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="21651-118">Puslapyje **Produktai** pasirinkite kategorijos, kurios kategorijos puslapį norite papildyti, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="21651-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="21651-119">Pasirinktos kategorijos numatytasis kategorijos puslapis atidaromas puslapio rengyklėje.</span><span class="sxs-lookup"><span data-stu-id="21651-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="21651-120">Pasirinkite **Papildyti kategorijos puslapį**.</span><span class="sxs-lookup"><span data-stu-id="21651-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="21651-121">Pasirinkti papildyto kategorijos puslapio šabloną.</span><span class="sxs-lookup"><span data-stu-id="21651-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="21651-122">Jei atliekate tik nedidelius keitimus, galite pasirinkti numatytąjį kategorijos puslapį.</span><span class="sxs-lookup"><span data-stu-id="21651-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="21651-123">Taip pat galite pasirinkti konkretų kategorijos puslapio šabloną.</span><span class="sxs-lookup"><span data-stu-id="21651-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="21651-124">Kai pasirenkate šabloną, atidaroma puslapio rengyklė, o pasirinktas šablonas naudojamas kuriant naują kategorijos puslapį pasirinktai kategorijai.</span><span class="sxs-lookup"><span data-stu-id="21651-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="21651-125">Puslapis paimamas ir užrakinamas, tad dabar galite atlikti savo keitimus.</span><span class="sxs-lookup"><span data-stu-id="21651-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="21651-126">Moduliai, kurie naudoja kategorijos specifikacijos duomenis, naudoja jūsų pasirinktoje kategorijoje esančius duomenis.</span><span class="sxs-lookup"><span data-stu-id="21651-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="21651-127">Pasirinkto šablono parametrai nustato keitimus, kuriuos galite atlikti.</span><span class="sxs-lookup"><span data-stu-id="21651-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21651-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="21651-128">Additional resources</span></span>

[<span data-ttu-id="21651-129">Modifikuoti esamą svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="21651-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="21651-130">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="21651-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="21651-131">Pasirinkti puslapių maketus</span><span class="sxs-lookup"><span data-stu-id="21651-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="21651-132">Tvarkyti SEO metaduomenis</span><span class="sxs-lookup"><span data-stu-id="21651-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="21651-133">Įrašyti, peržiūrėti ir publikuoti puslapį</span><span class="sxs-lookup"><span data-stu-id="21651-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="21651-134">Papildyti produkto puslapį</span><span class="sxs-lookup"><span data-stu-id="21651-134">Enrich a product page</span></span>](enrich-product-page.md)
