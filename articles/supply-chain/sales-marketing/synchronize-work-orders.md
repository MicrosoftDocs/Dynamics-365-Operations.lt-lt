---
title: „Field Service“ darbo užsakymų su projektu sinchronizavimas su „Finance and Operations“
description: Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536738"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>„Field Service“ darbo užsakymų su projektu sinchronizavimas su „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinė užduotis, naudojami „Microsoft Dynamics 365 for Field Service“ darbo užsakymus su projekto numeriu sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.

[![„Finance and Operations“ ir „Field Service“ verslo procesų sinchronizavimas](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Naudojamas šablonas **Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“)** yra paremtas šablonu **Darbo užsakymai („Field Service“ su „Fin and Ops“)**. Daugiau informacijos žr. temoje [„Field Service“ darbo užsakymų sinchronizavimas su „Finance and Operations“ pardavimo užsakymais](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Šioje temoje aprašomi tik skirtumus tarp dviejų šablonų.
- **Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“)**
- **Darbo užsakymai („Field Service“ su „Fin and Ops“)**

Pagrindinis skirtumas yra tas, kad į šį šabloną įtraukiamas „Field Service“ darbo užsakymui priskirto projekto numerio susiejimas, užtikrinant, kad į „Finance and Operations“ sukurtą pardavimo užsakymą būtų įtrauktas projekto numeris ir kad susijusiame projekte galėtų būti išrašomos sąskaitos faktūros. Be to, šis šablonas naudoja išplėstinę užklausą ir filtravimą.

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**

- Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“)

**Užduoties pavadinimas projekte Duomenų integravimas:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas
Laukas **Išorinis projektas** įtrauktas į darbo užsakymo objektą. Šis laukas yra peržvalga, o žymint darbo užsakymą su projektu Pardavimo užsakymas, prijungiama prie „Finance and Operations“ projekto. Kai **Sistemos būsena** keičiama iš „Atidarytas – vykdomas“ (690,970,000) į aukštesnę būseną, laukas **Išorinis projektas** užrakinamas, todėl negalėsite įtraukti, pašalinti ar pakeisti vertės.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“): WorkOrderHeader

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“): WorkOrderHeaderProject

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“): WorkOrderProduct

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Darbo užsakymai su projektu („Field Service“ su „Fin and Ops“): WorkOrderService

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSWOP4.png)](./media/FSWOP4.png)
