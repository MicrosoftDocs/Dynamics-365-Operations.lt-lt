--- 
title: "Elektroninių ataskaitų (ER) formato, skirto skaičiavimo ir sumavimo veiksmams atlikti, taikymas"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: c6d309416a3a0c4da07a76c90246f492585deef5
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---
# <a name="run-electronic-reporting-er-formats-to-do-counting-and-summing"></a>Elektroninių ataskaitų (ER) formato, skirto skaičiavimo ir sumavimo veiksmams atlikti, taikymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis. Šiuos veiksmus galima atlikti DEMF įmonėje.

Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „ER: formato konfigūravimas, norint atlikti skaičiavimo ir sumavimo veiksmus (3 dalis: konfigūracijų naudojimas, norit kurti išvestį)“.

Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Patikrinkite šią „Intrastat“ ataskaitų generavimo konfigūraciją
1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
2. Spustelėkite Ataskaitų konfigūracijos.
3. Medyje išplėskite „Intrastat“ modelis.
4. Medyje išplėskite dalį Intrastat model\Intrastat (DE).
5. Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
6. Veiksmų srityje spustelėkite Konfigūracijos.
7. Spustelėkite Vartotojo parametrai.
8. Lauke Paleisti parametrus pasirinkite Taip.
9. Spustelėkite GERAI.
10. Spustelėkite Redaguoti.
11. Lauke Paleisti juodraštį pasirinkite Taip.
12. Spustelėkite Įrašyti.
13. Eikite į Mokestis > Nustatymas > Užsienio prekyba > Užsienio prekybos parametrai.
14. Išplėskite skyrių Elektroninės ataskaitos.
15. Pasirinkite konfigūraciją „Intrastat“ (DE) su skaičiavimu ir sumavimu.
16. Pasirinkite konfigūraciją „Intrastat“ (DE) su skaičiavimu ir sumavimu.
17. Spustelėkite Įrašyti.
18. Uždarykite puslapį.
19. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.
20. Spustelėkite Išvestis.
21. Spustelėkite Ataskaita.
    * Paleiskite „Intrastat“ ataskaitos generavimo procesą.  
22. Lauke Pradžios data nustatykite datą „2000-01-01“.
    * Nurodykite ataskaitinio laikotarpio, kuris apima esamas formos operacijas, pradžios ir pabaigos datas.  
23. Lauke Pabaigos data nustatykite datą „2022-12-31“.
    * Nurodykite ataskaitinio laikotarpio, kuris apima esamas formos operacijas, pradžios ir pabaigos datas.  
24. Lauke Kryptis pasirinkite Gavimai.
25. Lauke Generuoti failą pasirinkite Taip.
26. Spustelėkite GERAI.
    * Peržiūrėkite sukurtą išvestį, kurios gale pateikiamos suvestinės eilutės.  
27. Spustelėkite Naujas.
28. Sąraše pažymėkite pasirinktą eilutę.
29. Lauke Kryptis pasirinkite Išsiuntimai.
30. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
31. Lauke Prekė įveskite arba pasirinkite reikšmę.
32. Lauke Svoris nustatykite reikšmę 10.
33. Lauke SF suma nustatykite reikšmę 10000.
34. Lauke Statistinė suma nustatykite reikšmę 10000.
35. Spustelėkite Išvestis.
36. Spustelėkite Ataskaita.
37. Lauke Kryptis pasirinkite Išsiuntimai.
38. Spustelėkite GERAI.
    * Peržiūrėkite sukurtą išvestį, kurios gale pateikiamos suvestinės eilutės. Atkreipkite dėmesį, kad ji buvo pakeista, lyginant su pirmuoju paleidimu.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Paleiskite šią konfigūraciją derinimo režimu, norėdami peržiūrėti surinktus skaičiavimo ir sumavimo duomenis
1. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
2. Medyje išplėskite „Intrastat“ modelis.
3. Medyje išplėskite dalį Intrastat model\Intrastat (DE).
4. Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
5. Veiksmų srityje spustelėkite Konfigūracijos.
6. Spustelėkite Vartotojo parametrai.
7. Lauke Vykdyti derinimo režimu pasirinkite Taip.
8. Spustelėkite GERAI.
9. Uždarykite puslapį.
10. Pasirinkite Mokesčiai > Deklaracijos > Užsienio prekyba > Intrastat.
11. Spustelėkite Išvestis.
12. Spustelėkite Ataskaita.
13. Spustelėkite GERAI.
14. Uždarykite puslapį.
15. Eikite į Organizacijos administravimas > Elektroninės ataskaitos > Konfigūracijos.
16. Medyje išplėskite „Intrastat“ modelis.
17. Medyje išplėskite dalį Intrastat model\Intrastat (DE).
18. Medyje pasirinkite Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.
19. Spustelėkite Derinimo žurnalai.
    * Atkreipkite dėmesį, kad sukurtas pasirinktos konfigūracijos vykdymo proceso derinimo žurnalo įrašas.  
20. Spustelėkite Pridėti.
21. Spustelėkite Atidaryti.
    * Peržiūrėkite sukurtą XML failą, kuriame yra skaičiavimo ir sumavimo informacija, surinkta vykdant pasirinktą konfigūraciją.  


