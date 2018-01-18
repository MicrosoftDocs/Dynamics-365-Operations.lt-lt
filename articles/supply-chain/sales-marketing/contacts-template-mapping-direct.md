---
title: "Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ kontakto (kontaktai) ir kontakto (klientai) objektus sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimu."
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
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ kontakto (kontaktai) ir kontakto (klientai) objektus tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimu.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ kontakto (kontaktai) objektą su „Finance and Operations“ kontakto (klientai) objektu.

- **Šablonų pavadinimai naudojant funkciją Duomenų integravimas:**

    - Kontaktai (iš „Sales“ į „Finance and Operations“) – tiesioginis
    - Iš kontaktų į klientą (iš „Sales“ į „Finance and Operations“) – tiesioginis

- **Užduočių pavadinimai projekte Duomenų integravimas:**

    - Kontaktai
    - ContactToCustomer

Toliau nurodytą sinchronizavimo užduotį būtina atlikti prieš įvykstant kontakto sinchronizavimui: Sąskaitos (iš „Sales“ į „Finance and Operations“)

## <a name="entity-sets"></a>Objektų rinkiniai

| Pardavimas    | „Finance and Operations” |
|----------|------------------------|
| Kontaktai | CDS kontaktai           |
| Kontaktai | Klientai V2           |

## <a name="entity-flow"></a>Objekto srautas

Kontaktai tvarkomi „Sales“ ir sinchronizuojami su „Finance and Operations“.

„Sales“ kontaktas gali tapti „Finance and Operations“ kontaktu arba klientu. Norėdama nustatyti, ar „Sales“ kontaktas su „Finance and Operations“ turi būti sinchronizuojamas kaip kontaktas ar klientas, sistema ieško toliau nurodytų „Sales“ kontakto ypatybių.

- **Sinchronizuojant su „Finance and Operations“ klientu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip**
- **Sinchronizuojant su „Finance and Operations“ kontaktu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Ne**, o **įmonės** (pirminė sąskaita / kontaktas) taškai – į sąskaitą (ne kontaktą).

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Kontaktui įtrauktas naujas **Yra aktyvus klientas** laukas. Šis laukas naudojamas kontaktams, pasižymintiems pardavimo veikla, ir kontaktams, nepasižymintiems pardavimo veikla, atskirti. Lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip** tik kontaktams, turintiems susijusių pasiūlymų, užsakymų ar sąskaitų faktūrų. Su „Finance and Operations“ sinchronizuojami tik kaip klientai pažymėti „Sales“ kontaktai.

Kontaktui įtrauktas naujas **IsCompanyAnAccount** laukas. Šis laukas nurodo, ar kontaktas susietas su **sąskaitos** tipo įmone (pirmine sąskaita / kontaktu). Ši informacija naudojama nustatant kontaktus, kuriuos su „Finance and Operations“ reikia sinchronizuoti kaip kontaktus.

Kontaktui įtrauktas naujas **Kontakto numeris**, kad būtų užtikrintas srities ir unikalus integravimo raktas. Sukūrus naują kontaktą, lauko **Kontakto numeris** vertė sugeneruojama automatiškai, naudojant numeraciją. Vertę sudaro raidės **CON**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis. Pavyzdys: **CON-01000-BVRCPS**

Pritaikius „Sales“ skirtą integravimo sprendimą, atnaujinimo scenarijus, naudodamas pirmiau minėtą numeraciją, nustato esamų kontaktų lauką **Kontakto numeris**. Taip pat atnaujinimo scenarijus visiems pardavimo veikla pasižymintiems klientams nustato lauko **Yra aktyvus klientas** reikšmę į **Taip**.

## <a name="in-finance-and-operations"></a>Programoje „Finance and Operations”

Kontaktai žymimi naudojant ypatybę **IsContactPersonExternallyMaintained**. Ši ypatybė nurodo, kad nurodytas kontaktas tvarkomas išoriškai. Tokiu atveju išoriškai tvarkomus kontaktus tvarko „Sales“.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

### <a name="contact-to-customer"></a>Iš kontakto į klientą

- Laukas **CustomerGroup** būtinas „Finance and Operations“. Siekdami padėti išvengti sinchronizavimo klaidų, susiejime galite nurodyti numatytąją vertę. Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.

    Numatytoji šablono vertė yra **10**.

- Pridėdami toliau nurodytus susiejimus, galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių. Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.

    - **SiteId** – numatytąją vietą taip pat galima nurodyti ant produktų programoje „Finance and Operations“. SiteId – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.

        Nenurodyta **SiteId** šablono vertė.

    - **WarehouseId** – numatytąjį sandėlį taip pat galima nurodyti ant produktų programoje „Finance and Operations“. Sandėlis būtinas norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.

        Nenurodyta **WarehouseId** šablono vertė.

    - **LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.
    
        Numatytoji paskirtoji šablono vertė yra **en-us**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.

### <a name="contact-to-contact"></a>Iš kontakto į kontaktą

![Šablono susiejimas duomenų integratoriuje](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Iš kontakto į klientą

![Šablono susiejimas duomenų integratoriuje](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Susijusios temos

[Potencialūs klientai ir grynieji pinigai](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais](products-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimas su „Sales“](sales-order-template-mapping-direct.md)

[Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)



