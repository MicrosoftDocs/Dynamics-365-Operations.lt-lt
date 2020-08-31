---
title: Antraštės modulis
description: Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686627"
---
# <a name="header-module"></a><span data-ttu-id="57757-103">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="57757-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57757-104">Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="57757-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="57757-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="57757-105">Overview</span></span>

<span data-ttu-id="57757-106">„Dynamics 365 Commerce“ puslapio antraštę sudaro keli moduliai, pavyzdžiui, antraštė, naršymo meniu, ieška, reklaminė juosta, sutikimo naudoti slapukus moduliai.</span><span class="sxs-lookup"><span data-stu-id="57757-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="57757-107">Antraštės modulyje yra svetainės logotipas, saitai į naršymo hierarchiją, saitai į kitus svetainės puslapius, krepšelio simbolis, pageidavimų sąrašo simbolis, prisijungimo parinktys ir ieškos juosta.</span><span class="sxs-lookup"><span data-stu-id="57757-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="57757-108">Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (kitais žodžiais, stacionariam įrenginiui arba mobiliajam įrenginiui).</span><span class="sxs-lookup"><span data-stu-id="57757-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="57757-109">Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).</span><span class="sxs-lookup"><span data-stu-id="57757-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="57757-110">Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio antraštės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="57757-110">The following image shows an example of a header module on a home page.</span></span>

![Antraštės modulio pavyzdys](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="57757-112">Antraštės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="57757-112">Properties of a header module</span></span>

<span data-ttu-id="57757-113">Antraštės modulis palaiko ypatybes **Logotipo vaizdas**, **Logotipo saitas** ir **Mano paskyros saitai**.</span><span class="sxs-lookup"><span data-stu-id="57757-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="57757-114">Ypatybės **Logotipo vaizdas** ir **Logotipo saitas** naudojamos logotipui puslapyje apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="57757-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="57757-115">Daugiau informacijos žr. [Logotipo pridėjimas](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="57757-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="57757-116">Ypatybę **Mano paskyros saitai** galima naudoti norint apibrėžti paskyros puslapius, kurių sparčiuosius saitus svetainės savininkas nori rodyti antraštėje.</span><span class="sxs-lookup"><span data-stu-id="57757-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="57757-117">Moduliai, esantys antraštės modulyje</span><span class="sxs-lookup"><span data-stu-id="57757-117">Modules that are available in a header module</span></span>

<span data-ttu-id="57757-118">Antraštės modulyje galima naudoti tolesnius modulius.</span><span class="sxs-lookup"><span data-stu-id="57757-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="57757-119">**Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai.</span><span class="sxs-lookup"><span data-stu-id="57757-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="57757-120">Kanalo naršymo hierarchiją galima konfigūruoti programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="57757-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="57757-121">Naršymo meniu turi ypatybę **Naršymo šaltinis**, kuri naudojama norint apibrėžti mažmeninės prekybos serverio naršymo meniu elementus ir statinio meniu elementus kaip šaltinį.</span><span class="sxs-lookup"><span data-stu-id="57757-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="57757-122">Jei statinio meniu elementai apibrėžiami kaip šaltinis, svetainėje gali būti pateikiami susiję saitai į kitus puslapius.</span><span class="sxs-lookup"><span data-stu-id="57757-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="57757-123">Sukonfigūruoti elementai tada rodomi kaip antraštės naršymo elementai.</span><span class="sxs-lookup"><span data-stu-id="57757-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="57757-124">**Ieška** – ieškos modulyje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų.</span><span class="sxs-lookup"><span data-stu-id="57757-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="57757-125">Numatytojo ieškos puslapio URL ir ieškos užklausos parametrai turi būti pateikti **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="57757-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="57757-126">Ieškos modulyje yra ypatybių, kurios leidžia nerodyti ieškos mygtuko arba pažymėti, kaip pageidaujate.</span><span class="sxs-lookup"><span data-stu-id="57757-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="57757-127">Ieškos modulis taip pat palaiko automatinio pasiūlymo parinktis, pavyzdžiui, produktų, raktažodžių ar kategorijų ieškos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="57757-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="57757-128">**Krepšelio piktograma** – krepšelio piktogramos modulis vaizduoja krepšelio piktogramą, rodančią krepšelyje esančių prekių skaičių bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="57757-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="57757-129">Daugiau informacijos žr. [Krepšelio piktogramos modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="57757-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="57757-130">Puslapio antraštės modulio kūrimas</span><span class="sxs-lookup"><span data-stu-id="57757-130">Create a header module for a page</span></span>

<span data-ttu-id="57757-131">Norėdami sukurti antraštės modulį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="57757-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="57757-132">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="57757-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="57757-133">**Naujo puslapio fragmento** teksto laukelyje pasirinkite **Talpyklos** modulį, įveskite puslapio fragmento pavadinimą ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="57757-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="57757-134">Pasirinkite lizdą **Numatytasis konteineris**, tada dešinėje esančioje ypatybių srityje nustatykite ypatybės **Plotis** vertę **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="57757-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="57757-135">Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="57757-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="57757-136">Dialogo lange **Įtraukti modulį** pasirinkite modulius **Reklaminė juosta** ir **Sutikimas dėl slapukų**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="57757-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="57757-137">Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="57757-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="57757-138">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="57757-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="57757-139">Pasirinkite vietą **Konteineris**, tada dešinėje esančioje ypatybių srityje nustatykite ypatybės **Plotis** vertę **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="57757-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="57757-140">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="57757-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="57757-141">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Antraštė**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="57757-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="57757-142">Antraštės modulio vietoje **Naršymo meniu** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="57757-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="57757-143">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo meniu** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="57757-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="57757-144">Naršymo meniu modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.</span><span class="sxs-lookup"><span data-stu-id="57757-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="57757-145">Antraštės modulio vietoje **Ieška** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="57757-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="57757-146">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Paieška**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="57757-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="57757-147">Ieškos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.</span><span class="sxs-lookup"><span data-stu-id="57757-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="57757-148">Antraštės modulio vietoje **Krepšelio piktograma** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="57757-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="57757-149">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Krepšelio piktograma**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="57757-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="57757-150">Krepšelio piktogramos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.</span><span class="sxs-lookup"><span data-stu-id="57757-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="57757-151">Jei norite, kad krepšelio piktogramoje būtų rodoma krepšelio santrauka (taip pat žinoma kaip mini krepšelis), kai vartotojai užveda žymeklį, pasirinkite **Rodyti mini krepšelį**.</span><span class="sxs-lookup"><span data-stu-id="57757-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="57757-152">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="57757-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="57757-153">Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="57757-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="57757-154">Modulio **Numatytasis puslapis** vietoje **Antraštė** įtraukite jūsų sukurtą poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="57757-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="57757-155">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="57757-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57757-156">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="57757-156">Additional resources</span></span>

[<span data-ttu-id="57757-157">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="57757-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="57757-158">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="57757-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="57757-159">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="57757-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="57757-160">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="57757-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="57757-161">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="57757-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="57757-162">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="57757-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="57757-163">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="57757-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="57757-164">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="57757-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="57757-165">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="57757-165">Footer module</span></span>](author-footer-module.md)
