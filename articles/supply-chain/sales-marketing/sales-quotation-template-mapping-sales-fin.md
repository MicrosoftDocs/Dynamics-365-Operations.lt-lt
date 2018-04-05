---
title: "„Sales“ pardavimo pasiūlymų antraščių ir eilučių tiesioginis sinchronizavimas su „Finance and Operations“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo pasiūlymo antraštes ir eilutes tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.openlocfilehash: 97536c27dea113cc3c019473f22d1925e7617f8f
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>„Sales“ pardavimo pasiūlymų antraščių ir eilučių tiesioginis sinchronizavimas su „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo pasiūlymo antraštes ir eilutes tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).

## <a name="template-and-tasks"></a>Šablonai ir užduotys

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami tiesiogiai sinchronizuojant „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo pasiūlymai (iš „Sales“ į „Finance and Operations“) – tiesioginis
- **Užduočių pavadinimai projekte Duomenų integravimas:**

    - QuoteHeader
    - QuoteLine

Prieš sinchronizuojant pardavimo pasiūlymų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis
- Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)
- Iš kontaktų į klientus (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)

## <a name="entity-set"></a>Objektų rinkinys

| Pardavimas        | „Finance and Operations”     |
|--------------|----------------------------|
| Pasiūlymai       | CDS pardavimo pasiūlymo antraštė |
| QuoteDetails | CDS pardavimo pasiūlymo eilutės  |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo pasiūlymai kuriami „Sales“ ir sinchronizuojami su „Finance and Operations“.

„Sales“ pardavimo pasiūlymai sinchronizuojami tik jei tenkinamos tolesnės sąlygos.

- Visi produktų pasiūlymai pardavimo pasiūlyme yra tvarkomi išoriškai.
- Spustelėjus **Aktyvinti pasiūlymą**, pardavimo pasiūlymas tampa aktyvus.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Pasiūlymas** , kad būtų galima nuosekliai sekti, ar pardavimo pasiūlymą sudaro tik išoriškai tvarkomi produktai. Jei pardavimo pasiūlymui priskirti tik išoriškai tvarkomi produktai, produktai tvarkomi „Finance and Operations“. Tai padeda užtikrinti, kad nebandysite sinchronizuoti pardavimo pasiūlymo eilučių, kuriose nurodyti „Finance and Operations“ neatpažįstami produktai.

Visi produktų pasiūlymai pardavimo pasiūlyme atnaujinami, įtraukiant pardavimo pasiūlymo antraštės informaciją **Sudaro tik išoriškai tvarkomi produktai**. Šią informacija pateikiama **QuoteDetails** objekto lauke **Pasiūlymą sudaro tik išoriškai tvarkomi produktai**.

Į produkto pasiūlymą gali būti įtraukta nuolaida ir visa tai bus sinchronizuojama su „Finance and Operations“. Antraštės laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo „Finance and Operations“ sąranka. Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas. Dabartinėje versijoje laukai **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** prižiūrimi bei tvarkomi programoje „Finance and Operations“.

„Sales“ versijoje šis sprendimas toliau nurodytus laukus nustato kaip tik skaitomus, nes reikšmės nėra sinchronizuojamos su „Finance and Operations“.

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

- Įsitikinkite, kad „Finance and Operations“ yra **SalesUnitSymbol** būtina verčių schema.
- Įsitikinkite, kad „Sales“ apibrėžti reikiami vienetai.

    Šablono vertė, kurioje yra vertės schema, apibrėžta **oumid.name** į **SalesUnitSymbol**.

- Pasirinktina: galite įtraukti toliau nurodytus susiejimus, norėdami užtikrinti, kad pardavimo pasiūlymo eilutės importuojamos „Finance and Operations“, jei nenurodyta kliento arba produkto numatytoji informacija.

    - **SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes. Numatytosios **SiteId** šablono reikšmės nėra.
    - **WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes. Numatytosios **WarehouseId** šablono reikšmės nėra.

## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

> [!NOTE]
> - Sudėtinga „Finance and Operations“ sąranka valdo laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai**. Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas. Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** tvarko „Finance and Operations“.
> - Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

### <a name="quoteheader"></a>QuoteHeader

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Susijusios temos

[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)


