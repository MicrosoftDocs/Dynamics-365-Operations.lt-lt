---
title: Pagrindiniai SF duomenys mokėtinose sumose naudojant patvirtinimo žurnalą
description: Šioje temoje paaiškinama, kaip naudoti sąskaitų faktūrų registrą kuriant sąskaitas faktūras ir kaip paskui naudoti patvirtinimo žurnalą išlaidų sąskaitoms atnaujinti.
author: abruer
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d01c04fcf707109cd7bc6f056846506914e96dec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838890"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Pagrindiniai SF duomenys mokėtinose sumose naudojant patvirtinimo žurnalą

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinama, kaip naudoti sąskaitų faktūrų registrą kuriant sąskaitas faktūras ir kaip paskui naudoti patvirtinimo žurnalą išlaidų sąskaitoms atnaujinti.

## <a name="create-and-post-and-invoice"></a>Kurti ir registruoti SF
1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų registras**.
2. Pasirinkite **Naujas**.
3. Pasirinkite norimo naudoti SF registro pavadinimą.
4. Pasirinkę **Eilutės**, atidarykite registrą ir įveskite išlaidų eilutes.
5. Pasirinkite tiekėją. Pavyzdžiui, įveskite arba pasirinkite `US-104`.
6. Lauke **Sąskaita faktūra** įveskite reikšmę.
7. Lauke **Aprašo laukas** surinkite reikšmę.
8. Lauke **Kreditas** įveskite skaičių.
9. Lauke **Patvirtino** išplečiamajame meniu pasirinkite tvirtintoją.
10. Pasirinkite **Registruoti**.

## <a name="approve-an-invoice"></a>Tvirtinti SF
1. Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Sąskaitos faktūros > Sąskaitų faktūrų patvirtinimas**.
2. Pasirinkite **Naujas**.
3. Pasirinkite norimo naudoti SF tvirtinimo žurnalo pavadinimą.
4. Pasirinkite **Eilutės**, kad butų parodytas puslapis, kuriame galėsite pasirinkti norimas patvirtinti sąskaitas faktūras.
5. Pasirinkite **Rasti kvitus**, kad būtų parodytos visos sąskaitos faktūros, kurias galima tvirtinti.
6. Pažymėkite sukurtą sąskaitą faktūrą, tada spustelėkite **Pasirinkti**. Jums pasirinkus pirmiau pateiktus kvitus, jie perkeliami į šį sąrašą.  
7. Pasirinkite **Gerai**.
8. Pasirinkę lauką **kliento numeris**, į sąskaitą faktūrą įtraukite išlaidų sąskaitą.
9. Įveskite sąskaitos numerį ir pereikite iš lauko. Pavyzdžiui, įveskite `600120`.
10. Pasirinkite **Registruoti**.
11. Pasirinkę **Kvitas**, pamatysite užregistruotus įrašus. Patvirtinimo laukiančių SF sąskaita atšaukiama ir pakeičiama faktine išlaidų sąskaita.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]