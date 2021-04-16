---
title: Naršymo kelio modulis
description: Šioje temoje aprašomi „duonos trupinėlių“ (angl. breadcrumb) moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 10/20/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e7b7cff280d8c6bcb09f2f59d96ec415b9cc1167
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796203"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="41ec6-103">Naršymo kelio modulis</span><span class="sxs-lookup"><span data-stu-id="41ec6-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="41ec6-104">Šioje temoje aprašomi „duonos trupinėlių“ (angl. breadcrumb) moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="41ec6-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="41ec6-105">Naršymo kelio moduliai naudojami antrinei navigacijai svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="41ec6-105">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="41ec6-106">Jis paprastai rodomas puslapio viršuje, po antrašte.</span><span class="sxs-lookup"><span data-stu-id="41ec6-106">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="41ec6-107">Nors naršymo kelio modulius galima įtraukti į bet kurį puslapį, dažniausiai jie naudojami produkto informacijos puslapiuose (PDP), kad būtų rodoma produktų kategorijų hierarchija ir būtų užtikrintas greitas būdas naršyti po svetainę.</span><span class="sxs-lookup"><span data-stu-id="41ec6-107">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="41ec6-108">Naršymo kelio modulis taip pat gali būti naudojamas siekiant parodyti saitą „Atgal į rezultatus“, kai vartotojai atidaro PDP ieškos ar sąrašo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="41ec6-108">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="41ec6-109">Šitaip vartotojai gali greitai grįžti prie filtruoto sąrašo puslapio ir tęsti apsipirkimą.</span><span class="sxs-lookup"><span data-stu-id="41ec6-109">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="41ec6-110">Puslapiuose, kurie turi produktų kategorijos konteksto, pvz., PDP ir kategorijos puslapiuose, naršymo kelio moduliai rodo kategorijų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="41ec6-110">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="41ec6-111">Puslapiuose, kuriuose nėra kategorijos konteksto, naršymo kelio moduliai pagal numatytąją nuostatą rodo **&lt;Svetainės šaknis&gt; / &lt;Dabartinis puslapis&gt;**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-111">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="41ec6-112">Naršymo kelio modulius taip pat galima rankiniu būdu konfigūruoti ir kitų tipų svetainės puslapiuose, kad būtų rodomi saitai į konkrečius svetainės puslapius.</span><span class="sxs-lookup"><span data-stu-id="41ec6-112">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="41ec6-113">Naršymo kelio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.12 leidime.</span><span class="sxs-lookup"><span data-stu-id="41ec6-113">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="41ec6-114">Toliau pateiktame paveikslėlyje parodytas naršymo kelio modulio pavyzdys, rodantis kategorijų hierarchiją PDP.</span><span class="sxs-lookup"><span data-stu-id="41ec6-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Naršymo kelio modulio pavyzdys](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="41ec6-116">Naršymo modulio parametrai</span><span class="sxs-lookup"><span data-stu-id="41ec6-116">Breadcrumb module settings</span></span>

<span data-ttu-id="41ec6-117">Naršymo kelio modulis priklauso nuo parametro **Naršymo kelio rodymo tipas PDP**, kuris nurodytas svetainių daryklės dalyje **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="41ec6-118">Galimos trys šio parametro vertės:</span><span class="sxs-lookup"><span data-stu-id="41ec6-118">This setting has three possible values:</span></span>

- <span data-ttu-id="41ec6-119">**Rodyti kategorijų hierarchiją** – kai ši vertė pasirinkta, naudojant naršymo kelio modulį bus rodoma išsami PDP peržiūrimo produkto kategorijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="41ec6-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="41ec6-120">**Rodyti „atgal į rezultatus“** – kai ši vertė pasirinkta, naršymo kelio modulis rodo saitą „Atgal į rezultatus“ PDP, jei vartotojas atidarė PDP modulyje, kuriame galima naudoti saitą „Atgal į rezultatus“.</span><span class="sxs-lookup"><span data-stu-id="41ec6-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="41ec6-121">Šią funkciją galima, kai vartotojai naršo iš kategorijos, ieškos, sąrašo ir rekomendacijų sąrašų puslapių.</span><span class="sxs-lookup"><span data-stu-id="41ec6-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="41ec6-122">Tam, kad ši funkcija veiktų, produktų rinkinys ir ieškos rezultatų moduliai turi ypatybę, kuri pavadinta **Leisti grįžti į rezultatus PDP**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="41ec6-123">Ši ypatybė suteikia jums galimybę apibrėžti, kurie moduliai turi palaikyti saito „Atgal į rezultatus“ funkciją PDP.</span><span class="sxs-lookup"><span data-stu-id="41ec6-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="41ec6-124">Pavyzdžiui, kai pasirinkta naršymo kelio modulio parametro **Naršymo kelio rodymo tipas PDP** ypatybė **Rodyti „atgal į rezultatus“** ir pasirinkta ieškos puslapio ieškos rezultatų modulio ypatybė **Leisti grįžti į rezultatus PDP**, saitą „Atgal į rezultatus“ bus rodoma tada, kai vartotojai pereina iš ieškos puslapio į PDP.</span><span class="sxs-lookup"><span data-stu-id="41ec6-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="41ec6-125">**Rodyti kategorijų hierarchiją ir grįžimo į rezultatus saitą** – ši vertė yra ankstesnių dviejų verčių derinys.</span><span class="sxs-lookup"><span data-stu-id="41ec6-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="41ec6-126">Pasirinkus šią vertę, naudojant naršymo kelio modulį, PDP bus rodoma ir išsami kategorijų hierarchija ir saitą „Atgal į rezultatus“ (jei sukonfigūruota).</span><span class="sxs-lookup"><span data-stu-id="41ec6-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41ec6-127">Šie parametrai galimi „Dynamics 365 Commerce” 10.0.12 leidime.</span><span class="sxs-lookup"><span data-stu-id="41ec6-127">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="41ec6-128">Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="41ec6-128">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="41ec6-129">Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="41ec6-129">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="41ec6-130">Naršymo kelio modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="41ec6-130">Breadcrumb module properties</span></span>

| <span data-ttu-id="41ec6-131">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="41ec6-131">Property name</span></span> | <span data-ttu-id="41ec6-132">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="41ec6-132">Values</span></span> | <span data-ttu-id="41ec6-133">aprašymas</span><span class="sxs-lookup"><span data-stu-id="41ec6-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="41ec6-134">Šakninis</span><span class="sxs-lookup"><span data-stu-id="41ec6-134">Root</span></span> | <span data-ttu-id="41ec6-135">Tekstas arba saitas</span><span class="sxs-lookup"><span data-stu-id="41ec6-135">Text or link</span></span>| <span data-ttu-id="41ec6-136">Ši neprivaloma ypatybė nurodo naršymo kelio šakninės svetainės saito tekstą ir paskirtį.</span><span class="sxs-lookup"><span data-stu-id="41ec6-136">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="41ec6-137">Jei ši ypatybė nesukonfigūruota, šaknis nebus apibrėžta.</span><span class="sxs-lookup"><span data-stu-id="41ec6-137">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="41ec6-138">Naršymo kelio saitas</span><span class="sxs-lookup"><span data-stu-id="41ec6-138">Breadcrumb link</span></span> | <span data-ttu-id="41ec6-139">Saitas</span><span class="sxs-lookup"><span data-stu-id="41ec6-139">Link</span></span> | <span data-ttu-id="41ec6-140">Ši pasirenkama ypatybė nurodo neautomatiniu būdu sukonfigūruoto naršymo kelio saitus, jei šie saitai būtini.</span><span class="sxs-lookup"><span data-stu-id="41ec6-140">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="41ec6-141">Saitai rodomi tokia tvarka, kokia jie pateikti sąraše.</span><span class="sxs-lookup"><span data-stu-id="41ec6-141">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="41ec6-142">Naršymo kelio modulio įtraukimas į naują puslapį</span><span class="sxs-lookup"><span data-stu-id="41ec6-142">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="41ec6-143">Norėdami į PDP įtraukti naršymo kelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="41ec6-143">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="41ec6-144">Eikite į **Saito nustatymus \> Plėtiniai** ir tada **Naršymo kelio rodymo tipo PDP** nustatymuose pasirinkite **Rodyti kategorijos hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-144">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="41ec6-145">Eikite į **Šablonai** ir pasirinkite PDP šabloną.</span><span class="sxs-lookup"><span data-stu-id="41ec6-145">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="41ec6-146">Vietoje **Konteineris**, kurioje yra pirkimo langelio modulis, pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-146">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="41ec6-147">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-147">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="41ec6-148">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="41ec6-148">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="41ec6-149">Eikite į **Puslapiai** ir atidarykite PDP, kuris naudoja PDP šabloną.</span><span class="sxs-lookup"><span data-stu-id="41ec6-149">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="41ec6-150">Jei PDP dar nėra, sukurkite jį.</span><span class="sxs-lookup"><span data-stu-id="41ec6-150">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="41ec6-151">Vietoje **Konteineris**, kurioje yra pirkimo langelio modulis, pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-151">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="41ec6-152">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-152">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="41ec6-153">Dalies **Naršymo kelias** ypatybių srityje, dalyje **Šaknis**, pasirinkite **Saito tekstas**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-153">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="41ec6-154">Dialogo lange **Saito tekstas** įveskite **Pagrindinis**, tada dalyje **Saito paskirtis** pasirinkite **Įtraukti saitą**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-154">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="41ec6-155">Dialogo lange **Įtraukti saitą** pasirinkite naršymo kelio šaknies saitą, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-155">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="41ec6-156">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="41ec6-156">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="41ec6-157">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="41ec6-157">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41ec6-158">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="41ec6-158">Additional resources</span></span>

[<span data-ttu-id="41ec6-159">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="41ec6-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="41ec6-160">Naršymo meniu modulis</span><span class="sxs-lookup"><span data-stu-id="41ec6-160">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="41ec6-161">Svetainės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="41ec6-161">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="41ec6-162">Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="41ec6-162">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="41ec6-163">Produktų rinkinio moduliai</span><span class="sxs-lookup"><span data-stu-id="41ec6-163">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="41ec6-164">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="41ec6-164">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="41ec6-165">SDK ir modulių bibliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="41ec6-165">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]