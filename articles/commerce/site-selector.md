---
title: Svetainės išrinkiklio modulis
description: Šioje temoje paaiškinamas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 10/20/2020
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
ms.openlocfilehash: b69156ee79dbbe8cbb8f5eb5988a751f0488d8e5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6357743"
---
# <a name="site-selector-module"></a>Svetainės išrinkiklio modulis

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinamas svetainės išrinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.

Kai įmonė turi įvairių svetainių rinkose, regionuose ir vietovėse, svetainės vartotojams reikia paprasto būdo perjungti svetaines ir pasirinkti pageidaujamą prekybos svetainę. Kad vartotojai galėtų išpildyti šį poreikį, svetainės išrinkiklio modulis leidžia naršyti keliose svetainėse.

Svetainės išrinkiklio modulis turi būti sukonfigūruotas naudojant rinkų, regionų ar vietovių svetainių, kuriose vartotojai gali naršyti, sąrašą.

> [!NOTE]
> Svetainės išrinkiklio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.14 leidime.

Toliau pateiktoje iliustracijoje parodytas svetainės išrinkiklio modulio, kuris rodomas svetainės puslapio antraštėje, pavyzdys.

![Svetainės išrinkiklio modulio, esančio svetainės puslapio antraštėje, pavyzdys.](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Svetainės išrinkiklio modulio ypatybės

| Ypatybės pavadinimas | Reikšmė                 | Aprašas |
|---------------|-----------------------|-------------|
| Antraštė       | Tekstas                  | Modulio antraštė. |
| Svetainės parinktys  | Pavadinimas, vaizdas, URL      | Ši ypatybė nurodo pavadinimą, saitą su pagrindiniu svetainės puslapiu ir pasirinktinį kiekvienos į modulį įtrauktos svetainės vaizdą. Šis vaizdas gali būti vėliavėlė arba tam tikras rinkos, regiono ar vietovės atvaizdavimas. |

## <a name="add-a-site-selector-module-to-a-page"></a>Svetainės išrinkiklio modulio įtraukimas į puslapį

Svetainės išrinkiklio modulį galima įtraukti į [antraštės modulį](author-header-module.md), esantį svetainės išrinkiklio vietoje. Po jo įtraukimo galite nurodyti modulio antraštę ir svetainės parinktis.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Antraštės modulis](author-header-module.md)

[Naršymo kelio modulis](add-breadcrumb.md)

[Naršymo meniu modulis](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]