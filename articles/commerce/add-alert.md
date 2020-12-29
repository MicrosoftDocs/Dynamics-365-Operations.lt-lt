---
title: Reklaminės juostos modulis
description: Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: d9debd16b18300d090bde1862a16920d8e9185eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414262"
---
# <a name="promo-banner-module"></a><span data-ttu-id="49648-103">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="49648-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="49648-104">Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="49648-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="49648-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="49648-105">Overview</span></span>

<span data-ttu-id="49648-106">Reklaminės juostos moduliai naudojami, kad puslapyje būtų rodomi įdėtieji informaciniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="49648-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="49648-107">Juos naudojant, visuose el. prekybos svetainės puslapiuose galima rodyti akcijas.</span><span class="sxs-lookup"><span data-stu-id="49648-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="49648-108">Reklaminės juostos moduliai palaiko tekstinio pranešimo ir saito galimybę.</span><span class="sxs-lookup"><span data-stu-id="49648-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="49648-109">Jei į reklaminės juostos modulį įtraukiami keli pranešimai, ji tampa besisukančia karuselės juosta, todėl vartotojai gali eiti per visus pranešimus.</span><span class="sxs-lookup"><span data-stu-id="49648-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="49648-110">Reklaminės juostos moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="49648-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="49648-111">Reklaminės juostos el. prekyboje naudojimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="49648-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="49648-112">Reklamines juostas galima naudoti svetainės antraštėje, kad būtų rodomos visos svetainės akcijos ar pranešimai, kaip pateikiama šiuose pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="49648-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="49648-113">„Metinis išpardavimas baigiasi už 10 dienų“</span><span class="sxs-lookup"><span data-stu-id="49648-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="49648-114">„Daug sutaupykite pasinaudodami priešmokyklinio išpardavimo pasiūlymais.</span><span class="sxs-lookup"><span data-stu-id="49648-114">"Save big with back to school sale.</span></span> <span data-ttu-id="49648-115">Apsipirkite jau dabar.“</span><span class="sxs-lookup"><span data-stu-id="49648-115">Shop Now."</span></span>

<span data-ttu-id="49648-116">„Apsipirkite per Padėkos dienos IŠPARDAVIMĄ!“</span><span class="sxs-lookup"><span data-stu-id="49648-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="49648-117">Toliau pateiktame vaizde parodytas reklaminės juostos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="49648-117">The following image shows an example of a promo banner.</span></span>

![Reklaminės juostos modulio pavyzdys](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="49648-119">Reklaminės juostos modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="49648-119">Promo banner module properties</span></span>

| <span data-ttu-id="49648-120">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="49648-120">Property name</span></span>             | <span data-ttu-id="49648-121">Vertė</span><span class="sxs-lookup"><span data-stu-id="49648-121">Value</span></span>                              | <span data-ttu-id="49648-122">aprašymas</span><span class="sxs-lookup"><span data-stu-id="49648-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="49648-123">Juostos pranešimai</span><span class="sxs-lookup"><span data-stu-id="49648-123">Banner messages</span></span>           | <span data-ttu-id="49648-124">Tekstas ir saitai</span><span class="sxs-lookup"><span data-stu-id="49648-124">Text and links</span></span>                     | <span data-ttu-id="49648-125">Teksto ir saitų masyvas.</span><span class="sxs-lookup"><span data-stu-id="49648-125">An array of text and links.</span></span> |
| <span data-ttu-id="49648-126">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="49648-126">Autoplay</span></span>                  | <span data-ttu-id="49648-127">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="49648-127">**True** or **False**</span></span>              | <span data-ttu-id="49648-128">Reikšmė, nurodanti, ar pranešimai automatiškai atlieka visą ciklą, jei sukonfigūruoti keli pranešimai.</span><span class="sxs-lookup"><span data-stu-id="49648-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="49648-129">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="49648-129">Slide transition interval</span></span> | <span data-ttu-id="49648-130">Milisekundžių skaičius (ms)</span><span class="sxs-lookup"><span data-stu-id="49648-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="49648-131">Intervalas, naudojamas norint peržiūrėti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="49648-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="49648-132">Leisti atmesti</span><span class="sxs-lookup"><span data-stu-id="49648-132">Allow dismiss</span></span>             | <span data-ttu-id="49648-133">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="49648-133">**True** or **False**</span></span>              | <span data-ttu-id="49648-134">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="49648-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="49648-135">Karuselės peleko rodymas</span><span class="sxs-lookup"><span data-stu-id="49648-135">Show carousel flipper</span></span>     | <span data-ttu-id="49648-136">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="49648-136">**True** or **False**</span></span>              | <span data-ttu-id="49648-137">Reikšmė, nurodanti, ar reikia rodyti karuselės pelekus, kad klientai galėtų rankiniu būdu pereiti per kelis reklaminės juostos elementus.</span><span class="sxs-lookup"><span data-stu-id="49648-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="49648-138">Teksto išlygiavimas</span><span class="sxs-lookup"><span data-stu-id="49648-138">Text alignment</span></span>            | <span data-ttu-id="49648-139">**Kairėje**, **Dešinėje** arba **Centre**</span><span class="sxs-lookup"><span data-stu-id="49648-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="49648-140">Teksto lygiuotė reklaminės juostos modulyje.</span><span class="sxs-lookup"><span data-stu-id="49648-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="49648-141">Saitas</span><span class="sxs-lookup"><span data-stu-id="49648-141">Link</span></span>                      | <span data-ttu-id="49648-142">A URL</span><span class="sxs-lookup"><span data-stu-id="49648-142">A URL</span></span>                              | <span data-ttu-id="49648-143">Nebūtino saito URL.</span><span class="sxs-lookup"><span data-stu-id="49648-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="49648-144">Reklaminės juostos modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="49648-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="49648-145">Norėdami į puslapį įtraukti reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="49648-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="49648-146">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="49648-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="49648-147">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Reklaminės juostos šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="49648-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="49648-148">Dalyje **Puslapio kontūras** įtraukite **Numatytasis puslapis** modulį į atkarpą **Pagrindinis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="49648-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="49648-149">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="49648-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="49648-150">Naudodami ką tik sukurtą šabloną, sukurkite puslapį, pavadintą **Reklaminės juostos puslapis**.</span><span class="sxs-lookup"><span data-stu-id="49648-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="49648-151">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="49648-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="49648-152">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti konteineris**.</span><span class="sxs-lookup"><span data-stu-id="49648-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="49648-153">Dalyje **Puslapio kontūras** įtraukite reklaminės juostos modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="49648-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="49648-154">Reklaminės juostos parametruose įtraukite vieną arba kelis reklaminės juostos pranešimus.</span><span class="sxs-lookup"><span data-stu-id="49648-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="49648-155">Kiekvienas pranešimas gali turėti tekstą kartu su saitu.</span><span class="sxs-lookup"><span data-stu-id="49648-155">Each message can have text together with a link.</span></span> <span data-ttu-id="49648-156">Jei norite modulį tinkinti daugiau, galite redaguoti kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="49648-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="49648-157">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="49648-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="49648-158">Puslapio viršuje turėtumėte matyti įspėjimą su jūsų įtrauktu tekstu.</span><span class="sxs-lookup"><span data-stu-id="49648-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="49648-159">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="49648-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="49648-160">Reklaminė juosta paprastai naudojama puslapio antraštės atkarpoje arba paantraštės atkarpoje.</span><span class="sxs-lookup"><span data-stu-id="49648-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="49648-161">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="49648-161">Additional resources</span></span>

[<span data-ttu-id="49648-162">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="49648-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="49648-163">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="49648-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="49648-164">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="49648-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="49648-165">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="49648-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="49648-166">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="49648-166">Video player module</span></span>](add-video-player.md)
