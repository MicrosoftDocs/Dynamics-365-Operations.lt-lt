---
title: Ieškokite rezultatų modulio
description: Šioje temoje aprašomi paieškos rezultatų moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3761be29955458099d01f2271057884fc1fd6f28
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097183"
---
# <a name="search-results-module"></a><span data-ttu-id="18082-103">Ieškokite rezultatų modulis</span><span class="sxs-lookup"><span data-stu-id="18082-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="18082-104">Šioje temoje aprašomi paieškos rezultatų moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="18082-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="18082-105">Paieškos rezultatų modulis grąžina produkto paieškos rezultatus ir taikomų perdirbimo įrankių sąrašą produktams.</span><span class="sxs-lookup"><span data-stu-id="18082-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="18082-106">Paieškos rezultatų moduliai „Dynamics 365 Commerce“ saituose gali būti naudojami siekiant apimti puslapius šiais scenarijais:</span><span class="sxs-lookup"><span data-stu-id="18082-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="18082-107">Paieškos rezultatai, kuriuos pradėjo vartotojo paieška</span><span class="sxs-lookup"><span data-stu-id="18082-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="18082-108">Paieškos rezultatai, kurie rodo konkretų produktų rinkinį, tokį kaip „Į parduotuvę panašios paieškos“</span><span class="sxs-lookup"><span data-stu-id="18082-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="18082-109">Produktų, priklausančių kategorijai, sąrašai</span><span class="sxs-lookup"><span data-stu-id="18082-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="18082-110">Dėl daugiau informacijos apie kategoriją ir paieškos rzultatų puslapius, žr. [Numatytos kategorijos užsklandos puslapis ir paieškos rezultatų puslapio apžvalga](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="18082-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="18082-111">Tolesnis paveikslėlis rodo paieškos rezultatų puslapio pavyzdį kategorijai „Fabrikam“ saite.</span><span class="sxs-lookup"><span data-stu-id="18082-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Paieškos rezultatų puslapio pavyzdys „Fabrikam“ saite](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="18082-113">Paieškos rezultatų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="18082-113">Search results module properties</span></span>

<span data-ttu-id="18082-114">Tolesnėje lentelėje išvardytos paieškos rezultato modulių ypatybės kartu su jų vertėmis ir aprašais.</span><span class="sxs-lookup"><span data-stu-id="18082-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="18082-115">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="18082-115">Property</span></span> | <span data-ttu-id="18082-116">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="18082-116">Values</span></span> | <span data-ttu-id="18082-117">aprašymas</span><span class="sxs-lookup"><span data-stu-id="18082-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="18082-118">Prekių skaičius viename puslapyje</span><span class="sxs-lookup"><span data-stu-id="18082-118">Items per page</span></span> | <span data-ttu-id="18082-119">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="18082-119">Integer</span></span> | <span data-ttu-id="18082-120">Prekių skaičius, kuris turi būti rodomas kiekviename puslapyje.</span><span class="sxs-lookup"><span data-stu-id="18082-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="18082-121">Leisti atgal į PDP</span><span class="sxs-lookup"><span data-stu-id="18082-121">Allow back on PDP</span></span> | <span data-ttu-id="18082-122">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="18082-122">**True** or **False**</span></span> | <span data-ttu-id="18082-123">Jei ši ypatybė nustatyta į **Teisinga**, kai vartotojas pasirenka produktą paieškos rezultatų puslapyje, atvertas džiūvesėlio naršymas produkto išsamios informacijos puslapyje (PDP) rodys „Grįžti į rezultatus“ nuorodą.</span><span class="sxs-lookup"><span data-stu-id="18082-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="18082-124">Išplėsti tikslinimo meniu</span><span class="sxs-lookup"><span data-stu-id="18082-124">Expand Refiners</span></span> | <span data-ttu-id="18082-125">**Visi**, **1**, **2**, **3** ar **4**</span><span class="sxs-lookup"><span data-stu-id="18082-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="18082-126">Pagrindinių apdirbėjų skaičius, kuris turi būti išplečiamas užkrovus puslapį.</span><span class="sxs-lookup"><span data-stu-id="18082-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="18082-127">Pavyzdžiui, jei ši ypatybė yra nustatyta į **3**, pirmieji trys apdirbėjai puslapyje bus išplėsti.</span><span class="sxs-lookup"><span data-stu-id="18082-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="18082-128">Slėpti kategorijų hierarchijos rodymą</span><span class="sxs-lookup"><span data-stu-id="18082-128">Hide category hierarchy display</span></span> | <span data-ttu-id="18082-129">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="18082-129">**True** or **False**</span></span> | <span data-ttu-id="18082-130">Jei ši ypatybė yra nustatyta į **Teisinga**, kategorijos hierarchija rodoma puslapyje bus paslėpta.</span><span class="sxs-lookup"><span data-stu-id="18082-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="18082-131">Ši ypatybė turi būti nustatyta į **Teisingą** jei naudojate [džiūvesėlio modulį](add-breadcrumb.md) tam, kad jis parodytų kategorijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="18082-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="18082-132">Į paieškos rezultatus įtraukite produkto atributus</span><span class="sxs-lookup"><span data-stu-id="18082-132">Include product attributes in search results</span></span> | <span data-ttu-id="18082-133">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="18082-133">**True** or **False**</span></span> | <span data-ttu-id="18082-134">Jei ši ypatybė yra nustatyta į **Teisinga**, atributai bus grąžinami produktams paieškos rezultatuose.</span><span class="sxs-lookup"><span data-stu-id="18082-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="18082-135">Nepaisant to, kad šie atributai gali būti rodomi „Commerce“ saite, būtinas plėtinys.</span><span class="sxs-lookup"><span data-stu-id="18082-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="18082-136">Rodyti priskyrimo kainas</span><span class="sxs-lookup"><span data-stu-id="18082-136">Show affiliation prices</span></span> | <span data-ttu-id="18082-137">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="18082-137">**True** or **False**</span></span> | <span data-ttu-id="18082-138">Jei ši ypatybė yra nustatyta į **Teisinga**, prisijungimo kainos produktams bus rodomos paieškos rezultatuose, kai prisijungęs vartotojas naršo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="18082-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="18082-139">„Dynamics 365 Commerce“ 10.0.16 leidimuose ir vėlesniuose, **Rodyti prisijungimo kainas** konfigūravimas gali būti naudojamas siekiant rodyti prisijungimo kainas puslapyje.</span><span class="sxs-lookup"><span data-stu-id="18082-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="18082-140">Palaikomi moduliai</span><span class="sxs-lookup"><span data-stu-id="18082-140">Supported modules</span></span>

<span data-ttu-id="18082-141">Paieškos rezultatų modulis palaiko [greito rodinio modulį](quick-view-module.md), kuris leidžia vartotojams peržiūrėti produkto informaciją ir įtraukti prekes į vežimėlį iš paieškos rezultatų puslapio.</span><span class="sxs-lookup"><span data-stu-id="18082-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="18082-142">Įtraukite paieškos rezultatų modulį į kategorijų puslapį</span><span class="sxs-lookup"><span data-stu-id="18082-142">Add a search results module to a category page</span></span>

<span data-ttu-id="18082-143">Norėdami įtraukti paieškos rezultatų modulį į kategorijų puslapį, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="18082-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="18082-144">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="18082-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="18082-145">Teksto laukelyje **Naujas šablonas** įveskite pavadinimą **Paieškos rezultatai** ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="18082-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="18082-146">Vietoje **tekstas** rinkiės daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="18082-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="18082-147">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="18082-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="18082-148">Vietoje **Pagrindinis** modulyje **Numatytas puslapis** rinkitės daugtaškį (...) ir tada rinkitės **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="18082-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="18082-149">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="18082-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="18082-150">Vietoje **Talpykla** rinkiės daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="18082-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="18082-151">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="18082-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="18082-152">Ypatybių juostoje **Džiūvesėlis** įveskite vertę **1** skirtą **Minimaliems atsitikimams**.</span><span class="sxs-lookup"><span data-stu-id="18082-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="18082-153">Vietoje **Talpykla** rinkiės daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="18082-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="18082-154">Teksto laukelyje **Įtraukti modulį** rinkitės **Paieškos rezultatai** modulį ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="18082-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="18082-155">Ypatybių juostoje **Paieškos rezultatai** įveskite vertę **1** skirtą **Minimalūs atsitikimai** ir tuomet nustatykite visas kitas reikiamas ypatybes paieškos rezultatų moduliui.</span><span class="sxs-lookup"><span data-stu-id="18082-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="18082-156">Nustatydami šias ypatybes šablone užtikrinate, kad bet kokie tinkinimai konkrečios kategorijos puslapyje automatiškai apims šiuos nustatymus.</span><span class="sxs-lookup"><span data-stu-id="18082-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="18082-157">Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="18082-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="18082-158">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="18082-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="18082-159">Teksto laukelyje **Rinkitės šabloną** rinkiės **Paieškos rezultatai** sukurtą šabloną, įveskite **Kategorijos puslapis** skirtą **Puslapio pavadinimas** ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="18082-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="18082-160">Kadangi visos vertės yra nustatyos šablone, puslapis yra parengtas publikuoti.</span><span class="sxs-lookup"><span data-stu-id="18082-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="18082-161">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="18082-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18082-162">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="18082-162">Additional resources</span></span>

[<span data-ttu-id="18082-163">Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="18082-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="18082-164">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="18082-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="18082-165">Greito rodinio modulis</span><span class="sxs-lookup"><span data-stu-id="18082-165">Quick view module</span></span>](quick-view-module.md)
