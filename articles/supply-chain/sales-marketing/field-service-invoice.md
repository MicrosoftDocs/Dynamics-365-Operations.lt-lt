---
title: Sinchronizuokite „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF
description: Šiame straipsnyje aptariamos šablonai ir su tuo susijusių užduočių, kurios naudojamos norint sinchronizuoti sutarties SF "Dynamics 365" laukų paslaugoje, kad būtų galima išrašyti laisvos formos SF Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 04/10/2018
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
ms.openlocfilehash: c4ef70af71ae223baaa2abb2b64428beab946e3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900889"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Sinchronizuokite „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF

[!include[banner](../includes/banner.md)]



Šiame straipsnyje aptariamos šablonai ir su tuo susijusių užduočių, kurios naudojamos norint sinchronizuoti sutarties SF, naudojamos Dynamics 365 Field Service laisvos formos SF Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF.

**Šablono pavadinimas naudojant funkciją Duomenų integravimas**

- Sutarties SF („Field Service“ su „Supply Chain Management“)

**Užduočių pavadinimai projekte Duomenų integravimas**

- SF antraštės
- SF eilutės

Prieš sinchronizuojant sutarčių SF, būtina atlikti toliau nurodytą sinchronizavimo užduotį.

- Sąskaitos (iš „Sales” į „Supply Chain Management”) – tiesioginis

## <a name="entity-set"></a>Objektų rinkinys

| „Field service“  | „Supply Chain Management”                 |
|----------------|----------------------------------------|
| SF       | Dataverse kliento laisvos formos sąskaitų faktūrų antraštės |
| invoicedetails | Dataverse kliento laisvos formos sąskaitų faktūrų eilutės   |

## <a name="entity-flow"></a>Objekto srautas

SF, kurios buvo sukurtos iš „Field Service“ sutarties, su „Supply Chain Management“ galima sinchronizuoti per „Microsoft Dataverse“ duomenų integravimo projektą. Jei laisvos formos SF apskaitos būsena yra **Vykdoma**, šių SF naujinimai bus sinchronizuojami su „Supply Chain Management“ laisvos formos SF. „Supply Chain Management“ paskelbus laisvos formos SF ir apskaitos būseną atnaujinus į **Baigta**, daugiau nebegalėsite sinchronizuoti „Field Service“ naujinimų.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas

Stulpelis **Yra eilučių su sutarties kilme** įtrauktas į **Sąskaita faktūra** lentelę. Šis stulpelis padeda užtikrinti, kad bus sinchronizuojamos tik tos SF, kurios buvo sukurtos iš sutarties. Jei SF yra bent viena SF eilutė, kuri buvo perkelta iš sutarties, vertė yra **teisinga**.

Stulpelis **Turi sutarties kilmę** įtrauktas į **Sąskaitos faktūros eilutė** lentelę. Šis stulpelis padeda užtikrinti, kad bus sinchronizuojamos tik tos sąskaitos faktūros eilutės, kurios buvo sukurtos iš sutarties. Jei SF eilutė perkeliama iš sutarties, vertė yra **teisinga**.

Laukas **SF data** programoje „Supply Chain Management“ yra privalomas. Todėl, prieš pradedant sinchronizavimą „Field Service“ stulpelyje turi būti nurodyta reikšmė. Kad būtų atitiktas šis reikalavimas, įtraukiama toliau nurodyta logika.

- Jei stulpelis **Sąskaitos faktūros data** lentelėje **Sąskaita faktūra** yra tuščias (tai yra, jame neįvesta jokia reikšmė), įtraukus sąskaitos faktūros eilutę, perkeltą iš sutarties, lauke bus įvesta dabartinė data.
- Vartotojas gali pakeisti stulpelio **Sąskaitos faktūros data** reikšmę. Tačiau, jei sąskaitos faktūros stulpelis **Sąskaitos faktūros data** bus tuščias, vartotojui bandant įrašyti sąskaitą faktūrą, perkeltą iš sutarties, bus pateikta verslo proceso klaida.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

### <a name="in-supply-chain-management"></a>„Supply Chain Management“

Kad būtų galima atskirti „Supply Chain Management“ laisvos formos SF, kurios buvo sukurtos remiantis „Field Service“ sutarties SF, integravime turi būti nustatyta SF kilmė. Kai sąskaitos faktūros kilmė yra **Sutarties SF integravimas** tipo, laukas **Išorinis sąskaitos faktūros numeris** rodomas lauko **Pardavimo SF** antraštėje.

Lauko **Išorinis sąskaitos faktūros numeris** informacija, rodoma sąskaitos faktūros antraštėje, taip pat galima pasinaudoti, siekiant padėti užtikrinti, kad sąskaitos faktūros, kurios sukurtos remiantis „Field Service“ sutarčių SF, bus filtruojamos „Supply Chain Management“ sinchronizavimo su „Field Service“ metu.

1. Eikite į **Gautinos sumos** \> **Sąranka** \> **Sąskaitų faktūrų kilmės kodai**.
2. Norėdami sukurti naują sąskaitos faktūros kilmę, pasirinkite **Nauja**.
3. Lauke **Sąskaitos faktūros kilmė** įveskite sąskaitos faktūros kilmės pavadinimą, pavyzdžiui, **FS**.
4. Lauke **Aprašas** įveskite aprašą, pvz., **„Field Service“ sutarties sąskaita faktūra**.
5. Pasirinkite žymės langelį **Kilmės tipo priskyrimas**.
6. Nustatykite lauko **Sąskaitos faktūros kilmės tipas** reikšmę į **Sutarties sąskaitos faktūros integravimas**.
7. Pasirinkite **Įrašyti**.

### <a name="in-the-data-integration-project"></a>Duomenų integravimo projekte

Užduotis: **SF eilutės**  

Įsitikinkite, kad numatytoji reikšmė „Supply Chain Management“ lauke **Pagrindinės sąskaitos rodoma reikšmė** yra atnaujinama, jog atitiktų norimą vertę.

Numatytoji šablono vertė yra **401100**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Sutarties SF („Field Service“ su „Supply Chain Management“): SF antraštės

[![Sąskaitos faktūros antraščių šablonų susiejimas integruojant duomenis.](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Sutarties SF („Field Service“ su „Supply Chain Management“): SF eilutės

[![Sąskaitos faktūros eilučių šablonų susiejimas integruojant duomenis.](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]