---
title: Tiekimo grandinės valdymo projektų sąrašo sinchronizavimas su „Field Service“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ projektus sinchronizuojant su „Dynamics 365 Field Service“.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3d17b226cabd0668bcdb52e9a7fdfc5973fe49b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243062"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Tiekimo grandinės valdymo projektų sąrašo sinchronizavimas su „Field Service“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ projektus sinchronizuojant su „Dynamics 365 Field Service“.

[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSProjectOW.png)](./media/FSProjectOW.png)

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

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]