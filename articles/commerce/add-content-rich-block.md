---
title: Teksto bloko modulis
description: Šioje temoje aprašomi teksto bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817383"
---
# <a name="text-block-module"></a><span data-ttu-id="3e5cd-103">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="3e5cd-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3e5cd-104">Šioje temoje aprašomi teksto bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3e5cd-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="3e5cd-105">Overview</span></span>

<span data-ttu-id="3e5cd-106">Teksto bloko modulis yra modulis, kuris naudojamas teksto turiniui pridėti.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="3e5cd-107">Šis turinys gali būti informacinis arba reklaminis.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="3e5cd-108">Teksto bloko moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="3e5cd-109">Jie yra atskiri moduliai, nepriklausantys nuo puslapio konteksto ar kitų modulių.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="3e5cd-110">Teksto bloko modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="3e5cd-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="3e5cd-111">Teksto bloko modulius galima naudoti toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="3e5cd-112">Norint produktų išsamios informacijos puslapyje parodyti produktų ypatybes.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="3e5cd-113">Informaciniais tikslais bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-113">For informational purposes on any page.</span></span> <span data-ttu-id="3e5cd-114">Pavyzdžiui, juos naudojant galima paaiškinti lojalumo programų privalumus, aprašyti siuntimo ir grąžinimo strategijas, atsakyti į dažnai užduodamus klausimus arba pateikti turinio „apie mus“.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="3e5cd-115">Norint produktų išsamios informacijos puslapyje įtraukti pasirinktinių pranešimų.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="3e5cd-116">(Pavyzdžiui, „Didesni, nei 50 USD, užsakymai pristatomi nemokamai“).</span><span class="sxs-lookup"><span data-stu-id="3e5cd-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="3e5cd-117">Norint produktų išsamios informacijos puslapiuose, krepšelio puslapiuose, pirkimo užbaigimo puslapiuose ir kituose puslapiuose įtraukti informaciją apie atsakomės atsisakymą ir kontaktinę informaciją (pavyzdžiui, „Siunčiant ir grąžinant prekes taikomos parduotuvės strategijos“).</span><span class="sxs-lookup"><span data-stu-id="3e5cd-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="3e5cd-118">Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio teksto bloko modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Teksto bloko modulio pavyzdys](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="3e5cd-120">Teksto bloko modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="3e5cd-120">Text block module properties</span></span>

| <span data-ttu-id="3e5cd-121">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3e5cd-121">Property name</span></span>     | <span data-ttu-id="3e5cd-122">Vertė</span><span class="sxs-lookup"><span data-stu-id="3e5cd-122">Value</span></span>                                            | <span data-ttu-id="3e5cd-123">aprašymas</span><span class="sxs-lookup"><span data-stu-id="3e5cd-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="3e5cd-124">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="3e5cd-124">Rich text</span></span>         | <span data-ttu-id="3e5cd-125">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="3e5cd-125">Rich text</span></span>                                        | <span data-ttu-id="3e5cd-126">Pastraipos tekstas.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-126">Paragraph text.</span></span> <span data-ttu-id="3e5cd-127">Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="3e5cd-128">Pasirinktinis klasės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3e5cd-128">Custom class name</span></span> | <span data-ttu-id="3e5cd-129">Pakopinio stiliaus aprašų (CSS) klasės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="3e5cd-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="3e5cd-130">Pasirinktinės CSS klasės, kurią kūrėjas teikia formatuoti šį modulį, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="3e5cd-131">Klasės pavadinimas turi būti nurodytas temų pakete.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="3e5cd-132">Šrifto dydis</span><span class="sxs-lookup"><span data-stu-id="3e5cd-132">Font size</span></span>         | <span data-ttu-id="3e5cd-133">**Mažas**, **Vidutinis**, **Didelis** arba **X dydžio**</span><span class="sxs-lookup"><span data-stu-id="3e5cd-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="3e5cd-134">Turinio šrifto dydis.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="3e5cd-135">Teksto bloko modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="3e5cd-135">Add a text block module to a page</span></span>

<span data-ttu-id="3e5cd-136">Norėdami į naują puslapį įtraukti teksto bloko modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3e5cd-137">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="3e5cd-138">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Turinio šablonas**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="3e5cd-139">Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3e5cd-140">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3e5cd-141">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3e5cd-142">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="3e5cd-143">Dialogo lange **Pasirinkti šabloną** pasirinkite **Turinio šablonas**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="3e5cd-144">Dalyje **Puslapio pavadinimas** įveskite **Turinio puslapis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="3e5cd-145">Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3e5cd-146">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3e5cd-147">Konteinerio modulio ypatybių srityje nustatykite ypatybę **Plotis** į **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="3e5cd-148">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3e5cd-149">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Teksto blokas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="3e5cd-150">Teksto bloko modulio ypatybių srityje įtraukite tekstą į lauką **Raiškusis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="3e5cd-151">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="3e5cd-152">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="3e5cd-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e5cd-153">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3e5cd-153">Additional resources</span></span>

[<span data-ttu-id="3e5cd-154">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="3e5cd-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3e5cd-155">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="3e5cd-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="3e5cd-156">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="3e5cd-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="3e5cd-157">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="3e5cd-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="3e5cd-158">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="3e5cd-158">Video player module</span></span>](add-video-player.md)

