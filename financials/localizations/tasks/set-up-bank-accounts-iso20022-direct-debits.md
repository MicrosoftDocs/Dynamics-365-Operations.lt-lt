--- 
title: "Nustatyti ISO20022 tiesioginio debeto klientus ir klientų banko sąskaitas"
description: "Ši užduotis apžvelgia, kaip nustatyti kliento banko sąskaitą ir kliento tiesioginio debeto įgaliojimą, kurių reikia norint generuoti kliento mokėjimo failą, pvz., ISO20022 tiesioginio debeto mokėjimo failą."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7aac1af99f2b5a7b1a123a8e3d3d6ddcaaa39b8d
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Nustatyti ISO20022 tiesioginio debeto klientus ir klientų banko sąskaitas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši užduotis apžvelgia, kaip nustatyti kliento banko sąskaitą ir kliento tiesioginio debeto įgaliojimą, kurių reikia norint generuoti kliento mokėjimo failą, pvz., ISO20022 tiesioginio debeto mokėjimo failą. Atsižvelgiant į nustatytus kliento mokėjimo formatus, gali būti reikalinga papildoma kliento arba kliento banko kodo informacija, kuri nėra aprašyta šioje procedūroje. 

Ši užduotis buvo sukurta naudojant demonstracinių duomenų įmonę DEMF, kai juridinio subjekto pirminis adresas yra Vokietijoje.



Tai yra ketvirtoji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.


## <a name="set-up-a-customer-bank-account"></a>Nustatyti kliento banko sąskaitą
1. Pasirinkite Gautinos sumos > Klientai > Visi klientai.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Sąskaita naudodami reikšmę „DE-010 “.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Veiksmų srityje spustelėkite Klientas.
5. Spustelėkite Banko sąskaitos.
6. Spustelėkite Naujas.
7. Lauke Banko sąskaita surinkite reikšmę.
8. Lauke Pavadinimas surinkite reikšmę.
    * Pavyzdžiui, įveskite EUR bankas.  
9. Lauke Bankų grupės įveskite arba pasirinkite reikšmę.
10. Lauke IBAN surinkite reikšmę.
    * Pavyzdžiui, įveskite DE36200400000628808808.  
11. Lauke SWIFT kodas surinkite reikšmę.
    * Pavyzdžiui: įveskite „COBADEFFXXX‟.  Atkreipkite dėmesį, kad SWIFT / BIC nereikalingas naudojant daugelį mokėjimo formatų, tačiau vis tiek rekomenduojama užregistruoti banko kodo SWIFT / BIC.  
12. Spustelėkite Įrašyti.
13. Uždarykite puslapį.
14. Spustelėkite Redaguoti.
15. Išplėskite dalį Numatytosios mokėjimo nuostatos.
16. Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.

## <a name="add-a-direct-debit-mandate"></a>Pridėti tiesioginio debeto įgaliojimą
1. Išplėskite dalį Tiesioginio debeto įgaliojimai.
2. Spustelėkite Pridėti.
3. Lauke Kreditoriaus banko sąskaita įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite DEMF OPER.  
4. Lauke Pasirašymo data įveskite datą.
5. Spustelėkite Taip, kad patvirtintumėte datos atnaujinimą.
6. Lauke Pasirašymo vieta įveskite arba pasirinkite reikšmę.
7. Lauke Numatomas mokėjimų skaičius įveskite skaičių.
8. Spustelėkite GERAI.
9. Spustelėkite Įrašyti.


