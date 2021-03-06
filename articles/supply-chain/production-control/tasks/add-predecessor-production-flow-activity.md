---
title: Ankstesnės veiklos įtraukimas į gamybos eigos veiklą
description: Gamybos eigos versijoje visos veiklos turi būti įtrauktos seką.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 968880db317f74db6bc6d92a4beca9136c0d8de4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825067"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Ankstesnės veiklos įtraukimas į gamybos eigos veiklą

[!include [banner](../../includes/banner.md)]

Gamybos eigos versijoje visos veiklos turi būti įtrauktos seką. Veiklai gali būti priskiriama viena arba kelios ankstesnės ar vėlesnės veiklos. 

Šioje procedūroje parodoma, kaip ankstesnę veiklą susieti su veikla. 

Norint atlikti šią užduotį, jums reikalinga juodraščio versijos gamybos eiga su bent dviem veiklomis, kurias galima sujungti. 

Norėdami sužinoti daugiau, skaitykite dokumentą „Gamybos eigos ir veiklos LEAN gamyboje.“


## <a name="find-the-production-flow-and-version"></a>Kaip rasti gamybos eigą ir versiją
1. Pasirinkite Gamybos kontrolė > Nustatymai > „Lean“ gamybos eiga > Gamybos eigos.
2. Sąraše raskite ir pasirinkite norimą įrašą.
3. Sąraše spustelėkite saitą pasirinktoje eilutėje.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Spustelėkite Veiklos.

## <a name="select-an-activity-and-add-a-predecessor"></a>Veiklos pasirinkimas ir ankstesnės veiklos įtraukimas
1. Sąraše raskite ir pasirinkite norimą įrašą.
2. Spustelėkite Įtraukti ankstesnę veiklą.
3. Lauke Veikla įveskite arba pasirinkite reikšmę.
4. Lauke Ciklo laiko koeficientas įveskite skaičių.
    * Numatytasis veiklos ryšio ciklo laiko koeficientas yra 1. Tai reiškia, kad abi veiklos yra vykdomos tuo pačiu tempu ir jų vieneto gamybos laikai sutampa. Jei ankstesnė veikla vykdoma didesniu tempu (trumpesnis vieneto gamybos laikas), koeficientas turėtų būti mažesnis už 1, jei ankstesnė veikla vykdoma mažesniu tempu (ilgesnis vieneto gamybos laikas), ciklo laiko koeficientas yra didesnis už 1.  
5. Spustelėkite GERAI.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]