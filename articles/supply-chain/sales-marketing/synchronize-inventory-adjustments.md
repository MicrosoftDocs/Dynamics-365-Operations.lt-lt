---
title: "„Field Service“ atsargų perkėlimo ir koregavimo sinchronizavimas su „Finance and Operations“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Field Service“."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>„Field Service“ atsargų koregavimo sinchronizavimas su „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Field Service“.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ atsargų koregavimą ir perkėlimą su „Microsoft Dynamics 365 for Finance and Operations“.

**Šablonų pavadinimas naudojant funkciją Duomenų integravimas:**
- Atsargų koregavimas („Field Service“ su „Finance and Operations“)
- Atsargų perkėlimas (iš „Field Service“ į „Finance and Operations“)

**Užduočių pavadinimai projektuose Duomenų integravimas:**
- Atsargų koregavimas
- Atsargų perkėlimas

## <a name="entity-set"></a>Objektų rinkinys
| Field Service                     | „Finance and Operations”                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   CDS atsargų koregavimo žurnalo antraštės ir eilutės |
| msdyn_inventoryadjustmentproducts | CDS atsargų perkėlimo žurnalo antraštės ir eilutės   |

## <a name="entity-flow"></a>Objekto srautas
„Field Service“ atliktas atsargų koregavimas ir perkėlimas sinchronizuojamas su „Finance and Operations“, kai **Registruoti būseną** pasikeičia iš Sukurta į Užregistruota. Tokiu atveju koregavimo arba perkėlimo užsakymas užrakinamas ir tampa tik skaitomas, nes koregavimas ir perkėlimas gali būti registruojami „Finance and Operations“, todėl jų modifikuoti negalima.
„Finance and Operations“ galite nustatyti paketinę užduotį automatiškai registruoti koregavimą ir perkelti sugeneruotus atsargų žurnalus atliekant integravimą. Išsamesnės būtinos informacijos apie tai, kaip įgalinti paketinę užduotį, žr. toliau.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas 
Atsargų vieneto laukas įtrauktas į produkto objektą. Šis laukas reikalingas, nes pardavimo ir atsargų vienetas „Operations“ ne visada yra tas pats, o dėl sandėlio atsargų operacijų mums reikia atsargų vieneto.
Nustatant į atsargų koregavimo produktą įtrauktą produktą, skirtą atsargų koregavimui ir atsargų perkėlimui, vieneto bus ieškoma pagal produktų atsargų produkto vertę. Jei nustatoma vertė, atsargų koregavimo produkto vieneto laukas užrakinamas

Laukas Registruoti būseną įtraukiamas į atsargų koregavimo objektą ir į atsargų perkėlimo objektą. Šis laukas naudojamas kaip filtras siunčiant koregavimą ar perkėlimą į „Operations“. Numatytasis laukas nustatomas į Sukurta (1) – tokiu atveju į „Operations“ nesiunčiama. Kai keičiate į Užregistruota (2), siunčiama operacijoms, tačiau tada nebegalėsite atlikti jokių koregavimo ar perkėlimo keitimų arba į juos įtraukti naujų eilučių.
Numeracijos laukas įtrauktas į atsargų koregavimo produkto objektą. Šis laukas padeda integravimui turėti unikalų numerį, todėl žinoma, kada kurti ir kada naujinti. Kuriant pirmąjį atsargų koregavimo produktą, sukuriamas naujas įrašas P2C automatinės numeracijos objekte, kad būtų palaikoma numerių serija ir naudojamas prefiksas.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

### <a name="in-finance-and-operations"></a>Programoje „Finance and Operations”
Integravimo sugeneruotus integravimo atsargų žurnalus galima automatiškai registruoti naudojant paketinę užduotį. Tai įgalinama iš: Atsargų valdymas > Periodinės užduotys > CDS integravimas > Registruoti integravimo atsargų žurnalus

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Atsargų koregavimas („Field Service“ su „Finance and Operations“): atsargų koregavimas

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Atsargų perkėlimas (iš „Field Service“ į „Finance and Operations“): atsargų perkėlimas

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSTrans1.png)](./media/FSTrans1.png)

