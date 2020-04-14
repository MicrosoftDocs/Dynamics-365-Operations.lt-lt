---
title: Mokėjimų sukūrimas klientui, turinčiam tiesioginio debeto įgaliojimus
description: Šioje procedūroje parodoma, kaip generuoti ISO20022 tiesioginio debeto mokėjimo failą klientui, turinčiam sukonfigūruotą tiesioginį debetą ir SF apmokėti.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a4714f1f1b24554684219fc1d766b4b87cff7bb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141608"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a>Mokėjimų sukūrimas klientui, turinčiam tiesioginio debeto įgaliojimus

[!include [banner](../../includes/banner.md)]

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
11. Spustelėkite Gerai.
12. Spustelėkite Gerai.
13. Spustelėkite Kurti mokėjimus.
