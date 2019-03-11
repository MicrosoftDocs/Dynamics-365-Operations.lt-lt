---
title: Registruoti pardavimo komisinius
description: Ši procedūra nurodo, kaip apskaičiuojami ir registruojami pardavimo komisiniai.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c39b2fcf521106dfb58466bc45a316c0b506345
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "355155"
---
# <a name="register-sales-commissions"></a>Registruoti pardavimo komisinius

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip apskaičiuojami ir registruojami pardavimo komisiniai. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Prieš paleisdami šį vadovą, paleiskite vadovą pavadinimu „Pardavimo komisinių taisyklių nustatymas“, kad įsitikintumėte, jog turite visus reikalingus komisinių skaičiavimo nustatymus.

Atkreipkite dėmesį į savo pasirinktus komisinių proceso kliento ir prekės numerius ir naudokite juos, kai šiame vadove jūsų bus paprašyta sukurti pardavimo užsakymą.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Pardavimo užsakymo, suteikiančio pardavėjui teisę gauti komisinius, sąskaitos faktūros išrašymas
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite GERAI.
7. Veiksmų srityje spustelėkite Parinktys.
8. Spustelėkite Keisti rodinį.
9. Spustelėkite antraštės rodinį.
10. Išplėskite skyrių Nustatymas.
    * Lauko Pardavimo grupė reikšmė nurodo grupę, kuriai priskirtas vienas ar keli pardavimo atstovai. Grupėje esantys žmonės išrašius užsakymo sąskaitą faktūrą gaus komisinius pagal iš anksto nustatytus tarifus ir paskirstymą.   Reikšmė kopijuojama iš dalies Kliento kortelė, tačiau, jei norite, galite ją pakeisti.  Pardavimo grupė taip pat nukopijuojama į pardavimo užsakymo eilutę. Galite ją pakeisti, kad ji skirtųsi nuo antraštėje ir (arba) tarp eilučių nurodytos grupės.  
    * Lauko Komisinių grupė reikšmė nurodo grupę, kurią sukūrėte vienam ar keliems klientams norėdami sekti komisinius.   Reikšmė kopijuojama iš dalies Kliento kortelė, tačiau, jei norite, galite ją pakeisti.   
11. Veiksmų srityje spustelėkite Parinktys.
12. Spustelėkite Keisti rodinį.
13. Spustelėkite Eilutės rodinys.
14. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
15. Sąraše pasirinkite nustatytą komisinių prekę. 
16. Lauke Kiekis įveskite skaičių.
    * Atkreipkite dėmesį į eilutės dalį Grynoji suma. Joje nurodomos pardavimo įplaukos, kurios, šiuo atveju, yra komisinių skaičiavimo pagrindas.  
17. Spustelėkite Įrašyti.
18. Veiksmų srityje spustelėkite Sąskaita faktūra.
19. Spustelėkite Sąskaita faktūra.
20. Išplėskite skyrių Parametrai.
21. Lauke Kiekis pasirinkite Visi.
22. Lauke Registravimas pasirinkite Taip.
23. Spustelėkite GERAI.
24. Spustelėkite GERAI.
    * Operacijos registravimas gali užtrukti apie minutę. Palaukite, kol apdorojimas baigsis ir neuždarykite puslapio.  

## <a name="review-the-registered-sales-commissions"></a>Registruotų pardavimo komisinių peržiūra
1. Veiksmų srityje spustelėkite Sąskaita faktūra.
2. Spustelėkite Sąskaita faktūra.
3. Veiksmų srityje spustelėkite Sąskaita faktūra.
4. Spustelėkite Komisinių operacijos.
    * Skirtuke Peržiūra rodomos eilutės, kuriose nurodomos su sąskaitą faktūrą turinčiu pardavimo užsakymu susietiems pardavimo atstovams mokėtinos komisinių sumos. Peržiūrėkime išsamią informaciją.     
    * Jei nustatydami komisinių pardavimo grupę naudojote vadovą „Pardavimo komisinių taisyklių nustatymas“, pardavimo komisinius gali gauti du pardavėjai ir komisiniai padalinami jiems po lygiai.  
    * Šiame pavyzdyje komisinių suma apskaičiuojama kaip pardavimo įplaukų procentinė dalis (užsakymo eilutės grynoji suma).   
5. Uždarykite puslapį.
6. Spustelėkite Kvitas.
    * Galite peržiūrėti komisinių sumų, kurios užregistruotos iš anksto numatytų komisinių išlaidų ir mokėtinų komisinių sąskaitose, kvitų operacijas.  

