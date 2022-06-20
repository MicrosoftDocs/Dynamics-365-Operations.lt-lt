---
title: Tiekimo grandinės valdymo projektų sąrašo sinchronizavimas su „Field Service“
description: Šiame straipsnyje aptariamos šablonai ir su juos susijusias užduotis, kurios naudojamos projektams sinchronizuoti Dynamics 365 Supply Chain Management Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 71c0580953f01c2d29e99fa2928a0b4a3937d5c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899359"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Tiekimo grandinės valdymo projektų sąrašo sinchronizavimas su „Field Service“

[!include[banner](../includes/banner.md)]

Šiame straipsnyje aptariamos šablonai ir su juos susijusias užduotis, kurios naudojamos projektams sinchronizuoti Dynamics 365 Supply Chain Management Dynamics 365 Field Service.

[![„Supply Chain Management“ ir „Field Service“ verslo procesų sinchronizavimas.](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant Tiekimo grandinės valdymo projektus su „Field Service“.

**Šablonas naudojant funkcija Duomenų integravimas**
- Projektai (iš Tiekimo grandinės valdymo į „Field Service“)

**Užduotis projekte Duomenų integravimas**
- Projektai

Prieš sinchronizuojant projektų sąrašą būtina atlikti toliau nurodytas sinchronizavimo užduotis.
- Sąskaitos (iš „Sales“ į Tiekimo grandinės valdymą) 

## <a name="entity-set"></a>Objektų rinkinys
| „Field Service“           | Tiekimo grandinės valdymas  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projektai                |

## <a name="entity-flow"></a>Objekto srautas
Projektai sukuriami Tiekimo grandinės valdyme. Projektai, kurių **Projekto tipas** – **Laikas ir medžiagos**, o **Projekto etapas** – **Vykdoma**, sinchronizuojami su „Field Service“ objektu **Išorinis projektas**, įskaitant projekto numerį, projekto pavadinimą, projekto etapą ir kliento sąskaitos informaciją. Sąrašas **Išorinis projektas** naudojamas „Field Service“ darbo užsakymams su Tiekimo grandinės valdymo projektais susieti.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
**Išorinis projektas** yra objektas, gaunantis visus Tiekimo grandinės valdymo projektus. Laukas **Išorinis projektas** įtrauktas į objektą **darbo užsakymo**. Tai peržvalgos laukas, todėl siejant darbo užsakymą su projektu, pardavimo užsakymas sujungiamas su Tiekimo grandinės valdymo projektu. Kai **sistemos būsena** **Atidarytas – vykdomas (690,970,000)** keičiama į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka
### <a name="supply-chain-management"></a>Tiekimo grandinės valdymas
Įgalinti duomenų objekto projektų keitimų sekimą.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projektai (iš Tiekimo grandinės valdymo į „Field Service“): projektai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas.](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]