---
title: Pardavimo užsakymų siuntimas be sandėliavimo
description: Šiame straipsnyje paaiškinama, kaip atnaujinti pardavimo užsakymą, kai produktai siunčiami klientui.
author: Henrikan
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3478e8c712c7bcbfb8ace9e7b43f0d8d3cf4ac8a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069159"
---
# <a name="ship-sales-orders-without-warehousing"></a>Pardavimo užsakymų siuntimas be sandėliavimo

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip atnaujinti pardavimo užsakymą, kai produktai siunčiami klientui. Vadovas taikomas įvykdymo srautui, kuris nėra nustatytas sandėlio valdymui (nei pagrindiniu, nei sandėlio valdymo procesams (WMS)),todėl nereikalaujama, kad produktų paėmimas prieš siuntimą būtų registruojamas. Šią procedūrą galite vykdyti su savo duomenimis arba demonstracinėje duomenų įmonėje USMF. Abiem atvejais, prieš pradėdami šią užduotį, sukurkite inventorizuoto produkto, kurio kiekis didesnis negu 1, pardavimo užsakymą. Norėdami išvengti registravimo klaidos, turite patikrinti, ar jūsų užsakytas prekių kiekis svetainėje ir sandėlyje atitinka užsakymo kiekį.

## <a name="post-packing-slip-for-an-order"></a>Užsakymo važtaraščio registravimas
1. Naršymo srityje eikite į **Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
2. Sąraše raskite ir pasirinkite šiai užduočiai sukurtą užsakymą.
3. Veiksmų srityje pasirinkite **Paimti ir pakuoti**.
4. Pasirinkite **Registruoti važtaraštį**.
5. Išplėskite arba sutraukite skyrių **Parametrai**.
6. Lauke **Kiekis** pasirinkite **Visi**.
    - Kitos parinktys – **Pristatyti dabar** ir **Paimta**. Jei užsakymo eilutė turi būti siunčiama iš dalies, o užsakymo eilutės lauke **Pristatyti dabar** nurodytas kiekis, pasirinktumėte **Pristatyti dabar**. Jei jūsų organizacijos vykdymo eiga kaip atskirą procesą apima išrinkimą, kuris valdomas ir registruojamas naudojant išrinkimo sąrašą, reikia pasirinkti **Paimta**.  
    - Patikrinkite, ar nustatyta parinkties **Registravimas** nuostata **Taip**.  
7. Nustatykite parinkties **Spausdinti važtaraštį** nuostatą **Taip**. Skirtuke **Apžvalga** pateiktas važtaraščių, kurie bus sugeneruoti šiame registravime, sąrašas. Jei siunčiate individualų užsakymą, paprastai būna vienas važtaraštis. Tačiau jei to užsakymo eilutės turi būti siunčiamos iš skirtingų vietų, registravimas bus automatiškai padalintas į atitinkamą skaičių dokumentų. Tai būtina sąlyga, kurios negalima keisti. Jei užsakymo eilutės bus siunčiamos skirtingais pristatymo adresais, o siuntimo strategijoje nustatyta, kad juos reikia padalyti, registravimas taip pat bus padalintas į kelis dokumentus panašiu būdu.  
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