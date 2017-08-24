--- 
title: "Trumpalaikio išrinkimo elementų perskirstymo nustatymas"
description: "Šioje procedūroje parodoma, kaip sandėlio darbuotojams suteikti galimybę greitai rasti kitų vietų, jei vietoje, į kurią jie buvo nukreipti, atsargų nepakanka."
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedd815cddfea4e00ed61ec6e176b633468c8fb2
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Trumpalaikio išrinkimo elementų perskirstymo nustatymas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip sandėlio darbuotojams suteikti galimybę greitai rasti kitų vietų, jei vietoje, į kurią jie buvo nukreipti, atsargų nepakanka. Galima naudoti automatinio pakartotinio paskirstymo procesą, kuris naudoja vietos nurodymus prekėms gauti, jei jų yra kitoje vietoje. Kitu atveju, kai naudojamas neautomatinis pakartotinis paskirstymas, mobiliajame įrenginyje rodomas vietų su turimu kiekiu sąrašas, todėl sandėlio darbuotojas gali pasirinkti, kurios vietos atsargas naudoti. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="set-up-work-exceptions"></a>Nustatyti darbo išimtis
1. Eikite į Sandėlio valdymas > Sąranka > Darbas > Darbo išimtys.
2. Spustelėkite Naujas.
    * Galima apibrėžti kelias darbo išimtis su skirtingomis prekių perskirstymo strategijomis, norint suteikti sandėlio darbuotojui galimybę strategiją pasirinkti pagal su jo apdorojama siunta susijusius poreikius.  
3. Lauke Darbo išimties kodas įveskite reikšmę.
    * Nurodykite darbo išimties pavadinimą nurodydami, kam ji naudojama. Pavyzdžiui, Neautomatinis nevisiškas paėmimas.  
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Išimties tipas pasirinkite Nevisiškas paėmimas.
6. Pasirinkite žymės langelį Koreguoti atsargas.
    * Ši parinktis nurodo, kad atsargų lygis bus automatiškai nustatytas į 0 vietoje, iš kurioje bus vykdomas nevisiškas paėmimas.  
7. Lauke Numatytasis koregavimo tipo kodas įveskite arba pasirinkite reikšmę.
    * Pavyzdžiui, USMF galite pasirinkti Šalinti Res Adj Out.  
8. Lauke Prekės perskirstymas pasirinkite Neautomatinis.
    * Jei pasirinksite Neautomatinis arba Automatinis ir neautomatinis, sandėlio darbuotojui reikia įjungti neautomatinio perskirstymo funkciją.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Darbuotojo nustatymas naudoti neautomatinį perskirstymą
1. Uždarykite puslapį.
2. Eikite į Sandėlio valdymas > Sąranka > Darbininkas.
3. Spustelėkite Redaguoti.
4. Sąraše pasirinkite 24 darbuotoją.
5. Išplėskite skyrių Darbas.
6. Lauke Leisti paskirstyti prekes neautomatiškai pasirinkite Taip.


