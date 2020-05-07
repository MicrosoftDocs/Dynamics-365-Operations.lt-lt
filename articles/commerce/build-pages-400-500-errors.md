---
title: Kurti pasirinktinius 4xx/5xx būsenos kodo klaidų atsakymų puslapius
description: Šioje temoje aprašoma, kaip, naudojant „Microsoft Dynamics 365 Commerce“ kūrimo įrankius, kurti pasirinktinius atsako į 4xx ir 5xx būsenos kodo klaidas puslapius.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269549"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="5a019-103">Kurti pasirinktinius 4xx/5xx būsenos kodo klaidų atsakymų puslapius</span><span class="sxs-lookup"><span data-stu-id="5a019-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5a019-104">Šioje temoje aprašoma, kaip, naudojant „Microsoft Dynamics 365 Commerce“ kūrimo įrankius, kurti pasirinktinius atsako į 4xx ir 5xx būsenos kodo klaidas puslapius.</span><span class="sxs-lookup"><span data-stu-id="5a019-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5a019-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="5a019-105">Overview</span></span>

<span data-ttu-id="5a019-106">Jei užklausa nėra sėkminga, serveris pateikia HTTP būsenos kodo klaidų atsakus.</span><span class="sxs-lookup"><span data-stu-id="5a019-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="5a019-107">Būsenos kodas 404 užfiksuojamas ir pateikiamas neradus puslapio, o būsenos kodas 500 – įvykus serverio klaidai.</span><span class="sxs-lookup"><span data-stu-id="5a019-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="5a019-108">Programos „Dynamics 365 Commerce“ vartotojai gali kurti pasirinktinius būsenos kodo klaidų atsako puslapių, kurie rodomi vartotojams dėl tokių būsenos kodo klaidų atsako.</span><span class="sxs-lookup"><span data-stu-id="5a019-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="5a019-109">Būsenos kodo klaidų atsako puslapio kūrimas</span><span class="sxs-lookup"><span data-stu-id="5a019-109">Build a status code error response page</span></span>

<span data-ttu-id="5a019-110">Norėdami pradėti kurti būsenos kodo klaidų atsako puslapį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5a019-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5a019-111">Savo pageidaujamoje žiniatinklio naršyklėje prisijunkite prie „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="5a019-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="5a019-112">Pasirinkite svetainę, kuriai norite sukurti 4xx / 5xx būsenos kodo klaidų atsako puslapį.</span><span class="sxs-lookup"><span data-stu-id="5a019-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="5a019-113">Šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="5a019-113">Build the template</span></span>

<span data-ttu-id="5a019-114">Norėdami sukurti būsenos kodo klaidų atsako puslapio šabloną, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5a019-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5a019-115">Eikite į parinktį **Šablonai**.</span><span class="sxs-lookup"><span data-stu-id="5a019-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="5a019-116">Pasirinkite **Naujas**, kad sukurtumėte puslapio šabloną.</span><span class="sxs-lookup"><span data-stu-id="5a019-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="5a019-117">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite naujo šablono pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5a019-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="5a019-118">Sukurkite šabloną su norima būsenos kodo klaidų atsako puslapio struktūra.</span><span class="sxs-lookup"><span data-stu-id="5a019-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="5a019-119">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="5a019-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="5a019-120">Būsenos kodo klaidų atsako puslapio kūrimas</span><span class="sxs-lookup"><span data-stu-id="5a019-120">Build the status code error response page</span></span>

<span data-ttu-id="5a019-121">Norėdami kurti būsenos kodo klaidų atsako puslapį, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5a019-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5a019-122">Eiti į **Puslapiai**.</span><span class="sxs-lookup"><span data-stu-id="5a019-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="5a019-123">Pasirinkite **Naujas**, kad sukurtumėte puslapį.</span><span class="sxs-lookup"><span data-stu-id="5a019-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="5a019-124">Dialogo lange **Pasirinkti šabloną** pasirinkite šabloną, tada dalyje **Puslapio pavadinimas** įveskite būsenos kodo klaidų atsako puslapio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="5a019-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="5a019-125">Lauką **Puslapio URL** palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="5a019-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="5a019-126">Sukurkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="5a019-126">Build the page.</span></span>
1. <span data-ttu-id="5a019-127">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="5a019-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="5a019-128">Galite sukurti atskirus būsenos kodo klaidų atsako puslapius, skirtus 4xx ir 5xx būsenos kodo klaidoms.</span><span class="sxs-lookup"><span data-stu-id="5a019-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="5a019-129">Taip pat galite naudoti tą patį bendrą būsenos kodo klaidų atsako puslapį abiem klaidų kategorijoms.</span><span class="sxs-lookup"><span data-stu-id="5a019-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="5a019-130">Būsenos kodo klaidų atsako puslapio peradresavimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="5a019-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="5a019-131">Norėdami nustatyti būsenos kodo klaidų atsako puslapio peradresavimą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5a019-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5a019-132">Nueikite į **URL \> Naujas \> Naujas pseudonimas** ir pasirinkite anksčiau sukurtą būsenos kodo klaidų atsako puslapį.</span><span class="sxs-lookup"><span data-stu-id="5a019-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="5a019-133">Lauke **Pseudonimas** įveskite **numatytasis-4xx** arba **numatytasis-5xx**, atsižvelgdami į būsenos kodo klaidų atsako puslapį, kurio peradresavimą nustatote.</span><span class="sxs-lookup"><span data-stu-id="5a019-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="5a019-134">Šiuos pseudonimus reikia publikuoti.</span><span class="sxs-lookup"><span data-stu-id="5a019-134">These aliases must be published.</span></span> <span data-ttu-id="5a019-135">Kitu atveju peradresavimas neveiks.</span><span class="sxs-lookup"><span data-stu-id="5a019-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="5a019-136">Pasirinkite **Gerai**, kad patvirtintumėte susiejimą.</span><span class="sxs-lookup"><span data-stu-id="5a019-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="5a019-137">Jei abiem klaidų kategorijoms naudojate vieną būsenos kodo klaidų atsako puslapį, pakartokite šią procedūrą, kad kitos klaidų kategorijos pseudonimą susietumėte su tuo pačiu puslapiu.</span><span class="sxs-lookup"><span data-stu-id="5a019-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a019-138">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5a019-138">Additional resources</span></span>

[<span data-ttu-id="5a019-139">Darbas su šablonais</span><span class="sxs-lookup"><span data-stu-id="5a019-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="5a019-140">Įtraukti naują svetainės puslapį</span><span class="sxs-lookup"><span data-stu-id="5a019-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="5a019-141">Kurti puslapio URL</span><span class="sxs-lookup"><span data-stu-id="5a019-141">Create a page URL</span></span>](create-page-url.md)
