---
title: "Bendrasis planavimas – teritorijos padengimo poreikis, privalomas sandėlis"
description: "Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija yra padengimo dimensija. Sandėlis yra privaloma dimensija."
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14df626025a22237afe30cc5b08d42b475fc3a4f
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="d2aab-104">Bendrasis planavimas – teritorijos padengimo poreikis, privalomas sandėlis</span><span class="sxs-lookup"><span data-stu-id="d2aab-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2aab-105">Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija yra padengimo dimensija.</span><span class="sxs-lookup"><span data-stu-id="d2aab-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="d2aab-106">Sandėlis yra privaloma dimensija.</span><span class="sxs-lookup"><span data-stu-id="d2aab-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="d2aab-107">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="d2aab-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="d2aab-108">Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.</span><span class="sxs-lookup"><span data-stu-id="d2aab-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="d2aab-109">Šios nuostatos modifikuoti negalima.</span><span class="sxs-lookup"><span data-stu-id="d2aab-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="d2aab-110">Sandėlio dimensija yra nustatoma kaip privaloma ir turi būti įvesta poreikio operacijos metu.</span><span class="sxs-lookup"><span data-stu-id="d2aab-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="d2aab-111">Teritorijos dimensija yra nustatyta padengimo planavimui.</span><span class="sxs-lookup"><span data-stu-id="d2aab-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="d2aab-112">Kitos dimensijos taip pat gali būti nustatytos padengimo planavimui.</span><span class="sxs-lookup"><span data-stu-id="d2aab-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="d2aab-113">Tačiau jų neveikia kelių teritorijų funkcionalumas.</span><span class="sxs-lookup"><span data-stu-id="d2aab-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="d2aab-114">Sandėlio dimensija nėra nustatyta padengimo planavimui.</span><span class="sxs-lookup"><span data-stu-id="d2aab-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="d2aab-115">Todėl tiekimas ir poreikis sujungiami pagal teritoriją ir galbūt kitas suplanuotas padengimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d2aab-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="d2aab-116">Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="d2aab-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="d2aab-117">Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:</span><span class="sxs-lookup"><span data-stu-id="d2aab-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="d2aab-118">Prekės padengimas yra apibrėžiamas prekei.</span><span class="sxs-lookup"><span data-stu-id="d2aab-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="d2aab-119">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="d2aab-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d2aab-120">Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Prekių padengimas**.</span><span class="sxs-lookup"><span data-stu-id="d2aab-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="d2aab-121">Papildymo ryšiai apibrėžiami sandėliui.</span><span class="sxs-lookup"><span data-stu-id="d2aab-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="d2aab-122">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="d2aab-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d2aab-123">**Bendrojo planavimo** skirtuke žr. laukų grupę **Pagrindinis sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="d2aab-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="d2aab-124">Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“.</span><span class="sxs-lookup"><span data-stu-id="d2aab-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="d2aab-125">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="d2aab-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d2aab-126">Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Numatytosios užsakymo nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="d2aab-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="d2aab-127">Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="d2aab-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Teritorijos padengimo poreikis, sandėlis privalomas](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="d2aab-129">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="d2aab-129">See also</span></span>
--------

[<span data-ttu-id="d2aab-130">Bendrasis planavimas ir kelių teritorijų funkcija</span><span class="sxs-lookup"><span data-stu-id="d2aab-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="d2aab-131">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="d2aab-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d2aab-132">Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="d2aab-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d2aab-133">Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="d2aab-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d2aab-134">Bendrasis planavimas – kaip nustatoma KS versija</span><span class="sxs-lookup"><span data-stu-id="d2aab-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




