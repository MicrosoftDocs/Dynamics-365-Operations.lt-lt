---
title: Žemėlapio modulis
description: Šis skyrius aprašo žemėlapio modulius ir tai, kaip konfigūruoti juos į „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/31/2020
ms.locfileid: "3647000"
---
# <a name="map-module"></a>Žemėlapio modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šis skyrius aprašo žemėlapio modulius ir tai, kaip konfigūruoti juos į „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Žemėlapio modulis rodo parduotuvių vietas interaktyviame žemėlapyje, kuris yra sukurtas naudojant [„Bing Maps V8 Web Control“](https://docs.microsoft.com/bingmaps/v8-web-control/). „Bing Maps“ API raktas yra reikalaujamas ir turi būti įtrauktas į bendrinamus parametrus komercijos štabo puslapyje Žemėlapio moduliai suteikia įvairias peržiūras, tokias kaip kelio, oro, kelkraščio, kurias naudotojai gali pasirinkti tam, kad peržiūrėtų žemėlapio vietas. Jie taip pat leidžia sąvaiką tokią kaip priartinimas ir naudotojo vietos naudojimas.

Žemėlapio modulis dirba kartu su parduotuvės sleketoriaus moduliu tam, kad nustatytų geografines parduotuvių vietas, kurios turi būti pažymėtos žemėlapyje. Parduotuvės selektorius ir žemėlapio modeliai sąveikauja, kai naudotojas pasirenka parduotuvę viename iš šių modulių svetainės puslapyje. Žemėlapio moduliai gali būti išplėsti kitiems scenarijams, už sąveikos tarp parduotuvės selektoriaus modulių. Nepaisant to, modulio tinkinimas yra būtinas.

Žemėlapio modulis buvo pristatytas prekybos versijoje 10.0.13.

Toliau pateiktas paveikslėlis rodo parduotuvės žemėlapio modulio pavyzdį, kuris yra naudojamas parduotuvės vietų puslapyje.

![Parduotuvės parinkiklio modulio pavyzdys](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Modulio ypatybės

| Ypatybės pavadinimas             | Vertė                 | aprašymas |
|---------------------------|-----------------------|-------------|
| Antraštė | Tekstas | Modulio antraštė. |
| Stūmoklio parinktys: nustatytoji piktograma | Nuotrauka | Stūmoklio simbolio paveikslėlis naudojamas parduotuvėms rodomoms žemėlapyje. |
| Stūmoklio parinktys: aktyvi piktograma | Nuotrauka | Stūmoklio simbolio paveikslėlis naudojamas parduotuvei pasirinktai žemėlapyje. |
| Stūmoklio parinktys: nustatytosios piktogramos spalva | Maskavimo pynė | Tekstas ir šešioliktainės vertės stūmoklio simbolio spalvai žemėlapyje. |
| Stūmoklio parinktys: aktyvi piktogramos spalva | Maskavimo pynė | Tekstas ir šešioliktainės vertės pasirinkto stūmoklio simbolio spalvai žemėlapyje. |
| Rodyti rodyklę | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatytą į **Teisingą**, visi stūmoklio simboliai rodantys parduotuvę bus rodomi turinyje. Šis turinys atitiks turinį sąrašo peržiūroje, kurioje parduotuvės selektoriaus modulis yra rodomas. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Įtraukti leidžiamą žemėlapio kūrimo URL į sveitainės turinio apsaugos politikos gaires

Žemėlapių moduliui sąveikauti su „Bing Maps“, privalote užtikrinti, kad tolesni žemėlapių kūrimo URL yra leidžiami (žinomi taip pat kaip „whitelisted“) jūsų svetainės turinio saugumo politikoje (CSP). Šis nustatymas yra atliekamas komercijos svetainės kūrimo įrankyje įtraukiant leidžiamus URL į skirtingas svateinės CSP gaires svetainei (pavyzdžiui, **img-src**). Dėl platesnės informacijos, žr. [Turinio saugos politika](manage-csp.md). 

- Į**connect-src** direktyvą, įtraukite **&#42;.bing.com**.
- Į**img-src** direktyvą, įtraukite **&#42;.virtualearth.net**.
- Į **script-src**direktyvą, įtraukite **&#42;.bing.com, &#42;.virtualearth.net**.
- Į **script style-src** direktyvą, įtraukite **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Įtraukti žemėlapio modulį į puslapį

Dėl išsamesnės informacijos apie tai, kaip konfigūruoti žemėlapio modulį puslapyje, žr. [Parduotuvės pasirinkimo modulis](store-selector.md). 
 
## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Parduotuvės išrinkiklio modulis](store-selector.md)

[„Bing“ žemėlapių valdymas jūsų organizacijoje](./dev-itpro/manage-bing-maps.md)

[„Bing Maps V8 Web Control“](https://docs.microsoft.com/bingmaps/v8-web-control/)
