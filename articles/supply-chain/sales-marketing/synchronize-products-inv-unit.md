---
title: "„Finance and Operations“ produktų su atsargų vienetu sinchronizavimas su „Field Service“"
description: "Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus su atsargų vienetu sinchronizuojant su „Microsoft Dynamics 365 for Field Service“."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="37cce-103">„Finance and Operations“ produktų su atsargų vienetu sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="37cce-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="37cce-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus su atsargų vienetu sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="37cce-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="37cce-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="37cce-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="37cce-106">Naudojamas šablonas **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** sukuriamas pagal potencialių klientų ir grynųjų pinigų šabloną **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="37cce-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="37cce-107">Daugiau informacijos žr. [Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="37cce-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="37cce-108">Šioje temoje aprašomi tik skirtumai tarp šablonų **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** ir **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)**.</span><span class="sxs-lookup"><span data-stu-id="37cce-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="37cce-109">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="37cce-109">Templates and tasks</span></span>

<span data-ttu-id="37cce-110">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="37cce-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="37cce-111">„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Sales“)</span><span class="sxs-lookup"><span data-stu-id="37cce-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="37cce-112">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="37cce-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="37cce-113">Produktai</span><span class="sxs-lookup"><span data-stu-id="37cce-113">Products</span></span>

<span data-ttu-id="37cce-114">Šablonas **„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Field Service“)** apima vieną susiejimą, kuris neįtrauktas į šabloną **„Field Service“ produktai („Finance and Operations“ su „Field Service“)**.</span><span class="sxs-lookup"><span data-stu-id="37cce-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="37cce-115">Šis susiejimas užtikrina, kad būtų įtrauktas atsargų lygio sinchronizavimui reikalingas atsargų vienetas.</span><span class="sxs-lookup"><span data-stu-id="37cce-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="37cce-116">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="37cce-116">Template mapping in Data integration</span></span>

<span data-ttu-id="37cce-117">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="37cce-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="37cce-118">„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Field Service“): produktai</span><span class="sxs-lookup"><span data-stu-id="37cce-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="37cce-119">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="37cce-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>

