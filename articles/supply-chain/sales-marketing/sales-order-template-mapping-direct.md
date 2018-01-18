---
title: "„Finance and Operations“ pardavimo užsakymo antraščių ir eilučių tiesioginis sinchronizavimas su „Sales“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo pardavimo užsakymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>„Finance and Operations“ pardavimo užsakymo antraščių ir eilučių tiesioginis sinchronizavimas su „Sales“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo pardavimo užsakymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ pardavimo užsakymų antraštes ir eilutes su „Sales“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo užsakymai (iš „Finance and Operations“ į „Sales“) – tiesioginis
- **Užduočių pavadinimai projekte Duomenų integravimas:**

    - OrderHeader
    - OrderLine

Prieš sinchronizuojant pardavimo sąskaitų faktūrų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis
- Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)
- Iš kontaktų į klientus (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)

## <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations”  | Pardavimas             |
|-------------------------|-------------------|
| CDS pardavimo užsakymų antraštės | SalesOrders       |
| CDS pardavimo užsakymo eilutės   | SalesOrderDetails |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo užsakymai kuriami sprendime „Finance and Operations“ ir sinchronizuojami su „Sales“.

Naudojant šablono filtrus padedama užtikrinti, kad sinchronizuojant būtų įtraukiami tik aktualūs pardavimo užsakymai:

- Sinchronizuojant bus įtraukiami „Sales“ pardavimo užsakyme nurodyti užsakantis klientas ir sąskaitą faktūrą išrašantis klientas. Sprendime „Finance and Operations“ laukai **OrderingCustomerIsExternallyMaintained** ir **InvoiceCustomerIsExternallyMaintained** naudojami sinchronizavimui duomenų objektuose sekti.
- Sprendime „Finance and Operations“ pardavimo užsakymą reikia patvirtinti. Su „Sales“ sinchronizuojami tik patvirtinti pardavimo užsakymai arba pardavimo užsakymai, kurių apdorojimo būsena aukštesnė, pavyzdžiui, **Išsiųsta** arba **Išrašyta SF**.
- Sukūrus arba modifikavus pardavimo užsakymą, „Finance and Operations“ reikia vykdyti paketinę užduotį **Skaičiuoti bendrąsias pardavimo sumas**. Su „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kuriuose apskaičiuotos bendrosios pardavimo sumos.

> [!NOTE]
> Šiuo metu su pardavimo užsakymo antraštės išlaidomis susijęs mokestis į sinchronizavimo iš „Finance and Operations“ į „Sales“ procesą nėra įtraukiamas. „Sales“ nepalaikoma mokesčių informacija antraštės lygyje. Tačiau su išlaidomis eilutės lygyje susijęs mokestis yra įtraukiamas į sinchronizavimą.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Į objektą **Užsakymas** įtraukiami nauji toliau nurodyti laukai, rodomi puslapyje.

- **Tvarkomas išoriškai** – šią parinktį nustatykite į **Taip**, kai užsakymas yra iš „Finance and Operations“.
- **Apdorojimo būsena** – šiame lauke rodoma „Finance and Operations“ užsakymo apdorojimo būsena. Galimos šios vertės:

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

Parametras **Sudaro tik išoriškai tvarkomi produktai** naudojamas kitose su pardavimo užsakymu susijusiose situacijose (pavyzdžiui, sinchronizuojant iš „Sales“ į „Finance and Operations“), kad būtų nuosekliai sekama, ar pardavimo užsakymą sudaro vien tik Išoriškai tvarkomi produktai. Jei pardavimo užsakymą sudaro tik išoriškai tvarkomi produktai, produktai tvarkomi „Finance and Operations“. Šis parametras padeda užtikrinti, kad nebandysite sinchronizuoti pardavimo užsakymo eilučių, kuriose pateikti „Finance and Operations“ neatpažįstami produktai.

Išoriškai tvarkomuose užsakymuose puslapio **Pardavimo užsakymas** mygtukai **Kurti sąskaitą faktūrą**, **Atšaukti užsakymą**, **Perskaičiuoti**, **Gauti produktų** ir **Peržvelgti adresą** yra paslėpti, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“. Užsakymo puslapio numerio redaguoti negalima, nes pardavimo užsakymo informacija bus sinchronizuojama su „Finance and Operations“.

Pardavimo užsakymo būsena liks **aktyvi**, kad padėtų užtikrinti, jog keitimai iš „Finance and Operations“ galėtų būti perkelti į „Sales“ pardavimo užsakymą. Norėdami valdyti šią veikseną, numatytąją **Būsenos kodas \[Būsena\]** reikšmę projekte Duomenų integravimas nustatykite į **Aktyvu**.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant pardavimo užsakymus, svarbu atnaujinti toliau nurodytus sistemų parametrus.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

- Įsitikinkite, kad komandai, kuriai priskirtas vartotojas iš „Sales“ ryšio rinkinio, nustatytos teisės. Jei naudojate demonstracinius duomenis, prieiga paprastai suteikiama vartotojui, bet ne komandai. Jei komanda taip pat neturės administratoriaus prieigos, vykdydami Duomenų integravimo projektą gausite klaidos pranešimą, kad trūksta pagrindinės komandos.

    Eikite į **Parametrai** > **Sauga** > **Komandos**, pasirinkite reikiamą komandą, pasirinkite **Valdyti vaidmenis** ir pasirinkite vaidmenį, kuriam suteiktos norimos teisės, pvz., **Sistemos administratorius**.

- Eikite į **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.

    - Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.
    - Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.

### <a name="setup-in-finance-and-operations"></a>Sąranka sprendime „Finance and Operations“

Eikite į **Pardavimas ir rinkodara** > **Periodinės užduotys** > **Skaičiuoti bendrąsias pardavimo sumas** ir nustatykite, kad užduotis būtų vykdoma kaip paketinė užduotis. Parinktį **Skaičiuoti bendrąsias pardavimo užsakymų sumas** nustatykite į **Taip**. Šis veiksmas svarbus, nes su „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kuriuose bus apskaičiuotos bendrosios pardavimo sumos. Paketinės užduoties dažnumas turi būti lygus pardavimo užsakymų sinchronizavimo dažnumui.

### <a name="setup-in-the-data-integration-project"></a>Sąranka projekte Duomenų integravimas

#### <a name="salesheader-task"></a>SalesHeader užduotis

- Įsitikinkite, kad yra reikiamas **InvoiceCountryRegionId** susiejimas su **BillingAddress\_Country** ir **DeliveryCountryRegionId** susiejimas su **DeliveryAddress\_Country**.

    Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų.

- Norint sprendime „Sales“ kurti užsakymus, reikalingas Kainoraštis. Dalyje **pricelevelid.name \[Kainoraščio pavadinimas\]** kiekvienos valiutos vertės schemą atnaujinkite į sprendime „Sales“ naudojamą kainoraštį. Kiekvienai valiutai galite naudoti numatytąjį kainoraštį. Taip pat, jei turite kainoraščių keliomis valiutomis, galite naudoti vertės schemą.

    Numatytoji **pricelevelid.name \[Kainoraščio pavadinimas\]** šablono reikšmė yra **„CRM Service USA“ (pavyzdys)**.

#### <a name="salesline-task"></a>SalesLine užduotis

- Įsitikinkite, kad yra reikiamas **DeliveryCountryRegionId** susiejimas su **DeliveryAddress\_Country**.

    Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų.

- Įsitikinkite, kad „Finance and Operations“ yra **SalesUnitSymbol** būtina verčių schema.

    Šablono vertė, kurioje yra vertės schema, apibrėžta **SalesUnitSymbol** su **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

> [!NOTE]
> Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.

### <a name="orderheader"></a>OrderHeader

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Susijusios temos

[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais](products-template-mapping-direct.md)

[Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)




