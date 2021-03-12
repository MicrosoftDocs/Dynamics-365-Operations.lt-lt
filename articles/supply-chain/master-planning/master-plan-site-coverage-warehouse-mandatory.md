---
title: Bendrasis planavimas – teritorijos padengimo poreikis, privalomas sandėlis
description: Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija yra padengimo dimensija. Sandėlis yra privaloma dimensija.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72240e7db8ec914220cb8f8f1185a91a304ff66b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977968"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="cbbee-104">Bendrasis planavimas – teritorijos padengimo poreikis, privalomas sandėlis</span><span class="sxs-lookup"><span data-stu-id="cbbee-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbbee-105">Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija yra padengimo dimensija.</span><span class="sxs-lookup"><span data-stu-id="cbbee-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="cbbee-106">Sandėlis yra privaloma dimensija.</span><span class="sxs-lookup"><span data-stu-id="cbbee-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="cbbee-107">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="cbbee-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="cbbee-108">Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.</span><span class="sxs-lookup"><span data-stu-id="cbbee-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="cbbee-109">Šios nuostatos modifikuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="cbbee-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="cbbee-110">Sandėlio dimensija yra nustatoma kaip privaloma ir turi būti įvesta poreikio operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="cbbee-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="cbbee-111">Teritorijos dimensija yra nustatyta padengimo planavimui.</span><span class="sxs-lookup"><span data-stu-id="cbbee-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="cbbee-112">Kitos dimensijos taip pat gali būti nustatytos padengimo planavimui.</span><span class="sxs-lookup"><span data-stu-id="cbbee-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="cbbee-113">Tačiau jų neveikia kelių teritorijų funkcionalumas.</span><span class="sxs-lookup"><span data-stu-id="cbbee-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="cbbee-114">Sandėlio dimensija nėra nustatyta padengimo planavimui.</span><span class="sxs-lookup"><span data-stu-id="cbbee-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="cbbee-115">Todėl tiekimas ir poreikis sujungiami pagal teritoriją ir galbūt kitas suplanuotas padengimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="cbbee-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="cbbee-116">Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="cbbee-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="cbbee-117">Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:</span><span class="sxs-lookup"><span data-stu-id="cbbee-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="cbbee-118">Prekės padengimas yra apibrėžiamas prekei.</span><span class="sxs-lookup"><span data-stu-id="cbbee-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="cbbee-119">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="cbbee-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="cbbee-120">Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Prekių padengimas**.</span><span class="sxs-lookup"><span data-stu-id="cbbee-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="cbbee-121">Papildymo ryšiai apibrėžiami sandėliui.</span><span class="sxs-lookup"><span data-stu-id="cbbee-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="cbbee-122">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="cbbee-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="cbbee-123">**Bendrojo planavimo** skirtuke žr. laukų grupę **Pagrindinis sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="cbbee-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="cbbee-124">Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“.</span><span class="sxs-lookup"><span data-stu-id="cbbee-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="cbbee-125">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="cbbee-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="cbbee-126">Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Numatytosios užsakymo nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="cbbee-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="cbbee-127">Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="cbbee-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Teritorijos padengimo poreikis, sandėlis privalomas](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="cbbee-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="cbbee-129">Additional resources</span></span>
--------

[<span data-ttu-id="cbbee-130">Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="cbbee-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="cbbee-131">Bendrasis vietos ir sandėlio padengimo planas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="cbbee-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="cbbee-132">Bendrasis vietos padengimo, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="cbbee-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="cbbee-133">Bendrasis vietos ir sandėlio padengimo planas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="cbbee-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="cbbee-134">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="cbbee-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



