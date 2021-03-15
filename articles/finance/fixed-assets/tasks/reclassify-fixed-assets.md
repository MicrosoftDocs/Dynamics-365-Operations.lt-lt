---
title: Perklasifikuoti ilgalaikį turtą
description: Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cfc1425aca7a62205e0c7c50237f206a179a0e7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968859"
---
# <a name="reclassify-fixed-assets"></a>Perklasifikuoti ilgalaikį turtą

[!include [banner](../../includes/banner.md)]

Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį. 

Kai perklasifikuojamas ilgalaikis turtas:

* Visos esamo ilgalaikio turto knygos sukuriamos naujam ilgalaikiam turtui. Bet kokia informacija, kuri buvo nustatyta pradiniam ilgalaikiam turtui, yra nukopijuojama naujam ilgalaikiam turtui. Pradinio ilgalaikio turto knygų būsena yra Uždaryta. 

* Naujose ilgalaikio turto knygose perklasifikavimo data yra lauke **Įsigijimo data**. Data, esanti lauke **Nusidėvėjimo vykdymo data**, yra nukopijuota iš pradinės informacijos apie turtą. Jei nusidėvėjimas jau prasidėjo, lauke **Paskutinio nusidėvėjimo vykdymo data** rodoma perklasifikavimo data. 

* Esamos pradinio ilgalaikio turto operacijos yra atšaukiamos ir iš naujo generuojamos naujam ilgalaikiam turtui.

Atlikite šiuos veiksmus, norėdami perklasifikuoti ilgalaikį turtą:

1. Pasirinkite **Ilgalaikis turtas > Periodinės užduotys > Perklasifikavimas.**
2. Lauke **Ilgalaikio turto grupė** pasirinkite grupę, kurią norite perklasifikuoti.
3. Lauke **Ilgalaikio turto numeris** pasirinkite ilgalaikį turtą, kurį norite perklasifikuoti.
4. Lauke **Nauja ilgalaikio turto grupė** pasirinkite grupę ilgalaikiam turtui perkelti.
    * Jei naujai ilgalaikio turto grupei pridedama numeracija, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš naujos ilgalaikio turto grupės numeracijos. Priešingu atveju, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš numeracijos, nustatytos **ilgalaikio turto parametrų** puslapyje. Jei numeracija **ilgalaikio turto parametrų** puslapyje nenustatyta, lauke **Naujas ilgalaikio turto numeris** įveskite numerį.  
5. Lauke **Perklasifikavimo data** įveskite datą.
6. Lauke **Kvitų serijos** įveskite arba pasirinkite reikšmę.
7. Spustelėkite **Gerai**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]