---
title: Reklaminės juostos modulis
description: Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025625"
---
# <a name="promo-banner-module"></a><span data-ttu-id="770ed-103">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="770ed-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="770ed-104">Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="770ed-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="770ed-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="770ed-105">Overview</span></span>

<span data-ttu-id="770ed-106">Reklaminės juostos moduliai naudojami, kad puslapyje būtų rodomi įdėtieji informaciniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="770ed-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="770ed-107">Juos naudojant, visuose el. prekybos svetainės puslapiuose galima rodyti akcijas.</span><span class="sxs-lookup"><span data-stu-id="770ed-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="770ed-108">Reklaminės juostos moduliai palaiko tekstinio pranešimo ir saito galimybę.</span><span class="sxs-lookup"><span data-stu-id="770ed-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="770ed-109">Jei į reklaminės juostos modulį įtraukiami keli pranešimai, ji tampa besisukančia karuselės juosta, todėl vartotojai gali eiti per visus pranešimus.</span><span class="sxs-lookup"><span data-stu-id="770ed-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="770ed-110">Reklaminės juostos moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="770ed-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="770ed-111">Reklaminės juostos el. prekyboje naudojimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="770ed-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="770ed-112">Reklamines juostas galima naudoti svetainės antraštėje, kad būtų rodomos visos svetainės akcijos ar pranešimai, kaip pateikiama šiuose pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="770ed-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="770ed-113">„Metinis išpardavimas baigiasi už 10 dienų“</span><span class="sxs-lookup"><span data-stu-id="770ed-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="770ed-114">„Daug sutaupykite pasinaudodami priešmokyklinio išpardavimo pasiūlymais.</span><span class="sxs-lookup"><span data-stu-id="770ed-114">"Save big with back to school sale.</span></span> <span data-ttu-id="770ed-115">Apsipirkite jau dabar.“</span><span class="sxs-lookup"><span data-stu-id="770ed-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="770ed-116">Reklaminės juostos modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="770ed-116">Promo banner module properties</span></span>

| <span data-ttu-id="770ed-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="770ed-117">Property name</span></span>             | <span data-ttu-id="770ed-118">Value</span><span class="sxs-lookup"><span data-stu-id="770ed-118">Value</span></span>                              | <span data-ttu-id="770ed-119">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="770ed-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="770ed-120">Juostos pranešimai</span><span class="sxs-lookup"><span data-stu-id="770ed-120">Banner messages</span></span>           | <span data-ttu-id="770ed-121">Tekstas ir saitai</span><span class="sxs-lookup"><span data-stu-id="770ed-121">Text and links</span></span>                     | <span data-ttu-id="770ed-122">Teksto ir saitų masyvas.</span><span class="sxs-lookup"><span data-stu-id="770ed-122">An array of text and links.</span></span> |
| <span data-ttu-id="770ed-123">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="770ed-123">Autoplay</span></span>                  | <span data-ttu-id="770ed-124">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="770ed-124">**True** or **False**</span></span>              | <span data-ttu-id="770ed-125">Reikšmė, nurodanti, ar pranešimai automatiškai atlieka visą ciklą, jei sukonfigūruoti keli pranešimai.</span><span class="sxs-lookup"><span data-stu-id="770ed-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="770ed-126">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="770ed-126">Slide transition interval</span></span> | <span data-ttu-id="770ed-127">Milisekundžių skaičius (ms)</span><span class="sxs-lookup"><span data-stu-id="770ed-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="770ed-128">Intervalas, naudojamas norint peržiūrėti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="770ed-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="770ed-129">Leisti atmesti</span><span class="sxs-lookup"><span data-stu-id="770ed-129">Allow dismiss</span></span>             | <span data-ttu-id="770ed-130">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="770ed-130">**True** or **False**</span></span>              | <span data-ttu-id="770ed-131">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="770ed-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="770ed-132">Karuselės peleko rodymas</span><span class="sxs-lookup"><span data-stu-id="770ed-132">Show carousel flipper</span></span>     | <span data-ttu-id="770ed-133">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="770ed-133">**True** or **False**</span></span>              | <span data-ttu-id="770ed-134">Reikšmė, nurodanti, ar reikia rodyti karuselės pelekus, kad klientai galėtų rankiniu būdu pereiti per kelis reklaminės juostos elementus.</span><span class="sxs-lookup"><span data-stu-id="770ed-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="770ed-135">Teksto išlygiavimas</span><span class="sxs-lookup"><span data-stu-id="770ed-135">Text alignment</span></span>            | <span data-ttu-id="770ed-136">**Kairėje**, **Dešinėje** arba **Centre**</span><span class="sxs-lookup"><span data-stu-id="770ed-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="770ed-137">Teksto lygiuotė reklaminės juostos modulyje.</span><span class="sxs-lookup"><span data-stu-id="770ed-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="770ed-138">Saitas</span><span class="sxs-lookup"><span data-stu-id="770ed-138">Link</span></span>                      | <span data-ttu-id="770ed-139">A URL</span><span class="sxs-lookup"><span data-stu-id="770ed-139">A URL</span></span>                              | <span data-ttu-id="770ed-140">Nebūtino saito URL.</span><span class="sxs-lookup"><span data-stu-id="770ed-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="770ed-141">Reklaminės juostos modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="770ed-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="770ed-142">Norėdami į puslapį įtraukti reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="770ed-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="770ed-143">Sukurkite puslapio šabloną, pavadintą **Reklaminės juostos šablonas**.</span><span class="sxs-lookup"><span data-stu-id="770ed-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="770ed-144">Dalyje **Puslapio kontūras** įtraukite **Numatytasis puslapis** modulį į atkarpą **Pagrindinis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="770ed-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="770ed-145">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="770ed-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="770ed-146">Naudodami ką tik sukurtą šabloną, sukurkite puslapį, pavadintą **Reklaminės juostos puslapis**.</span><span class="sxs-lookup"><span data-stu-id="770ed-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="770ed-147">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="770ed-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="770ed-148">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti konteineris**.</span><span class="sxs-lookup"><span data-stu-id="770ed-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="770ed-149">Dalyje **Puslapio kontūras** įtraukite reklaminės juostos modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="770ed-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="770ed-150">Reklaminės juostos parametruose įtraukite vieną arba kelis reklaminės juostos pranešimus.</span><span class="sxs-lookup"><span data-stu-id="770ed-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="770ed-151">Kiekvienas pranešimas gali turėti tekstą kartu su saitu.</span><span class="sxs-lookup"><span data-stu-id="770ed-151">Each message can have text together with a link.</span></span> <span data-ttu-id="770ed-152">Jei norite modulį tinkinti daugiau, galite redaguoti kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="770ed-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="770ed-153">Puslapį įrašykite ir peržiūrėkite.</span><span class="sxs-lookup"><span data-stu-id="770ed-153">Save and preview the page.</span></span> <span data-ttu-id="770ed-154">Puslapio viršuje turėtumėte matyti įspėjimą su jūsų įtrauktu tekstu.</span><span class="sxs-lookup"><span data-stu-id="770ed-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="770ed-155">Baikite puslapio redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="770ed-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="770ed-156">Reklaminė juosta paprastai naudojama puslapio antraštės atkarpoje arba paantraštės atkarpoje.</span><span class="sxs-lookup"><span data-stu-id="770ed-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="770ed-157">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="770ed-157">Additional resources</span></span>

[<span data-ttu-id="770ed-158">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="770ed-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="770ed-159">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="770ed-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="770ed-160">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="770ed-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="770ed-161">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="770ed-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="770ed-162">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="770ed-162">Video player module</span></span>](add-video-player.md)
