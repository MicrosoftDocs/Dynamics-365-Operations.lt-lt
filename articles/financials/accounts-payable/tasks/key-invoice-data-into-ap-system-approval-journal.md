---
title: Pagrindiniai SF duomenys AP sistemoje naudojant tvirtinimo žurnalą
description: Šis užduočių vadovas parodys, kaip naudojant SF registrą kurti SF ir tada, naudojant patvirtinimo žurnalą, atnaujinti išlaidų sąskaitas.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550379"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Pagrindiniai SF duomenys AP sistemoje naudojant tvirtinimo žurnalą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas parodys, kaip naudojant SF registrą kurti SF ir tada, naudojant patvirtinimo žurnalą, atnaujinti išlaidų sąskaitas.


## <a name="create-and-post-and-invoice"></a>Kurti ir registruoti SF
1. Pasirinkite Mokėtinos sumos > Sąskaitos faktūros > SF registras.
2. Spustelėkite Naujas.
3. Pasirinkite norimo naudoti SF registro pavadinimą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Spustelėdami Eilutės atidarykite registrą ir įveskite išlaidų eilutes.
6. Pasirinkite tiekėją. Pavyzdžiui, įveskite arba pasirinkite US-104
7. Lauke Sąskaita faktūra surinkite reikšmę.
8. Lauke Aprašas surinkite reikšmę.
9. Lauke Kreditas įveskite skaičių.
10. Lauke Patvirtino spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Pažymėkite tvirtintoją ir spustelėkite Pasirinkti, kad tą tvirtintoją pasirinktumėte.
12. Spustelėkite Registruoti.
13. Uždarykite puslapį.
14. Uždarykite puslapį.

## <a name="approve-an-invoice"></a>Tvirtinti SF
1. Pasirinkite Mokėtinos sumos > Sąskaitos faktūros > SF tvirtinimas.
2. Spustelėkite Naujas.
3. Pasirinkite norimo naudoti SF tvirtinimo žurnalo pavadinimą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Spustelėjus eilutes, bus rodomas puslapis, kuriame galėsite pasirinkti SF, kurias norite patvirtinti.
6. Pasirinkus Rasti kvitus, bus rodomos visos SF, kurias galima tvirtinti.
7. Pažymėkite savo sukurtą sąskaitą faktūrą.
8. Spustelėkite Pažymėti.
    * Jums pasirinkus pirmiau pateiktus kvitus, jie perkeliami į šį sąrašą.  
9. Spustelėkite GERAI.
10. Spustelėkite ant sąskaitos numerio lauko, kad į SF įtrauktumėte išlaidų sąskaitą.
11. Įveskite sąskaitos numerį ir pereikite iš lauko. Pavyzdžiui, įveskite 600120.
12. Spustelėkite Registruoti.
13. Spustelėkite Kvitas, kad peržiūrėtumėte visus registruotus įrašus.
    * Patvirtinimo laukiančių SF sąskaita atšaukiama ir pakeičiama faktine išlaidų sąskaita.  

