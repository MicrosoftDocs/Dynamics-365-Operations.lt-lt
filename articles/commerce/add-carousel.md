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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f09f3f98d174f965a75e27ee6a5c2ed8599042fc
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816991"
---
# <a name="carousel-module"></a><span data-ttu-id="9bba4-103">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="9bba4-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9bba4-104">Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="9bba4-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9bba4-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="9bba4-105">Overview</span></span>

<span data-ttu-id="9bba4-106">Naudojant karuselės modulį kelios reklaminės prekės (įskaitant išraiškingus veiksmus) įdedamos į rotacinę karuselės reklaminę juostą, kurią klientai gali naršyti.</span><span class="sxs-lookup"><span data-stu-id="9bba4-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="9bba4-107">Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.</span><span class="sxs-lookup"><span data-stu-id="9bba4-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="9bba4-108">Į karuselės modulį galite įtraukti turinio bloko modulius.</span><span class="sxs-lookup"><span data-stu-id="9bba4-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="9bba4-109">Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.</span><span class="sxs-lookup"><span data-stu-id="9bba4-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="9bba4-110">Karuselės modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="9bba4-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="9bba4-111">Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9bba4-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="9bba4-112">Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9bba4-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="9bba4-113">Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.</span><span class="sxs-lookup"><span data-stu-id="9bba4-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="9bba4-114">Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio karuselės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="9bba4-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="9bba4-115">Šiame karuselės modulyje yra keli turinio blokų elementai.</span><span class="sxs-lookup"><span data-stu-id="9bba4-115">This carousel module contains multiple content block items.</span></span>

![Karuselės modulio pavyzdys](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="9bba4-117">Karuselės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="9bba4-117">Carousel module properties</span></span>

| <span data-ttu-id="9bba4-118">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="9bba4-118">Property name</span></span>             | <span data-ttu-id="9bba4-119">Vertė</span><span class="sxs-lookup"><span data-stu-id="9bba4-119">Value</span></span>                 | <span data-ttu-id="9bba4-120">aprašymas</span><span class="sxs-lookup"><span data-stu-id="9bba4-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="9bba4-121">Automatinis paleidimas</span><span class="sxs-lookup"><span data-stu-id="9bba4-121">Autoplay</span></span>                  | <span data-ttu-id="9bba4-122">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="9bba4-122">**True** or **False**</span></span> | <span data-ttu-id="9bba4-123">Jei reikšmė nustatoma kaip **Teisinga**, nuo vienos prekės prie kitos karuselėje pereinama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="9bba4-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="9bba4-124">Jei reikšmė nustatoma kaip **Klaidinga**, prie kitos prekės nepereinama, nebent klientas nuo vienos prekės prie kitos pereina klaviatūra ar pele.</span><span class="sxs-lookup"><span data-stu-id="9bba4-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="9bba4-125">Skaidrių perėjimo intervalas</span><span class="sxs-lookup"><span data-stu-id="9bba4-125">Slide transition interval</span></span> | <span data-ttu-id="9bba4-126">Reikšmė sekundėmis</span><span class="sxs-lookup"><span data-stu-id="9bba4-126">A value in seconds</span></span>    | <span data-ttu-id="9bba4-127">Perėjimo nuo vienos prekės prie kitos intervalas.</span><span class="sxs-lookup"><span data-stu-id="9bba4-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="9bba4-128">Perėjimo tipas</span><span class="sxs-lookup"><span data-stu-id="9bba4-128">Transition type</span></span>           | <span data-ttu-id="9bba4-129">**Slinkimas** arba **Išnykimas**</span><span class="sxs-lookup"><span data-stu-id="9bba4-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="9bba4-130">Perėjimo poveikis tarp prekių.</span><span class="sxs-lookup"><span data-stu-id="9bba4-130">The transition effect between items.</span></span> |
| <span data-ttu-id="9bba4-131">Slėpti karuselės sukimo priemonę</span><span class="sxs-lookup"><span data-stu-id="9bba4-131">Hide carousel flipper</span></span>     | <span data-ttu-id="9bba4-132">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="9bba4-132">**True** or **False**</span></span> | <span data-ttu-id="9bba4-133">Jei reikšmė nustatyta kaip **Teisinga**, karuselės pelekas ir sekos indikatorius yra paslėpti.</span><span class="sxs-lookup"><span data-stu-id="9bba4-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="9bba4-134">Karuselės atmetimo leidimas</span><span class="sxs-lookup"><span data-stu-id="9bba4-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="9bba4-135">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="9bba4-135">**True** or **False**</span></span> | <span data-ttu-id="9bba4-136">Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti karuselę.</span><span class="sxs-lookup"><span data-stu-id="9bba4-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="9bba4-137">Karuselės modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="9bba4-137">Add a carousel module to a page</span></span>

<span data-ttu-id="9bba4-138">Norėdami į naują puslapį įtraukti karuselės modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9bba4-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9bba4-139">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="9bba4-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="9bba4-140">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Karuselės šablonas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="9bba4-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="9bba4-141">Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis modulis**.</span><span class="sxs-lookup"><span data-stu-id="9bba4-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="9bba4-142">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="9bba4-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="9bba4-143">Naudodami ką tik sukurtą karuselės šabloną, sukurkite puslapį, pavadintą **Karuselės puslapis**.</span><span class="sxs-lookup"><span data-stu-id="9bba4-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="9bba4-144">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="9bba4-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="9bba4-145">Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti ekraną**.</span><span class="sxs-lookup"><span data-stu-id="9bba4-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="9bba4-146">Dalyje **Puslapio kontūras** įtraukite karuselės modulį į konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="9bba4-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="9bba4-147">Į karuselės modulį įtraukite turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="9bba4-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="9bba4-148">Nustatykite turinio bloko modulio ypatybes pateikdami **Antraštė**, **Saitas**, **Išdėstymas** ir kitas ypatybes.</span><span class="sxs-lookup"><span data-stu-id="9bba4-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="9bba4-149">Įtraukite ir konfigūruokite kitą turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="9bba4-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="9bba4-150">Pagal pageidavimą, nustatykite kitas karuselės modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="9bba4-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="9bba4-151">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="9bba4-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="9bba4-152">Puslapyje turėtų būti rodoma karuselė su dviem moduliais (pagrindinės reklaminės juostos moduliu ir ypatybių moduliu).</span><span class="sxs-lookup"><span data-stu-id="9bba4-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="9bba4-153">Norėdami pasiekti norimą rezultatą, galite keisti papildomas karuselės, pagrindinės reklaminės juostos ir ypatybių modulių ypatybes.</span><span class="sxs-lookup"><span data-stu-id="9bba4-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="9bba4-154">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="9bba4-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9bba4-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9bba4-155">Additional resources</span></span>

[<span data-ttu-id="9bba4-156">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="9bba4-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9bba4-157">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="9bba4-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="9bba4-158">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="9bba4-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="9bba4-159">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="9bba4-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="9bba4-160">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="9bba4-160">Video player module</span></span>](add-video-player.md)
