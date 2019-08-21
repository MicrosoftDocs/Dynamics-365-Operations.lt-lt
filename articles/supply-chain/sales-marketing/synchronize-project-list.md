---
title: „Finance and Operations“ projektų sąrašo sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ projektus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843558"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>„Finance and Operations“ projektų sąrašo sinchronizavimas su „Field Service“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ projektus sinchronizuojant su „Microsoft Dynamics 365 for Field Service“.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projektus su „Microsoft Dynamics 365 for Field Service“.

**Šablonas naudojant funkcija Duomenų integravimas**
- Projektai („Finance and Operations“ su „Field Service“)

**Užduotis projekte Duomenų integravimas**
- Projektai

Prieš sinchronizuojant projektų sąrašą būtina atlikti toliau nurodytas sinchronizavimo užduotis.
- Sąskaitos (iš „Sales“ į „Finance and Operations“) 

## <a name="entity-set"></a>Objektų rinkinys
| Field Service           | „Finance and Operations”  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projektai                |

## <a name="entity-flow"></a>Objekto srautas
„Finance and Operations“ sukurti projektai. Projektai, kurių **Projekto tipas** – **Laikas ir medžiagos**, o **Projekto etapas** – **Vykdoma**, sinchronizuojami su „Field Service“ objektu **Išorinis projektas**, įskaitant projekto numerį, projekto pavadinimą, projekto etapą ir kliento sąskaitos informaciją. Sąrašas **Išorinis projektas** naudojamas „Field Service“ darbo užsakymams su „Finance and Operations“ projektais susieti.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
**Išorinis projektas** yra objektas, gaunantis visus „Finance and Operations“ projektus. Laukas **Išorinis projektas** įtrauktas į objektą **darbo užsakymo**. Šis laukas yra peržvalga, o žymint darbo užsakymą su projektu Pardavimo užsakymas, prijungiama prie „Finance and Operations“ projekto. Kai **sistemos būsena** **Atidarytas – vykdomas (690,970,000)** keičiama į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka
### <a name="finance-and-operations"></a>„Finance and Operations”
Įgalinti duomenų objekto projektų keitimų sekimą.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas


### <a name="projects-fin-and-ops-to-field-service-projects"></a>Projektai („Finance and Operations“ su „Field Service“): projektai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProject1.png)](./media/FSProject1.png)
