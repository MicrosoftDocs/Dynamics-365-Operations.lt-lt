---
title: Išskaidyti laikotarpiai periodiniuose žurnaluose
description: Šiame straipsnyje pateikta informacija apie Čekijos Respublika, Estija, Vengrija, Latvija, Lietuva, Lenkija ir Rusija suskaidytus laikotarpius periodinių žurnalų arba pasikartojančių žurnalų žurnaluose.
author: mrolecki
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 261354
ms.search.form: LedgerJournalTable
ms.openlocfilehash: 2446edd0f569efbe2f6304ecbb46d5a4265ff95e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287042"
---
# <a name="split-periods-in-periodic-journals"></a>Išskaidyti laikotarpiai periodiniuose žurnaluose

[!include [banner](../includes/banner.md)]

Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas. Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius. Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių.

Norėdami pakartotinai nuskaityti ir registruoti operacijos eilutes, galite naudoti puslapį **Periodiniai žurnalai**. Jei pagrindinis juridinio subjekto adresas yra Čekijos Respublikoje, Estijoje, Vengrijoje, Latvijoje, Lietuvoje, Lenkijoje arba Rusijoje, į puslapį **Periodiniai žurnalai** įtraukiama laikotarpių skaidymo funkcija. Norėdami gauti daugiau informacijos, žr. [Periodinių žurnalų registravimas](../general-ledger/tasks/post-periodic-journals.md)

### <a name="example-split-for-periods-in-periodic-journals"></a>Pavyzdys: laikotarpių skaidymas periodiniuose žurnaluose

Draudimo įmonė siūlo jūsų organizacijai nuolaidą už išankstinį draudimo strategijos apmokėjimą visiems metams. Mokėjimas registruojamas į turto sąskaitą, pvz., iš anksto sumokėto draudimo. Tada amortizuojate savo mėnesio draudimo išlaidas per metus sukurdami periodinį žurnalą, kuriame yra iš anksto apmokėtos draudimo sąskaitos kreditas ir draudimo išlaidų debetas. Šiuo atveju galite naudoti laikotarpių skaidymo funkcijas. Puslapio **Periodinių žurnalų** **eilutės** veiksmų srityje spustelėkite mygtuką **Skaidyti laikotarpius**, o tada nurodykite tolesnius laukus.


| Laukas            | Aprašymas                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------|
| **Pradžios data**        | Pasirinkite pirmosios periodinio žurnalo eilutės datą.                                                                                                                                                        |
| **Laikotarpių skaičius** | Įveskite laikotarpių, per kuriuos padalinti žurnalo eilutes, skaičių. Ši reikšmė nurodo, kiek naujų operacijų bus generuojama. Operacijos suma paskirstoma tolygiai naujose operacijose. |
| **Vienetas**              | Pasirinkite laikotarpio matavimo vienetą.                                                                                                                                                                  |
| **Laikotarpio intervalas**   | Nustatykite intervalą tarp registravimo laikotarpių.                                                                                                                                                              |

Pvz., norėdami generuoti ketvirčio registravimus, įveskite **4** lauke **Laikotarpių skaičius**, lauke **Vienetas** pasirinkite **Mėnesiai** ir lauke **Laikotarpio intervalas** įveskite **3**. Sistema sugeneruos keturias žurnalo eilutes, po vieną kiekvienam ketvirtadaliui visos įvestos žurnalo eilutės sumos, 3 mėnesių intervalais. Panaši funkcija taip pat pateikiama bendrajame žurnale. Peržiūrėdami bendrojo žurnalo eilutes, pasirinkite **Periodiniai žurnalai** &gt; **Įrašyti žurnalą**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
