---
title: "Sinchronizuoti „Finance and Operations“ produktus su „Field Service“ produktais"
description: "Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: lt-lt
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="cf5a5-103">Sinchronizuoti „Finance and Operations“ produktus su „Field Service“ produktais</span><span class="sxs-lookup"><span data-stu-id="cf5a5-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cf5a5-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="cf5a5-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cf5a5-105">Naudojamas šablonas **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** sukuriamas pagal potencialių klientų ir grynųjų pinigų šabloną **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="cf5a5-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="cf5a5-106">Daugiau informacijos žr. [Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="cf5a5-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="cf5a5-107">Šioje temoje aprašomas tik skirtumas tarp šablonų **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** ir **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="cf5a5-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cf5a5-108">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="cf5a5-108">Templates and tasks</span></span>

<span data-ttu-id="cf5a5-109">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="cf5a5-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cf5a5-110">„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="cf5a5-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="cf5a5-111">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="cf5a5-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="cf5a5-112">Produktai – produktai</span><span class="sxs-lookup"><span data-stu-id="cf5a5-112">Products - Products</span></span>

<span data-ttu-id="cf5a5-113">Šablone **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** pateikiamas vienas susiejimas, kuris nėra įtrauktas į šabloną **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="cf5a5-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="cf5a5-114">Šis susiejimas užtikrina, kad būtinas konkretus laukas **„Field Service“ produkto tipas** bus nustatytas teisingai.</span><span class="sxs-lookup"><span data-stu-id="cf5a5-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="cf5a5-115">Naudojamas toliau nurodytas vertės susiejimas.</span><span class="sxs-lookup"><span data-stu-id="cf5a5-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="cf5a5-116">Programoje „Finance and Operations“ vertė **„Field Service“ produkto tipas** duomenų objekte **Parduodami patvirtinti produktai** apskaičiuojamas taip, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="cf5a5-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="cf5a5-117">**Atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = True</span><span class="sxs-lookup"><span data-stu-id="cf5a5-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="cf5a5-118">**Ne atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = False</span><span class="sxs-lookup"><span data-stu-id="cf5a5-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="cf5a5-119">**„Service“:** produkto tipas = paslauga</span><span class="sxs-lookup"><span data-stu-id="cf5a5-119">**Service:** Product type = Service</span></span>

