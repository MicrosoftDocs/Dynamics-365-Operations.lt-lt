---
title: "Potencialūs klientai ir grynieji pinigai"
description: "Šioje temoje apžvelgiamas „Microsoft Dynamics 365 for Finance and Operations Enterprise edition“ ir „Microsoft Dynamics 365 for Sales“ sprendimas Potencialūs klientai ir grynieji pinigai."
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: lt-lt
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>Potencialūs klientai ir grynieji pinigai

[!include[banner](../includes/banner.md)]

Sprendimas Potencialūs klientai ir grynieji pinigai leidžia tiesiogiai sinchronizuoti „Microsoft Dynamics 365 for Finance and Operations Enterprise edition“ su „Microsoft Dynamics 365 for Sales“. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus. Sukūrus duomenų srautą tarp „Finance and Operations“ ir „Sales“ galima vykdyti pardavimo ir rinkodaros veiklas sprendime „Sales“ bei tvarkyti užsakymų įvykdymą naudojant atsargų valdymo funkciją sprendime „Finance and Operations“.

Dabartinėje versijoje sprendimas Potencialūs klientai ir grynieji pinigai leidžia šių tipų tiesioginį sinchronizavimą:

- [„Sales“ sąskaitų tvarkymas ir tiesioginis „Sales“ sinchronizavimas su „Finance and Operations“](accounts-template-mapping-direct.md)
- [„Finance and Operations“ produktų tvarkymas ir tiesioginis sinchronizavimas su „Sales“](products-template-mapping-direct.md)
- [„Sales“ kontaktų tvarkymas ir tiesioginis sinchronizavimas su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping-direct.md)
- [Tiesioginis „Sales“ pardavimo pasiūlymų sinchronizavimas iš „Sales“ į „Finance and Operations“](sales-quotation-template-mapping-sales-fin.md)
- [Tiesioginis pardavimo užsakymų sinchronizavimas iš „Finance and Operations“ į „Sales“](sales-order-template-mapping-direct.md)
- [Pardavimo užsakymų tiesioginis sinchronizavimas tarp „Sales“ ir „Finance and Operations“](sales-order-template-mapping-direct-two-ways.md)
- [Tiesioginis pardavimo sąskaitų faktūrų sinchronizavimas iš „Finance and Operations“ į „Sales“](sales-invoice-template-mapping-direct.md)

Ankstesnėse versijose sprendimas Potencialūs klientai ir grynieji pinigai leidžia šių tipų netiesioginį sinchronizavimą:

- [„Sales“ sąskaitų tvarkymas ir sinchronizavimas su „Finance and Operations“](accounts-template-mapping.md)
- [„Sales“ kontaktų tvarkymas ir sinchronizavimas su „Finance and Operations“](contacts-template-mapping.md)
- [„Finance and Operations“ produktų tvarkymas ir sinchronizavimas su „Sales“](products-template-mapping.md)
- [Pardavimo pasiūlymų kūrimas sprendime „Sales“ ir jų sinchronizavimas su „Finance and Operations“](sales-quotation-template-mapping.md)
- [Pardavimo užsakymų kūrimas sprendime „Finance and Operations“ ir jų sinchronizavimas su „Sales“](sales-order-template-mapping.md)
- [Pardavimo sąskaitų faktūrų kūrimas sprendime „Finance and Operations“ ir jų sinchronizavimas su „Sales“](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>„Finance and Operations“ sistemos reikalavimai

Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti šiuos komponentus:

### <a name="july-2017"></a>Liepos 2017 d. 

- „Microsoft Dynamics 365 for Finance and Operations Enterprise edition“ (2017 m. liepos mėn.) su 8 platformos naujinimu (programos komponavimo versija 7.2.11792.56024, platformos komponavimo versija 7.0.4565.16212)
- Šios „Finance and Operations“ karštosios pataisos:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Sales“ pardavimo užsakymus sinchronizuoti su „Finance and Operations“. Jos taip pat suteikia kelis kitus patobulinimus.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Finance and Operations“ pardavimo užsakymų eilutes sinchronizuoti su „Sales“.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Finance and Operations“ pardavimo užsakymus sinchronizuoti su „Sales“.

    > [!NOTE]
    > Reikia įdiegti tik KB4045570, nes į įdiegtį įtraukti kitų „Microsoft“ žinių bazės (KB) straipsnių pakeitimai.

### <a name="november-2016-version-1611"></a>2016 m. lapkričio mėn. (1611 versija)

- „Microsoft Dynamics 365 for Finance and Operations Enterprise edition“ (2016 m. lapkričio mėn.) su 8 arba naujesniu platformos naujinimu

- Šios „Finance and Operations“ karštosios pataisos:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – įgalina naudojant funkciją Duomenų integravimas „Microsoft Dynamics 365 for Finance and Operations“ pardavimo užsakymų sinchronizavimą su „Sales“. 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – įgalina naudojant funkciją Duomenų integravimas „Microsoft Dynamics 365 for Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimą su „Sales“.
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – reikalingas potencialių klientų ir grynųjų pinigų integravimo naudojant duomenų objektus palaikymas
    
    > [!NOTE]
    > Įdiegę karštąsias pataisas, turite paleisti paketinę užduotį formoje SalesPopulateProspectToCash. Ši forma paslėpta, nes jos jums reikia tik kartą. Norėdami ją pasiekti, prisijungę prie aplinkos į naršyklės adresą įtraukite &mi=action:SalesPopulateProspectToCash, pvz., https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash. Atsidariusioje formoje spustelėkite Gerai.
    Į naują lauką „LineCreationSequnceNumber“ lentelėse „SalesLine“, „SalesQuotationLine“ ir „CustInvoiceTrans“ bus automatiškai įvestos unikalios reikšmės ir atnaujintas produktų sąrašas. Tai būtina, kad P2C integravimas veiktų 7.1 versijoje


## <a name="system-requirements-for-sales"></a>„Sales“ sistemos reikalavimai

Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti šiuos komponentus:

- „Microsoft Dynamics 365 for Sales“ versija 1612 (8.2.1.207) (DB 8.2.1.207) (internetinė versija)
- Sprendimui „Microsoft Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai versija 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > Šablonai su versija 1.0.0.0 1.0.0.1 palaikomi „Microsoft Dynamics 365 for Sales“ skirtame sprendime Potencialūs klientai ir grynieji pinigai, versijoje 1.14.1.0
   >
   > Šablonai su versija 2.0.0.0 2.1.0.0 nepalaikomi „Microsoft Dynamics 365 for Sales“ skirtame sprendime Potencialūs klientai ir grynieji pinigai, versijoje 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Sprendimui „Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai diegimas

1. Iš „CustomerSource“ atsisiųskite [Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai paketo ZIP failą](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash).
2. Užtikrinkite, kad ZIP failas atblokuotas. Priešingu atveju, kai bandysite įdiegti sprendimo paketą, gausite tokį klaidos pranešimą: „Nerasta jokių importavimo paketų“. Norėdami atblokuoti ZIP failą, spustelėkite jį dešiniuoju pelės mygtuku ir pasirinkite **Ypatybės**. Tada pasirinkite **Atblokuoti**.
3. Išskleiskite ir paleiskite **PackageDeployer.exe**.
4. Savo „Sales“ egzemplioriuje įdiekite sprendimą Potencialūs klientai ir grynieji pinigai:

    1. Pasirinkite **„Office 365“** kaip visuotinio diegimo tipą.
    2. Pasirinkite **Rodyti išplėstines parinktis**.
    3. Norėdami greitai įdiegti, pasirinkite regioną. Jei pasirenkate **Nežinau**, sistema ieško visų regionų ir diegimas trunka ilgiau.
    4. Įveskite administratoriaus vartotojo, turinčio diegimo teises, vartotojo vardą ir slaptažodį.

