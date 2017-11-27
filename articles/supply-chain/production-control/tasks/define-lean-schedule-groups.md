--- 
title: "Nustatyti pažangiosios gamybos planavimo grupes"
description: "Pažangiosios gamybos planavimo grupės apibrėžtos grupuoti ir atskirti produktus iš „kanban“ planavimo."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3e07fa270b47be3527c572dc53ca30a7bcde5ba6
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---
# <a name="define-lean-schedule-groups"></a>Nustatyti pažangiosios gamybos planavimo grupes

[!include[task guide banner](../../includes/task-guide-banner.md)]

Pažangiosios gamybos planavimo grupės apibrėžtos grupuoti ir atskirti produktus iš „kanban“ planavimo. Grupavimą galima atlikti kaip bendrąjį susiejimą visoje įmonėje arba būdingą darbo elementui. Kiekviena grupė turi spalvos kodą, priskirtą vizualiai nurodyti „kanban“ planavimo sąrašo puslapyje. Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.


## <a name="define-lean-scheduling-group"></a>Apibrėžti pažangiosios gamybos planavimo grupę
1. Eikite į Produkto informacijos valdymas > „Lean manufacturing“ > Pažangiosios gamybos planavimo grupės.
2. Spustelėkite Naujas.
3. Lauke Grafiko grupė įveskite vertę.
    * Planavimo grupę galima apibrėžti kaip visuotinę grupę arba būdingą darbo elementui. Šiame paprastame pavyzdyje nustatėme visuotinę grupę, o darbo elementą palikome tuščią. Šios grupės nustatymai taikomi visiems darbo elementams, kurie neturi tam tikrų planavimo grupių.  
4. Iš spalvų pasirinkimo pasirinkite spalvą.
    * Spalvos naudojamos išryškinti užduotis „kanban“ grafiko sąrašo puslapyje ar „kanban“ proceso srityje.  
5. Sąraše pažymėkite pasirinktą eilutę.
6. Sąraše spustelėkite saitą pasirinktoje eilutėje.

## <a name="associate-product"></a>Susieti produktą
1. Susieti konkretų produktą
    * Yra du būdai susieti produktus su pažangiosios gamybos planavimo grupėmis: arba kaip konkretų produktą (Prekės ryšio tipas = Prekė), arba kaip prekių paskirstymo raktą (prekės ryšio tipas = grupė).    
2. Lauke Prekės ryšio tipas pasirinkite Prekė
3. Lauke Prekės numeris surinkite reikšmę.
4. Lauke Našumo dažnis įveskite skaičių.
    * Numatytasis Našumo koeficientas yra 1, tai reiškia, kad susijusiems produktams suvartojamas tiksliai toks pajėgumas, koks nurodytas gamybos eigos proceso veikloje. Našumo santykis > 1 nurodo didesnį išteklių suvartojimą, Našumo koeficientas < 1 nurodo mažesnį išteklių suvartojimą. Koeficientas naudojamas skaičiuojant savikainą ir „kanban“ užduoties suvartojimui skaičiuoti.  

## <a name="associate-item-allocation-key"></a>Susieti prekių paskirstymo raktą
1. Susieti prekių paskirstymo raktą
    * Į prekių paskirstymo raktą įtraukite sąsają naudodami prekės ryšio tipą Grupė.   Atkreipkite dėmesį, kad šiam procesui reikia, kad jūsų duomenyse būtų nustatyta prekių paskirstymo rakto prognozė.  
2. Lauke Prekės ryšio tipas pasirinkite Grupė
3. Lauke Prekės susiejimo raktas spustelėję išplečiamąjį mygtuką atidarykite peržvalgą.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.


