---
title: Žemėlapio modulis
description: Šis skyrius aprašo žemėlapio modulius ir tai, kaip konfigūruoti juos į „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 74991a2979540dab344f39976005250637fab29c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252587"
---
# <a name="map-module"></a>Žemėlapio modulis

[!include [banner](includes/banner.md)]


Šis skyrius aprašo žemėlapio modulius ir tai, kaip konfigūruoti juos į „Microsoft Dynamics 365 Commerce“.

Žemėlapio modulis rodo parduotuvių vietas interaktyviame žemėlapyje, kuris yra sukurtas naudojant [„Bing Maps V8 Web Control“](https://docs.microsoft.com/bingmaps/v8-web-control/). „Bing Maps“ API raktas yra reikalaujamas ir turi būti įtrauktas į bendrinamus parametrus komercijos štabo puslapyje Žemėlapio moduliai suteikia įvairias peržiūras, tokias kaip kelio, oro, kelkraščio, kurias naudotojai gali pasirinkti tam, kad peržiūrėtų žemėlapio vietas. Jie taip pat leidžia sąvaiką tokią kaip priartinimas ir naudotojo vietos naudojimas.

Žemėlapio modulis dirba kartu su parduotuvės sleketoriaus moduliu tam, kad nustatytų geografines parduotuvių vietas, kurios turi būti pažymėtos žemėlapyje. Parduotuvės selektorius ir žemėlapio modeliai sąveikauja, kai naudotojas pasirenka parduotuvę viename iš šių modulių svetainės puslapyje. Žemėlapio moduliai gali būti išplėsti kitiems scenarijams, už sąveikos tarp parduotuvės selektoriaus modulių. Nepaisant to, modulio tinkinimas yra būtinas.

> [!NOTE]
> Žemėlapio modulį galima naudoti „Dynamics 365 Commerce“ 10.0.13 leidime.

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

Tam, kad žemėlapių modulis sąveikatų su „Bing Maps“, turite užtikrinti, kad tolesni žemėlapio URL yra leidžiami jūsų saito turinio saugos politikoje (CSP). Šis nustatymas yra atliekamas komercijos svetainės kūrimo įrankyje įtraukiant leidžiamus URL į skirtingas svateinės CSP gaires svetainei (pavyzdžiui, **img-src**). Dėl platesnės informacijos, žr. [Turinio saugos politika](manage-csp.md). 

- Į **connect-src** direktyvą, įtraukite **&#42;.bing.com**.
- Į **img-src** direktyvą, įtraukite **&#42;.virtualearth.net**.
- Į **script-src** direktyvą, įtraukite **&#42;.bing.com, &#42;.virtualearth.net**.
- Į **script style-src** direktyvą, įtraukite **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Įtraukti žemėlapio modulį į puslapį

Dėl išsamesnės informacijos apie tai, kaip konfigūruoti žemėlapio modulį puslapyje, žr. [Parduotuvės pasirinkimo modulis](store-selector.md). 
 
## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Parduotuvės išrinkiklio modulis](store-selector.md)

[„Bing“ žemėlapių valdymas jūsų organizacijoje](./dev-itpro/manage-bing-maps.md)

[„Bing Maps V8 Web Control“](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]