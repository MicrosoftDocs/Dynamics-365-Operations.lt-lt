---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.openlocfilehash: 07d485012bfc93c957b3dc42e3b0ed62e761dee1
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686771"
---
# <a name="cart-module"></a><span data-ttu-id="30dbe-103">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="30dbe-103">Cart module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="30dbe-104">Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="30dbe-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30dbe-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="30dbe-105">Overview</span></span>

<span data-ttu-id="30dbe-106">Krepšelio modulyje rodomos prekes, kurios buvo įtrauktos į krepšelį, prieš klientui išsiregistruojant.</span><span class="sxs-lookup"><span data-stu-id="30dbe-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="30dbe-107">Šiame modulyje taip pat rodoma užsakymo suvestinė, be to, klientui leidžiama taikyti arba pašalinti reklaminius kodus.</span><span class="sxs-lookup"><span data-stu-id="30dbe-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="30dbe-108">Krepšelio modulis palaiko prisijungusiųjų išsiregistravimą ir svečių išsiregistravimą.</span><span class="sxs-lookup"><span data-stu-id="30dbe-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="30dbe-109">Jis taip pat palaiko saitą **Grįžti prie pirkimo**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="30dbe-110">Galite konfigūruoti šio saito maršrutą eidami į **Svetainės parametrai \> Plėtiniai \> Maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="30dbe-111">Krepšelio modulis generuoja duomenis pagal krepšelio ID, kuris yra naršyklės slapukas, pasiekiamas visoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="30dbe-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="30dbe-112">Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="30dbe-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Krepšelio modulio pavyzdys](./media/cart2.PNG)

<span data-ttu-id="30dbe-114">Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="30dbe-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="30dbe-115">Šiame pavyzdyje, nėra jokio eilutės prekės paėmimo mokesčio.</span><span class="sxs-lookup"><span data-stu-id="30dbe-115">In this example, there is a handling fee for a line item.</span></span>

![Krepšelio modulio pavyzdys](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="30dbe-117">Krepšelio modulio ypatybės ir vietos</span><span class="sxs-lookup"><span data-stu-id="30dbe-117">Cart module properties and slots</span></span>

| <span data-ttu-id="30dbe-118">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="30dbe-118">Property</span></span> | <span data-ttu-id="30dbe-119">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="30dbe-119">Values</span></span> | <span data-ttu-id="30dbe-120">aprašymas</span><span class="sxs-lookup"><span data-stu-id="30dbe-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="30dbe-121">Antraštė</span><span class="sxs-lookup"><span data-stu-id="30dbe-121">Heading</span></span> | <span data-ttu-id="30dbe-122">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**)</span><span class="sxs-lookup"><span data-stu-id="30dbe-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="30dbe-123">Vežimėlio antraštė, tokia kaip „Apsipirkimo maišelis“ arba „Prekės jūsų vežimėlyje“.</span><span class="sxs-lookup"><span data-stu-id="30dbe-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="30dbe-124">Rodyti nėra sandėlyje klaidas</span><span class="sxs-lookup"><span data-stu-id="30dbe-124">Show out of stock errors</span></span> | <span data-ttu-id="30dbe-125">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="30dbe-125">**True** or **False**</span></span> | <span data-ttu-id="30dbe-126">Jei ši ypatybė nustatyta į **Tiesa**, vežimėlio puslapyje bus rodomos su atsargomis susijusios klaidos.</span><span class="sxs-lookup"><span data-stu-id="30dbe-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="30dbe-127">Rekomenduojame nustatyti šią ypatybę į **Tiesa**, jei atsargų tikrinimai yra taikomi svetainėje.</span><span class="sxs-lookup"><span data-stu-id="30dbe-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="30dbe-128">Rodyti eilutės prekių siuntimo mokesčius</span><span class="sxs-lookup"><span data-stu-id="30dbe-128">Show shipping charges for line items</span></span> | <span data-ttu-id="30dbe-129">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="30dbe-129">**True** or **False**</span></span> | <span data-ttu-id="30dbe-130">Jei ši ypatybė yra nustatytą į **Teisinga**, vežimėlio eilučių prekės rodys siuntimo mokesčius, jei tokia informacija yra prieinama.</span><span class="sxs-lookup"><span data-stu-id="30dbe-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="30dbe-131">Ši savybė nėra palaikoam „Fabrikam“ temoje, nes vartotojai pasirenka siuntimą tik išsiregistravimo sraute.</span><span class="sxs-lookup"><span data-stu-id="30dbe-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="30dbe-132">Nepaisant to, šią funkciją galima įjungti kituose darbo srautuose, jei tai taikoma.</span><span class="sxs-lookup"><span data-stu-id="30dbe-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="30dbe-133">Moduliai, kuriuos galima naudoti krepšelio modulyje</span><span class="sxs-lookup"><span data-stu-id="30dbe-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="30dbe-134">**Teksto blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę.</span><span class="sxs-lookup"><span data-stu-id="30dbe-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="30dbe-135">Pranešimai grindžiami turinio valdymo sistema (TVS).</span><span class="sxs-lookup"><span data-stu-id="30dbe-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="30dbe-136">Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="30dbe-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="30dbe-137">**Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="30dbe-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="30dbe-138">Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves.</span><span class="sxs-lookup"><span data-stu-id="30dbe-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="30dbe-139">Daugiau informacijos apie šį modulį žr. [Parduotuvės parinkiklio modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="30dbe-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="30dbe-140">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="30dbe-140">Module properties</span></span>

<span data-ttu-id="30dbe-141">Dalyje **Svetainės parametrai \> Plėtiniai** galima konfigūruoti toliau pateiktus krepšelio modulio parametrus:</span><span class="sxs-lookup"><span data-stu-id="30dbe-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="30dbe-142">**Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="30dbe-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="30dbe-143">Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.</span><span class="sxs-lookup"><span data-stu-id="30dbe-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="30dbe-144">**Atsargos** – norėdami gauti informacijos apie atsargų parametrų taikymą, žr. [Atsargų parametrų taikymas](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="30dbe-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="30dbe-145">**Grįžimas prie pirkimo** – ši ypatybė naudojama norint nurodyti saito **Grįžimas prie pirkimo** maršrutą.</span><span class="sxs-lookup"><span data-stu-id="30dbe-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="30dbe-146">Maršrutas gali būti sukonfigūruotas svetainės lygiu, leidžiant mažmeninės prekybos klientams grįžti į pagrindinį puslapį arba bet kurį kitą svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="30dbe-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="30dbe-147">„Commerce Scale Unit“ sąveika</span><span class="sxs-lookup"><span data-stu-id="30dbe-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="30dbe-148">Vežimėlio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas.</span><span class="sxs-lookup"><span data-stu-id="30dbe-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="30dbe-149">Visa informacija apie produktus iš „Commerce Scale Unit“ gaunama naudojant krepšelio ID iš naršyklės slapuko.</span><span class="sxs-lookup"><span data-stu-id="30dbe-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="30dbe-150">Krepšelio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="30dbe-150">Add a cart module to a page</span></span>

<span data-ttu-id="30dbe-151">Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="30dbe-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="30dbe-152">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="30dbe-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="30dbe-153">**Naujo puslapio fragmentas** teksto laukelyje, pasirinkite **Vežimėlis** modulį.</span><span class="sxs-lookup"><span data-stu-id="30dbe-153">In the **New page fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="30dbe-154">**Puslapio fragmento pavadinime** įveskite pavadinimą **Vežimėlio fragmentas** ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-154">Under **Page fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="30dbe-155">Pasirinkite vietą **Krepšelis**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="30dbe-156">Dešinėje pusėje esančioje ypatybių srityje pasirinkite pieštuko simbolį, į laukelį įveskite antraštės tekstą ir pasirinkite varnelės simbolį.</span><span class="sxs-lookup"><span data-stu-id="30dbe-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="30dbe-157">Vietoje **Krepšelis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="30dbe-158">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Parduotuvės parinkiklis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="30dbe-159">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="30dbe-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="30dbe-160">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="30dbe-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="30dbe-161">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="30dbe-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="30dbe-162">Išorės medyje pasirinkite **Kūno** vietą ir pasirinkite elipsę (**...**), tuomet pasirinkite **Įtraukti puslapio fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="30dbe-163">**Pasirinkite puslapio fragmentą** teksto laukelyje, pasirinkite **Vežimėlio fragmentas** fragmentą ir tuomet pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-163">In the **Select page fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="30dbe-164">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="30dbe-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="30dbe-165">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="30dbe-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="30dbe-166">Dialogo lange **Pasirinkti šabloną** pasirinkite anksčiau sukurtą šabloną, įveskite puslapio pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="30dbe-167">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="30dbe-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="30dbe-168">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="30dbe-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30dbe-169">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="30dbe-169">Additional resources</span></span>

[<span data-ttu-id="30dbe-170">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="30dbe-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="30dbe-171">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="30dbe-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="30dbe-172">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="30dbe-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="30dbe-173">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="30dbe-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="30dbe-174">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="30dbe-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="30dbe-175">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="30dbe-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="30dbe-176">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="30dbe-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="30dbe-177">Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="30dbe-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
