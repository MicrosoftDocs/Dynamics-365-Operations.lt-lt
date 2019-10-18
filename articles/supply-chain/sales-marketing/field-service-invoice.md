---
title: Sinchronizuokite „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojamos sinchronizuojant „Dynamics 365 Field Service“ sutarčių SF su „Dynamics 365 Supply Chain Management“ laisvos formos SF.
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
ms.openlocfilehash: 3ca0014dc8bc1c70670a3cf85527eee0ef44865f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249870"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Sinchronizuokite „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF

[!include[banner](../includes/banner.md)]

Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Field Service“ sutarčių SF su „Dynamics 365 Supply Chain Management“ laisvos formos SF.

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

| „Field Service“  | „Supply Chain Management”                 |
|----------------|----------------------------------------|
| SF       | CDS kliento laisvos formos sąskaitų faktūrų antraštės |
| InvoiceDetails | CDS kliento laisvos formos sąskaitų faktūrų eilutės   |

## <a name="entity-flow"></a>Objekto srautas

SF, kurios buvo sukurtos iš „Field Service“ sutarties, su „Supply Chain Management“ galima sinchronizuoti per „Common Data Service“ duomenų integravimo projektą. Jei laisvos formos SF apskaitos būsena yra **Vykdoma**, šių SF naujinimai bus sinchronizuojami su „Supply Chain Management“ laisvos formos SF. „Supply Chain Management“ paskelbus laisvos formos SF ir apskaitos būseną atnaujinus į **Baigta**, daugiau nebegalėsite sinchronizuoti „Field Service“ naujinimų.

## <a name="field-service-crm-solution"></a>„Field Service“ CRM sprendimas

Laukas **Yra eilučių su sutarties kilme** įtrauktas į objektą **SF**. Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF, kurios buvo sukurtos iš sutarties. Jei SF yra bent viena SF eilutė, kuri buvo perkelta iš sutarties, vertė yra **teisinga**.

Laukas **Nurodyta sutarties kilmė** įtrauktas į objektą **SF eilutė**. Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF eilutės, kurios buvo sukurtos iš sutarties. Jei SF eilutė perkeliama iš sutarties, vertė yra **teisinga**.

Laukas **SF data** programoje „Supply Chain Management“ yra privalomas. Todėl, prieš pradedant sinchronizavimą „Field Service“ lauke turi būti nurodyta reikšmė. Kad būtų atitiktas šis reikalavimas, įtraukiama toliau nurodyta logika.

- Jei laukas **SF data** objekte **Sąskaita faktūra** yra tuščias (t. y., jame neįvesta jokia reikšmė), įtraukus SF eilutę, perkeltą iš sutarties, lauke bus įvesta dabartinė data.
- Vartotojas gali pakeisti lauko **SF data** reikšmę. Tačiau, jei laukas **SF data** sąskaitoje faktūroje bus tuščias, vartotojui bandant įrašyti SF, perkeltą iš sutarties, bus pateikta verslo proceso klaida.

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

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Sutarties SF („Field Service“ su „Supply Chain Management“): SF eilutės

[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
