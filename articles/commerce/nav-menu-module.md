---
title: Naršymo meniu modulis
description: Šioje temoje aprašomi naršymo meniu moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055742"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="4fe62-103">Naršymo meniu modulis</span><span class="sxs-lookup"><span data-stu-id="4fe62-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4fe62-104">Šioje temoje aprašomi naršymo meniu moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="4fe62-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4fe62-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="4fe62-105">Overview</span></span>

<span data-ttu-id="4fe62-106">Pagrindinė naršymo meniu modulių paskirtis yra leisti svetainių vartotojams naršyti produktus ir svetainių puslapius pagal kanalo naršymo hierarchiją, nustatytą „Dynamics 365 Commerce Headquarters”.</span><span class="sxs-lookup"><span data-stu-id="4fe62-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="4fe62-107">Naršymo meniu modulyje sukonfigūruotos prekės rodomos kaip svetainės antraštės naršymo elementai.</span><span class="sxs-lookup"><span data-stu-id="4fe62-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="4fe62-108">Naršymo meniu moduliai taip pat palaiko statinius meniu elementus, kurie susieti su kitais „e-Commerce” svetainės puslapiais.</span><span class="sxs-lookup"><span data-stu-id="4fe62-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="4fe62-109">Naršymo meniu modulį galima įtraukti į puslapio antraštės modulį.</span><span class="sxs-lookup"><span data-stu-id="4fe62-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="4fe62-110">„Fabrikam” temos naršymo meniu pagal numatytuosius nustatymus pateikiami du lygiai.</span><span class="sxs-lookup"><span data-stu-id="4fe62-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="4fe62-111">Darbo pradžios temos naršymo meniu pagal numatytuosius nustatymus pateikiami trys lygiai.</span><span class="sxs-lookup"><span data-stu-id="4fe62-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="4fe62-112">Norint pakeisti lygių skaičių, temoje reikalingas peržiūros plėtinys.</span><span class="sxs-lookup"><span data-stu-id="4fe62-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="4fe62-113">Toliau pateiktoje iliustracijoje parodytas „Fabrikam” svetainės naršymo meniu pavyzdys, kuriame yra du kategorijų hierarchijos lygiai ir keli statiniai meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="4fe62-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="4fe62-114">![Naršymo meniu modulio pavyzdys](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="4fe62-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="4fe62-115">Naršymo meniu modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="4fe62-115">Navigation menu module properties</span></span>

| <span data-ttu-id="4fe62-116">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="4fe62-116">Property name</span></span>             | <span data-ttu-id="4fe62-117">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="4fe62-117">Value</span></span>                 | <span data-ttu-id="4fe62-118">Aprašas</span><span class="sxs-lookup"><span data-stu-id="4fe62-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="4fe62-119">Šaltinis</span><span class="sxs-lookup"><span data-stu-id="4fe62-119">Source</span></span>                  | <span data-ttu-id="4fe62-120">**„Retail”** , **Kūrimas neautomatiniu būdu** , **„Retail” ir kūrimas neautomatiniu būdu**</span><span class="sxs-lookup"><span data-stu-id="4fe62-120">**Retail** , **Manual authoring** , **Retail and manual authoring**</span></span> | <span data-ttu-id="4fe62-121">Reikšmė **„Retail”** leidžia naršymo meniu rodyti „Commerce Headquarters” kanalų naršymo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="4fe62-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="4fe62-122">Reikšmė **Kūrimas neautomatiniu būdu** leidžia kuruoti statinius meniu elementus.</span><span class="sxs-lookup"><span data-stu-id="4fe62-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="4fe62-123">Reikšmė **„Retail” ir kūrimas neautomatiniu būdu** leidžia abiejų reikšmių derinį.</span><span class="sxs-lookup"><span data-stu-id="4fe62-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="4fe62-124">Rodyti kategorijos vaizdus</span><span class="sxs-lookup"><span data-stu-id="4fe62-124">Show category images</span></span> | <span data-ttu-id="4fe62-125">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="4fe62-125">**True** or **False**</span></span>    | <span data-ttu-id="4fe62-126">Įjungus Ši ypatybė naršymo meniu rodo kategorijos atvaizdus, kaip nurodyta kiekvienos kategorijos "Commerce Headquarters".</span><span class="sxs-lookup"><span data-stu-id="4fe62-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="4fe62-127">Įtraukta į „Commerce” 10.0.14 leidimą.</span><span class="sxs-lookup"><span data-stu-id="4fe62-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="4fe62-128">Įjungti kelių lygių naršymo meniu</span><span class="sxs-lookup"><span data-stu-id="4fe62-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="4fe62-129">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="4fe62-129">**True** or **False**</span></span> | <span data-ttu-id="4fe62-130">Kai ši ypatybė įjungta, naršymo meniu gali rodyti kelis naršymo hierarchijos lygius.</span><span class="sxs-lookup"><span data-stu-id="4fe62-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="4fe62-131">Ši funkcija pasiekiama „Dynamics 365 Commerce“ 10.0.15 leidime.</span><span class="sxs-lookup"><span data-stu-id="4fe62-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="4fe62-132">Lygių skaičius</span><span class="sxs-lookup"><span data-stu-id="4fe62-132">Number of levels</span></span> | <span data-ttu-id="4fe62-133">sveikasis skaičius</span><span class="sxs-lookup"><span data-stu-id="4fe62-133">integer</span></span> | <span data-ttu-id="4fe62-134">Ši ypatybė nurodo lygių, kurie turėtų būti rodomi, jei ypatybė **Įjungti kelių lygių naršymo meniu** nustatyta į **Teisinga** , skaičių.</span><span class="sxs-lookup"><span data-stu-id="4fe62-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="4fe62-135">Statinis meniu elementas</span><span class="sxs-lookup"><span data-stu-id="4fe62-135">Static menu item</span></span>| <span data-ttu-id="4fe62-136">Reikšmių masyvas</span><span class="sxs-lookup"><span data-stu-id="4fe62-136">Array of values</span></span>| <span data-ttu-id="4fe62-137">Statiniai meniu elementai, susiejantys meniu elemento pavadinimą su statinio svetainės puslapio saitu.</span><span class="sxs-lookup"><span data-stu-id="4fe62-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="4fe62-138">Galite kurti meniu elementus po kitais meniu elementais.</span><span class="sxs-lookup"><span data-stu-id="4fe62-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="4fe62-139">Pagal numatytuosius nustatymus statiniai meniu rodomi šakniniame lygyje ir yra pridedami prie kanalų naršymo hierarchijos, jei tokia yra.</span><span class="sxs-lookup"><span data-stu-id="4fe62-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="4fe62-140">Rodyti šakninį meniu</span><span class="sxs-lookup"><span data-stu-id="4fe62-140">Show root menu</span></span> | <span data-ttu-id="4fe62-141">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="4fe62-141">**True** or **False**</span></span> | <span data-ttu-id="4fe62-142">Kai ši ypatybė įjungta, naršymo meniu gali būti nustatytas pagal pasirinktinę šaknį (pvz., **Pirkti dabar** ).</span><span class="sxs-lookup"><span data-stu-id="4fe62-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now** ).</span></span> <span data-ttu-id="4fe62-143">Ši funkcija pasiekiama „Dynamics 365 Commerce“ 10.0.15 leidime.</span><span class="sxs-lookup"><span data-stu-id="4fe62-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="4fe62-144">Šakninis meniu</span><span class="sxs-lookup"><span data-stu-id="4fe62-144">Root menu</span></span> | <span data-ttu-id="4fe62-145">eilutė</span><span class="sxs-lookup"><span data-stu-id="4fe62-145">string</span></span> | <span data-ttu-id="4fe62-146">Ši ypatybė gali būti naudojama norint nustatyti pasirinktinės šaknies tekstą, jei ypatybė **Rodyti šakninį meniu** nustatyta į **Teisinga**.</span><span class="sxs-lookup"><span data-stu-id="4fe62-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="4fe62-147">Toliau pateiktame paveikslėlyje parodytas kategorijos vaizdo, rodomo „Fabrikam“ svetainės naršymo meniu, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="4fe62-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="4fe62-148">![Naršymo meniu modulio su kategorijos vaizdais pavyzdys](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="4fe62-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="4fe62-149">Naršymo meniu modulio įtraukimas į antraštės modulį</span><span class="sxs-lookup"><span data-stu-id="4fe62-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="4fe62-150">Daugiau informacijos apie tai, kaip įtraukti naršymo meniu modulį į antraštės modulį, žr. [Antraštės modulis](author-header-module.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe62-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fe62-151">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="4fe62-151">Additional resources</span></span>

[<span data-ttu-id="4fe62-152">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="4fe62-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4fe62-153">Naršymo kelio modulis</span><span class="sxs-lookup"><span data-stu-id="4fe62-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="4fe62-154">Svetainės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="4fe62-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="4fe62-155">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="4fe62-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4fe62-156">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="4fe62-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="4fe62-157">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="4fe62-157">Header module</span></span>](author-header-module.md)
