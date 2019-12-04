---
title: Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas
description: Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos. Sandėlio dimensija nėra privaloma.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cea228e04632bd61f60771b09481241df5d16bd3
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813712"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="eea79-104">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="eea79-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eea79-105">Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos.</span><span class="sxs-lookup"><span data-stu-id="eea79-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="eea79-106">Sandėlio dimensija nėra privaloma.</span><span class="sxs-lookup"><span data-stu-id="eea79-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="eea79-107">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="eea79-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="eea79-108">Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.</span><span class="sxs-lookup"><span data-stu-id="eea79-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="eea79-109">Šios nuostatos modifikuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="eea79-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="eea79-110">Sandėlio dimensija nėra nustatyta kaip privaloma.</span><span class="sxs-lookup"><span data-stu-id="eea79-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="eea79-111">Sandėlis gali būti žinomas, bet nenaudojamas bendrojo planavimo skaičiavimo metu.</span><span class="sxs-lookup"><span data-stu-id="eea79-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="eea79-112">Teritorijos ir sandėlio dimensijos nustatytos padengimui planuoti.</span><span class="sxs-lookup"><span data-stu-id="eea79-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="eea79-113">Kitos dimensijos taip pat gali būti nustatytos padengimui planuoti.</span><span class="sxs-lookup"><span data-stu-id="eea79-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="eea79-114">Tačiau jų neveikia kelių teritorijų funkcionalumas.</span><span class="sxs-lookup"><span data-stu-id="eea79-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="eea79-115">Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="eea79-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="eea79-116">Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:</span><span class="sxs-lookup"><span data-stu-id="eea79-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="eea79-117">Sandėlis nustatytas į Rankinis.</span><span class="sxs-lookup"><span data-stu-id="eea79-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="eea79-118">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="eea79-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="eea79-119">**Bendrojo planavimo** „FastTab‟ žr. lauką **Rankinis**.</span><span class="sxs-lookup"><span data-stu-id="eea79-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="eea79-120">Prekės padengimas yra apibrėžiamas prekei.</span><span class="sxs-lookup"><span data-stu-id="eea79-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="eea79-121">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="eea79-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="eea79-122">Pasirinkite prekę ir tada veiksmų srityje, skirtuke **Planas** spustelėkite **Prekės padengimas**.</span><span class="sxs-lookup"><span data-stu-id="eea79-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="eea79-123">Papildymo ryšiai apibrėžiami sandėliui.</span><span class="sxs-lookup"><span data-stu-id="eea79-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="eea79-124">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="eea79-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="eea79-125">**Bendrojo planavimo** „FastTab‟ žr. laukų grupę **Pagrindinis sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="eea79-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="eea79-126">Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“.</span><span class="sxs-lookup"><span data-stu-id="eea79-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="eea79-127">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="eea79-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="eea79-128">Pasirinkite prekę ir tada veiksmų srityje, skirtuke **Planas** spustelėkite **Numatytosios užsakymo nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="eea79-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="eea79-129">Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="eea79-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Teritorijos ir sandėlio poreikis, sandėlis neprivalomas](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="eea79-131">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="eea79-131">Additional resources</span></span>
--------

[<span data-ttu-id="eea79-132">Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="eea79-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="eea79-133">Bendrasis vietos padengimo, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="eea79-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="eea79-134">Bendrasis vietos ir sandėlio padengimo planas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="eea79-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="eea79-135">Bendrasis vietos ir sandėlio padengimo planas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="eea79-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="eea79-136">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="eea79-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



