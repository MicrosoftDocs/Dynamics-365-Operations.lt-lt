---
title: "Tvarkyti normatyvinę savikainą naujinimus"
description: "Normatyvinė savikaina duomenų atnaujinimai gali būti valdomas naudojant du skirtingi požiūriai - vieno versija metodu ir dvi versijos metodu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7e0f0817ff37c82ed98a51f10bcdde7e785a19a3
ms.lasthandoff: 03/31/2017


---

# <a name="manage-standard-cost-updates"></a>Tvarkyti normatyvinę savikainą naujinimus

Normatyvinė savikaina duomenų atnaujinimai gali būti valdomas naudojant du skirtingi požiūriai - vieno versija metodu ir dvi versijos metodu. 

Vienos versijos būdui naudojama viena savikainos nustatymo versija, kurioje įtraukiama visų išlaidų apskaita. Šie įrašai apima pradinę savikainą ir visus savikainos atnaujinimus.
Dviejų versijų būdui naudojama viena versija, kurioje yra pradinės savikainos įrašai, ir antroji versija, kurioje yra visų savikainos atnaujinimų įrašai. Svarbiausias dviejų versijų būdo pranašumas yra aiškus savikainų naujinimų apibrėžimas ir sekimas atskirose įkainojimo versijose, neįtakojant originalios įkainojimo versijos. Dviejų versijų principas gali būti naudojamas identifikuoti kelis papildančiuosius naujinimus, kur kiekvienas papildantysis naujinimas turi atskirą įkainojimo versiją, susidedančią iš papildančiosios savikainos įrašų. **Pavyzdys** Šis pavyzdys rodo, kaip galima naudoti vienos ir dviejų versijų būdus standartiniam savikainos naujinimui, pavyzdžiui, savikainos naujinimui gamybinėje aplinkoje. Pavyzdžiui, atnaujinimai, atspindintys naujus elementus arba klaidų pataisymus. Tarkime, kad vienos versijos įkainojimas apima standartinę savikainą einamiesiems metams. Šios versijos identifikatorius yra 2016-STD. Versija 2016-STD apima esamas aktyvias visų elementų savikainas. Be to, jame yra visos technologinės kortelės susijusių išlaidų kategorijas ir pridėtinių išlaidų apskaičiavimo formulės, kurios buvo žinomos 2016 metų pradžioje. 2016-STD yra originalus įkainojimo versijos.
-   **Savikainos duomenų naujinimo vienos versijos būdas** − Vienos versijos būdas reiškia, kad originalioje įkainojimo versijoje 2016-STD bus visi savikainos įrašai. Ekonomiškai naujinimai įrašomi į 2016-STD ir nustatytos kaip būsena "Laukiama". Laukiama išlaidų galima rankiniu būdu įvesti naują nupirktų prekių arba jie galima apskaičiuoti prekei pagaminti atspindi pataisymus. Kai viena versija metodas, skaičiuojant KS nereikia originalo duomenų šaltinio nes visos aktyvios išlaidos yra įtrauktos įkainojimo versijoje. Aktyvavus laukiančiąsias savikainas, originali įkainojimo versija 2016-STD dar kartą įtrauks visas esamas aktyvias savikainas.
-   **Savikainos duomenų naujinimo dviejų versijų būdas** − dviejų versijų būdui reikia papildomų sąnaudų versijos kurioje yra tik sąnaudų atnaujinimai. Šios versijos identifikatorius yra 2016-STD-CHANGES. Sąnaudų atnaujinimai fiksuojami 2016-STD-CHANGES ir nustatomi „Laukiama“ būsenai. Naudojant dviejų versijų būdą, pagamintų gaminių KS laukiančių sąnaudų skaičiavimams reikia atsarginio duomenų šaltinio. Taip yra todėl, papildoma savikainos nustatymo versija 2016-STD-CHANGES turi tik savikainos duomenų poaibį. Atsarginis skaičiavimas gali būti išreikštas kaip aktyvi savikaina ar kaip įkainojimo versija 2016-STD, nes abi jos nustato savikainos duomenų šaltinį, kurio 2016-STD-CHANGES nėra. Laukiančioms išlaidoms tapus aktyvioms, įkainojimo versijoje 2016-STD-KEITIMAI bus dabartinės aktyvios išlaidos, atspindinčios naujinimus, o pradinė įkainojimo versija 2016-STD bus nepakeista. Kai naudojamas dviejų versijų būdas, reikėtų nustatyti pradinės įkainojimo versijos blokavimo strategijas, kad nebūtų naujinama. Identišką blokavimo politiką reikia nustatyti papildomai savikainos nustatymo versijai, išskyrus nurodytą nuo-datos ir pasirinktinį blokavimo politikos naudojimą, kad būtų galima atlikti atnaujinimus. Nurodyta pradžios data turi būti atnaujinta kiekvienam pakeitimų paketui, kad atspindėtų suplanuotą aktyvinimo datą.

Šiame pavyzdyje naudojamas vienas papildomas įkainojimo versijos valdymo atnaujinimai visą 2016 metais. Daugiau nei vieną papildomą įkainojimo versija gali būti naudojama kaip atskira versija kiekvienos partijos naujinimų. Kai naudojamas daugiau nei vienas papildomas sąnaudų skaičiavimas, atsarginius duomenis reikia išreikšti kaip aktyvią savikainą, nes aktyvi savikaina paskirstoma kelioms savikainos versijoms.




