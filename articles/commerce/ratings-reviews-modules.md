---
title: Įvertinimų ir apžvalgų moduliai
description: Šiame straipsnyje aprašomas vertinimas ir peržiūros moduliai, naudojami produkto informacijos puslapiuose Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: f5829ccf9fad78e8669f5109d6c15e71af2ca768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894415"
---
# <a name="ratings-and-reviews-modules"></a>Įvertinimų ir apžvalgų moduliai

[!include [banner](includes/banner.md)]

Šiame straipsnyje rasite vertinimo ir peržiūros modulius, naudojamus produkto informacijos puslapiuose (PDPs)Microsoft Dynamics 365 Commerce.

El. prekybos svetainėse nurodyti įverčiai ir apžvalgos klientams padeda sužinoti apie produktus prieš priimant pirkimo sprendimą, taip pat tai yra mechanizmas, skirtas klientų atsiliepimams apie produktus surinkti. 

Įverčiai rodomi produktų sąrašų puslapiuose, kategorijų sąrašų puslapiuose, ieškos rezultatų puslapiuose ir kituose svetainės puslapiuose. 

Įverčių histogramos ir produktų apžvalgos rodomos produktų informacijos puslapiuose (PDP). Klientai pateikti produkto įverčius ir apžvalgas gali naudodami mygtuką **Rašyti apžvalgą**. Šios PDP funkcijos yra valdomos naudojant įverčių ir apžvalgų modulius.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Įverčių ir apžvalgų moduliai PIIP puslapiuose 

PIIP puslapiuose įverčių ir apžvalgų suvestinę rodo tolesni trys moduliai.
- Apžvalgų rašymo modulis
- Produktų apžvalgų sąrašo modulis
- Įverčių histogramų modulis
 
Toliau pateiktoje iliustracijoje rodoma, kaip PIIP puslapyje atrodo įverčių ir apžvalgų moduliai.

![Įverčių ir apžvalgų moduliai PIIP puslapyje.](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Norėdami gauti informacijos apie tai, kaip optimizuoti PIIP šablonus ir maketus, kad įverčių ir apžvalgų modulių konfigūracijas galėtumėte bendrai naudoti keliuose el. prekybos svetainės PIIP, žr. [Šablonų ir maketų apžvalga](templates-layouts-overview.md).

Tolesnėje iliustracijoje parodyta, kaip „Dynamics 365 Commerce“ dialogo lange **Modulio įtraukimas** pateikiami įverčių ir apžvalgų moduliai.
![Dialogo langas Modulio įtraukimas.](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Apžvalgų rašymo modulis

Apžvalgų rašymo modulyje yra mygtukas **Rašyti apžvalgą**, kurį naudodami vartotojai gali prisijungti, priskirti įvertį ir parašyti produkto apžvalgą. Naudodami šį modulį vartotojai taip pat gali redaguoti įvertį arba peržiūrėti, ką pateikė anksčiau. Šis modulis PIIP puslapyje paprastai rodomas virš įverčių histogramų ir produktų apžvalgų sąrašo modulių.
Tolesnėje iliustracijoje parodytas dialogo langas **Apžvalgos rašymas**, rodomas klientui pasirinkus **Rašyti apžvalgą**. Šiame dialogo lange klientas gali pateikti įvertį ir apžvalgą.

![Dialogo langas Apžvalgos rašymas.](media/rnr-eCommerce-write-review-module.png)

Tolesnėje lentelėje parodyta apžvalgų rašymo modulio ypatybė, kurią reikia sukonfigūruoti kūrimo įrankyje.

| Ypatybės pavadinimas | Vertė        | Ypatybės aprašas                 |
|---------------|--------------|--------------------------------------|
| Vardas ir pavardė          | Rašyti apžvalgą | Apžvalgų rašymo modulio pavadinimas. |

### <a name="ratings-histogram-module"></a>Įverčių histogramų modulis

Įverčių histogramų modulyje rodoma įverčių histograma. Šis modulis PIIP puslapyje paprastai rodomas tarp apžvalgų rašymo modulio ir produktų apžvalgų sąrašo modulio.
Įverčių histogramų modulio konfigūruoti nereikia. Tereikia modulį įtraukti į PIIP šabloną. Tolesnėse iliustracijose parodyta, kaip programoje „Dynamics 365 Commerce“ atrodo PIIP šablonas, kai sukonfigūruota PIIP puslapiuose rodyti įverčių ir apžvalgų modulius.
![PIIP šablonas, kai sukonfigūruota PIIP puslapiuose rodyti įverčius ir apžvalgas.](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Produktų apžvalgų sąrašo modulis

Produktų apžvalgų sąrašo modulyje rodomas produktų apžvalgų sąrašas su rikiavimo, filtravimo ir skaidymo į puslapius parinktimis. Šis modulis PIIP puslapyje paprastai rodomas už įverčių histogramų modulio.
Tolesnėje lentelėje parodytos produktų apžvalgų sąrašo modulio ypatybės, kurias reikia sukonfigūruoti kūrimo įrankyje.

| Ypatybės pavadinimas              | Vertė | Ypatybės aprašas |
|----------------------------|-------| ---------------------|
| Kiekviename puslapyje rodomos apžvalgos | 10    | Apžvalgų skaičius, kuris vienu metu turi būti rodomas PIIP puslapyje. Pateikti mygtukai **Kitas** ir **Ankstesnis**, kad vartotojai galėtų pereiti per apžvalgų puslapius. |

#### <a name="ratings-histogram--summary-view"></a>Įverčių histograma – suvestinės rodinys

Produktų apžvalgų sąrašo modulyje yra vieta, kurioje galite įtraukti įverčių histogramų modulį. Toliau pateiktoje iliustracijoje parodyta, kaip programoje „Dynamics 365 Commerce“ į produktų apžvalgų sąrašo modulį galite įtraukti įverčių histogramų modulį.

![Įverčių histogramų modulio įtraukimas į produktų apžvalgų sąrašo modulį.](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]