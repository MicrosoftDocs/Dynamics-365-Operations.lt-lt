---
title: "Veikiančios vidutinės prekės atsargų dimensijos sekimas"
description: "Atsargų dimensijų grupė pridedama prie kiekvienos atsargų prekės. Todėl einamoji prekės savikaina apskaičiuojama pagal finansiškai sekamas pasirinktas atsargų dimensijas."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-03-31 12 - 51 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f464f94632f7114da5a9cbf34036e4fcb87bcd02
ms.lasthandoff: 03/29/2017


---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>Veikiančios vidutinės prekės atsargų dimensijos sekimas

Atsargų dimensijų grupė pridedama prie kiekvienos atsargų prekės. Todėl einamoji prekės savikaina apskaičiuojama pagal finansiškai sekamas pasirinktas atsargų dimensijas.

Yra trys atsargų dimensijų tipai: produkto, saugojimo ir sekimo. Produkto dimensijos apima konfigūraciją, dydį ir spalvą. Produkto dimensijos visada sekamos finansiškai. Saugojimo ir sekimo dimensijos apima teritoriją, sandėlį, vietą, atsargų būseną, numerio lentelę, paketo numerį ir serijos numerį. Galite nuspręsti, kurias saugojimo ir sekimo dimensijas sekti finansiškai. **1 pavyzdys** Jeigu prie prekės pridėta laikymo dimensijų grupė finansiškai sekama pagal sandėlį, einamoji savikaina apskaičiuojama kiekvienam sandėliui. Išrašytos šių pirkimo užsakymų sąskaitos faktūros:

-   Pirkimo užsakymas, kurio kiekis – 2 prekės, jų savikaina yra 10,00 USD, išrašytas sandėliui GW.
-   Pirkimo užsakymas, kurio kiekis – 3 prekės, jų savikaina yra 12,00 USD, išrašytas sandėliui GW.
-   Pirkimo užsakymas, kurio kiekis – 5 prekės, jų savikaina yra 15,00 USD, išrašytas sandėliui MW.

Einamoji vidutinė sandėlio GW savikaina yra 11,20 USD, o einamoji sandėlio MW savikaina yra 15,00 USD. Sandėliui GW užregistruojama pardavimo užsakymo SF. Atsargų vertė ir parduotų prekių savikaina (prieš atsargų uždarymą ir nepažymėjus) yra 11,20 USD. Sandėliui MW užregistruojamas kitas pardavimo užsakymas. Atsargų vertė ir parduotų prekių savikaina (prieš atsargų uždarymą ir nepažymėjus) yra 15,00 USD. **2 pavyzdys** Jei prie prekės pridėta saugojimo dimensijų grupė finansiškai sekama pagal sandėlį ir sekimo dimensijų grupė finansiškai sekama pagal partijos numerį, einamoji savikaina apskaičiuojama kiekvienam paketui. **Pastaba.** Rekomenduojame visada peržiūrėti visų sekamų finansinių dimensijų savikainą. Išrašytos šių pirkimo užsakymų sąskaitos faktūros:

-   Pirkimo užsakymo, kurio kiekis – 2 prekės, jų savikaina yra 10,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui AAA.
-   Pirkimo užsakymo, kurio kiekis – 3 prekės, jų savikaina yra 12,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui AAA.
-   Pirkimo užsakymo, kurio kiekis – 2 prekės, jų savikaina yra 15,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui BBB.

Einamoji vidutinė sandėlio GW ir paketo AAA savikaina yra 11,20 USD, o einamoji sandėlio MW ir paketo BBB savikaina yra 15,00 USD.


