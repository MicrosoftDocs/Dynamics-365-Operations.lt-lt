---
title: "Standartinių savikainos atnaujinimų valdymas"
description: "Standartinių savikainos atnaujinimų duomenis galima valdyti dviem būdais: vienos versijos būdu ir dviejų versijų būdu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4a87a12b914fd16e0478cc898c4d53dba0ba0ebe
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="manage-standard-cost-updates"></a>Standartinių savikainos atnaujinimų valdymas

[!include[banner](../includes/banner.md)]


Standartinių savikainos atnaujinimų duomenis galima valdyti dviem būdais: vienos versijos būdu ir dviejų versijų būdu. 

Vienos versijos būdui naudojama viena savikainos nustatymo versija, kurioje įtraukiama visų išlaidų apskaita. Šie įrašai apima pradinę savikainą ir visus savikainos atnaujinimus.
Dviejų versijų būdui naudojama viena versija, kurioje yra pradinės savikainos įrašai, ir antroji versija, kurioje yra visų savikainos atnaujinimų įrašai. Svarbiausias dviejų versijų būdo pranašumas yra aiškus savikainų naujinimų apibrėžimas ir sekimas atskirose įkainojimo versijose, neįtakojant originalios įkainojimo versijos. Dviejų versijų principas gali būti naudojamas identifikuoti kelis papildančiuosius naujinimus, kur kiekvienas papildantysis naujinimas turi atskirą įkainojimo versiją, susidedančią iš papildančiosios savikainos įrašų. **Pavyzdys** Šis pavyzdys rodo, kaip galima naudoti vienos ir dviejų versijų būdus standartiniam savikainos naujinimui, pavyzdžiui, savikainos naujinimui gamybinėje aplinkoje. Pavyzdžiui, atnaujinimai, atspindintys naujus elementus arba klaidų pataisymus. Tarkime, kad vienos versijos įkainojimas apima standartinę savikainą einamiesiems metams. Šios versijos identifikatorius yra 2016-STD. Versija 2016-STD apima esamas aktyvias visų elementų savikainas. Be to, ją sudaro visų su paskirstymu susijusių savikainų kategorijos ir pridėtinių išlaidų skaičiavimo formulės kurios yra žinomos 2016 m. pradžioje. 2016-STD yra pradinė savikainos nustatymo versija.
-   **Savikainos duomenų naujinimo vienos versijos būdas** − Vienos versijos būdas reiškia, kad originalioje įkainojimo versijoje 2016-STD bus visi savikainos įrašai. Savikainos atnaujinimai yra įrašyti 2016-STD ir nustatyti „Laukiama“ būsenai. Laukiamą savikainą galima rankiniu būdu įvesti naujoms įsigytoms prekėms arba apskaičiuoti gatavam gaminiui, siekiant atspindėti pataisymus. Kai naudojamas vienos versijos būdas, KS skaičiavimams nereikia atsarginio duomenų šaltinio, nes visi aktyvūs kaštai yra įtraukti į savikainos nustatymo versiją. Aktyvavus laukiančiąsias savikainas, originali įkainojimo versija 2016-STD dar kartą įtrauks visas esamas aktyvias savikainas.
-   **Savikainos duomenų naujinimo dviejų versijų būdas** − dviejų versijų būdui reikia papildomų sąnaudų versijos kurioje yra tik sąnaudų atnaujinimai. Šios versijos identifikatorius yra 2016-STD-CHANGES. Sąnaudų atnaujinimai fiksuojami 2016-STD-CHANGES ir nustatomi „Laukiama“ būsenai. Naudojant dviejų versijų būdą, pagamintų gaminių KS laukiančių sąnaudų skaičiavimams reikia atsarginio duomenų šaltinio. Taip yra todėl, papildoma savikainos nustatymo versija 2016-STD-CHANGES turi tik savikainos duomenų poaibį. Atsarginis skaičiavimas gali būti išreikštas kaip aktyvi savikaina ar kaip įkainojimo versija 2016-STD, nes abi jos nustato savikainos duomenų šaltinį, kurio 2016-STD-CHANGES nėra. Laukiančioms išlaidoms tapus aktyvioms, įkainojimo versijoje 2016-STD-KEITIMAI bus dabartinės aktyvios išlaidos, atspindinčios naujinimus, o pradinė įkainojimo versija 2016-STD bus nepakeista. Kai naudojamas dviejų versijų būdas, reikėtų nustatyti pradinės įkainojimo versijos blokavimo strategijas, kad nebūtų naujinama. Identišką blokavimo politiką reikia nustatyti papildomai savikainos nustatymo versijai, išskyrus nurodytą nuo-datos ir pasirinktinį blokavimo politikos naudojimą, kad būtų galima atlikti atnaujinimus. Nurodyta pradžios data turi būti atnaujinta kiekvienam pakeitimų paketui, kad atspindėtų suplanuotą aktyvinimo datą.

Šiame pavyzdyje naudojama viena papildoma įkainojimo versija naujinimų valdymui 2016 m. Gali būti naudojama daugiau nei viena papildoma įkainojimo versija, pavyzdžiui, atskira versija kiekvienam naujinimo paketui. Kai naudojamas daugiau nei vienas papildomas sąnaudų skaičiavimas, atsarginius duomenis reikia išreikšti kaip aktyvią savikainą, nes aktyvi savikaina paskirstoma kelioms savikainos versijoms.






