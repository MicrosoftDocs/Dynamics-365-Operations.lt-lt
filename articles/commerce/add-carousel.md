---
title: Karuselės modulis
description: Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: 5333ecd7a1fe4f60684fa5f5bb3ac9f98efde6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206516"
---
# <a name="carousel-module"></a><span data-ttu-id="f243e-103">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="f243e-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f243e-104">Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="f243e-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f243e-105">Naudojant karuselės modulį kelios reklaminės prekės (įskaitant išraiškingus veiksmus) įdedamos į rotacinę karuselės reklaminę juostą, kurią klientai gali naršyti.</span><span class="sxs-lookup"><span data-stu-id="f243e-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="f243e-106">Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.</span><span class="sxs-lookup"><span data-stu-id="f243e-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="f243e-107">Į karuselės modulį galite įtraukti turinio bloko modulius.</span><span class="sxs-lookup"><span data-stu-id="f243e-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="f243e-108">Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.</span><span class="sxs-lookup"><span data-stu-id="f243e-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="f243e-109">Karuselės modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="f243e-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="f243e-110">Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f243e-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="f243e-111">Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f243e-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="f243e-112">Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.</span><span class="sxs-lookup"><span data-stu-id="f243e-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="f243e-113">Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio karuselės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="f243e-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="f243e-114">Šiame karuselės modulyje yra keli turinio blokų elementai.</span><span class="sxs-lookup"><span data-stu-id="f243e-114">This carousel module contains multiple content block items.</span></span>

![Karuselės modulio pavyzdys](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="f243e-116">Karuselės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="f243e-116">Carousel module properties</span></span>

| <span data-ttu-id="f243e-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="f243e-117">Property name</span></span>             | <span data-ttu-id="f243e-118">Vertė</span><span class="sxs-lookup"><span data-stu-id="f243e-118">Value</span></span>                 | <span data-ttu-id="f243e-119">aprašymas</span><span class="sxs-lookup"><span data-stu-id="f243e-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f243e-120">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="f243e-120">Autoplay</span></span>                  | <span data-ttu-id="f243e-121">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="f243e-121">**True** or **False**</span></span> | <span data-ttu-id="f243e-122">Jei reikšmė nustatoma kaip **Teisinga**, nuo vienos prekės prie kitos karuselėje pereinama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="f243e-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="f243e-123">Jei reikšmė nustatoma kaip **Klaidinga**, prie kitos prekės nepereinama, nebent klientas nuo vienos prekės prie kitos pereina klaviatūra ar pele.</span><span class="sxs-lookup"><span data-stu-id="f243e-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="f243e-124">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="f243e-124">Slide transition interval</span></span> | <span data-ttu-id="f243e-125">Reikšmė sekundėmis</span><span class="sxs-lookup"><span data-stu-id="f243e-125">A value in seconds</span></span>    | <span data-ttu-id="f243e-126">Perėjimo nuo vienos prekės prie kitos intervalas.</span><span class="sxs-lookup"><span data-stu-id="f243e-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="f243e-127">Perėjimo tipas</span><span class="sxs-lookup"><span data-stu-id="f243e-127">Transition type</span></span>           | <span data-ttu-id="f243e-128">**Slinkimas** arba **Išnykimas**</span><span class="sxs-lookup"><span data-stu-id="f243e-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="f243e-129">Perėjimo poveikis tarp prekių.</span><span class="sxs-lookup"><span data-stu-id="f243e-129">The transition effect between items.</span></span> |
| <span data-ttu-id="f243e-130">Slėpti karuselės sukimo priemonę</span><span class="sxs-lookup"><span data-stu-id="f243e-130">Hide carousel flipper</span></span>     | <span data-ttu-id="f243e-131">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="f243e-131">**True** or **False**</span></span> | <span data-ttu-id="f243e-132">Jei reikšmė nustatyta kaip **Teisinga**, karuselės pelekas ir sekos indikatorius yra paslėpti.</span><span class="sxs-lookup"><span data-stu-id="f243e-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="f243e-133">Karuselės atmetimo leidimas</span><span class="sxs-lookup"><span data-stu-id="f243e-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="f243e-134">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="f243e-134">**True** or **False**</span></span> | <span data-ttu-id="f243e-135">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti karuselę.</span><span class="sxs-lookup"><span data-stu-id="f243e-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="f243e-136">Karuselės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="f243e-136">Add a carousel module to a page</span></span>

<span data-ttu-id="f243e-137">Norėdami į naują puslapį įtraukti karuselės modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f243e-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f243e-138">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="f243e-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f243e-139">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Karuselės šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f243e-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f243e-140">Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis modulis**.</span><span class="sxs-lookup"><span data-stu-id="f243e-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="f243e-141">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="f243e-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="f243e-142">Naudodami ką tik sukurtą karuselės šabloną, sukurkite puslapį, pavadintą **Karuselės puslapis**.</span><span class="sxs-lookup"><span data-stu-id="f243e-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="f243e-143">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="f243e-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="f243e-144">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti ekraną**.</span><span class="sxs-lookup"><span data-stu-id="f243e-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="f243e-145">Dalyje **Puslapio kontūras** įtraukite karuselės modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="f243e-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="f243e-146">Į karuselės modulį įtraukite turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="f243e-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="f243e-147">Nustatykite turinio bloko modulio ypatybes pateikdami **Antraštė**, **Saitas**, **Išdėstymas** ir kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="f243e-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="f243e-148">Įtraukite ir konfigūruokite kitą turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="f243e-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="f243e-149">Pagal pageidavimą, nustatykite kitas karuselės modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="f243e-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="f243e-150">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="f243e-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f243e-151">Puslapyje turėtų būti rodoma karuselė su dviem moduliais (pagrindinės reklaminės juostos moduliu ir ypatybių moduliu).</span><span class="sxs-lookup"><span data-stu-id="f243e-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="f243e-152">Norėdami pasiekti norimą rezultatą, galite keisti papildomas karuselės, pagrindinės reklaminės juostos ir ypatybių modulių ypatybes.</span><span class="sxs-lookup"><span data-stu-id="f243e-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="f243e-153">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="f243e-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f243e-154">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f243e-154">Additional resources</span></span>

[<span data-ttu-id="f243e-155">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="f243e-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f243e-156">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="f243e-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f243e-157">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="f243e-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f243e-158">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="f243e-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f243e-159">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="f243e-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]