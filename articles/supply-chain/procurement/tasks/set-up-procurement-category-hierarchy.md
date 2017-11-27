--- 
title: "Nustatyti įsigijimo kategorijų hierarchiją"
description: "Ši procedūra nurodo, kaip sukurti naujų mazgų įsigijimo kategorijų hierarchijoje ir kaip konfigūruoti įsigijimo kategoriją, kuri bus naudojama įsigijimo procese."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
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
ms.sourcegitcommit: 6ad5c8552a6989e9093d0b1325754bc0f6d19372
ms.openlocfilehash: 4541d029c9c3be3ee42332e5d8ff183dd503f13e
ms.contentlocale: lt-lt
ms.lasthandoff: 11/06/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a>Nustatyti įsigijimo kategorijų hierarchiją

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip sukurti naujų mazgų įsigijimo kategorijų hierarchijoje ir kaip konfigūruoti įsigijimo kategoriją, kuri bus naudojama įsigijimo procese. Šias užduotis paprastai atlieka pirkimo vadybininkas. Šią procedūrą galėsite pradėti tik esant įsigijimo tipo kategorijų hierarchijai. Jei naudojate demonstracinių duomenų įmonę, šią procedūrą galite vykdyti su USMF įmonėje.


## <a name="add-a-new-procurement-category"></a>Įtraukiti naują įsigijimo kategoriją
1. Eikite į Įsigijimas ir šaltinio pasirinkimas > Įsigijimo kategorijos.
2. Spustelėkite „Redaguoti kategorijų hierarchiją“.
    * Kairiojoje puslapio pusėje rodoma dabartinė įsigijimo kategorijų hierarchija. Ketinate pakeisti hierarchiją.  
3. Spustelėkite „Naujas kategorijos mazgas“.
    * Sistema pasirenka viršutinį mazgą pagal numatytuosius nustatymus. Jei vykdote šią procedūrą kaip užduoties vadovą, galite spustelėti mygtuką „Atrakinti“ ir pasirinkti kitą pirminį mazgą, į kurį galėsite įterpti savo naująjį mazgą. Tai atlikę, vėl užrakinkite užduoties vadovą, o tada spustelėkite „Nauja kategorijos mazgas“.  
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Aprašas įveskite reikšmę.
6. Lauke „Patogus pavadinimas“ įveskite reikšmę.
    * Pasirinktinai galite įvesti patogų pavadinimą. Jis bus rodomas kategorijos peržvalgose kartu su kategorijos pavadinimu.  
7. Spustelėkite Įrašyti.

## <a name="add-products-to-your-new-procurement-category"></a>Įtraukti produktus į naują įsigijimo kategoriją
1. Eikite į Įsigijimas ir šaltinio pasirinkimas > Įsigijimo kategorijos.
    * Pasirinkite mazgą, kurį ką tik pridėjote. Jei šią procedūrą vykdote kaip užduočių vadovą, jį gali reikėti atrakinti, kad galėtumėte pasirinkti mazgą,  
2. Perjunkite skyriaus „Produktai“ išplėtimą.
3. Spustelėkite „Įtraukti“, kad susietumėte produktus su įsigijimo kategorija.
4. Pasirinkite produktą, kurį norite įtraukti į įsigijimo kategoriją.
5. Spustelėkite rodyklę, kad pasirinktumėte produktą.
6. Pasirinkite kitą produktą, kurį norite įtraukti į įsigijimo kategoriją.
7. Spustelėkite rodyklę, kad pasirinktumėte produktą.
8. Spustelėkite GERAI.

## <a name="add-approved-and-preferred-vendors"></a>Įtraukti patvirtintus ir pirmenybę turinčius tiekėjus
1. Perjunkite dalies Tiekėjai išplėtimą.
2. Spustelėkite Pridėti.
    * Galite įtraukti tiekėją į įsigijimo kategoriją ir nurodyti, ar tiekėjas toje kategorijoje yra turintis pirmenybę, ar jis joje tiesiog patvirtintas. Kai panaikinate tiekėją iš kategorijos, istorinės operacijos su tiekėju kategorijoje nepanaikinamos.   
3. Raskite tiekėją, kurį norite įtraukti į kategoriją.
4. Spustelėkite rodyklę, kad pasirinktumėte tiekėją.
5. Spustelėkite Gerai.
6. Pasirinkite tiekėjo eilutę, kurią norite modifikuoti.
7. Lauke „Tiekėjo būsena“ pasirinkite parinktį.
    * Tiekėjo pasirinkimo nustatymas kategorijos strategijos taisyklėje reguliuoja, ar pirkimo paraiškose bus pateikiami pirmenybę turintys, patvirtinti ar visi tiekėjai.   

## <a name="add-additional-information-to-the-category"></a>Įtraukti papildomą informaciją į kategoriją
1. Perjunkite skyriaus „Tiekėjo vertinimo kriterijų grupės“ išplėtimą.
    * Šiame skirtuke galima apibrėžti kriterijus, pagal kuriuos turi būti vertinami tiekėjai atitinkamoje įsigijimo kategorijoje. Jei norite tai padaryti, spustelėkite „Pridėti“ ir pasirinkite tiekėjo vertinimo grupę, kurioje yra jūsų norimi kriterijai.  
2. Perjunkite skyriaus „Klausimynai“ išplėtimą.
    * Šiame skirtuke galima pridėti klausimynus, kurie bus rodomi paraiškoje tol, kol nustatytas veiklos tipas bus „Paraiška“. Tada prašytojas turi užpildyti klausimyną, prieš pateikdamas paraišką dėl konkretaus produkto ar produktų toje įsigijimo kategorijoje.  
3. Perjunkite skyriaus „Prekių PVM grupės“ išplėtimą.
4. Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Pasirinkite PVM grupę.
6. Perjunkite skyriaus „Kategorijos puslapis“ išplėtimą.
    * Kategorijos puslapius galima sukurti puslapyje „Kategorijų hierarchija“. Juose yra informacija apie įsigijimo kategoriją, pvz., informacija apie kategorijos produktų tipus, kategorijos produktų vaizdai arba pranešimai, pvz., apie kategorijoje galimas nuolaidas. Kategorijos puslapyje esanti informacija rodoma pirkimo paraiškose.  
7. Uždarykite puslapį.


