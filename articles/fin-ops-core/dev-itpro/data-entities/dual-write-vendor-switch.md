---
title: Perjungti iš vieno tiekėjo dizaino į kitą
description: Šioje temoje aprašoma, kaip perjungti tiekėjo duomenų integravimą tarp „Finance and Operations“ programų ir „Common Data Service“.
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
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902730"
---
# <a name="switch-between-vendor-designs"></a>Perjungti iš vieno tiekėjo dizaino į kitą

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a>Tiekėjo duomenų srautas 

Jei tiekėjams valdyti naudojate kitas „Dynamics 365” programas ir norite atskirti tiekėjo informaciją nuo klientų, naudokite šį bazinį tiekėjo dizainą.  

![Bazinis tiekėjo srautas](media/dual-write-vendor-data-flow.png)
 
Jei tiekėjams valdyti naudojate kitas „Dynamics 365” programas ir norite toliau naudoti objektą **Klientas** tiekėjo informacijai saugoti, naudokite šį išplėstąjį tiekėjo dizainą. Taikant šį dizainą išplėstinė tiekėjo informacija, pvz., tiekėjo sulaikymo būsena ir profilis, saugoma „Common Data Service“ **tiekėjų** objekte. 

![Išplėstinis tiekėjo srautas](media/dual-write-vendor-detail.jpg)
 
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
    5. Norėdami pradėti tiekėjų informaciją saugoti naudojant objektą **Klientas**, suaktyvinkite darbo eigas, kurias sukūrėte objektuose **Klientas** ir **Tiekėjas**. 
 
