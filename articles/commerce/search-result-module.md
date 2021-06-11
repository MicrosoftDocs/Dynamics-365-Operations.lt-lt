---
title: Ieškokite rezultatų modulio
description: Šioje temoje aprašomi paieškos rezultatų moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 05/28/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 645022000d8746db3793a8a8611ab8f17c7bcc6e
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117138"
---
# <a name="search-results-module"></a><span data-ttu-id="c963f-103">Ieškos rezultatų modulis</span><span class="sxs-lookup"><span data-stu-id="c963f-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c963f-104">Šioje temoje aprašomi paieškos rezultatų moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="c963f-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c963f-105">Paieškos rezultatų modulis grąžina produkto paieškos rezultatus ir taikomų perdirbimo įrankių sąrašą produktams.</span><span class="sxs-lookup"><span data-stu-id="c963f-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="c963f-106">Paieškos rezultatų moduliai „Dynamics 365 Commerce“ saituose gali būti naudojami siekiant apimti puslapius šiais scenarijais:</span><span class="sxs-lookup"><span data-stu-id="c963f-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="c963f-107">Paieškos rezultatai, kuriuos pradėjo vartotojo paieška</span><span class="sxs-lookup"><span data-stu-id="c963f-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="c963f-108">Paieškos rezultatai, kurie rodo konkretų produktų rinkinį, tokį kaip „Į parduotuvę panašios paieškos“</span><span class="sxs-lookup"><span data-stu-id="c963f-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="c963f-109">Produktų, priklausančių kategorijai, sąrašai</span><span class="sxs-lookup"><span data-stu-id="c963f-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="c963f-110">Daugiau informacijos apie kategoriją ir paieškos rezultatų puslapius rasite [Numatytos kategorijos užsklandos puslapis ir paieškos rezultatų puslapio apžvalga](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c963f-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="c963f-111">Tolesnis paveikslėlis rodo paieškos rezultatų puslapio pavyzdį kategorijai „Fabrikam“ saite.</span><span class="sxs-lookup"><span data-stu-id="c963f-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Paieškos rezultatų puslapio pavyzdys „Fabrikam“ saite](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="c963f-113">Paieškos rezultatų modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="c963f-113">Search results module properties</span></span>

<span data-ttu-id="c963f-114">Tolesnėje lentelėje išvardytos paieškos rezultato modulių ypatybės kartu su jų vertėmis ir aprašais.</span><span class="sxs-lookup"><span data-stu-id="c963f-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="c963f-115">Ypatybė</span><span class="sxs-lookup"><span data-stu-id="c963f-115">Property</span></span> | <span data-ttu-id="c963f-116">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="c963f-116">Values</span></span> | <span data-ttu-id="c963f-117">aprašymas</span><span class="sxs-lookup"><span data-stu-id="c963f-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="c963f-118">Prekių skaičius viename puslapyje</span><span class="sxs-lookup"><span data-stu-id="c963f-118">Items per page</span></span> | <span data-ttu-id="c963f-119">Sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="c963f-119">Integer</span></span> | <span data-ttu-id="c963f-120">Prekių skaičius, kuris turi būti rodomas kiekviename puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c963f-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="c963f-121">Leisti atgal į PDP</span><span class="sxs-lookup"><span data-stu-id="c963f-121">Allow back on PDP</span></span> | <span data-ttu-id="c963f-122">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="c963f-122">**True** or **False**</span></span> | <span data-ttu-id="c963f-123">Jei ši ypatybė nustatyta į **Teisinga**, kai vartotojas pasirenka produktą paieškos rezultatų puslapyje, atvertas džiūvėsėlio naršymas produkto išsamios informacijos puslapyje (PDP) rodys „Grįžti į rezultatus“ nuorodą.</span><span class="sxs-lookup"><span data-stu-id="c963f-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="c963f-124">Išplėsti tikslinimo meniu</span><span class="sxs-lookup"><span data-stu-id="c963f-124">Expand Refiners</span></span> | <span data-ttu-id="c963f-125">**Visi**, **1**, **2**, **3** ar **4**</span><span class="sxs-lookup"><span data-stu-id="c963f-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="c963f-126">Pagrindinių apdirbėjų skaičius, kuris turi būti išplečiamas užkrovus puslapį.</span><span class="sxs-lookup"><span data-stu-id="c963f-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="c963f-127">Pavyzdžiui, jei ši ypatybė yra nustatyta į **3**, pirmieji trys apdirbėjai puslapyje bus išplėsti.</span><span class="sxs-lookup"><span data-stu-id="c963f-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="c963f-128">Slėpti kategorijų hierarchijos rodymą</span><span class="sxs-lookup"><span data-stu-id="c963f-128">Hide category hierarchy display</span></span> | <span data-ttu-id="c963f-129">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="c963f-129">**True** or **False**</span></span> | <span data-ttu-id="c963f-130">Jei ši ypatybė yra nustatyta į **Teisinga**, kategorijos hierarchija rodoma puslapyje bus paslėpta.</span><span class="sxs-lookup"><span data-stu-id="c963f-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="c963f-131">Ši ypatybė turi būti nustatyta į **Teisingą** jei naudojate [džiūvėsėlio modulį](add-breadcrumb.md) tam, kad jis parodytų kategorijos hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="c963f-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="c963f-132">Į paieškos rezultatus įtraukite produkto atributus</span><span class="sxs-lookup"><span data-stu-id="c963f-132">Include product attributes in search results</span></span> | <span data-ttu-id="c963f-133">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="c963f-133">**True** or **False**</span></span> | <span data-ttu-id="c963f-134">Jei ši ypatybė yra nustatyta į **Teisinga**, atributai bus grąžinami produktams paieškos rezultatuose.</span><span class="sxs-lookup"><span data-stu-id="c963f-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="c963f-135">Nepaisant to, kad šie atributai gali būti rodomi „Commerce“ saite, būtinas plėtinys.</span><span class="sxs-lookup"><span data-stu-id="c963f-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="c963f-136">Rodyti priskyrimo kainas</span><span class="sxs-lookup"><span data-stu-id="c963f-136">Show affiliation prices</span></span> | <span data-ttu-id="c963f-137">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="c963f-137">**True** or **False**</span></span> | <span data-ttu-id="c963f-138">Jei ši ypatybė yra nustatyta į **Teisinga**, prisijungimo kainos produktams bus rodomos paieškos rezultatuose, kai prisijungęs vartotojas naršo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c963f-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |
| <span data-ttu-id="c963f-139">Tikslinimo skydo naujinimas</span><span class="sxs-lookup"><span data-stu-id="c963f-139">Update refiner panel</span></span> | <span data-ttu-id="c963f-140">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="c963f-140">**True** or **False**</span></span> | <span data-ttu-id="c963f-141">Jei ši ypatybė nustatyta kaip **Teisinga**, tikslinimo skydas bus atnaujintas pasirinkus tikslinimo priemones.</span><span class="sxs-lookup"><span data-stu-id="c963f-141">If this property is set to **True**, the refiner panel will be updated when refiners are selected.</span></span> <span data-ttu-id="c963f-142">Šiuo režimu kai kurios kelių pasirinkimų tikslinimo priemonės elgsis kaip vieno pasirinkimo tikslinimo priemonės, atnaujinus tikslinimo skydą.</span><span class="sxs-lookup"><span data-stu-id="c963f-142">In this mode, some multiple-selection refiners will behave like single-selection refiners when the refiner panel is updated.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="c963f-143">„Commerce” 10.0.16 versijos leidime ir vėlesniuose konfigūracija **Rodyti priskyrimo kainas** galima naudoti norint rodyti priskyrimo kainas puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c963f-143">In the Commerce version 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>
>
> <span data-ttu-id="c963f-144">„Commerce” 10.0.20 versijos leidime ir vėlesniuose konfigūraciją **Naujinti tikslinimo skydą** galima naudoti norint atnaujinti tikslinimo skydą tikslinimo priemonės pasirinkimo metu.</span><span class="sxs-lookup"><span data-stu-id="c963f-144">In the Commerce version 10.0.20 release and later, the **Update refiner panel** configuration can be used to update the refiner panel during refiner selection.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="c963f-145">Palaikomi moduliai</span><span class="sxs-lookup"><span data-stu-id="c963f-145">Supported modules</span></span>

<span data-ttu-id="c963f-146">Paieškos rezultatų modulis palaiko [greito rodinio modulį](quick-view-module.md), kuris leidžia vartotojams peržiūrėti produkto informaciją ir įtraukti prekes į vežimėlį iš paieškos rezultatų puslapio.</span><span class="sxs-lookup"><span data-stu-id="c963f-146">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="c963f-147">Įtraukite paieškos rezultatų modulį į kategorijų puslapį</span><span class="sxs-lookup"><span data-stu-id="c963f-147">Add a search results module to a category page</span></span>

<span data-ttu-id="c963f-148">Norėdami įtraukti paieškos rezultatų modulį į kategorijų puslapį, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="c963f-148">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="c963f-149">Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="c963f-149">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c963f-150">Teksto laukelyje **Naujas šablonas** įveskite pavadinimą **Paieškos rezultatai** ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c963f-150">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="c963f-151">Vietoje **tekstas** pasirinkite daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="c963f-151">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c963f-152">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c963f-152">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c963f-153">Vietoje **Pagrindinis** modulyje **Numatytas puslapis** rinkitės daugtaškį (...) ir tada rinkitės **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="c963f-153">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c963f-154">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c963f-154">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c963f-155">Vietoje **Talpykla** pasirinkite daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="c963f-155">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c963f-156">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c963f-156">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c963f-157">Ypatybių juostoje **Džiūvėsėlis** įveskite vertę **1** skirtą **Minimaliems atsitikimams**.</span><span class="sxs-lookup"><span data-stu-id="c963f-157">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="c963f-158">Vietoje **Talpykla** pasirinkite daugtaškį (...), o tada pasirinkite **Įtraukite modulį**.</span><span class="sxs-lookup"><span data-stu-id="c963f-158">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c963f-159">Teksto laukelyje **Įtraukti modulį** pasirinkite **Paieškos rezultatai** modulį, o tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c963f-159">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c963f-160">Ypatybių juostoje **Paieškos rezultatai** įveskite vertę **1** skirtą **Minimalūs atsitikimai** ir tuomet nustatykite visas kitas reikiamas ypatybes paieškos rezultatų moduliui.</span><span class="sxs-lookup"><span data-stu-id="c963f-160">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="c963f-161">Nustatydami šias ypatybes šablone užtikrinate, kad bet kokie tinkinimai konkrečios kategorijos puslapyje automatiškai apims šiuos nustatymus.</span><span class="sxs-lookup"><span data-stu-id="c963f-161">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="c963f-162">Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte šabloną.</span><span class="sxs-lookup"><span data-stu-id="c963f-162">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="c963f-163">Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.</span><span class="sxs-lookup"><span data-stu-id="c963f-163">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="c963f-164">Teksto laukelyje **Rinkitės šabloną** pasirinkite **Paieškos rezultatai** sukurtą šabloną, įveskite **Kategorijos puslapis** skirtą **Puslapio pavadinimas** ir tada rinkitės **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c963f-164">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="c963f-165">Kadangi visos vertės yra nustatytos šablone, puslapis yra parengtas publikuoti.</span><span class="sxs-lookup"><span data-stu-id="c963f-165">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="c963f-166">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="c963f-166">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c963f-167">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c963f-167">Additional resources</span></span>

[<span data-ttu-id="c963f-168">Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="c963f-168">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="c963f-169">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="c963f-169">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c963f-170">Greito rodinio modulis</span><span class="sxs-lookup"><span data-stu-id="c963f-170">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
