---
title: Nusidėvėjimo metodai ir konvencijos
description: Šiame straipsnyje apžvelgiamos nusidėvėjimo konvencijos ir nusidėvėjimo metodai, kuriuos palaiko „Microsoft Dynamics 365 Finance“.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile, AssetGroupBookSetup, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.custom: 3441
ms.assetid: 1d8267b1-86a8-44bf-8814-f56b5d45a0ae
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1aacc57051f21b992d9f7feb44c99511fc2a65bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241295"
---
# <a name="depreciation-methods-and-conventions"></a>Nusidėvėjimo metodai ir konvencijos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamos palaikomos nusidėvėjimo konvencijos ir nusidėvėjimo metodai.

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





<a name="additional-resources"></a>Papildomi ištekliai
--------

[Ilgalaikio turto nusidėvėjimas](fixed-asset-depreciation.md)

[Tiesiogiai proporcingas nusidėvėjimas](Straight-line-service-life-depreciation.md)

[Mažėjančios vertės nusidėvėjimas](reduce-balance-depreciation.md)

[Neautomatinis nusidėvėjimas](manual-depreciation.md)

[Nusidėvėjimas pagal koeficientą](factor-depreciation.md)

[Produkcijos metodas](consumption-depreciation.md)

[Tiesiogiai proporcingas likutinės vertės nusidėvėjimas](straight-line-life-remaining-depreciation.md)

[125 procentų mažėjančios vertės metodas](125-percent-reducing-balance-depreciation.md)

[150 procentų mažėjančios vertės metodas](150-percent-reducing-balance-depreciation.md)

[175 procentų mažėjančios vertės metodas](175-percent-reducing-balance-depreciation.md)

[200 procentų mažėjančios vertės metodas](200-percent-reducing-balance-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]