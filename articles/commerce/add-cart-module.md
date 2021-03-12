---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: abb9909c03577763ff7e6242c9395a58159df6ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985984"
---
# <a name="cart-module"></a><span data-ttu-id="7bb18-103">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7bb18-104">Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="7bb18-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7bb18-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="7bb18-105">Overview</span></span>

<span data-ttu-id="7bb18-106">Krepšelio modulyje rodomos prekes, kurios buvo įtrauktos į krepšelį, prieš klientui išsiregistruojant.</span><span class="sxs-lookup"><span data-stu-id="7bb18-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="7bb18-107">Šiame modulyje taip pat rodoma užsakymo suvestinė, be to, klientui leidžiama taikyti arba pašalinti reklaminius kodus.</span><span class="sxs-lookup"><span data-stu-id="7bb18-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="7bb18-108">Krepšelio modulis palaiko prisijungusiųjų išsiregistravimą ir svečių išsiregistravimą.</span><span class="sxs-lookup"><span data-stu-id="7bb18-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="7bb18-109">Jis taip pat palaiko saitą **Grįžti prie pirkimo**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="7bb18-110">Galite konfigūruoti šio saito maršrutą eidami į **Svetainės parametrai \> Plėtiniai \> Maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="7bb18-111">Krepšelio modulis generuoja duomenis pagal krepšelio ID, kuris yra naršyklės slapukas, pasiekiamas visoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="7bb18-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="7bb18-112">Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7bb18-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Krepšelio modulio, esančio „Fabrikam” svetainėje, pavyzdys](./media/cart2.PNG)

<span data-ttu-id="7bb18-114">Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="7bb18-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="7bb18-115">Šiame pavyzdyje yra eilutės prekės paėmimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="7bb18-115">In this example, there is a handling fee for a line item.</span></span>

![Krepšelio modulio su eilutės prekės tvarkymo mokesčiu pavyzdys](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="7bb18-117">Krepšelio modulio ypatybės ir vietos</span><span class="sxs-lookup"><span data-stu-id="7bb18-117">Cart module properties and slots</span></span>

| <span data-ttu-id="7bb18-118">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="7bb18-118">Property</span></span> | <span data-ttu-id="7bb18-119">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="7bb18-119">Values</span></span> | <span data-ttu-id="7bb18-120">aprašymas</span><span class="sxs-lookup"><span data-stu-id="7bb18-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="7bb18-121">Antraštė</span><span class="sxs-lookup"><span data-stu-id="7bb18-121">Heading</span></span> | <span data-ttu-id="7bb18-122">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**)</span><span class="sxs-lookup"><span data-stu-id="7bb18-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="7bb18-123">Vežimėlio antraštė, tokia kaip „Apsipirkimo maišelis“ arba „Prekės jūsų vežimėlyje“.</span><span class="sxs-lookup"><span data-stu-id="7bb18-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="7bb18-124">Rodyti nėra sandėlyje klaidas</span><span class="sxs-lookup"><span data-stu-id="7bb18-124">Show out of stock errors</span></span> | <span data-ttu-id="7bb18-125">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="7bb18-125">**True** or **False**</span></span> | <span data-ttu-id="7bb18-126">Jei ši ypatybė nustatyta į **Tiesa**, vežimėlio puslapyje bus rodomos su atsargomis susijusios klaidos.</span><span class="sxs-lookup"><span data-stu-id="7bb18-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="7bb18-127">Rekomenduojame nustatyti šią ypatybę į **Tiesa**, jei atsargų tikrinimai yra taikomi svetainėje.</span><span class="sxs-lookup"><span data-stu-id="7bb18-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="7bb18-128">Rodyti eilutės prekių siuntimo mokesčius</span><span class="sxs-lookup"><span data-stu-id="7bb18-128">Show shipping charges for line items</span></span> | <span data-ttu-id="7bb18-129">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="7bb18-129">**True** or **False**</span></span> | <span data-ttu-id="7bb18-130">Jei ši ypatybė yra nustatytą į **Teisinga**, vežimėlio eilučių prekės rodys siuntimo mokesčius, jei tokia informacija yra prieinama.</span><span class="sxs-lookup"><span data-stu-id="7bb18-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="7bb18-131">Ši savybė nėra palaikoam „Fabrikam“ temoje, nes vartotojai pasirenka siuntimą tik išsiregistravimo sraute.</span><span class="sxs-lookup"><span data-stu-id="7bb18-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="7bb18-132">Nepaisant to, šią funkciją galima įjungti kituose darbo srautuose, jei tai taikoma.</span><span class="sxs-lookup"><span data-stu-id="7bb18-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="7bb18-133">Rodyti galimas akcijas</span><span class="sxs-lookup"><span data-stu-id="7bb18-133">Show available promotions</span></span>| <span data-ttu-id="7bb18-134">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="7bb18-134">**True** or **False**</span></span> | <span data-ttu-id="7bb18-135">Jei ši ypatybė nustatyta į **Taip**, vežimėlis rodys prieinamas akcijas pagal prekes vežimėlyje.</span><span class="sxs-lookup"><span data-stu-id="7bb18-135">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="7bb18-136">Ši galimybė yra prieinama „Dynamics 365 Commerce“ 10.0.16 leidime.</span><span class="sxs-lookup"><span data-stu-id="7bb18-136">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="7bb18-137">Moduliai, kuriuos galima naudoti krepšelio modulyje</span><span class="sxs-lookup"><span data-stu-id="7bb18-137">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="7bb18-138">**Teksto blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę.</span><span class="sxs-lookup"><span data-stu-id="7bb18-138">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="7bb18-139">Pranešimai grindžiami turinio valdymo sistema (TVS).</span><span class="sxs-lookup"><span data-stu-id="7bb18-139">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="7bb18-140">Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="7bb18-140">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="7bb18-141">**Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="7bb18-141">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="7bb18-142">Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves.</span><span class="sxs-lookup"><span data-stu-id="7bb18-142">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="7bb18-143">Daugiau informacijos apie šį modulį žr. [Parduotuvės parinkiklio modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="7bb18-143">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="7bb18-144">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="7bb18-144">Module properties</span></span>

<span data-ttu-id="7bb18-145">Dalyje **Svetainės parametrai \> Plėtiniai** galima konfigūruoti toliau pateiktus krepšelio modulio parametrus:</span><span class="sxs-lookup"><span data-stu-id="7bb18-145">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="7bb18-146">**Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="7bb18-146">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="7bb18-147">Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.</span><span class="sxs-lookup"><span data-stu-id="7bb18-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="7bb18-148">**Atsargos** – norėdami gauti informacijos apie atsargų parametrų taikymą, žr. [Atsargų parametrų taikymas](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7bb18-148">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="7bb18-149">**Grįžimas prie pirkimo** – ši ypatybė naudojama norint nurodyti saito **Grįžimas prie pirkimo** maršrutą.</span><span class="sxs-lookup"><span data-stu-id="7bb18-149">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="7bb18-150">Maršrutas gali būti sukonfigūruotas svetainės lygiu, leidžiant mažmeninės prekybos klientams grįžti į pagrindinį puslapį arba bet kurį kitą svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="7bb18-150">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bb18-151">„Dynamics 365 Commerce” 10.0.14 ir naujesniame leidime krepšelio prekės yra sutelkiamos pagal parametrus, apibrėžtus „Commerce Headquarters” interneto parduotuvės internetinių funkcijų šablone.</span><span class="sxs-lookup"><span data-stu-id="7bb18-151">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="7bb18-152">Daugiau informacijos apie tai, kaip kurti internetinių funkcijų šabloną ir nustatyti ypatybes, reikalingas telkimui, žr. [Internetinių funkcijų šablono kūrimas](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="7bb18-152">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="7bb18-153">„Commerce Scale Unit“ sąveika</span><span class="sxs-lookup"><span data-stu-id="7bb18-153">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="7bb18-154">Vežimėlio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas.</span><span class="sxs-lookup"><span data-stu-id="7bb18-154">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="7bb18-155">Visa informacija apie produktus iš „Commerce Scale Unit“ gaunama naudojant krepšelio ID iš naršyklės slapuko.</span><span class="sxs-lookup"><span data-stu-id="7bb18-155">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="7bb18-156">Krepšelio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="7bb18-156">Add a cart module to a page</span></span>

<span data-ttu-id="7bb18-157">Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7bb18-157">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7bb18-158">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="7bb18-158">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="7bb18-159">Dialogo lange **Naujas fragmentas** pasirinkite **Krepšelio** modulį.</span><span class="sxs-lookup"><span data-stu-id="7bb18-159">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="7bb18-160">Dalyje **Fragmento pavadinimas** įveskite pavadinimą **Krepšelio fragmentas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-160">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="7bb18-161">Pasirinkite vietą **Krepšelis**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-161">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="7bb18-162">Dešinėje pusėje esančioje ypatybių srityje pasirinkite pieštuko simbolį, į laukelį įveskite antraštės tekstą ir pasirinkite varnelės simbolį.</span><span class="sxs-lookup"><span data-stu-id="7bb18-162">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="7bb18-163">Vietoje **Krepšelis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-163">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7bb18-164">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Parduotuvės parinkiklis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-164">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7bb18-165">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="7bb18-165">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7bb18-166">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="7bb18-166">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7bb18-167">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7bb18-167">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="7bb18-168">Struktūros medyje pasirinkite vietą **Pagrindinė dalis**, pasirinkite daugtaškį (**...**), tada – **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-168">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="7bb18-169">Dialogo lange **Pasirinkti fragmentą** pasirinkite **Krepšelio fragmentas** fragmentą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-169">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7bb18-170">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="7bb18-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7bb18-171">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="7bb18-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="7bb18-172">Dialogo lange **Pasirinkti šabloną** pasirinkite anksčiau sukurtą šabloną, įveskite puslapio pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-172">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="7bb18-173">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="7bb18-173">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="7bb18-174">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="7bb18-174">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bb18-175">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="7bb18-175">Additional resources</span></span>

[<span data-ttu-id="7bb18-176">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-176">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7bb18-177">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7bb18-178">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-178">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="7bb18-179">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-179">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="7bb18-180">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-180">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="7bb18-181">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-181">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="7bb18-182">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-182">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7bb18-183">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="7bb18-183">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="7bb18-184">Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="7bb18-184">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="7bb18-185">Internetinių funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="7bb18-185">Create an online functionality profile</span></span>](online-functionality-profile.md)
