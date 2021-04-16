---
title: Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas
description: Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos. Sandėlio dimensija privaloma.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce4960ed6406587557ce12b72b30fa9a620d6b18
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833502"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="c1c49-104">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="c1c49-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1c49-105">Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos.</span><span class="sxs-lookup"><span data-stu-id="c1c49-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="c1c49-106">Sandėlio dimensija privaloma.</span><span class="sxs-lookup"><span data-stu-id="c1c49-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="c1c49-107">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="c1c49-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="c1c49-108">Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.</span><span class="sxs-lookup"><span data-stu-id="c1c49-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="c1c49-109">Sandėlio dimensija yra nustatoma kaip privaloma ir turi būti įvesta poreikio operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="c1c49-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="c1c49-110">Teritorijos ir sandėlio dimensijos nustatytos padengimui planuoti.</span><span class="sxs-lookup"><span data-stu-id="c1c49-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="c1c49-111">Kitos dimensijos taip pat gali būti nustatytos padengimui planuoti.</span><span class="sxs-lookup"><span data-stu-id="c1c49-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="c1c49-112">Tačiau jų neveikia kelių teritorijų funkcionalumas.</span><span class="sxs-lookup"><span data-stu-id="c1c49-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="c1c49-113">Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="c1c49-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="c1c49-114">Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:</span><span class="sxs-lookup"><span data-stu-id="c1c49-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="c1c49-115">Sandėlis nustatytas į **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="c1c49-116">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="c1c49-117">**Bendrojo planavimo** „FastTab‟ žr. lauką **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="c1c49-118">Prekės padengimas yra apibrėžiamas prekei.</span><span class="sxs-lookup"><span data-stu-id="c1c49-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="c1c49-119">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c1c49-120">Pasirinkite prekę ir tada veiksmų srityje, skirtuke **Planas** spustelėkite **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="c1c49-121">Papildymo ryšiai apibrėžiami sandėliui.</span><span class="sxs-lookup"><span data-stu-id="c1c49-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="c1c49-122">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="c1c49-123">**Bendrojo planavimo** „FastTab‟ žr. laukų grupę **Pagrindinis sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="c1c49-124">Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“.</span><span class="sxs-lookup"><span data-stu-id="c1c49-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="c1c49-125">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="c1c49-126">Pasirinkite prekę ir tada veiksmų srityje, skirtuke **Planas** spustelėkite **Numatytosios užsakymo nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="c1c49-127">Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="c1c49-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Poreikio teritorija ir sandėlio padengimas, sandėlis privalomas](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="c1c49-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="c1c49-129">Additional resources</span></span>
--------

[<span data-ttu-id="c1c49-130">Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="c1c49-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="c1c49-131">Bendrasis vietos padengimo, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="c1c49-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c1c49-132">Bendrasis vietos padengimo planavimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="c1c49-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c1c49-133">Bendrasis vietos ir sandėlio padengimo planas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="c1c49-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c1c49-134">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="c1c49-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]