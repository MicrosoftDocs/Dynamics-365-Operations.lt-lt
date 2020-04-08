---
title: Krepšelio modulis
description: Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154022"
---
# <a name="cart-module"></a><span data-ttu-id="5e290-103">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="5e290-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5e290-104">Šioje temoje aprašomi krepšelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="5e290-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5e290-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="5e290-105">Overview</span></span>

<span data-ttu-id="5e290-106">Krepšelio modulyje rodomos prekes, kurios buvo įtrauktos į krepšelį, prieš klientui išsiregistruojant.</span><span class="sxs-lookup"><span data-stu-id="5e290-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="5e290-107">Šiame modulyje taip pat rodoma užsakymo suvestinė, be to, klientui leidžiama taikyti arba pašalinti reklaminius kodus.</span><span class="sxs-lookup"><span data-stu-id="5e290-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="5e290-108">Krepšelio modulis palaiko prisijungusiųjų išsiregistravimą ir svečių išsiregistravimą.</span><span class="sxs-lookup"><span data-stu-id="5e290-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="5e290-109">Jis taip pat palaiko saitą **Grįžti prie pirkimo**.</span><span class="sxs-lookup"><span data-stu-id="5e290-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="5e290-110">Galite konfigūruoti šio saito maršrutą eidami į **Svetainės parametrai \> Plėtiniai \> Maršrutai**.</span><span class="sxs-lookup"><span data-stu-id="5e290-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="5e290-111">Krepšelio modulis generuoja duomenis pagal krepšelio ID, kuris yra naršyklės slapukas, pasiekiamas visoje svetainėje.</span><span class="sxs-lookup"><span data-stu-id="5e290-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="5e290-112">Krepšelio modulio ypatybės ir vietos</span><span class="sxs-lookup"><span data-stu-id="5e290-112">Cart module properties and slots</span></span>

<span data-ttu-id="5e290-113">Krepšelio modulyje yra ypatybė **Antraštė**, kurią galima nustatyti kaip **Pirkinių krepšelis** ir **Jūsų krepšelio prekės**.</span><span class="sxs-lookup"><span data-stu-id="5e290-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="5e290-114">Moduliai, kuriuos galima naudoti krepšelio modulyje</span><span class="sxs-lookup"><span data-stu-id="5e290-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="5e290-115">**Teksto blokas** – šis modulis palaiko pasirinktinių pranešimų krepšelio modulyje galimybę.</span><span class="sxs-lookup"><span data-stu-id="5e290-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="5e290-116">Pranešimai grindžiami turinio valdymo sistema (TVS).</span><span class="sxs-lookup"><span data-stu-id="5e290-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="5e290-117">Galimą įtraukti bet kokį pranešimą, pvz., „Jei kyla problemų dėl užsakymo, kreipkitės numeriu 1-800-Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="5e290-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="5e290-118">**Parduotuvės parinkiklis** – naudojant šį modulį rodomas netoliese esančių parduotuvių, kuriose galima atsiimti prekę, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="5e290-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="5e290-119">Jis leidžia vartotojams įvesti vietą, kad surastų netoliese esančias parduotuves.</span><span class="sxs-lookup"><span data-stu-id="5e290-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="5e290-120">Daugiau informacijos apie šį modulį žr. [Parduotuvės parinkiklio modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="5e290-120">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="5e290-121">Krepšelio modulio parametrai</span><span class="sxs-lookup"><span data-stu-id="5e290-121">Cart module settings</span></span>

<span data-ttu-id="5e290-122">Krepšelio moduliai turi šiuos parametrus, kuriuos galima konfigūruoti einant į **Svetainės parametrai \> Plėtiniai**:</span><span class="sxs-lookup"><span data-stu-id="5e290-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="5e290-123">**Maksimalus kiekis** – ši ypatybė yra naudojama nurodyti maksimalų kiekvienos prekės skaičių, kurį galima įtraukti į krepšelį.</span><span class="sxs-lookup"><span data-stu-id="5e290-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="5e290-124">Pavyzdžiui, pardavėjas gali nuspręsti, kad vienos operacijos metu galima parduoti tik 10 kiekvieno produkto vienetų.</span><span class="sxs-lookup"><span data-stu-id="5e290-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="5e290-125">**Atsargų patikra** – kai reikšmė nustatoma kaip **Teisinga**, prekė į krepšelį įtraukiama tik tada, kai pirkimo langelio modulis užtikrina, kad yra jos atsargų.</span><span class="sxs-lookup"><span data-stu-id="5e290-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="5e290-126">Ši atsargų patikra atliekama tose situacijose, kai prekė bus siunčiama, ir situacijose, kai ji bus atsiimama iš parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="5e290-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="5e290-127">Jei reikšmė nustatoma kaip **Klaidinga**, prieš prekę įtraukiant į krepšelį ir pateikiant užsakymą atsargos nepatikrinamos.</span><span class="sxs-lookup"><span data-stu-id="5e290-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="5e290-128">**Atsargų buferis** – ši ypatybė naudojama norint nurodyti atsargų buferio skaičių.</span><span class="sxs-lookup"><span data-stu-id="5e290-128">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="5e290-129">Atsargos tvarkomos realiuoju laiku ir dideliam klientų skaičiui teikiant užsakymus gali būti sudėtinga turėti tikslų atsargų skaičių.</span><span class="sxs-lookup"><span data-stu-id="5e290-129">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="5e290-130">Jei, tikrinant atsargas, jų yra mažiau nei buferio suma, laikoma, kad produkto atsargų nėra.</span><span class="sxs-lookup"><span data-stu-id="5e290-130">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="5e290-131">Todėl greitai pardudodant keliais kanalais, kai ne visiškai sinchronizuojamas atsargų kiekis, yra mažiau rizikos, kad bus parduota prekė, kurios atsargų nėra.</span><span class="sxs-lookup"><span data-stu-id="5e290-131">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="5e290-132">**Grįžimas prie pirkimo** – ši ypatybė naudojama norint nurodyti saito **Grįžimas prie pirkimo** maršrutą.</span><span class="sxs-lookup"><span data-stu-id="5e290-132">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="5e290-133">Maršrutas gali būti sukonfigūruotas svetainės lygiu, leidžiant mažmeninės prekybos klientams grįžti į pagrindinį puslapį arba bet kurį kitą svetainės puslapį.</span><span class="sxs-lookup"><span data-stu-id="5e290-133">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="5e290-134">„Commerce Scale Unit“ sąveika</span><span class="sxs-lookup"><span data-stu-id="5e290-134">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="5e290-135">Vežimėlio modulis produkto informaciją gauna naudodamas „Commerce Scale Unit“ API sąsajas.</span><span class="sxs-lookup"><span data-stu-id="5e290-135">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="5e290-136">Visa informacija apie produktus iš „Commerce Scale Unit“ gaunama naudojant krepšelio ID iš naršyklės slapuko.</span><span class="sxs-lookup"><span data-stu-id="5e290-136">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="5e290-137">Krepšelio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="5e290-137">Add a cart module to a page</span></span>

<span data-ttu-id="5e290-138">Norėdami į naują puslapį įtraukti krepšelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5e290-138">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5e290-139">Sukurkite fragmentą pavadinimu **Krepšelio fragmentas** ir į naują fragmentą įtraukite krepšelio modulį.</span><span class="sxs-lookup"><span data-stu-id="5e290-139">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="5e290-140">Į krepšelio modulį įtraukite antraštę.</span><span class="sxs-lookup"><span data-stu-id="5e290-140">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="5e290-141">Įtraukite parduotuvės parinkiklio modulį į krepšelio modulį.</span><span class="sxs-lookup"><span data-stu-id="5e290-141">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="5e290-142">Įrašykite fragmentą, baikite redagavimą, tada publikuokite fragmentą.</span><span class="sxs-lookup"><span data-stu-id="5e290-142">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="5e290-143">Sukurkite šabloną pavadinimu **Krepšelio šablonas** ir įtraukite ką tik sukurtą krepšelio fragmentą.</span><span class="sxs-lookup"><span data-stu-id="5e290-143">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="5e290-144">Įrašykite šabloną, baikite redagavimą, tada publikuokite šabloną.</span><span class="sxs-lookup"><span data-stu-id="5e290-144">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="5e290-145">Sukurkite puslapį, kuriame naudojamas naujasis šablonas.</span><span class="sxs-lookup"><span data-stu-id="5e290-145">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="5e290-146">Puslapį įrašykite ir peržiūrėkite.</span><span class="sxs-lookup"><span data-stu-id="5e290-146">Save and preview the page.</span></span>
1. <span data-ttu-id="5e290-147">Baikite redaguoti puslapį, tada jį paskelbkite.</span><span class="sxs-lookup"><span data-stu-id="5e290-147">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5e290-148">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5e290-148">Additional resources</span></span>

[<span data-ttu-id="5e290-149">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="5e290-149">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5e290-150">Konteinerio modulis</span><span class="sxs-lookup"><span data-stu-id="5e290-150">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5e290-151">Parduotuvės parinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="5e290-151">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="5e290-152">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="5e290-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5e290-153">Pirkimo užbaigimo modulis</span><span class="sxs-lookup"><span data-stu-id="5e290-153">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5e290-154">Užsakymo patvirtinimo modulis</span><span class="sxs-lookup"><span data-stu-id="5e290-154">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5e290-155">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="5e290-155">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5e290-156">Poraštės modulis</span><span class="sxs-lookup"><span data-stu-id="5e290-156">Footer module</span></span>](author-footer-module.md)
