---
title: Integruotos svetainės ir sandėliai
description: Šioje temoje aprašoma svetainės ir sandėlio duomenų integracija tarp „Finance and Operations“ ir „Dataverse“.
author: t-benebo
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 533635ece005636dcee4e24d1d132111e1e2b370
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750671"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="c8ba9-103">Integruotos svetainės ir sandėliai</span><span class="sxs-lookup"><span data-stu-id="c8ba9-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="c8ba9-104">Šioje temoje aprašoma svetainės ir sandėlio duomenų integracija tarp „Finance and Operations“ ir „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="c8ba9-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="c8ba9-105">Operatyviosios svetainės ir sandėliai yra bendrosios koncepcijos programoje „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="c8ba9-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="c8ba9-106">Jie naudojami jūsų įmonės tiekimo grandinei modeliuoti.</span><span class="sxs-lookup"><span data-stu-id="c8ba9-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="c8ba9-107">Šablonai</span><span class="sxs-lookup"><span data-stu-id="c8ba9-107">Templates</span></span>

<span data-ttu-id="c8ba9-108">Kartu su „Dataverse“ integracija, šios koncepcijos ir visa susijusi informacija yra pasiekiama programoje „Dataverse“ naudojant svetainių ir sandėlių duomenų lenteles toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="c8ba9-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="c8ba9-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="c8ba9-109">Finance and Operations apps</span></span> | <span data-ttu-id="c8ba9-110">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="c8ba9-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="c8ba9-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="c8ba9-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="c8ba9-112">Svetainės</span><span class="sxs-lookup"><span data-stu-id="c8ba9-112">Sites</span></span> | <span data-ttu-id="c8ba9-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="c8ba9-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="c8ba9-114">Sandėliai</span><span class="sxs-lookup"><span data-stu-id="c8ba9-114">Warehouses</span></span> | <span data-ttu-id="c8ba9-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="c8ba9-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]