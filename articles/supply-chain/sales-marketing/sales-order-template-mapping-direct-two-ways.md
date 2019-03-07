---
title: Pardavimo užsakymų tiesioginis sinchronizavimas tarp „Sales“ ir „Finance and Operations“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo užsakymus sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.
author: ChristianRytt
manager: AnnBe
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 985a5a908308bc2268b80e8eef7117fdd6d54af6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "339124"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Finance and Operations“

[!include [banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo užsakymus sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus. Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami pardavimo užsakymus tarp „Finance and Operations“ ir „Sales“ sinchronizuojant tiesiogiai.

- **Šablonų pavadinimai naudojant funkciją Duomenų integravimas:** 

    - Pardavimo užsakymai (iš „Sales“ į „Finance and Operations“) – tiesioginis
    - Pardavimo užsakymai (iš „Finance and Operations“ į „Sales“) – tiesioginis

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

Pardavimo užsakymai sprendime „Sales“ kuriami ir su „Finance and Operations“ sinchronizuojami tada, kai suaktyvinama projekto, paremto pagal šabloną **Pardavimo užsakymas („Sales“ ir „Finance and Operations“) – tiesioginis** funkcija **Vykdyti projektą**. „Sales“ užsakymus aktyvinti ir sinchronizuoti galite tik tada, jei visi **Užsakymo produktai** yra sudaryti iš išoriškai tvarkomų produktų. Todėl produktuose negali būti atliekami rašymai. Suaktyvinus užsakymą, pardavimo užsakymas vartotojo sąsajoje (UI) tampa tik skaitomas. Tuo metu sukuriami pagal „Finance and Operations“ pateiktą informaciją paremti atnaujinimai. Po to, kai pardavimo užsakymo būsena taps **Patvirtinta**, pagal šabloną **Pardavimo užsakymai („Finance and Operations“ ir „Sales“) – tiesioginis** paremtą projektą bus galima panaudoti sinchronizuojant naujinimus arba nustatant „Finance and Operations“ įvykdymo būseną sprendime „Sales“.

„Sales“ užsakymų kurti nereikia. Vietoj to „Finance and Operations“ galite sukurti naujų pardavimo užsakymų. Po to, kai pardavimo užsakymo būsena taps **Patvirtinta**, pardavimo užsakymas bus sinchronizuojamas su „Sales“ kaip aprašyta ankstesnėje pastraipoje.

„Finance and operations“ naudojant šablono filtrus padedama užtikrinti, kad sinchronizuojant būtų įtraukiami tik aktualūs pardavimo užsakymai:

- Norint, kad į sinchronizavimą būtų įtraukti pardavimo užsakyme nurodyti užsakantis klientas ir sąskaitą faktūrą išrašantis klientas, jie abu turi būti pateikiami „Sales“ . Sprendime „Finance and Operations“ laukai **OrderingCustomerIsExternallyMaintained** ir **InvoiceCustomerIsExternallyMaintained** naudojami duomenų objektų pardavimo užsakymams filtruoti.
- Sprendime „Finance and Operations“ pardavimo užsakymą reikia patvirtinti. Su „Sales“ sinchronizuojami tik patvirtinti pardavimo užsakymai arba pardavimo užsakymai, kurių apdorojimo būsena aukštesnė, pavyzdžiui, **Išsiųsta** arba **Išrašyta SF**.
- Sukūrus arba modifikavus pardavimo užsakymą, „Finance and Operations“ reikia vykdyti paketinę užduotį **Skaičiuoti bendrąsias pardavimo sumas**. Su „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kuriuose apskaičiuotos bendrosios pardavimo sumos.

## <a name="freight-tax"></a>Transportavimo mokestis

„Sales“ nepalaikomas mokestis antraštės lygyje, nes mokestis saugomas eilutės lygyje. Norėdama palaikyti mokestį, pavyzdžiui, krovinio tarifą, „Finance and Operations“ antraštės lygyje, sistema mokestį su „Sales“ sinchronizuoja kaip rašomą produktą pavadinimu **Transportavimo mokestis**, kuriam „Finance and Operations“ taip pat numatyta mokesčio suma. Tokiu būdu standartinis kainos skaičiavimas „Sales“ gali būti panaudotas bendrosioms sumoms, net jei „Finance and Operations“ antraštės lygyje yra nurodytas mokestis.

## <a name="discount-calculation-and-rounding"></a>Nuolaidų skaičiavimas ir apvalinimas.

„Sales“ nuolaidos skaičiavimo modelis skiriasi nuo „Finance and Operations“ nuolaidos skaičiavimo modelio. „Finance and Operations“ galutinė nuolaidos suma pardavimo eilutėje gali būti nuolaidos sumų ir nuolaidos procentų kombinacijos suma. Jei ši galutinė nuolaidos suma eilutėje padalinama pagal kiekį, gali būti taikomas apvalinimas. Tačiau apvalinimo taikymas nėra svarstomas, jei suapvalinta vieneto nuolaidos suma sinchronizuojama su „Sales“. Norint padėti užtikrinti, kad visa nuolaidos suma iš „Finance and Operations“ pardavimo eilutės su „Sales“ bus sinchronizuojama tinkamai, reikia sinchronizuoti visą sumą jos neskirstant pagal eilutės kiekį. Todėl „Sales“ **Nuolaidos skaičiavimo būdą** turite apibrėžti kaip **Eilutės elementą**.

„Sales“ pardavimo užsakymo eilutę sinchronizuojant su „Finance and Operations“, naudojama visa eilutės nuolaidos suma. „Finance and Operations“ nėra lauko, kuriame būtų galima saugoti visą nuolaidos eilutės sumą, todėl suma yra padaloma pagal kiekį ir saugoma lauke **Eilutės nuolaida**. Lauko **Pardavimo mokesčiai** pardavimo eilutėje neišsaugomas joks šiame suskirstyme įvykstantis apvalinimas.

### <a name="example"></a>Pavyzdys

**„Sales“ sinchronizavimas su „Finance and Operations”**

- **„Sales“:** kiekis = 3, atskiros eilutės nuolaida = 10,00 USD
- **„Finance and Operations”:** kiekis = 3, eilutės nuolaidos suma = 3,33 USD, pardavimo mokestis = -0,01 USD 

**„Finance and Operations” sinchronizavimas su „Sales“**

- **„Finance and Operations”:** kiekis = 3, eilutės nuolaidos suma = 3,33 USD, pardavimo mokestis = -0,01 USD
- **„Sales“:** kiekis = 3, atskiros eilutės nuolaida = (3 × 3,33 USD) + 0,01 USD = 10,00 USD

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Į objektą **Užsakymas** įtraukiami nauji toliau nurodyti laukai, rodomi puslapyje.

- **Tvarkomas išoriškai** – šią parinktį nustatykite į **Taip**, kai užsakymas yra iš „Finance and Operations“.
- **Apdorojimo būsena** – šiame lauke rodoma „Finance and Operations“ užsakymo apdorojimo būsena. Galimos šios vertės:

    - **Juodraštis** – pradinė būsena, kai „Sales“ sukuriamas pardavimo užsakymas. „Sales“ galima redaguoti tik šią apdorojimo būseną turinčius užsakymus.
    - **Aktyvus** – būsena, kai užsakymas „Sales“ suaktyvinamas naudojant mygtuką **Aktyvinti**.
    - **Pritarta**
    - **Važtaraštis**
    - **SF išrašyta**
    - **Paimta**
    - **Iš dalies paimtas**
    - **Iš dalies supakuotas**
    - **Išsiųsta**
    - **Iš dalies išsiųstas**
    - **Iš dalies išrašyta SF**
    - **Atšaukta**

Nustatymas **Sudaro tik išoriškai tvarkomi produktai** naudojamas aktyvinant užsakymą, kad būtų galima nuosekliai sekti, ar pardavimo užsakymą sudaro tik išoriškai tvarkomi produktai. Jei pardavimo užsakymą sudaro tik išoriškai tvarkomi produktai, produktai tvarkomi „Finance and Operations“. Šis parametras padeda užtikrinti, kad neaktyvinsite nebandysite sinchronizuoti pardavimo užsakymo eilučių, kuriose pateikti „Finance and Operations“ neatpažįstami produktai.

Išoriškai tvarkomuose užsakymuose puslapio **Pardavimo užsakymas** mygtukai **Kurti sąskaitą faktūrą**, **Atšaukti užsakymą**, **Perskaičiuoti**, **Gauti produktų** ir **Peržvelgti adresą** yra paslėpti, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“. Šių užsakymų redaguoti negalima, nes suaktyvinus pardavimo užsakymo informacija bus sinchronizuojama su „Finance and Operations“.

Pardavimo užsakymo būsena liks **aktyvi**, kad padėtų užtikrinti, jog keitimai iš „Finance and Operations“ galėtų būti perkelti į „Sales“ pardavimo užsakymą. Norėdami valdyti šią veikseną, numatytąją **Būsenos kodas \[Būsena\]** reikšmę projekte Duomenų integravimas nustatykite į **Aktyvu**.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant pardavimo užsakymus, svarbu atnaujinti toliau nurodytus sistemų parametrus.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

- Įsitikinkite, kad komandai, kuriai priskirtas vartotojas iš „Sales“ ryšio rinkinio, nustatytos teisės. Jei naudojate demonstracinius duomenis, prieiga paprastai suteikiama vartotojui, bet ne komandai. Jei komanda neturės administratoriaus prieigos, vykdydami Duomenų integravimo projektą gausite klaidos pranešimą, kad trūksta pagrindinės komandos.

    Eikite į **Parametrai** &gt; **Sauga** &gt; **Komandos**, pasirinkite reikiamą komandą, pasirinkite **Valdyti vaidmenis** ir pasirinkite vaidmenį, kuriam suteiktos norimos teisės, pvz., **Sistemos administratorius**.

- Siekdami užtikrinti, kad nuolaidos būtų teisingai skaičiuojamos tiek sprendime „Sales“, tiek sprendime „Finance and Operations“, **nuolaidos skaičiavimo būdą** turite nustatyti kaip **Eilutės elementas**.
- Eikite į **Parametrai** &gt; **Administravimas** &gt; **Sistemos parametrai** &gt; **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.

    - Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.
    - Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.

### <a name="setup-in-finance-and-operations"></a>Sąranka sprendime „Finance and Operations“

- Eikite į **Pardavimas ir rinkodara** &gt; **Periodinės užduotys** &gt; **Skaičiuoti bendrąsias pardavimo sumas** ir nustatykite, kad užduotis būtų vykdoma kaip paketinė užduotis. Parinktį **Skaičiuoti bendrąsias pardavimo užsakymų sumas** nustatykite į **Taip**. Šis veiksmas svarbus, nes su „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kuriuose bus apskaičiuotos bendrosios pardavimo sumos. Paketinės užduoties dažnumas turi būti lygus pardavimo užsakymų sinchronizavimo dažnumui.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Pardavimo užsakymo sąranka („Sales“ į „Finance and Operations“) – tiesioginis projektas Duomenų integravimas

- Įsitikinkite, kad yra reikiamas **Shipto\_country** susiejimas su **DeliveryAddressCountryRegionISOCode**. Verčių schemoje numatytosios vertės lauką galite palikti tuščią, kad atliekant užsakymus šalies viduje nereikėtų vesti šalies pavadinimo. Kairiąją pusę nustatykite į „Tuščia“, o dešiniąją – į pageidaujamą šalį arba regioną.

    Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų ir kurioje „Tuščia“ = JAV.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Pardavimo užsakymo sąranka (iš „Finance and Operations“ į „Sales“) – tiesioginis projektas Duomenų integravimas

#### <a name="salesheader-task"></a>SalesHeader užduotis

- Norint sprendime „Sales“ kurti užsakymus, reikalingas Kainoraštis. Dalyje **pricelevelid.name \[Kainoraščio pavadinimas\]** kiekvienos valiutos vertės schemą atnaujinkite į sprendime „Sales“ naudojamą kainoraštį. Kiekvienai valiutai galite naudoti numatytąjį kainoraštį. Taip pat, jei turite kainoraščių keliomis valiutomis, galite naudoti vertės schemą.

    Numatytoji **pricelevelid.name \[Kainoraščio pavadinimas\]** šablono reikšmė yra **„CRM Service USA“ (pavyzdys)**.

#### <a name="salesline-task"></a>SalesLine užduotis

- Įsitikinkite, kad „Finance and Operations“ yra **SalesUnitSymbol** būtina verčių schema.
- Įsitikinkite, kad „Sales“ apibrėžti reikiami vienetai.

    Šablono vertė, kurioje yra vertės schema, apibrėžta **SalesUnitSymbol** į **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

> [!NOTE]
> Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“ arba „Finance and Operations“ sinchronizavimą su „Sales“.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Pardavimo užsakymai (iš „Finance and Operations“ į „Sales“) – tiesioginis: OrderHeader

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Pardavimo užsakymai (iš „Finance and Operations“ į „Sales“) – tiesioginis: OrderLine

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Pardavimo užsakymai (iš „Sales“ į „Finance and Operations“) – tiesioginis: OrderHeader

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Pardavimo užsakymai (iš „Sales“ į „Finance and Operations“) – tiesioginis: OrderLine

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Susijusios temos

[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)
