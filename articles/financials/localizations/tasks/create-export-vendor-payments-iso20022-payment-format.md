--- 
title: "Tiekėjo mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą"
description: "Šioje procedūroje parodoma, kaip kurti mokėjimo eilutes tiekėjo mokėjimų žurnale ir generuoti tiekėjo mokėjimo failą naudojant ISO2022 kredito pervedimo pavyzdį."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cc90bc86cd489b124a806c480632dd53ba47f3f
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Tiekėjo mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip kurti mokėjimo eilutes tiekėjo mokėjimų žurnale ir generuoti tiekėjo mokėjimo failą naudojant ISO2022 kredito pervedimo pavyzdį. 

Juriant šią procedūrą naudojama demonstracinių duomenų įmonė yra DEMF.

Tai yra penktoji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="create-payment-lines"></a>Kurti mokėjimo eilutes
1. Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.
2. Spustelėkite Naujas.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
5. Spustelėkite Eilutės.
6. Spustelėkite Mokėjimo pasiūlymas.
7. Spustelėkite Kurti mokėjimo pasiūlymą.
8. Išplėskite dalį Įtrauktini įrašai.
9. Spustelėkite Filtras.
10. Sąraše pasirinkite lentelės Tiekėjai eilutę ir lauką Tiekėjo kodas.
11. Lauke Kriterijai įveskite arba pasirinkite reikšmę.
    * Galite taikyti bet kokį kriterijų, norėdami pasirinkti, kurias tiekėjo operacijas apmokėti, šiame pavyzdyje kaip tiekėjo kodą naudokite DE-001.  
12. Spustelėkite GERAI.
13. Spustelėkite GERAI.
14. Spustelėkite Kurti mokėjimus.

## <a name="generate-an-iso20022-payment-file"></a>ISO20022 mokėjimo failo generavimas


