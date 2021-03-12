---
title: Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Field Service“ produktais
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Supply Chain Management“ produktus sinchronizuojant su „Dynamics 365 Field Service“.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: ffa0616d51127a024bea526c5926a182c0449971
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996738"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="775b6-103">Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Field Service“ produktais</span><span class="sxs-lookup"><span data-stu-id="775b6-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="775b6-104">Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Supply Chain Management“ produktus sinchronizuojant su „Dynamics 365 Field Service“.</span><span class="sxs-lookup"><span data-stu-id="775b6-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="775b6-105">Naudojamas šablonas **„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)** sukuriamas pagal potencialių klientų ir grynųjų pinigų šabloną **Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="775b6-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="775b6-106">Daugiau informacijos žr. [Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="775b6-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="775b6-107">Šioje temoje aprašomas tik skirtumas tarp šablonų **„Field Service“ produktai (iš Supply Chain Management“ į „Field Service“)** ir **Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="775b6-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="775b6-108">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="775b6-108">Templates and tasks</span></span>

<span data-ttu-id="775b6-109">**Šablono pavadinimas naudojant funkciją Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="775b6-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="775b6-110">„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)</span><span class="sxs-lookup"><span data-stu-id="775b6-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="775b6-111">**Užduoties pavadinimas projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="775b6-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="775b6-112">Produktai – produktai</span><span class="sxs-lookup"><span data-stu-id="775b6-112">Products - Products</span></span>

<span data-ttu-id="775b6-113">Šablonas **„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)** apima vieną susiejimą, kuris nėra įtrauktas į šabloną **Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis**.</span><span class="sxs-lookup"><span data-stu-id="775b6-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="775b6-114">Šis susiejimas užtikrina, kad būtinas konkretus laukas **„Field Service“ produkto tipas** bus nustatytas teisingai.</span><span class="sxs-lookup"><span data-stu-id="775b6-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="775b6-115">Naudojamas toliau nurodytas vertės susiejimas.</span><span class="sxs-lookup"><span data-stu-id="775b6-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="775b6-116">Programoje„Supply Chain Management“ vertė **„Field Service“ produkto tipas** duomenų objekte **Parduodami išleisti produktai** apskaičiuojama taip, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="775b6-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="775b6-117">**Atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = True</span><span class="sxs-lookup"><span data-stu-id="775b6-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="775b6-118">**Ne atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = False</span><span class="sxs-lookup"><span data-stu-id="775b6-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="775b6-119">**„Service“:** produkto tipas = paslauga</span><span class="sxs-lookup"><span data-stu-id="775b6-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="775b6-120">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="775b6-120">Template mapping in Data integration</span></span>

<span data-ttu-id="775b6-121">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="775b6-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="775b6-122">„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“): Produktai – Produktai</span><span class="sxs-lookup"><span data-stu-id="775b6-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="775b6-123">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="775b6-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
