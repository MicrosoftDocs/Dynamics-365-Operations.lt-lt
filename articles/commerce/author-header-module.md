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
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411223"
---
# <a name="header-module"></a><span data-ttu-id="1a2ac-103">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a2ac-104">Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1a2ac-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="1a2ac-105">Overview</span></span>

<span data-ttu-id="1a2ac-106">„Dynamics 365 Commerce“ puslapio antraštę sudaro keli moduliai, pavyzdžiui, antraštė, naršymo meniu, ieška, reklaminė juosta, sutikimo naudoti slapukus moduliai.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="1a2ac-107">Antraštės modulyje yra svetainės logotipas, saitai į naršymo hierarchiją, saitai į kitus svetainės puslapius, krepšelio simbolis, pageidavimų sąrašo simbolis, prisijungimo parinktys ir ieškos juosta.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="1a2ac-108">Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (kitais žodžiais, stacionariam įrenginiui arba mobiliajam įrenginiui).</span><span class="sxs-lookup"><span data-stu-id="1a2ac-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="1a2ac-109">Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).</span><span class="sxs-lookup"><span data-stu-id="1a2ac-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="1a2ac-110">Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio antraštės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-110">The following image shows an example of a header module on a home page.</span></span>

![Antraštės modulio pavyzdys](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="1a2ac-112">Antraštės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="1a2ac-112">Properties of a header module</span></span>

<span data-ttu-id="1a2ac-113">Antraštės modulis palaiko ypatybes **Logotipo vaizdas**, **Logotipo saitas** ir **Mano paskyros saitai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="1a2ac-114">Ypatybės **Logotipo vaizdas** ir **Logotipo saitas** naudojamos logotipui puslapyje apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="1a2ac-115">Daugiau informacijos žr. [Logotipo pridėjimas](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ac-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="1a2ac-116">Ypatybę **Mano paskyros saitai** galima naudoti norint apibrėžti paskyros puslapius, kurių sparčiuosius saitus svetainės savininkas nori rodyti antraštėje.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="1a2ac-117">Moduliai, esantys antraštės modulyje</span><span class="sxs-lookup"><span data-stu-id="1a2ac-117">Modules that are available in a header module</span></span>

<span data-ttu-id="1a2ac-118">Antraštės modulyje galima naudoti tolesnius modulius.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="1a2ac-119">**Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="1a2ac-120">Kanalo naršymo hierarchiją galima konfigūruoti programoje „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1a2ac-121">Naršymo meniu turi ypatybę **Naršymo šaltinis**, kuri naudojama norint apibrėžti mažmeninės prekybos serverio naršymo meniu elementus ir statinio meniu elementus kaip šaltinį.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="1a2ac-122">Jei statinio meniu elementai apibrėžiami kaip šaltinis, svetainėje gali būti pateikiami susiję saitai į kitus puslapius.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="1a2ac-123">Sukonfigūruoti elementai tada rodomi kaip antraštės naršymo elementai.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="1a2ac-124">**Ieška** – ieškos modulyje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="1a2ac-125">Numatytojo ieškos puslapio URL ir ieškos užklausos parametrai turi būti pateikti **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="1a2ac-126">Ieškos modulyje yra ypatybių, kurios leidžia nerodyti ieškos mygtuko arba pažymėti, kaip pageidaujate.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="1a2ac-127">Ieškos modulis taip pat palaiko automatinio pasiūlymo parinktis, pavyzdžiui, produktų, raktažodžių ar kategorijų ieškos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="1a2ac-128">**Krepšelio piktograma** – krepšelio piktogramos modulis vaizduoja krepšelio piktogramą, rodančią krepšelyje esančių prekių skaičių bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="1a2ac-129">Daugiau informacijos žr. [Krepšelio piktogramos modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="1a2ac-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="1a2ac-130">Puslapio antraštės modulio kūrimas</span><span class="sxs-lookup"><span data-stu-id="1a2ac-130">Create a header module for a page</span></span>

<span data-ttu-id="1a2ac-131">Norėdami sukurti antraštės modulį, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="1a2ac-132">Nueikite į **Puslapio fragmentai** ir pasirinkite **Naujas**, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-132">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="1a2ac-133">Dialogo lange **Naujas puslapio fragmentas** pasirinkite modulį **Konteineris**, įveskite puslapio fragmento pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-133">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="1a2ac-134">Pasirinkite lizdą **Numatytasis konteineris**, tada dešinėje esančioje ypatybių srityje nustatykite ypatybės **Plotis** vertę **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="1a2ac-135">Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1a2ac-136">Dialogo lange **Įtraukti modulį** pasirinkite modulius **Reklaminė juosta** ir **Sutikimas dėl slapukų**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="1a2ac-137">Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1a2ac-138">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1a2ac-139">Pasirinkite vietą **Konteineris**, tada dešinėje esančioje ypatybių srityje nustatykite ypatybės **Plotis** vertę **Užpildyti konteinerį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="1a2ac-140">Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1a2ac-141">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Antraštė**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1a2ac-142">Antraštės modulio vietoje **Naršymo meniu** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1a2ac-143">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo meniu** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1a2ac-144">Naršymo meniu modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="1a2ac-145">Antraštės modulio vietoje **Ieška** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1a2ac-146">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Paieška**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1a2ac-147">Ieškos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="1a2ac-148">Antraštės modulio vietoje **Krepšelio piktograma** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1a2ac-149">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Krepšelio piktograma**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1a2ac-150">Krepšelio piktogramos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="1a2ac-151">Jei norite, kad krepšelio piktogramoje būtų rodoma krepšelio santrauka (taip pat žinoma kaip mini krepšelis), kai vartotojai užveda žymeklį, pasirinkite **Rodyti mini krepšelį**.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="1a2ac-152">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="1a2ac-153">Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="1a2ac-154">Modulio **Numatytasis puslapis** vietoje **Antraštė** įtraukite jūsų sukurtą poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="1a2ac-155">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="1a2ac-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a2ac-156">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="1a2ac-156">Additional resources</span></span>

[<span data-ttu-id="1a2ac-157">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="1a2ac-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1a2ac-158">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1a2ac-159">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="1a2ac-160">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1a2ac-161">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="1a2ac-162">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1a2ac-163">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1a2ac-164">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="1a2ac-165">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="1a2ac-165">Footer module</span></span>](author-footer-module.md)
