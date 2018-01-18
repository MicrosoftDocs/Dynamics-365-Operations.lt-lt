---
title: "Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo pardavimo sąskaitos faktūros antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e9d7e756c56932372ed931620016973c794fb3fc
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo pardavimo sąskaitos faktūros antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ pardavimo sąskaitų faktūrų antraštes ir eilutes su „Sales“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo sąskaitų faktūrų (iš „Finance and Operations“ į „Sales“) – tiesioginis
- **Užduočių pavadinimai projekte Duomenų integravimas:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Prieš sinchronizuojant pardavimo sąskaitų faktūrų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis
- Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)
- Kontaktai (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)
- Pardavimo užsakymo antraštė ir eilutės (iš „Finance and Operations“ į „Sales“) – tiesioginis

## <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations”                               | Pardavimas          |
|------------------------------------------------------|----------------|
| Išorėje tvarkomų klientų pardavimo SF antraštės | Sąskaitos faktūros       |
| Išorėje tvarkomų klientų pardavimo SF eilutės   | InvoiceDetails |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo sąskaitos faktūros kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“.

> [!NOTE]
> Šiuo metu su pardavimo sąskaitų faktūrų antraštės išlaidomis susijęs mokestis į sinchronizavimo iš „Finance and Operations“ į „Sales“ procesą nėra įtraukiamas. „Sales“ nepalaikoma mokesčių informacija antraštės lygyje. Tačiau su išlaidomis eilutės lygyje susijęs mokestis yra įtraukiamas į sinchronizavimą.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

- Į objektą **Sąskaita faktūra** įtrauktas ir puslapyje rodomas laukas **Sąskaitos faktūros numeris**.
- Puslapyje **Pardavimo užsakymas** esantis mygtukas **Kurti sąskaitą faktūrą** yra paslėptas, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“. Puslapio **Sąskaita faktūra** redaguoti negalima, nes sąskaitos faktūros bus sinchronizuojamos iš „Finance and Operations“.
- Kai susijusi „Finance and Operations“ sąskaita faktūra baigiama sinchronizuoti su „Sales“, srities **Pardavimo užsakymo būsena** vertė automatiškai pakeičiama į **Išrašyta sąskaita faktūra**. Be to, pardavimo užsakymo, iš kurio buvo sukurta sąskaita faktūra, savininkas priskiriamas sąskaitos faktūros savininku. Todėl pardavimo užsakymo savininkas gali peržiūrėti sąskaitą faktūrą.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant pardavimo sąskaitas faktūras, svarbu atnaujinti toliau nurodytus sistemų parametrus.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

Eikite į **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.

- Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.
- Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.

### <a name="setup-in-the-data-integration-project"></a>Sąranka projekte Duomenų integravimas

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader užduotis

- Įsitikinkite, kad yra reikiamas **InvoiceCountryRegionId** susiejimas su **BillingAddress\_Country**.

    Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų.

- Norint Sprendime „Sales“ kurti sąskaitas faktūras, reikalingas Kainoraštis. Dalyje **pricelevelid.name \[Kainoraščio pavadinimas\]** kiekvienos valiutos vertės schemą atnaujinkite į sprendime „Sales“ naudojamą kainoraštį. Kiekvienai valiutai galite naudoti numatytąjį kainoraštį. Taip pat, jei turite kainoraščių keliomis valiutomis, galite naudoti vertės schemą.

    Dalies **pricelevelid.name \[kainų sąrašo pavadinimas\]** šablono vertė yra vertės schema, pagrįsta USD valiuta = „CRM Service USA“ (pavyzdys).  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine užduotis

- Įsitikinkite, kad yra reikiamas **Matavimo vieneto** siejimas.
- Įsitikinkite, kad „Finance and Operations“ yra **SalesUnitSymbol** būtina verčių schema.

    Šablono vertė, kurioje yra vertės schema, apibrėžta **SalesUnitSymbol** su **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

> [!NOTE]
> Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Susijusios temos

[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais](products-template-mapping-direct.md)

[Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimas su „Sales“](sales-order-template-mapping-direct.md)







