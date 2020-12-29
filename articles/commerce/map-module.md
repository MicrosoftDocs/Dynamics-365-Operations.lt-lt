---
title: Žemėlapio modulis
description: Šis skyrius aprašo žemėlapio modulius ir tai, kaip konfigūruoti juos į „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: af6aedb6c0112822155c6d855909578a927d1c2c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665425"
---
# <a name="map-module"></a><span data-ttu-id="61082-103">Žemėlapio modulis</span><span class="sxs-lookup"><span data-stu-id="61082-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="61082-104">Šis skyrius aprašo žemėlapio modulius ir tai, kaip konfigūruoti juos į „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="61082-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="61082-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="61082-105">Overview</span></span>

<span data-ttu-id="61082-106">Žemėlapio modulis rodo parduotuvių vietas interaktyviame žemėlapyje, kuris yra sukurtas naudojant [„Bing Maps V8 Web Control“](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="61082-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="61082-107">„Bing Maps“ API raktas yra reikalaujamas ir turi būti įtrauktas į bendrinamus parametrus komercijos štabo puslapyje</span><span class="sxs-lookup"><span data-stu-id="61082-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="61082-108">Žemėlapio moduliai suteikia įvairias peržiūras, tokias kaip kelio, oro, kelkraščio, kurias naudotojai gali pasirinkti tam, kad peržiūrėtų žemėlapio vietas.</span><span class="sxs-lookup"><span data-stu-id="61082-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="61082-109">Jie taip pat leidžia sąvaiką tokią kaip priartinimas ir naudotojo vietos naudojimas.</span><span class="sxs-lookup"><span data-stu-id="61082-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="61082-110">Žemėlapio modulis dirba kartu su parduotuvės sleketoriaus moduliu tam, kad nustatytų geografines parduotuvių vietas, kurios turi būti pažymėtos žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="61082-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="61082-111">Parduotuvės selektorius ir žemėlapio modeliai sąveikauja, kai naudotojas pasirenka parduotuvę viename iš šių modulių svetainės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="61082-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="61082-112">Žemėlapio moduliai gali būti išplėsti kitiems scenarijams, už sąveikos tarp parduotuvės selektoriaus modulių.</span><span class="sxs-lookup"><span data-stu-id="61082-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="61082-113">Nepaisant to, modulio tinkinimas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="61082-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="61082-114">Žemėlapio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.13 leidime.</span><span class="sxs-lookup"><span data-stu-id="61082-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="61082-115">Toliau pateiktas paveikslėlis rodo parduotuvės žemėlapio modulio pavyzdį, kuris yra naudojamas parduotuvės vietų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="61082-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Parduotuvės parinkiklio modulio pavyzdys](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="61082-117">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="61082-117">Module properties</span></span>

| <span data-ttu-id="61082-118">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="61082-118">Property name</span></span>             | <span data-ttu-id="61082-119">Vertė</span><span class="sxs-lookup"><span data-stu-id="61082-119">Value</span></span>                 | <span data-ttu-id="61082-120">aprašymas</span><span class="sxs-lookup"><span data-stu-id="61082-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="61082-121">Antraštė</span><span class="sxs-lookup"><span data-stu-id="61082-121">Heading</span></span> | <span data-ttu-id="61082-122">Tekstas</span><span class="sxs-lookup"><span data-stu-id="61082-122">Text</span></span> | <span data-ttu-id="61082-123">Modulio antraštė.</span><span class="sxs-lookup"><span data-stu-id="61082-123">The heading for the module.</span></span> |
| <span data-ttu-id="61082-124">Stūmoklio parinktys: nustatytoji piktograma</span><span class="sxs-lookup"><span data-stu-id="61082-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="61082-125">Nuotrauka</span><span class="sxs-lookup"><span data-stu-id="61082-125">Image</span></span> | <span data-ttu-id="61082-126">Stūmoklio simbolio paveikslėlis naudojamas parduotuvėms rodomoms žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="61082-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="61082-127">Stūmoklio parinktys: aktyvi piktograma</span><span class="sxs-lookup"><span data-stu-id="61082-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="61082-128">Nuotrauka</span><span class="sxs-lookup"><span data-stu-id="61082-128">Image</span></span> | <span data-ttu-id="61082-129">Stūmoklio simbolio paveikslėlis naudojamas parduotuvei pasirinktai žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="61082-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="61082-130">Stūmoklio parinktys: nustatytosios piktogramos spalva</span><span class="sxs-lookup"><span data-stu-id="61082-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="61082-131">Maskavimo pynė</span><span class="sxs-lookup"><span data-stu-id="61082-131">Character string</span></span> | <span data-ttu-id="61082-132">Tekstas ir šešioliktainės vertės stūmoklio simbolio spalvai žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="61082-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="61082-133">Stūmoklio parinktys: aktyvi piktogramos spalva</span><span class="sxs-lookup"><span data-stu-id="61082-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="61082-134">Maskavimo pynė</span><span class="sxs-lookup"><span data-stu-id="61082-134">Character string</span></span> | <span data-ttu-id="61082-135">Tekstas ir šešioliktainės vertės pasirinkto stūmoklio simbolio spalvai žemėlapyje.</span><span class="sxs-lookup"><span data-stu-id="61082-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="61082-136">Rodyti rodyklę</span><span class="sxs-lookup"><span data-stu-id="61082-136">Show index</span></span> | <span data-ttu-id="61082-137">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="61082-137">**True** or **False**</span></span> | <span data-ttu-id="61082-138">Jei ši ypatybė yra nustatytą į **Teisingą**, visi stūmoklio simboliai rodantys parduotuvę bus rodomi turinyje.</span><span class="sxs-lookup"><span data-stu-id="61082-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="61082-139">Šis turinys atitiks turinį sąrašo peržiūroje, kurioje parduotuvės selektoriaus modulis yra rodomas.</span><span class="sxs-lookup"><span data-stu-id="61082-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="61082-140">Įtraukti leidžiamą žemėlapio kūrimo URL į sveitainės turinio apsaugos politikos gaires</span><span class="sxs-lookup"><span data-stu-id="61082-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="61082-141">Tam, kad žemėlapių modulis sąveikatų su „Bing Maps“, turite užtikrinti, kad tolesni žemėlapio URL yra leidžiami jūsų saito turinio saugos politikoje (CSP).</span><span class="sxs-lookup"><span data-stu-id="61082-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="61082-142">Šis nustatymas yra atliekamas komercijos svetainės kūrimo įrankyje įtraukiant leidžiamus URL į skirtingas svateinės CSP gaires svetainei (pavyzdžiui, **img-src**).</span><span class="sxs-lookup"><span data-stu-id="61082-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="61082-143">Dėl platesnės informacijos, žr. [Turinio saugos politika](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="61082-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="61082-144">Į **connect-src** direktyvą, įtraukite **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="61082-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="61082-145">Į **img-src** direktyvą, įtraukite **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="61082-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="61082-146">Į **script-src** direktyvą, įtraukite **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="61082-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="61082-147">Į **script style-src** direktyvą, įtraukite **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="61082-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="61082-148">Įtraukti žemėlapio modulį į puslapį</span><span class="sxs-lookup"><span data-stu-id="61082-148">Add a map module to a page</span></span>

<span data-ttu-id="61082-149">Dėl išsamesnės informacijos apie tai, kaip konfigūruoti žemėlapio modulį puslapyje, žr. [Parduotuvės pasirinkimo modulis](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="61082-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="61082-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="61082-150">Additional resources</span></span>

[<span data-ttu-id="61082-151">Modulių bibliotekos apžvalga</span><span class="sxs-lookup"><span data-stu-id="61082-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="61082-152">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="61082-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="61082-153">Krepšelio modulis</span><span class="sxs-lookup"><span data-stu-id="61082-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="61082-154">Parduotuvės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="61082-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="61082-155">„Bing“ žemėlapių valdymas jūsų organizacijoje</span><span class="sxs-lookup"><span data-stu-id="61082-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="61082-156">„Bing Maps V8 Web Control“</span><span class="sxs-lookup"><span data-stu-id="61082-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
