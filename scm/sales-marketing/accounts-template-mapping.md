---
title: "Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ sąskaitas sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimo)."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: b497f078d9786a5c7630e924da6bb04cad37f5e9
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

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

- **CustomerGroupId** reikia atnaujinti į tinkamą „Finance and Operations“ vertę. Galite nurodyti numatytąją vertę arba ją nustatyti naudodami verčių schemą. Numatytoji šablono vertė yra **10**.
- „Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas. Norėdami išvengti sinchronizavimo klaidų, galite nurodyti numatytąją vertę. Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.

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

[Sinchronizuoti pardavimo pasiūlymų antraštes ir eilutes „Sales“ su „Finance and Operations“](sales-quotation-template-mapping.md)




