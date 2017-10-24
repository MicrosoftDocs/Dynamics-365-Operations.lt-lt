---
title: "Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“"
description: "Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ pardavimo užsakymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 707efc97afc0679ed1fc22539789e98cbabcb581
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“

[!include[banner](../includes/banner.md)]

Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ pardavimo užsakymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“. 

## <a name="template-and-tasks"></a>Šablonai ir užduotys

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ pardavimo užsakymų antraštes ir eilutes su „Sales“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas** 

    - Pardavimo užsakymai (iš „Finance and Operations“ į „Sales“)
    
- **Užduočių pavadinimai projekte Duomenų integravimas**

    - OrderHeader
    - OrderLine

Reikiamos sinchronizavimo užduotys prieš sinchronizuojant „Sales“ sąskaitų faktūrų antraštes ir eilutes:

- Produktai (iš „Finance and Operations“ į „Sales“)
- Sąskaitos (iš „Sales“ į „Finance and Operations“) (jei naudojama)
- Iš kontaktų į klientus (iš „Sales“ į „Finance and Operations“) (jei naudojama)

## <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations” |    „Common Data Service“ (CDS)         |     Pardavimas      |
|------------------------|----------------|----------------|
| CDS pardavimo užsakymų antraštės| SalesOrder     | SalesOrders |
| CDS pardavimo užsakymo eilutės  | SalesOrderLine | SalesOrderDetails|

## <a name="entity-flow"></a>Objekto srautas

Pardavimo užsakymai kuriami sprendime „Finance and Operations“ ir sinchronizuojami su „Sales“.

Šablono filtrais užtikrinama, kad sinchronizuojant būtų įtraukiami tik aktualūs pardavimo užsakymai:

- Sinchronizuojant bus įtraukiami tiek užsakantis klientas, tiek sąskaitą faktūrą išrašantis klientas, nurodyti pardavimo užsakyme, gautame iš „Sales“. Sprendime „Finance and Operations“ laukai **OrderingCustomerIsExternallyMaintained** ir **InvoiceCustomerIsExternallyMaintained** naudojami sinchronizavimui duomenų objektuose sekti.

- Sprendime „Finance and Operations“ **pardavimo užsakymą** reikia patvirtinti. Su „Sales“ sinchronizuojami tik patvirtinti pardavimo užsakymai arba pardavimo užsakymai su aukštesne apdorojimo būsena, pavyzdžiui, būsena Išsiųstas arba Išrašyta SF.

- Sukūrus arba modifikavus pardavimo užsakymą, reikia vykdyti „Finance and Operations“ paketinę užduotį **Skaičiuoti bendrąsias pardavimo sumas**. Su CDS ir „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kurių bendrosios pardavimo sumos apskaičiuotos.

> [!NOTE]
> Su **pardavimo užsakymo antraštės** išlaidomis susijęs mokestis į sinchronizavimo iš „Finance and Operations“ į „Sales“ procesą šiuo metu nėra įtrauktas. Taip yra todėl, kad „Sales“ nepalaiko mokesčių informacijos antraštės lygyje. Įtrauktas mokestis, susijęs su išlaidomis eilutės lygyje.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Į objektą **Užsakymas** įtraukiami nauji toliau nurodyti laukai, kurie rodomi puslapyje.

- **Tvarkomas išoriškai** – nustatykite kaip **Taip**, kai užsakymas yra iš „Finance and Operations“.

- **Apdorojimo būsena** – naudojamas „Finance and Operations“ užsakymo apdorojimo būsenai rodyti. Reikšmės nurodytos toliau.

    - Aktyvu
    - Pritarta
    - Važtaraštis
    - SF išrašyta
    - Paimta
    - Iš dalies paimtas
    - Iš dalies supakuotas
    - Išsiųsta
    - Iš dalies išsiųstas
    - Iš dalies išrašyta SF
    - Atšaukta

Kitose su pardavimo užsakymais susijusiose situacijose (sinchronizuojant iš „Sales“ į „Finance and Operations“) naudojamas parametras **Sudaro tik išoriškai tvarkomi produktai**, kuriuo nuosekliai sekama, ar visą pardavimo užsakymą sudaro tik **Išoriškai tvarkomi produktai**, o tokiu atveju produktai tvarkomi sprendime „Finance and Operations“. Taip užtikrinama, kad nebandysite pardavimo užsakymo eilučių sinchronizuoti su produktais, kurių „Finance and Operations“ neatpažįsta.
 
Išoriškai tvarkomuose užsakymuose puslapio **Pardavimo užsakymas** mygtukai **Kurti sąskaitą faktūrą**, **Atšaukti užsakymą**, **Perskaičiuoti**, **Gauti produktų** ir **Peržvelgti adresą** yra paslėpti, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“. Užsakymo puslapio redaguoti negalima, nes pardavimo užsakymo informacija bus sinchronizuojama iš „Finance and Operations“.
 
Sritis **Pardavimo užsakymo būsena** liks aktyvi, siekiant užtikrinti, kad keitimai iš „Finance and Operations“ galėtų būti perkelti į „Sales“ sritį **Pardavimo užsakymas**. Tai valdoma projekte Duomenų integravimas numatytąją srities **Būsenos kodas [būsena]** reikšmę nustačius kaip **Aktyvu**.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas 

Prieš sinchronizuojant pardavimo užsakymus, svarbu sistemas atnaujinti tolesniu parametru.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

- Suteikite teises komandai, kuriai priskirtas vartotojas (iš „Sales“ **ryšio rinkinio**). Jei naudojate demonstracinius duomenis, paprastai administravimo prieigą turi vartotojas, bet ne komanda. To nenustatę, vykdydami projektą duomenų integratoriuje, gausite klaidą, kad trūksta pagrindinės komandos. 

    - Srityje **Parametrai** > **Sauga** > **Komandos** pasirinkite reikiamą komandą, spustelėkite **Valdyti vaidmenis** ir pasirinkite vaidmenį su norimomis teisėmis, pvz., Sistemos administratorius.

- Įsitikinkite, kad dalyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas** parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta kaip **Taip**. 

- Įsitikinkite, kad dalyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas** parinktis **Nuolaidos skaičiavimo būdas** nustatyta kaip **Eilutės prekė**. 

### <a name="setup-in-finance-and-operations"></a>Sąranka sprendime „Finance and Operations“

Nustatykite, kad užduotis **Pardavimas ir rinkodara** > **Periodinės užduotys** > **Skaičiuoti bendrąsias pardavimo sumas** būtų vykdoma kaip paketinė užduotis, o parinktį **Skaičiuoti bendrąsias pardavimo užsakymų sumas** nustatykite kaip **Taip**. Tai – svarbu, nes su CDS ir „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kurių bendrosios pardavimo sumos apskaičiuotos. Paketinės užduoties dažnis turi būti lygus pardavimo užsakymų sinchronizavimo dažniui.

### <a name="setup-in-the-data-integration-project"></a>Sąranka projekte Duomenų integravimas

#### <a name="salesheader-task"></a>SalesHeader užduotis

- Dalyje **Šaltinis** > **CDS** atnaujinkite CDS organizacijos ID susiejimą.

    - Numatytoji **Account_Organization_OrganizationId** šablono reikšmė yra ORG001.
    - Numatytoji **InvoiceAccount_Organization_OrganizationId** šablono reikšmė yra ORG001.
    - Numatytoji **Organization_OrganizationId** šablono reikšmė yra ORG001.

- Įsitikinkite, kad dalyje **Šaltinis** > **InvoiceCountryRegionId su BillingAddress_Country CDS** ir **DeliveryCountryRegionId su DeliveryAddress_Country** yra reikiamas susiejimas.

    - Šablono reikšmė yra **ValueMap** su susietų šalių skaičiumi.

- Sprendime „Sales“ norint kurti užsakymus, reikalingas **Kainoraštis**. **Dalyje** **CDS** > **pricelevelid.name paskirtis [kainoraščio pavadinimas]** kiekvienos valiutos reikšmę **ValueMap** atnaujinkite į sprendime „Sales“ naudojamą **kainoraštį**. Galite naudoti numatytąjį vienos valiutos **kainoraštį** arba **ValueMap**, jei turite **kainoraščių** keliomis valiutomis.
    
    - Numatytoji **pricelevelid.name [kainoraščio pavadinimas]** šablono reikšmė yra „CRM Service USA“ (pavyzdys). 

#### <a name="salesline-task"></a>SalesLine užduotis

- Dalyje **Šaltinis** > **CDS** atnaujinkite CDS organizacijos ID susiejimą. 
    
    - Numatytoji **SalesOrder_Organization_OrganizationId** šablono reikšmė yra ORG001.
    - Numatytoji **Product_Organization_OrganizationId** šablono reikšmė yra ORG001.

- Įsitikinkite, kad dalyje **Šaltinis** > **CDS** yra reikiamas **DeliveryCountryRegionId** susiejimas su **DeliveryAddress_Country**.

    - Šablono reikšmė yra **ValueMap** su susietų šalių skaičiumi.
    
- Įsitikinkite, kad „Finance and Operations“ dalyje **Šaltinis** > **CDS susiejimas** yra reikiama **SalesUnitSymbol** **ValueMap** reikšmė.

    - Apibrėžta **SalesUnitSymbol su Quantity_UOM** šablono reikšmė su **ValueMap**.

## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

> [!NOTE]
> Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

### <a name="orderheader"></a>OrderHeader

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-template-mapping-data-integrator-1.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>OrderLine

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-template-mapping-data-integrator-3.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Susijusios temos

[Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais](products-template-mapping.md)

[Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais](accounts-template-mapping.md)

[Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping.md)

[Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“](sales-quotation-template-mapping.md)

[Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“](sales-invoice-template-mapping.md)


