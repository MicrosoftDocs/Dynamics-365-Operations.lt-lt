---
title: Trumpalaikio išrinkimo elementų perskirstymo nustatymas
description: Šioje procedūroje pateikiama informacija apie tai, kaip įgalinti sandėlio darbuotojus greitai rasti alternatyvias vietas, jei toje vietoje, į kurią jie buvo nukreipti, nėra pakankamai atsargų.
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
ms.openlocfilehash: eae86b307ac8d8539c3897293c2fc21ea57d2d60
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148244"
---
# <a name="set-up-short-picking-item-reallocation"></a>Trumpalaikio išrinkimo elementų perskirstymo nustatymas

[!include [banner](../../includes/banner.md)]

Šioje procedūroje pateikiama informacija apie tai, kaip įgalinti sandėlio darbuotojus greitai rasti alternatyvias vietas, jei toje vietoje, į kurią jie buvo nukreipti, nėra pakankamai atsargų. Galima naudoti automatinį perskirstymo procesą, kuris naudoja vietos direktyvas prekėms gauti, jei jų yra kitoje vietoje. Kitu atveju, kai naudojamas neautomatinis pakartotinis paskirstymas, mobiliajame įrenginyje rodomas vietų su turimu kiekiu sąrašas, todėl sandėlio darbuotojas gali pasirinkti, kurios vietos atsargas naudoti. Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF. Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.


## <a name="set-up-work-exceptions"></a>Nustatyti darbo išimtis
1. **Naršymo srityje** eikite į **Sandėlio valdymas > Sąranka > Darbas > Darbo išimtys**.
2. Spustelėkite **Naujas**. Galima apibrėžti keletą darbo išimčių, naudojant skirtingas elementų perskirstymo strategijas, kad sandėlio darbuotojas galėtų pasirinkti vieną, atsižvelgdamas į siuntos, kurią jis apdoroja, specifikacijas.  
3. Lauke **Darbo išimties kodas** įveskite reikšmę. Sukurkite pavadinimą darbo išimčiai, kad būtų aišku, kam ji naudojama. Pavyzdžiui, Neautomatinis nevisiškas paėmimas.  
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

