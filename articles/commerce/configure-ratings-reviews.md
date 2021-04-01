---
title: Įvertinimų ir atsiliepimų konfigūravimas
description: Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 130c80c1d68c7fb207a4fa073fe2b0476cbdd409
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220539"
---
# <a name="configure-ratings-and-reviews"></a>Įvertinimų ir atsiliepimų konfigūravimas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip sukonfigūruoti savo el. prekybos svetainę, kad programoje „Microsoft Dynamics 365 Commerce“ būtų rodomi klientų įverčiai ir apžvalgos.

## <a name="overview"></a>Peržiūra

El. prekybos svetainėse nurodyti įverčiai ir apžvalgos klientams padeda sužinoti apie produktus prieš priimant pirkimo sprendimą, nes jiems parodo, ką apie tuos produktus mano kiti klientai. El. prekybos svetainėse įverčiai ir apžvalgos taip pat yra mechanizmas klientų atsiliepimams apie produktus rinkti. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Svetainės sukonfigūravimas, kad būtų rodomi įverčiai ir apžvalgos

Įverčių ir apžvalgų konfigūravimo reikšmės, pvz., nuomotojo ID, apžvalgos teksto ilgis ir apžvalgos pavadinimo ilgis, konfigūruojamos svetainės lygiu. 

Norėdami sukonfigūruoti svetainę, kad būtų rodomi įverčiai ir apžvalgos, atlikite tolesnius veiksmus. 

1. Nueikite į **Pradžia \> Svetainės**.
1. Pasirinkite savo svetainės pavadinimą. 
1. Eiti į **Svetainės parametrai \> Plėtiniai**. 
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
1. Eiti į **Svetainės parametrai \> Plėtiniai**.
1. Skirtuko **Maršrutai** dalyje **RNR privatumas ir strategija** pasirinkite **Įtraukti saitą**. Jei saitas jau įvestas ir norite jį pakeisti, jį pasirinkite. 
1. Dialogo lange **Saito įtraukimas** pasirinkite privatumo ir strategijos puslapio saitą ir **Gerai**. 
1. Pasirinkite **Įrašyti ir publikuoti**. 

Tolesnėje iliustracijoje rodoma, kaip ši konfigūracija atrodo programoje „Dynamics 365 Commerce“.

![Privatumo ir strategijų puslapio saito konfigūravimas](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Įvertinimų ir atsiliepimų modulių produkto informacijos puslapiuose konfigūravimas

Informacijos, kaip konfigūruoti įvertinimus ir atsiliepimų modulius produkto informacijos puslapiuose, žr. [Įvertinimų ir atsiliepimų moduliai](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Įvertinimų ir atsiliepimų apžvalga](ratings-reviews-overview.md)

[Norėdami naudoti įvertinimus ir atsiliepimus, prisijunkite](opt-in-ratings-reviews.md)

[Įvertinimų ir atsiliepimų tvarkymas](manage-reviews.md)

[Įvertinimų ir atsiliepimų modulių produkto informacijos puslapiuose konfigūravimas](ratings-reviews-modules.md)

[Produktų įvertinimų sinchronizavimas sprendime „Dynamics 365 Retail“](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]