---
title: Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais
description: Šiame straipsnyje aptariamos šablonai ir su tuo susijusių užduočių, kurios naudojamos "Dynamics 365" pardavimo ir "Dynamics 365" tiekimo grandinės valdymo kontaktams (kontaktams) ir kontaktams (klientams) sinchronizuoti.
author: Henrikan
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 4ddb91c34816791d8eca80e4798eb46c1b496439
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857350"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais

[!include [banner](../includes/banner.md)]



> [!NOTE]
> Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Microsoft Dataverse“, skirtą programoms](/powerapps/administrator/data-integrator).

Šiame straipsnyje aptariamos šablonai ir susijusios užduotys, naudojamos sinchronizuojant lenteles Kontaktas (Kontaktai) ir Kontaktas (Klientai) tiesiogiai iš "Dynamics 365" pardavimo į Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai

Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose. Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus. Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.

[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai.](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

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

### <a name="contact-to-contact-example"></a>Kontakto kontakto pavyzdys

![Susisiekti su kontakto šablono žymėjimu duomenų integratoriuje.](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer-example"></a>Kliento kontakto pavyzdys

![Susisiekti su kliento šablono žymėjimu duomenų integratoriuje.](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-articles"></a>Susiję straipsniai

[Potencialaus kliento pavertimas pinigais](prospect-to-cash.md)

[Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais](accounts-template-mapping-direct.md)

[Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Sales“ produktais](products-template-mapping-direct.md)

[Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Supply Chain Management”](sales-order-template-mapping-direct-two-ways.md)

[Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]