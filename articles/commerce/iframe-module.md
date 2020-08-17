---
title: „Iframe“ modulis
description: Šis skyrius aprašo „iframe“ modulį ir tai, kaip įtraukti jį į vietos puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0616a772a416a7c9d9756a840c93b8601c08c3d0
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/31/2020
ms.locfileid: "3647001"
---
# <a name="iframe-module"></a><span data-ttu-id="369f3-103">„Iframe“ modulis</span><span class="sxs-lookup"><span data-stu-id="369f3-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="369f3-104">Šis skyrius aprašo „iframe“ modulį ir tai, kaip įtraukti jį į vietos puslapius „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="369f3-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="369f3-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="369f3-105">Overview</span></span>

<span data-ttu-id="369f3-106">„iframe“ modulis suteikia „iframe“ (rėmelį pagal liniją), kuris apima išorės turinį svetainėje.</span><span class="sxs-lookup"><span data-stu-id="369f3-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="369f3-107">Pavyzdžiui, jis gali būti naudojamas „YouTube“ vaizdo įrašo ar PDF failo peržiūros patalpinimui bet kuriame svetainės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="369f3-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="369f3-108">„iframe“ modulis reikalauja galutinio URL.</span><span class="sxs-lookup"><span data-stu-id="369f3-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="369f3-109">Tuomet jis patalpina galutinio puslapio turinį HTML **„iframe“** elemente.</span><span class="sxs-lookup"><span data-stu-id="369f3-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="369f3-110">Išoriniai URSL turi būti leistinų sąraše (taip pat žinomas kaip „whitelist“) svetainės turinio saugumo politikoje (CSP) gairėse.</span><span class="sxs-lookup"><span data-stu-id="369f3-110">External URLs must be on the allow list (also known as a "whitelist") per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="369f3-111">„iframe“ turinui, URL turi būti leidžiami naudojant **rėmelio protėvio** gairę.</span><span class="sxs-lookup"><span data-stu-id="369f3-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="369f3-112">- Norėdami gauti daugiau informacijos, žr. [turinio saugumo politikos valdymas (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="369f3-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

<span data-ttu-id="369f3-113">Toliau pateiktas paveikslėlis rodo „iframe“ modulių pavyzdžius, kurie iliustruoja išorės vaizdo įrašus svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="369f3-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![„iframe“ modulio pavyzdys rodo išorinius vaizdo įrašus](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="369f3-115">„iframe“ modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="369f3-115">Iframe module properties</span></span>

| <span data-ttu-id="369f3-116">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="369f3-116">Property name</span></span>             | <span data-ttu-id="369f3-117">Vertė</span><span class="sxs-lookup"><span data-stu-id="369f3-117">Value</span></span>                 | <span data-ttu-id="369f3-118">aprašymas</span><span class="sxs-lookup"><span data-stu-id="369f3-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="369f3-119">Antraštė</span><span class="sxs-lookup"><span data-stu-id="369f3-119">Heading</span></span> | <span data-ttu-id="369f3-120">Tekstas</span><span class="sxs-lookup"><span data-stu-id="369f3-120">Text</span></span> | <span data-ttu-id="369f3-121">Modulio antraštė.</span><span class="sxs-lookup"><span data-stu-id="369f3-121">The heading for the module.</span></span> |
| <span data-ttu-id="369f3-122">Paskirties URL</span><span class="sxs-lookup"><span data-stu-id="369f3-122">Target URL</span></span> | <span data-ttu-id="369f3-123">URL</span><span class="sxs-lookup"><span data-stu-id="369f3-123">URL</span></span> | <span data-ttu-id="369f3-124">URL, kuris yra patalpintas modulyje.</span><span class="sxs-lookup"><span data-stu-id="369f3-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="369f3-125">Aukštis</span><span class="sxs-lookup"><span data-stu-id="369f3-125">Height</span></span> | <span data-ttu-id="369f3-126">Procentų skaičius</span><span class="sxs-lookup"><span data-stu-id="369f3-126">Number or percentage</span></span> | <span data-ttu-id="369f3-127">Modulio aukštis pikseliais arba procentais.</span><span class="sxs-lookup"><span data-stu-id="369f3-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="369f3-128">Pavyzdžiui,**100** vertė bus laikoma pikselių numeriais, o vertė **100%** traktuojama kaip procentai.</span><span class="sxs-lookup"><span data-stu-id="369f3-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="369f3-129">ARIA žyma</span><span class="sxs-lookup"><span data-stu-id="369f3-129">Aria label</span></span> | <span data-ttu-id="369f3-130">Tekstas</span><span class="sxs-lookup"><span data-stu-id="369f3-130">Text</span></span> | <span data-ttu-id="369f3-131">Prieinamų praturtinto interneto programų (ARIA) etiketės gali būti nustatytoas prieinamumo tikslais.</span><span class="sxs-lookup"><span data-stu-id="369f3-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="369f3-132">Įtraukti „iframe“ modulį į puslapį</span><span class="sxs-lookup"><span data-stu-id="369f3-132">Add an iframe module to a page</span></span>

<span data-ttu-id="369f3-133">Siekiant įtraukti „iframe“ modulį į puslapį ir parodyti išorinį vaizdo įrašą, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="369f3-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="369f3-134">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="369f3-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="369f3-135">**Naujo šablono** teksto laukelyje, skyriuje **Šablono pavadinimas** įveskite **Komercijos šablono** ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="369f3-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="369f3-136">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="369f3-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="369f3-137">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="369f3-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="369f3-138">**Pasirinkite šabloną** teksto laukelyje, pasirinkite **Komercijos šablono** šabloną.</span><span class="sxs-lookup"><span data-stu-id="369f3-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="369f3-139">Skyriuje **Puslapio pavadinimas**, įveskite **Komercijos puslapis** ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="369f3-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="369f3-140">Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="369f3-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="369f3-141">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="369f3-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="369f3-142">Modulio ypatybių juostoje, nustatykite**Pločio** vertę į **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="369f3-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="369f3-143">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="369f3-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="369f3-144">**Modulio įtraukimo** teksto laukelyje pasirinkite **„iframe“** modulį ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="369f3-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="369f3-145">Modulio ypatybių juostoje, nustatykite **Galutinis URL** vertę išorės URL vaizdo įrašui.</span><span class="sxs-lookup"><span data-stu-id="369f3-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="369f3-146">Nustatykite kitas ypatybes, tokias kaip **Antraštė** ir **Aukštis**, kaip norite.</span><span class="sxs-lookup"><span data-stu-id="369f3-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="369f3-147">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="369f3-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="369f3-148">Eikite į komercijos puslapį savo svetainėje.</span><span class="sxs-lookup"><span data-stu-id="369f3-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="369f3-149">Turėtumėte matyti, kad vaizdo įrašas yra sukurtas „iframe“ modulyje.</span><span class="sxs-lookup"><span data-stu-id="369f3-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="369f3-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="369f3-150">Additional resources</span></span>

[<span data-ttu-id="369f3-151">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="369f3-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="369f3-152">Turinio saugos strategijos (CSP) tvarkymas</span><span class="sxs-lookup"><span data-stu-id="369f3-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
