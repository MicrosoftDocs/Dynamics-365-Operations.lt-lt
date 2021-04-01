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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206588"
---
# <a name="promo-banner-module"></a><span data-ttu-id="7cf0e-103">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="7cf0e-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7cf0e-104">Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7cf0e-105">Reklaminės juostos moduliai naudojami, kad puslapyje būtų rodomi įdėtieji informaciniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="7cf0e-106">Juos naudojant, visuose el. prekybos svetainės puslapiuose galima rodyti akcijas.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="7cf0e-107">Reklaminės juostos moduliai palaiko tekstinio pranešimo ir saito galimybę.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="7cf0e-108">Jei į reklaminės juostos modulį įtraukiami keli pranešimai, ji tampa besisukančia karuselės juosta, todėl vartotojai gali eiti per visus pranešimus.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="7cf0e-109">Reklaminės juostos moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="7cf0e-110">Reklaminės juostos el. prekyboje naudojimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="7cf0e-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="7cf0e-111">Reklamines juostas galima naudoti svetainės antraštėje, kad būtų rodomos visos svetainės akcijos ar pranešimai, kaip pateikiama šiuose pavyzdžiuose.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="7cf0e-112">„Metinis išpardavimas baigiasi už 10 dienų“</span><span class="sxs-lookup"><span data-stu-id="7cf0e-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="7cf0e-113">„Daug sutaupykite pasinaudodami priešmokyklinio išpardavimo pasiūlymais.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-113">"Save big with back to school sale.</span></span> <span data-ttu-id="7cf0e-114">Apsipirkite jau dabar.“</span><span class="sxs-lookup"><span data-stu-id="7cf0e-114">Shop Now."</span></span>

<span data-ttu-id="7cf0e-115">„Apsipirkite per Padėkos dienos IŠPARDAVIMĄ!“</span><span class="sxs-lookup"><span data-stu-id="7cf0e-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="7cf0e-116">Toliau pateiktame vaizde parodytas reklaminės juostos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-116">The following image shows an example of a promo banner.</span></span>

![Reklaminės juostos modulio pavyzdys](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="7cf0e-118">Reklaminės juostos modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="7cf0e-118">Promo banner module properties</span></span>

| <span data-ttu-id="7cf0e-119">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="7cf0e-119">Property name</span></span>             | <span data-ttu-id="7cf0e-120">Vertė</span><span class="sxs-lookup"><span data-stu-id="7cf0e-120">Value</span></span>                              | <span data-ttu-id="7cf0e-121">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7cf0e-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="7cf0e-122">Juostos pranešimai</span><span class="sxs-lookup"><span data-stu-id="7cf0e-122">Banner messages</span></span>           | <span data-ttu-id="7cf0e-123">Tekstas ir saitai</span><span class="sxs-lookup"><span data-stu-id="7cf0e-123">Text and links</span></span>                     | <span data-ttu-id="7cf0e-124">Teksto ir saitų masyvas.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-124">An array of text and links.</span></span> |
| <span data-ttu-id="7cf0e-125">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="7cf0e-125">Autoplay</span></span>                  | <span data-ttu-id="7cf0e-126">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="7cf0e-126">**True** or **False**</span></span>              | <span data-ttu-id="7cf0e-127">Reikšmė, nurodanti, ar pranešimai automatiškai atlieka visą ciklą, jei sukonfigūruoti keli pranešimai.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="7cf0e-128">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="7cf0e-128">Slide transition interval</span></span> | <span data-ttu-id="7cf0e-129">Milisekundžių skaičius (ms)</span><span class="sxs-lookup"><span data-stu-id="7cf0e-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="7cf0e-130">Intervalas, naudojamas norint peržiūrėti pranešimus.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="7cf0e-131">Leisti atmesti</span><span class="sxs-lookup"><span data-stu-id="7cf0e-131">Allow dismiss</span></span>             | <span data-ttu-id="7cf0e-132">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="7cf0e-132">**True** or **False**</span></span>              | <span data-ttu-id="7cf0e-133">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="7cf0e-134">Karuselės peleko rodymas</span><span class="sxs-lookup"><span data-stu-id="7cf0e-134">Show carousel flipper</span></span>     | <span data-ttu-id="7cf0e-135">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="7cf0e-135">**True** or **False**</span></span>              | <span data-ttu-id="7cf0e-136">Reikšmė, nurodanti, ar reikia rodyti karuselės pelekus, kad klientai galėtų rankiniu būdu pereiti per kelis reklaminės juostos elementus.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="7cf0e-137">Teksto išlygiavimas</span><span class="sxs-lookup"><span data-stu-id="7cf0e-137">Text alignment</span></span>            | <span data-ttu-id="7cf0e-138">**Kairėje**, **Dešinėje** arba **Centre**</span><span class="sxs-lookup"><span data-stu-id="7cf0e-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="7cf0e-139">Teksto lygiuotė reklaminės juostos modulyje.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="7cf0e-140">Saitas</span><span class="sxs-lookup"><span data-stu-id="7cf0e-140">Link</span></span>                      | <span data-ttu-id="7cf0e-141">A URL</span><span class="sxs-lookup"><span data-stu-id="7cf0e-141">A URL</span></span>                              | <span data-ttu-id="7cf0e-142">Nebūtino saito URL.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="7cf0e-143">Reklaminės juostos modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="7cf0e-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="7cf0e-144">Norėdami į puslapį įtraukti reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7cf0e-145">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7cf0e-146">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Reklaminės juostos šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="7cf0e-147">Dalyje **Puslapio kontūras** įtraukite **Numatytasis puslapis** modulį į atkarpą **Pagrindinis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="7cf0e-148">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="7cf0e-149">Naudodami ką tik sukurtą šabloną, sukurkite puslapį, pavadintą **Reklaminės juostos puslapis**.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="7cf0e-150">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="7cf0e-151">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti konteineris**.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="7cf0e-152">Dalyje **Puslapio kontūras** įtraukite reklaminės juostos modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="7cf0e-153">Reklaminės juostos parametruose įtraukite vieną arba kelis reklaminės juostos pranešimus.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="7cf0e-154">Kiekvienas pranešimas gali turėti tekstą kartu su saitu.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-154">Each message can have text together with a link.</span></span> <span data-ttu-id="7cf0e-155">Jei norite modulį tinkinti daugiau, galite redaguoti kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="7cf0e-156">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="7cf0e-157">Puslapio viršuje turėtumėte matyti įspėjimą su jūsų įtrauktu tekstu.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="7cf0e-158">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="7cf0e-159">Reklaminė juosta paprastai naudojama puslapio antraštės atkarpoje arba paantraštės atkarpoje.</span><span class="sxs-lookup"><span data-stu-id="7cf0e-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="7cf0e-160">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7cf0e-160">Additional resources</span></span>

[<span data-ttu-id="7cf0e-161">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="7cf0e-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7cf0e-162">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="7cf0e-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="7cf0e-163">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="7cf0e-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="7cf0e-164">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="7cf0e-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="7cf0e-165">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="7cf0e-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]