---
title: Perklasifikuoti ilgalaikį turtą
description: Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį.
author: saraschi2
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fbfb754459fad1f3b1509f4f9c65c20e0385b013
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944719"
---
# <a name="reclassify-fixed-assets"></a>Perklasifikuoti ilgalaikį turtą

[!include [banner](../../includes/banner.md)]

Norėdami perklasifikuoti ilgalaikį turtą, turite perkelti jį į naują ilgalaikio turto grupę arba toje pačioje grupėje priskirti jam naują ilgalaikio turto numerį. 

Kai perklasifikuojamas ilgalaikis turtas:

- Visos esamo ilgalaikio turto knygos sukuriamos naujam ilgalaikiam turtui. Bet kokia informacija, kuri buvo nustatyta pradiniam ilgalaikiam turtui, yra nukopijuojama naujam ilgalaikiam turtui. Pradinio ilgalaikio turto knygų būsena yra Uždaryta. 

- Naujose ilgalaikio turto knygose perklasifikavimo data yra lauke **Įsigijimo data**. Data, esanti lauke **Nusidėvėjimo vykdymo data**, yra nukopijuota iš pradinės informacijos apie turtą. Jei nusidėvėjimas jau prasidėjo, lauke **Paskutinio nusidėvėjimo vykdymo data** rodoma perklasifikavimo data. 

- Esamos pradinio ilgalaikio turto operacijos yra atšaukiamos ir iš naujo generuojamos naujam ilgalaikiam turtui.

- Perklasifikuota, kai perkėlimo operacija yra perklasifikuota, sistema veiksmų centre rodys pranešimą, nurodantį, kad perkėlimo operacija nebuvo įvykdyta **perklasifikavimo** proceso metu. Būtina užbaigti perkėlimo operaciją, kad esamos perklasifikavimo operacijos būtų perkeltos į atitinkamas finansines dimensijas. 

   Perklasifikavimo proceso metu sistema vykdo toliau nurodytus veiksmus, kad perklasifikuos turto balansą iš pradinio turto į naują turtą. 
   
   - Perklasifikavimo proceso metu duomenys nukopijuojami iš pradinės ilgalaikio turto knygos į naują ilgalaikio turto knygą.

   - Perklasifikavimo operacija naudoja pradinio užregistruoto įsigijimo informaciją, kuri apima finansinės dimensijos informaciją, įtrauktą į įsigijimo operaciją.  
   
   - Tuo pat metu perklasifikavimo procesas atšaukia pradinio turto įsigijimo ir turto perkėlimo operaciją. 

Šioje diagramoje ir procedūroje pateikiamas perklasifikavimo proceso pavyzdys. 

[![Perklasifikavimo proceso diagrama](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Atlikite šiuos veiksmus, norėdami perklasifikuoti ilgalaikį turtą:

1. Pasirinkite **Ilgalaikis turtas > Periodinės užduotys > Perklasifikavimas.**
2. Lauke **Ilgalaikio turto grupė** pasirinkite grupę, kurią norite perklasifikuoti.
3. Lauke **Ilgalaikio turto numeris** pasirinkite ilgalaikį turtą, kurį norite perklasifikuoti.
4. Lauke **Nauja ilgalaikio turto grupė** pasirinkite grupę ilgalaikiam turtui perkelti.
    * Jei naujai ilgalaikio turto grupei pridedama numeracija, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš naujos ilgalaikio turto grupės numeracijos. Priešingu atveju, **naujo ilgalaikio turto numerio** lauke atnaujinamas numeris iš numeracijos, nustatytos **ilgalaikio turto parametrų** puslapyje. Jei numeracija **ilgalaikio turto parametrų** puslapyje nenustatyta, lauke **Naujas ilgalaikio turto numeris** įveskite numerį.  
5. Lauke **Perklasifikavimo data** įveskite datą.
6. Lauke **Kvitų serijos** įveskite arba pasirinkite reikšmę.
7. Pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
