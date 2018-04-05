---
title: "Nusidėvėjimo metodai ir konvencijos"
description: "Šiame straipsnyje apžvelgiamos nusidėvėjimo konvencijos ir nusidėvėjimo metodai, kuriuos palaiko „Microsoft Dynamics 365 for Finance and Operations“."
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: eb38de1e7e39cb66d15bfe344f6f5fcd5d4fccd7
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="depreciation-methods-and-conventions"></a>Nusidėvėjimo metodai ir konvencijos

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgiamos nusidėvėjimo konvencijos ir nusidėvėjimo metodai, kuriuos palaiko „Microsoft Dynamics 365 for Finance and Operations“.

Galite pasirinkti įvairius nusidėvėjimo metodus bei konvencijas. Metodų paskirtis yra paskirstyti ilgalaikio turto nusidėvėjimo vertę finansiniams laikotarpiams. Ilgalaikio turto nusidėvėjimo vertė yra įsigijimo vertė, sumažėjusi dėl likvidacinės vertės (jei tokia buvo). 

Jei taikote nusidėvėjimo konvenciją ir pakeičiate paskutinio turto nusidėvėjimo datą, dėl kurios praleidžiami keli nusidėvėjimai, praėjusių metų nusidėvėjimas gali būti didesnis arba mažesnis, nei buvo tikėtasi. Nusidėvėjimas yra koreguojamas nusidėvėjimo laikotarpių, kurios paveikė paskutinio nusidėvėjimo datos modifikavimas, skaičiumi.

Pavyzdžiui, jei naudojate pusmečio nusidėvėjimo konvenciją trejus metus, nusidėvėjimas paprastai atsiranda per 3 1/2 metų. Jei pakeičiate paskutinę nusidėvėjimo dieną per 3 1/2 metų, praėjusių metų nusidėvėjimas iškelia paveiktus laikotarpius. Jei datą perkeliate per tris mėnesius, praėję metai turės devynių mėnesių vertės nusidėvėjimą, nors paprastai tai būtų šešių mėnesių vertės nusidėvėjimas.

Galite pasirinkti iš šių nusidėvėjimo konvencijų.


-   Pusmetis
-   Visas mėnuo
-   Ketvirčio vidurys
-   Mėnesio vidurys (mėnesio 1 d.)
-   Mėnesio vidurys (mėnesio 15 d.)
-   Pusė metų (metų pradžia)
-   Pusė metų (kiti metai)

Galite pasirinkti šiuos nusidėvėjimo metodus:
-   Tiesiogiai proporcingas dėvėjimo laikas
-   Mažėjanti vertė
-   Rankiniu būdu
-   Koeficientas
-   Sunaudojimas
-   Likęs tiesiogiai proporcingas laikas
-   200% mažėjanti vertė
-   175% mažėjanti vertė
-   150% mažėjanti vertė
-   125% mažėjanti vertė

 



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Ilgalaikio turto nusidėvėjimas](fixed-asset-depreciation.md)

[Tiesiogiai proporcingas nusidėvėjimas](Straight-line-service-life-depreciation.md)

[Mažėjančios vertės nusidėvėjimas](reduce-balance-depreciation.md)

[Neautomatinis nusidėvėjimas](manual-depreciation.md)

[Nusidėvėjimo faktorius](factor-depreciation.md)

[Produkcijos metodas](consumption-depreciation.md)

[Tiesiogiai proporcingas likutinės vertės nusidėvėjimas](straight-line-life-remaining-depreciation.md)

[125 procentų mažėjančios vertės metodas](125-percent-reducing-balance-depreciation.md)

[150 procentų mažėjančios vertės metodas](150-percent-reducing-balance-depreciation.md)

[175 procentų mažėjančios vertės metodas](175-percent-reducing-balance-depreciation.md)

[200 procentų mažėjančios vertės metodas](200-percent-reducing-balance-depreciation.md)




