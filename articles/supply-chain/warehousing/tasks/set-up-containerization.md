--- 
title: "Nustatyti krovimą į konteinerius"
description: "Šia procedūra aprašoma, kaip automatizuoti krovinių krovimą į konteinerius modulyje Sandėlio valdymas."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-containerization"></a>Nustatyti krovimą į konteinerius

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šia procedūra aprašoma, kaip automatizuoti krovinių krovimą į konteinerius modulyje Sandėlio valdymas. Vykstant automatizuoto krovimo į konteinerius procesui, apdorojant bangą siuntoms sukuriami konteineriai ir paėmimo darbas, o darbo eilutes galima išskaidyti į kiekius, telpančius į konteinerius. Taip sandėlio darbininkams lengviau prekes paimti tiesiai į pasirinktą konteinerį. Palyginti su rankinio pakavimo procesu, tokias užduotis kaip konteinerių kūrimas, prekių priskyrimas ir konteinerių uždarymas automatizuoja sistema. Atliekant šią procedūrą naudojama demonstracinė įmonė USMF, o ją atlieka sandėlio vadovas.


## <a name="set-up-a-wave-template"></a>Bangos šablono nustatymas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Bangos > Bangų šablonai.
2. Spustelėkite Naujas.
3. Lauke Bangos šablono pavadinimas įveskite reikšmę.
4. Lauke Bangos šablono aprašas įveskite reikšmę.
5. Lauke Teritorija įveskite arba pasirinkite reikšmę.
6. Lauke Sandėlis įveskite arba pasirinkite reikšmę.
7. Išplėskite dalį Būdai.
    * Srityje Pasirinkti metodai pateikiami pasirinkto bangos šablono tipo metodai. Bangos šablone turi būti krovimo į konteinerius metodas.  
8. Sąraše raskite ir pasirinkite norimą įrašą.
9. Lauke Bangos veiksmo kodas įveskite reikšmę.
    * Įveskite įtraukto metodo bangos veiksmo kodą – tai gali būti bet koks kodas. Įtraukti metodą galimą keletą kartų ir galima priskirti skirtingus bangos veiksmų kodus. Norėdami tai padaryti, puslapyje Bangos apdorojimo metodai prie šio metodo pasirinkite Galima kartoti.  
10. Spustelėkite Įrašyti.
11. Uždarykite puslapį.

## <a name="set-up-a-container-type"></a>Konteinerio tipo nustatymas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių tipai.
    * Savo konteinerius galite apibrėžti puslapyje Konteinerių tipai. Galite sukonfigūruoti faktines konteinerių dimensijas – taros svorį, didžiausią svorį, didžiausią tūrį, ilgį, plotį ir aukštį. Šiame pavyzdyje turime tris skirtingus dėžių dydžius.  
2. Spustelėkite Naujas.
3. Lauke Konteinerio tipo kodas įveskite reikšmę.
4. Lauke „Taros svoris“ įveskite skaičių.
5. Lauke Didžiausias svoris įveskite skaičių.
6. Lauke „Tūris“ įveskite skaičių.
7. Lauke Ilgis įveskite skaičių.
8. Lauke Plotis įveskite skaičių.
9. Lauke Aukštis įveskite skaičių.
10. Lauke Aprašas įveskite reikšmę.
11. Spustelėkite Įrašyti.
12. Spustelėkite Naujas.
13. Lauke Konteinerio tipo kodas įveskite reikšmę.
14. Lauke Aprašas įveskite reikšmę.
15. Lauke „Taros svoris“ įveskite skaičių.
16. Lauke Didžiausias svoris įveskite skaičių.
17. Lauke „Tūris“ įveskite skaičių.
18. Lauke Ilgis įveskite skaičių.
19. Lauke Plotis įveskite skaičių.
20. Lauke Aukštis įveskite skaičių.
21. Spustelėkite Įrašyti.
22. Spustelėkite Naujas.
23. Lauke Konteinerio tipo kodas įveskite reikšmę.
24. Lauke Aprašas įveskite reikšmę.
25. Lauke „Taros svoris“ įveskite skaičių.
26. Lauke Didžiausias svoris įveskite skaičių.
27. Lauke „Tūris“ įveskite skaičių.
28. Lauke Ilgis įveskite skaičių.
29. Lauke Plotis įveskite skaičių.
30. Lauke Aukštis įveskite skaičių.
31. Spustelėkite Įrašyti.
32. Uždarykite puslapį.

## <a name="set-up-a-container-group"></a>Konteinerių grupės nustatymas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių grupės.
2. Spustelėkite Naujas.
    * Galite nustatyti logines konteinerių tipų grupes. Kiekvienai grupei galite nurodyti seką, kuria bus pakuojami konteineriai, ir konteinerių užpildymo procentą. Naudojami prekės matmenų dydžiai siekiant nustatyti, ar ji tilps konteineryje. Naudojamas konteineris, artimiausias prekės dydžio matmenims. Jei grupėje turite kelis konteinerių tipus, rekomenduojame išdėstyti seką pagal dydį, kad didžiausias konteineris sekoje būtų pirmas (Nr. 1), o mažiausias – paskutinis.    
3. Lauke Konteinerių grupės ID įveskite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Spustelėkite Naujas.
6. Sąraše pažymėkite pasirinktą eilutę.
7. Lauke Konteinerio tipas įveskite arba pasirinkite reikšmę.
8. Spustelėkite Naujas.
9. Sąraše pažymėkite pasirinktą eilutę.
10. Lauke Konteinerio tipas įveskite arba pasirinkite reikšmę.
11. Spustelėkite Naujas.
12. Sąraše pažymėkite pasirinktą eilutę.
13. Lauke Konteinerio tipas įveskite arba pasirinkite reikšmę.
14. Spustelėkite Įrašyti.
15. Uždarykite puslapį.

## <a name="set-up-a-container-build-template"></a>Konteinerio kūrimo šablono nustatymas
1. Pasirinkite Sandėlio valdymas > Nustatymas > Konteineriai > Konteinerių kūrimo šablonai.
2. Spustelėkite Naujas.
    * Konteinerio kūrimo šablonas priklauso nuo to, kuris iš krovimo į konteinerius procesų atliekamas. Kiekvienu konteinerio kūrimo šablonu apibrėžiamas vienas krovimo į konteinerius procesas, kurį naudos bangos šablonas. Parinktimi Redaguoti užklausą galima apibrėžti sąlygas, kuriomis pasirinktas šablonas bus apdorojamas. Pavyzdžiui, galbūt krovimo į konteinerius procesą norėsite vykdyti tik su konkrečiais klientais, produktais ar sandėliais, arba į šabloną galite įtraukti atitinkamų užklausos intervalų. Lauku Bangos veiksmo kodas nustatoma, kaip konteinerio kūrimo šablonas susietas su bangos šablono veiksmais. Kai vykdoma banga, ja nustatoma, kuris konteinerio kūrimo šablonas (-ai) naudojamas inicijuoti krovimo į konteinerius procesui. Lauku Pagrindinis užklausos tipas nustatoma, ką pakuoti ir kuo grįsti filtro užklausą.  
3. Sąraše pažymėkite pasirinktą eilutę.
4. Lauke Konteinerio šablono ID įveskite reikšmę.
5. Lauke Konteinerių grupės ID įveskite arba pasirinkite reikšmę.
6. Lauke Bangos veiksmo kodas įveskite reikšmę.
7. Pažymėkite žymės langelį Leisti skaidyti paėmimus.
8. Spustelėkite Įrašyti.
9. Spustelėkite Konteinerių maišymo apribojimai.
    * Maišymo logikos skaidymais galima nustatyti paskirstymo eilučių pakavimo konteineriuose taisykles. Pavyzdžiui, jei įtrauksite lauką Prekės numeris, prekes priskiriant konteineriams ir esant naujam prekės numeriui, bus sukurtas naujas konteineris. Taip darbininkai tame pačiame konteineryje nesupakuos paskirstymo eilučių dviem skirtingiems klientams.  
10. Spustelėkite Naujas.
11. Lauke Lentelė pasirinkite parinktį.
12. Lauke Laukų pasirinkimas įveskite arba pasirinkite reikšmę.
13. Spustelėkite GERAI.


