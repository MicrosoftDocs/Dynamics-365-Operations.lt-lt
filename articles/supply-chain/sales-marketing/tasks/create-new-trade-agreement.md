---
title: Kurti naują prekybos sutartį
description: Ši procedūra nurodo, kaip sukurti prekybos sutartį, kurioje registruojate naują produkto pardavimo kainą, dėl kurios sutarėte su konkrečiu klientu.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24290ec873da9e871c001bcdc97e14dcad0e3d1e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111114"
---
# <a name="create-a-new-trade-agreement"></a>Kurti naują prekybos sutartį

[!include [banner](../../includes/banner.md)]

Ši procedūra nurodo, kaip sukurti prekybos sutartį, kurioje registruojate naują produkto pardavimo kainą, dėl kurios sutarėte su konkrečiu klientu. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis. Jei naudojate savo duomenis, prieš pradėdami šį vadovą turite įsitikinti, kad egzistuoja prekybos sutarčių žurnalo pavadinimas, kai numatytasis ryšys nustatytas kaip „Kaina (pardavimai)“.

## <a name="create-and-post-a-new-trade-agreement-journal"></a>Kurti ir registruoti naują prekybos sutarčių žurnalą

1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Kainos ir nuolaidos > Prekybos sutarčių žurnalai**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše raskite ir pasirinkite norimą įrašą.
5. **Veiksmų srityje** spustelėkite **Eilutės**.
6. Lauke **Sąskaitos kodas** pasirinkite Lentelė.
    
    Šiame pavyzdyje atnaujinate kainą konkrečiam klientui – tai reiškia, kad turite pasirinkti „Lentelė“. Jei norėtumėte atnaujinti produkto kainų sąrašą, reikėtų rinktis Visi, kad naujoji kaina galiotų visiems klientams. Jei norėtumėte diferencijuoti kainą skirtingiems klientų segmentams, tada reikėtų rinktis „Grupė“. Norėdami pasirinkti „Grupė“, turite nustatyti klientų kainų grupes.  

7. Lauke **Sąskaitos pasirinkimas** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
8. Sąraše raskite ir pasirinkite norimą įrašą.
9. Lauke **Prekės kodas** pasirinkite Lentelė.
    
    Kai įvedate Kaina (pardavimai) tipo prekybos sutartį, lauke **Prekės kodas** turite pasirinkti tik Lentelė. Taip yra todėl, kad kaina yra absoliučioji reikšmė ir negali būti tokia pati visiems produktams ar produktų grupėms.
    
10. Lauke **Prekės ryšys** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
11. Sąraše pasirinkite produktą, kurį norite įtraukti į sutartį. Užsirašykite, kokį produktą pasirinkote.  
12. Lauke **Nuo** įveskite mažiausią kiekį.
    - Jei klientas turi užsakyti minimalų kiekį, kad jam būtų pasiūlyta nauja kaina, šį kiekį turite nurodyti čia.  
    - Įveskite reikšmę lauke **Iki**, kad nurodytumėte didžiausią kiekį, kurį viršijus sutarties kaina negalios. Jei siūlote kainas ir nuolaidas skirtingoms kiekių riboms, kiekvieną kiekio grupę nurodykite kaip mažiausią ir didžiausią kiekį laukuose **Nuo** ir **Iki**.
13. Lauke **Suma valiuta** įveskite kainą.
14. Skyriaus **Išsamiai** lauke **Pradžios data** įveskite datą, nuo kurios pradės galioti ši sutartis.
15. Spustelėkite **Įrašyti**.
16. Spustelėkite **Tikrinti**.
17. Spustelėkite **Tikrinti pasirinktas eilutes**.
18. Spustelėkite **Gerai**.
19. Spustelėkite **Registruoti**.
20. Spustelėkite **Gerai**.

## <a name="view-trade-agreements-for-a-product"></a>Peržiūrėti produkto prekybos sutartis

1. Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.
2. Sąraše raskite ir pasirinkite produktą, kurio kainą ką tik atnaujinote.
3. **Veiksmų srityje** spustelėkite **Pardavimas**.
4. Spustelėkite **Peržiūrėti prekybos sutartis**.
    
    Peržiūrėkite kainos prekybos sutarties informaciją, kurią ką tik sukūrėte.

5. Uždarykite puslapį.

## <a name="additional-resources"></a>Papildomi ištekliai

### <a name="whitepaper"></a>Techninė Dokumentacija

Norėdami gauti daugiau informacijos, atsisiųskite šią techninę dokumentaciją (sukurtą AX2012 palaikymui, tačiau vis dar taikoma „Dynamics 365 Supply Chain Management”)

- [Prekybos sutartys](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a>Bendruomenės tinklaraščiai

- [Pardavimo kainos finansuose ir operacijose](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
