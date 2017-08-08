---
title: "Laikotarpių skaidymas periodiniuose žurnaluose"
description: "Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas. Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius. Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9b07d2c274d3e4818ffd917a730aeba3e5dff76c
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="split-periods-in-periodic-journals"></a>Laikotarpių skaidymas periodiniuose žurnaluose

[!include[banner](../includes/banner.md)]


Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas. Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius. Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių.

Norėdami pakartotinai nuskaityti ir registruoti operacijos eilutes, galite naudoti puslapį **Periodiniai žurnalai**. Jei pagrindinis juridinio subjekto adresas yra Čekijos Respublikoje, Estijoje, Vengrijoje, Latvijoje, Lietuvoje, Lenkijoje arba Rusijoje, į puslapį **Periodiniai žurnalai** įtraukiama laikotarpių skaidymo funkcija. Daugiau informacijos ieškokite [Periodinio žurnalo registravimas](/dynamics365/unified-operations/financials/general-ledger/tasks/post-periodic-journals)

### <a name="example-split-for-periods-in-periodic-journals"></a>Pavyzdys: laikotarpių skaidymas periodiniuose žurnaluose

Draudimo įmonė siūlo jūsų organizacijai nuolaidą už išankstinį draudimo strategijos apmokėjimą visiems metams. Mokėjimas registruojamas į turto sąskaitą, pvz., iš anksto sumokėto draudimo. Tada amortizuojate savo mėnesio draudimo išlaidas per metus sukurdami periodinį žurnalą, kuriame yra iš anksto apmokėtos draudimo sąskaitos kreditas ir draudimo išlaidų debetas. Šiuo atveju galite naudoti laikotarpių skaidymo funkcijas. Puslapio **Periodinių žurnalų** **eilutės** veiksmų srityje spustelėkite mygtuką **Skaidyti laikotarpius**, o tada nurodykite tolesnius laukus.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Laukas**             | **Aprašas**                                                                                                                                                                                             |
| **Pradžios data**        | Pasirinkite pirmosios periodinio žurnalo eilutės datą.                                                                                                                                                        |
| **Laikotarpių skaičius** | Įveskite laikotarpių, per kuriuos padalinti žurnalo eilutes, skaičių. Ši reikšmė nurodo, kiek naujų operacijų bus generuojama. Operacijos suma paskirstoma tolygiai naujose operacijose. |
| **Vienetas**              | Pasirinkite laikotarpio matavimo vienetą.                                                                                                                                                                  |
| **Laikotarpio intervalas**   | Nustatykite intervalą tarp registravimo laikotarpių.                                                                                                                                                              |

Pvz., norėdami generuoti ketvirčio registravimus, įveskite **4** lauke **Laikotarpių skaičius**, lauke **Vienetas** pasirinkite **Mėnesiai** ir lauke **Laikotarpio intervalas** įveskite **3**. Sistema sugeneruos keturias žurnalo eilutes, po vieną kiekvienam ketvirtadaliui visos įvestos žurnalo eilutės sumos, 3 mėnesių intervalais. Panaši funkcija taip pat pateikiama bendrajame žurnale. Peržiūrėdami bendrojo žurnalo eilutes, pasirinkite **Periodiniai žurnalai** &gt; **Įrašyti žurnalą**.




