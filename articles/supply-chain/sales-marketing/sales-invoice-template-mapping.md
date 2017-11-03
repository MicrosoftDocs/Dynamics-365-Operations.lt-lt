---
title: "Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“"
description: "Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ pardavimo sąskaitų faktūrų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“

[!include[banner](../includes/banner.md)]

Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ pardavimo sąskaitų faktūrų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“. 

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ pardavimo sąskaitų faktūrų antraštes ir eilutes su „Sales“.

- **Šablono pavadinimas naudojant funkciją Duomenų integravimas** 

     - Pardavimo sąskaitos faktūros (iš „Finance and Operations“ į „Sales“)

- **Užduočių pavadinimai projekte Duomenų integravimas**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Reikiamos sinchronizavimo užduotys prieš sinchronizuojant „Sales“ sąskaitų faktūrų antraštes ir eilutes:
-   Produktai (iš „Finance and Operations“ į „Sales“)
-   Sąskaitos (iš „Sales“ į „Finance and Operations“) (jei naudojama)
-   Kontaktai (iš „Sales“ į „Finance and Operations“) (jei naudojama)
-   Pardavimo užsakymo antraštė ir eilutės (iš „Finance and Operations“ į „Sales“)

## <a name="entity-set"></a>Objektų rinkinys

| „Finance and Operations”                               | „Common Data Service“ (CDS)              | Pardavimas          |
|------------------------------------------------------|------------------|----------------|
| Išorėje tvarkomų klientų pardavimo SF antraštės | SalesInvoice     | Sąskaitos faktūros       |
| Išorėje tvarkomų klientų pardavimo SF eilutės   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Objekto srautas

Pardavimo sąskaitos faktūros kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“.

> [!NOTE]
> Su **pardavimo sąskaitos faktūros antraštės** išlaidomis susijęs mokestis į sinchronizavimo iš „Finance and Operations“ į „Sales“ procesą šiuo metu nėra įtrauktas. Taip yra todėl, kad „Sales“ nepalaiko mokesčių informacijos antraštės lygyje. Įtrauktas mokestis, susijęs su išlaidomis eilutės lygyje.

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

-  Į objektą **Sąskaita faktūra** įtraukiamas ir puslapyje rodomas laukas **Sąskaitos faktūros numeris**.
 
-  Puslapyje **Pardavimo užsakymas** esantis mygtukas **Kurti sąskaitą faktūrą** yra paslėptas, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“. Puslapio **Sąskaita faktūra** redaguoti negalima, nes sąskaitos faktūros bus sinchronizuojamos iš „Finance and Operations“.
 
-  Kai susijusi „Finance and Operations“ sąskaita faktūra baigiama sinchronizuoti su „Sales“, **pardavimo užsakymo būsena** automatiškai pasikeičia į **Išrašyta sąskaita faktūra**. Be to, pardavimo užsakymo, iš kurio buvo sukurta sąskaita faktūra, savininkas priskiriamas sąskaitos faktūros savininku. Taip pardavimo užsakymo savininkui suteikiama galimybė peržiūrėti sąskaitą faktūrą.
 
## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

Prieš sinchronizuojant pardavimo sąskaitas faktūras, svarbu sistemas atnaujinti tolesniu parametru.

### <a name="setup-in-sales"></a>Sąranka sprendime „Sales“

- Įsitikinkite, kad dalyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas** parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta kaip **Taip**. 

- Įsitikinkite, kad dalyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas** parinktis **Nuolaidos skaičiavimo būdas** nustatyta kaip **Eilutės prekė**. 

### <a name="setup-in-the-data-integration-project"></a>Sąranka projekte Duomenų integravimas

#### <a name="salesinvoiceheader-task"></a>SalesInvoiceHeader užduotis

- Dalyje **Šaltinis** > **CDS** atnaujinkite **CDS organizacijos ID** susiejimą. 

    -  Numatytoji **SalesOrder_Organization_OrganizationId** šablono reikšmė yra ORG001.
    -  Numatytoji **Account_Organization_OrganizationId** šablono reikšmė yra ORG001.
    -  Numatytoji **Organization_OrganizationId** šablono reikšmė yra ORG001.

- Įsitikinkite, kad dalyje **Šaltinis** > **InvoiceCountryRegionId CDS** yra reikiamas susiejimas su **BillingAddress_Country**.

    -  Šablono reikšmė yra **ValueMap** su susietų šalių skaičiumi.

- Sprendime „Sales“ norint kurti sąskaitas faktūras, reikalingas **Kainoraštis**. Dalyje **CDS** > **pricelevelid.name paskirtis [kainoraščio pavadinimas]** kiekvienos valiutos reikšmę **ValueMap** atnaujinkite į sprendime „Sales“ naudojamą **kainoraštį**. Galite naudoti numatytąjį vienos valiutos **kainoraštį** arba **ValueMap**, jei turite **kainoraščių** keliomis valiutomis.

    -  **pricelevelid.name [kainoraščio pavadinimas]** šablono reikšmė yra **ValueMap** pagal **valiutą**.
    -  usd: CRM Service USA (pavyzdys). 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine užduotis

- Įsitikinkite, kad dalyje **Šaltinis** > **CDS matavimo vienetas** yra reikiamas susiejimas.

- Įsitikinkite, kad „Finance and Operations“ dalyje **Šaltinis** > **CDS susiejimas** yra reikiama **SalesUnitSymbol** **ValueMap** reikšmė. 
    
    - Apibrėžta **SalesUnitSymbol su Quantity_UOM** šablono reikšmė su **ValueMap**.
    
-  Dalyje **Šaltinis** > **CDS** atnaujinkite CDS organizacijos ID susiejimą. 

    -  Numatytoji **SalesInvoicer_Organization_OrganizationId** šablono reikšmė yra ORG001.
    -  Numatytoji **Product_Organization_OrganizationId** šablono reikšmė yra ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

> [!NOTE]
> **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti. Norint susieti šiuos laukus, reikia nustatyti reikšmių susiejimą, kuris atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

![Šablono susiejimas duomenų integratoriuje](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Susijusios temos

[Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais](products-template-mapping.md)

[Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais](accounts-template-mapping.md)

[Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais](contacts-template-mapping.md)

[Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“](sales-quotation-template-mapping.md)

[Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“](sales-order-template-mapping.md)


