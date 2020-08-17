---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621041"
---
# <a name="cart-module"></a><span data-ttu-id="79164-103">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="79164-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="79164-104">Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="79164-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="79164-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="79164-105">Overview</span></span>

<span data-ttu-id="79164-106">Krepšelio modulyje rodomos prekes, kurios buvo įtrauktos į krepšelį, prieš klientui išsiregistruojant.</span><span class="sxs-lookup"><span data-stu-id="79164-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="79164-107">Šiame modulyje taip pat rodoma užsakymo suvestinė, be to, klientui leidžiama taikyti arba pašalinti reklaminius kodus.</span><span class="sxs-lookup"><span data-stu-id="79164-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="79164-108">Krepšelio modulis palaiko prisijungusiųjų išsiregistravimą ir svečių išsiregistravimą.</span><span class="sxs-lookup"><span data-stu-id="79164-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="79164-109">Jis taip pat palaiko saitą **Grįžti prie pirkimo**.</span><span class="sxs-lookup"><span data-stu-id="79164-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="79164-110">Galite konfigūruoti šio saito maršrutą eidami į **Svetainės parametrai \> Plėtiniai \> Maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="79164-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="79164-111">Krepšelio modulis generuoja duomenis pagal krepšelio ID, kuris yra naršyklės slapukas, pasiekiamas visoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="79164-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="79164-112">Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="79164-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Krepšelio modulio pavyzdys](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="79164-114">Krepšelio modulio ypatybės ir vietos</span><span class="sxs-lookup"><span data-stu-id="79164-114">Cart module properties and slots</span></span>

<span data-ttu-id="79164-115">Krepšelio modulyje yra ypatybė **Antraštė**, kurią galima nustatyti kaip **Pirkinių krepšelis** ir **Jūsų krepšelio prekės**.</span><span class="sxs-lookup"><span data-stu-id="79164-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="79164-116">Moduliai, kuriuos galima naudoti krepšelio modulyje</span><span class="sxs-lookup"><span data-stu-id="79164-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="79164-117">**Teksto blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę.</span><span class="sxs-lookup"><span data-stu-id="79164-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="79164-118">Pranešimai grindžiami turinio valdymo sistema (TVS).</span><span class="sxs-lookup"><span data-stu-id="79164-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="79164-119">Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="79164-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="79164-120">**Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="79164-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="79164-121">Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves.</span><span class="sxs-lookup"><span data-stu-id="79164-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="79164-122">Daugiau informacijos apie šį modulį žr. [Parduotuvės parinkiklio modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="79164-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="79164-123">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="79164-123">Module properties</span></span>

<span data-ttu-id="79164-124">Dalyje **Svetainės parametrai \> Plėtiniai** galima konfigūruoti toliau pateiktus krepšelio modulio parametrus:</span><span class="sxs-lookup"><span data-stu-id="79164-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="79164-125">**Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="79164-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="79164-126">Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.</span><span class="sxs-lookup"><span data-stu-id="79164-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="79164-127">**Atsargos** – norėdami gauti informacijos apie atsargų parametrų taikymą, žr. [Atsargų parametrų taikymas](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="79164-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="79164-128">**Grįžimas prie pirkimo** – ši ypatybė naudojama norint nurodyti saito **Grįžimas prie pirkimo** maršrutą.</span><span class="sxs-lookup"><span data-stu-id="79164-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="79164-129">Maršrutas gali būti sukonfigūruotas svetainės lygiu, leidžiant mažmeninės prekybos klientams grįžti į pagrindinį puslapį arba bet kurį kitą svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="79164-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="79164-130">„Commerce Scale Unit“ sąveika</span><span class="sxs-lookup"><span data-stu-id="79164-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="79164-131">Vežimėlio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas.</span><span class="sxs-lookup"><span data-stu-id="79164-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="79164-132">Visa informacija apie produktus iš „Commerce Scale Unit“ gaunama naudojant krepšelio ID iš naršyklės slapuko.</span><span class="sxs-lookup"><span data-stu-id="79164-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="79164-133">Krepšelio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="79164-133">Add a cart module to a page</span></span>

<span data-ttu-id="79164-134">Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="79164-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="79164-135">Nueikite į **Puslapio fragmentai** ir pasirinkite **Naujas**, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="79164-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="79164-136">Dialogo lange **Naujas puslapio fragmentas** pasirinkite modulį **Krepšelis**.</span><span class="sxs-lookup"><span data-stu-id="79164-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="79164-137">Dalyje **Puslapio fragmento pavadinimas** įveskite pavadinimą **Krepšelio fragmentas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="79164-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="79164-138">Pasirinkite vietą **Krepšelis**.</span><span class="sxs-lookup"><span data-stu-id="79164-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="79164-139">Dešinėje pusėje esančioje ypatybių srityje pasirinkite pieštuko simbolį, į laukelį įveskite antraštės tekstą ir pasirinkite varnelės simbolį.</span><span class="sxs-lookup"><span data-stu-id="79164-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="79164-140">Vietoje **Krepšelis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="79164-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="79164-141">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Parduotuvės parinkiklis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="79164-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="79164-142">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="79164-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="79164-143">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="79164-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="79164-144">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="79164-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="79164-145">Struktūros medyje pasirinkite vietą **Pagrindinė dalis**, pasirinkite daugtaškį (**...**), tada – **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="79164-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="79164-146">Dialogo lange **Pasirinkti puslapio fragmentą** pasirinkite **krepšelio fragmentą** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="79164-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="79164-147">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="79164-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="79164-148">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="79164-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="79164-149">Dialogo lange **Pasirinkti šabloną** pasirinkite anksčiau sukurtą šabloną, įveskite puslapio pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="79164-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="79164-150">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="79164-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="79164-151">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="79164-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79164-152">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="79164-152">Additional resources</span></span>

[<span data-ttu-id="79164-153">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="79164-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="79164-154">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="79164-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="79164-155">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="79164-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="79164-156">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="79164-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="79164-157">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="79164-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="79164-158">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="79164-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="79164-159">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="79164-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="79164-160">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="79164-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="79164-161">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="79164-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="79164-162">Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="79164-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
