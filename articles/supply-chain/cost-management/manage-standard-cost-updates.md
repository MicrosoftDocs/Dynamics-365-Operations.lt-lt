---
title: Standartinių savikainos atnaujinimų valdymas
description: 'Standartinių savikainos atnaujinimų duomenis galima valdyti dviem būdais: vienos versijos būdu arba dviejų versijų būdu.'
author: JennySong-SH
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a6d693b58e7fbbd8e082d68d124eae52fb840b02
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674539"
---
# <a name="manage-standard-cost-updates"></a>Standartinių savikainos atnaujinimų valdymas

[!include [banner](../includes/banner.md)]

Standartinių savikainos atnaujinimų duomenis galima valdyti dviem būdais: vienos versijos būdu arba dviejų versijų būdu.

Vienos versijos būdui naudojama viena savikainos nustatymo versija, kurioje įtraukiama visų išlaidų apskaita. Šie įrašai apima pradinę savikainą ir visus savikainos atnaujinimus.

Dviejų versijų būdui naudojama viena versija, kurioje yra pradinės savikainos įrašai, ir antroji versija, kurioje yra visų savikainos atnaujinimų įrašai. Svarbiausias dviejų versijų būdo pranašumas yra aiškus savikainų naujinimų apibrėžimas ir sekimas atskirose įkainojimo versijose, neįtakojant originalios įkainojimo versijos. Dviejų versijų principas gali būti naudojamas identifikuoti kelis papildančiuosius naujinimus, kur kiekvienas papildantysis naujinimas turi atskirą įkainojimo versiją, susidedančią iš papildančiosios savikainos įrašų.

## <a name="example"></a>Pavyzdys

Šiame pavyzdyje parodyta, kaip galima naudoti vienos ir dviejų versijų būdus standartinėms savikainoms gamybinėje aplinkoje naujinti. Pavyzdžiui, atnaujinimai, atspindintys naujus elementus arba klaidų pataisymus. Tarkime, kad vienos versijos įkainojimas apima standartinę savikainą einamiesiems metams. Šios versijos identifikatorius yra 2020-STD. Versija 2020-STD apima esamas aktyvias visų elementų savikainas. Be to, ją sudaro visų su paskirstymu susijusių savikainų kategorijos ir pridėtinių išlaidų skaičiavimo formulės kurios yra žinomos 2020 m. pradžioje. 2020-STD yra pradinė savikainos nustatymo versija.

- **Savikainos duomenų naujinimo vienos versijos būdas** − Vienos versijos būdas reiškia, kad originalioje įkainojimo versijoje 2020-STD bus visi savikainos įrašai. Savikainos atnaujinimai yra įrašyti „2020-STD” ir nustatyti būsenai Laukiama. Naujai įsigytų prekių laukiamą savikainą galima įvesti neautomatiškai arba apskaičiuoti pagamintos prekės savikainą, siekiant atspindėti pataisymus. Naudojant vienos versijos būdą, KS skaičiavimams atlikti nereikalingas atsarginis duomenų šaltinis, nes visos aktyvios savikainos yra įkainojimo versijoje. Aktyvavus laukiančiąsias savikainas, originali įkainojimo versija 2020-STD dar kartą įtrauks visas esamas aktyvias savikainas.
- **Savikainos duomenų naujinimo dviejų versijų būdas** − dviejų versijų būdui reikia papildomų sąnaudų versijos kurioje yra tik sąnaudų atnaujinimai. Šios versijos identifikatorius yra 2020-STD-CHANGES. Savikainos atnaujinimai yra įrašyti „2020-STD-CHANGES” ir jiems nustatyta būsena Laukiama. Naudojant dviejų versijų būdą, pagamintų prekių KS laukiančių sąnaudų skaičiavimams atlikti reikalingas atsarginis duomenų šaltinis. Taip yra todėl, papildoma savikainos nustatymo versija 2020-STD-CHANGES turi tik savikainos duomenų poaibį. Atsarginis skaičiavimas gali būti išreikštas kaip aktyvi savikaina ar kaip įkainojimo versija 2020-STD, nes abi jos nustato savikainos duomenų šaltinį, kurio 2020-STD-CHANGES nėra. Aktyvavus laukiančiąsias savikainas, įkainojimo versijoje „2020-STD-CHANGES” bus esančios aktyvios savikainos, kuriose atsižvelgta į naujinimus, o originali įkainojimo versija „2020-STD” nebus paveikta. Kai naudojamas dviejų versijų būdas, originalios įkainojimo versijos blokuojančiosios strategijos nustatomos taip, kad uždraustų naujinimus. Identišką blokavimo politiką reikia nustatyti papildomai savikainos nustatymo versijai, išskyrus nurodytą nuo-datos ir pasirinktinį blokavimo politikos naudojimą, kad būtų galima atlikti atnaujinimus. Nurodyta pradžios data turi būti atnaujinta kiekvienam pakeitimų paketui, kad atspindėtų suplanuotą aktyvinimo datą.

Šiame pavyzdyje naudojama viena papildoma įkainojimo versija naujinimų valdymui 2020 m. Gali būti naudojama daugiau nei viena papildoma įkainojimo versija, pavyzdžiui, atskira versija kiekvienam naujinimo paketui. Kai naudojamas daugiau nei vienas papildomas sąnaudų skaičiavimas, atsarginius duomenis reikia išreikšti kaip aktyvią savikainą, nes aktyvi savikaina paskirstoma kelioms savikainos versijoms.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Standartinio savikainos perkainojimo finansinės dimensijos

Naujos standartinės kainos aktyvinimas paprastai perkainos turimų atsargų vertę naudojant standartines savikainos perkainojimo operacijas. Paprastai tada prekės finansinės dimensijos yra užregistruojamos operacijose. Tačiau, jei norite kontroliuoti, ar ir kaip finansinės dimensijos yra registruojamos, naudokite [funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tam, kad įjungtumėte funkciją *Numatytųjų finansinių dimensijų atsargų standartiniam savikainos perkainojimui parinktys*. Įgalinę šią funkciją eikite į **Išlaidų valdymas > Atsargų apskaitos strategijų nustatymas > Parametrai** ir nustatykite naują išplečiamąjį sąrašą **Finansinės dimensijos kilmė** į vien iš šių reikšmių:

- **Nėra** – Jokios finansinės dimensijos nėra užregistruotos perkainojimo operacijose. Jeigu jūsų sąskaitos struktūroje yra reikiama finansinė dimensija, perkainojimo procesas vis dar vykdomas, bet bus sukuriami apskaitos įrašai, neturintys finansinių dimensijų. Šiuo atveju vartotojai pirmiausia gaus įspėjimo pranešimą, taigi, jie galės atšaukti perkainojimą, jei reikalinga.
- **Lentelė** – Prekės finansinės dimensijos yra užregistruojamos perkainojimo operacijose. Tai yra numatytasis parametras ir jis atitinka pradinę sistemos elgseną, neįjungus funkcijos *Numatytųjų finansinių dimensijų atsargų standartiniam savikainos perkainojimui parinktys*.
- **Registravimas** – Perkainojamos operacijos finansinės dimensijos yra registruojamos perkainojimo operacijose. Pagal numatytuosius nustatymus, finansinės dimensijos iš pradinės operacijos atsargų paskyros bus naudojamos tiek atsargų sąskaitai, tiek perkainojimo sąskaitai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]