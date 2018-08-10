--- 
title: "Eksportuoti akredityvą"
description: "Ši procedūra padeda eksportuoti akredityvą."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 0fa4b57825bcf81778d91ee01484511bb40f6bd7
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="export-a-letter-of-credit"></a>Eksportuoti akredityvą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padeda eksportuoti akredityvą.

Akredityvas yra banko išduota sutartis, pagal kurią bankas sutinka užtikrinti mokėjimą pirkėjo vardu, jei sutarties tarp pirkėjo ir pardavėjo sąlygos yra patenkinamos.



Prieš šią procedūrą atlikite procedūras „Banko priemonių ir registravimo šablonų nustatymas“ ir „Akredityvo banko priemonės sutarties kūrimas“. Reikia pasirinkti demonstracinę įmonę USMF, kad būtų galima sėkmingai atlikti šią procedūrą.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Kurti eksporto akredityvo pardavimo užsakymą
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Išplėskite arba sutraukite dalį Bendra.
7. Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite teritoriją, kurioje saugoma išduotina prekė.  
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite sandėlį, kuriame saugoma išduotina prekė.  
10. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pastaba: turi būti pasirinkta lauko Banko dokumento tipas reikšmė „Akredityvas“.  
11. Lauke Banko dokumento tipas pasirinkite „Akredityvas“.
12. Išplėskite arba sutraukite sekciją Pristatymas.
    * Pasirinkite Pristatymo datos valdymas = Nėra.  
13. Lauke Pageidaujama gavimo data įveskite datą.
14. Spustelėkite GERAI.
15. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Pasirinkite prekę, kurią reikia išduoti / parduoti.  
16. Sąraše raskite ir pasirinkite norimą įrašą.
17. Sąraše spustelėkite saitą pasirinktoje eilutėje.
18. Lauke Vieneto kaina įveskite skaičių.
19. Išplėskite arba sutraukite dalį Išsami eilučių informacija.
20. Spustelėkite skirtuką Pristatymas.
21. Lauke Pageidaujama siuntimo data įveskite datą.
22. Lauke Patvirtinta siuntimo data įveskite datą.
23. Veiksmų srityje spustelėkite Valdyti.
24. Spustelėkite Akredityvas.
25. Lauke Banko dokumento numeris įveskite reikšmę.
26. Lauke Galiojimo data įveskite datą ir laiką.
27. Išplėskite arba sutraukite sekciją Banko informacija.
28. Lauke Išduodantis bankas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
29. Sąraše spustelėkite saitą pasirinktoje eilutėje.
30. Lauke Konsultavimo bankas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
31. Sąraše raskite ir pasirinkite norimą įrašą.
32. Sąraše spustelėkite saitą pasirinktoje eilutėje.
33. Spustelėkite Surasti pardavimo užsakymo siuntas.
34. Spustelėkite Išduodančio banko dokumentas.
35. Uždarykite puslapį.

## <a name="post-packing-slip"></a>Registruoti važtaraštį
1. Veiksmų srityje spustelėkite Paimti ir pakuoti.
2. Spustelėkite Registruoti važtaraštį.
3. Išplėskite arba sutraukite skyrių Parametrai.
4. Lauke Kiekis pasirinkite „Visi‟.
5. Išplėskite arba sutraukite sekciją Sąranka.
6. Lauke Važtaraščio data įveskite datą.
7. Pasirinkite siuntos numerį.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Spustelėkite GERAI.
10. Spustelėkite GERAI.

## <a name="post-sales-invoice"></a>Registruoti pardavimo SF
1. Veiksmų srityje spustelėkite Sąskaita faktūra.
2. Spustelėkite Sąskaita faktūra.
3. Išplėskite arba sutraukite sekciją Peržiūra.
4. Pasirinkite siuntos numerį.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Išplėskite arba sutraukite sekciją Sąranka.
7. Įveskite datą lauke Sąskaitos faktūros data.
8. Spustelėkite GERAI.
9. Spustelėkite GERAI.

## <a name="shipment-document-submitted-status"></a>Pateikto siuntos dokumento būsena
1. Veiksmų srityje spustelėkite Valdyti.
2. Spustelėkite Akredityvas.
3. Išplėskite arba sutraukite sekciją Eilutės.
    * Pastaba: lauko „Dokumentas pateiktas“ reikšmė turi būti nustatyta kaip „Taip“.  

## <a name="verify-export-letter-of-credit"></a>Tikrinti eksporto akredityvą
1. Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Eksportuoti akredityvą ir importuoti rinkinį.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite, ar eksporto akredityvo siuntos būsena yra „SF išrašyta“.  

## <a name="customer-payment"></a>Kliento mokėjimas
1. Pasirinkite Gautinos sumos > Mokėjimai > Mokėjimų žurnalas.
2. Spustelėkite Naujas.
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite Eilutės.
7. Lauke Data įveskite datą.
8. Lauke Sąskaita nustatykite norimas reikšmes.
9. Spustelėkite Atsiskaitymas.
10. Antraštėje Bendrosios sumos pažymėkite žymės langelį.
    * Pastaba: nustatykite lauko Rodyti reikšmę kaip „Akredityvas“.  
11. Sąraše raskite ir pasirinkite norimą įrašą.
12. Pažymėkite arba išvalykite žymės langelį Žymėti.
13. Spustelėkite GERAI.
14. Spustelėkite skirtuką Mokėjimas.
    * Tikrinti banko dokumento numerio ir siuntos numerio informaciją  
15. Spustelėkite Registruoti.

## <a name="verify-export-letter-of-credit-after-payment"></a>Tikrinti eksporto akredityvą po apmokėjimo
1. Eikite į Grynųjų pinigų ir banko valdymas > Akredityvai > Eksportuoti akredityvą ir importuoti rinkinį.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Patikrinkite, ar siuntos būsena = mokėjimas gautas, o balanso suma = 0,00.  


