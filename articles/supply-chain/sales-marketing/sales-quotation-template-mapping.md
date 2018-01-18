---
title: "Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“"
description: "Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo pasiūlymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimu."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
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
ms.openlocfilehash: c8cfc484eed02423dbf0c7caaf8ac2337b6ac38d
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration). 

Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ („Sales“) pardavimo pasiūlymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimu („Finance and Operations“). 

## <a name="template-and-tasks"></a>Šablonai ir užduotys

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“.

- **Šablono pavadinimas:** pardavimo pasiūlymai (iš „Sales“ į „Finance and Operations“)
- **Užduočių pavadinimai projekte**

    - QuoteHeader
    - QuoteLine

Prieš sinchronizuojant pardavimo pasiūlymų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.

- Produktai (iš „Finance and Operations“ į „Sales“)
- Sąskaitos (iš „Sales“ į „Finance and Operations“) (jei naudojama)
- Iš kontaktų į klientus (iš „Sales“ į „Finance and Operations“) (jei naudojama)

## <a name="entity-set"></a>Objektų rinkinys

| Pardavimas        | CDS           | „Finance and Operations”    |
|--------------|---------------|---------------------------|
| Pasiūlymai       | Pasiūlymas     | Pardavimo pasiūlymo antraštės   |
| QuoteDetails | QuotationLine | CDS pardavimo pasiūlymo eilutės |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo pasiūlymai kuriami „Sales“ ir sinchronizuojami su „Finance and Operations“.

„Sales“ pardavimo pasiūlymai sinchronizuojami tik jei tenkinamos tolesnės sąlygos.

- Visi produktai pardavimo pasiūlymo eilutėse yra tvarkomi išoriškai.
- Pardavimo pasiūlymas yra aktyvus arba suaktyvintas.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą Pasiūlymas, kad būtų galima nuosekliai sekti, ar pardavimo pasiūlymą sudaro tik išoriškai tvarkomi produktai. Jei pardavimo pasiūlymui priskirti tik išoriškai tvarkomi produktai, produktai tvarkomi „Finance and Operations“. Tai padeda užtikrinti, kad nebandysite pardavimo pasiūlymo eilučių sinchronizuoti su produktais, kurių „Finance and Operations“ neatpažįsta.

Visi pasiūlymo produktai ir eilutės atnaujinami, įtraukiant pasiūlymo antraštės informaciją **Sudaro tik išoriškai tvarkomi produktai**. Šią informaciją galima rasti pasiūlymo eilutės objekto lauke **Pasiūlymą sudaro tik išoriškai tvarkomi produktai**.

Sudėtinga „Finance and Operations“ sąranka valdo laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai**. Ši sąranka šiuo metu nepalaiko integravimo susiejimo. Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo bei tvarko „Finance and Operations“.

„Sales“ versijoje šis sprendimas toliau nurodytus laukus nustato kaip tik skaitomus, nes reikšmės nėra sinchronizuojamos su „Finance and Operations“.

- **Tik skaitomi pardavimo pasiūlymo antraštės laukai:** Nuolaida %, Nuolaida, Transportavimo suma
- **Tik skaitomi pardavimo pasiūlymo eilučių laukai:** Mokesčiai

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant pardavimo užsakymus, svarbu sistemas atnaujinti tolesniu parametru.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

- Eikite į **Parametrai** &gt; **Administravimas** &gt; **Sistemos parametrai** &gt; **Pardavimas** ir įsitikinkite, kad laukas **Nuolaidos skaičiavimo būdas** nustatytas kaip **Taikoma vienetui**. Šis parametras padeda užtikrinti, kad „Sales“ eilutės prekės nuolaida atitinka „Finance and Operations“ parametrą. Priešingu atveju „Finance and Operations“ nuolaida bus neteisinga, nes „Finance and Operations“ nuolaidą skaičiuos kaip vienetui taikomą nuolaidą, net jei „Sales“ nustatyta eilutei taikoma nuolaida.

### <a name="setup-in-finance-and-operations"></a>Sąranka sprendime „Finance and Operations“

- Eikite į **Gautinos sumos** &gt; **Sąranka** &gt; **Gautinų sumų parametrai**. Skirtuke **Numeracija** pasirinkite pardavimo pasiūlymų numeraciją ir tada spustelėkite **Peržiūrėti informaciją**. Tada dalyje **Bendroji Sąranka** nustatykite lauką **Neautomatinis** į parinktį **Taip**.
- Eikite į **Gautinos sumos** &gt; **Sąranka** &gt; **Gautinų sumų parametrai**. Tada skirtuke **Siuntos** nustatykite lauką **Pristatymo datos valdymas** į parinktį **Nėra**. Šis parametras padeda užtikrinti sėkmingą pardavimo pasiūlymų sinchronizavimą.

### <a name="setup-in-the-data-integration-project"></a>Sąranka projekte Duomenų integravimas

#### <a name="quoteheader"></a>QuoteHeader

- „Finance and Operations“ laukas **Pageidaujama pristatymo data** yra būtinas, ir sinchronizavimas nepavyksta, jei šis laukas bus tuščias. Siekiant išvengti tokios problemos, jei laukas paliekamas tuščias, numatytoji data paimama iš čia: **Šaltinis &gt;CD**. Data turėtų būti atnaujinta į pageidaujamą reikšmę. Šiuo metu negalima įvesti tokios reikšmės kaip **Šiandien**, kad ji nurodytų šios dienos datą. Turite įvesti konkrečią datą. Numatytoji šablono lauko **Pageidaujama pristatymo data** reikšmė yra **2020-01-01**.
- „Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas. Norėdami išvengti sinchronizavimo klaidų, galite nurodyti numatytąją reikšmę, kuri bus naudojama, jei „Sales“ laukas paliekamas tuščias. Be to, ši numatytoji reikšmė yra naudinga, nes jums nereikia patiems įvesti reikšmės vietinio adreso lauke **Šalies regionas**. Numatytosios **DeliveryAddressCountryRegionISOCode** šablono reikšmės nėra.
- Atnaujinkite **CDS organizacijos ID** susiejimą dalyje **Šaltinis &gt; CDS**, kad jis atitiktų **CDS organizaciją** objekte Organizacija.

    - Numatytoji **Organization_OrganizationId** šablono reikšmė yra **ORG001**.
    - Numatytoji **Account_Organization_OrganizationId** šablono reikšmė yra **ORG001**.
    - Numatytoji **InvoiceAccount_OrganizationId** šablono reikšmė yra **ORG001**.

#### <a name="quoteline"></a>QuoteLine

- Atnaujinkite **CDS organizacijos ID** susiejimą dalyje **Šaltinis &gt; CDS**, kad jis atitiktų **CDS organizaciją** objekte Organizacija.

    - Numatytoji **Organization_OrganizationId** šablono reikšmė yra **ORG001**.
    - Numatytoji **Product_Organization_Organization_OrganizationId** šablono reikšmė yra **ORG001**.
    - Numatytoji **Quotation_Organization_Organization_OrganizationId** šablono reikšmė yra **ORG001**.

- „Finance and Operations“ laukas **Pageidaujama pristatymo data** yra būtinas, ir sinchronizavimas nepavyksta, jei šis laukas bus tuščias. Siekiant išvengti tokios problemos, jei laukas paliekamas tuščias, numatytoji data paimama iš čia: **Šaltinis &gt;CD**. Data turėtų būti atnaujinta į pageidaujamą reikšmę. Šiuo metu negalima įvesti tokios reikšmės kaip **Šiandien**, kad ji nurodytų šios dienos datą. Turite įvesti konkrečią datą. Numatytoji šablono lauko **Pageidaujama pristatymo data** reikšmė yra **2020-01-01**.
- Iš dalies **CDS &gt; Paskirties vieta** galite įtraukti toliau nurodytus susiejimus, norėdami užtikrinti, kad pasiūlymo eilutės importuojamos „Finance and Operations“, jei nenurodyta kliento arba produkto numatytoji informacija.

    - **SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes. Numatytosios **SiteId** šablono reikšmės nėra.
    - **WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes. Numatytosios **WarehouseId** šablono reikšmės nėra.

- Įsitikinkite, kad **CDS &gt; Paskirties vieta** susiejime (**Quantity_UOM** į **SALESUNITSYMBOL**) yra būtina „Finance and Operations“ pardavimo matavimo vieneto (MV) reikšmių schema.

## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

> [!NOTE]
> - Sudėtinga „Finance and Operations“ sąranka valdo laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai**. Ši sąranka šiuo metu nepalaiko integravimo susiejimo. Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** tvarko „Finance and Operations“.
> - Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

### <a name="quoteheader"></a>QuoteHeader

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Susijusios temos

[Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais](products-template-mapping.md)

[Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais](accounts-template-mapping.md)

[Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping.md)



