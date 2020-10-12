---
title: Pardavimo komisinių registravimas
description: Šioje temoje paaiškinta, kaip apskaičiuojami ir registruojami pardavimo komisiniai.
author: omulvad
manager: tfehr
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83cea952f4883d49621a9f7d16440927a8eddb98
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830566"
---
# <a name="register-sales-commissions"></a>Pardavimo komisinių registravimas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinta, kaip apskaičiuojami ir registruojami pardavimo komisiniai. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Prieš paleisdami šį vadovą, paleiskite vadovą pavadinimu „Pardavimo komisinių taisyklių nustatymas“, kad įsitikintumėte, jog turite visus reikalingus komisinių skaičiavimo nustatymus.

Atkreipkite dėmesį į savo pasirinktus komisinių proceso kliento ir prekės numerius ir naudokite juos, kai šiame vadove jūsų bus paprašyta sukurti pardavimo užsakymą.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Pardavimo užsakymo, suteikiančio pardavėjui teisę gauti komisinius, sąskaitos faktūros išrašymas
1. Naršymo srityje eikite į **Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento sąskaita** išplečiamajame meniu pasirinkite norimą įrašą.
4. Pasirinkite **Gerai**.
5. Veiksmų srityje pasirinkite**Parinktys**.
6. Pasirinkite **Keisti rodinį**.
7. Pasirinkite **Antraštės rodinys**.
8. Išplėskite skyrių **Sąranka**.

    - Lauko **Pardavimo grupė** reikšmė nurodo grupę, kuriai priskirtas vienas arba daugiau pardavimo atstovų. Grupėje esantys žmonės išrašius užsakymo sąskaitą faktūrą gaus komisinius pagal iš anksto nustatytus tarifus ir paskirstymą.   
    - Reikšmė kopijuojama iš dalies Kliento kortelė, tačiau, jei norite, galite ją pakeisti.  
    - Pardavimo grupė taip pat nukopijuojama į pardavimo užsakymo eilutę. Galite ją pakeisti, kad ji skirtųsi nuo antraštėje ir (arba) tarp eilučių nurodytos grupės.  
    - Lauko **Komisinių grupė** reikšmė nurodo grupę, kurią sukūrėte dėl vieno arba daugiau klientų, kad galėtumėte sekti komisinius.   
    - Reikšmė kopijuojama iš dalies Kliento kortelė, tačiau, jei norite, galite ją pakeisti.   

9. Veiksmų srityje pasirinkite**Parinktys**.
10. Pasirinkite **Keisti rodinį**.
11. Pasirinkite **Eilutės rodinys**.
12. Lauko **Prekės numeris** išplečiamajame meniu pasirinkite prekę, kurios komisinius nustatėte. 
13. Lauke **Kiekis** įveskite skaičių. Atkreipkite dėmesį į eilutės dalį Grynoji suma. Joje nurodomos pardavimo įplaukos, kurios, šiuo atveju, yra komisinių skaičiavimo pagrindas.  
14. Pasirinkite **Įrašyti**.
15. Veiksmų srityje pasirinkite **Sąskaita faktūra**.
16. Pasirinkite **Sąskaita faktūra**.
17. Išplėskite skyrių **Parametrai**.
18. Lauke **Kiekis** pasirinkite **Visi**.
19. Lauke **Registravimas** pasirinkite **Taip**.
20. Pasirinkite **Gerai**, tada kitoje srityje – **Gerai**. Operacijos registravimas gali užtrukti apie minutę. Neuždarykite puslapio, kol procesas nesibaigs.  

## <a name="review-the-registered-sales-commissions"></a>Registruotų pardavimo komisinių peržiūra
1. Veiksmų srityje pasirinkite **Sąskaita faktūra**, o tada vėl pasirinkite **Sąskaita faktūra**.
2. Veiksmų srityje pasirinkite **Sąskaita faktūra**, tada pasirinkite **Komisinių operacijos**.

    - Skirtuke **Apžvalga** rodomos eilutės, nurodančios pardavimo atstovams, susietiems su pardavimo užsakymu, už kurį išrašyta sąskaita faktūra, mokėtinas komisinių sumas. Peržiūrėkime išsamią informaciją.  
    - Jei naudojote vadovą „Pardavimo komisinių taisyklių nustatymas“ **Pardavimo komisinių** grupei nustatyti, yra du pardavėjai, kurie gaus pardavimo komisinius, ir komisiniai abiems pardavėjams padalijami po lygiai.  
    - Šiame pavyzdyje komisinių suma apskaičiuojama kaip pardavimo įplaukų procentinė dalis (užsakymo eilutės grynoji suma).  
3. Uždarykite puslapį.
4. Pasirinkite **Kvitas**. Galite peržiūrėti komisinių sumų, kurios užregistruotos iš anksto numatytų komisinių išlaidų ir mokėtinų komisinių sąskaitose, kvitų operacijas.  

