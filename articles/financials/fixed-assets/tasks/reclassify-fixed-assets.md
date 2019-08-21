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
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47d8cf2ff1e275df0466a7fe327a3180c0399e49
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839934"
---
# <a name="reclassify-fixed-assets"></a>Perklasifikuoti ilgalaikį turtą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį. 

Kai perklasifikuojamas ilgalaikis turtas:

• Visos esamo ilgalaikio turto knygos sukuriamos naujam ilgalaikiam turtui. Bet kokia informacija, kuri buvo nustatyta pradiniam ilgalaikiam turtui, yra nukopijuojama naujam ilgalaikiam turtui. Pradinio ilgalaikio turto knygų būsena yra Uždaryta. 

• Naujose ilgalaikio turto knygose perklasifikavimo data yra lauke **Įsigijimo data**. Data, esanti lauke **Nusidėvėjimo vykdymo data**, yra nukopijuota iš pradinės informacijos apie turtą. Jei nusidėvėjimas jau prasidėjo, lauke **Paskutinio nusidėvėjimo vykdymo data** rodoma perklasifikavimo data. 

• Esamos pradinio ilgalaikio turto operacijos yra atšaukiamos ir iš naujo generuojamos naujam ilgalaikiam turtui.

Atlikite šiuos veiksmus, norėdami perklasifikuoti ilgalaikį turtą:

1. Pasirinkite **Ilgalaikis turtas > Periodinės užduotys > Perklasifikavimas.**
2. Lauke **Ilgalaikio turto grupė** pasirinkite grupę, kurią norite perklasifikuoti.
3. Lauke **Ilgalaikio turto numeris** pasirinkite ilgalaikį turtą, kurį norite perklasifikuoti.
4. Lauke **Nauja ilgalaikio turto grupė** pasirinkite grupę ilgalaikiam turtui perkelti.
    * Jei naujai ilgalaikio turto grupei pridedama numeracija, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš naujos ilgalaikio turto grupės numeracijos. Priešingu atveju, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš numeracijos, nustatytos **ilgalaikio turto parametrų** puslapyje. Jei numeracija **ilgalaikio turto parametrų** puslapyje nenustatyta, lauke **Naujas ilgalaikio turto numeris** įveskite numerį.  
5. Lauke **Perklasifikavimo data** įveskite datą.
6. Lauke **Kvitų serijos** įveskite arba pasirinkite reikšmę.
7. Spustelėkite **Gerai**.
