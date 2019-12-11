---
title: Ypatybių modulis
description: Šioje temoje aprašomi ypatybių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785290"
---
# <a name="feature-module"></a><span data-ttu-id="1bcb9-103">Ypatybių modulis</span><span class="sxs-lookup"><span data-stu-id="1bcb9-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1bcb9-104">Šioje temoje aprašomi ypatybių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1bcb9-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="1bcb9-105">Overview</span></span>

<span data-ttu-id="1bcb9-106">Ypatybių modulis naudojamas produktams ar akcijoms reklamuoti derinant vaizdus ir tekstą.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="1bcb9-107">Pavyzdžiui, pardavėjas ypatybių modulį gali įtraukti į produkto išsamios informacijos puslapį, kad galėtų akcentuoti produkto ypatybes.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="1bcb9-108">Ypatybių modulis grindžiamas duomenimis iš turinio valdymo sistemos (TVS).</span><span class="sxs-lookup"><span data-stu-id="1bcb9-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="1bcb9-109">Tai yra atskiras modulis, nepriklausantis nuo jokių kitų puslapio modulių.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="1bcb9-110">Ypatybių modulį galima įdėti bet kuriame svetainės puslapyje, kuriame pardavėjas nori kažką parduoti ar reklamuoti, (pavyzdžiui, produktus, išpardavimus ar ypatybes).</span><span class="sxs-lookup"><span data-stu-id="1bcb9-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="1bcb9-111">Ypatybių modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="1bcb9-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="1bcb9-112">Ypatybių modulį galima naudoti tolesniuose puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="1bcb9-113">Produktų išsamios informacijos puslapyje, norint parodyti produktų ypatybes</span><span class="sxs-lookup"><span data-stu-id="1bcb9-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="1bcb9-114">Pagrindiniame puslapyje, norint reklamuoti produktus</span><span class="sxs-lookup"><span data-stu-id="1bcb9-114">The home page, to promote products</span></span>
- <span data-ttu-id="1bcb9-115">Kategorijos puslapyje, norint akcentuoti produktų kategoriją</span><span class="sxs-lookup"><span data-stu-id="1bcb9-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="1bcb9-116">Ypatybių modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="1bcb9-116">Feature module properties</span></span>

| <span data-ttu-id="1bcb9-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="1bcb9-117">Property name</span></span>     | <span data-ttu-id="1bcb9-118">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="1bcb9-118">Values</span></span> | <span data-ttu-id="1bcb9-119">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1bcb9-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="1bcb9-120">Vaizdas</span><span class="sxs-lookup"><span data-stu-id="1bcb9-120">Image</span></span>             | <span data-ttu-id="1bcb9-121">Vaizdo failas</span><span class="sxs-lookup"><span data-stu-id="1bcb9-121">Image file</span></span> | <span data-ttu-id="1bcb9-122">Parduoti produktą ar parodyti akciją galima naudojant vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="1bcb9-123">Vaizdą galima nusiųsti į vaizdų galeriją arba galima naudoti esamą vaizdą.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="1bcb9-124">Antraštė</span><span class="sxs-lookup"><span data-stu-id="1bcb9-124">Heading</span></span>           | <span data-ttu-id="1bcb9-125">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**)</span><span class="sxs-lookup"><span data-stu-id="1bcb9-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1bcb9-126">Kiekviename funkcijų modulyje gali būti antraštė.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-126">Every feature module can have a heading.</span></span> <span data-ttu-id="1bcb9-127">Numatyta, kad naudojama antrašės žymė **H2**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="1bcb9-128">Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="1bcb9-129">Pastraipa</span><span class="sxs-lookup"><span data-stu-id="1bcb9-129">Paragraph</span></span>         | <span data-ttu-id="1bcb9-130">Pastraipos tekstas</span><span class="sxs-lookup"><span data-stu-id="1bcb9-130">Paragraph text</span></span> | <span data-ttu-id="1bcb9-131">Ypatybių moduliai palaiko pastraipos tekstą raiškiojo teksto formatu.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="1bcb9-132">Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas bei hipersaitai.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="1bcb9-133">Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="1bcb9-134">Saitas</span><span class="sxs-lookup"><span data-stu-id="1bcb9-134">Link</span></span>              | <span data-ttu-id="1bcb9-135">Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke**</span><span class="sxs-lookup"><span data-stu-id="1bcb9-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="1bcb9-136">Ypatybių moduliai palaiko vieną ar kelis raginimo imtis veiksmų saitus.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="1bcb9-137">Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="1bcb9-138">ARIA žymos turi būti aprašomosios, kad atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="1bcb9-139">Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="1bcb9-140">Vaizdų išdėstymas</span><span class="sxs-lookup"><span data-stu-id="1bcb9-140">Image placement</span></span>   | <span data-ttu-id="1bcb9-141">**Dešinėje**, **Kairėje**, **Viršuje** arba **Apačioje**</span><span class="sxs-lookup"><span data-stu-id="1bcb9-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="1bcb9-142">Ši ypatybė nustato vaizdo padėtį teksto atžvilgiu.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="1bcb9-143">Pavyzdžiui, jei pasirenkama **Dešinėje**, vaizdas rodomas teksto dešinėje.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="1bcb9-144">Vaizdo stulpelio dydis</span><span class="sxs-lookup"><span data-stu-id="1bcb9-144">Image column size</span></span> | <span data-ttu-id="1bcb9-145">Reikšmė nuo **1** iki **12**</span><span class="sxs-lookup"><span data-stu-id="1bcb9-145">A value from **1** through **12**</span></span> | <span data-ttu-id="1bcb9-146">Ši ypatybė nustato vaizdo dydį teksto atžvilgiu.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="1bcb9-147">Dydis išreiškiamas kaip puslapio stulpelių skaičius.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="1bcb9-148">Puslapyje yra 12 stulpelių.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-148">There are 12 columns on a page.</span></span> <span data-ttu-id="1bcb9-149">Numatyta, kad vaizdas ir tekstas yra vienodo dydžio (po šešis stulpelius).</span><span class="sxs-lookup"><span data-stu-id="1bcb9-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="1bcb9-150">Tačiau dydį galima koreguoti pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="1bcb9-151">Ypatybių modulio įtraukimas į naują puslapį</span><span class="sxs-lookup"><span data-stu-id="1bcb9-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="1bcb9-152">Norėdami į naują puslapį įtraukti ypatybių modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1bcb9-153">Nueikite į **Šablonai** ir sukurkite puslapio šabloną pavadinimu **ypatybių šablonas**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="1bcb9-154">Numatytojo puslapio vietoje **Pagrindinis** įtraukite ypatybių modulį.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="1bcb9-155">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="1bcb9-156">Naudodami ką tik sukurtą ypatybių šabloną, sukurkite puslapį, pavadintą **ypatybių puslapis**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="1bcb9-157">Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1bcb9-158">Dialogo lango **Modulio įtraukimas** dalyje **Pasirinkti modulius** pasirinkite ypatybių modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="1bcb9-159">Kairėje esančiame struktūros medyje pasirinkite ypatybių modulį.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="1bcb9-160">Dešinėje esančioje ypatybių srityje pasirinkite **Įtraukti vaizdą**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="1bcb9-161">Tada pasirinkite esamą vaizdą arba nusiųskite naują.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="1bcb9-162">Pasirinkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-162">Select **Heading**.</span></span>
1. <span data-ttu-id="1bcb9-163">Dialogo lange **Antraštė** įtraukite antraštės tekstą, pasirinkite antraštės lygį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="1bcb9-164">Dalyje **Raiškusis tekstas** įtraukite reikiamą tekstą.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="1bcb9-165">Pasirinkite **Įtraukti veiksmo saitą**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="1bcb9-166">Dialogo lange **Veiksmo saitas** įtraukite saito tekstą, saito URL ir saito ARIA žymą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="1bcb9-167">Įrašykite puslapį ir peržiūrėkite keitimus.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="1bcb9-168">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="1bcb9-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1bcb9-169">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1bcb9-169">Additional resources</span></span>

[<span data-ttu-id="1bcb9-170">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="1bcb9-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1bcb9-171">Įspėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="1bcb9-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="1bcb9-172">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="1bcb9-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="1bcb9-173">Raiškiojo turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="1bcb9-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="1bcb9-174">Turinio išdėstymo modulis</span><span class="sxs-lookup"><span data-stu-id="1bcb9-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="1bcb9-175">Pagrindinės reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="1bcb9-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="1bcb9-176">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="1bcb9-176">Video player module</span></span>](add-video-player.md)
