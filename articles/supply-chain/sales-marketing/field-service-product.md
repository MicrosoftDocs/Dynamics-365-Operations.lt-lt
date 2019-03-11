---
title: Sinchronizuoti „Finance and Operations“ produktus su „Field Service“ produktais
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 3f26240ec289f5ddcc2682e598bbf93f516b99af
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "316331"
---
# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>„Finance and Operations“ produktų sinchronizavimas su „Field Service“ produktais

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.

Naudojamas šablonas **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** sukuriamas pagal potencialių klientų ir grynųjų pinigų šabloną **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**. Daugiau informacijos žr. [Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Šioje temoje aprašomas tik skirtumas tarp šablonų **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** ir **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**.

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**

- „Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)

**Užduoties pavadinimas projekte Duomenų integravimas:**

- Produktai – produktai

Šablone **„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“)** pateikiamas vienas susiejimas, kuris nėra įtrauktas į šabloną **Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis**. Šis susiejimas užtikrina, kad būtinas konkretus laukas **„Field Service“ produkto tipas** bus nustatytas teisingai.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Naudojamas toliau nurodytas vertės susiejimas.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Programoje „Finance and Operations“ vertė **„Field Service“ produkto tipas** duomenų objekte **Parduodami patvirtinti produktai** apskaičiuojamas taip, kaip nurodyta toliau.

- **Atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = True
- **Ne atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = False
- **„Service“:** produkto tipas = paslauga

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>„Field Service“ produktai (iš „Finance and Operations“ į „Field Service“): Produktai – produktai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct.png)](./media/FSProduct.png)
