---
title: Tiekimo grandinės valdymo produktų su atsargų vienetais sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Supply Chain Management“ produktus su atsargų vienetu sinchronizuojant su „Dynamics 365 Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 8b65e9640106c5d351270074e39c121e70917228
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251229"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="1524a-103">Tiekimo grandinės valdymo produktų su atsargų vienetais sinchronizavimas su „Field Service“</span><span class="sxs-lookup"><span data-stu-id="1524a-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1524a-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Supply Chain Management“ produktus su atsargų vienetu sinchronizuojant su „Dynamics 365 Field Service“.</span><span class="sxs-lookup"><span data-stu-id="1524a-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="1524a-105">[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="1524a-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="1524a-106">Naudojamas šablonas **„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Field Service“)** yra paremtas šablonu **„Field Service“ produktai (iš Tiekimo grandinės valdymo į „Field Service“)**.</span><span class="sxs-lookup"><span data-stu-id="1524a-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="1524a-107">Daugiau informacijos žr. [„Field Service“ produktai (iš Tiekimo grandinės valdymo į „Field Service“)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="1524a-107">For more information, see [Field Service Products (Supply Chain Management to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="1524a-108">Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų.</span><span class="sxs-lookup"><span data-stu-id="1524a-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="1524a-109">**„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Sales“)**</span><span class="sxs-lookup"><span data-stu-id="1524a-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="1524a-110">**„Field Service“ produktai (iš Tiekimo grandinės valdymo į „Field Service“)**</span><span class="sxs-lookup"><span data-stu-id="1524a-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="1524a-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="1524a-111">Templates and tasks</span></span>

<span data-ttu-id="1524a-112">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="1524a-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="1524a-113">„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Sales“)</span><span class="sxs-lookup"><span data-stu-id="1524a-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="1524a-114">**Užduoties pavadinimas projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="1524a-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="1524a-115">Produktai</span><span class="sxs-lookup"><span data-stu-id="1524a-115">Products</span></span>

<span data-ttu-id="1524a-116">Šablone **„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Field Service“)** yra vienas susiejimas, kuris nėra įtrauktas į šabloną **„Field Service“ produktai (iš Tiekimo grandinės valdymo į „Field Service“)**.</span><span class="sxs-lookup"><span data-stu-id="1524a-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Managementto Field Service)** template.</span></span> <span data-ttu-id="1524a-117">Šis susiejimas užtikrina, kad būtų įtrauktas atsargų lygio sinchronizavimui reikalingas atsargų vienetas.</span><span class="sxs-lookup"><span data-stu-id="1524a-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="1524a-118">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="1524a-118">Template mapping in Data integration</span></span>

<span data-ttu-id="1524a-119">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="1524a-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="1524a-120">„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Field Service“): produktai</span><span class="sxs-lookup"><span data-stu-id="1524a-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="1524a-121">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="1524a-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
