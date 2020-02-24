---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025441"
---
# <a name="cart-module"></a><span data-ttu-id="3a887-103">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="3a887-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3a887-104">Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="3a887-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3a887-105">Peržiūrėti</span><span class="sxs-lookup"><span data-stu-id="3a887-105">Overview</span></span>

<span data-ttu-id="3a887-106">Krepšelio modulis naudojamas norint parodyti prekes, kurios buvo įtrauktos į krepšelį, prieš klientui išsiregistruojant.</span><span class="sxs-lookup"><span data-stu-id="3a887-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="3a887-107">Pavyzdžiui, jame yra visos į krepšelį įtrauktos prekės ir užsakymo suvestinė.</span><span class="sxs-lookup"><span data-stu-id="3a887-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="3a887-108">Be to, jis leidžia klientui taikyti arba pašalinti akcijų kodus.</span><span class="sxs-lookup"><span data-stu-id="3a887-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="3a887-109">Krepšelio modulis palaiko prisijungusiųjų išsiregistravimą ir svečių išsiregistravimą.</span><span class="sxs-lookup"><span data-stu-id="3a887-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="3a887-110">Jis taip pat palaiko saitą **Grįžti prie pirkimo**.</span><span class="sxs-lookup"><span data-stu-id="3a887-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="3a887-111">Galite konfigūruoti šio saito maršrutą eidami į **Svetainės parametrai \> Plėtiniai \> Maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="3a887-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="3a887-112">Krepšelio modulis duomenis generuoja pagal krepšelio ID.</span><span class="sxs-lookup"><span data-stu-id="3a887-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="3a887-113">Krepšelio ID yra naršyklės slapukas, pasiekiamas visoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="3a887-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="3a887-114">Krepšelio modulio ypatybės ir vietos</span><span class="sxs-lookup"><span data-stu-id="3a887-114">Cart module properties and slots</span></span>

<span data-ttu-id="3a887-115">Krepšelio modulyje yra ypatybė **Antraštė**, kurią galima nustatyti kaip **Pirkinių krepšelis** ir **Jūsų krepšelio prekės**.</span><span class="sxs-lookup"><span data-stu-id="3a887-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="3a887-116">Moduliai, kuriuos galima naudoti krepšelio modulyje</span><span class="sxs-lookup"><span data-stu-id="3a887-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="3a887-117">**Teksto blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę.</span><span class="sxs-lookup"><span data-stu-id="3a887-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="3a887-118">Pranešimai grindžiami turinio valdymo sistema (TVS).</span><span class="sxs-lookup"><span data-stu-id="3a887-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="3a887-119">Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="3a887-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="3a887-120">**Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="3a887-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="3a887-121">Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves.</span><span class="sxs-lookup"><span data-stu-id="3a887-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="3a887-122">Parduotuvės parinkiklio modulis yra integruotas su „Bing“ žemėlapių geokodavimo programos programavimo sąsaja (API), kad vieta būtų konvertuojama į platumą ir ilgumą.</span><span class="sxs-lookup"><span data-stu-id="3a887-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="3a887-123">Reikalingas „Bing“ žemėlapių API raktas ir jį reikia įtraukti į mažmeninės prekybos bendrinamus parametrus puslapyje „Dynamics 365 Retail“.</span><span class="sxs-lookup"><span data-stu-id="3a887-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="3a887-124">Šis modulis palaiko dvi ypatybes – **Ieškos spindulys** ir **Paslaugų saito sąlygos**.</span><span class="sxs-lookup"><span data-stu-id="3a887-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="3a887-125">Ypatybė **Ieškos spindulys** nurodo parduotuvių ieškos spindulį, išreikštą myliomis.</span><span class="sxs-lookup"><span data-stu-id="3a887-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="3a887-126">Jei nenurodyta jokia reikšmė, naudojamas numatytasis ieškos spindulys, kuris yra 50 mylių.</span><span class="sxs-lookup"><span data-stu-id="3a887-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="3a887-127">Jei naudojami „Bing“ žemėlapiai arba bet kokia išorinė paslauga, ypatybė **Paslaugos saito sąlygos** gali būti naudojama norint pateikti saitą į paslaugos sąlygas.</span><span class="sxs-lookup"><span data-stu-id="3a887-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="3a887-128">Paslaugos saito sąlygų reikia „Bing“ žemėlapių paslaugai.</span><span class="sxs-lookup"><span data-stu-id="3a887-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="3a887-129">Krepšelio modulio parametrai</span><span class="sxs-lookup"><span data-stu-id="3a887-129">Cart module settings</span></span>

<span data-ttu-id="3a887-130">Krepšelio moduliai turi šiuos parametrus, kuriuos galima konfigūruoti einant į **Svetainės parametrai \> Plėtiniai**:</span><span class="sxs-lookup"><span data-stu-id="3a887-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="3a887-131">**Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="3a887-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="3a887-132">Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.</span><span class="sxs-lookup"><span data-stu-id="3a887-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="3a887-133">**Atsargų patikra** – kai reikšmė nustatoma kaip **Teisinga**, prekė į krepšelį įtraukiama tik tada, kai pirkimo langelio modulis užtikrina, kad yra jos atsargų.</span><span class="sxs-lookup"><span data-stu-id="3a887-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="3a887-134">Ši atsargų patikra atliekama tiek tose situacijose, kai prekė bus siunčiama, tiek tose situacijose, kai ji bus atsiimama iš parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="3a887-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="3a887-135">Jei reikšmė nustatoma kaip **Klaidinga**, prieš prekę įtraukiant į krepšelį ir pateikiant užsakymą atsargos nepatikrinamos.</span><span class="sxs-lookup"><span data-stu-id="3a887-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="3a887-136">**Atsargų buferis** – ši ypatybė naudojama norint nurodyti atsargų buferio skaičių.</span><span class="sxs-lookup"><span data-stu-id="3a887-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="3a887-137">Atsargos tvarkomos realiuoju laiku ir dideliam klientų skaičiui teikiant užsakymus gali būti sudėtinga turėti tikslų atsargų skaičių.</span><span class="sxs-lookup"><span data-stu-id="3a887-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="3a887-138">Jei, tikrinant atsargas, jų yra mažiau nei buferio suma, laikoma, kad produkto atsargų nėra.</span><span class="sxs-lookup"><span data-stu-id="3a887-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="3a887-139">Todėl greitai pardudodant keliais kanalais, kai ne visiškai sinchronizuojamas atsargų kiekis, yra mažiau rizikos, kad bus parduota prekė, kurios atsargų nėra.</span><span class="sxs-lookup"><span data-stu-id="3a887-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="3a887-140">**Grįžimas prie pirkimo** – ši ypatybė naudojama norint nurodyti saito **Grįžimas prie pirkimo** maršrutą.</span><span class="sxs-lookup"><span data-stu-id="3a887-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="3a887-141">Šis maršrutas gali būti sukonfigūruotas svetainės lygiu.</span><span class="sxs-lookup"><span data-stu-id="3a887-141">This route can be configured at the site level.</span></span> <span data-ttu-id="3a887-142">Naudojant šią konfigūraciją, mažmeninės prekybos klientai gali grįžta į pagrindinį puslapį arba bet kurį kitą svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="3a887-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="3a887-143">„Commerce Scale Unit“ sąveika</span><span class="sxs-lookup"><span data-stu-id="3a887-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="3a887-144">Vežimėlio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas.</span><span class="sxs-lookup"><span data-stu-id="3a887-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="3a887-145">Visa informacija apie produktus iš „Commerce Scale Unit“ gaunama naudojant krepšelio ID iš naršyklės slapuko.</span><span class="sxs-lookup"><span data-stu-id="3a887-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="3a887-146">Krepšelio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="3a887-146">Add a cart module to a page</span></span>

<span data-ttu-id="3a887-147">Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3a887-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3a887-148">Sukurkite fragmentą pavadinimu **Krepšelio fragmentas** ir į jį įtraukite krepšelio modulį.</span><span class="sxs-lookup"><span data-stu-id="3a887-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="3a887-149">Į krepšelio modulį įtraukite antraštę.</span><span class="sxs-lookup"><span data-stu-id="3a887-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="3a887-150">Įtraukite parduotuvės parinkiklio modulį į krepšelio modulį.</span><span class="sxs-lookup"><span data-stu-id="3a887-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="3a887-151">Įrašykite fragmentą, baikite redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="3a887-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="3a887-152">Sukurkite šabloną pavadinimu **Krepšelio šablonas** ir į jį įtraukite ką tik sukurtą krepšelio fragmentą.</span><span class="sxs-lookup"><span data-stu-id="3a887-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="3a887-153">Įrašykite šabloną, baikite redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="3a887-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="3a887-154">Sukurkite puslapį, kuriame naudojamas naujasis šablonas.</span><span class="sxs-lookup"><span data-stu-id="3a887-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="3a887-155">Puslapį įrašykite ir peržiūrėkite.</span><span class="sxs-lookup"><span data-stu-id="3a887-155">Save and preview the page.</span></span>
1. <span data-ttu-id="3a887-156">Baikite puslapio redagavimą ir publikuokite.</span><span class="sxs-lookup"><span data-stu-id="3a887-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a887-157">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3a887-157">Additional resources</span></span>

[<span data-ttu-id="3a887-158">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="3a887-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3a887-159">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="3a887-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3a887-160">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="3a887-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3a887-161">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="3a887-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3a887-162">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="3a887-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3a887-163">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="3a887-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3a887-164">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="3a887-164">Footer module</span></span>](author-footer-module.md)
