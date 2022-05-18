---
title: Svetainės išrinkiklio modulis
description: Šioje temoje aprašomas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti ją prie svetainės puslapių, kurie yra dalyje Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a1954f6b2fea35d5138218e6a2a23ab1fd04c8fc
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710308"
---
# <a name="site-picker-module"></a>Svetainės išrinkiklio modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti ją prie svetainės puslapių, kurie yra dalyje Microsoft Dynamics 365 Commerce.

Kai įmonė turi įvairių svetainių rinkose, regionuose ir vietovėse, svetainės vartotojams reikia paprasto būdo perjungti svetaines ir pasirinkti pageidaujamą prekybos svetainę. Norint talpinti šį scenarijų, svetainės išrinkiklio modulis leidžia vartotojams naršyti keliose svetainėse. Svetainės išrinkiklis [taip](geo-detection-redirection.md) pat rekomenduojamas, kai jūsų el. komercijos svetainei yra įdiegtas geografinis aptikimas ir nukreipimas, kad klientai galėtų nepaisyti svetainės nuostatų, [kurias jie nurodo naudodami šalies / regiono išrinkiklio modulį](country-region-picker-module.md). 

Teritorijos išrinkiklio modulis turi būti sukonfigūruotas su teritorijų (rinkų, regionų ar vietų), kurias gali naršyti teritorijos vartotojai, sąrašu. Šioje iliustracijoje pateikiamas svetainės išrinkiklio modulio, kuris pavaizduotas svetainės puslapio antraštėje, pavyzdys.

![Svetainės išrinkiklio modulio pavyzdys svetainės puslapio antraštėje.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Svetainės išrinkiklio modulio ypatybės

| Ypatybės pavadinimas | Reikšmė                 | Aprašymas |
|---------------|-----------------------|-------------|
| Antraštė       | Tekstas                  | Modulio antraštė. |
| Svetainės parinktys  | Pavadinimas, vaizdas, URL      | Ši ypatybė nurodo pavadinimą, saitą su pagrindiniu svetainės puslapiu ir pasirinktinį kiekvienos į modulį įtrauktos svetainės vaizdą. Šis vaizdas gali būti vėliavėlė arba tam tikras rinkos, regiono ar vietovės atvaizdavimas. |

## <a name="add-a-site-picker-module-to-a-page"></a>Svetainės išrinkiklio modulio įtraukimas į puslapį

Svetainės išrinkiklio modulį galima pridėti prie antraštės **modulio svetainės išrinkiklio**[atminties](author-header-module.md). Įdę svetainės išrinkiklio modulį galite apibrėžti modulio antraštę ir svetainės pasirinktis. Paprastai antraštės modulis yra antraštės fragmente, kurį galima bendrai naudoti svetainės el. komercijos puslapiuose. 

Norėdami įtraukti svetainės išrinkiklio modulį į antraštės modulį, atlikite šiuos veiksmus.

1. **Antraštės fragmento antraštės** modulio svetainės išrinkiklio atrinkiklio atrinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** įtraukite svetainės **išrinkiklio modulį**, tada pasirinkite **Gerai**.
1. Svetainės išrinkiklio **ypatybės** srityje pasirinkite Įtraukti svetainės **pasirinkčių sąrašą**. Atsiranda redaguojama **vietos pasirinkčių** sąrašo pasirinktis.
1. Pasirinkite **svetainės pasirinkčių sąrašą**. Atsiranda **vietos pasirinkčių** sąrašo dialogo langas.
1. Įveskite **svetainės** pavadinimo tekstą, kuris bus rodomas svetainės išrinkiklio išplečiamajame sąraše.
1. Prie **svetainės nukreipimo URL** pasirinkite **Įtraukti saitą**. Atsiranda **sritis Įtraukti saitą**.
1. Srityje Įtraukti **saito iškvėpimas** pasirinkite Pasirinktinį **puslapį**, tada pasirinkite **Pirmyn**.
1. Iš svetainės URL sąrašo pasirinkite URL su maršrutu, kurį sukūrėte į svetainę įtraukdami kanalą (pvz., `www.adventure-works.com/fr-ca`), tada pasirinkite **Taikyti**.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Pasirinkite **Publikuoti** ir publikuokite puslapį.

Pateiktame pavyzdyje svetainės išrinkiklio modulis buvo pridėtas prie antraštės modulio, kuris yra antraštės fragmente **,** **pavadintame HeaderContainer, svetainės išrinkiklio atrinkiklio**.

![Svetainės išrinkiklio modulio pavyzdys antraštės fragmente.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Antraštės modulis](author-header-module.md)

[Naršymo kelio modulis](add-breadcrumb.md)

[Naršymo meniu modulis](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
