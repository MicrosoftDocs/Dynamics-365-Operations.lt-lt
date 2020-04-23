---
title: Tiesioginis „Sales“ pardavimo pasiūlymų antraščių ir eilučių sinchronizavimas su Tiekimo grandinės valdymu
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ pardavimo pasiūlymų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b6b4384e1b5f712c08de55195a738295a36b75e7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204475"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Tiesioginis „Sales“ pardavimo pasiūlymų antraščių ir eilučių sinchronizavimas su Tiekimo grandinės valdymu

[!include [banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ pardavimo pasiūlymų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Common Data Service“, skirtą programoms](https://docs.microsoft.com/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose. Sprendimo Potencialūs klientai ir grynieji pinigai šablonai, pasiekiami naudojant duomenų integravimo funkciją, įjungia sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo SF duomenų srautą tarp Tiekimo grandinės valdymo ir „Sales“. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Šablonai ir užduotys

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami tiesiogiai sinchronizuojant „Sales“ pardavimo pasiūlymų antraštes ir eilutes su Tiekimo grandinės valdymu.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Pardavimo pasiūlymai (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis
- **Užduočių pavadinimai projekte Duomenų integravimas:**

    - QuoteHeader
    - QuoteLine

Prieš sinchronizuojant pardavimo pasiūlymų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- Produktai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis
- Sąskaitos (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis (jei naudojamas)
- Kontaktai klientams (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis (jei naudojamas)

## <a name="entity-set"></a>Objektų rinkinys

| Pardavimas        | Tiekimo grandinės valdymas     |
|--------------|----------------------------|
| Pasiūlymai       | CDS pardavimo pasiūlymo antraštė |
| QuoteDetails | CDS pardavimo pasiūlymo eilutės  |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo pasiūlymai kuriami sprendime „Sales“ ir sinchronizuojami su Tiekimo grandinės valdymu.

„Sales“ pardavimo pasiūlymai sinchronizuojami tik jei tenkinamos tolesnės sąlygos.

- Visi produktų pasiūlymai pardavimo pasiūlyme yra tvarkomi išoriškai.
- Spustelėjus **Aktyvinti pasiūlymą**, pardavimo pasiūlymas tampa aktyvus.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Pasiūlymas** , kad būtų galima nuosekliai sekti, ar pardavimo pasiūlymą sudaro tik išoriškai tvarkomi produktai. Jei pardavimo pasiūlymui priskirti tik išoriškai tvarkomi produktai, produktai tvarkomi Tiekimo grandinės valdyme. Tai padeda užtikrinti, kad nebandysite sinchronizuoti pardavimo pasiūlymų eilučių, kuriose nurodyti Tiekimo grandinės valdyme neatpažįstami produktai.

Visi produktų pasiūlymai pardavimo pasiūlyme atnaujinami, įtraukiant pardavimo pasiūlymo antraštės informaciją **Sudaro tik išoriškai tvarkomi produktai**. Šią informacija pateikiama **QuoteDetails** objekto lauke **Pasiūlymą sudaro tik išoriškai tvarkomi produktai**.

Į produkto pasiūlymą gali būti įtraukta nuolaida ir visa tai bus sinchronizuojama su Tiekimo grandinės valdymu. Antraštės laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo Tiekimo grandinės valdymo sąranka. Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas. Dabartinėje versijoje laukai **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** prižiūrimi bei tvarkomi naudojant Tiekimo grandinės valdymą.

Sprendime „Sales“ šis sprendimas toliau nurodytus laukus nustato kaip tik skaitomus, nes reikšmės nėra sinchronizuojamos su Tiekimo grandinės valdymu.

- Tik skaitomi pardavimo pasiūlymo antraštės laukai: **Nuolaida %**, **Nuolaida** ir **Transportavimo suma**
- Tik skaitomi produktų pasiūlymo laukai: **Mokestis**

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant pardavimo pasiūlymus, svarbu atnaujinti toliau nurodytus parametrus.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

- Įsitikinkite, kad komandai, kuriai nustatytas vartotojas iš „Sales“ ryšio rinkinio, nustatytos teisės. Jei naudojate demonstracinius duomenis, prieiga paprastai suteikiama vartotojui, bet ne komandai. Jei komanda neturės administratoriaus prieigos, vykdydami Duomenų integravimo projektą gausite klaidos pranešimą, kad trūksta pagrindinės komandos.

    Norėdami nustatyti komandos teises, eikite į **Parametrai** &gt; **Sauga** &gt; **Komandas** ir pasirinkite reikiamą komandą. Pasirinkite **Valdyti vaidmenis**, tada pasirinkite vaidmenį, kuriam suteiktos pageidaujamos teisės, pavyzdžiui, **Sistemos administratorius**.

- Eikite į **Parametrai** &gt; **Administravimas** &gt; **Sistemos parametrai** &gt; **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.

    - Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.
    - Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.

### <a name="setup-in-the-data-integration-project"></a>Sąranka projekte Duomenų integravimas

#### <a name="quoteheader"></a>QuoteHeader

- Įsitikinkite, kad yra reikiamas **Shipto\_country** susiejimas su **DeliveryAddressCountryRegionISOCode**. Vertės schemoje galite nurodyti numatytąją reikšmę, naudojamą tada, jei reikšmės laukas yra tuščias. Tiesiog kairiąją pusę palikite tuščią, o dešiniąją nustatykite į pageidaujamą šalį arba regioną. Tokiu būdu, atliekant užsakymus šalies viduje jums nereikės įvesti šalies arba regiono.

    Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų ir kurioje tuščios vertės laukas lygus vertei **JAV**.

#### <a name="quoteline"></a>QuoteLine

- Įsitikinkite, kad reikiamas **SalesUnitSymbol** skirtas susiejimas yra Tiekimo grandinės valdyme.
- Įsitikinkite, kad „Sales“ apibrėžti reikiami vienetai.

    Šablono vertė, kurioje yra vertės schema, apibrėžta **oumid.name** į **SalesUnitSymbol**.

- Pasirinktina: galite įtraukti toliau nurodytus susiejimus, norėdami užtikrinti, kad pardavimo pasiūlymo eilutės importuojamos į Tiekimo grandinės valdymą, jei nenurodyta kliento arba produkto numatytoji informacija.

    - **SiteId** – vieta būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes. Numatytosios **SiteId** šablono reikšmės nėra.
    - **WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes. Numatytosios **WarehouseId** šablono reikšmės nėra.

## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

> [!NOTE]
> - Laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo sudėtinga Tiekimo grandinės valdymo sąranka. Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas. Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** tvarko Tiekimo grandinės valdymas.
> - Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

### <a name="quoteheader"></a>QuoteHeader

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Susijusios temos

[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)

