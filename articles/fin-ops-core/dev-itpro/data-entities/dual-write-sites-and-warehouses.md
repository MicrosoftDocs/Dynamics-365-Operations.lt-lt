---
title: Integruotos svetainės ir sandėliai
description: Šioje temoje aprašoma svetainės ir sandėlio duomenų integracija tarp „Finance and Operations“ ir „Common Data Service“.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 4cf402e2811aaf92ddfa78eaf6d8887d88d93cbc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770998"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="e07dd-103">Integruotos svetainės ir sandėliai</span><span class="sxs-lookup"><span data-stu-id="e07dd-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e07dd-104">Šioje temoje aprašoma svetainės ir sandėlio duomenų integracija tarp „Finance and Operations“ ir „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="e07dd-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="e07dd-105">Operatyviosios svetainės ir sandėliai yra bendrosios koncepcijos programoje „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="e07dd-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="e07dd-106">Jie naudojami jūsų įmonės tiekimo grandinei modeliuoti.</span><span class="sxs-lookup"><span data-stu-id="e07dd-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="e07dd-107">Šablonai</span><span class="sxs-lookup"><span data-stu-id="e07dd-107">Templates</span></span>

<span data-ttu-id="e07dd-108">Kartu su „Common Data Service“ integracija, šios koncepcijos ir visa susijusi informacija yra pasiekiama programoje „Common Data Service“ naudojant svetainių ir sandėlių duomenų objektus toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="e07dd-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="e07dd-109">„Finance and Operations” programos</span><span class="sxs-lookup"><span data-stu-id="e07dd-109">Finance and Operations apps</span></span> | <span data-ttu-id="e07dd-110">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="e07dd-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="e07dd-111">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="e07dd-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="e07dd-112">Svetainės</span><span class="sxs-lookup"><span data-stu-id="e07dd-112">Sites</span></span> | <span data-ttu-id="e07dd-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="e07dd-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="e07dd-114">Sandėliai</span><span class="sxs-lookup"><span data-stu-id="e07dd-114">Warehouses</span></span> | <span data-ttu-id="e07dd-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="e07dd-115">msdyn_warehouses</span></span> | 

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [operational sites](dual-write/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](dual-write/InventWarehouseEntity-msdyn-warehouse.md)]

