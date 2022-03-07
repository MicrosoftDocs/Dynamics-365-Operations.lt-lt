---
title: Tiesioginis Tiekimo grandinės valdymo pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ leidimo pardavimo sąskaitų faktūrų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Sales“.
author: Henrikan
ms.date: 10/26/2017
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
ms.openlocfilehash: c2f988b4f170c027444ba7cf54a55e0bd846cedf
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571646"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“

[!include [banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ leidimo pardavimo sąskaitų faktūrų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Sales“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„Power Apps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami tiesiogiai sinchronizuojant „Supply Chain Management“ SF antraštes ir eilutes su „Sales“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo sąskaitų faktūrų (iš „Finance and Operations“ į „Sales“) – tiesioginis
- **Užduočių pavadinimai projekte Duomenų integravimas:**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Prieš sinchronizuojant pardavimo sąskaitų faktūrų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- Produktai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis
- Sąskaitos (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis (jei naudojamas)
- Kontaktai (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis (jei naudojamas)
- Pardavimo užsakymų antraštės ir eilutės (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis

## <a name="entity-set"></a>Objektų rinkinys

| Tiekimo grandinės valdymas                              | Pardavimas          |
|------------------------------------------------------|----------------|
| Išorėje tvarkomų klientų pardavimo SF antraštės | Sąskaitos faktūros       |
| Išorėje tvarkomų klientų pardavimo SF eilutės   | InvoiceDetails |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo sąskaitos faktūros kuriamos Tiekimo grandinės valdyme ir sinchronizuojamos su „Sales“.

> [!NOTE]
> Šiuo metu su pardavimo sąskaitų faktūrų antraštės išlaidomis susijęs mokestis į sinchronizavimo iš Tiekimo grandinės valdymo į „Sales“ procesą nėra įtraukiamas. „Sales“ nepalaikoma mokesčių informacija antraštės lygyje. Tačiau su išlaidomis eilutės lygyje susijęs mokestis yra įtraukiamas į sinchronizavimą.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

- Į objektą **Sąskaita faktūra** įtrauktas ir puslapyje rodomas laukas **Sąskaitos faktūros numeris**.
- Puslapyje **Pardavimo užsakymas** esantis mygtukas **Kurti sąskaitą faktūrą** yra paslėptas, nes sąskaitos faktūros bus kuriamos Tiekimo grandinės valdyme ir sinchronizuojamos su „Sales“. Puslapio **Sąskaita faktūra** redaguoti negalima, nes sąskaitos faktūros bus sinchronizuojamos iš Tiekimo grandinės valdymo.
- Kai susijusi Tiekimo grandinės valdymo sąskaita faktūra baigiama sinchronizuoti su „Sales“, srities **Pardavimo užsakymo būsena** reikšmė automatiškai pakeičiama į **Išrašyta sąskaita faktūra**. Be to, pardavimo užsakymo, iš kurio buvo sukurta sąskaita faktūra, savininkas priskiriamas sąskaitos faktūros savininku. Todėl pardavimo užsakymo savininkas gali peržiūrėti sąskaitą faktūrą.

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
- Įsitikinkite, kad reikiamas **SalesUnitSymbol** skirtas susiejimas yra Tiekimo grandinės valdyme.

    Šablono vertė, kurioje yra vertės schema, apibrėžta **SalesUnitSymbol** su **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

> [!NOTE]
> Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Šablonų susiejimas integruojant duomenis SalesInvoiceHeader.](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Šablonų susiejimas integruojant duomenis SalesInvoiceLine.](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Susijusios temos

[Potencialaus kliento pavertimas pinigais](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Sales“ produktais](products-template-mapping-direct.md)

[Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais](contacts-template-mapping-direct.md)

[Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir Tiekimo grandinės valdymo](sales-order-template-mapping-direct-two-ways.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]