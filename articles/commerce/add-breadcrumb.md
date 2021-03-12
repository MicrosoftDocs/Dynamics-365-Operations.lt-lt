---
title: Naršymo kelio modulis
description: Šioje temoje aprašomi naršymo kelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 1883281c62575ae0b48b6e584876185bb179b4f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986084"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="6ee97-103">Naršymo kelio modulis</span><span class="sxs-lookup"><span data-stu-id="6ee97-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ee97-104">Šioje temoje aprašomi naršymo kelio moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="6ee97-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6ee97-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="6ee97-105">Overview</span></span>

<span data-ttu-id="6ee97-106">Naršymo kelio moduliai naudojami antrinei navigacijai svetainės puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="6ee97-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="6ee97-107">Jis paprastai rodomas puslapio viršuje, po antrašte.</span><span class="sxs-lookup"><span data-stu-id="6ee97-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="6ee97-108">Nors naršymo kelio modulius galima įtraukti į bet kurį puslapį, dažniausiai jie naudojami produkto informacijos puslapiuose (PDP), kad būtų rodoma produktų kategorijų hierarchija ir būtų užtikrintas greitas būdas naršyti po svetainę.</span><span class="sxs-lookup"><span data-stu-id="6ee97-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="6ee97-109">Naršymo kelio modulis taip pat gali būti naudojamas siekiant parodyti saitą „Atgal į rezultatus“, kai vartotojai atidaro PDP ieškos ar sąrašo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="6ee97-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="6ee97-110">Šitaip vartotojai gali greitai grįžti prie filtruoto sąrašo puslapio ir tęsti apsipirkimą.</span><span class="sxs-lookup"><span data-stu-id="6ee97-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="6ee97-111">Puslapiuose, kurie turi produktų kategorijos konteksto, pvz., PDP ir kategorijos puslapiuose, naršymo kelio moduliai rodo kategorijų hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="6ee97-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="6ee97-112">Puslapiuose, kuriuose nėra kategorijos konteksto, naršymo kelio moduliai pagal numatytąją nuostatą rodo **&lt;Svetainės šaknis&gt; / &lt;Dabartinis puslapis&gt;**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="6ee97-113">Naršymo kelio modulius taip pat galima rankiniu būdu konfigūruoti ir kitų tipų svetainės puslapiuose, kad būtų rodomi saitai į konkrečius svetainės puslapius.</span><span class="sxs-lookup"><span data-stu-id="6ee97-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="6ee97-114">Naršymo kelio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.12 leidime.</span><span class="sxs-lookup"><span data-stu-id="6ee97-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="6ee97-115">Toliau pateiktame paveikslėlyje parodytas naršymo kelio modulio pavyzdys, rodantis kategorijų hierarchiją PDP.</span><span class="sxs-lookup"><span data-stu-id="6ee97-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Naršymo kelio modulio pavyzdys](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="6ee97-117">Naršymo modulio parametrai</span><span class="sxs-lookup"><span data-stu-id="6ee97-117">Breadcrumb module settings</span></span>

<span data-ttu-id="6ee97-118">Naršymo kelio modulis priklauso nuo parametro **Naršymo kelio rodymo tipas PDP**, kuris nurodytas svetainių daryklės dalyje **Svetainės parametrai \> Plėtiniai**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="6ee97-119">Galimos trys šio parametro vertės:</span><span class="sxs-lookup"><span data-stu-id="6ee97-119">This setting has three possible values:</span></span>

- <span data-ttu-id="6ee97-120">**Rodyti kategorijų hierarchiją** – kai ši vertė pasirinkta, naudojant naršymo kelio modulį bus rodoma išsami PDP peržiūrimo produkto kategorijų hierarchija.</span><span class="sxs-lookup"><span data-stu-id="6ee97-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="6ee97-121">**Rodyti „atgal į rezultatus“** – kai ši vertė pasirinkta, naršymo kelio modulis rodo saitą „Atgal į rezultatus“ PDP, jei vartotojas atidarė PDP modulyje, kuriame galima naudoti saitą „Atgal į rezultatus“.</span><span class="sxs-lookup"><span data-stu-id="6ee97-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="6ee97-122">Šią funkciją galima, kai vartotojai naršo iš kategorijos, ieškos, sąrašo ir rekomendacijų sąrašų puslapių.</span><span class="sxs-lookup"><span data-stu-id="6ee97-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="6ee97-123">Tam, kad ši funkcija veiktų, produktų rinkinys ir ieškos rezultatų moduliai turi ypatybę, kuri pavadinta **Leisti grįžti į rezultatus PDP**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="6ee97-124">Ši ypatybė suteikia jums galimybę apibrėžti, kurie moduliai turi palaikyti saito „Atgal į rezultatus“ funkciją PDP.</span><span class="sxs-lookup"><span data-stu-id="6ee97-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="6ee97-125">Pavyzdžiui, kai pasirinkta naršymo kelio modulio parametro **Naršymo kelio rodymo tipas PDP** ypatybė **Rodyti „atgal į rezultatus“** ir pasirinkta ieškos puslapio ieškos rezultatų modulio ypatybė **Leisti grįžti į rezultatus PDP**, saitą „Atgal į rezultatus“ bus rodoma tada, kai vartotojai pereina iš ieškos puslapio į PDP.</span><span class="sxs-lookup"><span data-stu-id="6ee97-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="6ee97-126">**Rodyti kategorijų hierarchiją ir grįžimo į rezultatus saitą** – ši vertė yra ankstesnių dviejų verčių derinys.</span><span class="sxs-lookup"><span data-stu-id="6ee97-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="6ee97-127">Pasirinkus šią vertę, naudojant naršymo kelio modulį, PDP bus rodoma ir išsami kategorijų hierarchija ir saitą „Atgal į rezultatus“ (jei sukonfigūruota).</span><span class="sxs-lookup"><span data-stu-id="6ee97-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ee97-128">Šie parametrai galimi „Dynamics 365 Commerce” 10.0.12 leidime.</span><span class="sxs-lookup"><span data-stu-id="6ee97-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="6ee97-129">Jei atnaujinate iš senesnės „Dynamics 365 Commerce” versijos, turite rankiniu būdu atnaujinti failą appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="6ee97-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="6ee97-130">Instrukcijų, kaip atnaujinti failą appsettings.json, žr. [SDK ir modulių bibliotekos naujinimai](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="6ee97-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="6ee97-131">Naršymo kelio modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="6ee97-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="6ee97-132">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="6ee97-132">Property name</span></span> | <span data-ttu-id="6ee97-133">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="6ee97-133">Values</span></span> | <span data-ttu-id="6ee97-134">aprašymas</span><span class="sxs-lookup"><span data-stu-id="6ee97-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="6ee97-135">Šakninis</span><span class="sxs-lookup"><span data-stu-id="6ee97-135">Root</span></span> | <span data-ttu-id="6ee97-136">Tekstas arba saitas</span><span class="sxs-lookup"><span data-stu-id="6ee97-136">Text or link</span></span>| <span data-ttu-id="6ee97-137">Ši neprivaloma ypatybė nurodo naršymo kelio šakninės svetainės saito tekstą ir paskirtį.</span><span class="sxs-lookup"><span data-stu-id="6ee97-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="6ee97-138">Jei ši ypatybė nesukonfigūruota, šaknis nebus apibrėžta.</span><span class="sxs-lookup"><span data-stu-id="6ee97-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="6ee97-139">Naršymo kelio saitas</span><span class="sxs-lookup"><span data-stu-id="6ee97-139">Breadcrumb link</span></span> | <span data-ttu-id="6ee97-140">Saitas</span><span class="sxs-lookup"><span data-stu-id="6ee97-140">Link</span></span> | <span data-ttu-id="6ee97-141">Ši pasirenkama ypatybė nurodo neautomatiniu būdu sukonfigūruoto naršymo kelio saitus, jei šie saitai būtini.</span><span class="sxs-lookup"><span data-stu-id="6ee97-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="6ee97-142">Saitai rodomi tokia tvarka, kokia jie pateikti sąraše.</span><span class="sxs-lookup"><span data-stu-id="6ee97-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="6ee97-143">Naršymo kelio modulio įtraukimas į naują puslapį</span><span class="sxs-lookup"><span data-stu-id="6ee97-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="6ee97-144">Norėdami į PDP įtraukti naršymo kelio modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ee97-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6ee97-145">Eikite į **Saito nustatymus \> Plėtiniai** ir tada **Naršymo kelio rodymo tipo PDP** nustatymuose pasirinkite **Rodyti kategorijos hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-145">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="6ee97-146">Eikite į **Šablonai** ir pasirinkite PDP šabloną.</span><span class="sxs-lookup"><span data-stu-id="6ee97-146">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="6ee97-147">Vietoje **Konteineris**, kurioje yra pirkimo langelio modulis, pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-147">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6ee97-148">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6ee97-149">Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="6ee97-149">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6ee97-150">Eikite į **Puslapiai** ir atidarykite PDP, kuris naudoja PDP šabloną.</span><span class="sxs-lookup"><span data-stu-id="6ee97-150">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="6ee97-151">Jei PDP dar nėra, sukurkite jį.</span><span class="sxs-lookup"><span data-stu-id="6ee97-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="6ee97-152">Vietoje **Konteineris**, kurioje yra pirkimo langelio modulis, pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-152">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6ee97-153">Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6ee97-154">Dalies **Naršymo kelias** ypatybių srityje, dalyje **Šaknis**, pasirinkite **Saito tekstas**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-154">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="6ee97-155">Dialogo lange **Saito tekstas** įveskite **Pagrindinis**, tada dalyje **Saito paskirtis** pasirinkite **Įtraukti saitą**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-155">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="6ee97-156">Dialogo lange **Įtraukti saitą** pasirinkite naršymo kelio šaknies saitą, tada – **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="6ee97-157">Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="6ee97-157">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="6ee97-158">Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.</span><span class="sxs-lookup"><span data-stu-id="6ee97-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ee97-159">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6ee97-159">Additional resources</span></span>

[<span data-ttu-id="6ee97-160">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="6ee97-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6ee97-161">Naršymo meniu modulis</span><span class="sxs-lookup"><span data-stu-id="6ee97-161">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="6ee97-162">Svetainės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="6ee97-162">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="6ee97-163">Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga</span><span class="sxs-lookup"><span data-stu-id="6ee97-163">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="6ee97-164">Produktų rinkinio moduliai</span><span class="sxs-lookup"><span data-stu-id="6ee97-164">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="6ee97-165">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="6ee97-165">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6ee97-166">SDK ir modulių bibliotekos naujinimai</span><span class="sxs-lookup"><span data-stu-id="6ee97-166">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
