---
title: Karuselės modulis
description: Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025786"
---
# <a name="carousel-module"></a><span data-ttu-id="3ed04-103">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="3ed04-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3ed04-104">Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="3ed04-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3ed04-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="3ed04-105">Overview</span></span>

<span data-ttu-id="3ed04-106">Naudojant karuselės modulį kelios reklaminės prekės (įskaitant išraiškingus veiksmus) įdedamos į rotacinę karuselės reklaminę juostą, kurią klientai gali naršyti.</span><span class="sxs-lookup"><span data-stu-id="3ed04-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="3ed04-107">Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.</span><span class="sxs-lookup"><span data-stu-id="3ed04-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="3ed04-108">Į karuselės modulį galite įtraukti turinio bloko modulius.</span><span class="sxs-lookup"><span data-stu-id="3ed04-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="3ed04-109">Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.</span><span class="sxs-lookup"><span data-stu-id="3ed04-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="3ed04-110">Karuselės modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="3ed04-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="3ed04-111">Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3ed04-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="3ed04-112">Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3ed04-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="3ed04-113">Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.</span><span class="sxs-lookup"><span data-stu-id="3ed04-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="3ed04-114">Karuselės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="3ed04-114">Carousel module properties</span></span>

| <span data-ttu-id="3ed04-115">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3ed04-115">Property name</span></span>             | <span data-ttu-id="3ed04-116">Vertė</span><span class="sxs-lookup"><span data-stu-id="3ed04-116">Value</span></span>                 | <span data-ttu-id="3ed04-117">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="3ed04-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="3ed04-118">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="3ed04-118">Autoplay</span></span>                  | <span data-ttu-id="3ed04-119">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="3ed04-119">**True** or **False**</span></span> | <span data-ttu-id="3ed04-120">Jei reikšmė nustatoma kaip **Teisinga**, nuo vienos prekės prie kitos karuselėje pereinama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="3ed04-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="3ed04-121">Jei reikšmė nustatoma kaip **Klaidinga**, prie kitos prekės nepereinama, nebent klientas nuo vienos prekės prie kitos pereina klaviatūra ar pele.</span><span class="sxs-lookup"><span data-stu-id="3ed04-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="3ed04-122">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="3ed04-122">Slide transition interval</span></span> | <span data-ttu-id="3ed04-123">Reikšmė sekundėmis</span><span class="sxs-lookup"><span data-stu-id="3ed04-123">A value in seconds</span></span>    | <span data-ttu-id="3ed04-124">Perėjimo nuo vienos prekės prie kitos intervalas.</span><span class="sxs-lookup"><span data-stu-id="3ed04-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="3ed04-125">Perėjimo tipas</span><span class="sxs-lookup"><span data-stu-id="3ed04-125">Transition type</span></span>           | <span data-ttu-id="3ed04-126">**Slinkimas** arba **Išnykimas**</span><span class="sxs-lookup"><span data-stu-id="3ed04-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="3ed04-127">Perėjimo poveikis tarp prekių.</span><span class="sxs-lookup"><span data-stu-id="3ed04-127">The transition effect between items.</span></span> |
| <span data-ttu-id="3ed04-128">Slėpti karuselės sukimo priemonę</span><span class="sxs-lookup"><span data-stu-id="3ed04-128">Hide carousel flipper</span></span>     | <span data-ttu-id="3ed04-129">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="3ed04-129">**True** or **False**</span></span> | <span data-ttu-id="3ed04-130">Jei reikšmė nustatyta kaip **Teisinga**, karuselės pelekas ir sekos indikatorius yra paslėpti.</span><span class="sxs-lookup"><span data-stu-id="3ed04-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="3ed04-131">Karuselės atmetimo leidimas</span><span class="sxs-lookup"><span data-stu-id="3ed04-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="3ed04-132">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="3ed04-132">**True** or **False**</span></span> | <span data-ttu-id="3ed04-133">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti karuselę.</span><span class="sxs-lookup"><span data-stu-id="3ed04-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="3ed04-134">Karuselės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="3ed04-134">Add a carousel module to a page</span></span>

<span data-ttu-id="3ed04-135">Norėdami į naują puslapį įtraukti karuselės modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3ed04-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3ed04-136">Sukurkite puslapio šabloną, pavadintą **karuselės šablonas**.</span><span class="sxs-lookup"><span data-stu-id="3ed04-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="3ed04-137">Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis modulis**.</span><span class="sxs-lookup"><span data-stu-id="3ed04-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="3ed04-138">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="3ed04-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="3ed04-139">Naudodami ką tik sukurtą karuselės šabloną, sukurkite puslapį, pavadintą **karuselės puslapis**.</span><span class="sxs-lookup"><span data-stu-id="3ed04-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="3ed04-140">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="3ed04-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="3ed04-141">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti ekraną**.</span><span class="sxs-lookup"><span data-stu-id="3ed04-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="3ed04-142">Dalyje **Puslapio kontūras** įtraukite karuselės modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="3ed04-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="3ed04-143">Į karuselės modulį įtraukite turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="3ed04-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="3ed04-144">Nustatykite turinio bloko modulio ypatybes pateikdami **Antraštė**, **Saitas**, **Išdėstymas** ir kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="3ed04-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="3ed04-145">Įtraukite ir konfigūruokite kitą turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="3ed04-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="3ed04-146">Pagal pageidavimą, nustatykite kitas karuselės modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="3ed04-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="3ed04-147">Puslapį įrašykite ir peržiūrėkite.</span><span class="sxs-lookup"><span data-stu-id="3ed04-147">Save and preview the page.</span></span> <span data-ttu-id="3ed04-148">Puslapyje turėtų būti rodoma karuselė su dviem moduliais (pagrindinės reklaminės juostos moduliu ir ypatybių moduliu).</span><span class="sxs-lookup"><span data-stu-id="3ed04-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="3ed04-149">Norėdami pasiekti norimą rezultatą, galite keisti papildomas karuselės, pagrindinės reklaminės juostos ir ypatybių modulių ypatybes.</span><span class="sxs-lookup"><span data-stu-id="3ed04-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="3ed04-150">Baikite puslapio redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="3ed04-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ed04-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3ed04-151">Additional resources</span></span>

[<span data-ttu-id="3ed04-152">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="3ed04-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3ed04-153">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="3ed04-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="3ed04-154">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="3ed04-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="3ed04-155">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="3ed04-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="3ed04-156">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="3ed04-156">Video player module</span></span>](add-video-player.md)
