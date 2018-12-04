--- 
title: "Registruoti prekės, kurios patobulinto sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą"
description: "Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 050d1fcbc59d9bb3253bfed2433987285423b334
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registruoti prekės, kurios patobulinto sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus. Paprastai tai atlieka gavimo klerkas. 

Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Prieš pradėdami šį vadovą, turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute. Prekė eilutėje turi būti laikoma atsargose, nenaudoti produktų variantų ir neturėti sekimo dimensijų. Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje įgalintas sandėlio valdymo procesas. Naudojamas sandėlis turi būti įgalintas naudoti sandėlio valdymo procesus, o naudojama gavimo vieta turi būti kontroliuojama pagal numerio lentelę. Jei naudojate USMF, norėdami sukurti savo PO, galite naudoti įmonės sąskaitą 1001, 51 sandėlį ir prekę M9200. 

Pasižymėkite savo sukurto pirkimo užsakymo numerį ir prekės numerį bei pirkimo užsakymo eilutėje naudotą vietą.


## <a name="create-an-item-arrival-journal-header"></a>Prekių gavimo žurnalo antraštės kūrimas
1. Eikite į Prekių gavimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
    * Jei naudojate USMF, galite surinkti WHS. Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinkote, turi turėti toliau nurodytas ypatybes: Tikrinti paėmimo vietą turi būti nustatyta į Ne ir Sulaikymo valdymas turi būti nustatyta į Ne.  
4. Lauke Numeris surinkite reikšmę.
5. Lauke Teritorija surinkite reikšmę.
    * Pasirinkite vietą, kurią naudojote savo pirkimo užsakymo eilutėje. Tai bus numatytoji visų žurnalo eilučių reikšmė. Jei USMF naudojote 51 sandėlį, pasirinkite 5 vietą.  
6. Lauke Sandėlis surinkite reikšmę.
    * Pasirinkite tinkamą pasirinktos vietos sandėlį. Tai bus numatytoji visų žurnalo eilučių reikšmė. Jei USMF naudojate reikšmių pavyzdžius, pasirinkite 51.  
7. Lauke Vieta surinkite reikšmę.
    * Pasirinkite tinkamą pasirinkto sandėlio vietą. Vieta turi būti susieta su vietos šablonu, kuris yra kontroliuojamas pagal numerio lentelę. Tai bus numatytoji visų žurnalo eilučių reikšmė. Jei USMF naudojate reikšmių pavyzdžius, pasirinkite Bulk-008.  
8. Dešiniuoju pelės mygtuku spustelėkite lauko Numerio lentelė išplečiamąją rodyklę ir pasirinkite Peržiūrėti išsamią informaciją.
9. Spustelėkite Naujas.
10. Lauke Numerio lentelė įveskite reikšmę.
    * Pasižymėkite reikšmę.  
11. Spustelėkite Įrašyti.
12. Uždarykite puslapį.
13. Lauke Numerio lentelė įveskite reikšmę.
    * Įveskite ką tik sukurtos numerio lentelės reikšmę. Tai bus numatytoji visų žurnalo eilučių reikšmė.  
14. Spustelėkite GERAI.

## <a name="add-a-line"></a>Įtraukti eilutę
1. Spustelėkite Pridėti eilutę.
2. Lauke Prekės numeris surinkite reikšmę.
    * Įveskite prekės numerį, kurį naudojote pirkimo užsakymo eilutėje.  
3. Lauke Kiekis įveskite skaičių.
    * Įveskite norimą registruoti kiekį.  
    * Lauke Data nurodoma data, kada atsargose bus užregistruotas turimas šios prekės kiekis.  
    * Lauką Partijos ID užpildys sistema, jei jį galima identifikuoti pagal pateiktą informaciją. Kitu atveju turite įtraukti jį patys. Tai yra privalomas laukas, kuris susieja šią registraciją su konkrečia šaltinio dokumento eilute.  

## <a name="complete-the-registration"></a>Registracijos užbaigimas
1. Spustelėkite Tikrinti.
    * Patikrinama, ar žurnalas parengtas registruoti. Jei patikrinti nepavyksta, norint registruoti žurnalą reikia ištaisyti klaidas.  
2. Spustelėkite GERAI.
    * Spustelėję Gerai, patikrinkite pranešimą. Turėtumėte gauti pranešimą, kuriame parašyta, kad žurnale problemų nėra.  
3. Spustelėkite Registruoti.
4. Spustelėkite GERAI.
    * Spustelėję Gerai, patikrinkite pranešimų juostą. Turėtumėte gauti pranešimą, kuriame parašyta, kad operacija baigta.  
5. Uždarykite puslapį.


