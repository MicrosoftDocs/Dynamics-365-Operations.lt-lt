---
title: „Iframe“ modulis
description: Šis skyrius aprašo „iframe“ modulį ir tai, kaip įtraukti jį į vietos puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b7b5935a81377e0cb6acfc497eece6148bf1eeee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993374"
---
# <a name="iframe-module"></a><span data-ttu-id="95a4c-103">„Iframe“ modulis</span><span class="sxs-lookup"><span data-stu-id="95a4c-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95a4c-104">Šis skyrius aprašo „iframe“ modulį ir tai, kaip įtraukti jį į vietos puslapius „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="95a4c-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="95a4c-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="95a4c-105">Overview</span></span>

<span data-ttu-id="95a4c-106">„iframe“ modulis suteikia „iframe“ (rėmelį pagal liniją), kuris apima išorės turinį svetainėje.</span><span class="sxs-lookup"><span data-stu-id="95a4c-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="95a4c-107">Pavyzdžiui, jis gali būti naudojamas „YouTube“ vaizdo įrašo ar PDF failo peržiūros patalpinimui bet kuriame svetainės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="95a4c-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="95a4c-108">„iframe“ modulis reikalauja galutinio URL.</span><span class="sxs-lookup"><span data-stu-id="95a4c-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="95a4c-109">Tuomet jis patalpina galutinio puslapio turinį HTML **„iframe“** elemente.</span><span class="sxs-lookup"><span data-stu-id="95a4c-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="95a4c-110">Išorės URL turi būti leidžiamųjų sąraše vietos turinio saugumo politikos (CSP) direktyvoms.</span><span class="sxs-lookup"><span data-stu-id="95a4c-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="95a4c-111">„iframe“ turinui, URL turi būti leidžiami naudojant **rėmelio protėvio** gairę.</span><span class="sxs-lookup"><span data-stu-id="95a4c-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="95a4c-112">- Norėdami gauti daugiau informacijos, žr. [turinio saugumo politikos valdymas (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="95a4c-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="95a4c-113">„iframe“ modulį galima naudoti „Dynamics 365 Commerce“ 10.0.13 leidime.</span><span class="sxs-lookup"><span data-stu-id="95a4c-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="95a4c-114">Toliau pateiktas paveikslėlis rodo „iframe“ modulių pavyzdžius, kurie iliustruoja išorės vaizdo įrašus svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="95a4c-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![„iframe“ modulio pavyzdys rodo išorinius vaizdo įrašus](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="95a4c-116">„iframe“ modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="95a4c-116">Iframe module properties</span></span>

| <span data-ttu-id="95a4c-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="95a4c-117">Property name</span></span>             | <span data-ttu-id="95a4c-118">Vertė</span><span class="sxs-lookup"><span data-stu-id="95a4c-118">Value</span></span>                 | <span data-ttu-id="95a4c-119">aprašymas</span><span class="sxs-lookup"><span data-stu-id="95a4c-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="95a4c-120">Antraštė</span><span class="sxs-lookup"><span data-stu-id="95a4c-120">Heading</span></span> | <span data-ttu-id="95a4c-121">Tekstas</span><span class="sxs-lookup"><span data-stu-id="95a4c-121">Text</span></span> | <span data-ttu-id="95a4c-122">Modulio antraštė.</span><span class="sxs-lookup"><span data-stu-id="95a4c-122">The heading for the module.</span></span> |
| <span data-ttu-id="95a4c-123">Paskirties URL</span><span class="sxs-lookup"><span data-stu-id="95a4c-123">Target URL</span></span> | <span data-ttu-id="95a4c-124">URL</span><span class="sxs-lookup"><span data-stu-id="95a4c-124">URL</span></span> | <span data-ttu-id="95a4c-125">URL, kuris yra patalpintas modulyje.</span><span class="sxs-lookup"><span data-stu-id="95a4c-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="95a4c-126">Aukštis</span><span class="sxs-lookup"><span data-stu-id="95a4c-126">Height</span></span> | <span data-ttu-id="95a4c-127">Procentų skaičius</span><span class="sxs-lookup"><span data-stu-id="95a4c-127">Number or percentage</span></span> | <span data-ttu-id="95a4c-128">Modulio aukštis pikseliais arba procentais.</span><span class="sxs-lookup"><span data-stu-id="95a4c-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="95a4c-129">Pavyzdžiui,**100** vertė bus laikoma pikselių numeriais, o vertė **100%** traktuojama kaip procentai.</span><span class="sxs-lookup"><span data-stu-id="95a4c-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="95a4c-130">ARIA žyma</span><span class="sxs-lookup"><span data-stu-id="95a4c-130">Aria label</span></span> | <span data-ttu-id="95a4c-131">Tekstas</span><span class="sxs-lookup"><span data-stu-id="95a4c-131">Text</span></span> | <span data-ttu-id="95a4c-132">Prieinamų praturtinto interneto programų (ARIA) etiketės gali būti nustatytoas prieinamumo tikslais.</span><span class="sxs-lookup"><span data-stu-id="95a4c-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="95a4c-133">Įtraukti „iframe“ modulį į puslapį</span><span class="sxs-lookup"><span data-stu-id="95a4c-133">Add an iframe module to a page</span></span>

<span data-ttu-id="95a4c-134">Siekiant įtraukti „iframe“ modulį į puslapį ir parodyti išorinį vaizdo įrašą, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="95a4c-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="95a4c-135">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="95a4c-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="95a4c-136">**Naujo šablono** teksto laukelyje, skyriuje **Šablono pavadinimas** įveskite **Komercijos šablono** ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="95a4c-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="95a4c-137">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="95a4c-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="95a4c-138">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="95a4c-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="95a4c-139">**Pasirinkite šabloną** teksto laukelyje, pasirinkite **Komercijos šablono** šabloną.</span><span class="sxs-lookup"><span data-stu-id="95a4c-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="95a4c-140">Skyriuje **Puslapio pavadinimas**, įveskite **Komercijos puslapis** ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="95a4c-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="95a4c-141">Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="95a4c-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="95a4c-142">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="95a4c-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="95a4c-143">Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="95a4c-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="95a4c-144">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="95a4c-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="95a4c-145">**Modulio įtraukimo** teksto laukelyje pasirinkite **„iframe“** modulį ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="95a4c-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="95a4c-146">Modulio ypatybių juostoje, nustatykite **Galutinis URL** vertę išorės URL vaizdo įrašui.</span><span class="sxs-lookup"><span data-stu-id="95a4c-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="95a4c-147">Nustatykite kitas ypatybes, tokias kaip **Antraštė** ir **Aukštis**, kaip norite.</span><span class="sxs-lookup"><span data-stu-id="95a4c-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="95a4c-148">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="95a4c-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="95a4c-149">Eikite į komercijos puslapį savo svetainėje.</span><span class="sxs-lookup"><span data-stu-id="95a4c-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="95a4c-150">Turėtumėte matyti, kad vaizdo įrašas yra sukurtas „iframe“ modulyje.</span><span class="sxs-lookup"><span data-stu-id="95a4c-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="95a4c-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="95a4c-151">Additional resources</span></span>

[<span data-ttu-id="95a4c-152">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="95a4c-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="95a4c-153">Turinio saugos strategijos (CSP) tvarkymas</span><span class="sxs-lookup"><span data-stu-id="95a4c-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
