---
title: Naršymo kelio modulis
description: Šioje temoje aprašomi naršymo kelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c6d846686e3214e976a55271694382d7c5973ed
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417397"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="5b4ed-103">Naršymo kelio modulis</span><span class="sxs-lookup"><span data-stu-id="5b4ed-103">Breadcrumb module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5b4ed-104">Šioje temoje aprašomi naršymo kelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5b4ed-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="5b4ed-105">Overview</span></span>

<span data-ttu-id="5b4ed-106">Naršymo kelio moduliai naudojami antrinei navigacijai svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="5b4ed-107">Jis paprastai rodomas puslapio viršuje, po antrašte.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="5b4ed-108">Nors naršymo kelio modulius galima įtraukti į bet kurį puslapį, dažniausiai jie naudojami produkto informacijos puslapiuose (PDP), kad būtų rodoma produktų kategorijų hierarchija ir būtų užtikrintas greitas būdas naršyti po svetainę.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="5b4ed-109">Naršymo kelio modulis taip pat gali būti naudojamas siekiant parodyti saitą „Atgal į rezultatus“, kai vartotojai atidaro PDP ieškos ar sąrašo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="5b4ed-110">Šitaip vartotojai gali greitai grįžti prie filtruoto sąrašo puslapio ir tęsti apsipirkimą.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="5b4ed-111">Puslapiuose, kurie turi produktų kategorijos konteksto, pvz., PDP ir kategorijos puslapiuose, naršymo kelio moduliai rodo kategorijų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="5b4ed-112">Puslapiuose, kuriuose nėra kategorijos konteksto, naršymo kelio moduliai pagal numatytąją nuostatą rodo **&lt;Svetainės šaknis&gt; / &lt;Dabartinis puslapis&gt;**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="5b4ed-113">Naršymo kelio modulius taip pat galima rankiniu būdu konfigūruoti ir kitų tipų svetainės puslapiuose, kad būtų rodomi saitai į konkrečius svetainės puslapius.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

<span data-ttu-id="5b4ed-114">Toliau pateiktame paveikslėlyje parodytas naršymo kelio modulio pavyzdys, rodantis kategorijų hierarchiją PDP.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Naršymo kelio modulio pavyzdys](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="5b4ed-116">Naršymo modulio parametrai</span><span class="sxs-lookup"><span data-stu-id="5b4ed-116">Breadcrumb module settings</span></span>

<span data-ttu-id="5b4ed-117">Naršymo kelio modulis priklauso nuo parametro **Naršymo kelio rodymo tipas PDP**, kuris nurodytas svetainių daryklės dalyje **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="5b4ed-118">Galimos trys šio parametro vertės:</span><span class="sxs-lookup"><span data-stu-id="5b4ed-118">This setting has three possible values:</span></span>

- <span data-ttu-id="5b4ed-119">**Rodyti kategorijų hierarchiją** – kai ši vertė pasirinkta, naudojant naršymo kelio modulį bus rodoma išsami PDP peržiūrimo produkto kategorijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="5b4ed-120">**Rodyti „atgal į rezultatus“** – kai ši vertė pasirinkta, naršymo kelio modulis rodo saitą „Atgal į rezultatus“ PDP, jei vartotojas atidarė PDP modulyje, kuriame galima naudoti saitą „Atgal į rezultatus“.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="5b4ed-121">Šią funkciją galima, kai vartotojai naršo iš kategorijos, ieškos, sąrašo ir rekomendacijų sąrašų puslapių.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="5b4ed-122">Tam, kad ši funkcija veiktų, produktų rinkinys ir ieškos rezultatų moduliai turi ypatybę, kuri pavadinta **Leisti grįžti į rezultatus PDP**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="5b4ed-123">Ši ypatybė suteikia jums galimybę apibrėžti, kurie moduliai turi palaikyti saito „Atgal į rezultatus“ funkciją PDP.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="5b4ed-124">Pavyzdžiui, kai pasirinkta naršymo kelio modulio parametro **Naršymo kelio rodymo tipas PDP** ypatybė **Rodyti „atgal į rezultatus“** ir pasirinkta ieškos puslapio ieškos rezultatų modulio ypatybė **Leisti grįžti į rezultatus PDP**, saitą „Atgal į rezultatus“ bus rodoma tada, kai vartotojai pereina iš ieškos puslapio į PDP.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="5b4ed-125">**Rodyti kategorijų hierarchiją ir grįžimo į rezultatus saitą** – ši vertė yra ankstesnių dviejų verčių derinys.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="5b4ed-126">Pasirinkus šią vertę, naudojant naršymo kelio modulį, PDP bus rodoma ir išsami kategorijų hierarchija ir saitą „Atgal į rezultatus“ (jei sukonfigūruota).</span><span class="sxs-lookup"><span data-stu-id="5b4ed-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="5b4ed-127">Naršymo kelio modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="5b4ed-127">Breadcrumb module properties</span></span>

| <span data-ttu-id="5b4ed-128">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="5b4ed-128">Property name</span></span> | <span data-ttu-id="5b4ed-129">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="5b4ed-129">Values</span></span> | <span data-ttu-id="5b4ed-130">aprašymas</span><span class="sxs-lookup"><span data-stu-id="5b4ed-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="5b4ed-131">Šakninis</span><span class="sxs-lookup"><span data-stu-id="5b4ed-131">Root</span></span> | <span data-ttu-id="5b4ed-132">Tekstas arba saitas</span><span class="sxs-lookup"><span data-stu-id="5b4ed-132">Text or link</span></span>| <span data-ttu-id="5b4ed-133">Ši neprivaloma ypatybė nurodo naršymo kelio šakninės svetainės saito tekstą ir paskirtį.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-133">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="5b4ed-134">Jei ši ypatybė nesukonfigūruota, šaknis nebus apibrėžta.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-134">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="5b4ed-135">Naršymo kelio saitas</span><span class="sxs-lookup"><span data-stu-id="5b4ed-135">Breadcrumb link</span></span> | <span data-ttu-id="5b4ed-136">Saitas</span><span class="sxs-lookup"><span data-stu-id="5b4ed-136">Link</span></span> | <span data-ttu-id="5b4ed-137">Ši pasirenkama ypatybė nurodo neautomatiniu būdu sukonfigūruoto naršymo kelio saitus, jei šie saitai būtini.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-137">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="5b4ed-138">Saitai rodomi tokia tvarka, kokia jie pateikti sąraše.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-138">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="5b4ed-139">Naršymo kelio modulio įtraukimas į naują puslapį</span><span class="sxs-lookup"><span data-stu-id="5b4ed-139">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="5b4ed-140">Norėdami į PDP įtraukti naršymo kelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-140">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="5b4ed-141">Eikite į **Svetainės parametrai /> Plėtiniai**, tada pasirinkite parametro **Naršymo kelio rodymo tipas PDP** vertę **Rodyti kategorijų hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-141">Go to **Site Settings /> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="5b4ed-142">Eikite į **Šablonai** ir pasirinkite PDP šabloną.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-142">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="5b4ed-143">Vietoje **Konteineris**, kurioje yra pirkimo langelio modulis, pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-143">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5b4ed-144">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-144">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5b4ed-145">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-145">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="5b4ed-146">Eikite į **Puslapiai** ir atidarykite PDP, kuris naudoja PDP šabloną.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-146">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="5b4ed-147">Jei PDP dar nėra, sukurkite jį.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-147">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="5b4ed-148">Vietoje **Konteineris**, kurioje yra pirkimo langelio modulis, pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-148">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5b4ed-149">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-149">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5b4ed-150">Dalies **Naršymo kelias** ypatybių srityje, dalyje **Šaknis**, pasirinkite **Saito tekstas**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-150">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="5b4ed-151">Dialogo lange **Saito tekstas** įveskite **Pagrindinis**, tada dalyje **Saito paskirtis** pasirinkite **Įtraukti saitą**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-151">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="5b4ed-152">Dialogo lange **Įtraukti saitą** pasirinkite naršymo kelio šaknies saitą, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-152">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="5b4ed-153">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-153">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="5b4ed-154">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="5b4ed-154">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b4ed-155">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="5b4ed-155">Additional resources</span></span>

[<span data-ttu-id="5b4ed-156">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="5b4ed-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5b4ed-157">Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="5b4ed-157">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="5b4ed-158">Produktų rinkinio moduliai</span><span class="sxs-lookup"><span data-stu-id="5b4ed-158">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="5b4ed-159">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="5b4ed-159">Buy box module</span></span>](add-buy-box.md)
