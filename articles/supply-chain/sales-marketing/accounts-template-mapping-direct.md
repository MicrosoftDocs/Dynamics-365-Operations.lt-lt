---
title: "Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ sąskaitas sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: fb694db32638756328623c186594cf5ba2e7d6b8
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ sąskaitas sinchronizuojant tiesiogiai su „Microsoft Dynamics 365 for Finance and Operations“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose.  Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinė užduotis yra naudojami sinchronizuojant „Sales“ sąskaitas su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis
- **Užduoties pavadinimas projekte:** Sąskaitos – Klientai

Prieš sinchronizuojant sąskaitą / klientą, nereikia atlikti jokių sinchronizavimo užduočių.

## <a name="entity-set"></a>Objektų rinkinys

| Pardavimas    | „Finance and Operations” |
|----------|------------------------|
| Sąskaitos | Klientai V2           |

## <a name="entity-flow"></a>Objekto srautas

Sąskaitos valdomos programoje „Sales“ ir su „Finance and Operations“ sinchronizuojamos kaip klientai. Ypatybė **Tvarkoma išoriškai** šiems klientams nustatyta į **Taip**, kad būtų galima sekti „Sales“ klientus. Išrašant sąskaitą faktūrą ši informacija naudojama sąskaitoms faktūros, sinchronizuojamoms su „Sales“, filtruoti.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Laukas **Sąskaitos numeris** galimas puslapyje **Sąskaita**. Integracijai palaikyti buvo sukurtas srities ir unikalus raktas. Ryšių su klientais valdymo (CRM) sprendimo srities rakto funkcija gali turėti įtakos klientams, jau naudojantiems lauką **Sąskaitos numeris**, bet nenaudojantiems unikalių **Sąskaitos numerio** verčių kiekvienoje sąskaitoje. Šiuo metu integravimo sprendimas nepalaiko šio atvejo.

Sukūrus naują sąskaitą, bet nesant vertei **Sąskaitos numeris**, ji automatiškai sugeneruojama naudojant numeraciją. Vertę sudaro raidės **ACC**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis. Pavyzdys: **ACC-01000-BVRCPS**

Pritaikius integravimo sprendimą „Sales“ naujinimo scenarijus nustato lauką **Sąskaitos numeris** „Sales“ esamoms sąskaitoms. Jei lauko **Sąskaitos numeris** verčių nėra, naudojama anksčiau minėta numeracija.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

- **CustomerGroupId** susiejimą reikia atnaujinti į tinkamą „Finance and Operations“ vertę. Galite nurodyti numatytąją vertę arba ją nustatyti naudodami verčių schemą.

    Numatytoji šablono vertė yra **10**.

- Pridėdami toliau nurodytus susiejimus, galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių. Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.

    - **SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes. Numatytąją vietą galima paimti iš produkto arba iš kliento užsakymo antraštės.

        Numatytoji šablono vertė yra **1**.

    - **WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes. Numatytąjį sandėlį galima paimti iš produkto arba iš „Finance and Operations“ kliento užsakymo antraštės.

        Numatytoji šablono vertė yra **13**.

    - **LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus. Pagal numatytuosius nustatymus naudojama kalba iš kliento užsakymo antraštės.

        Numatytoji šablono vertė yra **en-us**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

> [!NOTE]
> Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Susijusios temos


[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimas su „Sales“](sales-order-template-mapping-direct-two-ways.md)

[Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)


