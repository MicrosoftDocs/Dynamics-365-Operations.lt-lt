---
title: Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Field Service“ produktais
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Supply Chain Management“ produktus sinchronizuojant su „Dynamics 365 Field Service“.
author: ChristianRytt
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 45a989604d829db715756b6cd206a5675a18acf2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909996"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Field Service“ produktais

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Supply Chain Management“ produktus sinchronizuojant su „Dynamics 365 Field Service“.

Naudojamas šablonas **„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)** sukuriamas pagal potencialių klientų ir grynųjų pinigų šabloną **Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis**. Daugiau informacijos žr. [Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Šioje temoje aprašomas tik skirtumas tarp šablonų **„Field Service“ produktai (iš Supply Chain Management“ į „Field Service“)** ir **Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis**.

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

**Šablono pavadinimas naudojant funkciją Duomenų integravimas**

- „Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)

**Užduoties pavadinimas projekte Duomenų integravimas**

- Produktai – produktai

Šablonas **„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)** apima vieną susiejimą, kuris nėra įtrauktas į šabloną **Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis**. Šis susiejimas užtikrina, kad būtinas konkretus laukas **„Field Service“ produkto tipas** bus nustatytas teisingai.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Naudojamas toliau nurodytas vertės susiejimas.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Programoje„Supply Chain Management“ vertė **„Field Service“ produkto tipas** duomenų objekte **Parduodami išleisti produktai** apskaičiuojama taip, kaip nurodyta toliau.

- **Atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = True
- **Ne atsargos:** produkto tipas = produkto ir prekės modelio grupė, laikomas produktas = False
- **„Service“:** produkto tipas = paslauga

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“): Produktai – Produktai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]