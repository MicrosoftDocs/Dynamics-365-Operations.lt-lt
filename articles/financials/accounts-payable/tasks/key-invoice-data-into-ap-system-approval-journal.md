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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837049"
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

