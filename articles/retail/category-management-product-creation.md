---
title: "Produktų kategorijų valdymas ir kūrimas"
description: "Šioje temoje aprašomi mažmeninės prekybos produktų kategorijų valdymo funkcijos patobulinimai. Šie patobulinimai reklamavimo parduotuvėje vadovams leidžia nustatyti ryšį tarp mažmeninės prekybos produktų hierarchijos ir išleistų produktų informacijos."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 2aa9f913b7faac393c4b403c6c36b99cc9acc80c
ms.contentlocale: lt-lt
ms.lasthandoff: 01/19/2018

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="ec8b2-104">Produktų kategorijų valdymas ir kūrimas</span><span class="sxs-lookup"><span data-stu-id="ec8b2-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="ec8b2-105">Mažmeninės prekybos produktų kategorijų valdymo funkcijos patobulinimai reklamavimo parduotuvėje vadovams leidžia nustatyti ryšį tarp mažmeninės prekybos produktų hierarchijos ir išleistų produktų informacijos.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="ec8b2-106">Norėdami šiuos patobulinimus peržiūrėti, darbo srityje **Kategorijų ir produktų valdymas** pasirinkite **Mažmeninės prekybos produktų hierarchija**, kad atidarytumėte puslapį **Nauja mažmeninės prekybos produktų kategorijos struktūra**.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="ec8b2-107">Ankstesniuose leidimuose produktų ypatybės pagal jų taikomumą buvo suskirstytos į pagrindines produktų ypatybes ir mažmeninės prekybos produktų ypatybes.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="ec8b2-108">Mažmeninės prekybos produktų ypatybės buvo *visuotinės*.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-108">Retail product properties were *global*.</span></span> <span data-ttu-id="ec8b2-109">Kitaip tariant, ta pati konkrečios produkto ypatybės reikšmė taikoma visiems juridiniams subjektams.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="ec8b2-110">Pagrindinės produktų ypatybės buvo taikomos *konkrečiam juridiniam subjektui*.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="ec8b2-111">Kitaip tariant, konkreti produkto ypatybė įvairiuose juridiniuose subjektuose gali skirtis pagal atskirus verslo poreikius.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="ec8b2-112">Taikydami šiuos patobulinimus, mažmeninės prekybos produktų kategorijos produktų ypatybių laukus ir toliau atskiriame pagal jų taikomumą grupėje, kad būtų atspindėta išleisto produkto informacijos formos struktūra.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="ec8b2-113">Galite valdyti visų juridinių subjektų arba konkretaus juridinio subjekto ypatybes, taikomas konkrečiam juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="ec8b2-114">Tiesiog pagal poreikį pasirinkite **Peržiūrėti / redaguoti visų juridinių subjektų** arba **Peržiūrėti / redaguoti konkretaus juridinio subjekto**.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="ec8b2-115">Reklamavimo parduotuvėje vadovai atskiros kategorijos lygiu taip pat gali apibrėžti numatytąsias papildomų produktų ypatybių reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="ec8b2-116">Šias ypatybių reikšmes produktas paveldi pagal jų sąsają su kategorija kuriant produktą.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="ec8b2-117">Mažmeninės prekybos produktų kategorijos formos produktų naujinimo ypatybių pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="ec8b2-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="ec8b2-118">Naudodami loginio grupavimo ypatybes galite pasirinkti, kurias atnaujintas produktų ypatybes reikia perkelti į susietus produktus.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="ec8b2-119">Reklamavimo parduotuvėje vadovai gali modifikuoti šias paveldėtas kiekvieno produkto ypatybes, kad įvykdytų atskirus verslo reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="ec8b2-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

