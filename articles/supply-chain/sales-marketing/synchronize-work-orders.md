---
title: „Field Service“ darbo užsakymų ir projekto sinchronizavimas su Tiekimo grandinės valdymu
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Dynamics 365 Supply Chain Management“.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
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
ms.openlocfilehash: d2364378ce8992666e374ec6f665c180d2fa1981
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258028"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>„Field Service“ darbo užsakymų ir projekto sinchronizavimas su Tiekimo grandinės valdymu

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Dynamics 365 Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Dynamics 365 Supply Chain Management“.

[![Tiekimo grandinės valdymo ir „Field Service“ verslo procesų sinchronizavimas](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Naudojamas šablonas **Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)** yra paremtas šablonu **Darbo užsakymai (iš „Field Service“ į Tiekimo grandinės valdymą)**. Daugiau informacijos žr. temoje [„Field Service“ darbo užsakymų sinchronizavimas su Tiekimo grandinės valdymo pardavimo užsakymais](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų.
- **Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)**
- **Darbo užsakymai (iš „Field Service“ į Tiekimo grandinės valdymą)**

Pagrindinis skirtumas yra tas, kad į šį šabloną įtraukiamas „Field Service“ darbo užsakymui priskirto projekto numerio susiejimas, užtikrinant, kad į Tiekimo grandinės valdyme sukurtą pardavimo užsakymą būtų įtrauktas projekto numeris ir kad susijusiame projekte galėtų būti išrašomos sąskaitos faktūros. Be to, šis šablonas naudoja išplėstinę užklausą ir filtravimą.

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**

- Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą)

**Užduoties pavadinimas projekte Duomenų integravimas:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
Laukas **Išorinis projektas** įtrauktas į darbo užsakymo objektą. Tai peržvalgos laukas, todėl siejant darbo užsakymą su projektu, pardavimo užsakymas bus sujungtas su Tiekimo grandinės valdymo projektu. Kai **Sistemos būsena** keičiama iš Atidarytas – vykdomas (690,970,000) į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti reikšmės.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderHeader

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderHeaderProject

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderProduct

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Darbo užsakymai su projektu (iš „Field Service“ į Tiekimo grandinės valdymą): WorkOrderService

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]