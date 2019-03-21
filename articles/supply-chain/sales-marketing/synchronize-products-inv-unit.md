---
title: „Finance and Operations“ produktų su atsargų vienetu sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus su atsargų vienetu sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2019
ms.locfileid: "836307"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="48c69-103">„Finance and Operations“ produktų su atsargų vienetais sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="48c69-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="48c69-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus su atsargų vienetu sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.</span><span class="sxs-lookup"><span data-stu-id="48c69-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="48c69-105">[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="48c69-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="48c69-106">Naudojamas šablonas **„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Field Service“)** yra paremtas šablonu **„Field Service“ produktai („Finance and Operations“ su „Field Service“)**.</span><span class="sxs-lookup"><span data-stu-id="48c69-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="48c69-107">Daugiau informacijos žr. [„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="48c69-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="48c69-108">Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų.</span><span class="sxs-lookup"><span data-stu-id="48c69-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="48c69-109">**„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Sales“)**</span><span class="sxs-lookup"><span data-stu-id="48c69-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="48c69-110">**„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)**</span><span class="sxs-lookup"><span data-stu-id="48c69-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="48c69-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="48c69-111">Templates and tasks</span></span>

<span data-ttu-id="48c69-112">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="48c69-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="48c69-113">„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Sales“)</span><span class="sxs-lookup"><span data-stu-id="48c69-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="48c69-114">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="48c69-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="48c69-115">Produktai</span><span class="sxs-lookup"><span data-stu-id="48c69-115">Products</span></span>

<span data-ttu-id="48c69-116">Šablonas **„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Field Service“)** apima vieną susiejimą, kuris neįtrauktas į šabloną **„Field Service“ produktai („Finance and Operations“ su „Field Service“)**.</span><span class="sxs-lookup"><span data-stu-id="48c69-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="48c69-117">Šis susiejimas užtikrina, kad būtų įtrauktas atsargų lygio sinchronizavimui reikalingas atsargų vienetas.</span><span class="sxs-lookup"><span data-stu-id="48c69-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="48c69-118">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="48c69-118">Template mapping in Data integration</span></span>

<span data-ttu-id="48c69-119">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="48c69-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="48c69-120">„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Field Service“): produktai</span><span class="sxs-lookup"><span data-stu-id="48c69-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="48c69-121">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="48c69-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
