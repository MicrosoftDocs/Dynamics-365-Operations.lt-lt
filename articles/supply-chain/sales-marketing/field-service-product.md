---
title: Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Field Service“ produktais
description: Šiame straipsnyje aptariamos šablonus ir su juos susijusių užduočių, kurios naudojamos produktams sinchronizuoti iš "iki Dynamics 365 Supply Chain Management "Dynamics 365 Field Service.
author: Henrikan
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 114550f01f3aed197480fb6830fe913dbfa7b570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860557"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Field Service“ produktais

[!include[banner](../includes/banner.md)]

Šiame straipsnyje aptariamos šablonai ir su juos susijusių užduočių, naudojamų produktams sinchronizuoti Dynamics 365 Supply Chain Management iš "Dynamics 365 Field Service".

Naudojamas šablonas **„Field Service“ produktai (iš „Supply Chain Management“ į „Field Service“)** sukuriamas pagal potencialių klientų ir grynųjų pinigų šabloną **Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis**. Daugiau informacijos žr. [Produktai (iš „Supply Chain Management“ į „Sales“) – tiesioginis](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Šiame straipsnyje aprašomi tik " **Field Service" produktų (tiekimo grandinės valdymo į "Field Service") ir produktų (tiekimo grandinės valdymas iki pardavimo)** **skirtumai – tiesioginiai** šablonai.

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

[![Šablono susiejimas naudojant funkcija Duomenų integravimas.](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]