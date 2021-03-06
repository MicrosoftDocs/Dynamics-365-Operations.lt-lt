---
title: Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ objektus Kontaktas (Kontaktai) ir Kontaktas (Klientai) sinchronizuojant su „Dynamics 365 Supply Chain Management“.
author: ChristianRytt
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 7bc4b48260907788eb90a19c5dc0b5c8f1d9d3b5
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908113"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Microsoft Dataverse“, skirtą programoms](/powerapps/administrator/data-integrator).

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ lenteles Kontaktas (Kontaktai) ir Kontaktas (Klientai) tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration). Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.

Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ kontakto (kontaktai) lenteles su „Supply Chain Management“ kontakto (klientai) lentele.

- **Šablonų pavadinimai naudojant funkciją Duomenų integravimas**

    - Kontaktai (iš „Sales” į „Supply Chain Management”) – tiesioginis
    - Iš kontaktų į klientą (iš „Sales” į „Supply Chain Management”) – tiesioginis

- **Užduočių pavadinimai projekte Duomenų integravimas**

    - Kontaktai
    - ContactToCustomer

Toliau nurodytą sinchronizavimo užduotį būtina atlikti prieš įvykstant kontakto sinchronizavimui: Sąskaitos (iš „Sales“ į „Supply Chain Management“)

## <a name="entity-sets"></a>Objektų rinkiniai

| Pardavimas    | „Supply Chain Management” |
|----------|------------------------|
| Kontaktai | „Dataverse” kontaktai           |
| Kontaktai | Klientai V2           |

## <a name="entity-flow"></a>Objekto srautas

Kontaktai valdomi programoje „Sales“ ir sinchronizuojami su „Supply Chain Management“.

„Sales“ kontaktas gali tapti „Supply Chain Management“ kontaktu arba klientu. Norėdama nustatyti, ar „Sales“ kontaktas su „Supply Chain Management“ turi būti sinchronizuojamas kaip kontaktas ar klientas, sistema ieško toliau nurodytų „Sales“ kontakto ypatybių.

- **Sinchronizuojant su „Supply Chain Management“ klientu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip**
- **Sinchronizuojant su „Supply Chain Management“ kontaktu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Ne**, o **įmonės** (pirminė sąskaita / kontaktas) taškai – į sąskaitą (ne kontaktą)

## <a name="prospect-to-cash-solution-for-sales"></a>„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas

Kontaktui įtrauktas naujas **Yra aktyvus klientas** stulpelis. Šis stulpelis naudojamas kontaktams, pasižymintiems pardavimo veikla, ir kontaktams, nepasižymintiems pardavimo veikla, atskirti. Lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip** tik kontaktams, turintiems susijusių pasiūlymų, užsakymų ar sąskaitų faktūrų. Su „Supply Chain Management“ sinchronizuojami tik kaip klientai pažymėti „Sales“ kontaktai.

Kontaktui įtrauktas naujas **„IsCompanyAnAccount”** stulpelis. Šis stulpelis nurodo, ar kontaktas susietas su **sąskaitos** tipo įmone (pirmine sąskaita / kontaktu). Ši informacija naudojama nustatant kontaktus, kuriuos su „Supply Chain Management“ reikia sinchronizuoti kaip kontaktus.

Kontaktui įtrauktas naujas stulpelis **Kontakto numeris** tam, kad būtų užtikrintas srities ir unikalus integravimo raktas. Sukūrus naują kontaktą, lauko **Kontakto numeris** vertė sugeneruojama automatiškai, naudojant numeraciją. Vertę sudaro raidės **CON**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis. Pavyzdys: **CON-01000-BVRCPS**

Pritaikius „Sales“ skirtą integravimo sprendimą, atnaujinimo scenarijus nustato esamų kontaktų stulpelį **Kontakto numeris** naudodamas anksčiau minėtą numeraciją. Taip pat atnaujinimo scenarijus nustato lauko **Yra aktyvus klientas** reikšmę į **Taip** visiems pardavimo veikla pasižymintiems klientams.

## <a name="in-supply-chain-management"></a>„Supply Chain Management“

Kontaktai žymimi naudojant ypatybę **IsContactPersonExternallyMaintained**. Ši ypatybė nurodo, kad nurodytas kontaktas tvarkomas išoriškai. Tokiu atveju išoriškai tvarkomus kontaktus tvarko „Sales“.

## <a name="preconditions-and-mapping-setup"></a>Išankstinės sąlygos ir susiejimo nustatymas

### <a name="contact-to-customer"></a>Iš kontakto į klientą

- Laukas **CustomerGroup** būtinas „Supply Chain Management“. Siekdami padėti išvengti sinchronizavimo klaidų, susiejime galite nurodyti numatytąją vertę. Bus naudojama numatytoji reikšmė, jei „Sales“ stulpelis yra paliktas tuščias.

    Numatytoji šablono vertė yra **10**.

- Pridėdami toliau nurodytus susiejimus, galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Supply Chain Management“, skaičių. Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.

    - **SiteId** – numatytąją vietą taip pat galima nurodyti ant produktų programoje „Supply Chain Management“. Vieta būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymus.

        Nenurodyta **SiteId** šablono vertė.

    - **WarehouseId** – numatytąjį sandėlį taip pat galima nurodyti ant produktų programoje „Supply Chain Management“. Sandėlis būtinas norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymus.

        Nenurodyta **WarehouseId** šablono vertė.

    - **LanguageId** – kalba būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymus.
    
        Numatytoji paskirtoji šablono vertė yra **en-us**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas. 

> [!NOTE]
> Susiejime rodoma, kuri stulpelio informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.

### <a name="contact-to-contact"></a>Iš kontakto į kontaktą

![Šablono susiejimas duomenų integratoriuje](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Iš kontakto į klientą

![Šablono susiejimas duomenų integratoriuje](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Susijusios temos

[Potencialaus kliento pavertimas pinigais](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Sales“ produktais](products-template-mapping-direct.md)

[Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Supply Chain Management”](sales-order-template-mapping-direct-two-ways.md)

[Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]