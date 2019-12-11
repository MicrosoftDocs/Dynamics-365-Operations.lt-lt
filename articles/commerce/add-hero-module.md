---
title: Pagrindinės reklaminės juostos modulis
description: Šioje temoje aprašomi pagrindinės reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785400"
---
# <a name="hero-module"></a><span data-ttu-id="40f0e-103">Pagrindinės reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="40f0e-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="40f0e-104">Šioje temoje aprašomi pagrindinės reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="40f0e-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="40f0e-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="40f0e-105">Overview</span></span>

<span data-ttu-id="40f0e-106">Pagrindinės reklaminės juostos modulis naudojamas produktams ar akcijoms reklamuoti derinant vaizdus ir tekstą.</span><span class="sxs-lookup"><span data-stu-id="40f0e-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="40f0e-107">Pavyzdžiui, pardavėjas pagrindinės reklaminės juostos modulį gali įtraukti į pagrindinį el. prekybos svetainės puslapį, kad reklamuotų naują produktą ir pritrauktų klientų dėmesį.</span><span class="sxs-lookup"><span data-stu-id="40f0e-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="40f0e-108">Pagrindinės reklaminės juostos modulis grindžiamas duomenimis iš turinio valdymo sistemos (TVS).</span><span class="sxs-lookup"><span data-stu-id="40f0e-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="40f0e-109">Tai yra atskiras modulis, nepriklausantis nuo jokių kitų puslapio modulių.</span><span class="sxs-lookup"><span data-stu-id="40f0e-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="40f0e-110">Pagrindinės reklaminės juostos modulį galima įdėti bet kuriame svetainės puslapyje, kuriame pardavėjas nori kažką parduoti ar reklamuoti, (pavyzdžiui, produktus, išpardavimus ar ypatybes).</span><span class="sxs-lookup"><span data-stu-id="40f0e-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="40f0e-111">Pagrindinės reklaminės juostos modulio pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="40f0e-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="40f0e-112">Pagrindinės reklaminės juostos modulį galima naudoti pagrindiniame el. prekybos svetainės puslapyje, norint akcentuoti akcijas ir naujus produktus.</span><span class="sxs-lookup"><span data-stu-id="40f0e-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="40f0e-113">Pagrindinės reklaminės juostos modulį galima naudoti išsamios produktų informacijos puslapyje, norint parodyti produktų informaciją.</span><span class="sxs-lookup"><span data-stu-id="40f0e-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="40f0e-114">Kelis pagrindinės reklaminės juostos modulius galima įdėti į karuselės modulį, norint akcentuoti kelis produktus ar akcijas.</span><span class="sxs-lookup"><span data-stu-id="40f0e-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="40f0e-115">Pagrindinės reklaminės juostos modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="40f0e-115">Hero module properties</span></span>

| <span data-ttu-id="40f0e-116">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="40f0e-116">Property name</span></span>  | <span data-ttu-id="40f0e-117">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="40f0e-117">Values</span></span> | <span data-ttu-id="40f0e-118">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="40f0e-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="40f0e-119">Vaizdas</span><span class="sxs-lookup"><span data-stu-id="40f0e-119">Image</span></span>          | <span data-ttu-id="40f0e-120">Vaizdo failas</span><span class="sxs-lookup"><span data-stu-id="40f0e-120">Image file</span></span> | <span data-ttu-id="40f0e-121">Parodyti produktą ar akciją galima naudojant vaizdą.</span><span class="sxs-lookup"><span data-stu-id="40f0e-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="40f0e-122">Vaizdą galima nusiųsti į vaizdų galeriją arba galima naudoti esamą vaizdą.</span><span class="sxs-lookup"><span data-stu-id="40f0e-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="40f0e-123">Antraštė</span><span class="sxs-lookup"><span data-stu-id="40f0e-123">Heading</span></span>        | <span data-ttu-id="40f0e-124">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**)</span><span class="sxs-lookup"><span data-stu-id="40f0e-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="40f0e-125">Kiekviename pagrindinės reklaminės juostos modulyje gali būti antraštė.</span><span class="sxs-lookup"><span data-stu-id="40f0e-125">Every hero module can have a heading.</span></span> <span data-ttu-id="40f0e-126">Numatyta, kad naudojama antrašės žymė **H2**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="40f0e-127">Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="40f0e-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="40f0e-128">Pastraipa</span><span class="sxs-lookup"><span data-stu-id="40f0e-128">Paragraph</span></span>      | <span data-ttu-id="40f0e-129">Pastraipos tekstas</span><span class="sxs-lookup"><span data-stu-id="40f0e-129">Paragraph text</span></span> | <span data-ttu-id="40f0e-130">Pagrindinės reklaminės juostos moduliai palaiko pastraipos tekstą raiškiojo teksto formatu.</span><span class="sxs-lookup"><span data-stu-id="40f0e-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="40f0e-131">Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas bei hipersaitai.</span><span class="sxs-lookup"><span data-stu-id="40f0e-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="40f0e-132">Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema.</span><span class="sxs-lookup"><span data-stu-id="40f0e-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="40f0e-133">Saitas</span><span class="sxs-lookup"><span data-stu-id="40f0e-133">Link</span></span>           | <span data-ttu-id="40f0e-134">Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke**</span><span class="sxs-lookup"><span data-stu-id="40f0e-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="40f0e-135">Pagrindinės reklaminės juostos moduliai palaiko vieną ar kelis raginimo imtis veiksmų saitus.</span><span class="sxs-lookup"><span data-stu-id="40f0e-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="40f0e-136">Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma.</span><span class="sxs-lookup"><span data-stu-id="40f0e-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="40f0e-137">ARIA žymos turi būti aprašomosios, kad atitiktų pritaikymo neįgaliesiems reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="40f0e-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="40f0e-138">Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke.</span><span class="sxs-lookup"><span data-stu-id="40f0e-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="40f0e-139">Teksto talpinimas</span><span class="sxs-lookup"><span data-stu-id="40f0e-139">Text placement</span></span> | <span data-ttu-id="40f0e-140">**Viršuje kairėje**, **Viršuje dešinėje**, **Viršuje centre**, **Apačioje kairėje**, **Apačioje dešinėje**, **Apačioje centre**, **Centre kairėje**, **Centre dešinėje** arba **Pačiame centre**</span><span class="sxs-lookup"><span data-stu-id="40f0e-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="40f0e-141">Ši ypatybė nustato vaizdo padėtį teksto atžvilgiu.</span><span class="sxs-lookup"><span data-stu-id="40f0e-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="40f0e-142">Pavyzdžiui, jei pasirenkama **Dešinėje**, vaizdas rodomas teksto dešinėje.</span><span class="sxs-lookup"><span data-stu-id="40f0e-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="40f0e-143">Teksto tema</span><span class="sxs-lookup"><span data-stu-id="40f0e-143">Text theme</span></span>     | <span data-ttu-id="40f0e-144">**Šviesi** arba **Tamsi**</span><span class="sxs-lookup"><span data-stu-id="40f0e-144">**Light** or **Dark**</span></span> | <span data-ttu-id="40f0e-145">Pagal fono vaizdą galima nustatyti teksto spalvų schemą.</span><span class="sxs-lookup"><span data-stu-id="40f0e-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="40f0e-146">Pavyzdžiui, jei vaizdo fonas yra tamsus, galima taikyti šviesią temą, kad tekstas būtų matomesnis ir būtų pasiektas spalvų kontrasto santykis pritaikymo neįgaliesiems tikslais.</span><span class="sxs-lookup"><span data-stu-id="40f0e-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="40f0e-147">Perėjimas</span><span class="sxs-lookup"><span data-stu-id="40f0e-147">Gradient</span></span>       | <span data-ttu-id="40f0e-148">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="40f0e-148">**True** or **False**</span></span> | <span data-ttu-id="40f0e-149">Siekiant pasiekti spalvų kontrasto santykius pritaikymo neįgaliesiems tikslais, vaizdui galima taikyti perėjimą.</span><span class="sxs-lookup"><span data-stu-id="40f0e-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="40f0e-150">Pagrindinės reklaminės juostos modulio įtraukimas į naują puslapį</span><span class="sxs-lookup"><span data-stu-id="40f0e-150">Add a hero module to a new page</span></span>

<span data-ttu-id="40f0e-151">Norėdami į naują puslapį įtraukti pagrindinės reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="40f0e-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="40f0e-152">Nueikite į **Šablonai** ir sukurkite puslapio šabloną pavadinimu **pagrindinės reklaminės juostos šablonas**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="40f0e-153">Numatytojo puslapio vietoje **Pagrindinis** įtraukite pagrindinės reklaminės juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="40f0e-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="40f0e-154">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="40f0e-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="40f0e-155">Naudodami ką tik sukurtą pagrindinės reklaminės juostos šabloną, sukurkite puslapį, pavadintą **pagrindinės reklaminės juostos puslapis**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="40f0e-156">Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="40f0e-157">Dialogo lango **Modulio įtraukimas** dalyje **Pasirinkti modulius** pasirinkite pagrindinės reklaminės juostos modulį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="40f0e-158">Kairėje esančiame struktūros medyje pasirinkite pagrindinės reklaminės juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="40f0e-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="40f0e-159">Dešinėje esančioje ypatybių srityje pasirinkite **Įtraukti vaizdą**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="40f0e-160">Tada pasirinkite esamą vaizdą arba nusiųskite naują.</span><span class="sxs-lookup"><span data-stu-id="40f0e-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="40f0e-161">Pasirinkite **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-161">Select **Heading**.</span></span>
1. <span data-ttu-id="40f0e-162">Dialogo lange **Antraštė** įtraukite antraštės tekstą, pasirinkite antraštės lygį ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="40f0e-163">Dalyje **Raiškusis tekstas** įtraukite reikiamą tekstą.</span><span class="sxs-lookup"><span data-stu-id="40f0e-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="40f0e-164">Pasirinkite **Įtraukti veiksmo saitą**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="40f0e-165">Dialogo lange **Veiksmo saitas** įtraukite saito tekstą, saito URL ir saito ARIA žymą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="40f0e-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="40f0e-166">Įrašykite puslapį ir peržiūrėkite keitimus.</span><span class="sxs-lookup"><span data-stu-id="40f0e-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="40f0e-167">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="40f0e-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40f0e-168">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="40f0e-168">Additional resources</span></span>

[<span data-ttu-id="40f0e-169">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="40f0e-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="40f0e-170">Įspėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="40f0e-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="40f0e-171">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="40f0e-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="40f0e-172">Raiškiojo turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="40f0e-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="40f0e-173">Turinio išdėstymo modulis</span><span class="sxs-lookup"><span data-stu-id="40f0e-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="40f0e-174">Funkcijos modulis</span><span class="sxs-lookup"><span data-stu-id="40f0e-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="40f0e-175">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="40f0e-175">Video player module</span></span>](add-video-player.md)
