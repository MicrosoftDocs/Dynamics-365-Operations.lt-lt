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

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Sinchronizuoti „Finance and Operations“ produktus su „Field Service“ produktais

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

