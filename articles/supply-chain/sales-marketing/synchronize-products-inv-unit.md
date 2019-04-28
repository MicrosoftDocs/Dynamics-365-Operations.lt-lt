---
title: „Finance and Operations“ produktų su atsargų vienetu sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus su atsargų vienetu sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/14/2019
ms.locfileid: "842467"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>„Finance and Operations“ produktų su atsargų vienetais sinchronizavimas su „Field Service“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus su atsargų vienetu sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Naudojamas šablonas **„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Field Service“)** yra paremtas šablonu **„Field Service“ produktai („Finance and Operations“ su „Field Service“)**. Daugiau informacijos žr. [„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)](field-service-product.md).

Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų. 
- **„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Sales“)**
- **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** 

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**

- „Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Sales“)

**Užduoties pavadinimas projekte Duomenų integravimas:**

- Produktai

Šablonas **„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Field Service“)** apima vieną susiejimą, kuris neįtrauktas į šabloną **„Field Service“ produktai („Finance and Operations“ su „Field Service“)**. Šis susiejimas užtikrina, kad būtų įtrauktas atsargų lygio sinchronizavimui reikalingas atsargų vienetas.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>„Field Service“ produktai su atsargų vienetu („Finance and Operations“ su „Field Service“): produktai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct1.png)](./media/FSProduct1.png)
