---
title: Registruoti periodinius žurnalus
description: Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai periodinis žurnalas nuskaitomas.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fdf630e9d292d0e016b6624a82b047d32bab898
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175546"
---
# <a name="post-periodic-journals"></a>Registruoti periodinius žurnalus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai periodinis žurnalas nuskaitomas. Sukūrę periodinį žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius. Šis užduočių vadovas sukurs tokį periodinį žurnalą, kurio pasikartojimas yra mėnesinis.

1. Pasirinkę **Naršymo sritis, eikite į Moduliai > Didžioji knyga > Periodinės užduotys > Periodiniai žurnalai**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke **Aprašo laukas**surinkite reikšmę. Aprašą sudarys vėliau gauto periodinio žurnalo pavadinimas, todėl jį suteikite atitinkamą.
6. **Veiksmų srityje** spustelėkite **Eilutės**. Periodinį žurnalą paprastai sudaro kelios eilutės. tačiau šis užduočių vadovas įtrauks tik vieną eilutę.
7. Lauke **Data** įveskite datą. Lauke **Data** nurodyta kito perkėlimo į kasdienį žurnalą registravimo data. Žurnaluose, kurie bus gaunami kiekvieną mėnesį, rekomenduojama naudoti datą tame mėnesyje, kada žurnlas bus registruojamas – paprastai tai pirmoji arba paskutinioji laikotarpio data. Galima lauką Data palikti tuščią, ir datą nurodyti, kai gaunamas žurnalas, naudojant lauką Tuščia data. Kai operacijos nuskaitomos, laukas automatiškai atnaujinamas į kitą pasikartojančią datą. 
8. Lauke **Sąskaita**nustatykite norimas reikšmes.
9. Lauke **Aprašas** pasirinkite reikšmę.
10. Uždarykite puslapį.
11. Lauke **Debetas** įveskite skaičių.
12. Lauke **Korespondentinė sąskaita** nustatykite norimas reikšmes.
13. Lauke **Vienetas** pasirinkite „Mėnesiai‟.
14. Lauke **Vienetų skaičius** įveskite „1‟.
15. Lauke **Paskutinė data** įveskite datą. Paskutinę datą įvedus į ankstesnį laikotarpį, nebus galima pasikartojančio žurnalo netyčia sukurti neteisingame pradžios laikotarpyje. Paskutinė diena bus atnaujinama vėliau, kiekvieną kartą nuskaitant periodinį žurnalą. 
16. Spustelėkite **Įrašyti**.
17. Eikite į **Naršymo sritis > Moduliai > Bendroji didžioji knyga > Žurnalo įrašai > Bendrieji žurnalai**.
18. Spustelėkite **Naujas**.
19. Lauke **Pavadinimas** įveskite arba pasirinkite reikšmę.
20. Sąraše raskite ir pasirinkite norimą įrašą.
21. Sąraše spustelėkite saitą pasirinktoje eilutėje.
22. Lauke **Aprašo laukas**surinkite reikšmę.
23. **Veiksmų srityje** spustelėkite **Eilutės**.
24. **Veiksmų srityje** spustelėkite **Periodinis žurnalas**.
25. Spustelėkite **Nuskaityti žurnalą**.
26. Lauke **Pabaigos data** įveskite datą. **Pabaigos data** naudojama kaip periodinio kvito eilučių galutinė data. Atsižvelgiant į pasikartojimo nuostatą, paskutinę datą ir datą Iki, gautame žurnale ta pati eilutė gali būti įtraukta daugiau nei vieną kartą. Data Iki automatiškai atnaujinama pagal seanso datą, kada paskutinį kartą periodinė eilutė buvo perkelta į žurnalą. 
27. Lauke **Periodinio žurnalo numeris** įveskite arba pasirinkite reikšmę.
28. Sąraše spustelėkite saitą pasirinktoje eilutėje.
29. Spustelėkite **Gerai**. Laikotarpio žurnalą dabar galima peržiūrėti, patvirtinti arba registruoti – tai priklauso nuo poreikio ir nustatymo.   
