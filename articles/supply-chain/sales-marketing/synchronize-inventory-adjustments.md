---
title: „Field Service“ atsargų perkėlimo ir koregavimo sinchronizavimas su Tiekimo grandinės valdymu
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų koregavimą ir perkėlimą su „Dynamics 365 Field Service“.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: fce407a66c339f2ece4bbc37b30243a2ed172d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251894"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>„Field Service“ atsargų perkėlimo ir koregavimo sinchronizavimas su Tiekimo grandinės valdymu

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Supply Chain Management“ atsargų koregavimą ir perkėlimą su „Dynamics 365 Field Service“.

[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Field Service“ atsargų koregavimą ir perkėlimą su Tiekimo grandinės valdymu.

**Šablonai naudojant funkcija Duomenų integravimas**
- Atsargų koregavimas (iš „Field Service“ į Tiekimo grandinės valdymą)
- Atsargų perkėlimas (iš „Field Service“ į Tiekimo grandinės valdymą)

**Užduotys duomenų integravimo projektuose**
- Atsargų koregavimas
- Atsargų perkėlimas

## <a name="table-set"></a>Lentelės rinkinys
| „Field service“                     | Tiekimo grandinės valdymas                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts | „Dataverse” atsargų koregavimo žurnalo antraštės ir eilutės |
| msdyn_inventoryadjustmentproducts | „Dataverse” atsargų perkėlimo žurnalo antraštės ir eilutės   |

## <a name="table-flow"></a>Lentelių srautas
„Field Service“ atliktas atsargų koregavimas ir perkėlimas sinchronizuojamas su Tiekimo grandinės valdymu, kai **Registruoti būseną** pasikeičia iš **Sukurta** į **Užregistruota**. Tokiu atveju koregavimo arba perkėlimo užsakymas užrakinamas ir tampa tik skaitomas. Tai reiškia, kad koregavimas ir perkėlimas gali būti registruojami Tiekimo grandinės valdyme, bet jų modifikuoti negalima. Tiekimo grandinės valdyme galite nustatyti paketinę užduotį automatiškai registruoti koregavimą ir perkelti atsargų žurnalus, sugeneruotus atliekant integravimą. Išsamesnės būtinos informacijos apie tai, kaip įgalinti paketinę užduotį, žr. toliau.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas 
Stulpelis **Atsargų vienetas** įtrauktas į lentelę **Produktas**. Šis stulpelis reikalingas, nes Pardavimo ir atsargų vienetas „Supply Chain Management” ne visada yra tas pats, o Atsargų vienetas reikalingas naudojant Sandėlio atsargas „Supply Chain Management”.
Nustatant į atsargų koregavimo produktą įtrauktą produktą, skirtą atsargų koregavimui ir atsargų perkėlimui, vieneto bus ieškoma pagal produktų atsargų produkto reikšmę. Jei vertė randama, stulpelis **Vienetas** bus užrakintas ties Atsargų koregavimo produktu.

Stulpelis **Paskelbti būseną** įtraukiamas į lentelę **Atsargų koregavimas** ir į lentelę **Atsargų perkėlimas**. Šis stulpelis naudojamas kaip filtras siunčiant koregavimą ar perkėlimą į „Supply Chain Management”. Numatytoji šio stulpelio vertė yra Sukurta (1), tačiau ji nėra siunčiama į „Supply Chain Management”. Kai atnaujinate reikšmę į Užregistruota (2), ji siunčiama į Tiekimo grandinės valdymą, tačiau po to nebegalėsite atlikti jokių koregavimo ar perkėlimo keitimų arba įtraukti naujų eilučių.

Stulpelis **Numeracija** įtrauktas į lentelę **Atsargų koregavimo produktas**. Šis stulpelis užtikrina, kad integravimui būtų priskirtas unikalus numeris ir integravimas galėtų kurti bei atnaujinti koregavimą. Kuriant pirmąjį atsargų koregavimo produktą, sukuriamas naujas įrašas lentelėje **P2C automatinė numeracija**, kad būtų palaikoma numerių serija ir naudojamas prefiksas.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

### <a name="supply-chain-management"></a>Tiekimo grandinės valdymas
Integravimo sugeneruotus integravimo atsargų žurnalus galima automatiškai registruoti naudojant paketinę užduotį. Tai įgalinama **Atsargų tvarkymas > Periodinės užduotys > „Dataverse” integravimas > Atsargų žurnalai po integracijos**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Atsargų koregavimas (iš „Field Service“ į Tiekimo grandinės valdymą): atsargų koregavimas

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Atsargų perkėlimas (iš „Field Service“ į Tiekimo grandinės valdymą): atsargų perkėlimas

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]