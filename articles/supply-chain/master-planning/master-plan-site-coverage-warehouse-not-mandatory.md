---
title: Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas
description: Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorijos dimensija nustatyta padengimui.
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
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f4cde5c570148ca58c4ea583a8f538a72d4957d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987051"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="d4e6d-103">Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="d4e6d-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4e6d-104">Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorijos dimensija nustatyta padengimui.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="d4e6d-105">Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="d4e6d-106">Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="d4e6d-107">Sandėlio dimensija nėra nustatyta kaip privaloma.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="d4e6d-108">Sandėlis gali būti žinomas, bet nenaudojamas bendrojo planavimo skaičiavimo metu.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="d4e6d-109">Teritorijos dimensija yra nustatyta padengimo planavimui.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="d4e6d-110">Sandėlio dimensija nėra nustatyta padengimo planavimui.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="d4e6d-111">Todėl tiekimas ir poreikis sujungiami pagal teritoriją ir galbūt kitas suplanuotas padengimo dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="d4e6d-112">Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="d4e6d-113">Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:</span><span class="sxs-lookup"><span data-stu-id="d4e6d-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="d4e6d-114">Prekės padengimas yra apibrėžiamas prekei.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="d4e6d-115">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d4e6d-116">Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Prekių padengimas**.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="d4e6d-117">Papildymo ryšiai apibrėžiami sandėliui.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="d4e6d-118">Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="d4e6d-119">**Bendrojo planavimo** skirtuke žr. laukų grupę **Pagrindinis sandėlis**.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="d4e6d-120">Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="d4e6d-121">Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="d4e6d-122">Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Numatytosios užsakymo nuostatos**.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="d4e6d-123">Formoje **Numatytieji užsakymo parametrai** rasite lauką **Numatytasis užsakymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="d4e6d-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Teritorijos padengimo poreikis, sandėlis neprivalomas](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="d4e6d-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d4e6d-125">Additional resources</span></span>
--------

[<span data-ttu-id="d4e6d-126">Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga</span><span class="sxs-lookup"><span data-stu-id="d4e6d-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="d4e6d-127">Bendrasis vietos ir sandėlio padengimo planas, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="d4e6d-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d4e6d-128">Bendrasis vietos padengimo, sandėlis privalomas</span><span class="sxs-lookup"><span data-stu-id="d4e6d-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="d4e6d-129">Bendrasis vietos padengimo planavimas, sandėlis neprivalomas</span><span class="sxs-lookup"><span data-stu-id="d4e6d-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="d4e6d-130">KS versijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="d4e6d-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



