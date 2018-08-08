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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 3f26240ec289f5ddcc2682e598bbf93f516b99af
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="82e1e-103">Sinchronizuoti „Finance and Operations“ produktus su „Field Service“ produktais</span><span class="sxs-lookup"><span data-stu-id="82e1e-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82e1e-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="82e1e-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="82e1e-105">Naudojamas šablonas **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** sukuriamas pagal potencialių klientų ir grynųjų pinigų šabloną **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="82e1e-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="82e1e-106">Daugiau informacijos žr. [Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="82e1e-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="82e1e-107">Šioje temoje aprašomas tik skirtumas tarp šablonų **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** ir **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="82e1e-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="82e1e-108">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="82e1e-108">Templates and tasks</span></span>

<span data-ttu-id="82e1e-109">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="82e1e-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="82e1e-110">„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="82e1e-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="82e1e-111">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="82e1e-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="82e1e-112">Produktai – produktai</span><span class="sxs-lookup"><span data-stu-id="82e1e-112">Products - Products</span></span>

<span data-ttu-id="82e1e-113">Šablone **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** pateikiamas vienas susiejimas, kuris nėra įtrauktas į šabloną **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="82e1e-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="82e1e-114">Šis susiejimas užtikrina, kad būtinas konkretus laukas **„Field Service“ produkto tipas** bus nustatytas teisingai.</span><span class="sxs-lookup"><span data-stu-id="82e1e-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="82e1e-115">Naudojamas toliau nurodytas vertės susiejimas.</span><span class="sxs-lookup"><span data-stu-id="82e1e-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="82e1e-116">Programoje „Finance and Operations“ vertė **„Field Service“ produkto tipas** duomenų objekte **Parduodami patvirtinti produktai** apskaičiuojamas taip, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="82e1e-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="82e1e-117">**Atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = True</span><span class="sxs-lookup"><span data-stu-id="82e1e-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="82e1e-118">**Ne atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = False</span><span class="sxs-lookup"><span data-stu-id="82e1e-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="82e1e-119">**„Service“:** produkto tipas = paslauga</span><span class="sxs-lookup"><span data-stu-id="82e1e-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="82e1e-120">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="82e1e-120">Template mapping in Data integration</span></span>

<span data-ttu-id="82e1e-121">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="82e1e-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="82e1e-122">„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“): Produktai – produktai</span><span class="sxs-lookup"><span data-stu-id="82e1e-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="82e1e-123">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="82e1e-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>

