---
title: Tiesioginis „Sales“ pardavimo pasiūlymų antraščių ir eilučių sinchronizavimas su „Supply Chain Management”
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ pardavimo pasiūlymų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.
author: Henrikan
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 362b6c290b1784d05e42ecb650911cc51aa8478a
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061989"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a>Tiesioginis „Sales“ pardavimo pasiūlymų antraščių ir eilučių sinchronizavimas su „Supply Chain Management”

[!include [banner](../includes/banner.md)]



Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ pardavimo pasiūlymų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Microsoft Dataverse“, skirtą programoms](/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose. Sprendimo Potencialūs klientai ir grynieji pinigai šablonai, pasiekiami naudojant duomenų integravimo funkciją, įjungia sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo SF duomenų srautą tarp „Supply Chain Management” ir „Sales“. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Šablonai ir užduotys

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami tiesiogiai sinchronizuojant „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Supply Chain Management”.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Pardavimo pasiūlymai (iš „Sales“ į „Supply Chain Management”) – tiesioginis
- **Užduočių pavadinimai projekte Duomenų integravimas:**

    - QuoteHeader
    - QuoteLine

Prieš sinchronizuojant pardavimo pasiūlymų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- Produktai (iš „Supply Chain Management” į „Sales“) – tiesioginis
- Sąskaitos (iš „Sales“ į „Supply Chain Management”) – tiesioginis (jei naudojamas)
- Kontaktai klientams (iš „Sales“ į „Supply Chain Management”) – tiesioginis (jei naudojamas)

## <a name="entity-set"></a>Objektų rinkinys

| Pardavimas        | „Supply Chain Management”     |
|--------------|----------------------------|
| Pasiūlymai       | „Dataverse” pardavimo kainos pasiūlymo antraštė |
| QuoteDetails | „Dataverse” pardavimo kainos pasiūlymų eilutės  |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo pasiūlymai kuriami sprendime „Sales“ ir sinchronizuojami su „Supply Chain Management”.

„Sales“ pardavimo pasiūlymai sinchronizuojami tik jei tenkinamos tolesnės sąlygos.

- Visi produktų pasiūlymai pardavimo pasiūlyme yra tvarkomi išoriškai.
- Spustelėjus **Aktyvinti pasiūlymą**, pardavimo pasiūlymas tampa aktyvus.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Pasiūlymas** , kad būtų galima nuosekliai sekti, ar pardavimo pasiūlymą sudaro tik išoriškai tvarkomi produktai. Jei pardavimo pasiūlymui priskirti tik išoriškai tvarkomi produktai, produktai tvarkomi „Supply Chain Management”. Tai padeda užtikrinti, kad nebandysite sinchronizuoti pardavimo pasiūlymų eilučių, kuriose nurodyti „Supply Chain Management” neatpažįstami produktai.

Visi produktų pasiūlymai pardavimo pasiūlyme atnaujinami, įtraukiant pardavimo pasiūlymo antraštės informaciją **Sudaro tik išoriškai tvarkomi produktai**. Šią informacija pateikiama **QuoteDetails** objekto lauke **Pasiūlymą sudaro tik išoriškai tvarkomi produktai**.

Į produkto pasiūlymą gali būti įtraukta nuolaida ir visa tai bus sinchronizuojama su „Supply Chain Management”. Antraštės laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo „Supply Chain Management” sąranka. Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas. Dabartinėje versijoje laukai **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** prižiūrimi bei tvarkomi naudojant „Supply Chain Management”.

Sprendime „Sales“ šis sprendimas toliau nurodytus laukus nustato kaip tik skaitomus, nes reikšmės nėra sinchronizuojamos su „Supply Chain Management”.

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

- Įsitikinkite, kad reikiamas **SalesUnitSymbol** skirtas susiejimas yra „Supply Chain Management”.
- Įsitikinkite, kad „Sales“ apibrėžti reikiami vienetai.

    Šablono vertė, kurioje yra vertės schema, apibrėžta **oumid.name** į **SalesUnitSymbol**.

- Pasirinktina: galite įtraukti toliau nurodytus susiejimus, norėdami užtikrinti, kad pardavimo pasiūlymo eilutės importuojamos į „Supply Chain Management”, jei nenurodyta kliento arba produkto numatytoji informacija.

    - **SiteId** – vieta būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes. Numatytosios **SiteId** šablono reikšmės nėra.
    - **WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes. Numatytosios **WarehouseId** šablono reikšmės nėra.

## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

> [!NOTE]
> - Laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo sudėtinga „Supply Chain Management” sąranka. Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas. Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** tvarko „Supply Chain Management”.
> - Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

### <a name="quoteheader"></a>QuoteHeader

![Susieti šabloną duomenų integratoriuje, QuoteHeader.](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Susieti šabloną duomenų integratoriuje, QuoteLine.](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Susijusios temos

[Potencialaus kliento pavertimas pinigais](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]