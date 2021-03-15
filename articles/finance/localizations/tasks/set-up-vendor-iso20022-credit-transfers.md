---
title: Nustatyti ISO20022 kredito pervedimų tiekėjus ir tiekėjų banko sąskaitas
description: Ši procedūra padeda nustatyti tiekėjo ir konkretaus tiekėjo banko sąskaitos informaciją, reikalingą generuojant ISO20022 kredito pervedimo ar bet kurio kito tiekėjo mokėjimo failą.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a7245824c53ab594d62e9296e1f32d32a96ab84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988025"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Nustatyti ISO20022 kredito pervedimų tiekėjus ir tiekėjų banko sąskaitas

[!include [banner](../../includes/banner.md)]

Ši procedūra padeda nustatyti tiekėjo ir konkretaus tiekėjo banko sąskaitos informaciją, reikalingą generuojant ISO20022 kredito pervedimo ar bet kurio kito tiekėjo mokėjimo failą. 

Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.
Tai yra ketvirtoji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]