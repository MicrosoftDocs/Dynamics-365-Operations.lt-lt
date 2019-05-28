---
title: „Field Service“ sutarčių SF sinchronizavimas su „Finance and Operations“ laisvos formos SF
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ sutarčių SF su „Microsoft Dynamics 365 for Finance and Operations“ laisvos formos SF.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560169"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>„Field Service“ sutarčių sąskaitų faktūrų sinchronizavimas su „Finance and Operations“ laisvos formos sąskaitomis faktūromis

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ sutarčių SF su „Microsoft Dynamics 365 for Finance and Operations“ laisvos formos SF.

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Field Service“ sutarčių SF su „Finance and Operations“ laisvos formos SF.

**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**

- Sutarčių SF (iš „Field Service“ į „Finance and Operations“)

**Užduočių pavadinimai projekte Duomenų integravimas:**

- SF antraštės
- SF eilutės

Prieš sinchronizuojant sutarčių SF, būtina atlikti toliau nurodytą sinchronizavimo užduotį.

- Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis

## <a name="entity-set"></a>Objektų rinkinys

| Field Service  | „Finance and Operations”                 |
|----------------|----------------------------------------|
| SF       | CDS kliento laisvos formos sąskaitų faktūrų antraštės |
| InvoiceDetails | CDS kliento laisvos formos sąskaitų faktūrų eilutės   |

## <a name="entity-flow"></a>Objekto srautas

SF, kurios buvo sukurtos iš „Field Service“ sutarties, su „Finance and Operations“ galima sinchronizuoti per „Common Data Service“ (CDS) duomenų integravimo projektą. Jei laisvos formos SF apskaitos būsena yra **Vykdoma**, šių SF naujinimai bus sinchronizuojami su „Finance and Operations“ laisvos formos SF. „Finance and Operations“ paskelbus laisvos formos SF ir apskaitos būseną atnaujinus į **Baigta**, daugiau nebegalėsite sinchronizuoti „Field Service“ naujinimų.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas

Laukas **Yra eilučių su sutarties kilme** įtrauktas į objektą **SF**. Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF, kurios buvo sukurtos iš sutarties. Jei SF yra bent viena SF eilutė, kuri buvo perkelta iš sutarties, vertė yra **teisinga**.

Laukas **Nurodyta sutarties kilmė** įtrauktas į objektą **SF eilutė**. Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF eilutės, kurios buvo sukurtos iš sutarties. Jei SF eilutė perkeliama iš sutarties, vertė yra **teisinga**.

Laukas **SF data** programoje „Finance and Operations“ yra privalomas. Todėl, prieš pradedant sinchronizavimą „Field Service“ lauke turi būti nurodyta reikšmė. Kad būtų atitiktas šis reikalavimas, įtraukiama toliau nurodyta logika.

- Jei laukas **SF data** objekte **Sąskaita faktūra** yra tuščias (t. y., jame neįvesta jokia reikšmė), įtraukus SF eilutę, perkeltą iš sutarties, lauke bus įvesta dabartinė data.
- Vartotojas gali pakeisti lauko **SF data** reikšmę. Tačiau, jei laukas **SF data** sąskaitoje faktūroje bus tuščias, vartotojui bandant įrašyti SF, perkeltą iš sutarties, bus pateikta verslo proceso klaida.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

### <a name="in-finance-and-operations"></a>Programoje „Finance and Operations”

Kad būtų galima atskirti „Finance and Operations“ laisvos formos SF, kurios buvo sukurtos remiantis „Field Service“ sutarties SF, integravime turi būti nustatyta SF kilmė. Kai sąskaitos faktūros kilmė yra **Sutarties SF integravimas** tipo, laukas **Išorinis sąskaitos faktūros numeris** rodomas lauko **Pardavimo SF** antraštėje.

Lauko **Išorinis sąskaitos faktūros numeris** informacija, rodoma sąskaitos faktūros antraštėje, taip pat galima pasinaudoti, siekiant padėti užtikrinti, kad sąskaitos faktūros, kurios sukurtos remiantis „Field Service“ sutarčių SF, bus filtruojamos „Finance and Operations“ sinchronizavimo su „Field Service“ metu.

1. Eikite į **Gautinos sumos** \> **Sąranka** \> **Sąskaitų faktūrų kilmės kodai**.
2. Norėdami sukurti naują sąskaitos faktūros kilmę, pasirinkite **Nauja**.
3. Lauke **Sąskaitos faktūros kilmė** įveskite sąskaitos faktūros kilmės pavadinimą, pavyzdžiui, **FS**.
4. Lauke **Aprašas** įveskite aprašą, pvz., **„Field Service“ sutarties sąskaita faktūra**.
5. Pasirinkite žymės langelį **Kilmės tipo priskyrimas**.
6. Nustatykite lauko **Sąskaitos faktūros kilmės tipas** reikšmę į **Sutarties sąskaitos faktūros integravimas**.
7. Pasirinkite **Įrašyti**.

### <a name="in-the-data-integration-project"></a>Duomenų integravimo projekte

Užduotis: **SF eilutės**  

Įsitikinkite, kad numatytoji reikšmė „Finance and Operations“ lauke **Pagrindinės sąskaitos rodoma reikšmė** yra atnaujinama, jog atitiktų norimą vertę.

Numatytoji šablono vertė yra **401100**.

## <a name="template-mapping-in-data-integration"></a>Šablono susiejimas naudojant funkcija Duomenų integravimas

Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>Sutarčių SF (iš „Field Service“ į „Finance and Operations“): SF antraštės

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>Sutarčių SF (iš „Field Service“ į „Finance and Operations“): SF eilutės

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
