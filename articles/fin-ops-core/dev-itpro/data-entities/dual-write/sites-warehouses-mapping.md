---
title: Integruotos svetainės ir sandėliai
description: Šioje temoje aprašoma svetainės ir sandėlio duomenų integracija tarp „Finance and Operations“ ir „Dataverse“.
author: t-benebo
manager: AnnBe
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
ms.openlocfilehash: b93e5f15e281c20f8688d496fc78f8b46b8aa996
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560366"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="a3899-103">Integruotos svetainės ir sandėliai</span><span class="sxs-lookup"><span data-stu-id="a3899-103">Integrated sites and warehouses</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="a3899-104">Šioje temoje aprašoma svetainės ir sandėlio duomenų integracija tarp „Finance and Operations“ ir „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="a3899-104">This topic describes the integration of site and warehouse data between Finance and Operations and Dataverse.</span></span> <span data-ttu-id="a3899-105">Operatyviosios svetainės ir sandėliai yra bendrosios koncepcijos programoje „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="a3899-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="a3899-106">Jie naudojami jūsų įmonės tiekimo grandinei modeliuoti.</span><span class="sxs-lookup"><span data-stu-id="a3899-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="a3899-107">Šablonai</span><span class="sxs-lookup"><span data-stu-id="a3899-107">Templates</span></span>

<span data-ttu-id="a3899-108">Kartu su „Dataverse“ integracija, šios koncepcijos ir visa susijusi informacija yra pasiekiama programoje „Dataverse“ naudojant svetainių ir sandėlių duomenų lenteles toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="a3899-108">With the integration with Dataverse, these concepts and all their related information are available in Dataverse using the sites and warehouses data tables in the following table.</span></span>

<span data-ttu-id="a3899-109">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="a3899-109">Finance and Operations apps</span></span> | <span data-ttu-id="a3899-110">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="a3899-110">Other Dynamics 365 apps</span></span> | <span data-ttu-id="a3899-111">aprašymas</span><span class="sxs-lookup"><span data-stu-id="a3899-111">Description</span></span>
--------------------------|---------------------------|---
<span data-ttu-id="a3899-112">Svetainės</span><span class="sxs-lookup"><span data-stu-id="a3899-112">Sites</span></span> | <span data-ttu-id="a3899-113">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="a3899-113">msdyn_operationalsites</span></span> | 
<span data-ttu-id="a3899-114">Sandėliai</span><span class="sxs-lookup"><span data-stu-id="a3899-114">Warehouses</span></span> | <span data-ttu-id="a3899-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="a3899-115">msdyn_warehouses</span></span> | 

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [operational sites](includes/InventOperationalSiteEntity-msdyn-operationalsite.md)]

[!include [warehouses](includes/InventWarehouseEntity-msdyn-warehouse.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]