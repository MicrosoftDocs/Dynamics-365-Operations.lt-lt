---
title: Svetainės išrinkiklio modulis
description: Šioje temoje aprašomas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti ją prie svetainės puslapių, kurie yra dalyje Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/06/2022
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
ms.openlocfilehash: ad4d4d5f950d0631059d8f509e9e808a9106eb98
ms.sourcegitcommit: 4861ec2d3ae24cc9dd4ad3ac748fd05be3d80c70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2022
ms.locfileid: "8551699"
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

Svetainės išrinkiklio modulį galima pridėti prie antraštės **modulio svetainės išrinkiklio**[atminties](author-header-module.md). Įdę svetainės išrinkiklio modulį galite apibrėžti modulio antraštę ir svetainės pasirinktis. Paprastai antraštės modulis yra antraštės fragmente, kurį galima bendrai naudoti svetainės el. komercijos puslapiuose. Pateiktame pavyzdyje svetainės išrinkiklio modulis buvo pridėtas prie antraštės modulio, kuris yra antraštės fragmente **,** **pavadintame HeaderContainer, svetainės išrinkiklio atrinkiklio**.

![Svetainės išrinkiklio modulio pavyzdys antraštės fragmente.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Antraštės modulis](author-header-module.md)

[Naršymo kelio modulis](add-breadcrumb.md)

[Naršymo meniu modulis](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
