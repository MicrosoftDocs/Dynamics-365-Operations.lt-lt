---
title: Trumpalaikio išrinkimo elementų perskirstymo nustatymas
description: Šioje procedūroje parodoma, kaip sandėlio darbuotojams suteikti galimybę greitai rasti kitų vietų, jei vietoje, į kurią jie buvo nukreipti, atsargų nepakanka.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964302cb7e7835b6e619602ac7165c9e7adbcefb
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916765"
---
# <a name="set-up-short-picking-item-reallocation"></a>Trumpalaikio išrinkimo elementų perskirstymo nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip sandėlio darbuotojams suteikti galimybę greitai rasti kitų vietų, jei vietoje, į kurią jie buvo nukreipti, atsargų nepakanka. Galima naudoti automatinio pakartotinio paskirstymo procesą, kuris naudoja vietos nurodymus prekėms gauti, jei jų yra kitoje vietoje. Kitu atveju, kai naudojamas neautomatinis pakartotinis paskirstymas, mobiliajame įrenginyje rodomas vietų su turimu kiekiu sąrašas, todėl sandėlio darbuotojas gali pasirinkti, kurios vietos atsargas naudoti. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="set-up-work-exceptions"></a>Nustatyti darbo išimtis
1. **Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Darbas > Darbo išimtys**.
2. Spustelėkite **Naujas**. Galima apibrėžti kelias darbo išimtis su skirtingomis prekių perskirstymo strategijomis, norint suteikti sandėlio darbuotojui galimybę strategiją pasirinkti pagal su jo apdorojama siunta susijusius poreikius.  
3. Lauke **Darbo išimties kodas** įveskite reikšmę. Nurodykite darbo išimties pavadinimą nurodydami, kam ji naudojama. Pavyzdžiui, Neautomatinis nevisiškas paėmimas.  
4. Lauke **Aprašo laukas**surinkite reikšmę.
5. Lauke **Išimties tipas** pasirinkite Nevisiškas paėmimas.
6. Pažymėkite žymės langelį **Koreguoti atsargas**. Ši parinktis nurodo, kad atsargų lygis bus automatiškai nustatytas į 0 vietoje, iš kurioje bus vykdomas nevisiškas paėmimas.  
7. Lauke **Numatytojo koregavimo tipo kodas** įveskite arba pasirinkite reikšmę. Pavyzdžiui, USMF galite pasirinkti Šalinti Res Adj Out.  
8. Lauke **Prekių perskirstymas** pasirinkite Neautomatinis. Jei pasirinksite Neautomatinis arba Automatinis ir neautomatinis, sandėlio darbuotojui reikia įjungti neautomatinio perskirstymo funkciją.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Darbuotojo nustatymas naudoti neautomatinį perskirstymą
1. Uždarykite puslapį.
2. **Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Darbuotojas**.
3. Spustelėkite **Redaguoti**.
4. Sąraše pasirinkite 24 darbuotoją.
5. Išplėskite „fastTab“ **Darbas**.
6. Lauke **Leisti neautomatinį prekių perskirstymą** pasirinkite Taip.

