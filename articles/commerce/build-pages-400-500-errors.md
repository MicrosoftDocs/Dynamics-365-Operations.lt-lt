---
title: Kurti pasirinktinius 4xx/5xx būsenos kodo klaidų atsakymų puslapius
description: Šioje temoje aprašoma, kaip, naudojant „Microsoft Dynamics 365 Commerce“ kūrimo įrankius, kurti pasirinktinius atsako į 4xx ir 5xx būsenos kodo klaidas puslapius.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697111"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="acb81-103">Kurti pasirinktinius 4xx/5xx būsenos kodo klaidų atsakymų puslapius</span><span class="sxs-lookup"><span data-stu-id="acb81-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="acb81-104">Šioje temoje aprašoma, kaip, naudojant „Microsoft Dynamics 365 Commerce“ kūrimo įrankius, kurti pasirinktinius atsako į 4xx ir 5xx būsenos kodo klaidas puslapius.</span><span class="sxs-lookup"><span data-stu-id="acb81-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="acb81-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="acb81-105">Overview</span></span>

<span data-ttu-id="acb81-106">Jei užklausa nėra sėkminga, serveris pateikia HTTP būsenos kodo klaidų atsakus.</span><span class="sxs-lookup"><span data-stu-id="acb81-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="acb81-107">Būsenos kodas 404 užfiksuojamas ir pateikiamas neradus puslapio, o būsenos kodas 500 – įvykus serverio klaidai.</span><span class="sxs-lookup"><span data-stu-id="acb81-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="acb81-108">Programos „Dynamics 365 Commerce“ vartotojai gali kurti pasirinktinius būsenos kodo klaidų atsako puslapių, kurie rodomi vartotojams dėl tokių būsenos kodo klaidų atsako.</span><span class="sxs-lookup"><span data-stu-id="acb81-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="acb81-109">Būsenos kodo klaidų atsako puslapio kūrimas</span><span class="sxs-lookup"><span data-stu-id="acb81-109">Build a status code error response page</span></span>

<span data-ttu-id="acb81-110">Norėdami pradėti kurti būsenos kodo klaidų atsako puslapį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acb81-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="acb81-111">Savo pageidaujamoje žiniatinklio naršyklėje prisijunkite prie „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="acb81-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="acb81-112">Pasirinkite svetainę, kuriai norite sukurti 4xx / 5xx būsenos kodo klaidų atsako puslapį.</span><span class="sxs-lookup"><span data-stu-id="acb81-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="acb81-113">Šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="acb81-113">Build the template</span></span>

<span data-ttu-id="acb81-114">Norėdami sukurti būsenos kodo klaidų atsako puslapio šabloną, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acb81-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="acb81-115">Nueikite į **Šablonai \> Naujas šablonas**.</span><span class="sxs-lookup"><span data-stu-id="acb81-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="acb81-116">Naująjį šabloną pavadinkite.</span><span class="sxs-lookup"><span data-stu-id="acb81-116">Name the new template.</span></span>
1. <span data-ttu-id="acb81-117">Sukurkite šabloną su norima būsenos kodo klaidų atsako puslapio struktūra.</span><span class="sxs-lookup"><span data-stu-id="acb81-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="acb81-118">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="acb81-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="acb81-119">Būsenos kodo klaidų atsako puslapio kūrimas</span><span class="sxs-lookup"><span data-stu-id="acb81-119">Build the status code error response page</span></span>

<span data-ttu-id="acb81-120">Norėdami kurti būsenos kodo klaidų atsako puslapį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acb81-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="acb81-121">Nueikite į **Puslapiai \> Naujas puslapis**.</span><span class="sxs-lookup"><span data-stu-id="acb81-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="acb81-122">Pavadinkite būsenos kodo klaidų atsako puslapį, tačiau **nenustatykite** lauko **URL**.</span><span class="sxs-lookup"><span data-stu-id="acb81-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="acb81-123">Sukurkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="acb81-123">Build the page.</span></span>
1. <span data-ttu-id="acb81-124">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="acb81-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="acb81-125">Galite sukurti atskirus būsenos kodo klaidų atsako puslapius, skirtus 4xx ir 5xx būsenos kodo klaidoms.</span><span class="sxs-lookup"><span data-stu-id="acb81-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="acb81-126">Taip pat galite naudoti tą patį bendrą būsenos kodo klaidų atsako puslapį abiem klaidų kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="acb81-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="acb81-127">Būsenos kodo klaidų atsako puslapio peradresavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="acb81-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="acb81-128">Norėdami nustatyti būsenos kodo klaidų atsako puslapio peradresavimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="acb81-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="acb81-129">Nueikite į **URL \> Naujas \> Naujas pseudonimas** ir pasirinkite anksčiau sukurtą būsenos kodo klaidų atsako puslapį.</span><span class="sxs-lookup"><span data-stu-id="acb81-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="acb81-130">Lauke **Pseudonimas** įveskite **numatytasis-4xx** arba **numatytasis-5xx**, atsižvelgdami į būsenos kodo klaidų atsako puslapį, kurio peradresavimą nustatote.</span><span class="sxs-lookup"><span data-stu-id="acb81-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="acb81-131">Šiuos pseudonimus reikia publikuoti.</span><span class="sxs-lookup"><span data-stu-id="acb81-131">These aliases must be published.</span></span> <span data-ttu-id="acb81-132">Kitu atveju peradresavimas neveiks.</span><span class="sxs-lookup"><span data-stu-id="acb81-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="acb81-133">Pasirinkite **Gerai**, kad patvirtintumėte susiejimą.</span><span class="sxs-lookup"><span data-stu-id="acb81-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="acb81-134">Jei abiem klaidų kategorijoms naudojate vieną būsenos kodo klaidų atsako puslapį, pakartokite šią procedūrą, kad kitos klaidų kategorijos pseudonimą susietumėte su tuo pačiu puslapiu.</span><span class="sxs-lookup"><span data-stu-id="acb81-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="acb81-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="acb81-135">Additional resources</span></span>

[<span data-ttu-id="acb81-136">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="acb81-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="acb81-137">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="acb81-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="acb81-138">Kurti puslapio URL</span><span class="sxs-lookup"><span data-stu-id="acb81-138">Create a page URL</span></span>](create-page-url.md)
