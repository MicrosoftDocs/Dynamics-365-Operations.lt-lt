---
title: Teksto bloko modulis
description: Šioje temoje aprašomi teksto bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7dbeb8785641960cc2680335436aea10775759d3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797772"
---
# <a name="text-block-module"></a><span data-ttu-id="68926-103">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="68926-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="68926-104">Šioje temoje aprašomi teksto bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="68926-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="68926-105">Teksto bloko modulis yra modulis, kuris naudojamas teksto turiniui pridėti.</span><span class="sxs-lookup"><span data-stu-id="68926-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="68926-106">Šis turinys gali būti informacinis arba reklaminis.</span><span class="sxs-lookup"><span data-stu-id="68926-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="68926-107">Teksto bloko moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="68926-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="68926-108">Jie yra atskiri moduliai, nepriklausantys nuo puslapio konteksto ar kitų modulių.</span><span class="sxs-lookup"><span data-stu-id="68926-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="68926-109">Teksto bloko modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="68926-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="68926-110">Teksto bloko modulius galima naudoti toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="68926-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="68926-111">Norint produktų išsamios informacijos puslapyje parodyti produktų ypatybes.</span><span class="sxs-lookup"><span data-stu-id="68926-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="68926-112">Informaciniais tikslais bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="68926-112">For informational purposes on any page.</span></span> <span data-ttu-id="68926-113">Pavyzdžiui, juos naudojant galima paaiškinti lojalumo programų privalumus, aprašyti siuntimo ir grąžinimo strategijas, atsakyti į dažnai užduodamus klausimus arba pateikti turinio „apie mus“.</span><span class="sxs-lookup"><span data-stu-id="68926-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="68926-114">Norint produktų išsamios informacijos puslapyje įtraukti pasirinktinių pranešimų.</span><span class="sxs-lookup"><span data-stu-id="68926-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="68926-115">(Pavyzdžiui, „Didesni, nei 50 USD, užsakymai pristatomi nemokamai“).</span><span class="sxs-lookup"><span data-stu-id="68926-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="68926-116">Norint produktų išsamios informacijos puslapiuose, krepšelio puslapiuose, pirkimo užbaigimo puslapiuose ir kituose puslapiuose įtraukti informaciją apie atsakomybės atsisakymą ir kontaktinę informaciją (pavyzdžiui, „Siunčiant ir grąžinant prekes taikomos parduotuvės strategijos“).</span><span class="sxs-lookup"><span data-stu-id="68926-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="68926-117">Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio teksto bloko modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="68926-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Teksto bloko modulio pavyzdys](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="68926-119">Teksto bloko modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="68926-119">Text block module properties</span></span>

| <span data-ttu-id="68926-120">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="68926-120">Property name</span></span>     | <span data-ttu-id="68926-121">Vertė</span><span class="sxs-lookup"><span data-stu-id="68926-121">Value</span></span>                                            | <span data-ttu-id="68926-122">aprašymas</span><span class="sxs-lookup"><span data-stu-id="68926-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="68926-123">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="68926-123">Rich text</span></span>         | <span data-ttu-id="68926-124">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="68926-124">Rich text</span></span>                                        | <span data-ttu-id="68926-125">Pastraipos tekstas.</span><span class="sxs-lookup"><span data-stu-id="68926-125">Paragraph text.</span></span> <span data-ttu-id="68926-126">Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas.</span><span class="sxs-lookup"><span data-stu-id="68926-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="68926-127">Pasirinktinis klasės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="68926-127">Custom class name</span></span> | <span data-ttu-id="68926-128">Pakopinio stiliaus aprašų (CSS) klasės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="68926-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="68926-129">Pasirinktinės CSS klasės, kurią kūrėjas teikia formatuoti šį modulį, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="68926-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="68926-130">Klasės pavadinimas turi būti nurodytas temų pakete.</span><span class="sxs-lookup"><span data-stu-id="68926-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="68926-131">Šrifto dydis</span><span class="sxs-lookup"><span data-stu-id="68926-131">Font size</span></span>         | <span data-ttu-id="68926-132">**Mažas**, **Vidutinis**, **Didelis** arba **X dydžio**</span><span class="sxs-lookup"><span data-stu-id="68926-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="68926-133">Turinio šrifto dydis.</span><span class="sxs-lookup"><span data-stu-id="68926-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="68926-134">Teksto bloko modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="68926-134">Add a text block module to a page</span></span>

<span data-ttu-id="68926-135">Norėdami į naują puslapį įtraukti teksto bloko modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="68926-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="68926-136">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="68926-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="68926-137">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Turinio šablonas**.</span><span class="sxs-lookup"><span data-stu-id="68926-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="68926-138">Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="68926-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="68926-139">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68926-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="68926-140">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="68926-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="68926-141">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="68926-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="68926-142">Dialogo lange **Pasirinkti šabloną** pasirinkite **Turinio šablonas**.</span><span class="sxs-lookup"><span data-stu-id="68926-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="68926-143">Dalyje **Puslapio pavadinimas** įveskite **Turinio puslapis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68926-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="68926-144">Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="68926-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="68926-145">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68926-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="68926-146">Konteinerio modulio ypatybių srityje nustatykite ypatybę **Plotis** į **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="68926-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="68926-147">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="68926-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="68926-148">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Teksto blokas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="68926-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="68926-149">Teksto bloko modulio ypatybių srityje įtraukite tekstą į lauką **Raiškusis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="68926-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="68926-150">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="68926-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="68926-151">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="68926-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68926-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="68926-152">Additional resources</span></span>

[<span data-ttu-id="68926-153">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="68926-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="68926-154">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="68926-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="68926-155">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="68926-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="68926-156">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="68926-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="68926-157">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="68926-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]