--- 
title: "Ankstesnės veiklos įtraukimas į gamybos eigos veiklą"
description: "Gamybos eigos versijoje visos veiklos turi būti įtrauktos seką."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Ankstesnės veiklos įtraukimas į gamybos eigos veiklą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gamybos eigos versijoje visos veiklos turi būti įtrauktos seką. Veiklai gali būti priskiriama viena arba kelios ankstesnės ar vėlesnės veiklos. 

Šioje procedūroje parodoma, kaip ankstesnę veiklą susieti su veikla. 

Norint atlikti šią užduotį, jums reikalinga juodraščio versijos gamybos eiga su bent dviem veiklomis, kurias galima sujungti. 

Norėdami sužinoti daugiau, skaitykite dokumentą „Lean manufacturing“ gamybos eigos ir veiklos“.


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


