--- 
title: "Nustatyti „lean manufacturing“ darbo elementus"
description: "Darbo elementas yra konkreti išteklių grupių forma, kurios gali būti naudojamas „lean manufacturing“ proceso veiklose."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f060f084baab055a51e390f488ca2553bd997b92
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="define-lean-manufacturing-work-cells"></a>Nustatyti „lean manufacturing“ darbo elementus

[!include[task guide banner](../../includes/task-guide-banner.md)]

Darbo elementas yra konkreti išteklių grupių forma, kurios gali būti naudojamas „lean manufacturing“ proceso veiklose. Darbo elementai turi įvesties ir išvesties vietas ir pajėgumo apibrėžimą pagal gamybos eigos modelį. Norėdami daugiau sužinoti apie pagrindines „lean manufacturing“ darbo elementų ir pajėgumo skaičiavimų sąvokas, žr. „Lean manufacturing“ techninę dokumentaciją. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF


## <a name="create-a-work-cell"></a>Kurkite darbo elementą. 
1. Pasirinkite Organizacijos administravimas > Ištekliai > Išteklių grupės.
2. Spustelėkite Naujas.
3. Lauke Išteklių grupės surinkite reikšmę.
    * Darbo elemento ID paprastai yra sisteminis kodas, kuris juridiniam subjektui turi būti unikalus.  
4. Lauke Aprašas įveskite reikšmę.
    * Apraše pateikiamas darbo elemento vardas arba pavadinimas.  
5. Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Darbo elementas yra vienoje konkrečioje svetainėje. Ir įeigos, ir išeigos sandėlis bei vieta turi būti nurodyta šioje svetainėje.  
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Lauke Gamybos vienetas spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Pasirinkite gamybos vienetą, kuriam priklauso šis darbo elementas.  
9. Pažymėkite žymės langelį Darbo elementas.
    * Norint naudoti išteklių grupę kaip „lean“ darbo elementą, žymės langelis Darbo elementas turi būti pažymėtas.  Atkreipkite dėmesį, kad sukūrus išteklių grupę šios ypatybės negalima pakeisti.  
10. Lauke Įeigos sandėlis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
11. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Apskaitos ir medžiagų kontrolės tikslais, ant parduotuvės grindų išdėstytos prekės paprastai yra priskiriamos tam tikram virtualiam sandėliui. Tačiau, jei šias vietas norite papildyti naudodami sandėlio darbą, jos turi būti priimančio žaliavų sandėlio dalis.  
12. Lauke Įeigos vieta spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
    * Atkreipkite dėmesį, kad proceso veiklos įvesties vietą galima perrašyti apskritai arba konkrečiam produktui ar produkto variantui apibrėžiant paėmimo veiklas, sudarančias proceso veiklą. Darbo elemento įvesties vietos negali būti kontroliuojamos pagal numerio lentelę.  
14. Lauke Išeigos sandėlis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
15. Sąraše raskite ir pasirinkite norimą įrašą.
    * Kelių veiklos gamybos eigų ar gamybos eilučių atvejais, po gamybos proceso produktas paprastai perkeliamas į kito darbo elemento įeigos sandėlį arba pardavimo ar tranzito sandėlį. Atminkite, modeliuojant „lean manufacturing“ procesus, transportas paprastai yra nereikalingas kaip ir jo ataskaitos pateikimas.  
16. Sąraše spustelėkite saitą pasirinktoje eilutėje.
17. Lauke Išeigos vieta spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
    * Gamybos eigoje su keliomis proceso veiklomis dažnai tai yra kito darbo elemento įvesties vieta.  
18. Sąraše raskite ir pasirinkite norimą įrašą.
19. Sąraše spustelėkite saitą pasirinktoje eilutėje.
20. Išplėskite arba sutraukite skyrių Operacija.
    * Vykdymo laiko kategorija turi būti pateikta norint įgalinti išlaidų skaičiavimą ir „lean kanban" užduočių vykdymą.  
21. Lauke Apdorojimo laiko kategorija spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
22. Sąraše raskite ir pasirinkite norimą įrašą.
    * Apdorojimo laiko savikainos kategorija naudojama apskaičiuoti standartinę savikainą ir įkainojimą atvirkštine tvarka.  
23. Sąraše spustelėkite saitą pasirinktoje eilutėje.
24. Išplėskite arba sutraukite skyrių Kalendoriai.
25. Spustelėkite Pridėti.
26. Lauke Kalendorius spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
27. Sąraše raskite ir pasirinkite norimą įrašą.
    * Paprastai tam tikros svetainės darbo elementams naudojamas tas pats darbo laiko kalendorius. Jei darbo elementuose gali būti atskiri darbo laikai, gali reikėti sukurti tam tikrą darbo elemento darbo laiko kalendorių. Atkreipkite dėmesį, kad kalendoriuje turi būti nustatytas standartinis darbo laikas, kai naudojamas „lean“ darbo elementas, nes pajėgumo apibrėžimas paprastai yra susijęs su standartinės darbo dienos darbo laiku.  
28. Sąraše spustelėkite saitą pasirinktoje eilutėje.
29. Išplėskite arba sutraukite skyrių Darbo elemento pajėgumas.
30. Spustelėkite Pridėti.
31. Lauke Gamybos eigos modelis spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
32. Sąraše raskite ir pasirinkite norimą įrašą.
    * Šiai procedūrai reikalingas gamybos eigos modelio tipas Našumas, norint rodyti našumo pajėgumo apibrėžimą.  
33. Sąraše spustelėkite saitą pasirinktoje eilutėje.
34. Lauke Pajėgumo laikotarpis pasirinkite pasirinktį.
    * Pasirinktys yra šios: Standartinė darbo diena - darbo elemento darbo laiko kalendoriaus pajėgumas išreiškiamas standartinės darbo dienos trukme. Kiekvienos dienos faktinį darbo laiką nustato kalendorius, o tuo remiantis apskaičiuojamas efektyvus galimas pajėgumas.   Savaitė – leidžia savaitės pajėgumą. Nėra atliktas faktinio darbo laiko koregavimas.   Mėnesio – leidžia mėnesio pajėgumą. Nėra atliktas faktinio pajėgumo koregavimas.   Paprastai standartinė darbo diena naudojama dienos laikotarpiams, o savaitės pajėgumas naudojamas savaitės pajėgumo laikotarpiams.  
35. Lauke Vidutinis našumo kiekis įveskite skaičių.
    * Atkreipkite dėmesį, kad „lean“ operacijoms niekada nebūna nustatytas didžiausias galimas pajėgumas idealioje aplinkoje. Todėl pajėgumas visada turi būti nurodytas operacijoms, vykdomoms įprastomis aplinkybėmis.  
36. Lauke Vienetas spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
37. Sąraše spustelėkite saitą pasirinktoje eilutėje.
38. „ResolveChanges“ Vienetas.

## <a name="add-a-financial-dimension"></a>Įtraukti finansinę dimensiją
1. Išplėskite arba sutraukite skyrių Finansinės dimensijos.
    * Atkreipkite dėmesį, kad gamybos eigoje nustatytos finansinės dimensijos perrašo konkretaus darbo elemento finansinės dimensijas.    Finansinės dimensijos, kurias galima pasirinkti, priklauso nuo jūsų sistemos finansinių dimensijų konfigūracijos. Šie veiksmai atitinka demonstracinius duomenis, nustatytus USMF įmonėje. Naudojant skirtingus duomenis veiksmai gali būti netaikomi.  
2. Lauke „CostCenter“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite ir pasirinkite norimą įrašą.
    * Dimensijos, kurios turi būti pasirinktos „lean“ darbo elementuose, priklauso nuo konkretaus juridinio subjekto finansinių dimensijų įdiegimo apskaitos modelyje.  
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke Prekių grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="save"></a>Įrašyti
1. Spustelėkite Įrašyti.


