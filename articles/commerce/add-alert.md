---
title: Reklaminės juostos modulis
description: Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: 12cabbf0b8d9f337f15a8cd6cb1f2a85100b75f7
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269779"
---
# <a name="promo-banner-module"></a><span data-ttu-id="f8759-103">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="f8759-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f8759-104">Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="f8759-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8759-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="f8759-105">Overview</span></span>

<span data-ttu-id="f8759-106">Reklaminės juostos moduliai naudojami, kad puslapyje būtų rodomi įdėtieji informaciniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="f8759-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="f8759-107">Juos naudojant, visuose el. prekybos svetainės puslapiuose galima rodyti akcijas.</span><span class="sxs-lookup"><span data-stu-id="f8759-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="f8759-108">Reklaminės juostos moduliai palaiko tekstinio pranešimo ir saito galimybę.</span><span class="sxs-lookup"><span data-stu-id="f8759-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="f8759-109">Jei į reklaminės juostos modulį įtraukiami keli pranešimai, ji tampa besisukančia karuselės juosta, todėl vartotojai gali eiti per visus pranešimus.</span><span class="sxs-lookup"><span data-stu-id="f8759-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="f8759-110">Reklaminės juostos moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f8759-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="f8759-111">Reklaminės juostos el. prekyboje naudojimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="f8759-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="f8759-112">Reklamines juostas galima naudoti svetainės antraštėje, kad būtų rodomos visos svetainės akcijos ar pranešimai, kaip pateikiama šiuose pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="f8759-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="f8759-113">„Metinis išpardavimas baigiasi už 10 dienų“</span><span class="sxs-lookup"><span data-stu-id="f8759-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="f8759-114">„Daug sutaupykite pasinaudodami priešmokyklinio išpardavimo pasiūlymais.</span><span class="sxs-lookup"><span data-stu-id="f8759-114">"Save big with back to school sale.</span></span> <span data-ttu-id="f8759-115">Apsipirkite jau dabar.“</span><span class="sxs-lookup"><span data-stu-id="f8759-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="f8759-116">Reklaminės juostos modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="f8759-116">Promo banner module properties</span></span>

| <span data-ttu-id="f8759-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f8759-117">Property name</span></span>             | <span data-ttu-id="f8759-118">Value</span><span class="sxs-lookup"><span data-stu-id="f8759-118">Value</span></span>                              | <span data-ttu-id="f8759-119">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="f8759-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="f8759-120">Juostos pranešimai</span><span class="sxs-lookup"><span data-stu-id="f8759-120">Banner messages</span></span>           | <span data-ttu-id="f8759-121">Tekstas ir saitai</span><span class="sxs-lookup"><span data-stu-id="f8759-121">Text and links</span></span>                     | <span data-ttu-id="f8759-122">Teksto ir saitų masyvas.</span><span class="sxs-lookup"><span data-stu-id="f8759-122">An array of text and links.</span></span> |
| <span data-ttu-id="f8759-123">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="f8759-123">Autoplay</span></span>                  | <span data-ttu-id="f8759-124">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="f8759-124">**True** or **False**</span></span>              | <span data-ttu-id="f8759-125">Reikšmė, nurodanti, ar pranešimai automatiškai atlieka visą ciklą, jei sukonfigūruoti keli pranešimai.</span><span class="sxs-lookup"><span data-stu-id="f8759-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="f8759-126">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="f8759-126">Slide transition interval</span></span> | <span data-ttu-id="f8759-127">Milisekundžių skaičius (ms)</span><span class="sxs-lookup"><span data-stu-id="f8759-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="f8759-128">Intervalas, naudojamas norint peržiūrėti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="f8759-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="f8759-129">Leisti atmesti</span><span class="sxs-lookup"><span data-stu-id="f8759-129">Allow dismiss</span></span>             | <span data-ttu-id="f8759-130">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="f8759-130">**True** or **False**</span></span>              | <span data-ttu-id="f8759-131">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="f8759-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="f8759-132">Karuselės peleko rodymas</span><span class="sxs-lookup"><span data-stu-id="f8759-132">Show carousel flipper</span></span>     | <span data-ttu-id="f8759-133">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="f8759-133">**True** or **False**</span></span>              | <span data-ttu-id="f8759-134">Reikšmė, nurodanti, ar reikia rodyti karuselės pelekus, kad klientai galėtų rankiniu būdu pereiti per kelis reklaminės juostos elementus.</span><span class="sxs-lookup"><span data-stu-id="f8759-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="f8759-135">Teksto išlygiavimas</span><span class="sxs-lookup"><span data-stu-id="f8759-135">Text alignment</span></span>            | <span data-ttu-id="f8759-136">**Kairėje**, **Dešinėje** arba **Centre**</span><span class="sxs-lookup"><span data-stu-id="f8759-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="f8759-137">Teksto lygiuotė reklaminės juostos modulyje.</span><span class="sxs-lookup"><span data-stu-id="f8759-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="f8759-138">Saitas</span><span class="sxs-lookup"><span data-stu-id="f8759-138">Link</span></span>                      | <span data-ttu-id="f8759-139">A URL</span><span class="sxs-lookup"><span data-stu-id="f8759-139">A URL</span></span>                              | <span data-ttu-id="f8759-140">Nebūtino saito URL.</span><span class="sxs-lookup"><span data-stu-id="f8759-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="f8759-141">Reklaminės juostos modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="f8759-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="f8759-142">Norėdami į puslapį įtraukti reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f8759-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f8759-143">Pasirinkite **Naujas**, kad sukurtumėte puslapio šabloną.</span><span class="sxs-lookup"><span data-stu-id="f8759-143">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="f8759-144">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Reklaminės juostos šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f8759-144">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f8759-145">Dalyje **Puslapio kontūras** įtraukite **Numatytasis puslapis** modulį į atkarpą **Pagrindinis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="f8759-145">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="f8759-146">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="f8759-146">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="f8759-147">Naudodami ką tik sukurtą šabloną, sukurkite puslapį, pavadintą **Reklaminės juostos puslapis**.</span><span class="sxs-lookup"><span data-stu-id="f8759-147">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="f8759-148">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="f8759-148">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="f8759-149">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti konteineris**.</span><span class="sxs-lookup"><span data-stu-id="f8759-149">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="f8759-150">Dalyje **Puslapio kontūras** įtraukite reklaminės juostos modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="f8759-150">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="f8759-151">Reklaminės juostos parametruose įtraukite vieną arba kelis reklaminės juostos pranešimus.</span><span class="sxs-lookup"><span data-stu-id="f8759-151">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="f8759-152">Kiekvienas pranešimas gali turėti tekstą kartu su saitu.</span><span class="sxs-lookup"><span data-stu-id="f8759-152">Each message can have text together with a link.</span></span> <span data-ttu-id="f8759-153">Jei norite modulį tinkinti daugiau, galite redaguoti kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="f8759-153">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="f8759-154">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="f8759-154">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f8759-155">Puslapio viršuje turėtumėte matyti įspėjimą su jūsų įtrauktu tekstu.</span><span class="sxs-lookup"><span data-stu-id="f8759-155">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="f8759-156">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="f8759-156">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="f8759-157">Reklaminė juosta paprastai naudojama puslapio antraštės atkarpoje arba paantraštės atkarpoje.</span><span class="sxs-lookup"><span data-stu-id="f8759-157">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="f8759-158">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f8759-158">Additional resources</span></span>

[<span data-ttu-id="f8759-159">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="f8759-159">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f8759-160">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="f8759-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="f8759-161">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="f8759-161">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f8759-162">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="f8759-162">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f8759-163">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="f8759-163">Video player module</span></span>](add-video-player.md)
