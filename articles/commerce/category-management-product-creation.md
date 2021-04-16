---
title: Produktų kategorijų ir produktų valdymas
description: Šioje temoje aprašoma, kaip reklamavimo vadovai gali naudoti produktų kategorijas ryšiams tarp prekybos produktų hierarchijos ir išsamios informacijos apie išleistus produktus valdyti.
author: ashishmsft
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 678561856fbb5514ff954363a767091edac6dee2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794378"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="92c72-103">Produktų kategorijų ir produktų valdymas</span><span class="sxs-lookup"><span data-stu-id="92c72-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="92c72-104">Šioje temoje aprašomas patobulintas būdas valdyti produktų kategorijas ir produktus sprendime „Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="92c72-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="92c72-105">Dėl šių patobulinimų reklamavimo parduotuvėje vadovams leidžiama peržiūrėti produktų ypatybių struktūrą, bendrinamą tarp produktų hierarchijos ir išsamios informacijos apie išleistus produktus.</span><span class="sxs-lookup"><span data-stu-id="92c72-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="92c72-106">Norėdami sužinoti daugiau apie tai, kaip valdyti produktų kategorijas, darbo srityje **Kategorijų ir produktų valdymas** pasirinkite plytelę **Prekybos produktų hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="92c72-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="92c72-107">Atkreipkite dėmesį į patobulintą rodomo puslapio **Prekybos produktų hierarchija** struktūrą.</span><span class="sxs-lookup"><span data-stu-id="92c72-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="92c72-108">Ankstesnėse programos versijose produktų ypatybės pagal jų taikomumą buvo suskirstytos į *pagrindines produktų ypatybes* ir *Mažmeninės prekybos produktų ypatybes*.</span><span class="sxs-lookup"><span data-stu-id="92c72-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="92c72-109">Mažmeninės prekybos produkto ypatybės pagal taikomumą yra *visuotinos*.</span><span class="sxs-lookup"><span data-stu-id="92c72-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="92c72-110">Kitaip tariant, ta pati konkrečios produkto ypatybės reikšmė taikoma visiems juridiniams subjektams.</span><span class="sxs-lookup"><span data-stu-id="92c72-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="92c72-111">Priešingu atveju, pagrindinės produktų ypatybės yra taikomos *konkrečiam juridiniam subjektui*.</span><span class="sxs-lookup"><span data-stu-id="92c72-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="92c72-112">Kitaip tariant, juridinių subjektų naudojama konkrečios pagrindinės produktų ypatybės reikšmė gali skirtis priklausomai nuo atskirų kiekvieno juridinio subjekto verslo poreikių.</span><span class="sxs-lookup"><span data-stu-id="92c72-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="92c72-113">Patobulintoje produktų kategorijų struktūroje produktų ypatybės logiškai atskiriamos pagal jų taikomumą grupėje, kad būtų atspindėta išsamios išleisto produkto informacijos formos struktūra.</span><span class="sxs-lookup"><span data-stu-id="92c72-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Laukai, sugrupuoti pagal taikomumo ypatybes](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="92c72-115">Galite valdyti visų juridinių subjektų arba konkretaus juridinio subjekto ypatybes, taikomas konkrečiam juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="92c72-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="92c72-116">Norėdami valdyti ypatybes visuose juridiniuose subjektuose, pasirinkite **Peržiūrėti visus juridinius subjektus** (arba **Redaguoti visus juridinius subjektus**).</span><span class="sxs-lookup"><span data-stu-id="92c72-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Peržiūrėti / redaguoti visus juridinius subjektus](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="92c72-118">Norėdami valdyti konkretaus juridinio subjekto ypatybes, pasirinkite **Peržiūrėti konkretų juridinį subjektą** (arba **Redaguoti konkretų juridinį subjektą**).</span><span class="sxs-lookup"><span data-stu-id="92c72-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Peržiūrėti / redaguoti konkretų juridinį subjektą](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="92c72-120">Be to, patobulintoje produktų kategorijų struktūroje reklamavimo parduotuvėje vadovas dabar taip pat gali apibrėžti numatytąsias papildomo produktų ypatybių rinkinio reikšmes atskiros kategorijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="92c72-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="92c72-121">Tada, sukūrus produktų, šias numatytąsias produkto ypatybių reikšmes produktai paveldi pagal savo susiejimą su atskiros produktų hierarchijos kategorijos savybėmis.</span><span class="sxs-lookup"><span data-stu-id="92c72-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="92c72-122">Šias paveldėtas kiekvieno produkto ypatybes taip pat galima modifikuoti, kad būtų įvykdyti atskiri verslo reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="92c72-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="92c72-123">Produktų naujinimo ypatybių prekybos produktų hierarchijos puslapyje pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="92c72-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="92c72-124">Šią naują patobulintą produktų ypatybių struktūrą galite naudoti pasirinkdami atnaujintų produktų ypatybes, kurias reikia perkelti į susietus produktus.</span><span class="sxs-lookup"><span data-stu-id="92c72-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="92c72-125">Puslapio **Prekybos produktų hierarchija** veiksmų srityje pasirinkite **Kategorija**, tada pasirinkite **Naujinti produktus**, kad atidarytumėte dialogo langą **Produktų naujinimas**.</span><span class="sxs-lookup"><span data-stu-id="92c72-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Produktų naujinimo dialogo langas](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]