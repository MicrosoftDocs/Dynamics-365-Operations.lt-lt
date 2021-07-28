---
title: Rodymo parametrų taikymas produktų dimensijoms
description: Šioje temoje apžvelgiami produkto dimensijų rodymo parametrai ir aprašoma, kaip juos taikyti „Microsoft Dynamics 365 Commerce” platformoje.
author: anupamar-ms
ms.date: 05/28/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d6854c11822e07ff06426b7a35eac86cdc0e9b06
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356907"
---
# <a name="apply-display-settings-for-product-dimensions"></a>Rodymo parametrų taikymas produktų dimensijoms

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje apžvelgiami produkto dimensijų rodymo parametrai ir aprašoma, kaip juos taikyti „Microsoft Dynamics 365 Commerce” platformoje.

„Dynamics 365 Commerce” palaiko dydžio, stiliaus ir spalvos dimensijas, kad būtų galima atskirti produkto variantus. Dimensijos įprastai rodomos kaip tekstinės reikšmės, pavyzdžiui, „Maža”, „Vidutinė” ir „Didelė” – dydžiams, o spalvoms – „Juoda” ir „Ruda”. Tačiau, jei produktas palaiko daug variantų, gali būti sunku naršyti produkto variantus, nes reikia kelių pasirinkimų kiekvieno varianto vaizdui peržiūrėti. Kad būtų lengviau naršyti produkto variantus, „Commerce” leidimo 10.0.20 versijoje galima naudoti vaizdus ir šešioliktainius („hex”) kodus, kad dimensijos būtų rodomos kaip pavyzdžiai.

„Commerce“ svetainės kūrimo priemonėje dimensijų parametrai yra apibrėžiami **Svetainės parametrai \> Plėtiniai \> Dimensijų parametrai**. Šioje iliustracijoje pateikiamas dimensijos nustatymų pavyzdys svetainės kūrimo priemonėje.

![Svetainės parametrų pavyzdys „Commerce“ svetainės kūrimo priemonėje.](./dev-itpro/media/swatch_site_settings.PNG)

Galimi du dimensijų parametrai:

- **Dimensijos, rodytinos kaip vaizdas** – Nurodykite, kurios dimensijos turėtų būti rodomos kaip pavyzdžiai el. prekybos svetainės puslapiuose, pavyzdžiui, produkto informacijos puslapiuose (PDP) ir ieškos rezultatų sąrašo puslapiuose. Bet koks spalvos, dydžio ir stiliaus dimensijų derinys gali būti rodomas kaip pavyzdys. Jei dimensija pasirinkta rodymui kaip pavyzdys, „Commerce” modulio generavimas ieškos galimos šešioliktainio kodo pavyzdžio konfigūracijos. Jei nesukonfigūruotas šešioliktainis kodas, sistemos logika ieškos vaizdo URL pavyzdžio konfigūracijos. Jei nesukonfigūruotas nei šešioliktainis kodas, nei vaizdo URL, bus rodomas tekstas.

    Šioje iliustracijoje pateikiamas pavyzdys, kuriame PDP el. komercijos svetainėje apima spalvų ir dydžių pavyzdžius. Šiame pavyzdyje šešioliktainis kodas konfigūruojamas spalvos dimensijai. Todėl pavyzdžiai rodomi kaip spalvos. Tačiau dydžio dimensijai nesukonfigūruojamas nei šešioliktainis kodas, nei vaizdo URL. Todėl rodomas tekstas.

    ![Spalvos dimensija rodoma kaip pavyzdys elektroninės prekybos išsamios produkto informacijos puslapyje.](./dev-itpro/media/swatch_pdp.png)

- **Dimensijos, rodytinos produkto kortelėje** – Nurodykite, kurios dimensijos turėtų būti rodomos produkto kortelėse, rodomose sąrašuose ir sąrašo puslapiuose. Kad dimensija galėtų būti rodoma produkto kortelėje, šis nustatymas turi būti įgalintas tai dimensijai. Parametras **Dimensijos, rodytinos kaip vaizdas** taip pat turi būti įgalintas. Pavyzdžių pasirinkimo veikimas produkto kortelėse yra optimizuotas spalvos dimensijai. Norint tinkinti kitų dimensijų pavyzdžių pasirinkimo būdą, gali būti reikalingas rodinio plėtinys.

    Šioje iliustracijoje pateikiamas pavyzdys, kuriame el. komercijos svetainės sąrašo puslapyje yra produktų kortelės, apimančios spalvų pavyzdžius.

    ![Spalvos dimensija rodoma kaip pavyzdys elektroninės prekybos sąrašo puslapyje.](./dev-itpro/media/swatch_searchresults.PNG)

Daugiau informacijos apie tai, kaip konfigūruoti produkto dimensijas, kad jos būtų rodomos kaip pavyzdžiai svetainės puslapiuose, rasite [Konfigūruoti produkto dimensijų reikšmes, kad jos būtų rodomos kaip pavyzdžiai](./dev-itpro/dimensions-swatch.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Ieškos rezultatų modulis](search-result-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Konfigūruoti produkto dimensijų reikšmes, kad jos būtų rodomos kaip pavyzdžiai](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
