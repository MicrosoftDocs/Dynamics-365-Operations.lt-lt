---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ec8e89ed82bcdffdc21e62d24ad8c8a7d939cdf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797868"
---
# <a name="cart-module"></a><span data-ttu-id="062e1-103">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="062e1-104">Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="062e1-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="062e1-105">Krepšelio modulyje rodomos prekes, kurios buvo įtrauktos į krepšelį, prieš klientui išsiregistruojant.</span><span class="sxs-lookup"><span data-stu-id="062e1-105">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="062e1-106">Šiame modulyje taip pat rodoma užsakymo suvestinė, be to, klientui leidžiama taikyti arba pašalinti reklaminius kodus.</span><span class="sxs-lookup"><span data-stu-id="062e1-106">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="062e1-107">Krepšelio modulis palaiko prisijungusiųjų išsiregistravimą ir svečių išsiregistravimą.</span><span class="sxs-lookup"><span data-stu-id="062e1-107">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="062e1-108">Jis taip pat palaiko saitą **Grįžti prie pirkimo**.</span><span class="sxs-lookup"><span data-stu-id="062e1-108">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="062e1-109">Galite konfigūruoti šio saito maršrutą eidami į **Svetainės parametrai \> Plėtiniai \> Maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="062e1-109">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="062e1-110">Krepšelio modulis generuoja duomenis pagal krepšelio ID, kuris yra naršyklės slapukas, pasiekiamas visoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="062e1-110">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="062e1-111">Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="062e1-111">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Krepšelio modulio, esančio „Fabrikam” svetainėje, pavyzdys](./media/cart2.PNG)

<span data-ttu-id="062e1-113">Toliau pateiktame paveikslėlyje parodytas „Fabrikam“ svetainėje esančio krepšelio puslapio pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="062e1-113">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="062e1-114">Šiame pavyzdyje yra eilutės prekės paėmimo mokestis.</span><span class="sxs-lookup"><span data-stu-id="062e1-114">In this example, there is a handling fee for a line item.</span></span>

![Krepšelio modulio su eilutės prekės tvarkymo mokesčiu pavyzdys](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="062e1-116">Krepšelio modulio ypatybės ir vietos</span><span class="sxs-lookup"><span data-stu-id="062e1-116">Cart module properties and slots</span></span>

| <span data-ttu-id="062e1-117">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="062e1-117">Property</span></span> | <span data-ttu-id="062e1-118">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="062e1-118">Values</span></span> | <span data-ttu-id="062e1-119">aprašymas</span><span class="sxs-lookup"><span data-stu-id="062e1-119">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="062e1-120">Antraštė</span><span class="sxs-lookup"><span data-stu-id="062e1-120">Heading</span></span> | <span data-ttu-id="062e1-121">Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**)</span><span class="sxs-lookup"><span data-stu-id="062e1-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="062e1-122">Vežimėlio antraštė, tokia kaip „Apsipirkimo maišelis“ arba „Prekės jūsų vežimėlyje“.</span><span class="sxs-lookup"><span data-stu-id="062e1-122">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="062e1-123">Rodyti nėra sandėlyje klaidas</span><span class="sxs-lookup"><span data-stu-id="062e1-123">Show out of stock errors</span></span> | <span data-ttu-id="062e1-124">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="062e1-124">**True** or **False**</span></span> | <span data-ttu-id="062e1-125">Jei ši ypatybė nustatyta į **Tiesa**, vežimėlio puslapyje bus rodomos su atsargomis susijusios klaidos.</span><span class="sxs-lookup"><span data-stu-id="062e1-125">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="062e1-126">Rekomenduojame nustatyti šią ypatybę į **Tiesa**, jei atsargų tikrinimai yra taikomi svetainėje.</span><span class="sxs-lookup"><span data-stu-id="062e1-126">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="062e1-127">Rodyti eilutės prekių siuntimo mokesčius</span><span class="sxs-lookup"><span data-stu-id="062e1-127">Show shipping charges for line items</span></span> | <span data-ttu-id="062e1-128">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="062e1-128">**True** or **False**</span></span> | <span data-ttu-id="062e1-129">Jei ši ypatybė yra nustatytą į **Teisinga**, vežimėlio eilučių prekės rodys siuntimo mokesčius, jei tokia informacija yra prieinama.</span><span class="sxs-lookup"><span data-stu-id="062e1-129">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="062e1-130">Ši savybė nėra palaikoma „Fabrikam“ temoje, nes vartotojai pasirenka siuntimą tik išsiregistravimo sraute.</span><span class="sxs-lookup"><span data-stu-id="062e1-130">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="062e1-131">Nepaisant to, šią funkciją galima įjungti kituose darbo srautuose, jei tai taikoma.</span><span class="sxs-lookup"><span data-stu-id="062e1-131">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="062e1-132">Rodyti galimas akcijas</span><span class="sxs-lookup"><span data-stu-id="062e1-132">Show available promotions</span></span>| <span data-ttu-id="062e1-133">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="062e1-133">**True** or **False**</span></span> | <span data-ttu-id="062e1-134">Jei ši ypatybė nustatyta į **Taip**, vežimėlis rodys prieinamas akcijas pagal prekes vežimėlyje.</span><span class="sxs-lookup"><span data-stu-id="062e1-134">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="062e1-135">Ši galimybė yra prieinama „Dynamics 365 Commerce“ 10.0.16 leidime.</span><span class="sxs-lookup"><span data-stu-id="062e1-135">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="062e1-136">Moduliai, kuriuos galima naudoti krepšelio modulyje</span><span class="sxs-lookup"><span data-stu-id="062e1-136">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="062e1-137">**Teksto blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę.</span><span class="sxs-lookup"><span data-stu-id="062e1-137">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="062e1-138">Pranešimai grindžiami turinio valdymo sistema (TVS).</span><span class="sxs-lookup"><span data-stu-id="062e1-138">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="062e1-139">Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="062e1-139">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="062e1-140">**Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="062e1-140">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="062e1-141">Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves.</span><span class="sxs-lookup"><span data-stu-id="062e1-141">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="062e1-142">Daugiau informacijos apie šį modulį žr. [Parduotuvės parinkiklio modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="062e1-142">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="062e1-143">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="062e1-143">Module properties</span></span>

<span data-ttu-id="062e1-144">Dalyje **Svetainės parametrai \> Plėtiniai** galima konfigūruoti toliau pateiktus krepšelio modulio parametrus:</span><span class="sxs-lookup"><span data-stu-id="062e1-144">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="062e1-145">**Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="062e1-145">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="062e1-146">Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.</span><span class="sxs-lookup"><span data-stu-id="062e1-146">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="062e1-147">**Atsargos** – norėdami gauti informacijos apie atsargų parametrų taikymą, žr. [Atsargų parametrų taikymas](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="062e1-147">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="062e1-148">**Grįžimas prie pirkimo** – ši ypatybė naudojama norint nurodyti saito **Grįžimas prie pirkimo** maršrutą.</span><span class="sxs-lookup"><span data-stu-id="062e1-148">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="062e1-149">Maršrutas gali būti sukonfigūruotas svetainės lygiu, leidžiant mažmeninės prekybos klientams grįžti į pagrindinį puslapį arba bet kurį kitą svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="062e1-149">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="062e1-150">„Dynamics 365 Commerce” 10.0.14 ir naujesniame leidime krepšelio prekės yra sutelkiamos pagal parametrus, apibrėžtus „Commerce Headquarters” interneto parduotuvės internetinių funkcijų šablone.</span><span class="sxs-lookup"><span data-stu-id="062e1-150">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="062e1-151">Daugiau informacijos apie tai, kaip kurti internetinių funkcijų šabloną ir nustatyti ypatybes, reikalingas telkimui, žr. [Internetinių funkcijų šablono kūrimas](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="062e1-151">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="062e1-152">„Commerce Scale Unit“ sąveika</span><span class="sxs-lookup"><span data-stu-id="062e1-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="062e1-153">Vežimėlio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas.</span><span class="sxs-lookup"><span data-stu-id="062e1-153">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="062e1-154">Visa informacija apie produktus iš „Commerce Scale Unit“ gaunama naudojant krepšelio ID iš naršyklės slapuko.</span><span class="sxs-lookup"><span data-stu-id="062e1-154">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="062e1-155">Krepšelio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="062e1-155">Add a cart module to a page</span></span>

<span data-ttu-id="062e1-156">Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="062e1-156">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="062e1-157">Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.</span><span class="sxs-lookup"><span data-stu-id="062e1-157">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="062e1-158">Dialogo lange **Naujas fragmentas** pasirinkite **Krepšelio** modulį.</span><span class="sxs-lookup"><span data-stu-id="062e1-158">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="062e1-159">Dalyje **Fragmento pavadinimas** įveskite pavadinimą **Krepšelio fragmentas** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="062e1-159">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="062e1-160">Pasirinkite vietą **Krepšelis**.</span><span class="sxs-lookup"><span data-stu-id="062e1-160">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="062e1-161">Dešinėje pusėje esančioje ypatybių srityje pasirinkite pieštuko simbolį, į laukelį įveskite antraštės tekstą ir pasirinkite varnelės simbolį.</span><span class="sxs-lookup"><span data-stu-id="062e1-161">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="062e1-162">Vietoje **Krepšelis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="062e1-162">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="062e1-163">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Parduotuvės parinkiklis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="062e1-163">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="062e1-164">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="062e1-164">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="062e1-165">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="062e1-165">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="062e1-166">Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="062e1-166">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="062e1-167">Struktūros medyje pasirinkite vietą **Pagrindinė dalis**, pasirinkite daugtaškį (**...**), tada – **Įtraukti fragmentą**.</span><span class="sxs-lookup"><span data-stu-id="062e1-167">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="062e1-168">Dialogo lange **Pasirinkti fragmentą** pasirinkite **Krepšelio fragmentas** fragmentą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="062e1-168">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="062e1-169">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="062e1-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="062e1-170">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="062e1-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="062e1-171">Dialogo lange **Pasirinkti šabloną** pasirinkite anksčiau sukurtą šabloną, įveskite puslapio pavadinimą ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="062e1-171">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="062e1-172">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="062e1-172">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="062e1-173">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="062e1-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="062e1-174">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="062e1-174">Additional resources</span></span>

[<span data-ttu-id="062e1-175">Krepšelio piktogramos modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-175">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="062e1-176">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-176">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="062e1-177">Mokėjimo modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-177">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="062e1-178">Siuntimo adreso modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-178">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="062e1-179">Pristatymo parinkčių modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-179">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="062e1-180">Paėmimo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-180">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="062e1-181">Išsamios užsakymo informacijos modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-181">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="062e1-182">Dovanų kortelės modulis</span><span class="sxs-lookup"><span data-stu-id="062e1-182">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="062e1-183">Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas</span><span class="sxs-lookup"><span data-stu-id="062e1-183">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="062e1-184">Internetinių funkcijų šablono kūrimas</span><span class="sxs-lookup"><span data-stu-id="062e1-184">Create an online functionality profile</span></span>](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]