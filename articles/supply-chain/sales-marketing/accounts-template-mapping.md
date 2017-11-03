---
title: "Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ sąskaitas sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimo)."
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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: f322c5b273c29d863c059092bf1a41c424c19a7d
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration). 

Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales (Sales)“ sąskaitas sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimu, „Finance and Operations“).

## <a name="template-and-task"></a>Šablonai ir užduotys

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ sąskaitas su „Finance and Operations“.

- **Šablono pavadinimas:** sąskaitos (iš „Sales“ į „Finance and Operations“)
- **Užduoties pavadinimas projekte:** sąskaitos – sąskaita – klientai

Prieš sukuriant sąskaitą būtina sinchronizuoti užduotis / atlikti kliento sinchronizavimą: nėra

## <a name="entity-set"></a>Objektų rinkinys

| Pardavimas    | CDS     | „Finance and Operations” |
|----------|---------|------------------------|
| Sąskaitos | Paskyra | Klientai              |

## <a name="entity-flow"></a>Objekto srautas

Sąskaitos valdomos programoje „Sales“ ir su „Finance and Operations“ sinchronizuojamos kaip klientai. Ypatybė **Tvarkoma išoriškai** šiems klientams nustatyta į **Taip**, kad būtų galima sekti klientus, atsirandančius iš „Sales“. Išrašant sąskaitą faktūrą ši informacija naudojama sąskaitoms faktūros, sinchronizuojamoms su „Sales“, filtruoti.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Laukas **Sąskaitos numeris** galimas puslapyje **Sąskaita**. Integracijai palaikyti buvo sukurtas srities ir unikalus raktas. Ryšių su klientais valdymo (CRM) sprendimo srities rakto funkcija gali turėti įtakos klientams, jau naudojantiems lauką **Sąskaitos numeris**, bet nenaudojantiems unikalių **Sąskaitos numerio** verčių kiekvienoje sąskaitoje. Šiuo metu integravimo sprendimas nepalaiko šio atvejo.

Sukūrus naują sąskaitą, bet nesant vertei **Sąskaitos numeris**, ji automatiškai sugeneruojama naudojant numeraciją. Vertę sudaro raidės **ACC**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis. Pavyzdys: **ACC-01000-BVRCPS**

Pritaikius integravimo sprendimą „Sales“ naujinimo scenarijus nustato lauką **Sąskaitos numeris** „Sales“ esamoms sąskaitoms. Jei lauko **Sąskaitos numeris** verčių nėra, naudojama anksčiau aprašyta numeracija.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

- **CustomerGroupId** susiejimą iš **CDS &gt; Paskirties vieta** reikia atnaujinti į tinkamą „Finance and Operations“ reikšmę. Galite nurodyti numatytąją vertę arba ją nustatyti naudodami verčių schemą. Numatytoji šablono vertė yra **10**.
- „Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas. Norėdami išvengti sinchronizavimo klaidų, susiejime iš **CDS &gt; Paskirties vieta** galite nurodyti numatytąją reikšmę. Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.

    - Numatytoji **AddressCountryRegionISOCode** šablono vertė yra **USA**.
    - Numatytoji **DeliveryAddressCountryRegionISOCode** šablono reikšmė vertė **USA**.

- Pridėdami toliau nurodytus susiejimus iš **CDS &gt; Paskirties vietos** galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių. Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.

    - **SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes. Numatytąją vietą galima paimti iš produkto arba iš kliento užsakymo antraštės. Numatytoji **SiteId** šablono vertė yra **1**.
    - **WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes. Numatytąjį sandėlį galima paimti iš produkto arba iš „Finance and Operations“ kliento užsakymo antraštės. Numatytoji **WarehouseId** šablono vertė yra **13**.
    - **LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus. Pagal numatytuosius nustatymus naudojama kalba iš kliento užsakymo antraštės. Numatytoji **LanguageId** šablono vertė yra **en-us**.

- Atnaujinkite CDS organizacijos ID (**Organization_OrganizationId**) dalies **Šaltinis &gt; CDS** susiejime. Numatytoji šablono vertė yra **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

> [!NOTE]
> Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti verčių schemą. Verčių susiejimams būdingi duomenys organizacijų, tarp kurių objektas yra sinchronizuojamas.

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

![Šablono susiejimas duomenų integratoriuje](./media/accounts-template-mapping-data-integrator-1.png)

![Sąskaitų šablono susiejimas duomenų integratoriuje](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Susijusios temos

[Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais](products-template-mapping.md)

[Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping.md)

[Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“](sales-quotation-template-mapping.md)

[Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“](sales-order-template-mapping.md)

[Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“](sales-invoice-template-mapping.md)




