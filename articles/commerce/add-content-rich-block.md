---
title: Raiškiojo turinio bloko modulis
description: Šioje temoje aprašomi raiškiojo turinio bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785426"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="184f1-103">Raiškiojo turinio bloko modulis</span><span class="sxs-lookup"><span data-stu-id="184f1-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="184f1-104">Šioje temoje aprašomi raiškiojo turinio bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="184f1-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="184f1-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="184f1-105">Overview</span></span>

<span data-ttu-id="184f1-106">Raiškiojo turinio bloko modulis yra specialus konteineris, į kurį galima įdėti vieną ar kelis raiškiojo turinio bloko elementus.</span><span class="sxs-lookup"><span data-stu-id="184f1-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="184f1-107">Raiškiojo turinio bloko moduliai naudojami tekstiniam puslapio turiniui.</span><span class="sxs-lookup"><span data-stu-id="184f1-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="184f1-108">Šis turinys gali būti informacinis arba reklaminis.</span><span class="sxs-lookup"><span data-stu-id="184f1-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="184f1-109">Raiškiojo turinio bloko elementų moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="184f1-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="184f1-110">Jie yra atskiri moduliai, nepriklausantys nuo puslapio konteksto ar kitų modulių.</span><span class="sxs-lookup"><span data-stu-id="184f1-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="184f1-111">Raiškiojo turinio bloko modulių pavyzdžiai el. prekyboje</span><span class="sxs-lookup"><span data-stu-id="184f1-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="184f1-112">Raiškiojo turinio bloko modulius galima naudoti toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="184f1-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="184f1-113">Norint produktų išsamios informacijos puslapyje parodyti produktų ypatybes.</span><span class="sxs-lookup"><span data-stu-id="184f1-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="184f1-114">Informaciniais tikslais bet kuriame puslapyje.</span><span class="sxs-lookup"><span data-stu-id="184f1-114">For informational purposes on any page.</span></span> <span data-ttu-id="184f1-115">Pavyzdžiui, juos naudojant galima paaiškinti lojalumo programų privalumus, aprašyti siuntimo ir grąžinimo strategijas, atsakyti į dažnai užduodamus klausimus arba pateikti turinio „apie mus“.</span><span class="sxs-lookup"><span data-stu-id="184f1-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="184f1-116">Norint produktų išsamios informacijos puslapyje įtraukti pasirinktinių pranešimų.</span><span class="sxs-lookup"><span data-stu-id="184f1-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="184f1-117">(Pavyzdžiui, „Didesni, nei 50 USD, užsakymai pristatomi nemokamai“).</span><span class="sxs-lookup"><span data-stu-id="184f1-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="184f1-118">Norint produktų išsamios informacijos puslapiuose, krepšelio puslapiuose, pirkimo užbaigimo puslapiuose ir kituose puslapiuose įtraukti informaciją apie atsakomės atsisakymą ir kontaktinę informaciją (pavyzdžiui, „Siunčiant ir grąžinant prekes taikomos parduotuvės strategijos“).</span><span class="sxs-lookup"><span data-stu-id="184f1-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="184f1-119">Raiškiojo turinio bloko modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="184f1-119">Content rich block module properties</span></span>

| <span data-ttu-id="184f1-120">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="184f1-120">Property name</span></span>     | <span data-ttu-id="184f1-121">Vertė</span><span class="sxs-lookup"><span data-stu-id="184f1-121">Value</span></span>                                 | <span data-ttu-id="184f1-122">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="184f1-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="184f1-123">Stulpelių skaičius</span><span class="sxs-lookup"><span data-stu-id="184f1-123">Number of columns</span></span> | <span data-ttu-id="184f1-124">Skaičius nuo **1** iki **4**</span><span class="sxs-lookup"><span data-stu-id="184f1-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="184f1-125">Raiškiojo turinio bloko stulpelių skaičius.</span><span class="sxs-lookup"><span data-stu-id="184f1-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="184f1-126">Gali būti iki keturių stulpelių.</span><span class="sxs-lookup"><span data-stu-id="184f1-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="184f1-127">Plotis</span><span class="sxs-lookup"><span data-stu-id="184f1-127">Width</span></span>             | <span data-ttu-id="184f1-128">**Užpildyti konteinerį** arba **Užpildyti ekraną**</span><span class="sxs-lookup"><span data-stu-id="184f1-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="184f1-129">Jei reikšmė nustatoma kaip **Užpildyti konteinerį**, konteinerio elementų plotį riboja konteineris.</span><span class="sxs-lookup"><span data-stu-id="184f1-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="184f1-130">Jei reikšmė nustatoma kaip **Užpildyti ekraną**, elementų pločio konteineris neriboja ir juos galima vaizduoti viso ekrano režimu.</span><span class="sxs-lookup"><span data-stu-id="184f1-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="184f1-131">Keisdami reikšmę, galite pasiekti norimą išdėstymą.</span><span class="sxs-lookup"><span data-stu-id="184f1-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="184f1-132">Raiškiojo turinio bloko elementų modulių ypatybės</span><span class="sxs-lookup"><span data-stu-id="184f1-132">Content rich block item module properties</span></span>

| <span data-ttu-id="184f1-133">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="184f1-133">Property name</span></span> | <span data-ttu-id="184f1-134">Vertė</span><span class="sxs-lookup"><span data-stu-id="184f1-134">Value</span></span>          | <span data-ttu-id="184f1-135">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="184f1-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="184f1-136">Pastraipa</span><span class="sxs-lookup"><span data-stu-id="184f1-136">Paragraph</span></span>     | <span data-ttu-id="184f1-137">Pastraipos tekstas</span><span class="sxs-lookup"><span data-stu-id="184f1-137">Paragraph text</span></span> | <span data-ttu-id="184f1-138">Tekstas, pridedamas prie kiekvieno raiškiojo turinio bloko elemento.</span><span class="sxs-lookup"><span data-stu-id="184f1-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="184f1-139">Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas.</span><span class="sxs-lookup"><span data-stu-id="184f1-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="184f1-140">Raiškiojo turinio bloko modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="184f1-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="184f1-141">Norėdami į naują puslapį įtraukti raiškiojo turinio bloko modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="184f1-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="184f1-142">Sukurkite puslapio šabloną, pavadintą **Turinio šablonas**.</span><span class="sxs-lookup"><span data-stu-id="184f1-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="184f1-143">Numatytojo puslapio vietoje **Pagrindinis** įtraukite raiškiojo turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="184f1-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="184f1-144">Šabloną įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="184f1-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="184f1-145">Naudodami ką tik sukurtą turinio šabloną, sukurkite puslapį, pavadintą **Turinio puslapis**.</span><span class="sxs-lookup"><span data-stu-id="184f1-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="184f1-146">Naujo puslapio vietoje **Pagrindinis** įtraukite raiškiojo turinio bloko modulį.</span><span class="sxs-lookup"><span data-stu-id="184f1-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="184f1-147">Raiškiojo turinio bloko modulio ypatybėse stulpelių skaičių nustatykite kaip **2**.</span><span class="sxs-lookup"><span data-stu-id="184f1-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="184f1-148">Raiškiojo turinio bloko modulyje pasirinkite **Įtraukti modulį** ir įtraukite raiškiojo turinio bloko elementą (pavyzdžiui, **1elementas**).</span><span class="sxs-lookup"><span data-stu-id="184f1-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="184f1-149">Naujame raiškiojo turinio bloko elemente įtraukite pastraipos tekstą.</span><span class="sxs-lookup"><span data-stu-id="184f1-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="184f1-150">Raiškiojo turinio bloko modulyje pasirinkite **Įtraukti modulį** ir įtraukite raiškiojo turinio bloko elementą (pavyzdžiui, **2elementas**).</span><span class="sxs-lookup"><span data-stu-id="184f1-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="184f1-151">Naujame raiškiojo turinio bloko elemente įtraukite pastraipos tekstą.</span><span class="sxs-lookup"><span data-stu-id="184f1-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="184f1-152">Įrašykite puslapį ir peržiūrėkite keitimus.</span><span class="sxs-lookup"><span data-stu-id="184f1-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="184f1-153">Turėtumėte matyti du raiškiojo teksto blokus dviejų stulpelių rodinyje.</span><span class="sxs-lookup"><span data-stu-id="184f1-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="184f1-154">Puslapį įrašykite ir atrakinkite bei publikuokite.</span><span class="sxs-lookup"><span data-stu-id="184f1-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="184f1-155">Jei įtrauksite trečią raiškiojo turinio bloko elementą, jis bus padėtas po anksčiau įtrauktais dviem elementais.</span><span class="sxs-lookup"><span data-stu-id="184f1-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="184f1-156">Keisdami konteinerio stulpelių ir elementų skaičių, galite pasiekti skirtingus tekstinio turinio maketus.</span><span class="sxs-lookup"><span data-stu-id="184f1-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="184f1-157">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="184f1-157">Additional resources</span></span>

[<span data-ttu-id="184f1-158">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="184f1-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="184f1-159">Įspėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="184f1-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="184f1-160">Karuselės modulis</span><span class="sxs-lookup"><span data-stu-id="184f1-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="184f1-161">Turinio išdėstymo modulis</span><span class="sxs-lookup"><span data-stu-id="184f1-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="184f1-162">Funkcijos modulis</span><span class="sxs-lookup"><span data-stu-id="184f1-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="184f1-163">Pagrindinės reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="184f1-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="184f1-164">Vaizdo įrašų leistuvo modulis</span><span class="sxs-lookup"><span data-stu-id="184f1-164">Video player module</span></span>](add-video-player.md)

