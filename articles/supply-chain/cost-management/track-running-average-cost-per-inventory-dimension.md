---
title: Veikiančios vidutinės prekės atsargų dimensijos sekimas
description: Atsargų dimensijų grupė pridedama prie kiekvienos atsargų prekės. Todėl einamoji prekės savikaina apskaičiuojama pagal finansiškai sekamas pasirinktas atsargų dimensijas.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8da13a01b28ca09ce9c29ecd3a9342dfb9eaa4bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834318"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a>Veikiančios vidutinės prekės atsargų dimensijos sekimas

[!include [banner](../includes/banner.md)]

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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]