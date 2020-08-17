---
title: Karuselės modulis
description: Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 10ff0cd566a1a8d89ccadce9571dafc5a592520b
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/27/2020
ms.locfileid: "3620991"
---
# <a name="carousel-module"></a><span data-ttu-id="212de-103">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="212de-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="212de-104">Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="212de-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="212de-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="212de-105">Overview</span></span>

<span data-ttu-id="212de-106">Naudojant karuselės modulį kelios reklaminės prekės (įskaitant išraiškingus veiksmus) įdedamos į rotacinę karuselės reklaminę juostą, kurią klientai gali naršyti.</span><span class="sxs-lookup"><span data-stu-id="212de-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="212de-107">Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.</span><span class="sxs-lookup"><span data-stu-id="212de-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="212de-108">Į karuselės modulį galite įtraukti turinio bloko modulius.</span><span class="sxs-lookup"><span data-stu-id="212de-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="212de-109">Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.</span><span class="sxs-lookup"><span data-stu-id="212de-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="212de-110">Karuselės modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="212de-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="212de-111">Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="212de-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="212de-112">Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="212de-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="212de-113">Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.</span><span class="sxs-lookup"><span data-stu-id="212de-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="212de-114">Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio karuselės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="212de-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="212de-115">Šiame karuselės modulyje yra keli turinio blokų elementai.</span><span class="sxs-lookup"><span data-stu-id="212de-115">This carousel module contains multiple content block items.</span></span>

![Karuselės modulio pavyzdys](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="212de-117">Karuselės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="212de-117">Carousel module properties</span></span>

| <span data-ttu-id="212de-118">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="212de-118">Property name</span></span>             | <span data-ttu-id="212de-119">Vertė</span><span class="sxs-lookup"><span data-stu-id="212de-119">Value</span></span>                 | <span data-ttu-id="212de-120">aprašymas</span><span class="sxs-lookup"><span data-stu-id="212de-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="212de-121">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="212de-121">Autoplay</span></span>                  | <span data-ttu-id="212de-122">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="212de-122">**True** or **False**</span></span> | <span data-ttu-id="212de-123">Jei reikšmė nustatoma kaip **Teisinga**, nuo vienos prekės prie kitos karuselėje pereinama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="212de-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="212de-124">Jei reikšmė nustatoma kaip **Klaidinga**, prie kitos prekės nepereinama, nebent klientas nuo vienos prekės prie kitos pereina klaviatūra ar pele.</span><span class="sxs-lookup"><span data-stu-id="212de-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="212de-125">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="212de-125">Slide transition interval</span></span> | <span data-ttu-id="212de-126">Reikšmė sekundėmis</span><span class="sxs-lookup"><span data-stu-id="212de-126">A value in seconds</span></span>    | <span data-ttu-id="212de-127">Perėjimo nuo vienos prekės prie kitos intervalas.</span><span class="sxs-lookup"><span data-stu-id="212de-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="212de-128">Perėjimo tipas</span><span class="sxs-lookup"><span data-stu-id="212de-128">Transition type</span></span>           | <span data-ttu-id="212de-129">**Slinkimas** arba **Išnykimas**</span><span class="sxs-lookup"><span data-stu-id="212de-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="212de-130">Perėjimo poveikis tarp prekių.</span><span class="sxs-lookup"><span data-stu-id="212de-130">The transition effect between items.</span></span> |
| <span data-ttu-id="212de-131">Slėpti karuselės sukimo priemonę</span><span class="sxs-lookup"><span data-stu-id="212de-131">Hide carousel flipper</span></span>     | <span data-ttu-id="212de-132">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="212de-132">**True** or **False**</span></span> | <span data-ttu-id="212de-133">Jei reikšmė nustatyta kaip **Teisinga**, karuselės pelekas ir sekos indikatorius yra paslėpti.</span><span class="sxs-lookup"><span data-stu-id="212de-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="212de-134">Karuselės atmetimo leidimas</span><span class="sxs-lookup"><span data-stu-id="212de-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="212de-135">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="212de-135">**True** or **False**</span></span> | <span data-ttu-id="212de-136">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti karuselę.</span><span class="sxs-lookup"><span data-stu-id="212de-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="212de-137">Karuselės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="212de-137">Add a carousel module to a page</span></span>

<span data-ttu-id="212de-138">Norėdami į naują puslapį įtraukti karuselės modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="212de-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="212de-139">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="212de-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="212de-140">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Karuselės šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="212de-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="212de-141">Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis modulis**.</span><span class="sxs-lookup"><span data-stu-id="212de-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="212de-142">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="212de-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="212de-143">Naudodami ką tik sukurtą karuselės šabloną, sukurkite puslapį, pavadintą **Karuselės puslapis**.</span><span class="sxs-lookup"><span data-stu-id="212de-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="212de-144">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="212de-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="212de-145">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti ekraną**.</span><span class="sxs-lookup"><span data-stu-id="212de-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="212de-146">Dalyje **Puslapio kontūras** įtraukite karuselės modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="212de-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="212de-147">Į karuselės modulį įtraukite turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="212de-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="212de-148">Nustatykite turinio bloko modulio ypatybes pateikdami **Antraštė**, **Saitas**, **Išdėstymas** ir kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="212de-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="212de-149">Įtraukite ir konfigūruokite kitą turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="212de-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="212de-150">Pagal pageidavimą, nustatykite kitas karuselės modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="212de-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="212de-151">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="212de-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="212de-152">Puslapyje turėtų būti rodoma karuselė su dviem moduliais (pagrindinės reklaminės juostos moduliu ir ypatybių moduliu).</span><span class="sxs-lookup"><span data-stu-id="212de-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="212de-153">Norėdami pasiekti norimą rezultatą, galite keisti papildomas karuselės, pagrindinės reklaminės juostos ir ypatybių modulių ypatybes.</span><span class="sxs-lookup"><span data-stu-id="212de-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="212de-154">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="212de-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="212de-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="212de-155">Additional resources</span></span>

[<span data-ttu-id="212de-156">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="212de-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="212de-157">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="212de-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="212de-158">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="212de-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="212de-159">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="212de-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="212de-160">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="212de-160">Video player module</span></span>](add-video-player.md)
