--- 
title: "Įgalinti numerio lentelės žymės spausdinimą"
description: "Ši procedūra leidžia vykstant pardavimo išrinkimo darbo procesui ir iš atsargų paėmus paskutinę prekę, automatiškai spausdinti gabenimo konteinerio serijos kodo (SSCC) etiketę."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="enable-license-plate-label-printing"></a>Įgalinti numerio lentelės žymės spausdinimą

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra leidžia vykstant pardavimo išrinkimo darbo procesui ir iš atsargų paėmus paskutinę prekę, automatiškai spausdinti gabenimo konteinerio serijos kodo (SSCC) etiketę. Šią procedūrą galite vykdyti demonstracinių duomenų įmonėje USMF. Jei ją vykdote naudodami savo duomenis, reikia nustatyti numerio lentelių numeraciją. Prieš pradėdami šią užduotį, turite nustatyti etikečių spausdintuvą. Pasirinkite Organizacijos administravimas > Nustatymas > Tinklo spausdintuvai. Srityje Veiksmas spustelėkite Parinktys ir tada spustelėkite mygtuką Atsisiųsti dokumento kelvados agento diegimo programą. Paleiskite diegimo programą ir prieš tęsdami procedūrą įsitikinkite, kad nustatyta veikiančio tinklo spausdintuvo parinktis Aktyvus.


## <a name="set-up-the-gs1-company-prefix"></a>Nustatyti GS1 įmonės prefiksą
1. Pasirinkite Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai.
2. Lauke GS1 įmonės prefiksas įveskite savo GS1 įmonės numerio 7 skaitmenis.
3. Spustelėkite Įrašyti.
4. Uždarykite puslapį.

## <a name="setup-the-sscc-license-plate-number-sequence"></a>Nustatyti SSCC numerio lentelės numeraciją
1. Pasirinkite Organizacijos administravimas > Numeracijos > Numeracijos.
2. Lauke Sritis pasirinkite parinktį.
3. Lauke Nuoroda pasirinkite parinktį.
4. Lauke Įmonė surinkite reikšmę.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.
7. Išplėskite skyrių Segmentai.
8. Spustelėkite Redaguoti.
9. Lentelėje Segmentai pasirinkite pirmąją eilutę
10. Spustelėkite Šalinti.
11. Spustelėkite Šalinti.
12. Spustelėkite Įrašyti.
13. Uždarykite puslapį.

## <a name="create-the-document-route-layout"></a>Kurti dokumento maršruto maketą
1. Pasirinkite Sandėlio valdymas > Nustatymas > Dokumento maršruto planavimas > Dokumento maršruto planavimo maketai.
    * Įgalinti SSCC maketą.  
2. Spustelėkite Naujas.
3. Lauke Maketo ID surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Sąraše raskite ir pasirinkite norimą įrašą.
6. Spustelėkite Įterpti teksto pabaigoje.
7. Spustelėkite Įrašyti.
8. Uždarykite puslapį.

## <a name="set-up-the-document-routing"></a>Nustatyti dokumentų maršruto planavimą
1. Pasirinkite Sandėlio valdymas > Nustatymas > Dokumento maršruto planavimas > Dokumento maršruto planavimas.
2. Lauke Darbo užsakymo tipas pasirinkite parinktį.
3. Spustelėkite Naujas.
4. Lauke Sandėlis surinkite reikšmę.
5. Lauke Pavadinimas surinkite reikšmę.
6. Spustelėkite Naujas.
7. Lauke Maketo ID įveskite arba pasirinkite reikšmę.
8. Lauke Pavadinimas įveskite spausdintuvo, kurį norite naudoti, pavadinimą.
9. Spustelėkite Įrašyti.
10. Uždarykite puslapį.

## <a name="create-mobile-device-menu"></a>Kurti mobiliojo įrenginio meniu
1. Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.
2. Spustelėkite Naujas.
3. Lauke Meniu elemento pavadinimas surinkite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Režimas pasirinkite parinktį.
6. Lauke Naudoti esamą darbą pasirinkite Taip.
7. Lauke Generuoti numerio lentelę pasirinkite Taip.
8. Išplėskite skyrių Darbo klasės.
9. Spustelėkite Naujas.
10. Lauke Darbo klasės ID surinkite reikšmę.
11. Spustelėkite Įrašyti.
12. Uždarykite puslapį.
13. Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu.
14. Sąraše raskite ir pasirinkite norimą įrašą.
15. Medyje pasirinkite „Medyje pasirinkite meniu elementą, kurį sukūrėte anksčiau.‟.
16. Spustelėkite Redaguoti.
17. Norėdami įtraukti meniu elementą į meniu, spustelėkite rodyklę.
18. Spustelėkite Įrašyti.
19. Uždarykite puslapį.

## <a name="update-a-work-template"></a>Naujinti darbo šabloną
1. Pasirinkite Sandėlio valdymas > Nustatymas > Darbas > Darbo šablonai.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Spustelėkite Redaguoti.
4. Spustelėkite Naujas.
5. Sąraše pažymėkite pasirinktą eilutę.
6. Lauke Darbo tipas pasirinkite „Spausdinti‟.
7. Lauke Darbo klasės ID įveskite arba pasirinkite reikšmę.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Spustelėkite Perkelti aukštyn.
10. Spustelėkite Įrašyti.
11. Uždarykite puslapį.


