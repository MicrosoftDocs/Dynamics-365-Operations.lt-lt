---
title: Standartinių savikainos atnaujinimų valdymas
description: 'Standartinių savikainos atnaujinimų duomenis galima valdyti dviem būdais: vienos versijos būdu arba dviejų versijų būdu.'
author: AndersGirke
manager: tfehr
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a7beeafa6d0bb22a687278ccebc3127409e1ee0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433646"
---
# <a name="manage-standard-cost-updates"></a>Standartinių savikainos atnaujinimų valdymas

[!include [banner](../includes/banner.md)]

Standartinių savikainos atnaujinimų duomenis galima valdyti dviem būdais: vienos versijos būdu arba dviejų versijų būdu. 

Vienos versijos būdui naudojama viena savikainos nustatymo versija, kurioje įtraukiama visų išlaidų apskaita. Šie įrašai apima pradinę savikainą ir visus savikainos atnaujinimus.

Dviejų versijų būdui naudojama viena versija, kurioje yra pradinės savikainos įrašai, ir antroji versija, kurioje yra visų savikainos atnaujinimų įrašai. Svarbiausias dviejų versijų būdo pranašumas yra aiškus savikainų naujinimų apibrėžimas ir sekimas atskirose įkainojimo versijose, neįtakojant originalios įkainojimo versijos. Dviejų versijų principas gali būti naudojamas identifikuoti kelis papildančiuosius naujinimus, kur kiekvienas papildantysis naujinimas turi atskirą įkainojimo versiją, susidedančią iš papildančiosios savikainos įrašų. 

**Pavyzdys** 

Šiame pavyzdyje parodyta, kaip galima naudoti vienos ir dviejų versijų būdus standartinėms savikainoms gamybinėje aplinkoje naujinti. Pavyzdžiui, atnaujinimai, atspindintys naujus elementus arba klaidų pataisymus. Tarkime, kad vienos versijos įkainojimas apima standartinę savikainą einamiesiems metams. Šios versijos identifikatorius yra 2016-STD. Versija 2016-STD apima esamas aktyvias visų elementų savikainas. Be to, ją sudaro visų su paskirstymu susijusių savikainų kategorijos ir pridėtinių išlaidų skaičiavimo formulės kurios yra žinomos 2016 m. pradžioje. 2016-STD yra pradinė savikainos nustatymo versija.

-   **Savikainos duomenų naujinimo vienos versijos būdas** − Vienos versijos būdas reiškia, kad originalioje įkainojimo versijoje 2016-STD bus visi savikainos įrašai. Savikainos atnaujinimai yra įrašyti 2016-STD ir nustatyti „Laukiama“ būsenai. Naujai įsigytų prekių laukiamą savikainą galima įvesti neautomatiškai arba apskaičiuoti pagamintos prekės savikainą, siekiant atspindėti pataisymus. Naudojant vienos versijos būdą, KS skaičiavimams atlikti nereikalingas atsarginis duomenų šaltinis, nes visos aktyvios savikainos yra įkainojimo versijoje. Aktyvavus laukiančiąsias savikainas, originali įkainojimo versija 2016-STD dar kartą įtrauks visas esamas aktyvias savikainas.
-   **Savikainos duomenų naujinimo dviejų versijų būdas** − dviejų versijų būdui reikia papildomų sąnaudų versijos kurioje yra tik sąnaudų atnaujinimai. Šios versijos identifikatorius yra 2016-STD-CHANGES. Savikainos atnaujinimai yra įrašyti 2016-STD-CHANGES ir jiems nustatyta būsena „Laukiama“. Naudojant dviejų versijų būdą, pagamintų prekių KS laukiančių sąnaudų skaičiavimams atlikti reikalingas atsarginis duomenų šaltinis. Taip yra todėl, papildoma savikainos nustatymo versija 2016-STD-CHANGES turi tik savikainos duomenų poaibį. Atsarginis skaičiavimas gali būti išreikštas kaip aktyvi savikaina ar kaip įkainojimo versija 2016-STD, nes abi jos nustato savikainos duomenų šaltinį, kurio 2016-STD-CHANGES nėra. Aktyvavus laukiančiąsias savikainas, įkainojimo versijoje 2016-STD-CHANGES bus esančios aktyvios savikainos, kuriose atsižvelgta į naujinimus, o originali įkainojimo versija 2016-STD liks nepakeista. Kai naudojamas dviejų versijų būdas, originalios įkainojimo versijos blokuojančiosios strategijos nustatomos taip, kad uždraustų naujinimus. Identišką blokavimo politiką reikia nustatyti papildomai savikainos nustatymo versijai, išskyrus nurodytą nuo-datos ir pasirinktinį blokavimo politikos naudojimą, kad būtų galima atlikti atnaujinimus. Nurodyta pradžios data turi būti atnaujinta kiekvienam pakeitimų paketui, kad atspindėtų suplanuotą aktyvinimo datą.

Šiame pavyzdyje naudojama viena papildoma įkainojimo versija naujinimų valdymui 2016 m. Gali būti naudojama daugiau nei viena papildoma įkainojimo versija, pavyzdžiui, atskira versija kiekvienam naujinimo paketui. Kai naudojamas daugiau nei vienas papildomas sąnaudų skaičiavimas, atsarginius duomenis reikia išreikšti kaip aktyvią savikainą, nes aktyvi savikaina paskirstoma kelioms savikainos versijoms.





