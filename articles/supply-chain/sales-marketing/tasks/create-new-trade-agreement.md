---
title: Kurti naują prekybos sutartį
description: Ši procedūra nurodo, kaip sukurti prekybos sutartį, kurioje registruojate naują produkto pardavimo kainą, dėl kurios sutarėte su konkrečiu klientu.
author: omulvad
manager: AnnBe
ms.date: 11/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e132cd20437b7929e81fcaa123d70bb57fb320c8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "323507"
---
# <a name="create-a-new-trade-agreement"></a>Kurti naują prekybos sutartį

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip sukurti prekybos sutartį, kurioje registruojate naują produkto pardavimo kainą, dėl kurios sutarėte su konkrečiu klientu. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Jei naudojate savo duomenis, prieš pradėdami šį vadovą turite įsitikinti, kad egzistuoja prekybos sutarčių žurnalo pavadinimas, kai numatytasis ryšys nustatytas kaip „Kaina (pardavimai)“.


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Kurti ir registruoti naują prekybos sutarčių žurnalą
1. Eikite į Pardavimas ir rinkodara > Kainos ir nuolaidos > Prekybos sutarčių žurnalai.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. Sąraše spustelėkite saitą pasirinktoje eilutėje.
6. Spustelėkite Eilutės.
7. Lauke „Sąskaitos kodas“ pasirinkite „Lentelė“.
    * Šiame pavyzdyje atnaujinate kainą konkrečiam klientui – tai reiškia, kad turite pasirinkti „Lentelė“. Jei norėtumėte atnaujinti produkto kainų sąrašą, reikėtų rinktis „Visi“, kad naujoji kaina galiotų visiems klientams. Jei norėtumėte diferencijuoti kainą skirtingiems klientų segmentams, tada reikėtų rinktis „Grupė“. Norėdami pasirinkti „Grupė“, turite nustatyti klientų kainų grupes.  
8. Lauke „Sąskaitos pasirinkimas“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
9. Sąraše raskite ir pasirinkite norimą įrašą.
10. Lauke „Prekės kodas“ pasirinkite „Lenetelė“.
    * Kai įvedate „Kaina (pardavimai)“ tipo prekybos sutartį, turite pasirinkti tik „Lentelė“ lauke „Prekės kodas“. Taip yra todėl, kad kaina yra absoliučioji reikšmė ir negali būti tokia pati visiems produktams ar produktų grupėms.  
11. Lauke „Prekės ryšys“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
12. Sąraše pasirinkite produktą, kurį norite įtraukti į sutartį.
    * Užsirašykite, kokį produktą pasirinkote.  
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
14. Lauke „Nuo“ įveskite mažiausią kiekį.
    * Jei klientas turi užsakyti minimalų kiekį, kad jam būtų pasiūlyta nauja kaina, šį kiekį turite nurodyti čia.  
    * Įveskite reikšmę lauke „Iki“, kad nurodytumėte didžiausią kiekį, kurį viršijus sutarties kaina negalios. Jei siūlote kainas ir nuolaidas skirtingoms kiekių riboms, kiekvieną kiekio grupę nurodykite kaip mažiausią ir didžiausią kiekį laukuose „Nuo“ ir „Iki“.  
15. Lauke „Suma valiuta“ įveskite kainą.
16. Lauke „Pradžios data“ įveskite datą, nuo kurios pradės galioti ši sutartis.
17. Spustelėkite Įrašyti.
18. Spustelėkite Tikrinti.
19. Spustelėkite „Tikrinti pasirinktas eilutes“.
20. Spustelėkite GERAI.
21. Spustelėkite Registruoti.
22. Spustelėkite GERAI.

## <a name="view-trade-agreements-for-a-product"></a>Peržiūrėti produkto prekybos sutartis
1. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
2. Sąraše raskite ir pasirinkite produktą, kurio kainą ką tik atnaujinote.
3. Veiksmų srityje spustelėkite Parduoti.
4. Spustelėkite „Peržiūrėti prekybos sutartis“.
    * Peržiūrėkite kainos prekybos sutarties informaciją, kurią ką tik sukūrėte.    
5. Uždarykite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai
### <a name="community-blogs"></a>Bendruomenės tinklaraščiai
- [Pardavimo kainos „Dynamics 365 for Finance and Operations“](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)
