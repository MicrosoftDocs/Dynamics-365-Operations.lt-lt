---
title: Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ sąskaitas sinchronizuojant su „Supply Chain Management“.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 0499f604049240a226b4002710817034598b1e66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977718"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Microsoft Dataverse“, skirtą programoms](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ sąskaitas tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management”.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose.  Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„Power Apps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinė užduotis yra naudojami sinchronizuojant „Sales“ sąskaitas su „Supply Chain Management“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis
- **Užduoties pavadinimas projekte:** Sąskaitos – Klientai

Prieš sinchronizuojant sąskaitą / klientą, nereikia atlikti jokių sinchronizavimo užduočių.

## <a name="entity-set"></a>Objektų rinkinys

| Pardavimas    | „Supply Chain Management” |
|----------|------------------------|
| Sąskaitos | Klientai V2           |

## <a name="entity-flow"></a>Objekto srautas

Sąskaitos valdomos programoje „Sales“ ir su „Supply Chain Management“ sinchronizuojamos kaip klientai. Ypatybė **Tvarkoma išoriškai** šiems klientams nustatyta į **Taip**, kad būtų galima sekti „Sales“ klientus. Išrašant sąskaitą faktūrą ši informacija naudojama sąskaitoms faktūros, sinchronizuojamoms su „Sales“, filtruoti.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Stulpelis **Sąskaitos numeris** galimas **Sąskaita** puslapyje. Integracijai palaikyti buvo sukurtas srities ir unikalus raktas. Ryšių su klientais valdymo (CRM) sprendimo srities rakto funkcija gali turėti įtakos klientams, jau naudojantiems **Sąskaitos numeris** stulpelį, bet nenaudojantiems unikalių **Sąskaitos numerio** verčių kiekvienoje sąskaitoje. Šiuo metu integravimo sprendimas nepalaiko šio atvejo.

Sukūrus naują sąskaitą, bet nesant vertei **Sąskaitos numeris**, ji automatiškai sugeneruojama naudojant numeraciją. Vertę sudaro raidės **ACC**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis. Pavyzdys: **ACC-01000-BVRCPS**

Pritaikius integravimo sprendimą „Sales“ naujinimo scenarijus nustato stulpelį **Sąskaitos numeris** „Sales“ esamoms sąskaitoms. Jei lauko **Sąskaitos numeris** verčių nėra, naudojama anksčiau minėta numeracija.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

- **CustomerGroupId** susiejimą reikia atnaujinti į tinkamą „Supply Chain Management“ vertę. Galite nurodyti numatytąją vertę arba ją nustatyti naudodami verčių schemą.

    Numatytoji šablono vertė yra **10**.

- Pridėdami toliau nurodytus susiejimus, galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Supply Chain Management“, skaičių. Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.

    - **SiteId** – vieta būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes. Numatytąją vietą galima paimti iš produkto arba iš kliento užsakymo antraštės.

        Numatytoji šablono vertė yra **1**.

    - **WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes. Numatytąjį sandėlį galima paimti iš produkto arba iš „Supply Chain Management“ kliento užsakymo antraštės.

        Numatytoji šablono vertė yra **13**.

    - **LanguageId** – kalba būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymus. Pagal numatytuosius nustatymus naudojama kalba iš kliento užsakymo antraštės.

        Numatytoji šablono vertė yra **en-us**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

> [!NOTE]
> Stulpeliai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos stulpelius, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių lentelė sinchronizuojama, duomenis.

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri stulpelio informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Susijusios temos


[Potencialaus kliento pavertimas pinigais](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais](contacts-template-mapping-direct.md)

[Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir Tiekimo grandinės valdymo](sales-order-template-mapping-direct-two-ways.md)

[Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)

