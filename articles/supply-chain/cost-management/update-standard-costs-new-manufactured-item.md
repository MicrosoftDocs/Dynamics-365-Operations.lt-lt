---
title: Naujos pagamintos prekės standartinių savikainų atnaujinimas
description: Šiame straipsnyje patariama, kaip atnaujinti naujos pagamintos prekės standartines išlaidas.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79693
ms.assetid: ba64b70f-3f4c-4373-9a7d-8fd07c45a8cf
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc8725bcab61fa20a4c35a83473b00e54cf0bf28
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "325508"
---
# <a name="update-standard-costs-for-a-new-manufactured-item"></a>Naujos pagamintos prekės standartinių savikainų atnaujinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje patariama, kaip atnaujinti naujos pagamintos prekės standartines išlaidas. 

Šiose rekomendacijose taikomas dviejų versijų būdas į standartinius išlaidų naujinimus. Naudojant šį būdą, viena įkainojimo versija turi iš pradžių nustatytas standartines įšaldyto laikotarpio išlaidas, o antra įkainojimo versija turi papildančiuosius naujinimus, susijusius su naujai pagamintomis prekėmis. Papildantieji naujinimai įvedami kaip išlaidų įrašai antroje įkainojimo versijoje ir galiausiai jie suaktyvinami. Dviejų versijų būdui reikalingas antros įkainojimo versijos apibrėžimas. Toliau pateikti patarimai, kaip apibrėžti šią įkainojimo versiją.

-   Priskirkite įkainojimo tipą **Standartinės išlaidos**.
-   Priskirkite reikšminį identifikatorių, kuris nurodo įkainojimo versijos turinį, pvz., **2016-NAUJINIMAI**.
-   Įsitikinkite, kad laukų grupėje **Leisti kainų tipus** **Savikaina** nustatyta į **Taip**.
-   Leiskite įvesti visų vietų išlaidų įrašus (t. y., lauką **Vieta** palikite tuščią). Jei įvedate vietą, galima įvesti tik tos vietos išlaidų įrašus.
-   Naudokite atsarginį principą **Aktyvus**.

Norėdami pagamintas prekes įtraukti įšaldyto laikotarpio metu, atlikite tolesnius veiksmus.

1.  Naudodami puslapį **Įkainojimo versijos nustatymas**, galite išlaidų įrašus leisti įvesti į antrą įkainojimo versiją, kurioje yra papildančiųjų naujinimų. Neleiskite suaktyvinti laukiančių išlaidų, kai suaktyvinti leidžiama tik išsamiai ir tiksliai apibrėžus laukiančias išlaidas. Kaip įkainojimo versijos strategiją palikite tušią pradžios datos langelį, pradžios datą įveskite, kai įvesite kiekvieną išlaidų įrašą. Pradžios data turėtų rodyti datą prieš naujų prekių pirkimą arba gamybą.
2.  Norėdami įvesti naujų nupirktų prekių išlaidų įrašus, naudokite puslapį **Prekės kaina**. Kiekvienam išlaidų įrašui įveskite įkainojimo versiją, kurioje yra papildančiųjų naujinimų, ir naudokite pradžios datą, kurį yra ankstesnė nei numatoma naujai pagamintų prekių gamybos data.
3.  Naujų pagamintų prekių išlaidas apskaičiuokite naudodami puslapį **Skaičiavimas**. Iš puslapio **Įkainojimo versijos tvarkymas** atidarykite puslapį **Skaičiavimas** ir pasirinkite įkainojimo versiją, kurioje yra papildančiųjų naujinimų. Naudokite atrankos kriterijus, norėdami nurodyti naujai pagamintą prekę ir bet kokį jos pagamintą komponentą. Keleto lygių produkto struktūroje taip pat gali reikėti nurodyti bet kurią pirminę prekę, kurioje kaip komponentų yra naujai pagamintų prekių. Įveskite komplektavimo specifikacijos (KS) skaičiavimo pradžios datą, atitinkančią naujai pagamintų prekių gamybos pradžią. Pradžios data turėtų patekti į prekės KS versijos ir maršruto versijos galiojimo datas. **Pastaba.** Trūkstamas išlaidų įrašas gali rodyti naujai pagamintą prekę. KS skaičiavimai gali būti apriboti prekėmis su trūkstamomis išlaidomis.
4.  Patikrinkite naujai pagamintų prekių apskaičiuotų išlaidų išsamumą ir tikslumą. Nauodami puslapį **Baigta**, galite peržiūrėti kiekvienos prekės išlaidų įrašo apskaičiuotas išlaidas ir sistemos pranešimo perspėjimo pranešimus. Taip pat galite naudoti puslapį **Skaičiavimas**, kad peržiūrėtumėte apskaičiuotų išlaidų sąrašą.
5.  Naudodami puslapį **Įkainojimo versijos nustatymas**, galite pakeisti blokavimo vėliavėlę, kad leistumėte antrojoje įkainojimo versijoje aktyvinti laukiančius išlaidų įrašus.
6.  Naudodami puslapį **Aktyvinti kainas** (kurį galite atidaryti iš puslapio **Įkainojimo versijos tvarkymas**), galite leisti antrojoje įkainojimo versijoje aktyvinti laukiančius išlaidų įrašus. Aktyvinti atskirų prekių laukiančių išlaidų įrašus taip pat galite puslapyje **Prekės kaina** spustelėdami mygtuką **Aktyvinti**.
7.  Naudokite puslapį **Įkainojimo versijos nustatymas**, kad pakeistumėte blokavimo vėliavėles antrojoje įkainojimo versijoje, kad uždraustumėte papildomą duomenų naudojimą. Blokavimo strategija apsaugo nuo naujų laukiančių išlaidų įvedimo ir laukiančių išlaidų aktyvinimo.




