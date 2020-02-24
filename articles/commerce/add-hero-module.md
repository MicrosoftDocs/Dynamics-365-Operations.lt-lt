---
title: Turinio bloko modulis
description: Šioje temoje aprašomi turinio bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f91de93ce5ed4813f9f2adbe7678229189b5af2f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025763"
---
# <a name="content-block-module"></a><span data-ttu-id="3057c-103">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="3057c-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3057c-104">Šioje temoje aprašomi turinio bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="3057c-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3057c-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="3057c-105">Overview</span></span>

<span data-ttu-id="3057c-106">Turinio bloko modulis naudojamas produktams ar akcijoms reklamuoti derinant vaizdus ir tekstą.</span><span class="sxs-lookup"><span data-stu-id="3057c-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="3057c-107">Pavyzdžiui, pardavėjas turinio bloko modulį gali įtraukti į pagrindinį el. prekybos svetainės puslapį, kad reklamuotų naują produktą ir pritrauktų klientų dėmesį.</span><span class="sxs-lookup"><span data-stu-id="3057c-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="3057c-108">Turinio bloko modulis grindžiamas duomenimis iš turinio valdymo sistemos (TVS).</span><span class="sxs-lookup"><span data-stu-id="3057c-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="3057c-109">Tai yra atskiras modulis, nepriklausantis nuo jokių kitų puslapio modulių.</span><span class="sxs-lookup"><span data-stu-id="3057c-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="3057c-110">Turinio bloko modulį galima įdėti bet kuriame svetainės puslapyje, kuriame pardavėjas nori kažką parduoti ar reklamuoti, (pavyzdžiui, produktus, išpardavimus ar ypatybes).</span><span class="sxs-lookup"><span data-stu-id="3057c-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="3057c-111">Turinio bloko modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="3057c-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="3057c-112">Turinio bloko modulį galima naudoti pagrindiniame el. prekybos svetainės puslapyje, norint akcentuoti akcijas ir naujus produktus.</span><span class="sxs-lookup"><span data-stu-id="3057c-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="3057c-113">Turinio bloko modulį galima naudoti išsamios produktų informacijos puslapyje, norint parodyti produktų informaciją.</span><span class="sxs-lookup"><span data-stu-id="3057c-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="3057c-114">Kelis turinio bloko modulius galima įdėti į karuselės modulį, norint akcentuoti kelis produktus ar akcijas.</span><span class="sxs-lookup"><span data-stu-id="3057c-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="3057c-115">Turinio bloko moduliai ir temos</span><span class="sxs-lookup"><span data-stu-id="3057c-115">Content block modules and themes</span></span>

<span data-ttu-id="3057c-116">Turinio bloko moduliai gali palaikyti įvairius maketus ir stilius, pagrįstus tema.</span><span class="sxs-lookup"><span data-stu-id="3057c-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="3057c-117">Pavyzdžiui, „Fabrikam“ tema palaiko tris turinio bloko modulio maketo variantus: pagrindinis, funkcija ir plytelė.</span><span class="sxs-lookup"><span data-stu-id="3057c-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="3057c-118">Pagrindinis maketas rodo vaizdą fone su teksto perdanga.</span><span class="sxs-lookup"><span data-stu-id="3057c-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="3057c-119">Funkcijos maketas vaizdą ir tekstą vienas šalia kito.</span><span class="sxs-lookup"><span data-stu-id="3057c-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="3057c-120">Plytelės maketas leidžia daug turinio blokų plytelės formatu.</span><span class="sxs-lookup"><span data-stu-id="3057c-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="3057c-121">Be to, tema gali turėti skirtingų ypatybių kiekvienam maketui.</span><span class="sxs-lookup"><span data-stu-id="3057c-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="3057c-122">Temo kūrėjas gali sukurti daugiau maketų, kuriuose yra daugiau stilių, naudodamas turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="3057c-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="3057c-123">Toliau pateiktame paveiksle parodytas turinio bloko modulis su pagrindiniu maketu.</span><span class="sxs-lookup"><span data-stu-id="3057c-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Pagrindinės reklaminės juostos modulio pavyzdys](./media/Hero.PNG)

<span data-ttu-id="3057c-125">Toliau pateiktame paveiksle parodytas turinio bloko modulis su funkcijos maketu.</span><span class="sxs-lookup"><span data-stu-id="3057c-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Reklamuojamų produktų modulių pavyzdžiai](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="3057c-127">Turinio bloko modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="3057c-127">Content block module properties</span></span>

| <span data-ttu-id="3057c-128">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3057c-128">Property name</span></span>  | <span data-ttu-id="3057c-129">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="3057c-129">Values</span></span> | <span data-ttu-id="3057c-130">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="3057c-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="3057c-131">Vaizdas</span><span class="sxs-lookup"><span data-stu-id="3057c-131">Image</span></span>          | <span data-ttu-id="3057c-132">Vaizdo failas</span><span class="sxs-lookup"><span data-stu-id="3057c-132">Image file</span></span> | <span data-ttu-id="3057c-133">Parodyti produktą ar akciją galima naudojant vaizdą.</span><span class="sxs-lookup"><span data-stu-id="3057c-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="3057c-134">Vaizdą galima nusiųsti į vaizdų galeriją arba galima naudoti esamą vaizdą.</span><span class="sxs-lookup"><span data-stu-id="3057c-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="3057c-135">Antraštė</span><span class="sxs-lookup"><span data-stu-id="3057c-135">Heading</span></span>        | <span data-ttu-id="3057c-136">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**)</span><span class="sxs-lookup"><span data-stu-id="3057c-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="3057c-137">Kiekviename pagrindinės reklaminės juostos modulyje gali būti antraštė.</span><span class="sxs-lookup"><span data-stu-id="3057c-137">Every hero module can have a heading.</span></span> <span data-ttu-id="3057c-138">Numatyta, kad naudojama antrašės žymė **H2**.</span><span class="sxs-lookup"><span data-stu-id="3057c-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="3057c-139">Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="3057c-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="3057c-140">Pastraipa</span><span class="sxs-lookup"><span data-stu-id="3057c-140">Paragraph</span></span>      | <span data-ttu-id="3057c-141">Pastraipos tekstas</span><span class="sxs-lookup"><span data-stu-id="3057c-141">Paragraph text</span></span> | <span data-ttu-id="3057c-142">Pagrindinės reklaminės juostos moduliai palaiko pastraipos tekstą raiškiojo teksto formatu.</span><span class="sxs-lookup"><span data-stu-id="3057c-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="3057c-143">Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas bei hipersaitai.</span><span class="sxs-lookup"><span data-stu-id="3057c-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="3057c-144">Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema.</span><span class="sxs-lookup"><span data-stu-id="3057c-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="3057c-145">Saitas</span><span class="sxs-lookup"><span data-stu-id="3057c-145">Link</span></span>           | <span data-ttu-id="3057c-146">Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke**</span><span class="sxs-lookup"><span data-stu-id="3057c-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="3057c-147">Pagrindinės reklaminės juostos moduliai palaiko vieną ar kelis raginimo imtis veiksmų saitus.</span><span class="sxs-lookup"><span data-stu-id="3057c-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="3057c-148">Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma.</span><span class="sxs-lookup"><span data-stu-id="3057c-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="3057c-149">ARIA žymos turi būti aprašomosios, kad atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="3057c-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="3057c-150">Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke.</span><span class="sxs-lookup"><span data-stu-id="3057c-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="3057c-151">Turinio bloko modulio ypatybės „Fabrikam“ temoje</span><span class="sxs-lookup"><span data-stu-id="3057c-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="3057c-152">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3057c-152">Property name</span></span>  | <span data-ttu-id="3057c-153">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="3057c-153">Values</span></span> | <span data-ttu-id="3057c-154">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="3057c-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="3057c-155">Teksto talpinimas</span><span class="sxs-lookup"><span data-stu-id="3057c-155">Text placement</span></span> | <span data-ttu-id="3057c-156">**Kairė**, **Dešinė**, **Centras**</span><span class="sxs-lookup"><span data-stu-id="3057c-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="3057c-157">Ši ypatybė nustato teksto ant vaizdo padėtį.</span><span class="sxs-lookup"><span data-stu-id="3057c-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="3057c-158">Ji taikoma tik pagrindiniame makete.</span><span class="sxs-lookup"><span data-stu-id="3057c-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="3057c-159">Teksto tema</span><span class="sxs-lookup"><span data-stu-id="3057c-159">Text theme</span></span>     | <span data-ttu-id="3057c-160">**Šviesi** arba **Tamsi**</span><span class="sxs-lookup"><span data-stu-id="3057c-160">**Light** or **Dark**</span></span> | <span data-ttu-id="3057c-161">Pagal fono vaizdą galima nustatyti teksto spalvų schemą.</span><span class="sxs-lookup"><span data-stu-id="3057c-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="3057c-162">Pavyzdžiui, jei vaizdo fonas yra tamsus, galima taikyti šviesią temą, kad tekstas būtų matomesnis ir būtų pasiektas spalvų kontrasto santykis pritaikymo neįgaliesiems tikslais.</span><span class="sxs-lookup"><span data-stu-id="3057c-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="3057c-163">Ji taikoma tik pagrindiniame makete.</span><span class="sxs-lookup"><span data-stu-id="3057c-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="3057c-164">Vaizdų išdėstymas</span><span class="sxs-lookup"><span data-stu-id="3057c-164">Image placement</span></span>       | <span data-ttu-id="3057c-165">**Kairė**, **Dešinė**</span><span class="sxs-lookup"><span data-stu-id="3057c-165">**Left**,  **Right**</span></span> | <span data-ttu-id="3057c-166">Ši ypatybė nurodo, ar vaizdas turi būti teksto kairėje ar dešinėje.</span><span class="sxs-lookup"><span data-stu-id="3057c-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="3057c-167">Ji taikoma tik funkcijos makete.</span><span class="sxs-lookup"><span data-stu-id="3057c-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="3057c-168">Turinio bloko modulio įtraukimas į naują puslapį</span><span class="sxs-lookup"><span data-stu-id="3057c-168">Add a content block module to a new page</span></span>

<span data-ttu-id="3057c-169">Norėdami į naują puslapį įtraukti pagrindinės reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3057c-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3057c-170">Eikite į **Šablonai** ir sukurkite puslapio šabloną pavadinimu **turinio bloko šablonas**.</span><span class="sxs-lookup"><span data-stu-id="3057c-170">Go to **Templates**, and create a page template that is named **content block template**.</span></span>
1. <span data-ttu-id="3057c-171">Numatytojo puslapio vietoje **Pagrindinis** įtraukite pagrindinės reklaminės juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="3057c-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="3057c-172">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="3057c-172">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="3057c-173">Naudodami ką tik sukurtą pagrindinį šabloną, sukurkite puslapį, pavadintą **turinio bloko puslapis**.</span><span class="sxs-lookup"><span data-stu-id="3057c-173">Use the hero template that you just created to create a page that is named **content block page**.</span></span>
1. <span data-ttu-id="3057c-174">Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="3057c-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3057c-175">Dialogo lango **Modulio įtraukimas** dalyje **Pasirinkti modulius** pasirinkite pagrindinės reklaminės juostos modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3057c-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="3057c-176">Kairėje esančiame struktūros medyje pasirinkite turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="3057c-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="3057c-177">Dešinėje esančioje ypatybių srityje pasirinkite **Įtraukti vaizdą**.</span><span class="sxs-lookup"><span data-stu-id="3057c-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="3057c-178">Tada pasirinkite esamą vaizdą arba nusiųskite naują.</span><span class="sxs-lookup"><span data-stu-id="3057c-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="3057c-179">Pasirinkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="3057c-179">Select **Heading**.</span></span>
1. <span data-ttu-id="3057c-180">Dialogo lange **Antraštė** įtraukite antraštės tekstą, pasirinkite antraštės lygį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3057c-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="3057c-181">Dalyje **Raiškusis tekstas** įtraukite reikiamą tekstą.</span><span class="sxs-lookup"><span data-stu-id="3057c-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="3057c-182">Pasirinkite **Pridėti saitą**.</span><span class="sxs-lookup"><span data-stu-id="3057c-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="3057c-183">Dialogo lange **Saitas** įtraukite saito tekstą, saito URL ir saito ARIA žymą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3057c-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="3057c-184">Pasirinkite maketą **Pagrindinis**.</span><span class="sxs-lookup"><span data-stu-id="3057c-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="3057c-185">Įrašykite puslapį ir peržiūrėkite keitimus.</span><span class="sxs-lookup"><span data-stu-id="3057c-185">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="3057c-186">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="3057c-186">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3057c-187">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3057c-187">Additional resources</span></span>

[<span data-ttu-id="3057c-188">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="3057c-188">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3057c-189">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="3057c-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="3057c-190">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="3057c-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="3057c-191">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="3057c-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="3057c-192">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="3057c-192">Video player module</span></span>](add-video-player.md)
