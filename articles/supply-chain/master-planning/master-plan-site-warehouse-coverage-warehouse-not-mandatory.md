---
title: "Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas"
description: "Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos. Sandėlio dimensija nėra privaloma."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9c7b13a7a018ce584c877fed6212abc3c2913903
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="b6902-104">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="b6902-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b6902-105">Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos.</span><span class="sxs-lookup"><span data-stu-id="b6902-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="b6902-106">Sandėlio dimensija nėra privaloma.</span><span class="sxs-lookup"><span data-stu-id="b6902-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="b6902-107">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="b6902-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b6902-108">Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.</span><span class="sxs-lookup"><span data-stu-id="b6902-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="b6902-109">Šios nuostatos modifikuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="b6902-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="b6902-110">Sandėlio dimensija nėra nustatyta kaip privaloma.</span><span class="sxs-lookup"><span data-stu-id="b6902-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="b6902-111">Sandėlis gali būti žinomas, bet nenaudojamas bendrojo planavimo skaičiavimo metu.</span><span class="sxs-lookup"><span data-stu-id="b6902-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="b6902-112">Teritorijos ir sandėlio dimensijos nustatytos padengimui planuoti.</span><span class="sxs-lookup"><span data-stu-id="b6902-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="b6902-113">Kitos dimensijos taip pat gali būti nustatytos padengimui planuoti.</span><span class="sxs-lookup"><span data-stu-id="b6902-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="b6902-114">Tačiau jų neveikia kelių teritorijų funkcionalumas.</span><span class="sxs-lookup"><span data-stu-id="b6902-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="b6902-115">Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="b6902-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="b6902-116">Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:</span><span class="sxs-lookup"><span data-stu-id="b6902-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="b6902-117">Sandėlis nustatytas į Rankinis.</span><span class="sxs-lookup"><span data-stu-id="b6902-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="b6902-118">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="b6902-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b6902-119">**Bendrojo planavimo** „FastTab‟ žr. lauką **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="b6902-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="b6902-120">Prekės padengimas yra apibrėžiamas prekei.</span><span class="sxs-lookup"><span data-stu-id="b6902-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="b6902-121">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="b6902-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b6902-122">Pasirinkite prekę ir tada veiksmų srityje, skirtuke **Planas** spustelėkite **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="b6902-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="b6902-123">Papildymo ryšiai apibrėžiami sandėliui.</span><span class="sxs-lookup"><span data-stu-id="b6902-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="b6902-124">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="b6902-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b6902-125">**Bendrojo planavimo** „FastTab‟ žr. laukų grupę **Pagrindinis sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="b6902-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="b6902-126">Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“.</span><span class="sxs-lookup"><span data-stu-id="b6902-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="b6902-127">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="b6902-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b6902-128">Pasirinkite prekę ir tada veiksmų srityje, skirtuke **Planas** spustelėkite **Numatytosios užsakymo nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="b6902-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="b6902-129">Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="b6902-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Teritorijos ir sandėlio poreikis, sandėlis neprivalomas](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a><span data-ttu-id="b6902-131">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="b6902-131">See also</span></span>
--------

[<span data-ttu-id="b6902-132">Bendrasis planavimas ir kelių teritorijų funkcija</span><span class="sxs-lookup"><span data-stu-id="b6902-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="b6902-133">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="b6902-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b6902-134">Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="b6902-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b6902-135">Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="b6902-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b6902-136">Bendrasis planavimas – kaip nustatoma KS versija</span><span class="sxs-lookup"><span data-stu-id="b6902-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



