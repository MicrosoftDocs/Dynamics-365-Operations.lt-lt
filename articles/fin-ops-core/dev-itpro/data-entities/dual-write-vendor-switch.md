---
title: Vieno tiekėjo dizaino perjungimas į kitą
description: ''
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772369"
---
# <a name="switch-between-vendor-designs"></a>Vieno tiekėjo dizaino perjungimas į kitą

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas 

Jei tiekėjams valdyti naudojate kitas „Dynamics 365” programas ir norite atskirti tiekėjo informaciją nuo klientų, naudokite šį bazinį tiekėjo dizainą.  

![Bazinis tiekėjo srautas](media/dual-write-switch-1.png)
 
Jei tiekėjams valdyti naudojate kitas „Dynamics 365” programas ir norite toliau naudoti objektą **Klientas** tiekėjo informacijai saugoti, naudokite šį išplėstąjį tiekėjo dizainą. Taikant šį dizainą išplėstinė tiekėjo informacija, pvz., tiekėjo sulaikymo būsena ir profilis, saugoma „Common Data Service“ **tiekėjų** objekte. 

![Išplėstinis tiekėjo srautas](media/dual-write-switch-2.png)
 
Norėdami naudoti išplėstinį tiekėjo dizainą, atlikite toliau nurodytus veiksmus. 
 
1. **SupplyChainCommon** sprendimo pakete pateikiami darbo eigos procesų šablonai, kaip parodyta tolesniame vaizde.
    > [!div class="mx-imgBorder"]
    > ![Darbo eigos procesų šablonai](media/dual-write-switch-3.png)
2. Naujus darbo eigos procesus galite kurti naudodami darbo eigos procesų šablonus, kaip nurodyta toliau. 
    1. Naudodami darbo eigos procesą **Kurti tiekėjus kliento objekte**, sukurkite naują objekto **Tiekėjas** darbo eigos procesą ir spustelėkite **Gerai**. Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų kūrimo scenarijus.
        > [!div class="mx-imgBorder"]
        > ![Kurti tiekėjus kliento objekte](media/dual-write-switch-4.png)
    2. Naudodami darbo eigos procesą **Atnaujinti klientų objektą**, sukurkite naują objekto **Tiekėjas** darbo eigos procesą ir spustelėkite **Gerai**. Šia darbo eiga tvarkomas objekto **Klientas** tiekėjų naujinimo scenarijus. 
        > [!div class="mx-imgBorder"]
        > ![Atnaujinti klientų objektą](media/dual-write-switch-5.png)
    3. Sukurkite naujų darbo eigos procesų pagal objekte **Klientai** sukurtus šablonus. 
        > [!div class="mx-imgBorder"]
        > ![Kurti tiekėjus tiekėjų objekte](media/dual-write-switch-6.png)
        > [!div class="mx-imgBorder"]
        > ![Atnaujinti tiekėjų objektą](media/dual-write-switch-7.png)
    4. Darbo eigas pagal poreikius galite konfigūruoti kaip realiuoju laiku vykdomas arba fonines darbo eigas. 
        > [!div class="mx-imgBorder"]
        > ![Konvertavimas į foninę darbo eigą](media/dual-write-switch-8.png)
    5. Norėdami pradėti tiekėjų informaciją saugoti naudojant „Customer Engagement“ objektą **Klientas**, suaktyvinkite darbo eigas, kurias sukūrėte objektuose **Klientas** ir **Tiekėjas**. 
 
