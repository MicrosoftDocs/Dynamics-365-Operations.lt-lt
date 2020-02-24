---
title: Įvertinimų ir atsiliepimų konfigūravimas
description: Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002202"
---
# <a name="configure-ratings-and-reviews"></a>Įvertinimų ir atsiliepimų konfigūravimas


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.

## <a name="overview"></a>Peržiūrėti

El. prekybos svetainėse nurodyti įverčiai ir apžvalgos klientams padeda sužinoti apie produktus prieš priimant pirkimo sprendimą, nes jiems parodo, ką apie tuos produktus mano kiti klientai. El. prekybos svetainėse įverčiai ir apžvalgos taip pat yra mechanizmas klientų atsiliepimams apie produktus rinkti. 

Įverčiai rodomi produktų sąrašų puslapiuose, kategorijų sąrašų puslapiuose, ieškos rezultatų puslapiuose ir kituose svetainės puslapiuose. Įverčių histogramos ir produktų apžvalgos rodomos produktų išsamios informacijos puslapiuose (PIIP). Klientai pateikti produkto įverčius ir apžvalgas gali naudodami mygtuką **Rašyti apžvalgą**.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Įverčių ir apžvalgų moduliai PIIP puslapiuose 

PIIP puslapiuose įverčių ir apžvalgų suvestinę rodo tolesni trys moduliai.

- Apžvalgų rašymo modulis
- Produktų apžvalgų sąrašo modulis
- Įverčių histogramų modulis
 
Toliau pateiktoje iliustracijoje rodoma, kaip PIIP puslapyje atrodo įverčių ir apžvalgų moduliai.

![Įverčių ir apžvalgų moduliai PIIP puslapyje](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Norėdami gauti informacijos apie tai, kaip optimizuoti PIIP šablonus ir maketus, kad įverčių ir apžvalgų modulių konfigūracijas galėtumėte bendrai naudoti keliuose el. prekybos svetainės PIIP, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md).

Tolesnėje iliustracijoje parodyta, kaip „Dynamics 365 Commerce“ dialogo lange **Modulio įtraukimas** pateikiami įverčių ir apžvalgų moduliai.

![Dialogo langas Modulio įtraukimas](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Apžvalgų rašymo modulis

Apžvalgų rašymo modulyje yra mygtukas **Rašyti apžvalgą**, kurį naudodami vartotojai gali prisijungti, priskirti įvertį ir parašyti produkto apžvalgą. Naudodami šį modulį vartotojai taip pat gali redaguoti įvertį arba peržiūrėti, ką pateikė anksčiau. Šis modulis PIIP puslapyje paprastai rodomas virš įverčių histogramų ir produktų apžvalgų sąrašo modulių.

Tolesnėje iliustracijoje parodytas dialogo langas **Apžvalgos rašymas**, rodomas klientui pasirinkus **Rašyti apžvalgą**. Šiame dialogo lange klientas gali pateikti įvertį ir apžvalgą.

![Dialogo langas Apžvalgos rašymas](media/rnr-eCommerce-write-review-module.png)

Tolesnėje lentelėje parodyta apžvalgų rašymo modulio ypatybė, kurią reikia sukonfigūruoti kūrimo įrankyje.

| Ypatybės pavadinimas | Vertė        | Ypatybės aprašas                 |
|---------------|--------------|--------------------------------------|
| Vardas ir pavardė          | Rašyti apžvalgą | Apžvalgų rašymo modulio pavadinimas. |

### <a name="ratings-histogram-module"></a>Įverčių histogramų modulis

Įverčių histogramų modulyje rodoma įverčių histograma. Šis modulis PIIP puslapyje paprastai rodomas tarp apžvalgų rašymo modulio ir produktų apžvalgų sąrašo modulio.

Įverčių histogramų modulio konfigūruoti nereikia. Tereikia modulį įtraukti į PIIP šabloną. 

Tolesnėse iliustacijose parodyta, kaip programoje „Dynamics 365 Commerce“ atrodo PIIP šablonas, kai sukonfigūruota PIIP puslapiuose rodyti įverčių ir apžvalgų modulius.

![PIIP šablonas, kai sukonfigūruota PIIP puslapiuose rodyti įverčius ir apžvalgas](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Produktų apžvalgų sąrašo modulis

Produktų apžvalgų sąrašo modulyje rodomas produktų apžvalgų sąrašas su rikiavimo, filtravimo ir skaidymo į puslapius parinktimis. Šis modulis PIIP puslapyje paprastai rodomas už įverčių histogramų modulio.

Tolesnėje lentelėje parodytos produktų apžvalgų sąrašo modulio ypatybės, kurias reikia sukonfigūruoti kūrimo įrankyje.

| Ypatybės pavadinimas              | Vertė | Ypatybės aprašas |
|----------------------------|-------| ---------------------|
| Kiekviename puslapyje rodomos apžvalgos | 10    | Apžvalgų skaičius, kuris vienu metu turi būti rodomas PIIP puslapyje. Pateikti mygtukai **Kitas** ir **Ankstesnis**, kad vartotojai galėtų pereiti per apžvalgų puslapius. |

#### <a name="ratings-histogram--summary-view"></a>Įverčių histograma – suvestinės rodinys

Produktų apžvalgų sąrašo modulyje yra vieta, kurioje galite įtraukti įverčių histogramų modulį. Toliau pateiktoje iliustracijoje parodyta, kaip programoje „Dynamics 365 Commerce“ į produktų apžvalgų sąrašo modulį galite įtraukti įverčių histogramų modulį.

![Įverčių histogramų modulio įtraukimas į produktų apžvalgų sąrašo modulį](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos

Įverčių ir apžvalgų konfigūravimo reikšmės, pvz., nuomotojo ID, apžvalgos teksto ilgis ir apžvalgos pavadinimo ilgis, konfigūruojamos svetainės lygiu. 

Norėdami sukonfigūruoti svetainę, kad būtų rodomi įverčiai ir apžvalgos, atlikite tolesnius veiksmus. 

1. Nueikite į **Pradžia \> Svetainės**.
1. Pasirinkite savo svetainės pavadinimą. 
1. Nueikite į **Svetainės valdymas \> Išplečiamumas**. 
1. Lauke **Maks. apžvalgos teksto ilgis** įveskite maksimalų galimą apžvalgos teksto simbolių skaičių (pavyzdžiui, **1000**). 
1. Lauke **Maks. apžvalgos pavadinimo ilgis** įveskite maksimalų galimą apžvalgos pavadinimų simbolių skaičių (pavyzdžiui, **55**). 
1. Pasirinkite **Įrašyti ir publikuoti**. 

Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.

![Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Produkto įverčio susiejimas su PIIP skyriumi Apžvalgos

Produkto įvertis rodomas po produkto pavadinimu PIIP viršuje. Galima sukonfigūruoti, kad produkto įvertis būtų susietas su to paties PIIP skyriumi **Apžvalgos**. 

Norėdami produkto įvertį susieti su PIIP skyriumi **Apžvalgos**, atlikite tolesnius veiksmus.

1. Atidarykite PIIP šabloną. 
1. Nueikite į **Pirkimo langelio konteinerio modulių parametrai**.
1. Dalyje **Pirkimo langelis** pasirinkite **Produktų įverčiai**, tada pažymėkite žymės langelį **Spustelėjimą susieti su visų apžvalgų moduliu**.

Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.

![Produkto įverčio susiejimas su PIIP skyriumi Apžvalgos](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Privatumo ir strategijų puslapio saito konfigūravimas

Norėdami sukonfigūruoti privatumo ir strategijų puslapio saitą, atlikite tolesnius veiksmus.

1. Nueikite į **Pradžia \> Svetainės**.
1. Pasirinkite savo svetainės pavadinimą. 
1. Nueikite į **Svetainės valdymas \> Išplečiamumas**
1. Skirtuko **Maršrutai** dalyje **RNR privatumas ir strategija** pasirinkite **Įtraukti saitą**. Jei saitas jau įvestas ir norite jį pakeisti, jį pasirinkite. 
1. Dialogo lange **Saito įtraukimas** pasirinkite privatumo ir strategijos puslapio saitą ir **Gerai**. 
1. Pasirinkite **Įrašyti ir publikuoti**. 

Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.

![Privatumo ir strategijų puslapio saito konfigūravimas](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Prisijunkite, norėdami naudoti įvertinimus ir atsiliepimus](opt-in-ratings-reviews.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“](sync-product-ratings.md)
