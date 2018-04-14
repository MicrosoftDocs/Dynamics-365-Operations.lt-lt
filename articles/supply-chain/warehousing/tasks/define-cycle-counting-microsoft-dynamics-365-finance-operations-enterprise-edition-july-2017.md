--- 
title: "Apibrėžti ciklo skaičiavimą "
description: "Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f9cdb0a7de0199363279c53e817c98085b31fe6b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="define-cycle-counting"></a>Apibrėžti ciklo skaičiavimą  

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes. Šios užduoties įraše rodoma, kaip nustatyti numatytąjį skaičiavimo darbo prioritetą, įgalinti mobiliojo įrenginio meniu elementą, kad būtų apdorojamos išrinkimo ir skaičiavimo operacijos, įgalinti skaičiavimo ribinės vertės paleidiklį, kai vieta taps tuščia ir įgalinti konkrečiame sandėlyje esančios konkrečios prekės ciklo skaičiavimo planą. Šias užduotis paprastai atlieka sandėlio vadovas. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.


## <a name="set-the-priority-of-counting-work"></a>Skaičiavimo darbo prioriteto nustatymas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.
2. Spustelėkite skirtuką Ciklo skaičiavimas.
3. Lauke Numatytasis ciklų skaičiavimo darbo prioritetas įveskite skaičių.
    * Šis veiksmas pakeičia ciklo skaičiavimo darbo prioritetą, palyginti su kitais darbo sandėlyje tipais. Įvesdami skaičių, mažesnį negu kitiems darbo tipams, didesnį prioritetą suteikiate ciklo skaičiavimo darbui.  
4. Spustelėkite Įrašyti.
5. Uždarykite puslapį.

## <a name="enable-the-mobile-device"></a>Įgalinkite mobilųjį įrenginį
1. Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.
2. Spustelėkite Naujas.
3. Lauke Meniu elemento pavadinimas surinkite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Režimas pasirinkite „Darbas“.
6. Nustatykite pasirinkties Naudoti esamą darbą padėtį Taip.
    * Kai nustatote šią parinktį Taip, sistema ieškos esamo darbo, kuriam atlikti naudojamas mobiliojo įrenginio meniu elementas.  
7. Lauke Nukreipė pasirinkite „Nurodomas sistemos“.
    * Pasirinkus „Sistemos nurodyta“, sandėlio darbuotojas bus nukreiptas atlikti atvirą darbą, apibrėžtą darbo klasėse. (Mes sukursime šias darbo klases paskui.)  
8. Išplėskite arba sutraukite sekciją Darbo klasės.
    * Dabar mes sukursime dvi darbo klases, kurios bus naudojamos su šiuo mobiliojo įrenginio meniu elementu. Naudojant meniu elementą bus ieškoma šių darbo klasių, ir todėl vartotojui bus rodomas darbas, kurio prioritetas aukščiausias.  
9. Spustelėkite Naujas.
10. Lauke Darbo klasės ID pasirinkite vertę.
11. Spustelėkite Naujas.
12. Lauke Darbo klasės ID pasirinkite vertę.
13. Spustelėkite Įrašyti.
14. Uždarykite puslapį.
15. Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu.
16. Sąraše raskite ir pasirinkite norimą įrašą.
17. Medyje pasirinkite meniu elementą, kurį ką tik sukūrėte.
18. Spustelėkite Redaguoti.
19. Norėdami įtraukti meniu elementą į meniu, spustelėkite rodyklę.
20. Spustelėkite Įrašyti.

## <a name="create-a-counting-threshold"></a>Sukurkite skaičiavimo ribinę vertę
1. Pasirinkite Sandėlio valdymas > Nustatymai > Ciklo skaičiavimas > Ciklų skaičiavimo ribinės reikšmės.
2. Spustelėkite Naujas.
3. Lauke Ciklo skaičiavimo ribinės vertės ID įveskite vertę.
4. Nustatykite pasirinkties Apdoroti ciklo skaičiavimą nedelsiant padėtį Taip.
5. Lauke Aprašas įveskite reikšmę.
6. Spustelėkite Įrašyti.
7. Spustelėkite Pasirinkti vietas.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke Kriterijai pasirinkite vertę.
10. Spustelėkite GERAI.
11. Uždarykite puslapį.

## <a name="create-a-cycle-count-plan"></a>Sukurkite ciklų skaičiavimo planą
1. Pasirinkite Sandėlio valdymas > Nustatymai > Ciklo skaičiavimas > Ciklų skaičiavimo planai.
2. Spustelėkite Naujas.
3. Lauke Ciklo skaičiavimo plano ID įveskite vertę.
4. Lauke Aprašas surinkite reikšmę.
5. Lauke Maksimalus ciklų skaičiavimo skaičius įveskite skaičių.
6. Spustelėkite Įrašyti.
7. Spustelėkite Pasirinkti vietas.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke Kriterijai pasirinkite vertę.
10. Spustelėkite GERAI.
11. Lauke Dienos tarp ciklo skaičiavimų įveskite skaičių.
    * Pavyzdžiui, jei lauke Dienos tarp ciklo skaičiavimų nustatyta 5, ciklo skaičiavimo darbas bus sukuriamas kas penkias dienas. Tačiau jei ciklo skaičiavimo darbas apdorojamas trečią dieną, kitas ciklo skaičiavimo darbas bus sukurtas po penkių dienų nuo paskutinio ciklo skaičiavimo, 8 dieną.  
12. Spustelėkite Įrašyti.
13. Spustelėkite Naujas.
14. Lauke Sekos numeris įveskite skaičių.
    * Rūšiuojama yra nuo mažiausio iki didžiausio skaičiaus. Reikšmė turi būti didesnė už 0 (nulį).  
15. Sąraše pažymėkite pasirinktą eilutę.
16. Lauke Aprašas įveskite reikšmę.
17. Spustelėkite Įrašyti.
18. Spustelėkite Apibrėžti produkto užklausą.
19. Sąraše pažymėkite pasirinktą eilutę.
20. Lauke Kriterijai įveskite arba pasirinkite reikšmę.
21. Spustelėkite GERAI.
22. Uždarykite puslapį.


