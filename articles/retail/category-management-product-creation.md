---
title: "Produktų kategorijų valdymas"
description: "Šioje temoje aprašoma, kaip reklamavimo parduotuvėje vadovai naudodami mažmeninės prekybos produktų kategorijas gali valdyti ryšius tarp mažmeninės prekybos produktų hierarchijos ir išsamios informacijos apie išleistus produktus."
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
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: lt-lt
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="d0798-103">Patobulintas produktų ir kategorijų valdymas</span><span class="sxs-lookup"><span data-stu-id="d0798-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="d0798-104">Šioje temoje aprašomas patobulintas būdas valdyti mažmeninės prekybos produktų kategorijas ir produktus sprendime „Dynamics 365 for Retail“.</span><span class="sxs-lookup"><span data-stu-id="d0798-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="d0798-105">Šie patobulinimai reklamavimo parduotuvėje vadovams leidžia peržiūrėti bendrąją produktų ypatybių struktūrą tarp mažmeninės prekybos produktų hierarchijos ir išsamios informacijos apie išleistus produktus.</span><span class="sxs-lookup"><span data-stu-id="d0798-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="d0798-106">Norėdami apie mažmeninės prekybos produktų kategorijų valdymą sužinoti daugiau, iš darbo srities **Kategorijų ir produktų valdymas** eikite į **mažmeninės prekybos produktų hierarchiją** ir atkreipkite dėmesį į patobulintą puslapio **Mažmeninės prekybos produktų kategorija** struktūrą.</span><span class="sxs-lookup"><span data-stu-id="d0798-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Darbo sritis Kategorijų ir produktų valdymas](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="d0798-108">Ankstesnėse versijose produktų ypatybės pagal jų taikomumą buvo suskirstytos į **pagrindines produktų ypatybes** ir **mažmeninės prekybos produktų ypatybes**.</span><span class="sxs-lookup"><span data-stu-id="d0798-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="d0798-109">**Mažmeninės prekybos produktų ypatybės** pagal taikomumą buvo *visuotinės*, o tai reiškia, kad tą pačią konkrečios **mažmeninės prekybos produktų ypatybės** reikšmę bendrai naudoj visi juridiniai subjektai.</span><span class="sxs-lookup"><span data-stu-id="d0798-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="d0798-110">**Pagrindinės produktų ypatybės** yra *taikomos konkrečiam juridiniam subjektui*.</span><span class="sxs-lookup"><span data-stu-id="d0798-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="d0798-111">Kitaip tariant, juridinių subjektų naudojama konkrečios **pagrindinės produktų ypatybės** reikšmė gali skirtis pagal atskirus verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="d0798-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="d0798-112">Patobulintoje mažmeninės prekybos produktų kategorijų struktūroje produktų ypatybės logiškai atskiriamos pagal jų taikomumą grupėje, kad būtų atspindėta išsamios išleisto produkto informacijos formos struktūra.</span><span class="sxs-lookup"><span data-stu-id="d0798-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Laukų grupavimas pagal jų taikomumą](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="d0798-114">Galite valdyti visų juridinių subjektų arba konkretaus juridinio subjekto ypatybes, taikomas konkrečiam juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="d0798-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="d0798-115">Norėdami tai atlikti, pasirinkite **Peržiūrėti / redaguoti visų juridinių subjektų** arba **Peržiūrėti / redaguoti konkretaus juridinio subjekto**.</span><span class="sxs-lookup"><span data-stu-id="d0798-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Atskiro ir visų juridinių subjektų rodinių perjungimas](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Atskiro ir visų juridinių subjektų rodinių perjungimas](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="d0798-118">Palyginti su ankstesnėmis versijomis, naujoje mažmeninės prekybos produktų kategorijų struktūroje reklamavimo parduotuvėje vadovas taip pat gali apibrėžti numatytąsias papildomo produktų ypatybių rinkinio reikšmes atskiros kategorijos lygiu.</span><span class="sxs-lookup"><span data-stu-id="d0798-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="d0798-119">Kuriant produktą, šias numatytąsias produkto ypatybių reikšmes produktas paveldi pagal savo susiejimą su atskira mažmeninės prekybos produktų hierarchijos kategorija.</span><span class="sxs-lookup"><span data-stu-id="d0798-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="d0798-120">Šias paveldėtas kiekvieno produkto ypatybes taip pat galima modifikuoti, kad būtų įvykdyti atskiri verslo reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="d0798-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="d0798-121">Mažmeninės prekybos produktų kategorijos formos produktų naujinimo ypatybių pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="d0798-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="d0798-122">Naudodami šią naują patobulintą produktų ypatybių struktūrą, galite pasirinkti, kurias atnaujintų produktų ypatybes reikia perkelti į susietus produktus.</span><span class="sxs-lookup"><span data-stu-id="d0798-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Naujas patobulintas atnaujintų produktų rodinys](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="d0798-124">Reklamavimo parduotuvėje vadovai gali modifikuoti šias paveldėtas kiekvieno produkto ypatybes, kad įvykdytų atskirus verslo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="d0798-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


