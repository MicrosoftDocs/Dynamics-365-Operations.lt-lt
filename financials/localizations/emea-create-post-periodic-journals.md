---
title: "Išskaidyti laikotarpiai periodinius žurnalus"
description: "Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas. Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius. Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261354
ms.assetid: 76c0d7bf-f795-4d42-9a86-a9f36989962c
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 58ab77aea9e66834c516806e5f0cfe3069c94ff3
ms.lasthandoff: 03/31/2017


---

# <a name="split-periods-in-periodic-journals"></a>Išskaidyti laikotarpiai periodinius žurnalus

Periodiniai žurnalai kartais vadinami pasikartojančias žurnalais nes suma, tekstas ir kitą informaciją kartojasi kiekvieną kartą, kai žurnalas užregistruojamas. Sukūrę žurnalą, nurodote pasikartojimų laikotarpio intervalą pvz., dienas ar mėnesius. Taip pat nurodote laikotarpių, kuriems užregistruojamas žurnalas, skaičių.

Pakartotinai nuskaityti ir pasidėti operacijos eilutes, galite naudoti su **periodinius žurnalus** puslapis. Juridiniams asmenims – Čekijos Respublikos, Estijos, Vengrijos, Latvijos, Lietuvos, Lenkijos ir Rusijos, ir **periodinius žurnalus** puslapis būtų pratęstas laikotarpiais funkciją split. <!---For more information, see [Create and process a periodic journal](http://ax.help.dynamics.com/en/wiki/create-and-process-a-periodic-journal/).-->

### <a name="example-split-for-periods-in-periodic-journals"></a>Pavyzdys: Split laikotarpių periodiniams žurnalams

Draudimo bendrovės siūlo jūsų organizacijos nuolaidą už prepaying draudimo polisą už visus metus. Mokėjimas registruojamas į turto sąskaitą, pvz., iš anksto sumokėto draudimo. Tada amortizuojate savo mėnesio draudimo išlaidas per metus sukurdami periodinį žurnalą, kuriame yra iš anksto apmokėtos draudimo sąskaitos kreditas ir draudimo išlaidų debetas. Šiuo atveju, galite padalinti laikotarpių funkcionalumą. Spustelėkite į **laikotarpių padalijimas** mygtuką Naujintiveiksmų srityje, **periodinio žurnalo****linijos** psl., ir tada nurodykite šiuos laukus.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**             | **Description**                                                                                                                                                                                             |
| **Start date**        | Pasirinkite datą pirmosios periodinio žurnalo eilutės.                                                                                                                                                        |
| **Number of periods** | Įveskite skaičius laikotarpių, per kurį skaidyti žurnalo eilutės. Ši reikšmė nurodo, kiek naujų operacijų bus generuojama. Operacijos suma paskirstoma tolygiai naujose operacijose. |
| **Unit**              | Pasirinkite matavimo laikotarpiui.                                                                                                                                                                  |
| **Laikotarpių intervalas**   | Nustatyti intervalą nuo registravimo laikotarpius.                                                                                                                                                              |

Pvz., generuoti ketvirtinius pranešimus, įveskite **4**, į **laikotarpių skaičius** srityje, pasirinkite **mėnesių** – į **vieneto** lauko ir **3**, į **laikotarpis** lauko. Sistema sugeneruoja keturis žurnalo eilutes, kiekvienas ketvirtadalis visos žurnalo eilutės suma, kurią įvedėte, kas 3 mėnesius. Panašias funkcijas, taip pat tinka bendrajame žurnale. Kai peržiūrite bendrojo žurnalo eilutes, pasirinkite **laikotarpio leidinyje**&gt;**Išsaugoti žurnalo**.


