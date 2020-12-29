---
title: Svetainės išrinkiklio modulis
description: Šioje temoje paaiškinamas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: b4e5f715efcac7f883df99508d282db904be0d80
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665228"
---
# <a name="site-selector-module"></a><span data-ttu-id="11f39-103">Svetainės išrinkiklio modulis</span><span class="sxs-lookup"><span data-stu-id="11f39-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="11f39-104">Šioje temoje paaiškinamas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="11f39-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="11f39-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="11f39-105">Overview</span></span>

<span data-ttu-id="11f39-106">Kai įmonė turi įvairių svetainių rinkose, regionuose ir vietovėse, svetainės vartotojams reikia paprasto būdo perjungti svetaines ir pasirinkti pageidaujamą prekybos svetainę.</span><span class="sxs-lookup"><span data-stu-id="11f39-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="11f39-107">Kad vartotojai galėtų išpildyti šį poreikį, svetainės išrinkiklio modulis leidžia naršyti keliose svetainėse.</span><span class="sxs-lookup"><span data-stu-id="11f39-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="11f39-108">Svetainės išrinkiklio modulis turi būti sukonfigūruotas naudojant rinkų, regionų ar vietovių svetainių, kuriose vartotojai gali naršyti, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="11f39-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="11f39-109">Svetainės išrinkiklio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.14 leidime.</span><span class="sxs-lookup"><span data-stu-id="11f39-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="11f39-110">Toliau pateiktoje iliustracijoje parodytas svetainės išrinkiklio modulio, kuris rodomas svetainės puslapio antraštėje, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="11f39-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Svetainės išrinkiklio modulio, esančio svetainės puslapio antraštėje, pavyzdys](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="11f39-112">Svetainės išrinkiklio modulio ypatybės</span><span class="sxs-lookup"><span data-stu-id="11f39-112">Site selector module properties</span></span>

| <span data-ttu-id="11f39-113">Ypatybės pavadinimas</span><span class="sxs-lookup"><span data-stu-id="11f39-113">Property name</span></span> | <span data-ttu-id="11f39-114">Reikšmė</span><span class="sxs-lookup"><span data-stu-id="11f39-114">Value</span></span>                 | <span data-ttu-id="11f39-115">Aprašas</span><span class="sxs-lookup"><span data-stu-id="11f39-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="11f39-116">Antraštė</span><span class="sxs-lookup"><span data-stu-id="11f39-116">Heading</span></span>       | <span data-ttu-id="11f39-117">Tekstas</span><span class="sxs-lookup"><span data-stu-id="11f39-117">Text</span></span>                  | <span data-ttu-id="11f39-118">Modulio antraštė.</span><span class="sxs-lookup"><span data-stu-id="11f39-118">The heading for the module.</span></span> |
| <span data-ttu-id="11f39-119">Svetainės parinktys</span><span class="sxs-lookup"><span data-stu-id="11f39-119">Site options</span></span>  | <span data-ttu-id="11f39-120">Pavadinimas, vaizdas, URL</span><span class="sxs-lookup"><span data-stu-id="11f39-120">Name, Image, URL</span></span>      | <span data-ttu-id="11f39-121">Ši ypatybė nurodo pavadinimą, saitą su pagrindiniu svetainės puslapiu ir pasirinktinį kiekvienos į modulį įtrauktos svetainės vaizdą.</span><span class="sxs-lookup"><span data-stu-id="11f39-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="11f39-122">Šis vaizdas gali būti vėliavėlė arba tam tikras rinkos, regiono ar vietovės atvaizdavimas.</span><span class="sxs-lookup"><span data-stu-id="11f39-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="11f39-123">Svetainės išrinkiklio modulio įtraukimas į puslapį</span><span class="sxs-lookup"><span data-stu-id="11f39-123">Add a site selector module to a page</span></span>

<span data-ttu-id="11f39-124">Svetainės išrinkiklio modulį galima įtraukti į [antraštės modulį](author-header-module.md), esantį svetainės išrinkiklio vietoje.</span><span class="sxs-lookup"><span data-stu-id="11f39-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="11f39-125">Po jo įtraukimo galite nurodyti modulio antraštę ir svetainės parinktis.</span><span class="sxs-lookup"><span data-stu-id="11f39-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11f39-126">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="11f39-126">Additional resources</span></span>

[<span data-ttu-id="11f39-127">Modulių bibliotekos peržiūra</span><span class="sxs-lookup"><span data-stu-id="11f39-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="11f39-128">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="11f39-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="11f39-129">Naršymo kelio modulis</span><span class="sxs-lookup"><span data-stu-id="11f39-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="11f39-130">Naršymo meniu modulis</span><span class="sxs-lookup"><span data-stu-id="11f39-130">Navigation menu module</span></span>](nav-menu-module.md)
