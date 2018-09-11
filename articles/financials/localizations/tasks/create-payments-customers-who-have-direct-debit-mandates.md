--- 
title: "Mokėjimų sukūrimas klientui, turinčiam tiesioginio debeto įgaliojimus"
description: "Šioje procedūroje parodoma, kaip generuoti ISO20022 tiesioginio debeto mokėjimo failą klientui, turinčiam sukonfigūruotą tiesioginį debetą ir SF apmokėti."
author: mrolecki
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: acd6a8076288d8d1d1aa05af33e306c6a29780f7
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Mokėjimų sukūrimas klientui, turinčiam tiesioginio debeto įgaliojimus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip generuoti ISO20022 tiesioginio debeto mokėjimo failą klientui, turinčiam sukonfigūruotą tiesioginį debetą ir SF apmokėti. SF kūrimas ir registravimas nėra būtinas. Užuot nustatę, kad SF turi būti apmokėta, žurnale galite pasirinkti įgaliojimą prieš generuodami mokėjimo failą, kad būtų palaikomas kliento išankstinio mokėjimo scenarijus.



Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.



Tai yra penktoji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas. Prieš atlikdami šią užduotį, turite baigti ankstesnes užduotis. Pirmiausia turite importuoti kliento mokėjimo elektroninių ataskaitų konfigūracijas, sukonfigūruoti mokėjimų metodus ir nustatyti savo įmonės bei kliento informaciją. 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a>Registruoti laisvos formos SF su tiesioginio debeto informacija
1. Pasirinkite Gautinos sumos > Sąskaitos faktūros > Visos laisvos formos SF.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, pasirinkite DE-010.  
4. Lauke Mokėjimo metodas įveskite arba pasirinkite vertę.
    * 2) Dabartinis įvykis: bus siunčiamas dabartinis produktas. pasirinkite Elektroninis.  
5. Lauke Tiesioginio debeto įgaliojimo ID įveskite arba pasirinkite vertę.
6. Spustelėkite Pridėti eilutę.
7. Lauke Aprašas surinkite reikšmę.
8. Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.
9. Lauke Vieneto kaina įveskite skaičių.
10. Spustelėkite Registruoti.
11. Spustelėkite GERAI.

## <a name="create-a-payment"></a>Kurti mokėjimą
1. Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų žurnalas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
4. Spustelėkite Eilutės.
5. Spustelėkite Mokėjimo pasiūlymas.
6. Spustelėkite Kurti mokėjimo pasiūlymą.
7. Išplėskite dalį Įtrauktini įrašai.
8. Spustelėkite Filtras.
9. Sąraše pasirinkite lentelės Kliento operacijos eilutę ir lauką Mokėjimo būdas.
    * Galite taikyti bet kokius kriterijus, norėdami pasirinkti, kurias kliento operacijas apmokėti. Šiame pavyzdyje norėdami filtruoti operacijas naudokite apmokėjimo būdą Elektroninis.  
10. Lauke Kriterijai įveskite arba pasirinkite reikšmę.
11. Spustelėkite GERAI.
12. Spustelėkite GERAI.
13. Spustelėkite Kurti mokėjimus.

## <a name="generate-a-payment-file"></a>Generuoti mokėjimo failą


