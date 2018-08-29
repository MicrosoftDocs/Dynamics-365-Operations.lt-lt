---
title: "Mažmeninės prekybos produktų kategorijų ir produktų valdymas"
description: "Šioje temoje aprašoma, kaip reklamavimo vadovai gali naudoti mažmeninės prekybos produktų kategorijas ryšiams tarp mažmeninės prekybos produktų hierarchijos ir išsamios informacijos apie išleistus produktus valdyti."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 19c972164474c972aab642c3cccc67cf396a6cb2
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="3248d-103">Mažmeninės prekybos produktų kategorijų ir produktų valdymas</span><span class="sxs-lookup"><span data-stu-id="3248d-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="3248d-104">Šioje temoje aprašomas patobulintas būdas valdyti mažmeninės prekybos produktų kategorijas ir produktus sprendime „Microsoft Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="3248d-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="3248d-105">Dėl šių patobulinimų reklamavimo parduotuvėje vadovams leidžiama peržiūrėti produktų ypatybių struktūrą, bendrinamą tarp mažmeninės prekybos produktų hierarchijos ir išsamios informacijos apie išleistus produktus.</span><span class="sxs-lookup"><span data-stu-id="3248d-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="3248d-106">Norėdami sužinoti daugiau apie tai, kaip valdyti mažmeninės prekybos produktų kategorijas, darbo srityje **Kategorijų ir produktų valdymas** pasirinkite plytelę **Mažmeninės prekybos produktų hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="3248d-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="3248d-107">Atkreipkite dėmesį, į patobulintą rodomo puslapio **Mažmeninės prekybos produktų hierarchija** struktūrą.</span><span class="sxs-lookup"><span data-stu-id="3248d-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="3248d-108">Ankstesnėse „Retail“ versijose produktų ypatybės pagal jų taikomumą buvo suskirstytos į *pagrindines produktų ypatybes* ir *mažmeninės prekybos produktų ypatybes*.</span><span class="sxs-lookup"><span data-stu-id="3248d-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="3248d-109">Mažmeninės prekybos produkto ypatybės pagal taikomumą yra *visuotinos*.</span><span class="sxs-lookup"><span data-stu-id="3248d-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="3248d-110">Kitaip tariant, ta pati konkrečios „Retail“ produkto ypatybės reikšmė taikoma visiems juridiniams subjektams.</span><span class="sxs-lookup"><span data-stu-id="3248d-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="3248d-111">Priešingu atveju, pagrindinės produktų ypatybės yra taikomos *konkrečiam juridiniam subjektui*.</span><span class="sxs-lookup"><span data-stu-id="3248d-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="3248d-112">Kitaip tariant, juridinių subjektų naudojama konkrečios pagrindinės produktų ypatybės reikšmė gali skirtis priklausomai nuo atskirų kiekvieno juridinio subjekto verslo poreikių.</span><span class="sxs-lookup"><span data-stu-id="3248d-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="3248d-113">Patobulintoje mažmeninės prekybos produktų kategorijų struktūroje produktų ypatybės logiškai atskiriamos pagal jų taikomumą grupėje, kad būtų atspindėta išsamios išleisto produkto informacijos formos struktūra.</span><span class="sxs-lookup"><span data-stu-id="3248d-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Laukai, sugrupuoti pagal taikomumo ypatybes](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="3248d-115">Galite valdyti visų juridinių subjektų arba konkretaus juridinio subjekto ypatybes, taikomas konkrečiam juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="3248d-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="3248d-116">Norėdami valdyti ypatybes visuose juridiniuose subjektuose, pasirinkite **Peržiūrėti visus juridinius subjektus** (arba **Redaguoti visus juridinius subjektus**).</span><span class="sxs-lookup"><span data-stu-id="3248d-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Peržiūrėti / redaguoti visus juridinius subjektus](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="3248d-118">Norėdami valdyti konkretaus juridinio subjekto ypatybes, pasirinkite **Peržiūrėti konkretų juridinį subjektą** (arba **Redaguoti konkretų juridinį subjektą**).</span><span class="sxs-lookup"><span data-stu-id="3248d-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Peržiūrėti / redaguoti konkretų juridinį subjektą](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="3248d-120">Be to, patobulintoje mažmeninės prekybos produktų kategorijų struktūroje reklamavimo parduotuvėje vadovas dabar taip pat gali apibrėžti numatytąsias papildomo produktų ypatybių rinkinio reikšmes atskiros kategorijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="3248d-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="3248d-121">Tada, sukūrus produktų, šias numatytąsias produkto ypatybių reikšmes produktai paveldi pagal savo susiejimą su atskiros mažmeninės prekybos produktų hierarchijos kategorijos savybėmis.</span><span class="sxs-lookup"><span data-stu-id="3248d-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="3248d-122">Šias paveldėtas kiekvieno produkto ypatybes taip pat galima modifikuoti, kad būtų įvykdyti atskiri verslo reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="3248d-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="3248d-123">Produktų naujinimo ypatybių mažmeninės prekybos produktų hierarchijos puslapyje pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="3248d-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="3248d-124">Šią naują patobulintą produktų ypatybių struktūrą galite naudoti pasirinkdami atnaujintų produktų ypatybes, kurias reikia perkelti į susietus produktus.</span><span class="sxs-lookup"><span data-stu-id="3248d-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="3248d-125">Puslapio **Mažmeninės prekybos produktų hierarchija** veiksmų srityje pasirinkite **Kategorija**, tada pasirinkite **Naujinti produktus**, kad atidarytumėte dialogo langą **Produktų naujinimas**.</span><span class="sxs-lookup"><span data-stu-id="3248d-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Produktų naujinimo dialogo langas](media/NewUpdateProductsEnhancedView.PNG)


