--- 
title: "Perklasifikuoti ilgalaikį turtą"
description: "Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: 6bce294329c7ec6dc436c3d3baf6597e0283c9bd
ms.contentlocale: lt-lt
ms.lasthandoff: 10/30/2017

---
# <a name="reclassify-fixed-assets"></a>Perklasifikuoti ilgalaikį turtą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį. 

Kai perklasifikuojamas ilgalaikis turtas:

• Visi esamo ilgalaikio turto vertinimo modeliai sukuriami naujam ilgalaikiam turtui. Bet kokia informacija, kuri buvo nustatyta pradiniam ilgalaikiam turtui, yra nukopijuojama naujam ilgalaikiam turtui. Pradinio ilgalaikio turto vertinimo modelių būsena yra Uždaryta. 

• Naujuose ilgalaikio turto vertinimo modeliuose perklasifikavimo data yra lauke Įsigijimo data. Data, esanti lauke Nusidėvėjimo vykdymo data, yra nukopijuota iš pradinės informacijos apie turtą. Jei nusidėvėjimas jau prasidėjo, lauke Paskutinio nusidėvėjimo vykdymo data rodoma perklasifikavimo data. 

• Esamos pradinio ilgalaikio turto operacijos yra atšaukiamos ir iš naujo generuojamos naujam ilgalaikiam turtui.

1. Pasirinkite Ilgalaikis turtas > Periodinės užduotys > Perklasifikavimas.
2. Lauke Ilgalaikio turto grupė pasirinkite grupę, kurią norite perklasifikuoti.
3. Lauke Ilgalaikio turto numeris pasirinkite ilgalaikį turtą, kurį norite perklasifikuoti.
4. Lauke Nauja ilgalaikio turto grupė pasirinkite grupę ilgalaikiam turtui perkelti.
    * Jei naujai ilgalaikio turto grupei pridedama numeracija, naujo ilgalaikio turto numerio lauke atnaujinamas numeris iš naujos ilgalaikio turto grupės numeracijos. Priešingu atveju, naujo ilgalaikio turto numerio lauke atnaujinamas numeris iš numeracijos, nustatytos ilgalaikio turto parametrų puslapyje. Jei numeracija ilgalaikio turto parametrų puslapyje nenustatyta, lauke Naujas ilgalaikio turto numeris įveskite numerį.  
5. Lauke Perklasifikavimo data įveskite datą.
6. Lauke Kvitų serijos įveskite arba pasirinkite reikšmę.
7. Spustelėkite GERAI.


