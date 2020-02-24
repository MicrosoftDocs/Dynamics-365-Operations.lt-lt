---
title: Teksto bloko modulis
description: Šioje temoje aprašomi teksto bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025602"
---
# <a name="text-block-module"></a><span data-ttu-id="dac35-103">Teksto bloko modulis</span><span class="sxs-lookup"><span data-stu-id="dac35-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dac35-104">Šioje temoje aprašomi teksto bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="dac35-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dac35-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="dac35-105">Overview</span></span>

<span data-ttu-id="dac35-106">Teksto bloko modulis yra modulis, kuris naudojamas teksto turiniui pridėti.</span><span class="sxs-lookup"><span data-stu-id="dac35-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="dac35-107">Šis turinys gali būti informacinis arba reklaminis.</span><span class="sxs-lookup"><span data-stu-id="dac35-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="dac35-108">Teksto bloko moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="dac35-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="dac35-109">Jie yra atskiri moduliai, nepriklausantys nuo puslapio konteksto ar kitų modulių.</span><span class="sxs-lookup"><span data-stu-id="dac35-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="dac35-110">Teksto bloko modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="dac35-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="dac35-111">Teksto bloko modulius galima naudoti toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="dac35-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="dac35-112">Norint produktų išsamios informacijos puslapyje parodyti produktų ypatybes.</span><span class="sxs-lookup"><span data-stu-id="dac35-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="dac35-113">Informaciniais tikslais bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="dac35-113">For informational purposes on any page.</span></span> <span data-ttu-id="dac35-114">Pavyzdžiui, juos naudojant galima paaiškinti lojalumo programų privalumus, aprašyti siuntimo ir grąžinimo strategijas, atsakyti į dažnai užduodamus klausimus arba pateikti turinio „apie mus“.</span><span class="sxs-lookup"><span data-stu-id="dac35-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="dac35-115">Norint produktų išsamios informacijos puslapyje įtraukti pasirinktinių pranešimų.</span><span class="sxs-lookup"><span data-stu-id="dac35-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="dac35-116">(Pavyzdžiui, „Didesni, nei 50 USD, užsakymai pristatomi nemokamai“).</span><span class="sxs-lookup"><span data-stu-id="dac35-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="dac35-117">Norint produktų išsamios informacijos puslapiuose, krepšelio puslapiuose, pirkimo užbaigimo puslapiuose ir kituose puslapiuose įtraukti informaciją apie atsakomės atsisakymą ir kontaktinę informaciją (pavyzdžiui, „Siunčiant ir grąžinant prekes taikomos parduotuvės strategijos“).</span><span class="sxs-lookup"><span data-stu-id="dac35-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="dac35-118">Teksto bloko modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="dac35-118">Text block module properties</span></span>

| <span data-ttu-id="dac35-119">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="dac35-119">Property name</span></span>     | <span data-ttu-id="dac35-120">Value</span><span class="sxs-lookup"><span data-stu-id="dac35-120">Value</span></span>                                            | <span data-ttu-id="dac35-121">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="dac35-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="dac35-122">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="dac35-122">Rich text</span></span>         | <span data-ttu-id="dac35-123">Raiškusis tekstas</span><span class="sxs-lookup"><span data-stu-id="dac35-123">Rich text</span></span>                                        | <span data-ttu-id="dac35-124">Pastraipos tekstas.</span><span class="sxs-lookup"><span data-stu-id="dac35-124">Paragraph text.</span></span> <span data-ttu-id="dac35-125">Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas.</span><span class="sxs-lookup"><span data-stu-id="dac35-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="dac35-126">Pasirinktinis klasės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="dac35-126">Custom class name</span></span> | <span data-ttu-id="dac35-127">Pakopinio stiliaus aprašų (CSS) klasės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="dac35-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="dac35-128">Pasirinktinės CSS klasės, kurią kūrėjas teikia formatuoti šį modulį, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="dac35-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="dac35-129">Klasės pavadinimas turi būti nurodytas temų pakete.</span><span class="sxs-lookup"><span data-stu-id="dac35-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="dac35-130">Šrifto dydis</span><span class="sxs-lookup"><span data-stu-id="dac35-130">Font size</span></span>         | <span data-ttu-id="dac35-131">**Mažas**, **Vidutinis**, **Didelis** arba **X dydžio**</span><span class="sxs-lookup"><span data-stu-id="dac35-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="dac35-132">Turinio šrifto dydis.</span><span class="sxs-lookup"><span data-stu-id="dac35-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="dac35-133">Teksto bloko modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="dac35-133">Add a text block module to a page</span></span>

<span data-ttu-id="dac35-134">Norėdami į naują puslapį įtraukti teksto bloko modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dac35-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="dac35-135">Sukurkite puslapio šabloną, pavadintą **Turinio šablonas**.</span><span class="sxs-lookup"><span data-stu-id="dac35-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="dac35-136">Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis modulis**.</span><span class="sxs-lookup"><span data-stu-id="dac35-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="dac35-137">Baikite šablono redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="dac35-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="dac35-138">Naudodami ką tik sukurtą turinio šabloną, sukurkite puslapį, pavadintą **Turinio puslapis**.</span><span class="sxs-lookup"><span data-stu-id="dac35-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="dac35-139">Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="dac35-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="dac35-140">Konteinerio modulio ypatybių srityje nustatykite ypatybę **Plotis** į **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="dac35-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="dac35-141">Į konteinerio modulį įtraukite teksto bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="dac35-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="dac35-142">Teksto bloko modulio ypatybių srityje įtraukite tekstą į lauką **Raiškusis tekstas**.</span><span class="sxs-lookup"><span data-stu-id="dac35-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="dac35-143">Baikite puslapio redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="dac35-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dac35-144">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="dac35-144">Additional resources</span></span>

[<span data-ttu-id="dac35-145">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="dac35-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="dac35-146">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="dac35-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="dac35-147">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="dac35-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="dac35-148">Turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="dac35-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="dac35-149">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="dac35-149">Video player module</span></span>](add-video-player.md)

