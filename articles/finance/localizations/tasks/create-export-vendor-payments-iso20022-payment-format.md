---
title: Tiekėjo mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą
description: Šioje procedūroje parodoma, kaip kurti mokėjimo eilutes tiekėjo mokėjimų žurnale ir generuoti tiekėjo mokėjimo failą naudojant ISO2022 kredito pervedimo pavyzdį.
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b70ad94014587ba8e55735192dbe0ab2e4adf4ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185824"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a>Tiekėjų mokėjimų kūrimas ir eksportavimas naudojant ISO20022 mokėjimo formatą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje paaiškinama, kaip kurti mokėjimo eilutes tiekėjo mokėjimų žurnale ir generuoti tiekėjo mokėjimo failą naudojant ISO2022 kredito pervedimo pavyzdį.

Tai yra penktoji iš penkių procedūrų, kuriose aprašomas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas. Šiame pavyzdyje naudokite demonstracinių duomenų įmonę DEMF.

## <a name="example"></a>Pavyzdys

1.  Pasirinkite **Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas**.
2.  Spustelėkite **Naujas**.
3.  Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.
4.  Spustelėkite **Eilutės > Mokėjimo pasiūlymas -> Kurti mokėjimo pasiūlymą**.
5.  Išplėskite dalį **Įtrauktini įrašai**.
6.  Spustelėkite **Filtras**.
7.  Sąraše pasirinkite lentelės **Tiekėjai** eilutę ir lauką **Tiekėjo kodas**.
8.  Lauke **Kriterijai** įveskite arba pasirinkite reikšmę. Galite taikyti bet kokį kriterijų, norėdami pasirinkti, kurias tiekėjo operacijas apmokėti, šiame pavyzdyje kaip tiekėjo kodą naudokite DE-001.
12. Spustelėkite **Gerai**.
13. Spustelėkite **Gerai**.
14. Spustelėkite **Kurti mokėjimus**.
15. Generuokite ISO20022 mokėjimo failą.
    1.  Spustelėkite **Generuoti mokėjimus**.
    2.  Lauke **Mokėjimo metodas** įveskite arba pasirinkite vertę.
    3.  Lauke **Failo pavadinimas** suveskite reikšmę. Šiame pavyzdyje sugeneroro uostotas failas bus suderinamas su SEPA, nes mokėjimas – eurais. ISO20022 kredito pavedimas ir kiti tiekėjo mokėjimo formatai taip pat gali būti naudojami generuojant mokėjimus kitomis valiutomis.
    4.  Lauke **Banko sąskaita** įveskite arba pasirinkite reikšmę.
