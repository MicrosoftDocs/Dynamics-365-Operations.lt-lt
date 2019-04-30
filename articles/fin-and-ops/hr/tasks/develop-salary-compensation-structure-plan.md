---
title: Kurti atlyginimų / kompensavimo struktūrą ir planą
description: Šis užduočių vadovas apžvelgia procesą, kaip kurti pastoviosios atlyginimo dalies planą ir leisti darbuotojams būti įtrauktiems į tą planą taikant tinkamumo taisykles.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichsea
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e3b71e679539441b90f399a84ad8ef8d3decf19
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/19/2019
ms.locfileid: "859418"
---
# <a name="develop-salarycompensation-structure-and-plan"></a>Kurti atlyginimų / kompensavimo struktūrą ir planą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas apžvelgia procesą, kaip kurti pastoviosios atlyginimo dalies planą ir leisti darbuotojams būti įtrauktiems į tą planą taikant tinkamumo taisykles. Demonstracinė duomenų įmonė, naudota kuriant šią užduotį, yra USMF, ir užduotis yra skirta kompensacijų ir išmokų vadovams.


## <a name="create-fixed-compensation-plan"></a>Kurti pastoviosios atlyginimo dalies planą
1. Spustelėkite Kompensavimo valdymas.
2. Spustelėkite Pastoviosios atlyginimo dalies planai.
3. Spustelėkite Naujas.
4. Lauke Planas surinkite reikšmę.
5. Lauke Aprašas įveskite reikšmę.
6. Lauke Įsigaliojimo data įveskite datą.
7. Lauke Tipas pasirinkite, ar pastoviosios atlyginimo dalies planas yra Intervalo, Kategorijos, ar Veiksmo.
8. Žymės langelis Leistina rekomendacija veikia kaip bet kokių veiksmų, įtrauktų į šį planą apdorojimo įvykyje, numatytoji reikšmė.  Leidę rekomendacijas galėsite nepaisyti paskaičiuotos siūlomos sumos apdorodami kompensaciją.
9. Funkcija Nepatenka į leistiną nuokrypio diapazoną leidžia nurodyti, kaip norite elgtis su kompensacijų sumomis, kurios nepatenka į nurodytą pateikto lygio kompensavimo struktūros diapazoną.  Funkcijos Nepatenka į leistiną nuokrypio diapazoną parinktis Nėra leis naudoti bet kokią kompensacijos sumą.  Negriežto nuokrypio parinktis naudotoją įspės, jei kompensacijos suma bus mažesnė nei minimali to lygio atskaitos taško suma, arba didesnė nei maksimali to lygio suma. Naudotojas gali įspėjimo nepaisyti ir tęsti veiklą.  Griežto nuokrypio parinktis generuos klaidą, jei darbuotojo kompensacija bus nustatyta ne tarp minimalių ir maksimalių to lygio atskaitos taškų, ir darbuotojo kompensaciją automatiškai pakoreguos, kad ji patektų į šį diapazoną.
10. Laukas Samdos taisyklė naudojamas, kai, norint apskaičiuoti darbuotojo kompensaciją, vykdomas kompensacijos apdorojimo įvykis.  Procentinė samdos taisyklė skaičiuos padidėjimą, proporcingą laiko trukmei, kurią darbuotojas dirba cikle.
11. Lauke Valiuta surinkite reikšmę.
12. Lauke Užmokesčio tarifo konvertavimas įveskite arba pasirinkite reikšmę.
13. Išplėskite dalį Diapazono realizavimo matrica.
    * Papildomai galite įtraukti diapazono realizavimo įrašų, kad darbuotojai greičiau pasiektų vidurio tašką ir kad sulėtintumėte spartą, kuria jie juda link savo diapazono maksimumo.  
14. Šiame etape turite įrašyti pastoviosios atlyginimo dalies planą, kad įgalintumėte mygtuką Nustatyti kompensaciją ir toliau apibrėžtumėte plano kompensacijų struktūrą.  Spustelėkite Įrašyti.
15. Spustelėkite Nustatyti kompensaciją.
    * Yra trys būdai, kaip sukurti kompensavimo struktūrą. 1: sukurti visiškai naują struktūrą, pasirenkant atskaitos taškų rinkinį ir įtraukiant lygių bei sukuriant savą struktūrą. 2: kompensavimo struktūrą kopijuoti iš esamo plano kaip pradžios tašką ir ją modifikuoti naujajam planui. 3: pasirinkti esamą kompensacijų tinklelį. Jei kompensacijų tinklelį jau naudoja kitas planas, visi atlikti tinklelio pakeitimai taip pat atsispindės kitame plane.  
16. Pažymėkite parinktį Pagal esamą kompensavimo matricą sukurti naują.
17. Lauke Kopijuoti iš tinklelio įveskite arba pasirinkite reikšmę.
    * Jei norite, galite keisti naujojo kompensacijų tinklelio, kuris bus sukurtas kaip pasirinkto tinklelio kopija, pavadinimą.  
18. Spustelėkite GERAI.
19. Spustelėkite Masinis keitimas.
    * Masinis keitimas leidžia išlaikyti kompensacijų matricos sumas, vieną ar kelis lygius ir (arba) atskaitos taškus padidinant procentine dalimi arba standartine suma.  
20. Lauke Koregavimo suma įveskite skaičių.
21. Pažymėkite arba atžymėkite visas sąrašo eilutes.
22. Spustelėkite Taikyti tinkleliui.
23. Uždarykite puslapį.
    * Kai kompensavimo struktūra sukurta arba pasirinkta, galite pasirinkti, kurie atskaitos taškai turėtų būti naudojami kaip pastoviosios atlyginimo dalies plano kontrolinis taškas.  Kontrolinis taškas naudojamas skaičiuoti darbuotojo lyginamajam koeficientui.  
24. Lauke Kontrolinis taškas įveskite arba pasirinkite reikšmę.
25. Uždarykite puslapį.

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a>Kurti naujojo kompensavimo plano tinkamumo taisyklę
    * Naujojo pastoviosios atlyginimo dalies plano darbuotojui priskirti negalima tol, kol nebus nustatytos plano tinkamumo taisyklės.  
1. Spustelėkite Tinkamumo taisyklės.
2. Spustelėkite Naujas.
3. Lauke Tinkamumas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Įsigaliojimo data įveskite datą.
    * Tinkamumo taisyklės naudojamos tiek pastoviosios, tiek kintamosios atlyginimo dalies planams.  Lauke Tipas pasirinkite, kokio tipo planui skirtas šis tinkamumo taisyklių rinkinys.  
6. Lauke Planas įveskite arba pasirinkite vertę.
    * Pasirinkite kriterijus, kuriuos turi atitikti darbuotojas, kad turėtų teisę į kompensavimo planą. Kriterijai gali būti Skyrius, Profesinė sąjunga, Vieta (Kompensacijos sritis), Darbas, Funkcija, Darbo tipas arba Kompensavimo lygis. Kad turėtų teisę į kompensavimo planą, darbuotojas turi atitikti visus nurodytus kriterijus. Jei nenurodyti jokie kriterijai, į kompensavimo planą teisę turi visi darbuotojai. Jei darbuotojas neatitinka tinkamumo taisyklėje nurodytų kriterijų, arba jei kompensavimo plano tinkamumo taisyklė nenurodyta, kuriant darbuotojo pastoviosios atlyginimo dalies įrašą, peržvalgoje kompensavimo planas nebus rodomas.  
7. Uždarykite puslapį.
8. Uždarykite puslapį.

