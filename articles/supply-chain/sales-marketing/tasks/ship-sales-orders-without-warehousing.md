--- 
title: "Siųsti pardavimo užsakymus be sandėliavimo"
description: "Šiame vadove parodoma, kaip naujinti pardavimo užsakymą, kai produktai siunčiami klientui."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3f1b9dd4b99bcbcc6cfbc5cfd8e3271fa80c628c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="ship-sales-orders-without-warehousing"></a>Siųsti pardavimo užsakymus be sandėliavimo

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šiame vadove parodoma, kaip naujinti pardavimo užsakymą, kai produktai siunčiami klientui. Vadovas taikomas vykdymo eigai, kuri nenustatyta sandėlio valdymui (nei pagrindiniam, nei papildomam sandėliui), ir todėl prieš siunčiant nereikia užregistruoti produkto išrinkimo. Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF. Abiem atvejais, prieš pradėdami šią užduotį, sukurkite inventorizuoto produkto, kurio kiekis didesnis negu 1, pardavimo užsakymą. Norėdami išvengti registravimo klaidos, turite patikrinti, ar šiuo metu užsakyme pasirinktoje vietoje ir sandėlyje turimo produkto kiekis sutampa su užsakymo kiekiu.


## <a name="post-packing-slip-for-an-order"></a>Užsakymo važtaraščio registravimas
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
2. Sąraše raskite ir pasirinkite šiai užduočiai sukurtą užsakymą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Veiksmų srityje spustelėkite Paimti ir pakuoti.
5. Spustelėkite Registruoti važtaraštį.
6. Išplėskite arba sutraukite skyrių Parametrai.
7. Lauke Kiekis pasirinkite Visi.
    * Kitos pasirinktys yra Pristatyti dabar arba Išrinkta. Jei užsakymo eilutė siunčiama iš dalies, o užsakymo eilutės lauke Pristatyti dabar nurodytas kiekis, pasirinkite Pristatyti dabar. Jei jūsų organizacijos vykdymo eigoje išrinkimas nurodytas kaip atskiras procesas, kuris valdomas ir registruojamas naudojant išrinkimo dokumentą, pasirinkite Išrinkta.  
    * Patikrinkite, ar nustatyta parinkties Registravimas padėtis Taip.  
8. Nustatykite pasirinkties Važtaraščio spausdinimas padėtį Taip.
    * Skirtuke Peržiūra yra atliekant šį registravimą turimų sugeneruoti važtaraščių sąrašas. Jei siunčiate individualų užsakymą, paprastai būna vienas važtaraštis. Tačiau jei to užsakymo eilutės turi būti siunčiamos iš skirtingų vietų, registravimas bus automatiškai padalintas į atitinkamą skaičių dokumentų. Tai būtina sąlyga, kurios negalima keisti. Be to, jei užsakymo eilutės turi būti siunčiamos skirtingais pristatymo adresais, o siuntimo strategijoje nustatyta, kad būtų reikalaujama padalinimo, registravimas bus taip pat padalintas į keletą dokumentų.  
9. Skirtuke Eilutės pasirinkite siunčiamos užsakymo eilutės eilutę.
10. Lauke Atnaujinti įveskite už pradinio kiekio skaičių mažesnį skaičių.
11. Spustelėkite GERAI.
12. Spustelėkite Taip.
13. Uždarykite puslapį.
14. Veiksmų srityje spustelėkite Parinktys.
15. Spustelėkite Keisti rodinį.
16. Spustelėkite antraštės rodinį.
    * Jei visos užsakymo eilutės buvo visiškai išsiųstos, užsakymo būsena pasikeičia iš Atvira į Pristatyta.  
    * Šiame pavyzdyje užsakymo eilutė išsiųsta iš dalies. Todėl užsakymo būsena išlieka Atidarytas.     
    * Nustatyta lauko Dokumento būsena padėtis Važtaraštis, nes išsiųsta bent viena užsakymo eilutė.  
17. Veiksmų srityje spustelėkite Bendra.
18. Spustelėkite Eilutės kiekis.
19. Uždarykite puslapį.
20. Veiksmų srityje spustelėkite Paimti ir pakuoti.
21. Spustelėkite Važtaraštis.
    * Puslapyje Važtaraščio žurnalas pateikiami visi jūsų užsakymui sugeneruoti važtaraščio dokumentai. Galite peržiūrėti kiekvieno dokumento informaciją ir, jei norite, ją atsispausdinti.  


