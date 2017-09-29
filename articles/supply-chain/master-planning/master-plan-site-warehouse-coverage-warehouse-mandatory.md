---
title: "Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas"
description: "Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos. Sandėlio dimensija privaloma."
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e753edacb0e2e019d701745308e7d9190ef09fe8
ms.contentlocale: lt-lt
ms.lasthandoff: 08/29/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="73061-104">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="73061-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="73061-105">Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos.</span><span class="sxs-lookup"><span data-stu-id="73061-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="73061-106">Sandėlio dimensija privaloma.</span><span class="sxs-lookup"><span data-stu-id="73061-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="73061-107">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="73061-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="73061-108">Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.</span><span class="sxs-lookup"><span data-stu-id="73061-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="73061-109">Sandėlio dimensija yra nustatoma kaip privaloma ir turi būti įvesta poreikio operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="73061-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="73061-110">Teritorijos ir sandėlio dimensijos nustatytos padengimui planuoti.</span><span class="sxs-lookup"><span data-stu-id="73061-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="73061-111">Kitos dimensijos taip pat gali būti nustatytos padengimui planuoti.</span><span class="sxs-lookup"><span data-stu-id="73061-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="73061-112">Tačiau jų neveikia kelių teritorijų funkcionalumas.</span><span class="sxs-lookup"><span data-stu-id="73061-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="73061-113">Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="73061-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="73061-114">Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:</span><span class="sxs-lookup"><span data-stu-id="73061-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="73061-115">Sandėlis nustatytas į **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="73061-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="73061-116">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="73061-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="73061-117">**Bendrojo planavimo** „FastTab‟ žr. lauką **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="73061-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="73061-118">Prekės padengimas yra apibrėžiamas prekei.</span><span class="sxs-lookup"><span data-stu-id="73061-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="73061-119">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="73061-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="73061-120">Pasirinkite prekę ir tada veiksmų srityje, skirtuke **Planas** spustelėkite **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="73061-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="73061-121">Papildymo ryšiai apibrėžiami sandėliui.</span><span class="sxs-lookup"><span data-stu-id="73061-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="73061-122">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="73061-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="73061-123">**Bendrojo planavimo** „FastTab‟ žr. laukų grupę **Pagrindinis sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="73061-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="73061-124">Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“.</span><span class="sxs-lookup"><span data-stu-id="73061-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="73061-125">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="73061-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="73061-126">Pasirinkite prekę ir tada veiksmų srityje, skirtuke **Planas** spustelėkite **Numatytosios užsakymo nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="73061-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="73061-127">Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="73061-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Poreikio teritorija ir sandėlio padengimas, sandėlis privalomas](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="73061-129">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="73061-129">See also</span></span>
--------

[<span data-ttu-id="73061-130">Bendrasis planavimas ir kelių teritorijų funkcija</span><span class="sxs-lookup"><span data-stu-id="73061-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="73061-131">Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="73061-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="73061-132">Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="73061-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="73061-133">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="73061-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="73061-134">Bendrasis planavimas – kaip nustatoma KS versija</span><span class="sxs-lookup"><span data-stu-id="73061-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



