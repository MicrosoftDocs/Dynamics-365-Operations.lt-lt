---
title: „Field Service“ darbo užsakymų ir projekto sinchronizavimas su „Supply Chain Management”
description: Šiame straipsnyje aptariamas šablonas ir žemiau nurodyta užduotis, kurios naudojamos darbo užsakymams sinchronizuoti su projekto numeriu Nuo Dynamics 365 Field Service Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 03/12/2019
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
ms.openlocfilehash: a43a7f7e900205bdb23fb9a35ca1518369683a42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860499"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>„Field Service“ darbo užsakymų ir projekto sinchronizavimas su „Supply Chain Management”

[!include[banner](../includes/banner.md)]

Šiame straipsnyje aptariamas šablonas ir žemiau nurodyta užduotis, kurios naudojamos darbo užsakymams sinchronizuoti su projekto numeriu Nuo Dynamics 365 Field Service Dynamics 365 Supply Chain Management.

[![„Supply Chain Management“ ir „Field Service“ verslo procesų sinchronizavimas.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Naudojamas šablonas **Darbo užsakymai su projektu (iš „Field Service“ į „Supply Chain Management”)** yra paremtas šablonu **Darbo užsakymai (iš „Field Service“ į „Supply Chain Management”)**. Daugiau informacijos žr. temoje [„Field Service“ darbo užsakymų sinchronizavimas su „Supply Chain Management” pardavimo užsakymais](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Šiame straipsnyje aprašomi tik šių dviejų šablonų skirtumai:
- **Darbo užsakymai su projektu (iš „Field Service“ į „Supply Chain Management”)**
- **Darbo užsakymai (iš „Field Service“ į „Supply Chain Management”)**

Pagrindinis skirtumas yra tas, kad į šį šabloną įtraukiamas „Field Service“ darbo užsakymui priskirto projekto numerio susiejimas, užtikrinant, kad į „Supply Chain Management” sukurtą pardavimo užsakymą būtų įtrauktas projekto numeris ir kad susijusiame projekte galėtų būti išrašomos sąskaitos faktūros. Be to, šis šablonas naudoja išplėstinę užklausą ir filtravimą.

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**

- Darbo užsakymai su projektu (iš „Field Service“ į „Supply Chain Management”)

**Užduoties pavadinimas projekte Duomenų integravimas:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
Laukas **Išorinis projektas** įtrauktas į darbo užsakymo objektą. Tai peržvalgos laukas, todėl siejant darbo užsakymą su projektu, pardavimo užsakymas bus sujungtas su „Supply Chain Management” projektu. Kai **Sistemos būsena** keičiama iš Atidarytas – vykdomas (690,970,000) į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti reikšmės.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Darbo užsakymai su projektu (iš „Field Service“ į „Supply Chain Management”): WorkOrderHeader

[![Šablono susiejimas integruojant darbo užsakymų duomenis su darbo su projektu užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderHeader.](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Darbo užsakymai su projektu (iš „Field Service“ į „Supply Chain Management”): WorkOrderHeaderProject

[![Šablono susiejimas integruojant darbo užsakymų duomenis su darbo su projektu užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderHeaderProject.](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Darbo užsakymai su projektu (iš „Field Service“ į „Supply Chain Management”): WorkOrderProduct

[![Šablono susiejimas integruojant darbo užsakymų duomenis su darbo su projektu užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderProduct.](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Darbo užsakymai su projektu (iš „Field Service“ į „Supply Chain Management”): WorkOrderService

[![Šablono susiejimas integruojant darbo užsakymų duomenis su darbo su projektu užsakymais („Field Service“ ir „Supply Chain Management“): WorkOrderService.](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]