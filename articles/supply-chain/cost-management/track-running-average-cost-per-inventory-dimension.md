---
title: "Veikiančios vidutinės prekės atsargų dimensijos sekimas"
description: "Atsargų dimensijų grupė pridedama prie kiekvienos atsargų prekės. Todėl einamoji prekės savikaina apskaičiuojama pagal finansiškai sekamas pasirinktas atsargų dimensijas."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 48db7ff047a50343bd473d2c71f878e4ee2201e5
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="track-running-average-cost-per-inventory-dimension"></a>Veikiančios vidutinės prekės atsargų dimensijos sekimas

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

Atsargų dimensijų grupė pridedama prie kiekvienos atsargų prekės. Todėl einamoji prekės savikaina apskaičiuojama pagal finansiškai sekamas pasirinktas atsargų dimensijas.

Yra trys atsargų dimensijų tipai: produkto, saugojimo ir sekimo. Produkto dimensijos apima konfigūraciją, dydį ir spalvą. Produkto dimensijos visada sekamos finansiškai. Saugojimo ir sekimo dimensijos apima teritoriją, sandėlį, vietą, atsargų būseną, numerio lentelę, paketo numerį ir serijos numerį. Galite nuspręsti, kurias saugojimo ir sekimo dimensijas sekti finansiškai. 

**1 pavyzdys** 

Jei prie prekės pridėta laikymo dimensijų grupė finansiškai sekama pagal sandėlį, apskaičiuojama kiekvieno sandėlio naudojama savikaina. Išrašytos šių pirkimo užsakymų sąskaitos faktūros:

-   Pirkimo užsakymas, kurio kiekis – 2 prekės, jų savikaina yra 10,00 USD, išrašytas sandėliui GW.
-   Pirkimo užsakymas, kurio kiekis – 3 prekės, jų savikaina yra 12,00 USD, išrašytas sandėliui GW.
-   Pirkimo užsakymas, kurio kiekis – 5 prekės, jų savikaina yra 15,00 USD, išrašytas sandėliui MW.

Einamoji vidutinė sandėlio GW savikaina yra 11,20 USD, o einamoji sandėlio MW savikaina yra 15,00 USD. Sandėliui GW užregistruojama pardavimo užsakymo SF. Atsargų vertė ir parduotų prekių savikaina (prieš atsargų uždarymą ir nepažymėjus) yra 11,20 USD. Sandėliui MW užregistruojamas kitas pardavimo užsakymas. Atsargų vertė ir parduotų prekių savikaina (prieš atsargų uždarymą ir nepažymėjus) yra 15,00 USD. 

**2 pavyzdys** Jei prie prekės pridėta saugojimo dimensijų grupė finansiškai sekama pagal sandėlį ir sekimo dimensijų grupė finansiškai sekama pagal partijos numerį, einamoji savikaina apskaičiuojama kiekvienam paketui. 

**Pastaba.** Rekomenduojame visada peržiūrėti visų sekamų finansinių dimensijų savikainą. Išrašytos šių pirkimo užsakymų sąskaitos faktūros:

-   Pirkimo užsakymo, kurio kiekis – 2 prekės, jų savikaina yra 10,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui AAA.
-   Pirkimo užsakymo, kurio kiekis – 3 prekės, jų savikaina yra 12,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui AAA.
-   Pirkimo užsakymo, kurio kiekis – 2 prekės, jų savikaina yra 15,00 USD, sąskaita faktūra išrašyta sandėliui GW ir paketui BBB.

Einamoji vidutinė sandėlio GW ir paketo AAA savikaina yra 11,20 USD, o einamoji sandėlio MW ir paketo BBB savikaina yra 15,00 USD.




