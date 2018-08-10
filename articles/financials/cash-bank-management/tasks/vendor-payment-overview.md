--- 
title: "Tiekėjo mokėjimų peržiūra"
description: "Šios užduoties vadovas žingsnis po žingsnio supažindins jus su įvairiais mokėjimų tiėkėjams kūrimo būdais, be kita ko – kaip naudoti mokėjimo pasiūlymą arba rankiniu būdu įvesti vienkartinį mokėjimą."
author: kweekley
manager: AnnBe
ms.date: 10/30/2017
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
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: e9a94231f755ff23bb442d62e90daff8f2d1f4fb
ms.contentlocale: lt-lt
ms.lasthandoff: 10/30/2017

---
# <a name="vendor-payment-overview"></a>Tiekėjo mokėjimų peržiūra

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šios užduoties vadovas žingsnis po žingsnio supažindins jus su įvairiais mokėjimų tiėkėjams kūrimo būdais, be kita ko – kaip naudoti mokėjimo pasiūlymą arba rankiniu būdu įvesti vienkartinį mokėjimą. Šioje procedūroje naudojama demonstracinė įmonė USMF.

1. Pasirinkite Mokėtinos sumos > Mokėjimai > Mokėjimų žurnalas.
2. Spustelėkite Naujas.
3. Pasirinkite mokėjimo žurnalą, kuriame norite įrašyti mokėjimus tiekėjams. 
4. Pasirinkite žurnalą arba įveskite jį rankiniu būdu.
5. Spustelėkite Eilutės.
6. Spustelėkite Mokėjimo pasiūlymas.
7. Spustelėkite Kurti mokėjimo pasiūlymą.
    * Mokėjimo pasiūlymas yra užklausa, naudojama pasirinkti SF apmokėjimui. Galite redaguoti mokėtinų sąskaitų faktūrų sąrašą prieš sukurdami ar atlikdami mokėjimus tiekėjams.  
8. Pasirinkite mokėtinas sąskaitas faktūras pagal galutinį terminą, mokėjimo nuolaidą arba abu. 
9. Įveskite datą palyginimui su galutiniu terminu arba mokėjimo nuolaidos data. 
10. Pasirinktinai: įveskite mokėjimo datą visiems mokėjimams.
    * Čia įvesta data bus visų sukurtų mokėjimų data, nepriklausomai nuo galutinio mokėjimo termino ar mokėjimo nuolaidos dienos.  
11. Pasirinktinai: įveskite minimalią mokėjimo datą, kuri gali būti naudojama kaip mokėjimo data.
    * Minimali mokėjimo data bus anksčiausia mokėjimų atlikimo data. Pvz., jei galutinis sąskaitos faktūros terminas yra vėlesnis nei minimali mokėjimo data, apmokėjimo data bus šis terminas, o ne minimali mokėjimo data, kad sąskaitą faktūrą būtų galima apmokėti vėliausiu įmanomu terminu.  
12. Įveskite papildomus užklausos filtrus įtraukiamų įrašų skiltyje.
    * Filtras dažnai naudojamas norint filtruoti apmokėjimui pasirinktas sąskaitas faktūras pagal tiekėjų grupę arba apmokėjimo būdą. Pvz., galite naudoti filtrą, kad šiame mokėjimo cikle sąskaitas faktūras apmokėtumėte tik čekiais.  
13. Įveskite papildomus užklausos filtrus arba mokėjimo numatytąsias vertes. 
    * Galima naudoti papildomus parametrus, apibrėžiančius mokėjimo valiutą arba suteikiančius galimybę per šį mokėjimo ciklą atlikti centralizuotus mokėjimus.  
14. Spustelėkite GERAI.
    * Spustelėjus „Gerai“, bus rodomi užklausos rezultatai. Jei nenorite peržiūrėti apmokėjimui pasirinktų sąskaitų faktūrų sąrašo, galite grįžti į gretąjį skirtuką „Parametrai“ ir pakeisti nustatymą „Kurti mokėjimus be sąskaitos faktūros peržiūros“ = Taip.  
15. Paspaudę mygtuką „Rodyti mokėjimų peržiūra“ peržiūrėkite mokėjimus, kurie bus sukurti pasirinktoje sąskaitoje faktūroje nurodytam tiekėjui.
16. Pasirinkę mygtuką „Slėpti mokėjimo peržiūrą paslėpsite mokėjimus. 
17. Spustelėkite Kurti mokėjimus.
    * Prieš pasirinkdami „Kurti mokėjimus“ galite spustelėti dešiniuoju pelės mygtuku ant tinklelio ir eksportuoti SF sąrašą į „Excel“. Mygtukas „Kurti mokėjimus“ sukurs mokėjimus tiekėjams mokėjimų žurnale.  
18. Patikrinkite savo mokėjimus ir įsitikinkite, kad visi mokėjimai turi nurodytą mokėjimo būdą. 
    * Generuojant mokėjimus, pvz., spausdinant čekį arba kuriant elektroninį mokėjimą, turi būti nurodytas mokėjimo būdas. Banko sąskaitą, iš kurios bus atliktas mokėjimas, mokėjimo būdas paskirs numatytąja.  
19. Spustelėkite „Naujas“, kad sukurtumėte vienkartinį mokėjimą.
    * Prieš registruojant vienkartinį mokėjimą jį galima bet kada įtraukti į mokėjimų žurnalą. Tai atliekama spustelėjus mygtuką Naujas ir rankiniu būdu įvedus mokėjimo informaciją, o ne naudojant mokėjimo pasiūlymą.  
20. Pasirinkite tiekėją, kuriam bus atliktas mokėjimas.
21. Jei mokėtina sąskaita faktūra parengta, pasirinkite „Sudengti operacijas“, kad šią sąskaitą faktūrą priskirtumėte apmokėjimui.
    * Jei tai yra išankstinis mokėjimas, šis veiksmas nebūtinas. Mokėjimą galite sukurti nepasirinkę jokios sąskaitos faktūros.  
22. Pažymėkite visas sąskaitas faktūras, kurios bus apmokėtos.
    * Jei mokėtinas sąskaitas faktūras pasirinksite per „Sudengti operacijas“, mokėjimo suma bus automatiškai apskaičiuota pagal jūsų pažymėtas mokėtinas sąskaitas faktūras ir pagal tai, kokią sumą įvedėte į „Sudengimo suma“.  
23. Spustelėkite GERAI.
24. Jei norite ištrinti mokėjimą, pažymėkite eilutę.
25. Spustelėkite Naikinti.
    * Mokėjimo ištrynimas ištrins tik mokėjimą. Visas pažymėtas mokėtinas sąskaitas faktūras vis tiek bus galima apmokėti kitu mokėjimu.  
26. Spustelėkite Taip.
27. Pasirinkite „Generuoti mokėjimą“, kad atspausdintumėte čekius arba sukurtumėte elektroninio mokėjimo failą.
28. Pasirinkite norimą generuoti mokėjimo būdą.
    * Mokėjimo žurnale gali būti ir mokėjimų čekiais, ir elektroninių mokėjimų, tačiau vienu kartu galite generuoti tik vieno tipo mokėjimą.  
29. Pasirinkite banko sąskaitą, iš kurios norite generuoti mokėjimus.
30. Spustelėkite GERAI.
    * Bus generuojami tik tie mokėjimai, kurie atitinka jūsų pasirinktą mokėjimo būdą ir banko sąskaitą.  
31. Jei generuojate čekius, pasirinkite dokumentą, kad užtikrintumėte teisingą čekių spausdinimo paskirties vietą.
32. Spustelėkite GERAI.
33. Spustelėkite „Gerai“, kad generuotumėte mokėjimus.
34. Spustelėkite „Registruoti“, jei visi mokėjimai patvirtinti ir sugeneruoti. 


