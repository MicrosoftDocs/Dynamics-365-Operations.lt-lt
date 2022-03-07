---
title: Kurti kliento tiesioginio debeto įgaliojimą
description: Šis užduočių vadovas parodo, kaip sukurti tiesioginio debeto įgaliojimą ir jį naudoti SF.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f746da0bcf2b1e0cb09af6b5e2ea61938213c924
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991047"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Kurti kliento tiesioginio debeto įgaliojimą

[!include [banner](../../includes/banner.md)]

Šis užduočių vadovas parodo, kaip sukurti tiesioginio debeto įgaliojimą ir jį naudoti SF.


## <a name="create-a-bank-account"></a>Kurti banko sąskaitą
1. **Naršymo srityje** eikite į **Moduliai > Gautinos sumos > Klientai > Visi klientai**.
2. Sąraše pažymėkite įrašą. Pavyzdžiui, pasirinkite US-001
3. Veiksmų srityje spustelėkite **Klientas**.
4. Spustelėkite **Banko sąskaitos**.
5. Spustelėkite **Naujas**.
6. Lauke **Banko sąskaita** įveskite reikšmę.
7. Lauke **Pavadinimas** įveskite reikšmę.
8. Lauke **IBAN** įveskite reikšmę.
9. Lauke **Valiuta** įveskite reikšmę.
10. Spustelėkite **Įrašyti**.
11. Uždarykite puslapį.
12. **Naršymo sritis** eikite į **Moduliai > Pinigų ir banko valdymas > Banko sąskaitos > Banko sąskaitos**.
13. Sąraše raskite ir pasirinkite norimą įrašą.
14. Sąraše spustelėkite saitą pasirinktoje eilutėje.
15. Spustelėkite **Redaguoti**.
16. Išplėskite „fastTab“ **Papildomas identifikavimas**.
17. Lauke **Tiesioginio debeto ID** įveskite reikšmę.
18. Lauke **IBAN** įveskite reikšmę.
19. Uždarykite puslapį.
20. Uždarykite puslapį.

## <a name="define-the-electronic-payment-method"></a>Apibrėžti elektroninio mokėjimo būdą
1. **Naršymo sritis** eikite į **Moduliai > Gautinos sumos > Mokėjimų sąranką > Mokėjimo būdai**.
2. Spustelėkite **Naujas**.
3. Lauke **Mokėjimo būdas** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke **Mokėjimo tipas** įveskite „Elektroninis mokėjimas“. Tiesioginio debeto įgaliojimo mokėjimo tipas turi būti Elektroninis mokėjimas.
6. Pažymėkite Taip lauke **Reikia įgaliojimo**.
7. Uždarykite puslapį.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Prie kliento pridėkite tiesioginio debeto įgaliojimą.
1. **Naršymo srityje** eikite į **Moduliai > Gautinos sumos > Klientai > Visi klientai**.
2. Sąraše pažymėkite įrašą. Pavyzdžiui, pasirinkite US-001
3. Spustelėkite **Redaguoti**.
4. Išplėskite „fastTab“ **Numatytieji mokėjimai**.
5. Lauke **Mokėjimo metodas** įveskite arba pasirinkite vertę.
6. Išplėskite „fastTab“ **Numatytieji mokėjimai**.
7. Išplėskite „fastTab“ **Tiesioginio debeto įgaliojimai**.
8. Spustelėkite **Pridėti**.
9. Lauke **Banko sąskaita** įveskite arba pasirinkite reikšmę.
10. Lauke **Kreditoriaus banko sąskaita** įveskite arba pažymėkite reikšmę.
11. Lauke **Mokėjimo dažnumas** įveskite mokėjimų skaičių, kurį tikitės apdoroti pagal šį įgaliojimą.
12. Spustelėkite **Gerai**.
13. Spustelėkite **Spausdinti**.
14. Spustelėkite **Įgaliojimo ataskaita**.
15. Uždarykite puslapį.
16. Spustelėkite **Redaguoti**.
17. Lauke **Parašo data** įveskite datą.
18. Spustelėkite **Taip**.
19. Įveskite vietą, kurioje buvo pasirašytas įgaliojimas.
20. Spustelėkite **Gerai**.
21. Uždarykite puslapį.

## <a name="create-a-free-text-invoice-with-mandate"></a>Kurti laisvos formos SF su įgaliojimu
1. **Naršymo sritis** eikite į **Moduliai > Gautinos sumos > Sąskaita-faktūra > Visos laisvos formos sąskaitos-faktūros**.
2. Spustelėkite **Naujas**.
3. Pasirinkite klientą, prie kurio pridėjote įgaliojimą.
4. Lauke **Tiesioginio debeto įgaliojimo ID** įveskite arba pažymėkite reikšmę.

