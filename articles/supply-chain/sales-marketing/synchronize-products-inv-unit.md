---
title: Tiekimo grandinės valdymo produktų su atsargų vienetais sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Supply Chain Management“ produktus su atsargų vienetu sinchronizuojant su „Dynamics 365 Field Service“.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 911c5cc79ae359bbb77d31f366ccfeabf282a33e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433737"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Tiekimo grandinės valdymo produktų su atsargų vienetais sinchronizavimas su „Field Service“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Supply Chain Management“ produktus su atsargų vienetu sinchronizuojant su „Dynamics 365 Field Service“.

[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Naudojamas šablonas **„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Field Service“)** yra paremtas šablonu **„Field Service“ produktai (iš Tiekimo grandinės valdymo į „Field Service“)**. Daugiau informacijos žr. [Produktų „Supply Chain Management“ sinchronizavimas į produktus „Field Service“](field-service-product.md).

Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų. 
- **„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Sales“)**
- **„Field Service“ produktai (iš Tiekimo grandinės valdymo į „Field Service“)** 

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**

- „Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Sales“)

**Užduoties pavadinimas projekte Duomenų integravimas:**

- Produktai

Šablone **„Field Service“ produktai su atsargų vienetu (iš „Supply Chain Management“ į „Field Service“)** yra vienas susiejimas, kuris nėra įtrauktas į šabloną **„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)**. Šis susiejimas užtikrina, kad būtų įtrauktas atsargų lygio sinchronizavimui reikalingas atsargų vienetas.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>„Field Service“ produktai su atsargų vienetu (iš Tiekimo grandinės valdymo į „Field Service“): produktai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]