---
title: Registruoti prekės, kurios patobulinto sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą
description: Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea8b5e03282aa21aa9dfa486b1deaced6af4601c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433741"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registruoti prekės, kurios patobulinto sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą

[!include [banner](../../includes/banner.md)]

Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai naudojate patobulintus sandėlio valdymo procesus. Paprastai tai atlieka gavimo klerkas. 

Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Prieš pradėdami šį vadovą, turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute. Prekė eilutėje turi būti laikoma atsargose, nenaudoti produktų variantų ir neturėti sekimo dimensijų. Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje įgalintas sandėlio valdymo procesas. Naudojamame sandėlyje turi būti įgalinti sandėlio valdymo procesai, o vieta, kurią naudojate prekių gavimui, turi būti kontroliuojama numerio lentelės. Jei naudojate USMF, kurdami savo pirkimo užsakymą, galite naudoti įmonės klientą 1001, sandėlį 51 ir elementą M9200. 

Pasižymėkite savo sukurto pirkimo užsakymo numerį ir prekės numerį bei pirkimo užsakymo eilutėje naudotą vietą.


## <a name="create-an-item-arrival-journal-header"></a>Prekių gavimo žurnalo antraštės kūrimas
1. Eikite į Prekių gavimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
    * Jei naudojate USMF, galite surinkti WHS. Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinksite, turi turėti šias savybes: patikros rinkimo vieta turi būti nustatyta į „Ne“ ir karantino valdymas turi būti nustatytas į „Ne“.  
4. Lauke Numeris surinkite reikšmę.
5. Lauke Teritorija surinkite reikšmę.
    * Pasirinkite vietą, kurią naudojote savo pirkimo užsakymo eilutėje. Tai bus numatytoji visų žurnalo eilučių reikšmė. Jei USMF naudojote 51 sandėlį, pasirinkite 5 vietą.  
6. Lauke Sandėlis surinkite reikšmę.
    * Pasirinkite tinkamą jūsų pasirinktos svetainės sandėlį. Tai bus numatytoji visų žurnalo eilučių reikšmė. Jeigu USMF naudojate reikšmių pavyzdžius, pasirinkite „51“.  
7. Lauke Vieta surinkite reikšmę.
    * Pasirinkite tinkamą jūsų pasirinktos vietos sandėlį. Vieta turi būti susieta su vietos šablonu, kuris yra kontroliuojamas pagal numerio lentelę. Tai bus numatytoji visų žurnalo eilučių reikšmė. Jeigu USMF naudojate reikšmių pavyzdžius, pasirinkite „Bulk-008“.  
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]