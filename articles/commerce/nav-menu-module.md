---
title: Naršymo meniu modulis
description: Šioje temoje aprašomi naršymo meniu moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761409"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="b1530-103">Naršymo meniu modulis</span><span class="sxs-lookup"><span data-stu-id="b1530-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b1530-104">Šioje temoje aprašomi naršymo meniu moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.</span><span class="sxs-lookup"><span data-stu-id="b1530-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b1530-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="b1530-105">Overview</span></span>

<span data-ttu-id="b1530-106">Pagrindinė naršymo meniu modulių paskirtis yra leisti svetainių vartotojams naršyti produktus ir svetainių puslapius pagal kanalo naršymo hierarchiją, nustatytą „Dynamics 365 Commerce Headquarters”.</span><span class="sxs-lookup"><span data-stu-id="b1530-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="b1530-107">Naršymo meniu modulyje sukonfigūruotos prekės rodomos kaip svetainės antraštės naršymo elementai.</span><span class="sxs-lookup"><span data-stu-id="b1530-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="b1530-108">Naršymo meniu moduliai taip pat palaiko statinius meniu elementus, kurie susieti su kitais „e-Commerce” svetainės puslapiais.</span><span class="sxs-lookup"><span data-stu-id="b1530-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="b1530-109">Naršymo meniu modulį galima įtraukti į puslapio antraštės modulį.</span><span class="sxs-lookup"><span data-stu-id="b1530-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="b1530-110">„Fabrikam” temos naršymo meniu pagal numatytuosius nustatymus pateikiami du lygiai.</span><span class="sxs-lookup"><span data-stu-id="b1530-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="b1530-111">Darbo pradžios temos naršymo meniu pagal numatytuosius nustatymus pateikiami trys lygiai.</span><span class="sxs-lookup"><span data-stu-id="b1530-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="b1530-112">Norint pakeisti lygių skaičių, temoje reikalingas peržiūros plėtinys.</span><span class="sxs-lookup"><span data-stu-id="b1530-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="b1530-113">Toliau pateiktoje iliustracijoje parodytas „Fabrikam” svetainės naršymo meniu pavyzdys, kuriame yra du kategorijų hierarchijos lygiai ir keli statiniai meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="b1530-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="b1530-114">![Naršymo meniu modulio pavyzdys](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="b1530-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="b1530-115">Naršymo meniu modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="b1530-115">Navigation menu module properties</span></span>

| <span data-ttu-id="b1530-116">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="b1530-116">Property name</span></span>             | <span data-ttu-id="b1530-117">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="b1530-117">Value</span></span>                 | <span data-ttu-id="b1530-118">Aprašas</span><span class="sxs-lookup"><span data-stu-id="b1530-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b1530-119">Šaltinis</span><span class="sxs-lookup"><span data-stu-id="b1530-119">Source</span></span>                  | <span data-ttu-id="b1530-120">**„Retail”** , **Kūrimas neautomatiniu būdu** , **„Retail” ir kūrimas neautomatiniu būdu**</span><span class="sxs-lookup"><span data-stu-id="b1530-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="b1530-121">Reikšmė **„Retail”** leidžia naršymo meniu rodyti „Commerce Headquarters” kanalų naršymo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="b1530-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="b1530-122">Reikšmė **Kūrimas neautomatiniu būdu** leidžia kuruoti statinius meniu elementus.</span><span class="sxs-lookup"><span data-stu-id="b1530-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="b1530-123">Reikšmė **„Retail” ir kūrimas neautomatiniu būdu** leidžia abiejų reikšmių derinį.</span><span class="sxs-lookup"><span data-stu-id="b1530-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="b1530-124">Rodyti kategorijos vaizdus</span><span class="sxs-lookup"><span data-stu-id="b1530-124">Show category images</span></span> | <span data-ttu-id="b1530-125">**Teisinga** arba **Klaidinga**</span><span class="sxs-lookup"><span data-stu-id="b1530-125">**True** or **False**</span></span>    | <span data-ttu-id="b1530-126">Įjungus Ši ypatybė naršymo meniu rodo kategorijos atvaizdus, kaip nurodyta kiekvienos kategorijos "Commerce Headquarters".</span><span class="sxs-lookup"><span data-stu-id="b1530-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="b1530-127">Įtraukta į „Commerce” 10.0.14 leidimą.</span><span class="sxs-lookup"><span data-stu-id="b1530-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="b1530-128">Statinis meniu elementas</span><span class="sxs-lookup"><span data-stu-id="b1530-128">Static menu item</span></span>| <span data-ttu-id="b1530-129">Reikšmių masyvas</span><span class="sxs-lookup"><span data-stu-id="b1530-129">Array of values</span></span>| <span data-ttu-id="b1530-130">Statiniai meniu elementai, susiejantys meniu elemento pavadinimą su statinio svetainės puslapio saitu.</span><span class="sxs-lookup"><span data-stu-id="b1530-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="b1530-131">Galite kurti meniu elementus po kitais meniu elementais.</span><span class="sxs-lookup"><span data-stu-id="b1530-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="b1530-132">Pagal numatytuosius nustatymus statiniai meniu rodomi šakniniame lygyje ir yra pridedami prie kanalų naršymo hierarchijos, jei tokia yra.</span><span class="sxs-lookup"><span data-stu-id="b1530-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="b1530-133">Toliau pateiktame paveikslėlyje parodytas kategorijos vaizdo, rodomo „Fabrikam“ svetainės naršymo meniu, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="b1530-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="b1530-134">![Naršymo meniu modulio su kategorijos vaizdais pavyzdys](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="b1530-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="b1530-135">Naršymo meniu modulio įtraukimas į antraštės modulį</span><span class="sxs-lookup"><span data-stu-id="b1530-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="b1530-136">Daugiau informacijos apie tai, kaip įtraukti naršymo meniu modulį į antraštės modulį, žr. [Antraštės modulis](author-header-module.md) .</span><span class="sxs-lookup"><span data-stu-id="b1530-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1530-137">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b1530-137">Additional resources</span></span>

[<span data-ttu-id="b1530-138">Darbo pradžios rinkinio apžvalga</span><span class="sxs-lookup"><span data-stu-id="b1530-138">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b1530-139">Pirkimo langelio modulis</span><span class="sxs-lookup"><span data-stu-id="b1530-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b1530-140">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="b1530-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="b1530-141">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="b1530-141">Header module</span></span>](author-header-module.md)
