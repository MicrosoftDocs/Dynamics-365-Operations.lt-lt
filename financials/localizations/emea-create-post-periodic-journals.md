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
ms.search.scope: Operations, Core
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8343c3c28e9b3cf79bdee568b81fc8cad659f4ab
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="split-periods-in-periodic-journals"></a>Laikotarpių skaidymas periodiniuose žurnaluose

[!include[banner](../includes/banner.md)]


Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas. Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius. Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių.

Norėdami pakartotinai nuskaityti ir registruoti operacijos eilutes, galite naudoti puslapį **Periodiniai žurnalai**. Jei pagrindinis juridinio subjekto adresas yra Čekijos Respublikoje, Estijoje, Vengrijoje, Latvijoje, Lietuvoje, Lenkijoje arba Rusijoje, į puslapį **Periodiniai žurnalai** įtraukiama laikotarpių skaidymo funkcija. <!---For more information, see [Create and process a periodic journal](http://ax.help.dynamics.com/en/wiki/create-and-process-a-periodic-journal/).-->

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




