---
title: Parduotuvės išrinkiklio modulis
description: Šiame straipsnyje aprašomas parduotuvės išrinkėjo modulis ir aprašoma, kaip įtraukti jį į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
manager: annbe
ms.openlocfilehash: aa3aed837072cb6c3d4f7f92bec2f4b700408cf7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268346"
---
# <a name="store-selector-module"></a>Parduotuvės išrinkiklio modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomas parduotuvės išrinkėjo modulis ir aprašoma, kaip įtraukti jį į svetainės puslapius Microsoft Dynamics 365 Commerce.

Klientai gali naudoti parduotuvės parinkėjo modulį tam, kad paimtų gaminį pasirinktoje parduotuvėje po pirkimo internetu. Prekybos versijoje 10.0.13, parduotuvės išrinkiklio modulis taip pat apima papildomas galimybes, kurios gali rodyti **Rasti parduotuvę** puslapį, kuris rodo šalia esančias parduotuves.

Parduotuvės selektoriaus modulis leidžia vartotojui įvesti vietą (miestą, valstybę, adresą ir taip toliau) parduotuvių paieškai paieškos spindulyje. Kai modulis yra atidaromas pirmą kartą, jis naudoja kliento naršymo vietą tam, kad surastų parduotuves (jei sutikimas yra duotas).

## <a name="store-selector-module-usage"></a>Parduotuvės selektoriaus modulio naudojimas

- Parduotuvės selektoriaus modulis gali būti naudojamas produkto informacijos puslapyje (PDP) siekiant pasirinkti parduotuvę paėmimui.
- Parduotuvės selektoriaus modulis gali būti naudojamas vežimėlio puslapyje siekiant pasirinkti parduotuvę paėmimui.
- Parduotuvės selektoriaus modulis gali būti naudojamas atskirame puslapyje, kuris rodo visas prieinamas parduotuves.

## <a name="fulfillment-group-setup-in-commerce-headquarters"></a>Įvykdymo grupės nustatymas „Commerce” būstinėje

Norint, kad parduotuvės selektorius rodytų galimas parduotuves, „Commerce” būstinėje turi būti nustatyta įvykdymo grupė. Daugiau informacijos rasite [Įvykdymo grupių nustatymas](customer-orders-overview.md#set-up-fulfillment-groups).

Be to, kiekvienai įvykdymo grupės parduotuvei, parduotuvės vietos platuma ir ilguma turi būti apibrėžta būstinėje.

Norėdami įvesti parduotuvės vietos „Commerce” būstinėje ilgumos ir platumos reikšmes, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargų paskirstymas**.
1. Kairiojoje srityje pasirinkite sandėlio vietą.
1. „FastTab” **Adresai** pasirinkite **Išplėstiniai**.

    ![Parduotuvės išsamios informacijos būstinėje pavyzdys.](./media/Store-address.png)

1. Veiksmų srityje pasirinkite **Redaguoti**.
1. „FastTab” **Bendra** įveskite **Platumos** ir **Ilgumos** reikšmes.

    ![Platumos ir ilgumos nustatymo parduotuvei būstinėje pavyzdys.](./media/Store-latitude-longitude.png)

1. Veiksmų srityje pasirinkite **Įrašyti**. 

### <a name="hide-a-store-from-the-store-selector-module"></a>Slėpti parduotuvę parduotuvės išrinkiklis modulyje

Kai kurios įvykdymo grupės parduotuvės gali būti negaliojančios paėmimo vietos. Norėdami užtikrinti, kad kaip parduotuvių išrinkiklio modulio pasirinktys bus rodomos tik tinkamos paėmimo vietos, atlikite šiuos veiksmus" "Commerce Headquarters".

1. Eikite į " **Retail" ir "Commerce \> Commerce" nustatymo \> įvykdymo grupes \> Visos parduotuvės**.
1. Veiksmų srityje pasirinkite **Redaguoti**.
1. Dalyje **Nustatymas** pažymėkite kiekvienos parduotuvės, kuri nėra tinkama paėmimo vieta, **žymės langelį Paėmimo** vieta.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Vykdykite 1070 kanalo konfigūracijos **paskirstymo** grafiko užduotį.

## <a name="bing-maps-integration"></a>„Bing“ žemėlapių integravimas

Parduotuvės selektoriaus modulis yra integruojamas su [„Bing Maps REST“ programa programavimo sąsajomis (API)](/bingmaps/rest-services/) siekiant naudoti „Bing Geocoding and Autosuggest“ funkcijomis. „Bing Maps“ API raktas yra reikalaujamas ir turi būti įtrauktas į bendrinamus parametrus komercijos štabo puslapyje „Geocoding API“ yra naudojamas konvertuoti vietą į ilgumos ir platumo vertes. Integravimas su „Autosuggest API“ yra naudojamas rodyti ieškos pasiūlymus, kai vartotojai įveda vietas paieškos lauke.

Dėl automatinio„REST API“, privalote užtikrinti, kad tolesni URL yra leidžiami savo saito turinio saugumo politikoje (CSP). Šis nustatymas yra atliekamas komercijos svetainės kūrimo įrankyje įtraukiant leidžiamus URL į skirtingas CSP gaires svetainei (pavyzdžiui, **img-src**). Dėl platesnės informacijos, žr. [Turinio saugos politika](manage-csp.md). 

- Į **connect-src** direktyvą, įtraukite **&#42;.bing.com**.
- Į **img-src** direktyvą, įtraukite **&#42;.virtualearth.net**.
- Į **script-src** direktyvą, **įtraukite &#42;.bing.com, &#42;.virtualearth.net**.
- Į **script style-src** direktyvą, įtraukite **&#42;.bing.com**.

## <a name="pickup-in-store-mode"></a>Paėmimas parduotuvės režime

Parduotuvės selektoriaus modulis palaiko **Atsiėmimas parduotuvėje** režimą, kuris rodo parduotuvių sąrašą, kuriose produktas yra prieinamas paėmimui. Jis taip pat rodo parduotuvės valandas ir produkto atsargas kiekvienai parduotuvei sąraše. Parduotuvės selektoriaus modulis reikalauja produkto turinio sukurti produkto prieinamumą ir leisti naudotojui įtraukti produktą į vežimėlį, jei produkto pristatymo režimas yra nustatytas į **paėmimą** pasirinktoje parduotuvėje. Norėdami gauti daugiau informacijos, žr. [inventoriaus parametrai](inventory-settings.md). 

Parduotuvės selektoriaus modulis gali būti įtrauktas siekiant įsigyti dėžutės modulį PDP tam, kad būtų parodytos parduotuvės, kuriose produktas yra prieinamas pasiėmimui. Jį taip pat galima pridėti prie krepšelio modulio. Šiuo atveju, parduotuvės selektoriaus modulis rodo pasiėmimo parinktis kiekvienos linijos elementui vežimėlyje. Parduotuvės selektoriaus modulis gali taip pat būti įtrauktas į kitus puslapius ar modulius per plėtinius ir tinkinimus.

Šiam scenarijui veikti, produktai turi būti sukonfigūruoti taip, kad **paėmimo** pristatymo režimas būtų naudojamas. Kitu atveju, modulis nebus rodomas produkto puslapiuose. Dėl daugiau informacijos apie tai, kaip konfigūruoti pristatymo režimą, žr. [Nustatyti pristatymo režimus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Toliau pateiktame paveikslėlyje vaizduojamas išsamios produkto informacijos puslapyje (PDP) naudojamo parduotuvių parinkiklio modulio pavyzdys.

![Parduotuvės parinkiklio modulio pavyzdys, kuris naudojamas PDP.](./media/BOPIS.PNG)

> [!NOTE]
> Versijoje 10.0.16 ir vėlesnėje versijoje, naujoji funkcija gali būti įjungta, kuri leidžia organizacijai nustatyti keletą paėmimo pristatymo būdų parinkčių klientams.  Jei ši funkcija įjungta, parduotuvės parinkėjas ir kiti e-komercijos moduliai bus pagerinti siekiant leisti klientui pasirinkti iš potencialiai kelių paėmimo pristatymo parinkčių, jei sukonfigūruota.  Norėdami sužinoti daugiau apie šią funkciją, žiūrėkite [šiuos dokumentus](./multiple-pickup-modes.md). 

## <a name="find-stores-mode"></a>Surasti parduotuvių režimą

Parduotuvės selektoriaus režimas taip pat palaiko **Rasti parduotuves** režimą. Šis režimas gali būti naudojamas siekiant sukurti talpinimo vietos puslapį, kuris rodo esamas parduotuves ir jų informaciją. Šiame režime parduotuvės selektoriaus modulis veikia be produkto konteksto ir gali būti naudojamas kaip vienas režimas bet kuriame vietos puslapyje. Taip pat, jei atitinkami parametrai yra įjungiami režimui, vartotojai gali pasirinkti laikyti jų pirmenybines parduotuves. Pasirinkus parduotuvę kaip vartotojo primenybinę parduotuvę, jos ID yra laikomas naršyklės slapukuose. Dėl to, vartotojas privalo priimti slapuko sutikimo žinutę.

Toliau pateiktas paveikslėlis rodo parduotuvės selektoriaus modulio pavyzdį, kuris yra naudojamas kartu su žemėlapio moduliu parduotuvės vietos puslapyje.

![Parduotuvės parinkiklio modulio ir žemėlapių modulio pavyzdys parduotuvių vietų puslapyje.](./media/ecommerce-Storelocator.PNG)

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

## <a name="site-settings"></a>Svetainės parametrai

Parduotuvės parinkiklio modulis laikosi [Įtraukti produktą į krepšelį parametrų](add-cart-settings.md). Kai prekė įtraukta į krepšelį iš parduotuvės parinkiklio modulio, svetainės vartotojai matys atitinkamas sukonfigūruotas darbo eigas.

## <a name="add-a-store-selector-module-to-a-page"></a>Parduotuvės parinkiklio modulio pridėjimas prie puslapio

**Atsiėmimui parduotuvėje** režimui, režimas gali būti naudojamas tik PDP ar vežimėlio puslapiuose. Privalote nustatyti režimą į **Atsiėmimas parduotuvėje** modulio ypatybių juostoje.

- Norėdami gauti informacijos apie tai, kaip pridėti parduotuvės parinkiklio modulį prie pirkimo langelio modulio, žr. [Pirkimo langelio modulis](add-buy-box.md). 
- Norėdami gauti informacijos apie tai, kaip pridėti parduotuvės parinkiklio modulį prie krepšelio modulio, žr. [Krepšelio modulis](add-cart-module.md).

Norėdami konfigūruoti parduotuvės išrinkėjo modulį, kad būtų galima rodyti galimas parduotuvės vietų puslapio parduotuves, kaip parodyta anksčiau šiame straipsnyje pateiktoje pavyzdyje, atlikite šiuos veiksmus.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lange **Naujas šablonas**, po Šablono **pavadinimu**, įveskite **Rinkodaros šabloną** ir pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį** po Puslapio pavadinimas **įveskite** Parduotuvės **vietos ir** pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną** pasirinkite rinkodaros šabloną **, kurį** sukūrėte, tada pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**. 
1. Naujo puslapio **pagrindiniame** atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerį **su 2 stulpelių** moduliu, tada pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite **Pločio** vertę į **Užpildyti konteinerį**.
1. Nustatykite **X-Small peržiūros prievado stulpelio konfigūravimo** vertę į **100%**.
1. Nustatykite **X-Small peržiūros prievado stulpelio konfigūravimo** vertę į **100%**.
1. Nustatykite **Medium peržiūros prievado stulpelio konfigūravimo** vertę į **33% 67%**.
1. Nustatykite **Didelio peržiūros prievado stulpelio konfigūravimo** vertę į **33% 67%**.
1. Konteineryje **su 2 stulpelių** atminties stulpeliu pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite parduotuvės išrinkiklis **modulį**, tada pasirinkite **Gerai**.
1. Modulio ypatybių juostoje, nustatykite **Režimo** vertę į **Rasti parduotuves**.
1. Nustatykite **Paieškos spindulio** vertę į mylias.
1. Nustatykite kitas ypatybes, tokias kaip **Nustatyti pirmenybinę parduotuvę**, **Rodyti visas parduotuves** ir **Įjungti automatinį siūlymą**, kaip norite.
1. Konteineryje **su 2 stulpelių** atminties stulpeliu pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius pasirinkite Schemą** **ir tada pasirinkite** Gerai **.**
1. Modulio ypatybių juostoje, nustatykite bet kurias papildomas ypatybes, kurias norite.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
 
## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Greitai susipažinkite su išsamios produkto informacijos puslapiu (PDP)](quick-tour-pdp.md)

[Greita krepšelio ir užsakymo formavimo apžvalga](quick-tour-cart-checkout.md)

[Nustatyti pristatymo būdus](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[„Bing“ žemėlapių valdymas jūsų organizacijoje](dev-itpro/manage-bing-maps.md)

[„Bing Maps REST“ API](/bingmaps/rest-services/)

[Žemėlapių modulis](map-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
