---
title: Karuselės modulis
description: Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269733"
---
# <a name="carousel-module"></a><span data-ttu-id="c69b5-103">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="c69b5-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c69b5-104">Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="c69b5-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c69b5-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="c69b5-105">Overview</span></span>

<span data-ttu-id="c69b5-106">Naudojant karuselės modulį kelios reklaminės prekės (įskaitant išraiškingus veiksmus) įdedamos į rotacinę karuselės reklaminę juostą, kurią klientai gali naršyti.</span><span class="sxs-lookup"><span data-stu-id="c69b5-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="c69b5-107">Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.</span><span class="sxs-lookup"><span data-stu-id="c69b5-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="c69b5-108">Į karuselės modulį galite įtraukti turinio bloko modulius.</span><span class="sxs-lookup"><span data-stu-id="c69b5-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="c69b5-109">Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.</span><span class="sxs-lookup"><span data-stu-id="c69b5-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="c69b5-110">Karuselės modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="c69b5-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="c69b5-111">Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c69b5-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="c69b5-112">Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c69b5-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="c69b5-113">Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.</span><span class="sxs-lookup"><span data-stu-id="c69b5-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="c69b5-114">Karuselės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="c69b5-114">Carousel module properties</span></span>

| <span data-ttu-id="c69b5-115">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="c69b5-115">Property name</span></span>             | <span data-ttu-id="c69b5-116">Vertė</span><span class="sxs-lookup"><span data-stu-id="c69b5-116">Value</span></span>                 | <span data-ttu-id="c69b5-117">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="c69b5-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c69b5-118">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="c69b5-118">Autoplay</span></span>                  | <span data-ttu-id="c69b5-119">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="c69b5-119">**True** or **False**</span></span> | <span data-ttu-id="c69b5-120">Jei reikšmė nustatoma kaip **Teisinga**, nuo vienos prekės prie kitos karuselėje pereinama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="c69b5-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="c69b5-121">Jei reikšmė nustatoma kaip **Klaidinga**, prie kitos prekės nepereinama, nebent klientas nuo vienos prekės prie kitos pereina klaviatūra ar pele.</span><span class="sxs-lookup"><span data-stu-id="c69b5-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="c69b5-122">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="c69b5-122">Slide transition interval</span></span> | <span data-ttu-id="c69b5-123">Reikšmė sekundėmis</span><span class="sxs-lookup"><span data-stu-id="c69b5-123">A value in seconds</span></span>    | <span data-ttu-id="c69b5-124">Perėjimo nuo vienos prekės prie kitos intervalas.</span><span class="sxs-lookup"><span data-stu-id="c69b5-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="c69b5-125">Perėjimo tipas</span><span class="sxs-lookup"><span data-stu-id="c69b5-125">Transition type</span></span>           | <span data-ttu-id="c69b5-126">**Slinkimas** arba **Išnykimas**</span><span class="sxs-lookup"><span data-stu-id="c69b5-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="c69b5-127">Perėjimo poveikis tarp prekių.</span><span class="sxs-lookup"><span data-stu-id="c69b5-127">The transition effect between items.</span></span> |
| <span data-ttu-id="c69b5-128">Slėpti karuselės sukimo priemonę</span><span class="sxs-lookup"><span data-stu-id="c69b5-128">Hide carousel flipper</span></span>     | <span data-ttu-id="c69b5-129">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="c69b5-129">**True** or **False**</span></span> | <span data-ttu-id="c69b5-130">Jei reikšmė nustatyta kaip **Teisinga**, karuselės pelekas ir sekos indikatorius yra paslėpti.</span><span class="sxs-lookup"><span data-stu-id="c69b5-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="c69b5-131">Karuselės atmetimo leidimas</span><span class="sxs-lookup"><span data-stu-id="c69b5-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="c69b5-132">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="c69b5-132">**True** or **False**</span></span> | <span data-ttu-id="c69b5-133">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti karuselę.</span><span class="sxs-lookup"><span data-stu-id="c69b5-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="c69b5-134">Karuselės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="c69b5-134">Add a carousel module to a page</span></span>

<span data-ttu-id="c69b5-135">Norėdami į naują puslapį įtraukti karuselės modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c69b5-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c69b5-136">Pasirinkite **Naujas**, kad sukurtumėte puslapio šabloną.</span><span class="sxs-lookup"><span data-stu-id="c69b5-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="c69b5-137">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Karuselės šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c69b5-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c69b5-138">Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis modulis**.</span><span class="sxs-lookup"><span data-stu-id="c69b5-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="c69b5-139">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="c69b5-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="c69b5-140">Naudodami ką tik sukurtą karuselės šabloną, sukurkite puslapį, pavadintą **Karuselės puslapis**.</span><span class="sxs-lookup"><span data-stu-id="c69b5-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="c69b5-141">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="c69b5-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="c69b5-142">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti ekraną**.</span><span class="sxs-lookup"><span data-stu-id="c69b5-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="c69b5-143">Dalyje **Puslapio kontūras** įtraukite karuselės modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="c69b5-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="c69b5-144">Į karuselės modulį įtraukite turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="c69b5-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="c69b5-145">Nustatykite turinio bloko modulio ypatybes pateikdami **Antraštė**, **Saitas**, **Išdėstymas** ir kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="c69b5-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="c69b5-146">Įtraukite ir konfigūruokite kitą turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="c69b5-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="c69b5-147">Pagal pageidavimą, nustatykite kitas karuselės modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="c69b5-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="c69b5-148">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="c69b5-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="c69b5-149">Puslapyje turėtų būti rodoma karuselė su dviem moduliais (pagrindinės reklaminės juostos moduliu ir ypatybių moduliu).</span><span class="sxs-lookup"><span data-stu-id="c69b5-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="c69b5-150">Norėdami pasiekti norimą rezultatą, galite keisti papildomas karuselės, pagrindinės reklaminės juostos ir ypatybių modulių ypatybes.</span><span class="sxs-lookup"><span data-stu-id="c69b5-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="c69b5-151">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="c69b5-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c69b5-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c69b5-152">Additional resources</span></span>

[<span data-ttu-id="c69b5-153">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="c69b5-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c69b5-154">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="c69b5-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="c69b5-155">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="c69b5-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="c69b5-156">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="c69b5-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="c69b5-157">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="c69b5-157">Video player module</span></span>](add-video-player.md)
