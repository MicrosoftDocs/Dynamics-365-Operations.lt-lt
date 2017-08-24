--- 
title: "Nustatyti ISO20022 kredito pervedimų tiekėjus ir tiekėjų banko sąskaitas"
description: "Ši procedūra padeda nustatyti tiekėjo ir konkretaus tiekėjo banko sąskaitos informaciją, reikalingą generuojant ISO20022 kredito pervedimo ar bet kurio kito tiekėjo mokėjimo failą."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 147d8fa82bf15c984ad263cada42789038fa7371
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Nustatyti ISO20022 kredito pervedimų tiekėjus ir tiekėjų banko sąskaitas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padeda nustatyti tiekėjo ir konkretaus tiekėjo banko sąskaitos informaciją, reikalingą generuojant ISO20022 kredito pervedimo ar bet kurio kito tiekėjo mokėjimo failą. 

Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.
Tai yra ketvirtoji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="set-up-bank-details"></a>Nustatyti banko informaciją
1. Pasirinkite Mokėtinos sumos > Tiekėjai > Visi tiekėjai.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Tiekėjo sąskaita naudodami reikšmę „DE-001“.
3. Spustelėkite DE-001, kad atidarytumėte tiekėjo informaciją.
4. Veiksmų srityje spustelėkite Tiekėjas.
5. Spustelėkite Banko sąskaitos.
6. Spustelėkite Redaguoti.
    * Jei banko sąskaitos nėra, turite sukurti naują.  
7. Lauke SWIFT kodas surinkite „COBADEFFXXX‟.
8. Lauke IBAN surinkite „DE36200400000628808808‟.
9. Uždarykite puslapį.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Tiekėjo mokėjimo būdo nustatymas
1. Spustelėkite Redaguoti.
2. Išplėskite arba sutraukite skyrių „Mokėjimas“.
3. Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite saitą eilutėje SEPA CT.
5. Spustelėkite Įrašyti.


