---
title: Parduotuvės parinkiklio modulis
description: Šioje temoje paaiškinamas parduotuvės parinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5400a2e743a78124dca4bf9be3ccaf7870ea8b7d
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665277"
---
# <a name="store-selector-module"></a>Parduotuvės parinkiklio modulis

[!include [banner](includes/banner.md)]

Šioje temoje paaiškinamas parduotuvės parinkiklio modulis ir aprašoma, kaip pridėti jį prie svetainių puslapių, esančių „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Klientai gali naudoti parduotuvės parinkėjo modulį tam, kad paimtų gaminį pasirinktoje parduotuvėje po pirkimo internetu. Prekybos versijoje 10.0.13, parduotuvės sleketoriaus modulis taip pat apima papildomas galimybes, kurios gali rodyti **Rasti parduotuvę** puslapį, kuris rodo šalia esančias parduotuves.

Parduotuvės selektoriaus modulis leidžia vartotojui įvesti veitą (miestą, valstybę, adresą ir taip toliau) parduotuvių paieškai paieškos spindulyje. Kai modulis yra atidaromas pirmą kartą, jis naudoja kliento naršymo vietą tam, kad surastų parduotuves (jei sutikimas yra duotas).

## <a name="store-selector-module-usage-in-e-commerce"></a>Parduotuvės parinkiklio modulio naudojimas „e-Commerce“

- Parduotuvės selektoriaus modulis gali būti naudojamas produkto informacijos puslapyje (PDP) siekiant pasirinkti parduotuvę paėmimui.
- Parduotuvės selektoriaus modulis gali būti naudojamas vežimėlio puslapyje siekiant pasirinkti parduotuvę paėmimui.
- Parduotuvės selektoriaus modulis gali būti naudojamas atskirame puslapyje, kuris rodo visas prieinamas parduotuves.

## <a name="bing-maps-integration"></a>„Bing“ žemėlapių integravimas

Parduotuvės selektoriaus modulis yra integruojamas su [„Bing Maps REST“ programa programavimo sąsajomis (API)](https://docs.microsoft.com/bingmaps/rest-services/) siekiant naudoti „Bing Geocoding and Autosuggest“ funkcijomis. „Bing Maps“ API raktas yra reikalaujamas ir turi būti įtrauktas į bendrinamus parametrus komercijos štabo puslapyje „Geocoding API“ yra naudojamas konvertuoti vietą į ilgumos ir platumo vertes. Integravimas su „Autosuggest API“ yra naudojamas rodyti ieškos pasiūlymus, kai vartotojai įveda vietas paieškos lauke.

Dėl automatinio„REST API“, privalote užtikrinti, kad tolesni URL yra leidžiami savo saito turinio saugumo politikoje (CSP). Šis nustatymas yra atliekamas komercijos svetainės kūrimo įrankyje įtraukiant leidžiamus URL į skirtingas CSP gaires svetainei (pavyzdžiui, **img-src**). Dėl platesnės informacijos, žr. [Turinio saugos politika](manage-csp.md). 

- Į **connect-src** direktyvą, įtraukite **&#42;.bing.com**.
- Į **img-src** direktyvą, įtraukite **&#42;.virtualearth.net**.
- Į **script-src** direktyvą, **įtraukite &#42;.bing.com, &#42;.virtualearth.net**.
- Į **script style-src** direktyvą, įtraukite **&#42;.bing.com**.
 
## <a name="pickup-in-store-mode"></a>Paėmimas parduotuvės režime

Parduotuvės selektoriaus modulis palaiko **Atsiėmimas parduotuvėje** režimą, kuris rodo parduotuvių sąrašą, kuriose produktas yra prieinamas paėmimui. Jis taip pat rodo parduotuvės valandas ir produkto atsargas kiekvienai parduotuvei sąraše. Parduotuvės selektoriaus modulis reikalauja produkto turinio sukurti produkto prieinamumą ir leisti naudotojui įtraukti produktą į vežimėlį, jei produkto pristatymo režimas yra nustatytas į **paėmimą** pasirinktoje parduotuvėje. Norėdami gauti daugiau informacijos, žr. [inventoriaus parametrai](inventory-settings.md). 

Parduotuvės selektoriaus modulis gali būti įtrauktas siekiant įsigyti dėžutės modulį PDP tam, kad būtų parodytos parduotuvės, kuriose produktas yra prieinamas pasiėmimui. Jį taip pat galima pridėti prie krepšelio modulio. Šiuo atveju, parduotuvės selektoriaus modulis rodo pasiėmimo parinktis keikvienos linijos elementui vežimėlyje. Parduotuvės selektoriaus modulis gali taip pat būti įtrauktas į kitus puslapius ar modulius per plėtinius ir tinkinimus.

Šiam scenarijui veikti, produktai turi būti sukonfigūruoti taip, kad **paėmimo** pristatymo režimas būtų naudojamas. Kitu atveju, modulis nebus rodomas produkto puslapiuose. Dėl daugiau informacijos apie tai, kaip konfigūruoti pristatymo režimą, žr. [Nustatyti pristatymo režimus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Toliau pateiktame paveikslėlyje vaizduojamas išsamios produkto informacijos puslapyje (PDP) naudojamo parduotuvių parinkiklio modulio pavyzdys.

![Parduotuvės parinkiklio modulio pavyzdys, naudojamas PDP.](./media/BOPIS.PNG)

> [!NOTE]
> Versijoje 10.0.16 ir vėlesnėje versijoje, naujoji funkcija gali būti įjungta, kuri leidžia organizacijai nustatyti keletą paėmimo pristatymo būdų parinkčių klientams.  Jei ši funkcija įjungta, parduotuvės parinkėjas ir kiti e-komercijos moduliai bus pagerinti siekiant leisti klientui pasirinkti iš potencialiai kelių paėmimo pristatymo parinkčių, jei sukonfigūruota.  Norėdami sužinoti daugiau apie šią funkciją, žiūrėkite [šiuos dokumentus](https://docs.microsoft.com/dynamics365/commerce/multiple-pickup-modes). 

## <a name="find-stores-mode"></a>Surasti parduotuvių režimą

Parduotuvės selektoriaus režimas taip pat palaiko **Rasti parduotuves** režimą. Šis režimas gali būti naudojamas siekiant sukurti talpinimo vietos puslapį, kuris rodo esamas parduotuves ir jų informaciją. Šiame režime parduotuvės selektoriaus modulis veikia be produkto konteksto ir gali būti naudojamas kaip vienas režimas bet kuriame vietos puslapyje. Taip pat, jei atitinkami parametrai yra įjungiami režimui, vartotojai gali pasirinkti laikyti jų pirmenybines parduotuves. Pasirinkus parduotuvę kaip vartotojo primenybinę parduotuvę, jos ID yra laikomas naršyklės slapukuose. Dėl to, vartotojas privalo priimti slapuko sutikimo žinutę.

Toliau pateiktas paveikslėlis rodo parduotuvės selektoriaus modulio pavyzdį, kuris yra naudojamas kartu su žemėlapio moduliu parduotuvės vietos puslapyje.

![Parduotuvės parinkiklio modulio ir žemėlapių modulio pavyzdys parduotuvės vietų puslapyje.](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a>Žemėlapio kūrimas

Parduotuvės selektoriaus modulis gali būti naudojamas kartu su žemėlapio moduliu tam, kad būtų parodyta parduotuvės vieta žemėlapyje. Dėl daugiau informacijos apie žemėlapio modulį, žr. [Žemėlapio modulis](map-module.md).

## <a name="store-selector-module-properties"></a>Parduotuvės parinkiklio modulio ypatybės

| Ypatybės pavadinimas | Vertė | aprašymas |
|---------------|-------|-------------|
| Antraštė | Tekstas | Modulio antraštė. |
| Režimas | **Rasti parduotuves** ar **Atsiimti parduotuvėje** | **Rasti parduotuves** režimas rodo prieinamas parduotuves. **Atsiėmimas parduotuvėje** režimas leidžia vartotojams pasirinkti laikymą paėmimui. |
| Stilius | **Tekstas** ar **Sulygintas su linija** | Modulis gali būti sukuriamas pagal liniją, arba teksto laukelyje. |
| Nustatyti kaip pageidaujamą parduotuvę | **Teisinga** arba **Klaidinga** | Kai ši ypatybė yra nustatyta į **Teisinga**, vartotojai gali nustatyti pirmenybinę parduotuvę. Ši funkcija reikalauja, kad vartotojai priimtų slapuko sutikimo žinutę. |
| Rodyti visas parduotuves | **Teisinga** arba **Klaidinga** | Kai ši ypatybė yra nustatyta **Teisinga**, vartotojai gali apeiti **Ieškos spindulio** ypatybes ir peržiūrėti visas parduotuves. |
| Automatiniu siūlymo parinktys: maksimalūs rezultatai | Skaičius | Šios ypatybės nustato maksimalų automatinių siūlymų rezultatų skaičių, kurie gali būti rodomi per „Bing Autosuggest“ API. |
| Ieškos spindulys | Skaičius | Šios ypatybės nustato ieškos spindulį parduotuvėms myliomis. Jeigu vertė nenurodyta, naudojamas numatytasis 50 mylių ieškos spindulys. |
| Paslaugų teikimo sąlygos | URL |  Šios ypatybės nustato paslaugų teikimo sąlygas URL, kurios yra reikalaujamos naudoti „Bing Maps“ paslaugoms. |

## <a name="add-a-store-selector-module-to-a-page"></a>Parduotuvės parinkiklio modulio pridėjimas prie puslapio

**Atsiėmimui parduotuvėje** režimui, režimas gali būti naudojamas tik PDP ar vežimėlio puslapiuose. Privalote nustatyti režimą į **Atsiėmimas parduotuvėje** modulio ypatybių juostoje.

- Norėdami gauti informacijos apie tai, kaip pridėti parduotuvės parinkiklio modulį prie pirkimo langelio modulio, žr. [Pirkimo langelio modulis](add-buy-box.md). 
- Norėdami gauti informacijos apie tai, kaip pridėti parduotuvės parinkiklio modulį prie krepšelio modulio, žr. [Krepšelio modulis](add-cart-module.md).

Tam, kad sukonfigūruotumėte selektoriaus modulį ir jis rodytų esamas parduotuves parduotuvių vietų puslapyje, kaip paveikslėlyje, kuris pasirodo šioje temoje, atlikite šiuos žingsnius.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. **Naujo šablono** teksto laukelyje, skyriuje **Šablono pavadinimas** įveskite **Komercijos šablono** ir tuomet pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. **Pasirinkite šabloną** teksto laukelyje, pasirinkite **Komercijos šablono** šabloną. Skyriuje **Puslapio pavadinimas**, įveskite **Parduotuvių vietos** ir tuomet pasirinkite **Gerai**.
1. Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. **Modulio įtraukimo** teksto laukelyje pasirinkite **Konteineris su dviem stulpeliais** modulį ir tuomet pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Nustatykite **X-Small peržiūros prievado stulpelio konfigūravimo** vertę į **100%**.
1. Nustatykite **X-Small peržiūros prievado stulpelio konfigūravimo** vertę į **100%**.
1. Nustatykite **Medium peržiūros prievado stulpelio konfigūravimo** vertę į **33% 67%**.
1. Nustatykite **Didelio peržiūros prievado stulpelio konfigūravimo** vertę į **33% 67%**.
1. **Konteinerio su dviem stulpeliais** vietoje pasirinkite elipsę (**...**), ir tuomet pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Parduotuvės parinkiklis**, tada pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite **Režimo** vertę į **Rasti parduotuves**.
1. Nustatykite **Paieškos spindulio** vertę į mylias.
1. Nustatykite kitas ypatybes, tokias kaip **Nustatyti pirmenybinę parduotuvę**, **Rodyti visas parduotuves** ir **Įjungti automatinį siūlymą**, kaip norite.
1. **Konteinerio su dviem stulpeliais** vietoje pasirinkite elipsę (**...**), ir tuomet pasirinkite **Įtraukti modulį**.
1. **Modulio įtraukimo** teksto laukelyje pasirinkite **Žemėlapio** modulį ir tuomet pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite bet kurias papildomas ypatybes, kurias norite.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
 
## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Greitai susipažinkite su išsamios produkto informacijos puslapiu (PDP)](quick-tour-pdp.md)

[Greita krepšelio ir užsakymo formavimo apžvalga](quick-tour-cart-checkout.md)

[Nustatyti pristatymo būdus](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[„Bing“ žemėlapių valdymas jūsų organizacijoje](dev-itpro/manage-bing-maps.md)

[„Bing Maps REST“ API](https://docs.microsoft.com/bingmaps/rest-services/)

[Žemėlapių modulis](map-module.md)
