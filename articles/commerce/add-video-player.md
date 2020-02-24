---
title: Vaizdo įrašų leistuvo modulis
description: Šioje temoje aprašomi vaizdo įrašų leistuvo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025664"
---
# <a name="video-player-module"></a><span data-ttu-id="bc6c3-103">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="bc6c3-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bc6c3-104">Šioje temoje aprašomi vaizdo įrašų leistuvo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bc6c3-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="bc6c3-105">Overview</span></span>

<span data-ttu-id="bc6c3-106">Vaizdo įrašų leistuvo modulis naudojamas vaizdo įrašų atkūrimo galimybei palaikyti.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="bc6c3-107">Jis gali būti įtrauktas į bet kurį puslapį, jei vaizdo įrašo turinys įkeliamas ir pasiekiamas turinio valdymo sistemoje (TVS).</span><span class="sxs-lookup"><span data-stu-id="bc6c3-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="bc6c3-108">Vaizdo įrašų leistuvo modulis palaiko .mp4 medijos tipą.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="bc6c3-109">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="bc6c3-109">Video player module</span></span>

<span data-ttu-id="bc6c3-110">Naudojant vaizdo įrašų leistuvo modulį, el. prekybos svetainėje galima parodyti vaizdo įrašus.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="bc6c3-111">Jis palaiko visas atkūrimo galimybes, pvz., leidimo, pristabdymo, viso dydžio režimo, garso aprašymų ir subtitrų.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="bc6c3-112">Vaizdo įrašų leistuvo modulis taip pat palaiko subtitrų tinkinimo galimybę, kad jie atitiktų „Microsoft“ pritaikymo neįgaliesiems standartus.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="bc6c3-113">Pavyzdžiui, galite tinkinti šrifto dydį ir fono spalvą.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="bc6c3-114">Vaizdo įrašų leistuvo modulis taip pat palaiko antrinius garso takelius.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="bc6c3-115">Įkeliant vaizdo įrašą TVS, taip pat galima įkelti antrinį garso takelį.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="bc6c3-116">Tada, jei vartotojas pasirenka antrinį garso takelį, vaizdo įrašų leistuvo modulis gali jį leisti.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="bc6c3-117">Vaizdo įrašų leistuvo modulio pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="bc6c3-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="bc6c3-118">Mokomieji vaizdo įrašai produktų išsamios informacijos puslapiuose ar rinkodaros puslapiuose</span><span class="sxs-lookup"><span data-stu-id="bc6c3-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="bc6c3-119">Reklaminiai vaizdo įrašai arba vaizdo įrašai apie strategijas bet kuriame rinkodaros puslapyje</span><span class="sxs-lookup"><span data-stu-id="bc6c3-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="bc6c3-120">Rinkodaros vaizdo įrašai, akcentuojantys produktų ypatybes produktų išsamios informacijos puslapiuose ar rinkodaros puslapiuose</span><span class="sxs-lookup"><span data-stu-id="bc6c3-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="bc6c3-121">Vaizdo įrašų leistuvo modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="bc6c3-121">Video player module properties</span></span>

| <span data-ttu-id="bc6c3-122">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="bc6c3-122">Property name</span></span>         | <span data-ttu-id="bc6c3-123">Vertė</span><span class="sxs-lookup"><span data-stu-id="bc6c3-123">Value</span></span>                               | <span data-ttu-id="bc6c3-124">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="bc6c3-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="bc6c3-125">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="bc6c3-125">Auto play</span></span>             | <span data-ttu-id="bc6c3-126">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="bc6c3-126">**True** or **False**</span></span>               | <span data-ttu-id="bc6c3-127">Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas paleidžiamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="bc6c3-128">Nutildyti</span><span class="sxs-lookup"><span data-stu-id="bc6c3-128">Mute</span></span>                  | <span data-ttu-id="bc6c3-129">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="bc6c3-129">**True** or **False**</span></span>               | <span data-ttu-id="bc6c3-130">Kai reikšmė nustatoma kaip **Teisinga**, garsas yra nutildomas.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="bc6c3-131">Numatytoji šio leistuvo reikšmė yra **Klaidinga**.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="bc6c3-132">Naršyklėje „Chrome“ automatiškai leidžiami vaizdo įrašai yra nutildyti pagal numatytuosius parametrus, o garsas leidžiamas, tik jei vartotojas pats paleidžia vaizdo įrašą.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="bc6c3-133">Ciklas</span><span class="sxs-lookup"><span data-stu-id="bc6c3-133">Loop</span></span>                  | <span data-ttu-id="bc6c3-134">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="bc6c3-134">**True** or **False**</span></span>               | <span data-ttu-id="bc6c3-135">Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas vis kartojamas.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="bc6c3-136">Publikavimo kanalai</span><span class="sxs-lookup"><span data-stu-id="bc6c3-136">Media</span></span>                 | <span data-ttu-id="bc6c3-137">Vaizdo įrašo failo kelias ir pavadinimas</span><span class="sxs-lookup"><span data-stu-id="bc6c3-137">Video file path and name</span></span> | <span data-ttu-id="bc6c3-138">Vaizdo įrašo failas, leidžiamas vaizdo įrašų leistuve.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="bc6c3-139">Leisti visame ekrane</span><span class="sxs-lookup"><span data-stu-id="bc6c3-139">Play fullscreen</span></span>       | <span data-ttu-id="bc6c3-140">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="bc6c3-140">**True** or **False**</span></span>               | <span data-ttu-id="bc6c3-141">Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas paleidžiamas viso ekrano režimu.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="bc6c3-142">Paleidiklis Leisti / pristabdyti</span><span class="sxs-lookup"><span data-stu-id="bc6c3-142">Play pause trigger</span></span>    | <span data-ttu-id="bc6c3-143">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="bc6c3-143">**True** or **False**</span></span>               | <span data-ttu-id="bc6c3-144">Kai reikšmė nustatoma kaip **Teisinga**, rodomas vaizdo įrašo leidimo / pristabdymo mygtukas.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="bc6c3-145">Vaizdo įrašų leistuvo valdikliai</span><span class="sxs-lookup"><span data-stu-id="bc6c3-145">Video player controls</span></span> | <span data-ttu-id="bc6c3-146">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="bc6c3-146">**True** or **False**</span></span>               | <span data-ttu-id="bc6c3-147">Kai reikšmė nustatoma kaip **Teisinga**, rodomi visi vaizdo įrašų leistuvo valdikliai.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="bc6c3-148">Šie valdikliai apima leidimo ir pristabdymo mygtukus, eigos indikatorių bei subtitrų parinktis.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="bc6c3-149">Slėpti plakato vaizdą</span><span class="sxs-lookup"><span data-stu-id="bc6c3-149">Hide poster image</span></span>     | <span data-ttu-id="bc6c3-150">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="bc6c3-150">**True** or **False**</span></span>               | <span data-ttu-id="bc6c3-151">Vaizdo įrašas gali turėti atsklandą.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-151">A video can have a poster frame.</span></span> <span data-ttu-id="bc6c3-152">Kai šios ypatybės reikšmė nustatoma kaip **Teisinga**, atsklanda paslepiama.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="bc6c3-153">Maskavimo lygis</span><span class="sxs-lookup"><span data-stu-id="bc6c3-153">Mask level</span></span>            | <span data-ttu-id="bc6c3-154">Skaičius nuo **0** iki **100**</span><span class="sxs-lookup"><span data-stu-id="bc6c3-154">A number from **0** through **100**</span></span> | <span data-ttu-id="bc6c3-155">Maskavimas, taikomas vaizdo įrašui dėl stiliaus.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="bc6c3-156">Vaizdo įrašų leistuvo modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="bc6c3-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="bc6c3-157">Prieš kurdami vaizdo įrašų leistuvo modulį, pirmiausia turite įkelti vaizdo įrašą į medijų biblioteką.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="bc6c3-158">Norėdami į naują puslapį įtraukti vaizdo įrašų leistuvo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="bc6c3-159">Sukurkite puslapio šabloną, pavadintą **vaizdo įrašų leistuvo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="bc6c3-160">Numatytojo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="bc6c3-161">Konteinerio modulyje įtraukite vaizdo įrašų leistuvo ir aplinkos vaizdo įrašų leistuvo modulius.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="bc6c3-162">Baikite šablono redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="bc6c3-163">Naudodami ką tik sukurtą vaizdo įrašų leistuvo šabloną, sukurkite puslapį, pavadintą **vaizdo įrašų leistuvo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="bc6c3-164">Naujo puslapio vietoje **Pagrindinis** įtraukite vaizdo įrašų leistuvo modulį.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="bc6c3-165">Vaizdo įrašų leistuvo modulio ypatybių srityje pasirinkite **Įtraukti vaizdo įrašą**.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="bc6c3-166">Dialogo lange **Medijos parinkiklis** pasirinkite vaizdo įrašą, tada pasirinkite **Įkelti naują medijos elementą**.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="bc6c3-167">Puslapį įrašykite ir peržiūrėkite.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-167">Save and preview the page.</span></span> <span data-ttu-id="bc6c3-168">Puslapyje turėtumėte matyti vaizdo įrašų leistuvo modulį.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-168">You should see the video module on the page.</span></span> <span data-ttu-id="bc6c3-169">Keisdami papildomus parametrus, galite tinkinti modulio veikimą.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="bc6c3-170">Baikite puslapio redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="bc6c3-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc6c3-171">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bc6c3-171">Additional resources</span></span>

[<span data-ttu-id="bc6c3-172">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="bc6c3-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bc6c3-173">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="bc6c3-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="bc6c3-174">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="bc6c3-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="bc6c3-175">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="bc6c3-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="bc6c3-176">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="bc6c3-176">Content block module</span></span>](add-hero-module.md)
