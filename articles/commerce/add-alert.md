---
title: Įspėjimo modulis
description: Šioje temoje aprašomi įspėjimo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785357"
---
# <a name="alert-module"></a><span data-ttu-id="1f142-103">Įspėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="1f142-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1f142-104">Šioje temoje aprašomi įspėjimo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="1f142-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1f142-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="1f142-105">Overview</span></span>

<span data-ttu-id="1f142-106">Naudojant įspėjimo modulį puslapyje rodomi įdėtieji informaciniai pranešimai.</span><span class="sxs-lookup"><span data-stu-id="1f142-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="1f142-107">Įspėjimo moduliai palaiko tekstinio pranešimo ir saito galimybę.</span><span class="sxs-lookup"><span data-stu-id="1f142-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="1f142-108">Juos naudojant, visuose el. prekybos svetainės puslapiuose galima rodyti akcijas.</span><span class="sxs-lookup"><span data-stu-id="1f142-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="1f142-109">Įspėjimo moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="1f142-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="1f142-110">Įspėjimo modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="1f142-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="1f142-111">Įspėjimo modulius naudojant svetainės antraštėje, visoje svetainėje galima nurodyti akcijas ar pranešimus.</span><span class="sxs-lookup"><span data-stu-id="1f142-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="1f142-112">Štai keletas pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="1f142-112">Here are some examples:</span></span>

<span data-ttu-id="1f142-113">„Metinis išpardavimas baigiasi už 10 dienų“</span><span class="sxs-lookup"><span data-stu-id="1f142-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="1f142-114">„Daug sutaupykite pasinaudodami priešmokyklinio išpardavimo pasiūlymais.</span><span class="sxs-lookup"><span data-stu-id="1f142-114">"Save big with back to school sale.</span></span> <span data-ttu-id="1f142-115">Apsipirkite jau dabar.“</span><span class="sxs-lookup"><span data-stu-id="1f142-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="1f142-116">Įspėjimo modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="1f142-116">Alert module properties</span></span>

| <span data-ttu-id="1f142-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="1f142-117">Property name</span></span>  | <span data-ttu-id="1f142-118">Vertė</span><span class="sxs-lookup"><span data-stu-id="1f142-118">Value</span></span>                              | <span data-ttu-id="1f142-119">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="1f142-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="1f142-120">Tekstas</span><span class="sxs-lookup"><span data-stu-id="1f142-120">Text</span></span>           | <span data-ttu-id="1f142-121">Tekstas</span><span class="sxs-lookup"><span data-stu-id="1f142-121">Text</span></span>                               | <span data-ttu-id="1f142-122">Įspėjimo modulyje rodomas tekstinis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="1f142-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="1f142-123">Teksto išlygiavimas</span><span class="sxs-lookup"><span data-stu-id="1f142-123">Text alignment</span></span> | <span data-ttu-id="1f142-124">**Kairėje**, **Dešinėje** arba **Centre**</span><span class="sxs-lookup"><span data-stu-id="1f142-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="1f142-125">Reikšmė, apibrėžianti, kaip tekstas lygiuojamas įspėjimo modulyje.</span><span class="sxs-lookup"><span data-stu-id="1f142-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="1f142-126">Atmesti įspėjimą</span><span class="sxs-lookup"><span data-stu-id="1f142-126">Dismiss alert</span></span>  | <span data-ttu-id="1f142-127">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="1f142-127">**True** or **False**</span></span>              | <span data-ttu-id="1f142-128">Jei reikšmė nustatyta kaip **Teisinga**, klientas gali atmesti įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="1f142-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="1f142-129">Saitas</span><span class="sxs-lookup"><span data-stu-id="1f142-129">Link</span></span>           | <span data-ttu-id="1f142-130">URL</span><span class="sxs-lookup"><span data-stu-id="1f142-130">URL</span></span>                                | <span data-ttu-id="1f142-131">Nebūtino saito URL.</span><span class="sxs-lookup"><span data-stu-id="1f142-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="1f142-132">Įspėjimo modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="1f142-132">Add an alert module to a page</span></span> 

<span data-ttu-id="1f142-133">Norėdami į puslapį įtraukti įspėjimo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1f142-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1f142-134">Sukurkite puslapio šabloną, pavadintą **įspėjimo šablonas**.</span><span class="sxs-lookup"><span data-stu-id="1f142-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="1f142-135">Numatytojo puslapio vietoje **Pagrindinis** įtraukite įspėjimo modulį.</span><span class="sxs-lookup"><span data-stu-id="1f142-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="1f142-136">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="1f142-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="1f142-137">Naudodami ką tik sukurtą įspėjimo šabloną, sukurkite puslapį, pavadintą **įspėjimo puslapis**.</span><span class="sxs-lookup"><span data-stu-id="1f142-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="1f142-138">Naujo puslapio vietoje **Pagrindinis** įtraukite įspėjimo modulį.</span><span class="sxs-lookup"><span data-stu-id="1f142-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="1f142-139">Įspėjimo modulio parametruose įveskite įspėjimo tekstą.</span><span class="sxs-lookup"><span data-stu-id="1f142-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="1f142-140">Jei norite įspėjimo modulį tinkinti daugiau, galite redaguoti kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="1f142-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="1f142-141">Puslapį įrašykite ir peržiūrėkite.</span><span class="sxs-lookup"><span data-stu-id="1f142-141">Save and preview the page.</span></span> <span data-ttu-id="1f142-142">Puslapio viršuje turėtumėte matyti įspėjimą su jūsų įtrauktu tekstu.</span><span class="sxs-lookup"><span data-stu-id="1f142-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="1f142-143">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="1f142-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="1f142-144">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1f142-144">Additional resources</span></span>

[<span data-ttu-id="1f142-145">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="1f142-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1f142-146">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="1f142-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="1f142-147">Raiškiojo turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="1f142-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="1f142-148">Turinio išdėstymo modulis</span><span class="sxs-lookup"><span data-stu-id="1f142-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="1f142-149">Ypatybių modulis</span><span class="sxs-lookup"><span data-stu-id="1f142-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="1f142-150">Pagrindinės reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="1f142-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="1f142-151">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="1f142-151">Video player module</span></span>](add-video-player.md)
