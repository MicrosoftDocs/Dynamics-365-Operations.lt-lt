---
title: Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei
description: Šioje temoje aptariamos ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei, pradedant kūrimu, baigiant gamyba.
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
ms.openlocfilehash: 7c7afed8e4620d5fe49ead47eb6c17d97d7492ad
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002812"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="e0bd5-103">Ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei</span><span class="sxs-lookup"><span data-stu-id="e0bd5-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e0bd5-104">Šioje temoje aptariamos ieškos modulio optimizavimo (SEO) aplinkybės jūsų svetainei, pradedant kūrimu, baigiant gamyba.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="e0bd5-105">Svetainė, kuri vis dar kuriama</span><span class="sxs-lookup"><span data-stu-id="e0bd5-105">A site that is under development</span></span>

<span data-ttu-id="e0bd5-106">Kai svetainė vis dar kuriama, visi svetainės puslapiai turėtų turėti metažymes **NOINDEX** ir **NOFOLLOW**, kad ieškos moduliai savo talpyklose neindeksuotų jūsų svetainės puslapių ir nesaugotų jos kūrimo versijų.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="e0bd5-107">Norint tai sukonfigūruoti, į svetainės puslapio šabloną reikia įtraukti numatytųjų metažymių modulį.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="e0bd5-108">Tada numatytųjų metažymių ypatybės bus pasiekiamos puslapio rengyklės SEO ypatybių dalyje.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="e0bd5-109">Galite naudoti šias ypatybes metažymėms tvarkyti.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="e0bd5-110">Svetainės peržiūros versijos paleidimas</span><span class="sxs-lookup"><span data-stu-id="e0bd5-110">Soft launch of a site</span></span>

<span data-ttu-id="e0bd5-111">Paleidus svetainės peržiūros versiją svetainė pateikiama ribotai auditorijai arba rinkai prieš paleidžiant visą svetainę.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="e0bd5-112">Jei paleisite svetainės peržiūros versiją, turėtumėte palikti metažymes **NOINDEX**.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="e0bd5-113">Taip padėsite užtikrinti, kad peržiūros versija bus prieinama tik ribotai auditorijai, kurią norite pasiekti.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="e0bd5-114">Svetainė, kuri yra gamybos etape</span><span class="sxs-lookup"><span data-stu-id="e0bd5-114">A site that is in production</span></span>

<span data-ttu-id="e0bd5-115">Kai svetainė yra gamybos etape, reikėtų įsitikinti, kad visi svetainės puslapiai yra teisingai pažymėti.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="e0bd5-116">„Microsoft Dynamics 365 Commerce“ naudoja puslapyje įvestą informaciją, kad tame puslapyje sugeneruotų visą SEO informaciją.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="e0bd5-117">Šias funkcijas turi šie moduliai: kategorijos puslapių suvestinė, sąrašo puslapių suvestinė ir produkto puslapių suvestinė.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="e0bd5-118">Ieškos modulio indeksavimui optimizuoti generavimo sistema naudoja ir informaciją iš „Dynamics 365 Commerce“ konfigūruojamų SEO ypatybių, ir konkretaus modulio informaciją.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="e0bd5-119">Dėl svetainės, kuri yra gamybos etape, turėtumėte įsitikinti, kad failas robots. txt leidžia indeksuoti visą svetainę ir kad jame yra saitų į jūsų publikuotą svetainės struktūros dokumentą.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="e0bd5-120">Turėtumėte įjungti svetainės struktūros generavimo funkcijas dalyje **Svetainės parametrai \> Įjungta svetainės struktūra**.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="e0bd5-121">Puslapio SEO parametrai vidinei peržiūrai, ribotoms auditorijoms ir visoms auditorijoms</span><span class="sxs-lookup"><span data-stu-id="e0bd5-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="e0bd5-122">Kadangi „Dynamics 365 Commerce“ palaikomos „ką matau, tą gaunu“ (WYSIWYG) autentifikuotos peržiūros, autoriai gali paruošti savo puslapio turinį nesirūpindami dėl to, kad informacija gali tapti matoma svetainės lankytojams.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="e0bd5-123">Jei puslapis turi būti publikuojamas, bet jo matomumas turi būti apribotas, puslapis turi turėti metažymę **NOINDEX**, kad ieškos moduliai jo neindeksuotų.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="e0bd5-124">Tada, kai puslapis bus paruoštas visoms auditorijoms, turėtų būti visi pagrindiniai SEO metaduomenys, siekiant maksimaliai padidinti ieškos modulio indeksavimo efektyvumą.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="e0bd5-125">Be to, reikia pašalinti metažymę **NOLIMIT**.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0bd5-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e0bd5-126">Additional resources</span></span>

[<span data-ttu-id="e0bd5-127">El. prekybos vartotojų ir vaidmenų valdymas</span><span class="sxs-lookup"><span data-stu-id="e0bd5-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="e0bd5-128">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="e0bd5-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="e0bd5-129">Tvarkyti turinio saugos strategiją (CSP)</span><span class="sxs-lookup"><span data-stu-id="e0bd5-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
