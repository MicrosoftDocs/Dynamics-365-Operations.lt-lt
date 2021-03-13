---
title: Greito rodinio modulis
description: Šioje temoje aprašomi greito rodinio moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7e8244a06c515029b559b2061d9a25c7355e9e14
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097057"
---
# <a name="quick-view-module"></a><span data-ttu-id="d0671-103">Greito rodinio modulis</span><span class="sxs-lookup"><span data-stu-id="d0671-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d0671-104">Šioje temoje aprašomi greito rodinio moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="d0671-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d0671-105">Greito rodinio modulis leidžia vartotojams greitai peržiūrėti produkto informaciją, kai jie naršo produktus sąrašo puslapyje ir įtraukia vieną ar daugiau produktų į vežimėlį iš sąrašo puslapio be poreikio eiti į produkto išsamios informacijos puslapį (PDP).</span><span class="sxs-lookup"><span data-stu-id="d0671-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="d0671-106">Greito rodinio modulis pateikia produkto informacijos apžvalgą, dėl kurios vartotojai turi padaryti „pridėti prie vežimėlio“ sprendimą.</span><span class="sxs-lookup"><span data-stu-id="d0671-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="d0671-107">Jis taip pat pateikia nuorodą į PDP tam, kad vartotojai galėtų peržiūrėti papildomą produkto informaciją ir pirkimo parinktis.</span><span class="sxs-lookup"><span data-stu-id="d0671-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="d0671-108">Greito rodinio modulis yra palaikomas [produkto kolekcijos](product-collection-module-overview.md) ir [paieškos rezultatų](search-result-module.md) modulių.</span><span class="sxs-lookup"><span data-stu-id="d0671-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0671-109">Greito rodinio modulis yra prieinamas nuo „Commerce“ versijos 10.0.17 leidime.</span><span class="sxs-lookup"><span data-stu-id="d0671-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="d0671-110">Tolesnis paveikslėlis rodo greito rodinio modulio pavyzdžio produkto sąrašą puslapyje.</span><span class="sxs-lookup"><span data-stu-id="d0671-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Greito rodinio modulio produkto sąrašo puslapyej pavyzdys](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="d0671-112">Modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="d0671-112">Module properties</span></span>

<span data-ttu-id="d0671-113">Greito rodinio modulis palaiko kelias tas pačias funkcijas, tokias kaip pirkimo dėžutės modulis.</span><span class="sxs-lookup"><span data-stu-id="d0671-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="d0671-114">Dėl to, greito rodinio modulio ypatybės rodo pirkimo dėžutės modulio ypatybes.</span><span class="sxs-lookup"><span data-stu-id="d0671-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="d0671-115">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="d0671-115">Property</span></span> | <span data-ttu-id="d0671-116">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="d0671-116">Values</span></span> | <span data-ttu-id="d0671-117">aprašymas</span><span class="sxs-lookup"><span data-stu-id="d0671-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="d0671-118">Antraštės žymė</span><span class="sxs-lookup"><span data-stu-id="d0671-118">Heading tag</span></span> | <span data-ttu-id="d0671-119">**H1**, **H2**, **H3**, **H4**, **H5** ar **H6**</span><span class="sxs-lookup"><span data-stu-id="d0671-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="d0671-120">Šios ypatybės nustato antraštęs skirtuką produkto pavadinimui.</span><span class="sxs-lookup"><span data-stu-id="d0671-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="d0671-121">Jei greito rodinio modulis yra puslapio viršuje, ši ypatybė turi būti nustatyta į **H1** tam, kad atitiktų prieinamumo standartus.</span><span class="sxs-lookup"><span data-stu-id="d0671-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="d0671-122">Leisti pasirinktinę kainą</span><span class="sxs-lookup"><span data-stu-id="d0671-122">Allow custom price</span></span> | <span data-ttu-id="d0671-123">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="d0671-123">**True** or **False**</span></span> | <span data-ttu-id="d0671-124">Jei ši ypatybė yra nustatyta į **Teisingą**, vartotojas gali įvesti tinkintą kainą.</span><span class="sxs-lookup"><span data-stu-id="d0671-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="d0671-125">Minimali kaina</span><span class="sxs-lookup"><span data-stu-id="d0671-125">Minimum price</span></span> | <span data-ttu-id="d0671-126">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="d0671-126">Integer</span></span> | <span data-ttu-id="d0671-127">Ši ypatybė yra taikoma tik, jei **Leisti tinkintą kainą** ypatybė yra nustatyta į **Teisingą**.</span><span class="sxs-lookup"><span data-stu-id="d0671-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="d0671-128">Ji nustato minimalią kainą, kurią vartotojas gali įvesti (pavyzdžiui, $1).</span><span class="sxs-lookup"><span data-stu-id="d0671-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="d0671-129">Maksimali kaina</span><span class="sxs-lookup"><span data-stu-id="d0671-129">Maximum price</span></span> | <span data-ttu-id="d0671-130">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="d0671-130">Integer</span></span> | <span data-ttu-id="d0671-131">Ši ypatybė yra taikoma tik, jei **Leisti tinkintą kainą** ypatybė yra nustatyta į **Teisingą**.</span><span class="sxs-lookup"><span data-stu-id="d0671-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="d0671-132">Ji nustato maksimalią kainą, kurią vartotojas gali įvesti (pavyzdžiui, $1,000).</span><span class="sxs-lookup"><span data-stu-id="d0671-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="d0671-133">„Commerce“ saito kūrimo įrankio nustatymai</span><span class="sxs-lookup"><span data-stu-id="d0671-133">Commerce site builder settings</span></span>

<span data-ttu-id="d0671-134">Kaip ir pirkimo laukelio modulis, greito rodinio modulis laikosi nustatymų **Saito nustatymai \> Plėtiniai \> Įtraukti produktą į vežimėlį**.</span><span class="sxs-lookup"><span data-stu-id="d0671-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="d0671-135">Nepaisant to, **Naršyti į vežimėlio puslapį** nustatymai yra ignoruojami, nes jie nėra nenuosėklūs su greito rodinio modulio tikslu, kuris skirtas įjungti vartotojams galimybę naršyti keliuose produktuose puslapio sąraše ir įtraukti juos į vežimėlį neatsitraukiant nuo sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="d0671-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="d0671-136">Įtraukite greito rodinio modulį į produkto kolekcijos modulį</span><span class="sxs-lookup"><span data-stu-id="d0671-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="d0671-137">Greito rodinio modulis gali būti įtrauktas į produkto kolekciją ir paieškos rezultatų modulius.</span><span class="sxs-lookup"><span data-stu-id="d0671-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="d0671-138">Norėdami įtraukti greito rodinio modulį į produkto kolekcijos modulį „Commerce“ saito kūrimo įrankyje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d0671-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d0671-139">Eikite į **Puslapiai** ir tada rinkitės pagrindinį puslapį „Fabrikam“ saite.</span><span class="sxs-lookup"><span data-stu-id="d0671-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="d0671-140">Eikite į bet kurį **Produkto kolekcijos** modulyje pagrindiniame puslapyje, rinkitės daugtaškį (**...**) ir tada rinkitės **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="d0671-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d0671-141">Teksto laukelyje **Įtraukti modulį** rinkitės **Greito rodinio** modulį ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d0671-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d0671-142">Ypatybių juostoje **Greito rodinio** modulyje rinkitės **Antraštė**.</span><span class="sxs-lookup"><span data-stu-id="d0671-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="d0671-143">Teksto laukelyje **Antraštė** nustatykite **Antraštės lygio** laukelį į **H2** ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d0671-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="d0671-144">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="d0671-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0671-145">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d0671-145">Additional resources</span></span>

[<span data-ttu-id="d0671-146">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="d0671-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d0671-147">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="d0671-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d0671-148">Produktų atsiėmimo modulis</span><span class="sxs-lookup"><span data-stu-id="d0671-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="d0671-149">Ieškokite rezultatų modulio</span><span class="sxs-lookup"><span data-stu-id="d0671-149">Search results module</span></span>](search-result-module.md)
