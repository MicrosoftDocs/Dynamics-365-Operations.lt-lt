---
title: Inicijuoti atsargų lygius sandėlyje
description: Ši procedūra nurodo, kaip atnaujinti turimas atsargas rankiniu būdu, naudojant atsargų perkėlimo žurnalą.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c1e5ca96919acde7e850292a73ebd00185f1f7a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244480"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Inicijuoti atsargų lygius sandėlyje

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip atnaujinti turimas atsargas rankiniu būdu, naudojant atsargų perkėlimo žurnalą. (Turimas atsargas taip pat galima atnaujinti importuojant duomenų objektų operacijas.) Šį vadovą galite paleisti naudodami demonstracinių duomenų įmonę USMF, kurioje pateikiami visi būtinieji komponentai, pvz., žurnalo pavadinimas, prekių nustatymai, registravimo šablonai ir sąskaitos. Vadovas siūlo konkrečias naudojamos prekės ir dimensijų reikšmes. Jei pasirinksite kitą prekę, gali reikėti įvesti kitų dimensijų reikšmes.

1. Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekės > Perkėlimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Pasirinkite IMov.
    * Kitais verslo tikslais pravartu naudoti kitus žurnalo pavadinimo šablonus.  
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke Korespondentinė sąskaita nurodykite reikšmes „140200“.
    * Ši korespondentinė sąskaita bus numatytoji žurnalo eilučių sąskaita. Galima perrašyti numatytąją reikšmę ir eilutėms priskirti kitas korespondentines sąskaitas.  
7. Spustelėkite GERAI.
8. Spustelėkite Naujas.
9. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
10. Pasirinkite prekę A0001.
11. Sąraše spustelėkite saitą pasirinktoje eilutėje.
12. Spustelėkite skirtuką Atsargų dimensijos.
13. Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
14. Pasirinkite 1 vietą.
15. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
16. Pasirinkite 13 sandėlį.
17. Sąraše spustelėkite saitą pasirinktoje eilutėje.
18. Lauke Vieta spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
19. Pasirinkite 13 vietą.
20. Lauke Kiekis įveskite skaičių.
21. Spustelėkite Įrašyti.
22. Spustelėkite Registruoti.
23. Pažymėkite arba atžymėkite žymės langelį Perkelti visas registravimo klaidas į naują žurnalą.
    * Jei įgalinsite šią parinktį, visos eilutės, kurių nepavyksta registruoti, bus nukopijuotos į naują žurnalą. Pasinaudodami žurnale esančia informacija galite ištaisyti klaidas ir iš naujo registruoti eilutes.  
24. Spustelėkite GERAI.
25. Uždarykite puslapį.
26. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]