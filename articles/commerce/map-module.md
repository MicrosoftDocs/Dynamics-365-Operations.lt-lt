---
title: Žemėlapio modulis
description: Šis skyrius aprašo žemėlapio modulius ir tai, kaip konfigūruoti juos į „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 659211f3a74c38389f991cd2385366d175b0c7c0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020264"
---
# <a name="map-module"></a><span data-ttu-id="ddf40-103">Žemėlapio modulis</span><span class="sxs-lookup"><span data-stu-id="ddf40-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="ddf40-104">Šis skyrius aprašo žemėlapio modulius ir tai, kaip konfigūruoti juos į „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="ddf40-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ddf40-105">Žemėlapio modulis rodo parduotuvių vietas interaktyviame žemėlapyje, kuris yra sukurtas naudojant [„Bing Maps V8 Web Control“](/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="ddf40-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="ddf40-106">„Bing Maps“ API raktas yra reikalaujamas ir turi būti įtrauktas į bendrinamus parametrus komercijos štabo puslapyje</span><span class="sxs-lookup"><span data-stu-id="ddf40-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="ddf40-107">Žemėlapio moduliai suteikia įvairias peržiūras, tokias kaip kelio, oro, kelkraščio, kurias naudotojai gali pasirinkti tam, kad peržiūrėtų žemėlapio vietas.</span><span class="sxs-lookup"><span data-stu-id="ddf40-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="ddf40-108">Jie taip pat leidžia sąveiką tokią kaip priartinimas ir naudotojo vietos naudojimas.</span><span class="sxs-lookup"><span data-stu-id="ddf40-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="ddf40-109">Žemėlapio modulis dirba kartu su parduotuvės selektoriaus moduliu tam, kad nustatytų geografines parduotuvių vietas, kurios turi būti pažymėtos žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="ddf40-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="ddf40-110">Parduotuvės selektorius ir žemėlapio modeliai sąveikauja, kai naudotojas pasirenka parduotuvę viename iš šių modulių svetainės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="ddf40-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="ddf40-111">Žemėlapio moduliai gali būti išplėsti kitiems scenarijams, už sąveikos tarp parduotuvės selektoriaus modulių.</span><span class="sxs-lookup"><span data-stu-id="ddf40-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="ddf40-112">Nepaisant to, modulio tinkinimas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="ddf40-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="ddf40-113">Žemėlapio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.13 leidime.</span><span class="sxs-lookup"><span data-stu-id="ddf40-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="ddf40-114">Toliau pateiktas paveikslėlis rodo parduotuvės žemėlapio modulio pavyzdį, kuris yra naudojamas parduotuvės vietų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="ddf40-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Parduotuvės parinkiklio modulio pavyzdys](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="ddf40-116">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="ddf40-116">Module properties</span></span>

| <span data-ttu-id="ddf40-117">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ddf40-117">Property name</span></span>             | <span data-ttu-id="ddf40-118">Vertė</span><span class="sxs-lookup"><span data-stu-id="ddf40-118">Value</span></span>                 | <span data-ttu-id="ddf40-119">aprašymas</span><span class="sxs-lookup"><span data-stu-id="ddf40-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="ddf40-120">Antraštė</span><span class="sxs-lookup"><span data-stu-id="ddf40-120">Heading</span></span> | <span data-ttu-id="ddf40-121">Tekstas</span><span class="sxs-lookup"><span data-stu-id="ddf40-121">Text</span></span> | <span data-ttu-id="ddf40-122">Modulio antraštė.</span><span class="sxs-lookup"><span data-stu-id="ddf40-122">The heading for the module.</span></span> |
| <span data-ttu-id="ddf40-123">Stūmoklio parinktys: nustatytoji piktograma</span><span class="sxs-lookup"><span data-stu-id="ddf40-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="ddf40-124">Nuotrauka</span><span class="sxs-lookup"><span data-stu-id="ddf40-124">Image</span></span> | <span data-ttu-id="ddf40-125">Stūmoklio simbolio paveikslėlis naudojamas parduotuvėms rodomoms žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="ddf40-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="ddf40-126">Stūmoklio parinktys: aktyvi piktograma</span><span class="sxs-lookup"><span data-stu-id="ddf40-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="ddf40-127">Nuotrauka</span><span class="sxs-lookup"><span data-stu-id="ddf40-127">Image</span></span> | <span data-ttu-id="ddf40-128">Stūmoklio simbolio paveikslėlis naudojamas parduotuvei pasirinktai žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="ddf40-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="ddf40-129">Stūmoklio parinktys: nustatytosios piktogramos spalva</span><span class="sxs-lookup"><span data-stu-id="ddf40-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="ddf40-130">Maskavimo pynė</span><span class="sxs-lookup"><span data-stu-id="ddf40-130">Character string</span></span> | <span data-ttu-id="ddf40-131">Tekstas ir šešioliktainės vertės stūmoklio simbolio spalvai žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="ddf40-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="ddf40-132">Stūmoklio parinktys: aktyvi piktogramos spalva</span><span class="sxs-lookup"><span data-stu-id="ddf40-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="ddf40-133">Maskavimo pynė</span><span class="sxs-lookup"><span data-stu-id="ddf40-133">Character string</span></span> | <span data-ttu-id="ddf40-134">Tekstas ir šešioliktainės vertės pasirinkto stūmoklio simbolio spalvai žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="ddf40-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="ddf40-135">Rodyti rodyklę</span><span class="sxs-lookup"><span data-stu-id="ddf40-135">Show index</span></span> | <span data-ttu-id="ddf40-136">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="ddf40-136">**True** or **False**</span></span> | <span data-ttu-id="ddf40-137">Jei ši ypatybė yra nustatytą į **Teisingą**, visi stūmoklio simboliai rodantys parduotuvę bus rodomi turinyje.</span><span class="sxs-lookup"><span data-stu-id="ddf40-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="ddf40-138">Šis turinys atitiks turinį sąrašo peržiūroje, kurioje parduotuvės selektoriaus modulis yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="ddf40-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="ddf40-139">Įtraukti leidžiamą žemėlapio kūrimo URL į svetainės turinio apsaugos politikos gaires</span><span class="sxs-lookup"><span data-stu-id="ddf40-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="ddf40-140">Tam, kad žemėlapių modulis sąveikautų su „Bing Maps“, turite užtikrinti, kad tolesni žemėlapio URL yra leidžiami jūsų saito turinio saugos politikoje (CSP).</span><span class="sxs-lookup"><span data-stu-id="ddf40-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="ddf40-141">Šis nustatymas yra atliekamas komercijos svetainės kūrimo įrankyje įtraukiant leidžiamus URL į skirtingas svetainės CSP gaires (pavyzdžiui, **img-src**).</span><span class="sxs-lookup"><span data-stu-id="ddf40-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="ddf40-142">Dėl platesnės informacijos, žr. [Turinio saugos politika](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="ddf40-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="ddf40-143">Į **connect-src** direktyvą, įtraukite **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="ddf40-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="ddf40-144">Į **img-src** direktyvą, įtraukite **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="ddf40-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="ddf40-145">Į **script-src** direktyvą, įtraukite **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="ddf40-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="ddf40-146">Į **script style-src** direktyvą, įtraukite **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="ddf40-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="ddf40-147">Įtraukti žemėlapio modulį į puslapį</span><span class="sxs-lookup"><span data-stu-id="ddf40-147">Add a map module to a page</span></span>

<span data-ttu-id="ddf40-148">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti žemėlapio modulį puslapyje, žr. [Parduotuvės pasirinkimo modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="ddf40-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="ddf40-149">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="ddf40-149">Additional resources</span></span>

[<span data-ttu-id="ddf40-150">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="ddf40-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ddf40-151">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="ddf40-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ddf40-152">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="ddf40-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ddf40-153">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="ddf40-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="ddf40-154">„Bing“ žemėlapių valdymas jūsų organizacijoje</span><span class="sxs-lookup"><span data-stu-id="ddf40-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="ddf40-155">„Bing Maps V8 Web Control“</span><span class="sxs-lookup"><span data-stu-id="ddf40-155">Bing Maps V8 Web Control</span></span>](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]