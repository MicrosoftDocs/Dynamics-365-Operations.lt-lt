---
title: 'Apibrėžti ciklo skaičiavimą '
description: Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24c4c27745a15f013d20b52efc6e36de848a0251
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916788"
---
# <a name="define-cycle-counting"></a>Apibrėžti ciklo skaičiavimą  

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ciklo skaičiavimas yra sandėlio procesas, kurį galite naudoti norėdami audituoti turimas atsargų prekes. Šios užduoties įraše rodoma, kaip nustatyti numatytąjį skaičiavimo darbo prioritetą, įgalinti mobiliojo įrenginio meniu elementą, kad būtų apdorojamos išrinkimo ir skaičiavimo operacijos, įgalinti skaičiavimo ribinės vertės paleidiklį, kai vieta taps tuščia ir įgalinti konkrečiame sandėlyje esančios konkrečios prekės ciklo skaičiavimo planą. Šias užduotis paprastai atlieka sandėlio vadovas. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis.


## <a name="set-the-priority-of-counting-work"></a>Skaičiavimo darbo prioriteto nustatymas
1. Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Sandėlio valdymo parametrai**.
2. Spustelėkite skirtuką **Ciklo skaičiavimas**.
3. Lauke **Numatytasis ciklo skaičiavimo darbo prioritetas** įveskite skaičių. Šis veiksmas pakeičia ciklo skaičiavimo darbo prioritetą, palyginti su kitais darbo sandėlyje tipais. Įvesdami skaičių, mažesnį negu kitiems darbo tipams, didesnį prioritetą suteikiate ciklo skaičiavimo darbui.  
4. Spustelėkite **Įrašyti**.
5. Uždarykite puslapį.

## <a name="enable-the-mobile-device"></a>Įgalinkite mobilųjį įrenginį
1. Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai**.
2. Spustelėkite **Naujas**.
3. Lauke **Meniu elemento pavadinimas** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Režimas** pasirinkite Darbas.
6. Nustatykite parinktį **Naudoti esamą darbą** į Taip.  Kai nustatote šią parinktį Taip, sistema ieškos esamo darbo, kuriam atlikti naudojamas mobiliojo įrenginio meniu elementas.  
7. Lauke **Nurodyta pagal** pasirinkite Sistemos nurodyta. Pasirinkus „Sistemos nurodyta“, sandėlio darbuotojas bus nukreiptas atlikti atvirą darbą, apibrėžtą darbo klasėse. (Mes sukursime šias darbo klases paskui.)  
8. Išplėskite parinkties **Darbo klasės** „fastTab“. Dabar mes sukursime dvi darbo klases, kurios bus naudojamos su šiuo mobiliojo įrenginio meniu elementu. Naudojant meniu elementą bus ieškoma šių darbo klasių, ir todėl vartotojui bus rodomas darbas, kurio prioritetas aukščiausias.  
9. Spustelėkite **Naujas**.
10. Lauke **Darbo klasės ID** pasirinkite reikšmę.
11. Spustelėkite **Naujas**.
12. Lauke **Darbo klasės ID** pasirinkite reikšmę.
13. Parinktyje **Veiksmų sritis** spustelėkite **Įrašyti**.
14. Uždarykite puslapį.
15. Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu**.
16. Sąraše raskite ir pasirinkite norimą įrašą.
17. Medyje pasirinkite meniu elementą, kurį ką tik sukūrėte.
18. Spustelėkite **Redaguoti**.
19. Norėdami įtraukti meniu elementą į meniu, spustelėkite rodyklę.
20. Spustelėkite **Įrašyti**.

## <a name="create-a-counting-threshold"></a>Sukurkite skaičiavimo ribinę vertę
1. Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Ciklo skaičiavimas > Ciklo skaičiavimo ribinės vertės**.
2. Spustelėkite **Naujas**.
3. Lauke **Ciklo skaičiavimo ribinės vertės ID** įveskite reikšmę.
4. Nustatykite parinktį **Nedelsiant apdoroti ciklo skaičiavimą** į Taip
5. Lauke **Aprašo laukas**surinkite reikšmę.
6. Spustelėkite **Įrašyti**.
7. Spustelėkite **Pasirinkti vietas**.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke **Kriterijai** pasirinkite reikšmę.
10. Spustelėkite **Gerai**.
11. Uždarykite puslapį.

## <a name="create-a-cycle-count-plan"></a>Sukurkite ciklų skaičiavimo planą
1. Parinktyje **Naršymo sritis** eikite į **Moduliai > Sandėlio valdymas > Sąranka > Ciklo skaičiavimas > Ciklo skaičiavimo planai**.
2. Spustelėkite **Naujas**.
3. Lauke **Ciklo skaičiavimo plano ID** įveskite reikšmę.
4. Lauke **Aprašo laukas**surinkite reikšmę.
5. Lauke **Maksimalus ciklo skaičiavimų skaičius** įveskite skaičių.
6. Spustelėkite **Įrašyti**.
7. Spustelėkite **Pasirinkti vietas**.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke **Kriterijai** pasirinkite reikšmę.
10. Spustelėkite **Gerai**.
11. Lauke **Dienos tarp ciklo skaičiavimų** įveskite skaičių. Pavyzdžiui, jei lauke **Dienos tarp ciklo skaičiavimų** nustatysite 5, ciklo skaičiavimo darbas bus sukurtas kas penkias dienas. Tačiau jei ciklo skaičiavimo darbas apdorojamas trečią dieną, kitas ciklo skaičiavimo darbas bus sukurtas po penkių dienų nuo paskutinio ciklo skaičiavimo, 8 dieną.  
12. Spustelėkite **Įrašyti**.
13. Spustelėkite **Naujas**.
14. Lauke **Sekos skaičius** įveskite skaičių. Rūšiuojama yra nuo mažiausio iki didžiausio skaičiaus. Reikšmė turi būti didesnė už 0 (nulį).  
15. Sąraše pažymėkite pasirinktą eilutę.
16. Lauke **Aprašo laukas**surinkite reikšmę.
17. Spustelėkite **Įrašyti**.
18. Spustelėkite užklausą **Apibrėžti produktą**.
19. Sąraše pažymėkite pasirinktą eilutę.
20. Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.
21. Spustelėkite **Gerai**.
22. Uždarykite puslapį.

