---
title: Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir Tiekimo grandinės valdymo
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ pardavimo užsakymus tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.
author: ChristianRytt
manager: tfehr
ms.date: 05/09/2019
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
ms.openlocfilehash: ddc6159480d1ff9fb823dbd95465c991ae51f9c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974990"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir Tiekimo grandinės valdymo

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ pardavimo užsakymus tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose. Sprendimo Potencialūs klientai ir grynieji pinigai šablonai, pasiekiami naudojant duomenų integravimo funkciją, įjungia sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo SF duomenų srautą tarp Tiekimo grandinės valdymo ir „Sales“. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„Power Apps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami pardavimo užsakymus tarp „Sales“ ir Tiekimo grandinės valdymo sinchronizuojant tiesiogiai.

- **Šablonų pavadinimai naudojant funkciją Duomenų integravimas:** 

    - Pardavimo užsakymai (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis
    - Pardavimo užsakymai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis

- **Užduočių pavadinimai projekte Duomenų integravimas:**

    - OrderHeader
    - OrderLine

Prieš sinchronizuojant pardavimo sąskaitų faktūrų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- Produktai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis
- Sąskaitos (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis (jei naudojamas)
- Kontaktai klientams (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis (jei naudojamas)

## <a name="entity-set"></a>Objektų rinkinys

| Tiekimo grandinės valdymas  | Pardavimas             |
|-------------------------|-------------------|
| „Dataverse” pardavimo užsakymo antraštės | SalesOrders       |
| „Dataverse” pardavimo užsakymo eilutės   | SalesOrderDetails |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo užsakymai sprendime „Sales“ kuriami ir su Tiekimo grandinės valdymu sinchronizuojami tada, kai suaktyvinama projekto, parengto pagal šabloną **Pardavimo užsakymas (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis**, funkcija **Vykdyti projektą**. „Sales“ užsakymus aktyvinti ir sinchronizuoti galite tik tada, jei visi **Užsakymo produktai** yra sudaryti iš išoriškai tvarkomų produktų. Todėl produktuose negali būti atliekami rašymai. Suaktyvinus užsakymą, pardavimo užsakymas vartotojo sąsajoje (UI) tampa tik skaitomas. Tuo metu naujinimai kuriami naudojant Tiekimo grandinės valdymą. Po to, kai pardavimo užsakymo būsena taps **Patvirtinta**, pagal šabloną **Pardavimo užsakymai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis** parengtą projektą bus galima panaudoti sinchronizuojant naujinimus arba iš Tiekimo grandinės valdymo į „Sales“ įvykdymo būseną.

„Sales“ užsakymų kurti nereikia. Vietoj to Tiekimo grandinės valdyme galite sukurti naujų pardavimo užsakymų. Po to, kai pardavimo užsakymo būsena taps **Patvirtinta**, pardavimo užsakymas bus sinchronizuojamas su „Sales“ kaip aprašyta ankstesnėje pastraipoje.

Tiekimo grandinės valdyme naudojant šablono filtrus padedama užtikrinti, kad sinchronizuojant būtų įtraukiami tik aktualūs pardavimo užsakymai.

- Norint, kad į sinchronizavimą būtų įtraukti pardavimo užsakyme nurodyti užsakantis klientas ir sąskaitą faktūrą išrašantis klientas, jie abu turi būti pateikiami „Sales“ . „Supply Chain Management” **OrderingCustomerIsExternallyMaintained** ir **InvoiceCustomerIsExternallyMaintained** stulpeliai naudojami išfiltruoti pardavimų užsakymus iš duomenų lentelių.
- Tiekimo grandinės valdyme pardavimo užsakymą reikia patvirtinti. Su „Sales“ sinchronizuojami tik patvirtinti pardavimo užsakymai arba pardavimo užsakymai, kurių apdorojimo būsena aukštesnė, pavyzdžiui, **Išsiųsta** arba **Išrašyta SF**.
- Sukūrus arba modifikavus pardavimo užsakymą, Tiekimo grandinės valdyme reikia vykdyti paketinę užduotį **Skaičiuoti bendrąsias pardavimo sumas**. Su „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kuriuose apskaičiuotos bendrosios pardavimo sumos.

## <a name="freight-tax"></a>Transportavimo mokestis

„Sales“ nepalaikomas mokestis antraštės lygyje, nes mokestis saugomas eilutės lygyje. Norėdama palaikyti mokestį, pavyzdžiui, krovinio tarifą, Tiekimo grandinės valdymo antraštės lygiu, sistema mokestį su „Sales“ sinchronizuoja kaip rašomą produktą pavadinimu **Transportavimo mokestis**, kuriam Tiekimo grandinės valdyme taip pat numatyta mokesčio suma. Tokiu būdu standartinis kainos skaičiavimas „Sales“ gali būti panaudotas bendrosioms sumoms, net jei Tiekimo grandinės valdymo antraštės lygiu yra nurodytas mokestis.

## <a name="discount-calculation-and-rounding"></a>Nuolaidų skaičiavimas ir apvalinimas.

„Sales“ nuolaidos skaičiavimo modelis skiriasi nuo Tiekimo grandinės valdymo nuolaidos skaičiavimo modelio. Tiekimo grandinės valdyme galutinė nuolaidos suma pardavimo eilutėje gali būti nuolaidos sumų ir nuolaidos procentų kombinacijos suma. Jei ši galutinė nuolaidos suma eilutėje padalinama pagal kiekį, gali būti taikomas apvalinimas. Tačiau apvalinimo taikymas nėra svarstomas, jei suapvalinta vieneto nuolaidos suma sinchronizuojama su „Sales“. Norint padėti užtikrinti, kad visa nuolaidos suma iš Tiekimo grandinės valdymo pardavimo eilutės su „Sales“ bus sinchronizuojama tinkamai, reikia sinchronizuoti visą sumą jos neskirstant pagal eilutės kiekį. Todėl „Sales“ **Nuolaidos skaičiavimo būdą** turite apibrėžti kaip **Eilutės elementą**.

„Sales“ pardavimo užsakymo eilutę sinchronizuojant su Tiekimo grandinės valdymu, naudojama visa eilutės nuolaidos suma. Tiekimo grandinės valdyme nėra lauko, kuriame būtų galima saugoti visą nuolaidos eilutės sumą, todėl suma yra suskirstoma pagal kiekį ir saugoma lauke **Eilutės nuolaida**. Lauko **Pardavimo mokesčiai** pardavimo eilutėje neišsaugomas joks šiame suskirstyme įvykstantis apvalinimas.

### <a name="example"></a>Pavyzdys

**Sinchronizavimas iš „Sales“ į Tiekimo grandinės valdymą**

- **„Sales“:** kiekis = 3, atskiros eilutės nuolaida = 10,00 USD
- **Tiekimo grandinės valdymas:** kiekis = 3, eilutės nuolaidos suma = 3,33 USD, pardavimo mokestis = -0,01 USD 

**Sinchronizavimas iš Tiekimo grandinės valdymo į „Sales“**

- **Tiekimo grandinės valdymas:** kiekis = 3, eilutės nuolaidos suma = 3,33 USD, pardavimo mokestis = -0,01 USD
- **„Sales“:** kiekis = 3, atskiros eilutės nuolaida = (3 × 3,33 USD) + 0,01 USD = 10,00 USD

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Nauji stulpeliai pridėti į **Užsakymas** lentelę ir pasirodo puslapyje:

- **Tvarkomas išoriškai** – šioje parinktyje nustatykite **Taip**, kai užsakymas yra iš Tiekimo grandinės valdymo.
- **Apdorojimo būsena** – šiame stulpelyje rodoma „Supply Chain Management” užsakymo apdorojimo būsena. Galimos šios vertės:

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

Nustatymas **Sudaro tik išoriškai tvarkomi produktai** naudojamas aktyvinant užsakymą, kad būtų galima nuosekliai sekti, ar pardavimo užsakymą sudaro tik išoriškai tvarkomi produktai. Jei pardavimo užsakymą sudaro tik išoriškai tvarkomi produktai, produktai tvarkomi Tiekimo grandinės valdyme. Šis parametras padeda užtikrinti, kad neaktyvinsite ir nebandysite sinchronizuoti pardavimo užsakymo eilučių, kuriose pateikti Tiekimo grandinės valdyme neatpažįstami produktai.

Išoriškai tvarkomuose užsakymuose puslapio **Pardavimo užsakymas** mygtukai **Kurti sąskaitą faktūrą**, **Atšaukti užsakymą**, **Perskaičiuoti**, **Gauti produktų** ir **Peržvelgti adresą** yra paslėpti, nes sąskaitos faktūros bus kuriamos Tiekimo grandinės valdyme ir sinchronizuojamos su „Sales“. Šių užsakymų redaguoti negalima, nes suaktyvinus pardavimo užsakymų informacija bus sinchronizuojama iš Tiekimo grandinės valdymo.

Pardavimo užsakymo būsena liks **Aktyvi**, kad padėtų užtikrinti, jog keitimai iš Tiekimo grandinės valdymo galėtų būti perkelti į „Sales“ pardavimo užsakymą. Norėdami valdyti šią veikseną, numatytąją **Būsenos kodas \[Būsena\]** reikšmę projekte Duomenų integravimas nustatykite į **Aktyvu**.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant pardavimo užsakymus, svarbu atnaujinti toliau nurodytus sistemų parametrus.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

- Įsitikinkite, kad komandai, kuriai priskirtas vartotojas iš „Sales“ ryšio rinkinio, nustatytos teisės. Jei naudojate demonstracinius duomenis, prieiga paprastai suteikiama vartotojui, bet ne komandai. Jei komanda neturės administratoriaus prieigos, vykdydami Duomenų integravimo projektą gausite klaidos pranešimą, kad trūksta pagrindinės komandos.

    Eikite į **Parametrai** &gt; **Sauga** &gt; **Komandos**, pasirinkite reikiamą komandą, pasirinkite **Valdyti vaidmenis** ir pasirinkite vaidmenį, kuriam suteiktos norimos teisės, pvz., **Sistemos administratorius**.

- Siekdami užtikrinti, kad nuolaidos būtų tinkamai skaičiuojamos tiek sprendime „Sales“, tiek Tiekimo grandinės valdyme, **Nuolaidos skaičiavimo būdą** turite nustatyti kaip **Eilutės elementas**.
- Eikite į **Parametrai** &gt; **Administravimas** &gt; **Sistemos parametrai** &gt; **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.

    - Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.
    - Stulpelis **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.

### <a name="setup-in-supply-chain-management"></a>„Supply Chain Management“ nustatymas

- Eikite į **Pardavimas ir rinkodara** &gt; **Periodinės užduotys** &gt; **Skaičiuoti bendrąsias pardavimo sumas** ir nustatykite, kad užduotis būtų vykdoma kaip paketinė užduotis. Parinktį **Skaičiuoti bendrąsias pardavimo užsakymų sumas** nustatykite į **Taip**. Šis veiksmas svarbus, nes su „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kuriuose bus apskaičiuotos bendrosios pardavimo sumos. Paketinės užduoties dažnumas turi būti lygus pardavimo užsakymų sinchronizavimo dažnumui.

Jei taip pat naudojate darbo užsakymo integravimą, turite nustatyti pardavimo kilmę. Pardavimo kilmė naudojama siekiant atskirti sukurtus „Supply Chain Management“ pardavimo užsakymus nuo „Field Service“ darbo užsakymų. Kai pardavimo užsakymo pardavimo kilmės tipas yra **Darbo užsakymo integravimas**, laukas **Išorinė darbo užsakymo būsena** rodomas pardavimo užsakymo antraštėje. Be to, pardavimo kilmė užtikrina, kad pardavimo užsakymai, sukurti pagal „Field Service“ darbo užsakymus, bus pašalinami naudojant filtrą, kai pardavimo užsakymai sinchronizuojami iš Tiekimo grandinės valdymo į „Field Service“.

1. Pasirinkite **Pardavimas ir rinkodara** \> **Sąranka** \> **Pardavimo užsakymai** \> **Pardavimo kilmė**.
2. Norėdami kurti naują pardavimo kilmę, pasirinkite **Nauja**.
3. Stulpelyje **Pardavimo kilmė** įveskite pardavimo kilmės pavadinimą, pavyzdžiui, **SalesOrder**.
4. Stulpelyje **Aprašas** įveskite aprašą, pvz., **Pardavimo užsakymas iš pardavimų**.
5. Pasirinkite žymės langelį **Kilmės tipo priskyrimas**.
6. Nustatykite stulpelio **Pardavimo kilmės tipas** vertę į **Pardavimo užsakymo integravimas**.
7. Pasirinkite **Įrašyti**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Pardavimo užsakymų sąranka (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis projektas Duomenų integravimas

- Įsitikinkite, kad yra reikiamas **Shipto\_country** susiejimas su **DeliveryAddressCountryRegionISOCode**. Verčių schemoje numatytosios vertės lauką galite palikti tuščią, kad atliekant užsakymus šalies viduje nereikėtų vesti šalies pavadinimo. Kairiąją pusę nustatykite į „Tuščia“, o dešiniąją – į pageidaujamą šalį arba regioną.

    Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų ir kurioje „Tuščia“ = JAV.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Pardavimo užsakymų sąranka (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis projektas Duomenų integravimas

#### <a name="salesheader-task"></a>SalesHeader užduotis

- Norint sprendime „Sales“ kurti užsakymus, reikalingas Kainoraštis. Dalyje **pricelevelid.name \[Kainoraščio pavadinimas\]** kiekvienos valiutos vertės schemą atnaujinkite į sprendime „Sales“ naudojamą kainoraštį. Kiekvienai valiutai galite naudoti numatytąjį kainoraštį. Taip pat, jei turite kainoraščių keliomis valiutomis, galite naudoti vertės schemą.

    Numatytoji **pricelevelid.name \[Kainoraščio pavadinimas\]** šablono reikšmė yra **„CRM Service USA“ (pavyzdys)**.

#### <a name="salesline-task"></a>SalesLine užduotis

- Įsitikinkite, kad reikiamas **SalesUnitSymbol** skirtas susiejimas yra Tiekimo grandinės valdyme.
- Įsitikinkite, kad „Sales“ apibrėžti reikiami vienetai.

    Šablono vertė, kurioje yra vertės schema, apibrėžta **SalesUnitSymbol** į **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

> [!NOTE]
> Stulpeliai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos stulpelius, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių lentelė sinchronizuojama, duomenis.

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.

> [!NOTE]
> Susiejime rodoma, kuri stulpelio informacija bus sinchronizuota iš pardavimų į „Supply Chain Management” ar iš „Supply Chain Management” į pardavimus.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Pardavimo užsakymai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis: OrderHeader

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Pardavimo užsakymai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis: OrderLine

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Pardavimo užsakymai (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis: OrderHeader

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Pardavimo užsakymai (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis: OrderLine

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Susijusios temos

[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)
