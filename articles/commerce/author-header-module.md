---
title: Antraštės modulis
description: Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261449"
---
# <a name="header-module"></a><span data-ttu-id="cace9-103">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cace9-104">Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="cace9-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cace9-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="cace9-105">Overview</span></span>

<span data-ttu-id="cace9-106">„Dynamics 365 Commerce“ puslapio antraštę sudaro keli moduliai, pavyzdžiui, antraštė, naršymo meniu, ieška, reklaminė juosta, sutikimo naudoti slapukus moduliai.</span><span class="sxs-lookup"><span data-stu-id="cace9-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="cace9-107">Antraštės modulyje yra svetainės logotipas, saitai į naršymo hierarchiją, saitai į kitus svetainės puslapius, krepšelio simbolis, pageidavimų sąrašo simbolis, prisijungimo parinktys ir ieškos juosta.</span><span class="sxs-lookup"><span data-stu-id="cace9-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="cace9-108">Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (kitais žodžiais, stacionariam įrenginiui arba mobiliajam įrenginiui).</span><span class="sxs-lookup"><span data-stu-id="cace9-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="cace9-109">Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).</span><span class="sxs-lookup"><span data-stu-id="cace9-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="cace9-110">Antraštės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="cace9-110">Properties of a header module</span></span>

<span data-ttu-id="cace9-111">Antraštės modulis palaiko ypatybes **Logotipo vaizdas**, **Logotipo saitas** ir **Mano paskyros saitai**.</span><span class="sxs-lookup"><span data-stu-id="cace9-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="cace9-112">Ypatybės **Logotipo vaizdas** ir **Logotipo saitas** naudojamos logotipui puslapyje apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="cace9-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="cace9-113">Daugiau informacijos žr. [Logotipo pridėjimas](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="cace9-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="cace9-114">Ypatybę **Mano paskyros saitai** galima naudoti norint apibrėžti paskyros puslapius, kurių sparčiuosius saitus svetainės savininkas nori rodyti antraštėje.</span><span class="sxs-lookup"><span data-stu-id="cace9-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="cace9-115">Moduliai, esantys antraštės modulyje</span><span class="sxs-lookup"><span data-stu-id="cace9-115">Modules that are available in a header module</span></span>

<span data-ttu-id="cace9-116">Antraštės modulyje galima naudoti tolesnius modulius.</span><span class="sxs-lookup"><span data-stu-id="cace9-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="cace9-117">**Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai.</span><span class="sxs-lookup"><span data-stu-id="cace9-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="cace9-118">Kanalo naršymo hierarchiją galima konfigūruoti programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="cace9-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="cace9-119">Naršymo meniu turi ypatybę **Naršymo šaltinis**, kuri naudojama norint apibrėžti mažmeninės prekybos serverio naršymo meniu elementus ir statinio meniu elementus kaip šaltinį.</span><span class="sxs-lookup"><span data-stu-id="cace9-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="cace9-120">Jei statinio meniu elementai apibrėžiami kaip šaltinis, svetainėje gali būti pateikiami susiję saitai į kitus puslapius.</span><span class="sxs-lookup"><span data-stu-id="cace9-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="cace9-121">Sukonfigūruoti elementai tada rodomi kaip antraštės naršymo elementai.</span><span class="sxs-lookup"><span data-stu-id="cace9-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="cace9-122">**Ieška** – ieškos modulyje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų.</span><span class="sxs-lookup"><span data-stu-id="cace9-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="cace9-123">Numatytojo ieškos puslapio URL ir ieškos užklausos parametrai turi būti pateikti **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="cace9-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="cace9-124">Ieškos modulyje yra ypatybių, kurios leidžia nerodyti ieškos mygtuko arba pažymėti, kaip pageidaujate.</span><span class="sxs-lookup"><span data-stu-id="cace9-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="cace9-125">Ieškos modulis taip pat palaiko automatinio pasiūlymo parinktis, pavyzdžiui, produktų, raktažodžių ar kategorijų ieškos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="cace9-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="cace9-126">**Krepšelio piktograma** – krepšelio piktogramos modulis vaizduoja krepšelio piktogramą, rodančią krepšelyje esančių prekių skaičių bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="cace9-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="cace9-127">Daugiau informacijos žr. [Krepšelio piktogramos modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="cace9-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="cace9-128">Puslapio antraštės modulio kūrimas</span><span class="sxs-lookup"><span data-stu-id="cace9-128">Create a header module for a page</span></span>

<span data-ttu-id="cace9-129">Norėdami sukurti antraštės modulį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cace9-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="cace9-130">Sukurkite fragmentą pavadinimu **Antraštės fragmentas** ir į jį įtraukite konteinerio modulį.</span><span class="sxs-lookup"><span data-stu-id="cace9-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="cace9-131">Konteinerio modulio ypatybių srityje nustatykite ypatybę **Plotis** į **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="cace9-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="cace9-132">Į konteinerio modulį įtraukite reklaminę juostą ir sutikimo dėl slapukų modulius.</span><span class="sxs-lookup"><span data-stu-id="cace9-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="cace9-133">Į fragmentą įtraukite kitą konteinerio modulį ir ypatybę **Plotis** nustatykite į **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="cace9-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="cace9-134">Į antrą konteinerio modulį įtraukite antraštę.</span><span class="sxs-lookup"><span data-stu-id="cace9-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="cace9-135">Antraštės modulio atkarpoje **Naršymo meniu** įtraukite naršymo meniu modulį.</span><span class="sxs-lookup"><span data-stu-id="cace9-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="cace9-136">Naršymo meniu modulio ypatybių srityje sukonfigūruokite naršymo meniu modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="cace9-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="cace9-137">Į antraštės modulio atkarpą **Ieška** įtraukite ieškos modulį.</span><span class="sxs-lookup"><span data-stu-id="cace9-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="cace9-138">Ieškos meniu modulio ypatybių srityje sukonfigūruokite ieškos modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="cace9-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="cace9-139">Antraštės modulio vietoje **Krepšelio piktograma** įtraukite krepšelio piktogramos modulį.</span><span class="sxs-lookup"><span data-stu-id="cace9-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="cace9-140">Krepšelio piktogramos modulio ypatybių srityje sukonfigūruokite krepšelio piktogramos modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="cace9-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="cace9-141">Jei norite, kad būtų rodomas mažasis krepšelis, kai virš jo užvestas pelės žymiklis, nustatykite parinktį **Rodyti mažąjį krepšelį** į **Teisinga**.</span><span class="sxs-lookup"><span data-stu-id="cace9-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="cace9-142">Įrašykite puslapio fragmentą, baikite redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="cace9-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="cace9-143">Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cace9-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="cace9-144">Į numatytojo puslapio atkarpą **Pagrindinis** įtraukite antraštės puslapio fragmentą, kuriame yra antraštės modulis.</span><span class="sxs-lookup"><span data-stu-id="cace9-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="cace9-145">Įrašykite šabloną, baikite redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="cace9-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cace9-146">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cace9-146">Additional resources</span></span>

[<span data-ttu-id="cace9-147">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="cace9-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cace9-148">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="cace9-149">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cace9-150">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cace9-151">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="cace9-152">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="cace9-153">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="cace9-154">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="cace9-155">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="cace9-155">Footer module</span></span>](author-footer-module.md)
