---
title: „Field Service“ atsargų perkėlimo ir koregavimo sinchronizavimas su „Finance and Operations“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: aa54945cea5821da163e1f6ea1747ac29b31a3ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "308373"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>„Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Field Service“.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Finance and Operations“.

**Šablonai naudojant funkcija Duomenų integravimas**
- Atsargų koregavimas („Field Service“ su „Finance and Operations“)
- Atsargų perkėlimas (iš „Field Service“ į „Finance and Operations“)

**Užduotys duomenų integravimo projektuose**
- Atsargų koregavimas
- Atsargų perkėlimas

## <a name="entity-set"></a>Objektų rinkinys
| Field Service                     | „Finance and Operations”                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS atsargų koregavimo žurnalo antraštės ir eilutės |
| msdyn_inventoryadjustmentproducts | CDS atsargų perkėlimo žurnalo antraštės ir eilutės   |

## <a name="entity-flow"></a>Objekto srautas
„Field Service“ atliktas atsargų koregavimas ir perkėlimas sinchronizuojamas su „Finance and Operations“, kai **Registruoti būseną** pasikeičia iš **Sukurta** į **Užregistruota**. Tokiu atveju koregavimo arba perkėlimo užsakymas užrakinamas ir tampa tik skaitomas. Tai reiškia, kad koregavimas ir perkėlimas gali būti registruojami „Finance and Operations“, bet jų modifikuoti negalima. „Finance and Operations“ galite nustatyti paketinę užduotį automatiškai registruoti koregavimą ir perkelti atsargų žurnalus, sugeneruotus atliekant integravimą. Išsamesnės būtinos informacijos apie tai, kaip įgalinti paketinę užduotį, žr. toliau.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas 
Laukas **Atsargų vienetas** įtrauktas į objektą **Produktas**. Šis laukas reikalingas, nes pardavimo ir atsargų vienetas „Finance and Operations“ ne visada yra tas pats, o atsargų vienetas reikalingas naudojant sandėlio atsargas programoje „Finance and Operations“.
Nustatant į atsargų koregavimo produktą įtrauktą produktą, skirtą atsargų koregavimui ir atsargų perkėlimui, vieneto bus ieškoma pagal produktų atsargų produkto reikšmę. Jei nustatoma vertė, atsargų koregavimo produkto laukas **Vienetas** užrakinamas.

Laukas **Registruoti būseną** įtraukiamas į objektą **Atsargų koregavimas** ir į objektą **Atsargų perkėlimas**. Šis laukas naudojamas kaip filtras siunčiant koregavimą ar perkėlimą į „Finance and Operations“. Numatytoji šio lauko reikšmė yra Sukurta (1), tačiau ji nėra siunčiama „Finance and Operations“. Kai atnaujinate reikšmę į Užregistruota (2), ji siunčiama „Finance and Operations“, tačiau po to nebegalėsite atlikti jokių koregavimo ar perkėlimo keitimų arba įtraukti naujų eilučių.

Laukas **Numeracija** įtrauktas į objektą **Atsargų koregavimo produktas**. Šis laukas užtikrina, kad integravimui būtų priskirtas unikalus numeris ir integravimas galėtų kurti bei atnaujinti koregavimą. Kuriant pirmąjį atsargų koregavimo produktą, sukuriamas naujas įrašas objekte **P2C automatinė numeracija**, kad būtų palaikoma numerių serija ir naudojamas prefiksas.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

### <a name="finance-and-operations"></a>„Finance and Operations”
Integravimo sugeneruotus integravimo atsargų žurnalus galima automatiškai registruoti naudojant paketinę užduotį. Tai įgalinama iš: **Atsargų valdymas > Periodinės užduotys > CDS integravimas > Registruoti integravimo atsargų žurnalus**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Atsargų koregavimas („Field Service“ su „Finance and Operations“): atsargų koregavimas

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Atsargų perkėlimas (iš „Field Service“ į „Finance and Operations“): atsargų perkėlimas

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSTrans1.png)](./media/FSTrans1.png)
