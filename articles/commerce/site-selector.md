---
title: Svetainės išrinkiklio modulis
description: Šioje temoje paaiškinamas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6e8eefe7afe385ca77eca6027638ff938e1356e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791780"
---
# <a name="site-selector-module"></a><span data-ttu-id="0203a-103">Svetainės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="0203a-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0203a-104">Šioje temoje paaiškinamas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="0203a-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0203a-105">Kai įmonė turi įvairių svetainių rinkose, regionuose ir vietovėse, svetainės vartotojams reikia paprasto būdo perjungti svetaines ir pasirinkti pageidaujamą prekybos svetainę.</span><span class="sxs-lookup"><span data-stu-id="0203a-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="0203a-106">Kad vartotojai galėtų išpildyti šį poreikį, svetainės išrinkiklio modulis leidžia naršyti keliose svetainėse.</span><span class="sxs-lookup"><span data-stu-id="0203a-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="0203a-107">Svetainės išrinkiklio modulis turi būti sukonfigūruotas naudojant rinkų, regionų ar vietovių svetainių, kuriose vartotojai gali naršyti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="0203a-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="0203a-108">Svetainės išrinkiklio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.14 leidime.</span><span class="sxs-lookup"><span data-stu-id="0203a-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="0203a-109">Toliau pateiktoje iliustracijoje parodytas svetainės išrinkiklio modulio, kuris rodomas svetainės puslapio antraštėje, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="0203a-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Svetainės išrinkiklio modulio, esančio svetainės puslapio antraštėje, pavyzdys](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="0203a-111">Svetainės išrinkiklio modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="0203a-111">Site selector module properties</span></span>

| <span data-ttu-id="0203a-112">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="0203a-112">Property name</span></span> | <span data-ttu-id="0203a-113">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="0203a-113">Value</span></span>                 | <span data-ttu-id="0203a-114">Aprašas</span><span class="sxs-lookup"><span data-stu-id="0203a-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="0203a-115">Antraštė</span><span class="sxs-lookup"><span data-stu-id="0203a-115">Heading</span></span>       | <span data-ttu-id="0203a-116">Tekstas</span><span class="sxs-lookup"><span data-stu-id="0203a-116">Text</span></span>                  | <span data-ttu-id="0203a-117">Modulio antraštė.</span><span class="sxs-lookup"><span data-stu-id="0203a-117">The heading for the module.</span></span> |
| <span data-ttu-id="0203a-118">Svetainės parinktys</span><span class="sxs-lookup"><span data-stu-id="0203a-118">Site options</span></span>  | <span data-ttu-id="0203a-119">Pavadinimas, vaizdas, URL</span><span class="sxs-lookup"><span data-stu-id="0203a-119">Name, Image, URL</span></span>      | <span data-ttu-id="0203a-120">Ši ypatybė nurodo pavadinimą, saitą su pagrindiniu svetainės puslapiu ir pasirinktinį kiekvienos į modulį įtrauktos svetainės vaizdą.</span><span class="sxs-lookup"><span data-stu-id="0203a-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="0203a-121">Šis vaizdas gali būti vėliavėlė arba tam tikras rinkos, regiono ar vietovės atvaizdavimas.</span><span class="sxs-lookup"><span data-stu-id="0203a-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="0203a-122">Svetainės išrinkiklio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="0203a-122">Add a site selector module to a page</span></span>

<span data-ttu-id="0203a-123">Svetainės išrinkiklio modulį galima įtraukti į [antraštės modulį](author-header-module.md), esantį svetainės išrinkiklio vietoje.</span><span class="sxs-lookup"><span data-stu-id="0203a-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="0203a-124">Po jo įtraukimo galite nurodyti modulio antraštę ir svetainės parinktis.</span><span class="sxs-lookup"><span data-stu-id="0203a-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0203a-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0203a-125">Additional resources</span></span>

[<span data-ttu-id="0203a-126">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="0203a-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0203a-127">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="0203a-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0203a-128">Naršymo kelio modulis</span><span class="sxs-lookup"><span data-stu-id="0203a-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="0203a-129">Naršymo meniu modulis</span><span class="sxs-lookup"><span data-stu-id="0203a-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]