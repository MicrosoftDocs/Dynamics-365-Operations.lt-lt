---
title: Potencialūs klientai ir grynieji pinigai
description: Šioje temoje apžvelgiamas „Dynamics 365 Supply Chain Management“ ir „Dynamics 365 Sales“ sprendimas Potencialūs klientai ir grynieji pinigai.
author: ChristianRytt
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: bb928a14d231bef1255612194ec9fdeb9be8f611d26aa4dfbf3efaec8a8d3e9f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726686"
---
# <a name="prospect-to-cash"></a>Potencialaus kliento pavertimas pinigais

[!include [banner](../includes/banner.md)]

Sprendimas Potencialūs klientai ir grynieji pinigai leidžia tiesiogiai sinchronizuoti „Dynamics 365 Supply Chain Management“ su „Dynamics 365 Sales“. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, pasiekiamus naudojant duomenų integravimo funkciją, įgalinami sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautai. Sukūrus duomenų srautą, galima vykdyti pardavimo ir rinkodaros veiklas sprendime „Sales“ bei tvarkyti užsakymų įvykdymą naudojant atsargų valdymo funkciją sprendime Tiekimo grandinės valdymas. 

Norėdami gauti daugiau informacijos apie sprendimo Potencialūs klientai ir grynieji pinigai integravimą, peržiūrėkite trumpą „YouTube“ vaizdo įrašą: [Sprendimo Potencialūs klientai ir grynieji pinigai integravimas](https://www.youtube.com/watch?v=AVV9x5x-XCg).

Dabartinėje versijoje sprendimas Potencialūs klientai ir grynieji pinigai leidžia šių tipų tiesioginį sinchronizavimą:

- [Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais](accounts-template-mapping-direct.md)
- [Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Sales“ produktais](products-template-mapping-direct.md)
- [Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais](contacts-template-mapping-direct.md)
- [Tiesioginis „Sales“ pardavimo pasiūlymų antraščių ir eilučių sinchronizavimas su Tiekimo grandinės valdymu](sales-quotation-template-mapping-sales-fin.md)
- [Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir Tiekimo grandinės valdymo](sales-order-template-mapping-direct-two-ways.md)
- [Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>„Supply Chain Management“ sistemos reikalavimai
Sprendimo Potencialūs klientai ir grynieji pinigai integravimo funkcija palaikoma tolesnėse versijose.

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>„Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3“ (2017 m. gruodžio mėn.)

- „Dynamics 365 for Finance and Operations, Enterprise Edition“ (2017 m. gruodžio mėn.) – programos komponavimo versija 7.3.11971.56116 su 12 platformos naujinimu (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>„Dynamics 365 for Finance and Operations, Enterprise Edition“ (2017 m. liepos mėn.)

- „Dynamics 365 for Finance and Operations, Enterprise Edition“ (2017 m. liepos mėn.) – su 8 platformos naujinimu (programos komponavimo versija 7.2.11792.56024, platformos komponavimo versija 7.0.4565.16212).
- Būtinos toliau nurodytos karštosios pataisos.

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Sales“ pardavimo užsakymus sinchronizuoti su Tiekimo grandinės valdymu. Jos taip pat suteikia kelis kitus patobulinimus.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima Tiekimo grandinės valdymo pardavimo užsakymo eilutę sinchronizuoti su „Sales“.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima Tiekimo grandinės valdymo pardavimo užsakymus sinchronizuoti su „Sales“.

    > [!NOTE]
    > Turite įdiegti tik KB4045570, nes į įdiegtį įtraukti kitų karštųjų pataisų pakeitimai. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>„Dynamics 365 for Finance and Operations“ 1611 versija (2016 m. lapkričio mėn.)

- „Dynamics 365 for Finance and Operations“ 1611 versija (2016 m. lapkričio mėn.) su 8 arba naujesniu platformos naujinimu

- Būtinos toliau nurodytos karštosios pataisos.

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – įgalina Tiekimo grandinės valdymo pardavimo užsakymų sinchronizavimą su „Sales“ naudojant Duomenų integratorių. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – įgalina Tiekimo grandinės valdymo pardavimo užsakymo antraštės ir eilutės sinchronizavimą su „Sales“ naudojant Duomenų integratorių.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – reikalingas potencialių klientų ir grynųjų pinigų integravimo naudojant duomenų objektus palaikymas.
    
    > [!NOTE]
    > Įdiegę karštąsias pataisas, turite paleisti paketinę užduotį formoje **SalesPopulateProspectToCash**. Ši forma paslėpta, nes jos jums reikia tik kartą. Norėdami atidaryti formą, prisijunkite prie aplinkos ir prie naršyklės adreso pridėkite šį URL: *&mi=action:SalesPopulateProspectToCash*, pvz., `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Atsidarius formai spustelėkite Gerai. Į naują lauką **LineCreationSequnceNumber** lentelėse **SalesLine**, **SalesQuotationLine** ir **CustInvoiceTrans** bus automatiškai įvestos unikalios reikšmės ir atnaujintas produktų sąrašas. Tai yra būtina, veiktų potencialių klientų ir grynųjų pinigų integravimas.


## <a name="system-requirements-for-sales"></a>„Sales“ sistemos reikalavimai

Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti šiuos komponentus:

- „Dynamics 365 Sales“ 1612 versija (8.2.1.207) (DB 8.2.1.207) (internetinė versija) arba naujesnė versija
- „Dynamics 365 Sales“ skirtą sprendimą Potencialūs klientai ir grynieji pinigai 1.15.0.0 arba naujesnė versija. Sprendimą galima atsisiųsti iš „AppSource“. [„Dynamics 365“ sprendimo Potencialaus kliento pavertimo pinigais atsisiuntimas](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]