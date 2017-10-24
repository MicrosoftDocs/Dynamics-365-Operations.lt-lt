---
title: "Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ kontaktą (kontaktai) ir kontaktą (klientai) sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimu)."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration). 

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ („Sales“) kontakto (kontaktai) objektus ir kontaktą (klientai) sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimu, „Finance and Operations“).

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ kontaktą (kontaktai) su „Finance and Operations“ kontaktu (klientai).

- **Šablono pavadinimai**

    - Kontaktai (iš „Sales“ į „Finance and Operations“)
    - Iš kontaktų į klientą (iš „Sales“ į „Finance and Operations“)

- **Užduočių pavadinimai projekte**

    - Kontaktai
    - ContactToCustomer

Toliau nurodytą sinchronizavimo užduotį būtina atlikti prieš sinchronizuojant kontaktą: sąskaitos (iš „Sales“ į „Finance and Operations“)

## <a name="entity-sets"></a>Objektų rinkiniai

| Pardavimas    | CDS     | „Finance and Operations” |
|----------|---------|------------------------|
| Kontaktai | Kontaktas | CDS kontaktai           |
| Kontaktai | Paskyra | Klientai V2           |

## <a name="entity-flow"></a>Objekto srautas

Kontaktai valdomi programoje „Sales“ ir sinchronizuojami su „Finance and Operations“ programa „Common Data Service“ (CDS).

„Sales“ kontaktas gali tapti CDS ir „Finance and Operations“ kontaktu. Taip pat jis gali atsidaryti sąskaitą CDS ir tapti „Finance and Operations“ klientu. Norėdama nustatyti, ar kontaktą reikia paimti iš „Sales“ ir sinchronizuoti su CDS ir „Finance and Operations“ (pvz., „Sales“ kontaktus &gt;CDS kontaktą &gt; „Finance and Operations“ kontaktą), sistema ieško toliau nurodytų „Sales“ kontakto ypatybių.

- **Sinchronizuojant su CDS sąskaita ir „Finance and Operations“ klientu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip**
- **Sinchronizuojant su CDS kontaktu ir „Finance and Operations“ kontaktu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Ne**, o **įmonės** (pirminė sąskaita / kontaktas) taškai į sąskaitą (ne kontaktą).

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas 

Kontaktui įtrauktas naujas **Yra aktyvus klientas** laukas. Šis laukas naudojamas kontaktams, pasižymintiems pardavimo veikla, ir kontaktams, nepasižymintiems pardavimo veikla, atskirti. Lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip** tik kontaktams, turintiems susijusių pasiūlymų, užsakymų ar sąskaitų faktūrų. Su „Finance and Operations“ sinchronizuojami tik kaip klientai pažymėti „Sales“ kontaktai.

Kontaktui įtrauktas naujas **IsCompanyAnAccount** laukas. Šis laukas naudojamas nurodyti, ar kontaktas susietas su **sąskaitos** tipo įmone (pirmine sąskaita / kontaktu). Ši informacija naudojama nustatant kontaktus, kuriuos su „Finance and Operations“ reikia sinchronizuoti kaip kontaktus.

Kontaktui įtrauktas naujas **Kontakto numeris**, kad būtų užtikrintas srities ir unikalus integravimo raktas. Sukūrus naują kontaktą lauko **Kontakto numeris** vertė sugeneruojama automatiškai, naudojant numeraciją. Vertę sudaro raidės **CON**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis. Pavyzdys: **CON-01000-BVRCPS**

Į „Sales“ įtraukus „Sales“ skirtą integravimo sprendimą, atnaujinimo scenarijus, naudodamas pirmiau minėtą numeraciją, nustato esamų kontaktų lauką **Kontakto numeris**. Taip pat atnaujinimo scenarijus visiems pardavimo veikla pasižymintiems klientams nustato lauko **Yra aktyvus klientas** reikšmę į **Taip**.

## <a name="in-finance-and-operations"></a>Programoje „Finance and Operations” 

Kontaktai žymimi naudojant ypatybę **IsContactPersonExternallyMaintained**. Ši ypatybė nurodo, kad nurodytas kontaktas tvarkomas išoriškai. Tokiu atveju išoriškai tvarkomus kontaktus tvarko „Sales“.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

### <a name="contact-to-contact"></a>Iš kontakto į kontaktą

- Atnaujinkite **CDS organizacijos ID** susiejime **Šaltinis &gt;CDS**.

    - Numatytoji **Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.
    - Numatytoji **PrimaryAccount_Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.

- „Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas. Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Operacijos** galite nurodyti numatytąją vertę. Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė. Numatytoji **PrimaryAddressCountryRegionISOCode** šablono reikšmė vertė **USA**.
- Įsitikinkite, kad „Finance and Operations“ yra toliau nurodyto lauko vertė. Jei „Finance and Operations“ ši informacija nebūtina, galite pašalinti susiejimą iš susiejimo **CDS &gt; Paskirties vieta**.

    - **Lauko pavadinimas programoje „Finance and Operations“:** sprendimas
    - **Susiejimas:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Iš kontakto į klientą

- Atnaujinkite **CDS organizacijos ID** susiejime **Šaltinis &gt;CDS**. Numatytoji **Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.
- „Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas. Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Paskirties vieta** galite nurodyti numatytąją vertę. Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė. Numatytoji **PrimaryAddressCountryRegionISOCode** šablono reikšmė vertė **USA**.
- Laukas **CustomerGroup** būtinas „Finance and Operations“. Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Paskirties vieta** galite nurodyti numatytąją vertę. Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė. Numatytoji **CustomerGroupId** šablono vertė yra **10**.
- Pridėdami toliau nurodytus susiejimus iš **CDS &gt; Paskirties vietos** galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių. Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.

    - **SiteId** – numatytąją vietą taip pat galima nurodyti ant produktų programoje „Finance and Operations“. SiteId – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus. Nenurodyta **SiteId** šablono vertė.
    - **WarehouseId** – numatytąjį sandėlį taip pat galima nurodyti ant produktų programoje „Finance and Operations“. Sandėlis būtinas norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus. Nenurodyta **WarehouseId** šablono vertė.
    - **LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus. Numatytoji **LanguageId** šablono vertė yra **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Šablono susiejimas duomenų integratoriuje

Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.

### <a name="contact-to-contact"></a>Iš kontakto į kontaktą

![Šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-1.png)

![Kontaktų šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Iš kontakto į klientą

![Šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-3.png)

![Kontaktų šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Susijusios temos

[Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais](products-template-mapping.md)

[Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais](accounts-template-mapping.md)

[Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“](sales-quotation-template-mapping.md)

[Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“](sales-order-template-mapping.md)

[Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“](sales-invoice-template-mapping.md)

