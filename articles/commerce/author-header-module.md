---
title: Antraštės modulis
description: Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b14178431b281daa827749781dd16481f8bfb74
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799921"
---
# <a name="header-module"></a><span data-ttu-id="d46f4-103">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="d46f4-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d46f4-104">Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="d46f4-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d46f4-105">„Dynamics 365 Commerce” puslapio antraštė sukonfigūruota kaip puslapio fragmentas, į kurį įtraukta antraštė, reklaminė juosta ir sutikimo naudoti slapukus moduliai.</span><span class="sxs-lookup"><span data-stu-id="d46f4-105">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="d46f4-106">Antraštės modulyje yra svetainės logotipas, saitai į naršymo hierarchiją, saitai į kitus svetainės puslapius, krepšelio piktogramos modulis, pageidavimų sąrašo simbolis, prisijungimo parinktys ir ieškos juosta.</span><span class="sxs-lookup"><span data-stu-id="d46f4-106">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="d46f4-107">Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (kitais žodžiais, stacionariam įrenginiui arba mobiliajam įrenginiui).</span><span class="sxs-lookup"><span data-stu-id="d46f4-107">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="d46f4-108">Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).</span><span class="sxs-lookup"><span data-stu-id="d46f4-108">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="d46f4-109">Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio antraštės modulio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="d46f4-109">The following image shows an example of a header module on a home page.</span></span>

![Antraštės modulio pavyzdys](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="d46f4-111">Antraštės modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="d46f4-111">Properties of a header module</span></span>

<span data-ttu-id="d46f4-112">Antraštės modulis palaiko ypatybes **Logotipo vaizdas**, **Logotipo saitas** ir **Mano paskyros saitai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-112">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="d46f4-113">Ypatybės **Logotipo vaizdas** ir **Logotipo saitas** naudojamos logotipui puslapyje apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="d46f4-113">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="d46f4-114">Daugiau informacijos žr. [Logotipo pridėjimas](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="d46f4-114">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="d46f4-115">Ypatybę **Mano paskyros saitai** galima naudoti norint apibrėžti paskyros puslapius, kurių sparčiuosius saitus svetainės savininkas nori rodyti antraštėje.</span><span class="sxs-lookup"><span data-stu-id="d46f4-115">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="d46f4-116">Moduliai, esantys antraštės modulyje</span><span class="sxs-lookup"><span data-stu-id="d46f4-116">Modules that are available within a header module</span></span>

<span data-ttu-id="d46f4-117">Antraštės modulyje galima naudoti tolesnius modulius.</span><span class="sxs-lookup"><span data-stu-id="d46f4-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="d46f4-118">**Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai.</span><span class="sxs-lookup"><span data-stu-id="d46f4-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="d46f4-119">Daugiau informacijos žr. [Naršymo meniu modulis](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="d46f4-119">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="d46f4-120">**Ieška** – ieškos modulyje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų.</span><span class="sxs-lookup"><span data-stu-id="d46f4-120">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="d46f4-121">Numatytojo ieškos puslapio URL ir ieškos užklausos parametrai turi būti pateikti **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-121">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="d46f4-122">Ieškos modulyje yra ypatybių, kurios leidžia nerodyti ieškos mygtuko arba pažymėti, kaip pageidaujate.</span><span class="sxs-lookup"><span data-stu-id="d46f4-122">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="d46f4-123">Ieškos modulis taip pat palaiko automatinio pasiūlymo parinktis, pavyzdžiui, produktų, raktažodžių ar kategorijų ieškos rezultatus.</span><span class="sxs-lookup"><span data-stu-id="d46f4-123">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="d46f4-124">**Krepšelio piktograma** – krepšelio piktogramos modulis vaizduoja krepšelio piktogramą, rodančią krepšelyje esančių prekių skaičių bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="d46f4-124">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="d46f4-125">Daugiau informacijos žr. [Krepšelio piktogramos modulis](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="d46f4-125">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="d46f4-126">**Svetainės išrinkiklis** – svetainės išrinkiklio modulis leidžia vartotojams naršyti įvairiose iš anksto nustatytose rinkų, regionų ir vietovių svetainėse.</span><span class="sxs-lookup"><span data-stu-id="d46f4-126">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="d46f4-127">Daugiau informacijos žr. [Svetainės išrinkiklio modulis](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d46f4-127">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="d46f4-128">**Parduotuvės išrinkiklis** – parduotuvės išrinkiklio modulį galima įtraukti į antraštės modulio parduotuvės išrinkiklio vietą.</span><span class="sxs-lookup"><span data-stu-id="d46f4-128">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="d46f4-129">Jis leidžia vartotojams naršyti ir rasti netoliese esančias parduotuves.</span><span class="sxs-lookup"><span data-stu-id="d46f4-129">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="d46f4-130">Vartotojai taip pat gali nurodyti pageidaujamą parduotuvę.</span><span class="sxs-lookup"><span data-stu-id="d46f4-130">Users can also specify a preferred store.</span></span> <span data-ttu-id="d46f4-131">Ši parduotuvė bus rodoma antraštėje.</span><span class="sxs-lookup"><span data-stu-id="d46f4-131">That store will then be shown in the header.</span></span> <span data-ttu-id="d46f4-132">Kai parduotuvės išrinkiklio modulis įtraukiamas į antraštės modulį, jo ypatybė **Režimas** turi būti nustatyta į **Rasti parduotuves**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-132">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="d46f4-133">Daugiau informacijos žr. [Parduotuvės išrinkiklio modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="d46f4-133">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="d46f4-134">Krepšelio piktogramos modulio naudojimo antraštės moduliuose palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.11 leidime.</span><span class="sxs-lookup"><span data-stu-id="d46f4-134">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="d46f4-135">Svetainės išrinkiklio modulio naudojimo antraštės moduliuose palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.14 leidime.</span><span class="sxs-lookup"><span data-stu-id="d46f4-135">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="d46f4-136">Parduotuvės išrinkiklio modulio naudojimo antraštės moduliuose palaikymas pasiekiamas „Dynamics 365 Commerce” 10.0.15 leidime.</span><span class="sxs-lookup"><span data-stu-id="d46f4-136">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="d46f4-137">Puslapio antraštės fragmento kūrimas</span><span class="sxs-lookup"><span data-stu-id="d46f4-137">Create a header fragment for a page</span></span>

<span data-ttu-id="d46f4-138">Norėdami sukurti antraštės fragmentą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d46f4-138">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="d46f4-139">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="d46f4-139">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d46f4-140">Dialogo lange **Naujas fragmentas** pasirinkite **Konteinerio** modulį, įveskite fragmento pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-140">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d46f4-141">Pasirinkite lizdą **Numatytasis konteineris**, tada dešinėje esančioje ypatybių srityje nustatykite ypatybės **Plotis** vertę **Užpildyti ekraną**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-141">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="d46f4-142">Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-142">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d46f4-143">Dialogo lange **Įtraukti modulį** pasirinkite modulius **Sutikimas dėl slapukų**, **Antraštė** ir **Reklaminė juosta**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-143">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="d46f4-144">Modulio **Reklaminė juosta** ypatybių srityje pasirinkite **Įtraukti pranešimą**, tada pasirinkite **Pranešimas**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-144">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="d46f4-145">Dialogo lange **Pranešimas** įtraukite tekstą ir reklaminio turinio saitų, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-145">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="d46f4-146">Modulio **Sutikimas dėl slapukų** ypatybių srityje įtraukite ir konfigūruokite tekstą bei saitą su svetainės privatumo puslapiu.</span><span class="sxs-lookup"><span data-stu-id="d46f4-146">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="d46f4-147">Antraštės modulio vietoje **Naršymo meniu** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-147">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d46f4-148">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo meniu** ir **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-148">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d46f4-149">Naršymo meniu modulio ypatybių srityje, dalyje **Naršymo meniu šaltinis**, pasirinkite **„Retail Server“**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-149">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="d46f4-150">Naršymo meniu modulio ypatybių srityje, dalyje **Statiniai meniu elementai**, pasirinkite **Įtraukti meniu elementą**, tada pasirinkite **Meniu elementas**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-150">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="d46f4-151">Dialogo lango **Meniu elementas** dalyje **Meniu elemento tekstas** įveskite „Kontaktas.”</span><span class="sxs-lookup"><span data-stu-id="d46f4-151">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="d46f4-152">Dialogo lango **Meniu elementas** dalyje **Meniu elemento saito paskirtis** pasirinkite **Įtraukti saitą**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-152">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="d46f4-153">Dialogo lange **Saito įtraukimas** pasirinkite svetainės puslapio „Kontaktas” URL, o tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-153">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="d46f4-154">Dialogo lange **Meniu elementas** pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-154">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="d46f4-155">Antraštės modulio vietoje **Ieška** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-155">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d46f4-156">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Paieška**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-156">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d46f4-157">Ieškos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.</span><span class="sxs-lookup"><span data-stu-id="d46f4-157">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="d46f4-158">Antraštės modulio vietoje **Krepšelio piktograma** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-158">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d46f4-159">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Krepšelio piktograma**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-159">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d46f4-160">Krepšelio piktogramos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.</span><span class="sxs-lookup"><span data-stu-id="d46f4-160">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="d46f4-161">Jei norite, kad krepšelio piktogramoje būtų rodoma krepšelio santrauka (taip pat žinoma kaip mini krepšelis), kai vartotojai užveda žymeklį, pasirinkite **Rodyti mini krepšelį**.</span><span class="sxs-lookup"><span data-stu-id="d46f4-161">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="d46f4-162">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="d46f4-162">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="d46f4-163">Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d46f4-163">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="d46f4-164">Modulio **Numatytasis puslapis** vietoje **Antraštė** įtraukite jūsų sukurtą poraštės fragmentą.</span><span class="sxs-lookup"><span data-stu-id="d46f4-164">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="d46f4-165">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="d46f4-165">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d46f4-166">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d46f4-166">Additional resources</span></span>

[<span data-ttu-id="d46f4-167">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="d46f4-167">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d46f4-168">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="d46f4-168">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d46f4-169">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="d46f4-169">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d46f4-170">Reklaminės juostos modulis</span><span class="sxs-lookup"><span data-stu-id="d46f4-170">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="d46f4-171">Naršymo meniu modulis</span><span class="sxs-lookup"><span data-stu-id="d46f4-171">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="d46f4-172">Sutikimas su slapukais</span><span class="sxs-lookup"><span data-stu-id="d46f4-172">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="d46f4-173">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="d46f4-173">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="d46f4-174">Svetainės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="d46f4-174">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="d46f4-175">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="d46f4-175">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]