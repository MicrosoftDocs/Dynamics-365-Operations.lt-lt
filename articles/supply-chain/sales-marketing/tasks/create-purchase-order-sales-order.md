--- 
title: "Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą"
description: "Ši procedūra nurodo, kaip kurti pirkimo užsakymą, pagrįstą pardavimo užsakymu."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 412a8c7acca06fc1be073019f91144e2a3f1c94b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip kurti pirkimo užsakymą, pagrįstą pardavimo užsakymu. Produkto pirkimo užsakymo kiekiai tada nurodomi norint patenkinti pradinio pardavimo užsakymo poreikį. Pardavimo poreikio vykdymas tokiu būdu yra išsamesnio ir optimizuoto metodo Platinimo poreikio planavimas alternatyva. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Pirkimo užsakymo kūrimas naudojant pardavimo užsakymą
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Spustelėkite Gerai.
6. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite ir pasirinkite norimą įrašą.
    * Jei naudojate USMF, galite pasirinkti D0001.  
8. Lauke Kiekis įveskite skaičių.
9. Spustelėkite Pridėti eilutę.
10. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše raskite ir pasirinkite norimą įrašą.
    * Jei naudojate USMF, galite pasirinkti T0020.  
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13. Lauke Kiekis įveskite skaičių.
14. Spustelėkite Įrašyti.
15. Veiksmų srityje spustelėkite Pardavimo užsakymas.
16. Spustelėkite Pirkimo užsakymas.
    * Puslapyje Kurti pirkimo pristatymą pateikiamos visos atvirų pardavimo užsakymų eilutės, kurios buvo nukopijuotos iš pardavimo užsakymo. Galite peržiūrėti užsakymo informaciją ir, jei reikia, galite modifikuoti pasirinktą informaciją, pvz., pirkimo kiekį ir kainų nustatymo sąlygas, prieš kurdami pirkimus.  
17. Pasirinkite pasirinktį Įtraukti viską.
    * Jei pirkimo užsakymą norite sugeneruoti tik pardavimo užsakymo eilučių pogrupiui, pažymėkite jas atskirai.  
    * Lauke Tiekėjo sąskaita gali būti įvestas arba dar nebūti įvestas tiekėjo numeris. Jei yra nustatytas produkto numatytasis tiekėjas (susietame Prekės padengime), šis tiekėjas bus nukopijuotas į eilutę. Priešingu atveju, tiekėją turite įvesti rankiniu būdu.  Šiame vadove, nepriklausomai nuo to, ar Tiekėjo sąskaitos lauke jau yra vertė ar ne, tolesni veiksmai nurodo, kaip pasirinkti naują tiekėją, kuris skiriasi kiekvienoje eilutėje.  
18. Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
19. Sąraše raskite ir pasirinkite norimą įrašą.
20. Sąraše spustelėkite saitą pasirinktoje eilutėje.
21. Pasirinkite antrąją užsakymo eilutę.
22. Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
23. Sąraše raskite ir pasirinkite norimą įrašą.
24. Sąraše spustelėkite saitą pasirinktoje eilutėje.
25. Spustelėkite Tikrinti.
26. Spustelėkite GERAI.
    * Pranešimas informuoja, kad sukurtas vienas ar daugiau pirkimo užsakymų. Kiekvienam tiekėjui, kurį nurodėte pardavimo užsakymo eilutėse, sistema sukuria po atskirą pirkimo užsakymą. Tai reiškia, kad jei tas pats tiekėjas nurodytas keliose pardavimo užsakymo eilutėse, bus sugeneruotas vienas pirkimo užsakymą su keliomis eilutėmis.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Peržiūrėti pirkimo užsakymus, sukurtus pagal pardavimo užsakymus
1. Veiksmų srityje spustelėkite Bendra.
2. Spustelėkite Susiję užsakymai.
    * Puslapyje Susiję užsakymai pateikiami visi užsakymai, sukurti iš pardavimo užsakymo. Šiame pavyzdyje yra du pirkimo užsakymai, sugeneruoti atitinkamai dviem skirtingiems tiekėjams.  
3. Spustelėkite, jei norite atidaryti lauke Pirkimo užsakymas esantį saitą.
    * Kiekviena pirkimo užsakymo eilutė susieta su pardavimo užsakymo eilute, dėl kurios buvo sukurtas pirkimas. Ryšys su pardavimo užsakymu nurodytas skirtuke Produktas, esančiame Eilutės informacijos „FastTab“, laukuose Nuorodos tipas, Nuorodos numeris ir Nuoroda į partiją.  
4. Išplėskite arba sutraukite dalį Išsami eilučių informacija.
5. Spustelėkite skirtuką Produktas.
    * Nuoroda į partiją užtikrina, kad esamo pirkimo išlaidos bus įtrauktos į pridėtą pardavimo užsakymą.  
    * Atidarę saitą lauke Nuorodos numeris, galite pereiti į pradinį pardavimo užsakymą.  


