--- 
title: "Kurti įsigijimo katalogą"
description: "Šiame vedlyje parodoma, kaip kurti įsigijimo katalogą."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 19d053a0bdbdcc764b3361fe5a326e8c68cdc682
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-procurement-catalog"></a>Kurti įsigijimo katalogą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šiame vedlyje parodoma, kaip kurti įsigijimo katalogą. Šią užduotį paprastai atlieka įsigijimo specialistas. Taip pat sužinosite, kaip kurdami paraišką darbuotojai gali naudoti katalogą. Prieš kuriant katalogą, sistemoje turi būti nustatyta įsigijimo kategorijų hierarchija. Naujas katalogas perima hierarchiją ir visus hierarchijos produktus. Šį vedlį galite naudoti demonstracinių duomenų įmonėje USMF, kurioje įgalinta įsigijimo kategorijų hierarchija, taip pat procedūros veiksmų pavyzdžiuose.


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a>Įsitikinkite, kad įsigijimo kategorijų hierarchija nustatyta
1. Eikite į Įsigijimas ir šaltinio pasirinkimas > Įsigijimo kategorijos.
    * Demonstracinių duomenų įmonėje USMF galima naudoti įsigijimo kategorijų hierarchiją, be to, produktai yra įtraukti į kategoriją Biuro mašinos / Kompiuteriai. Jei šią procedūrą vykdote kaip užduočių vedlį, turėsite jį atrakinti, kad galėtumėte naršyti kategoriją. Jei hierarchija nesukurta, galite ją kurti spustelėdami Nauja. Tai galima atlikti tik vieną kartą.  
2. Uždarykite puslapį.

## <a name="create-a-catalog"></a>Katalogo kūrimas
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Katalogai > Įsigijimo katalogai.
2. Spustelėdami Naujas įsigijimo katalogas atidarykite išplečiamąjį dialogo langą.
3. Lauke Pavadinimas surinkite reikšmę.
4. Spustelėkite Gerai.
5. Medyje išplėskite CORP ĮSIGIJIMO KATEGORIJOS.
6. Medyje išplėskite BIURO MAŠINOS.
7. Medyje pasirinkite Kompiuteriai.
    * Sąraše rodomi įsigijimo kategorijos produktai. Jei į kategoriją norite įtraukti produktą, tai turite atlikti puslapyje Įsigijimo kategorijų hierarchija arba puslapyje Prekės informacija.  
    * Numatytasis naujinimo tipas nustato, ar nauji į įsigijimo kategorijų hierarchiją įtraukti produktai yra iš karto matomi kataloge. Jei naujinimo tipas nustatytas kaip Dinamiškas, keitimai matomi iš karto. Jei naujinimo tipas nustatytas kaip Statinis, katalogą naudojantys asmenys naujus produktus matys tik tada, kai katalogas bus iš naujo publikuotas. Veiksmas Publikuoti pateikiamas puslapio viršuje esančioje veiksmų srityje. Jei produktai pašalinami iš įsigijimo kategorijų hierarchijos, pakeitimas matomas iš karto, neatsižvelgiant į lauko Numatytasis naujinimo tipas reikšmę.  
8. Sąraše raskite ir pasirinkite norimą įrašą.
9. Spustelėkite Slėpti.
10. Veiksmų srityje spustelėkite Kategorijos naršymas.
11. Spustelėkite Drausti.
12. Veiksmų srityje spustelėkite Kategorijos naršymas.
13. Spustelėkite Įgalinti.
14. Spustelėkite Aktyvinti katalogą.
15. Uždarykite puslapį.

## <a name="make-the-catalog-visible"></a>Nustatyti katalogą kaip matomą
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Sąranka > Strategijos > Pirkimo strategijos.
2. Pasirinkite Įsigijimo strategijos USMF.
    * Turite pasirinkti juridinio subjekto pirkimo strategiją, pagal kurią su jūsų vartotojo profilių susietas darbuotojas gali užsakyti produktus. USMF demonstraciniuose duomenyse vartotojas administratorius yra susietas su darbuotoja, vardu Julia Funderburk, ir ji USMF produktus užsako pagal numatytuosius parametrus.  
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Pasirinkite katalogą, kurį ką tik sukūrėte.
5. Spustelėkite GERAI.
6. Uždarykite puslapį.
7. Uždarykite puslapį.

## <a name="use-the-catalog"></a>Naudoti katalogą
1. Pasirinkite Įsigijimas ir šaltinio pasirinkimas > Pirkimo paraiškos > Visos pirkimo paraiškos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Spustelėkite GERAI.
5. Spustelėkite „Įtraukti produktus“.
6. Sąraše raskite ir pasirinkite norimą įrašą.
    * Norėdami filtruoti produktus, galite naudoti kategorijų hierarchiją sąrašo kairėje pusėje arba filtrą sąrašo viršuje.  
7. Spustelėkite „Įtraukti į eilutes“.
8. Sąraše raskite ir pasirinkite norimą įrašą.
9. Spustelėkite „Įtraukti į eilutes“.
10. Spustelėkite GERAI.


