---
title: "„Finance and Operations“ projektų sąrašo sinchronizavimas su „Field Service“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projektus su „Microsoft Dynamics 365 for Field Service“."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: lt-lt
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>„Finance and Operations“ projektų sąrašo sinchronizavimas su „Field Service“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projektus su „Microsoft Dynamics 365 for Field Service“.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys
Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Microsoft Dynamics 365 for Finance and Operations“ projektus su „Microsoft Dynamics 365 for Field Service“.

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**
- Projektai („Finance and Operations“ su „Field Service“)

**Užduočių pavadinimai projekte Duomenų integravimas:**
- Projektai

Prieš sinchronizuojant projektų sąrašą būtina atlikti toliau nurodytas sinchronizavimo užduotis.
- Sąskaitos („Sales“ su „Finance and Operations“) 

## <a name="entity-set"></a>Objektų rinkinys
„Field Service“   „Finance and Operations“

| Field Service           | „Finance and Operations”  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projektai                |

## <a name="entity-flow"></a>Objekto srautas
„Finance and Operations“ sukurti projektai. Projektai, kurių **Projekto tipas** – Laikas ir medžiagos, o **Projekto etapas** – Vykdoma, sinchronizuojami su „Field Service“ objektu **Išorinis objektas**, įskaitant projekto numerį, projekto pavadinimą, projekto etapą ir kliento sąskaitos informaciją. **Išorinio projekto** sąrašas naudojamas „Field Service“ darbo užsakymams su „Finance and Operations“ projektais susieti.
„Field Service“ CRM sprendimas Išorinis projektas yra naujas objektas, gaunantis visus „Operations“ projektus.
Išorinio projekto laukas įtrauktas į darbo užsakymo objektą. Šis laukas yra peržvalga, o žymint darbo užsakymą su projektu Pardavimo užsakymas, prijungiama prie „Operations“ projekto. Kai sistemos būsena „Atidarytas – vykdomas“ (690,970,000) keičiama į aukštesnę būseną, išorinio projekto laukas užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka
### <a name="in-finance-and-operations"></a>Programoje „Finance and Operations”
Įgalinti duomenų objekto projektų keitimų sekimą

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projektai („Finance and Operations“ su „Field Service“): projektai

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProject1.png)](./media/FSProject1.png)

