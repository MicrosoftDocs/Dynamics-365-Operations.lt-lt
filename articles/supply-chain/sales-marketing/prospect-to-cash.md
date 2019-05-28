---
title: Potencialūs klientai ir grynieji pinigai
description: Šioje temoje apžvelgiamas „Microsoft Dynamics 365 for Finance and Operations“ ir „Microsoft Dynamics 365 for Sales“ sprendimas Potencialūs klientai ir grynieji pinigai.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b46ece384a28f8e78989253fcf467fbf3feaf1b7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554626"
---
# <a name="prospect-to-cash"></a>Potencialūs klientai ir grynieji pinigai

[!include [banner](../includes/banner.md)]

Sprendimas Potencialūs klientai ir grynieji pinigai leidžia tiesiogiai sinchronizuoti „Dynamics 365 for Finance and Operations“ su „Dynamics 365 for Sales“. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus. Sukūrus duomenų srautą tarp „Finance and Operations“ ir „Sales“ galima vykdyti pardavimo ir rinkodaros veiklas sprendime „Sales“ bei tvarkyti užsakymų įvykdymą naudojant atsargų valdymo funkciją sprendime „Finance and Operations“. 

Norėdami gauti daugiau informacijos apie sprendimo Potencialūs klientai ir grynieji pinigai integravimą, peržiūrėkite trumpą „YouTube“ vaizdo įrašą: [Sprendimo Potencialūs klientai ir grynieji pinigai integravimas](https://www.youtube.com/watch?v=AVV9x5x-XCg).

Dabartinėje versijoje sprendimas Potencialūs klientai ir grynieji pinigai leidžia šių tipų tiesioginį sinchronizavimą:

- [„Sales“ sąskaitų tvarkymas ir tiesioginis „Sales“ sinchronizavimas su „Finance and Operations“](accounts-template-mapping-direct.md)
- [„Finance and Operations“ produktų tvarkymas ir tiesioginis sinchronizavimas su „Sales“](products-template-mapping-direct.md)
- [„Sales“ kontaktų tvarkymas ir tiesioginis sinchronizavimas su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping-direct.md)
- [Tiesioginis „Sales“ pardavimo pasiūlymų sinchronizavimas iš „Sales“ į „Finance and Operations“](sales-quotation-template-mapping-sales-fin.md)
- [Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Finance and Operations“](sales-order-template-mapping-direct-two-ways.md)
- [Tiesioginis pardavimo sąskaitos faktūros sinchronizavimas iš „Finance and Operations“ į „Sales“](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>„Finance and Operations“ sistemos reikalavimai
Sprendimo Potencialūs klientai ir grynieji pinigai integravimo funkcija palaikoma tolesnėse versijose.

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>„Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3“ (2017 m. gruodžio mėn.)

- „Dynamics 365 for Finance and Operations, Enterprise Edition“ (2017 m. gruodžio mėn.) – programos komponavimo versija 7.3.11971.56116 su 12 platformos naujinimu (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>„Dynamics 365 for Finance and Operations, Enterprise Edition“ (2017 m. liepos mėn.)

- „Dynamics 365 for Finance and Operations, Enterprise Edition“ (2017 m. liepos mėn.) – su 8 platformos naujinimu (programos komponavimo versija 7.2.11792.56024, platformos komponavimo versija 7.0.4565.16212).
- Būtinos toliau nurodytos karštosios pataisos.

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Sales“ pardavimo užsakymus sinchronizuoti su „Finance and Operations“. Jos taip pat suteikia kelis kitus patobulinimus.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Finance and Operations“ pardavimo užsakymų eilutes sinchronizuoti su „Sales“.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Finance and Operations“ pardavimo užsakymus sinchronizuoti su „Sales“.

    > [!NOTE]
    > Turite įdiegti tik KB4045570, nes į įdiegtį įtraukti kitų karštųjų pataisų pakeitimai. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>„Dynamics 365 for Finance and Operations“ 1611 versija (2016 m. lapkričio mėn.)

- „Dynamics 365 for Finance and Operations“ 1611 versija (2016 m. lapkričio mėn.) su 8 arba naujesniu platformos naujinimu

- Būtinos toliau nurodytos karštosios pataisos.

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – įgalina naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymų sinchronizavimą su „Sales“. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – įgalina naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymo antraščių ir eilučių sinchronizavimą su „Sales“.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – reikalingas potencialių klientų ir grynųjų pinigų integravimo naudojant duomenų objektus palaikymas.
    
    > [!NOTE]
    > Įdiegę karštąsias pataisas, turite paleisti paketinę užduotį formoje **SalesPopulateProspectToCash**. Ši forma paslėpta, nes jos jums reikia tik kartą. Norėdami atidaryti formą, prisijunkite prie aplinkos ir prie naršyklės adreso pridėkite šį URL: *&mi=action:SalesPopulateProspectToCash*, pvz., `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Atsidarius formai spustelėkite Gerai. Į naują lauką **LineCreationSequnceNumber** lentelėse **SalesLine**, **SalesQuotationLine** ir **CustInvoiceTrans** bus automatiškai įvestos unikalios reikšmės ir atnaujintas produktų sąrašas. Tai yra būtina, veiktų potencialių klientų ir grynųjų pinigų integravimas.


## <a name="system-requirements-for-sales"></a>„Sales“ sistemos reikalavimai

Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti šiuos komponentus:

- „Dynamics 365 for Sales“ versija 1612 (8.2.1.207) (DB 8.2.1.207) (internetinė versija) arba naujesnė versija
- Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai 1.15.0.0 arba naujesnė versija. Sprendimą galima atsisiųsti iš „AppSource“. [„Dynamics 365“ sprendimo Potencialaus kliento pavertimo pinigais atsisiuntimas](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
