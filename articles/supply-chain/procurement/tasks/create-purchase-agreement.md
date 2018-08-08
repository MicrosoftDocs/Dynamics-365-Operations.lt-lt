--- 
title: "Kurti pirkimo sutartį"
description: "Ši procedūra padės jums sukurti pirkimo sutartį."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0d0cc6508071bea3f622bc21f06aa55d2b757b6f
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-agreement"></a>Kurti pirkimo sutartį

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra padės jums sukurti pirkimo sutartį. Paprastai tai atlieka pirkimo vadybininkas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis. Prieš pradėdami turite nustatyti pirkimo sutarčių klasifikacijas. Sukūrę sutartį, galėsite ją naudoti, kai sukursite PU – pirkimo sutarties sąlygos bus nukopijuotos į antraštę ir į visas užsakymo eilutes, susijusias su šia sutartimi.


## <a name="create-a-new-purchase-agreement"></a>Kurti naują pirkimo sutartį
1. Pasirinkite Pirkimai ir tiekėjų parinkimas > Pirkimo sutartys > Pirkimo sutartys.
2. Spustelėkite Naujas.
3. Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke „Pirkimo sutarties klasifikacija“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše raskite ir pasirinkite norimą įrašą.
8. Sąraše spustelėkite saitą pasirinktoje eilutėje.
9. Išplėskite skyrių Bendra.
10. Lauke „Galiojimo data“ įveskite datą.
    * Ši galiojimo data bus numatytoji visose įsipareigojimų eilutėse ir nulems, kiek laiko galios kiekvienas konkretus įsipareigojimas.  
11. Lauke „Dokumento pavadinimas“ įveskite pirkimo sutarties pavadinimą.
    * Palikite lauką „Numatytasis įsipareigojimas“ nustatytą kaip „Produkto kiekio įsipareigojimas“ (arba pakeiskite jį, jei jo nustatymas kitas).  
    * Numatytoji įsipareigojimo reikšmė nurodo jūsų parinktis sutarties eilutėse. Jei jums reikia naujo įsipareigojimo tipo kuriant sutarties eilutes, turite pakeisti numatytąjį įsipareigojimą antraštėje.  Yra 4 tipų įsipareigojimai: produkto kiekio įsipareigojimas – dėl konkretaus produkto kiekio; produkto vertės įsipareigojimas – dėl konkrečios produkto valiutos sumos; produkto kategorijos vertės įsipareigojimas – dėl konkrečios valiutos sumos įsigijimo kategorijoje, kurioje suma gali būti skirta kataloginei prekei arba nekataloginei prekei; vertės įsipareigojimas – dėl konkrečios valiutos sumos, kurią galima skirti bet kokiam produktui arba bet kokiai įsigijimo kategorijai.  
12. Spustelėkite GERAI.

## <a name="add-a-commitment"></a>Įtraukti įsipareigojimą
1. Spustelėkite Pridėti eilutę.
2. Sąraše pažymėkite pasirinktą eilutę.
3. Lauke Prekės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Pasirinkite produktą, prie kurio norite pridėti įsipareigojimą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Lauke Kiekis įveskite skaičių.
    * Tai yra bendras kiekis, kurį susitarėte pirkti iš tiekėjo.  
7. Lauke Vieneto kaina įveskite skaičių.
8. Išplėskite skyrių Eilutės informacija.
9. Nustatykite parinkties „Maksimaliai vykdoma“ reikšmę „Taip“.
    * Parinktis „Maksimaliai vykdoma“ riboja įsipareigojimų naudojimą. Galite pirkti tik tokį kiekį, kuris nurodytas eilutės lauke „Kiekis“.  
10. Sutraukite skyrių „Eilutės informacija“.

## <a name="add-header-conditions"></a>Įtraukti antraštės sąlygas
1. Veiksmų srityje spustelėkite Parinktys.
2. Spustelėkite Keisti rodinį.
3. Spustelėkite antraštės rodinį.
4. Išplėskite skyrių Sąlygos.
5. Lauke Mokėjimo būdas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Čia pagal numatytuosius nustatymus rodomos mokėjimo sąlygos iš tiekėjo sąskaitos.       
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Lauke „Pristatymo būdas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše spustelėkite saitą pasirinktoje eilutėje.
10. Lauke „Pristatymo sąlygos“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="confirm-and-activate-the-agreement"></a>Patvirtinti ir aktyvinti sutartį
1. Veiksmų srityje spustelėkite „Pardavimo sutartis“.
2. Spustelėkite „Patvirtinimas“.
    * Nustatykite parinkties „Pažymėti sutartį kaip galiojančią“ reikšmę „Taip“.  
3. Spustelėkite Gerai.
4. Veiksmų srityje spustelėkite „Pardavimo sutartis“.
5. Spustelėkite „Pirkimo sutarties patvirtinimai“.
    * Parinktis „Peržiūrėti / spausdinti“ leidžia generuoti pirkimo sutarties dokumentą, kurį paskui galite atspausdinti arba nusiųsti tiekėjui. Jei vėliau sutartį atnaujinsite ir iš naujo patvirtinsite, abi jos versijos bus rodomas čia.  
6. Uždarykite puslapį.


