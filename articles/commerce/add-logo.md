---
title: Įtraukti logotipą
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti logotipą.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914628"
---
# <a name="add-a-logo"></a><span data-ttu-id="fd274-103">Įtraukti logotipą</span><span class="sxs-lookup"><span data-stu-id="fd274-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fd274-104">Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ į svetainę įtraukti logotipą.</span><span class="sxs-lookup"><span data-stu-id="fd274-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fd274-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="fd274-105">Overview</span></span>

<span data-ttu-id="fd274-106">Kuriant svetainę vienas iš pirmųjų atliekamų veiksmų yra įmonės ar prekės ženklo logotipo įtraukimas į svetainės antraštę.</span><span class="sxs-lookup"><span data-stu-id="fd274-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="fd274-107">„Dynamics 365 Commerce“ internetiniame darbo pradžios rinkinyje yra modulis, kurį naudojant šią užduotį atlikti lengva.</span><span class="sxs-lookup"><span data-stu-id="fd274-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="fd274-108">Logotipą galite įtraukti tiesiai į šabloną, maketą arba puslapį.</span><span class="sxs-lookup"><span data-stu-id="fd274-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="fd274-109">Tokiu būdu galite lengvai keisti logotipą, kuris rodomas konkrečiuose puslapiuose arba puslapių grupėse.</span><span class="sxs-lookup"><span data-stu-id="fd274-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="fd274-110">Tačiau šioje temoje aprašoma dažniausiai pasitaikanti situacija, kai logotipas įtraukiamas į antraštės fragmentą, kurį galima pakartotinai naudoti visuose svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="fd274-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fd274-111">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="fd274-111">Prerequisites</span></span>

<span data-ttu-id="fd274-112">Kad galėtumėte įtraukti logotipą į visus svetainės puslapius, turite atlikti tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="fd274-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="fd274-113">Logotipą nusiųskite į skaitmeninių išteklių tvarkytuvą, kurį galite pasiekti puslapyje **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="fd274-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="fd274-114">Sukurkite antraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="fd274-114">Create a header fragment.</span></span> <span data-ttu-id="fd274-115">Daugiau informacijos apie tai, kaip kurti ir naudoti fragmentus, rasite temoje [Darbas su fragmentais](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="fd274-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="fd274-116">Antraštės fragmentą įtraukite į šabloną, kuris svetainės puslapiuose naudojamas kaip jų maketo ir modulių parinktys.</span><span class="sxs-lookup"><span data-stu-id="fd274-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="fd274-117">Daugiau informacijos apie šablonus rasite temoje [Darbas su šablonais](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="fd274-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="fd274-118">Logotipo įtraukimas į antraštės fragmentą</span><span class="sxs-lookup"><span data-stu-id="fd274-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="fd274-119">Norėdami logotipą įtraukti į svetainės antraštės fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fd274-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="fd274-120">Kairėje esančioje naršymo srityje pasirinkite **Fragmentai**, tada – savo sukurtą antraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="fd274-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="fd274-121">Pasirinkite **Paimti**.</span><span class="sxs-lookup"><span data-stu-id="fd274-121">Select **Check out**.</span></span>
3. <span data-ttu-id="fd274-122">Išplėskite dalis **Antraštė** ir **Logotipas**.</span><span class="sxs-lookup"><span data-stu-id="fd274-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="fd274-123">Pasirinkite prie dalies **Logotipas** esantį daugtaškio mygtuką (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="fd274-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="fd274-124">Pasirinkite logotipo modulį.</span><span class="sxs-lookup"><span data-stu-id="fd274-124">Select the logo module.</span></span>
6. <span data-ttu-id="fd274-125">Dešinėje esančioje ypatybių srityje sukonfigūruokite logotipo modulį, kad jame būtų rodomas jūsų logotipas.</span><span class="sxs-lookup"><span data-stu-id="fd274-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="fd274-126">Antraštės fragmentą įrašykite, atrakinkite ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="fd274-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="fd274-127">Publikavus atnaujintą antraštės fragmentą, visuose svetainės puslapiuose, kuriuose naudojamas šablonas su šiuo antraštės fragmentu, bus rodomas jūsų logotipas.</span><span class="sxs-lookup"><span data-stu-id="fd274-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd274-128">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="fd274-128">Additional resources</span></span>

[<span data-ttu-id="fd274-129">Pasirinkti svetainės temą</span><span class="sxs-lookup"><span data-stu-id="fd274-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="fd274-130">Darbas su CSS perrašymo failais</span><span class="sxs-lookup"><span data-stu-id="fd274-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="fd274-131">Įtraukti parankinių piktogramą</span><span class="sxs-lookup"><span data-stu-id="fd274-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="fd274-132">Įtraukti pasveikinimo pranešimą</span><span class="sxs-lookup"><span data-stu-id="fd274-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="fd274-133">Įtraukti informaciją apie autorių teises</span><span class="sxs-lookup"><span data-stu-id="fd274-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="fd274-134">Kalbų įtraukimas į savo svetainę</span><span class="sxs-lookup"><span data-stu-id="fd274-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="fd274-135">Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija</span><span class="sxs-lookup"><span data-stu-id="fd274-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

