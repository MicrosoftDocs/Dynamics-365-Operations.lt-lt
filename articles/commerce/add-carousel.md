---
title: Karuselės modulis
description: Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785242"
---
# <a name="carousel-module"></a><span data-ttu-id="e9570-103">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="e9570-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e9570-104">Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="e9570-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e9570-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="e9570-105">Overview</span></span>

<span data-ttu-id="e9570-106">Naudojant karuselės modulį kelios reklaminės prekės įdedamos į karuselę, kurią klientai gali naršyti.</span><span class="sxs-lookup"><span data-stu-id="e9570-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="e9570-107">Tai yra specialus konteinerio modulis, kuriame yra kitų modulių.</span><span class="sxs-lookup"><span data-stu-id="e9570-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="e9570-108">Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.</span><span class="sxs-lookup"><span data-stu-id="e9570-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="e9570-109">Į karuselės modulį galite įtraukti pagrindinės reklaminės juostos ir ypatybių modulius.</span><span class="sxs-lookup"><span data-stu-id="e9570-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="e9570-110">Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.</span><span class="sxs-lookup"><span data-stu-id="e9570-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="e9570-111">Karuselės modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="e9570-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="e9570-112">Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e9570-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="e9570-113">Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e9570-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="e9570-114">Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.</span><span class="sxs-lookup"><span data-stu-id="e9570-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="e9570-115">Karuselės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="e9570-115">Carousel module properties</span></span>

| <span data-ttu-id="e9570-116">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="e9570-116">Property name</span></span>             | <span data-ttu-id="e9570-117">Vertė</span><span class="sxs-lookup"><span data-stu-id="e9570-117">Value</span></span>                                | <span data-ttu-id="e9570-118">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="e9570-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="e9570-119">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="e9570-119">Autoplay</span></span>                  | <span data-ttu-id="e9570-120">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="e9570-120">**True** or **False**</span></span>                | <span data-ttu-id="e9570-121">Jei reikšmė nustatoma kaip **Teisinga**, nuo vienos prekės prie kitos karuselėje pereinama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="e9570-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="e9570-122">Jei reikšmė nustatoma kaip **Klaidinga**, prie kitos prekės nepereinama, nebent klientas nuo vienos prekės prie kitos pereina klaviatūra ar pele.</span><span class="sxs-lookup"><span data-stu-id="e9570-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="e9570-123">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="e9570-123">Slide transition interval</span></span> | <span data-ttu-id="e9570-124">Reikšmė sekundėmis</span><span class="sxs-lookup"><span data-stu-id="e9570-124">A value in seconds</span></span>                   | <span data-ttu-id="e9570-125">Perėjimo nuo vienos prekės prie kitos intervalas.</span><span class="sxs-lookup"><span data-stu-id="e9570-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="e9570-126">Perėjimo animacija</span><span class="sxs-lookup"><span data-stu-id="e9570-126">Transition animation</span></span>      | <span data-ttu-id="e9570-127">**Slinkimas** arba **Išnykimas**</span><span class="sxs-lookup"><span data-stu-id="e9570-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="e9570-128">Perėjimo efektas.</span><span class="sxs-lookup"><span data-stu-id="e9570-128">The transition effect.</span></span> |
| <span data-ttu-id="e9570-129">Plotis</span><span class="sxs-lookup"><span data-stu-id="e9570-129">Width</span></span>                     | <span data-ttu-id="e9570-130">**Priderinti prie konteinerio** arba **Užpildyti ekraną**</span><span class="sxs-lookup"><span data-stu-id="e9570-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="e9570-131">Jei reikšmė nustatoma kaip **Priderinti prie konteinerio**, karuselės prekių plotį riboja karuselė.</span><span class="sxs-lookup"><span data-stu-id="e9570-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="e9570-132">Jei reikšmė nustatoma kaip **Užpildyti ekraną**, prekių pločio karuselė neriboja ir jas galima vaizduoti viso ekrano režimu.</span><span class="sxs-lookup"><span data-stu-id="e9570-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="e9570-133">Keisdami reikšmę, galite pasiekti norimą išdėstymą.</span><span class="sxs-lookup"><span data-stu-id="e9570-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="e9570-134">Karuselės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="e9570-134">Add a carousel module to a page</span></span>

<span data-ttu-id="e9570-135">Norėdami į naują puslapį įtraukti karuselės modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e9570-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e9570-136">Sukurkite puslapio šabloną, pavadintą **karuselės šablonas**.</span><span class="sxs-lookup"><span data-stu-id="e9570-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="e9570-137">Numatytojo puslapio vietoje **Pagrindinis** įtraukite karuselės modulį.</span><span class="sxs-lookup"><span data-stu-id="e9570-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="e9570-138">Į karuselės modulį įtraukite pagrindinės reklaminės juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="e9570-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="e9570-139">Į karuselės modulį įtraukite ypatybių modulį.</span><span class="sxs-lookup"><span data-stu-id="e9570-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="e9570-140">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="e9570-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="e9570-141">Naudodami ką tik sukurtą karuselės šabloną, sukurkite puslapį, pavadintą **karuselės puslapis**.</span><span class="sxs-lookup"><span data-stu-id="e9570-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="e9570-142">Naujo puslapio vietoje **Pagrindinis** įtraukite karuselės modulį.</span><span class="sxs-lookup"><span data-stu-id="e9570-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="e9570-143">Karuselės modulio ypatybę **Plotis** nustatykite kaip **Užpildyti ekraną**.</span><span class="sxs-lookup"><span data-stu-id="e9570-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="e9570-144">Ypatybę **Perėjimo animacija** nustatykite kaip **Slinkimas**.</span><span class="sxs-lookup"><span data-stu-id="e9570-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="e9570-145">Į karuselės modulį įtraukite pagrindinės reklaminės juostos modulį.</span><span class="sxs-lookup"><span data-stu-id="e9570-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="e9570-146">Pagrindinės reklaminės juostos modulyje įtraukite vaizdą ir antraštę, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e9570-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="e9570-147">Į karuselės modulį įtraukite ypatybių modulį.</span><span class="sxs-lookup"><span data-stu-id="e9570-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="e9570-148">Ypatybių modulyje įtraukite vaizdą, antraštę ir teksto pastraipą.</span><span class="sxs-lookup"><span data-stu-id="e9570-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="e9570-149">Puslapį įrašykite ir peržiūrėkite.</span><span class="sxs-lookup"><span data-stu-id="e9570-149">Save and preview the page.</span></span> <span data-ttu-id="e9570-150">Puslapyje turėtų būti rodoma karuselė su dviem moduliais (pagrindinės reklaminės juostos moduliu ir ypatybių moduliu).</span><span class="sxs-lookup"><span data-stu-id="e9570-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="e9570-151">Norėdami pasiekti norimą rezultatą, galite keisti papildomas karuselės, pagrindinės reklaminės juostos ir ypatybių modulių ypatybes.</span><span class="sxs-lookup"><span data-stu-id="e9570-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="e9570-152">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="e9570-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9570-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="e9570-153">Additional resources</span></span>

[<span data-ttu-id="e9570-154">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="e9570-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e9570-155">Įspėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="e9570-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="e9570-156">Raiškiojo turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="e9570-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e9570-157">Turinio išdėstymo modulis</span><span class="sxs-lookup"><span data-stu-id="e9570-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e9570-158">Ypatybių modulis</span><span class="sxs-lookup"><span data-stu-id="e9570-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="e9570-159">Pagrindinės reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="e9570-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="e9570-160">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="e9570-160">Video player module</span></span>](add-video-player.md)
