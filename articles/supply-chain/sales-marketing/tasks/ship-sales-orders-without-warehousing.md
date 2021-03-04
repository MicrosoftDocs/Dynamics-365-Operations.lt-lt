---
title: Pardavimo užsakymų siuntimas be sandėliavimo
description: Šioje temoje paaiškinta, kaip atnaujinti pardavimo užsakymą, kai produktai siunčiami klientui.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6b1dbb4d53785c226f7c9d40339d9dd19f47152
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433870"
---
# <a name="ship-sales-orders-without-warehousing"></a>Pardavimo užsakymų siuntimas be sandėliavimo

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinta, kaip atnaujinti pardavimo užsakymą, kai produktai siunčiami klientui. Vadovas taikomas vykdymo eigai, kuri nenustatyta sandėlio valdymui (nei pagrindiniam, nei papildomam sandėliui), ir todėl prieš siunčiant nereikia užregistruoti produkto išrinkimo. Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF. Abiem atvejais, prieš pradėdami šią užduotį, sukurkite inventorizuoto produkto, kurio kiekis didesnis negu 1, pardavimo užsakymą. Norėdami išvengti registravimo klaidos, turite patikrinti, ar jūsų užsakytas prekių kiekis svetainėje ir sandėlyje atitinka užsakymo kiekį.

## <a name="post-packing-slip-for-an-order"></a>Užsakymo važtaraščio registravimas
1. Naršymo srityje eikite į **Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
2. Sąraše raskite ir pasirinkite šiai užduočiai sukurtą užsakymą.
3. Veiksmų srityje pasirinkite **Paimti ir pakuoti**.
4. Pasirinkite **Registruoti važtaraštį**.
5. Išplėskite arba sutraukite skyrių **Parametrai**.
6. Lauke **Kiekis** pasirinkite **Visi**.
    - Kitos parinktys – **Pristatyti dabar** ir **Paimta**. Jei užsakymo eilutė turi būti siunčiama iš dalies, o užsakymo eilutės lauke **Pristatyti dabar** nurodytas kiekis, pasirinktumėte **Pristatyti dabar**. Jei jūsų organizacijos vykdymo eiga kaip atskirą procesą apima išrinkimą, kuris valdomas ir registruojamas naudojant išrinkimo sąrašą, reikia pasirinkti **Paimta**.  
    - Patikrinkite, ar nustatyta parinkties **Registravimas** nuostata **Taip**.  
7. Nustatykite parinkties **Spausdinti važtaraštį** nuostatą **Taip**.  Skirtuke **Apžvalga** pateiktas važtaraščių, kurie bus sugeneruoti šiame registravime, sąrašas. Jei siunčiate individualų užsakymą, paprastai būna vienas važtaraštis. Tačiau jei to užsakymo eilutės turi būti siunčiamos iš skirtingų vietų, registravimas bus automatiškai padalintas į atitinkamą skaičių dokumentų. Tai būtina sąlyga, kurios negalima keisti. Jei užsakymo eilutės bus siunčiamos skirtingais pristatymo adresais, o siuntimo strategijoje nustatyta, kad juos reikia padalyti, registravimas taip pat bus padalintas į kelis dokumentus panašiu būdu.  
8. Skirtuke **Eilutės** pasirinkite užsakymo eilutės, kurią reikia išsiųsti, eilutę.
9. Lauke **Naujinimas** įveskite skaičių, kuris yra mažesnis nei pradinis kiekis.
10. Pasirinkite **Gerai**.
11. Pasirinkite **Taip**.
12. Uždarykite puslapį.
13. Veiksmų srityje pasirinkite **Parinktys**.
14. Pasirinkite **Keisti rodinį**.
15. Pasirinkite **Antraštės rodinys**.
    - Jei visos užsakymo eilutės buvo visiškai išsiųstos, užsakymo būsena pasikeičia iš Atvira į Pristatyta.  
    - Šiame pavyzdyje užsakymo eilutė išsiųsta iš dalies. Todėl užsakymo būsena išlieka Atidarytas.     
    - Lauke **Dokumento būsena** nustatyta reikšmė Važtaraštis, nes bent viena iš užsakymo eilučių buvo išsiųsta.  
16. Veiksmų srityje spustelėkite **Bendra**.
17. Pasirinkite **Eilutės kiekis**.
18. Uždarykite puslapį.
19. Veiksmų srityje pasirinkite **Paimti ir pakuoti**.
20. Pasirinkite **Važtaraštis**. Puslapyje **Važtaraščio žurnalas** pateikti visi pagal jūsų užsakymą sugeneruoti važtaraščio dokumentai. Galite peržiūrėti kiekvieno dokumento informaciją ir, jei norite, ją atsispausdinti.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]