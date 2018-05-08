---
title: "Nustatyti kokybės užsakymus"
description: "Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 73981313fc662094ee4f8bb15a88271e16d41193
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-quality-orders"></a>Nustatyti kokybės užsakymus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra parodo, kaip įgalinti kokybės valdymo procesą, kai gaunamas atsargas reikia tikrinti iš karto po pristatymo registracijos. Procedūrą paprastai atlieka kokybės vadovas. Šis procesas apima kokybės grupės kūrimą apibrėžti prekėms, iš kurių bus imami pavyzdžiai, ir bandymo grupės kūrimą grupuoti bandymams, kuriuos reikia atlikti su prekėmis kokybės grupėje. Šį vedlį galite vykdyti demonstracinių duomenų įmonėje USMF.


## <a name="enable-quality-management"></a>Kokybės valdymo įgalinimas
1. Pasirinkite Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai.
2. Spustelėkite skirtuką Kokybės valdymas.
3. Nustatykite parinkčiai Naudoti kokybės valdymą reikšmę Taip.
4. Spustelėkite Ataskaitų sąranka.
    * USMF kokybės valdymo ataskaitos sąranka jau yra nurodyta. Jei tai buvo atlikta, čia galite įtraukti naujas skirtingų ataskaitų tipų eilutes ir pasirinkti kiekvienos ataskaitos dokumento tipą.  
5. Uždarykite puslapį.
6. Uždarykite puslapį.

## <a name="create-a-test"></a>Kurti bandymą
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymai.
2. Spustelėkite Naujas.
3. Lauke Bandymas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Tipas pasirinkite „Parinktis‟.
    * Šiame pavyzdyje pasirinksime „Parinktis‟ – bus galima priskirti tikrinimo rezultatus pagal iš anksto apibrėžtas reikšmes.  
6. Spustelėkite Įrašyti.
7. Uždarykite puslapį.

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a>Kurti bandymų kintamuosius, kad būtų galima apibrėžti, kaip įrašomi bandymų rezultatai
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymo kintamieji.
2. Spustelėkite Naujas.
3. Lauke Kintamasis surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Įrašyti.
6. Spustelėkite Rezultatai.
7. Spustelėkite Naujas.
8. Lauke Rezultatas surinkite reikšmę.
9. Lauke Aprašas įveskite reikšmę.
10. Lauke Rezultato būsena pasirinkite „Sėkmingai‟.
11. Spustelėkite Įrašyti.
12. Spustelėkite Naujas.
13. Lauke Rezultatas surinkite reikšmę.
14. Lauke Aprašas įveskite reikšmę.
15. Spustelėkite Įrašyti.
16. Uždarykite puslapį.
17. Uždarykite puslapį.

## <a name="set-up-item-sampling"></a>Nustatyti prekių pavyzdžių ėmimą
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Prekių pavyzdžių ėmimas.
2. Spustelėkite Naujas.
3. Lauke Prekių pavyzdžių ėmimas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Vertė įveskite skaičių.
    * Ši reikšmė susijusi su kiekio specifikacija, pasirinkta gretimame lauke.  
6. Išplėskite arba sutraukite sekciją Procesas.
7. Pažymėkite arba panaikinkite žymės langelio Visiškas blokavimas žymėjimą.
    * Jei pasirenkate šią parinktį ir jei tikrinti nepavyksta, užblokuojama visa partija ar užsakymo eilutės kiekis. Jei jos nepasirenkate, blokuojamos tik kokybės užsakymo prekės.  
8. Spustelėkite Įrašyti.
9. Uždarykite puslapį.

## <a name="create-a-quality-group"></a>Kurti kokybės grupę
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Kokybės grupės.
2. Spustelėkite Naujas.
3. Lauke Kokybės grupė surinkite reikšmę.
    * Naudokite aprašomąjį pavadinimą, kad būtų lengviau identifikuoti, kokios rūšies prekės bus grupėje (pavyzdžių ėmimo kriterijai).  
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Įrašyti.
6. Spustelėkite Įtraukti prekes.
7. Pasirinkti eilutę Prekės numeris
    * Šiame pavyzdyje filtravimas bus vykdomas pagal prekės numerį.  
8. Lauke Kriterijai surinkite reikšmę.
    * Pavyzdžiui, įveskite T*, kad filtruotumėte tuos prekių numerius, kurie prasideda T.  
9. Spustelėkite GERAI.
10. Spustelėkite GERAI.
11. Spustelėkite Prekių kokybės grupės.
12. Uždarykite puslapį.
13. Uždarykite puslapį.

## <a name="create-a-test-group"></a>Kurti bandymų grupę
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Bandymų grupės.
2. Spustelėkite Naujas.
3. Lauke Bandymų grupė surinkite reikšmę.
    * Suteikite bandymų grupei pavadinimą, kuris padės prisiminti, kokie bandymai vykdomi ir su kuria kokybės grupe ji turėtų būti susieta. Pavyzdžiui, jei ji bus naudojama su kokybės grupe, kuri pasirenka prekes, prasidedančias „T‟, galite ją pavadinti „T prekių bandymai‟.  
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Prekių pavyzdžių ėmimas pasirinkite prekių pavyzdžių ėmimo eilutę, kurią sukūrėte anksčiau.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Spustelėkite Pridėti.
8. Lauke Sekos numeris įveskite skaičių.
9. Lauke Bandymas pasirinkite bandymą, kurį sukūrėte anksčiau.
10. Sąraše raskite ir pasirinkite norimą įrašą.
11. Spustelėkite skirtuką Tikrinti.
12. Lauke Kintamasis pasirinkite bandymo kintamąjį, kurį sukūrėte prieš tai.
13. Sąraše raskite ir pasirinkite norimą įrašą.
14. Lauke Numatytasis rezultatas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
15. Sąraše spustelėkite saitą pasirinktoje eilutėje.
16. Spustelėkite Įrašyti.
17. Uždarykite puslapį.

## <a name="define-when-quality-orders-will-be-created"></a>Apibrėžti, kada bus kuriami kokybės užsakymai
1. Pasirinkite Atsargų valdymas > Nustatymas > Kokybės kontrolė > Kokybės susiejimai.
2. Spustelėkite Naujas.
3. Lauke Nuorodos tipas pasirinkite parinktį.
4. Lauke Prekės kodas pasirinkite „Grupė‟.
    * Šiame pavyzdyje pasirinksime „Grupė‟ ir naudosime anksčiau savo sukurtą kokybės grupę. Taip pat galite nustatyti „Lentelė‟, kad prekes nurodytumėte rankiniu būdu, arba pasirinkti „Visi‟, kad visos prekės būtų pridėtos į kokybės užsakymą.  
5. Lauke Prekė pasirinkite kokybės grupę, kurią sukūrėte prieš tai.
    * Galimos parinktys lauke Prekė priklauso nuo to, ką nustatote lauke Prekės kodas.  
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Išplėskite arba sutraukite sekciją Procesas.
8. Lauke Įvykio tipas pasirinkite parinktį.
    * Tai yra įvykis, kuris suaktyvina bandymą. Čia galimos parinktys priklauso nuo to, kokį procesą pasirinkote lauke Nuorodos tipas.  
9. Lauke Vykdymas pasirinkite parinktį.
10. Išplėskite arba sutraukite sekciją Kokybės užsakymo procesas.
11. Lauke Įvykių blokavimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Šiame lauke rodomas procesų, kuriuos galima blokuoti, jei kokybės užsakymas vis dar atidarytas, sąrašas. Parinktys priklauso nuo to, ką pasirinkote lauke Įvykio tipas.  
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Tai priklausys nuo ankstesnių pasirinktų reikšmių. Pasirinkite, are reikia blokuoti šiuos procesus, o atidarytus kokybės užsakymus susieti su šaltinio dokumento eilute.  
13. Išplėskite arba sutraukite sekciją Specifikacijos.
14. Lauke Bandymų grupė pasirinkite bandymų grupę, kurią sukūrėte prieš tai.
15. Sąraše raskite ir pasirinkite norimą įrašą.
16. Spustelėkite Įrašyti.
17. Uždarykite puslapį.

