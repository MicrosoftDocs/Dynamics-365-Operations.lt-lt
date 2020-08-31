---
title: Įtraukti logotipą
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti logotipą.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 62b8237fa0c30fa9d901d670de38416cf8615c8d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686651"
---
# <a name="add-a-logo"></a><span data-ttu-id="0b5c2-103">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="0b5c2-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0b5c2-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti logotipą.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0b5c2-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="0b5c2-105">Overview</span></span>

<span data-ttu-id="0b5c2-106">Kuriant svetainę vienas iš pirmųjų atliekamų veiksmų yra įmonės ar prekės ženklo logotipo įtraukimas į svetainės antraštę.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="0b5c2-107">„Dynamics 365 Commerce“ internetiniame darbo pradžios rinkinyje yra modulis, kurį naudojant šią užduotį atlikti lengva.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="0b5c2-108">Logotipą galite įtraukti tiesiai į šabloną, maketą arba puslapį.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="0b5c2-109">Tokiu būdu galite lengvai keisti logotipą, kuris rodomas konkrečiuose puslapiuose arba puslapių grupėse.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="0b5c2-110">Tačiau šioje temoje aprašoma dažniausiai pasitaikanti situacija, kai logotipas įtraukiamas į antraštės fragmentą, kurį galima pakartotinai naudoti visuose svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0b5c2-111">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="0b5c2-111">Prerequisites</span></span>

<span data-ttu-id="0b5c2-112">Kad galėtumėte įtraukti logotipą į visus svetainės puslapius, turite atlikti tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="0b5c2-113">Įkelkite savo logotipą į medijos biblioteką.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="0b5c2-114">Sukurkite antraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-114">Create a header fragment.</span></span> <span data-ttu-id="0b5c2-115">Daugiau informacijos apie tai, kaip kurti ir naudoti fragmentus, rasite temoje [Darbas su fragmentais](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="0b5c2-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="0b5c2-116">Antraštės fragmentą įtraukite į šabloną, kuris svetainės puslapiuose naudojamas kaip jų maketo ir modulių parinktys.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="0b5c2-117">Daugiau informacijos apie šablonus rasite temoje [Darbas su šablonais](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="0b5c2-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="0b5c2-118">Logotipo įtraukimas į antraštės fragmentą</span><span class="sxs-lookup"><span data-stu-id="0b5c2-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="0b5c2-119">Norėdami logotipą įtraukti į svetainės antraštės fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="0b5c2-120">Kairėje naršymo srityje pasirinkite **Fragmentai**.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="0b5c2-121">Pasirinkite sukurtą antraštės fragmentą, tada – **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="0b5c2-122">Išplėskite antraštės modulį.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-122">Expand the header module.</span></span>
1. <span data-ttu-id="0b5c2-123">Antraštės modulio ypatybių srityje pateikite vaizdą ir saitą į logotipą.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="0b5c2-124">Įrašykite antraštės fragmentą, baikite redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="0b5c2-125">Publikavus atnaujintą antraštės fragmentą, visuose svetainės puslapiuose, kuriuose naudojamas šablonas su šiuo antraštės fragmentu, bus rodomas jūsų logotipas.</span><span class="sxs-lookup"><span data-stu-id="0b5c2-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b5c2-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0b5c2-126">Additional resources</span></span>

[<span data-ttu-id="0b5c2-127">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="0b5c2-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0b5c2-128">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="0b5c2-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0b5c2-129">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="0b5c2-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="0b5c2-130">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="0b5c2-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0b5c2-131">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="0b5c2-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0b5c2-132">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="0b5c2-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0b5c2-133">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="0b5c2-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

