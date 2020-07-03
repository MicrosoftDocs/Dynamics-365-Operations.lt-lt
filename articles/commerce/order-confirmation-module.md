---
title: Išsamios užsakymo informacijos modulis
description: Šioje temoje aprašomi išsamios užsakymo informacijos moduliai ir jų naudojimas „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464935"
---
# <a name="order-details-module"></a>Išsamios užsakymo informacijos modulis


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi išsamios užsakymo informacijos moduliai ir jų naudojimas „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

Išsamios užsakymo informacijos modulis pateikia užsakymo patvirtinimo informaciją. Pateikiamas užsakymo patvirtinimo ID, užsakymo kontaktinė informacija ir kita išsami informacija apie užsakymą, kaip pvz., įsigytos prekės, mokėjimo informacija ir pristatymo būdas.

## <a name="order-details-module-properties"></a>Užsakymo išsamios informacijos modulio ypatybės

| Ypatybės pavadinimas  | Reikšmės | aprašymas |
|----------------|--------|-------------|
| Antraštė        | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Užsakymo išsamios informacijos modulis gali turėti antraštę. Numatyta, kad naudojama antrašės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Kontaktinis numeris | Tekstas | Galite pateikti su užsakymais susijusių klausimų kontaktinį numerį. |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a>Moduliai, kuriuos galima naudoti užsakymo informacijos puslapyje

Kurdami išsamios užsakymo informacijos puslapį, prie užsakymo informacijos modulio galite pridėti ir kitus svarbius modulius. Štai keletas pavyzdžių:

- **Rekomendacijų modulis** – jis gali būti pridėtas prie išsamios užsakymo informacijos puslapio, kad klientui būtų pasiūlyti kiti produktai.
- **Rinkodaros moduliai** – prie išsamios užsakymo informacijos puslapio galima pridėti bet kurį rinkodaros modulį, kad būtų parodytas rinkodaros turinys.

## <a name="add-an-order-details-module-to-a-page"></a>Pridėkite užsakymo išsamios informacijos modulį prie puslapio

Norėdami pridėti užsakymo išsamios informacijos modulį naujame puslapyje ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. **Naujas šablonas** dialogo lange po **Šablono pavadinimas** įveskite pavadinimą **Užsakymo išsamios informacijos šablonas** ir pasirinkite **Gerai**.
1. Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.
1. Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.
1. Dialogo lange **Pridėti modulį** pasirinkite **Užsakymo išsami informacija** modulį, tada pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti** ir tada pasirinkite **Peržiūrėti**, kad peržiūrėtumėte šabloną. Užsakymo informacijos modulis nebus atvaizduotas, nes tam reikalingas užsakymo patvirtinimo numerio kontekstas.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite **Užsakymo išsamios informacijos šablonas**. Po **Puslapio pavadinimas** įveskite **Užsakymo išsamios informacijos puslapis**, tada pasirinkite **Gerai**.
1. Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.
1. Dialogo lange **Pridėti modulį** pasirinkite **Užsakymo išsami informacija** modulį, tada pasirinkite **Gerai**.
1. Užsakymo išsamios informacijos modulio ypatybių srityje, šalia pieštuko simbolio, pasirinkite **Antraštė**.
1. **Antraštės tekstas** lauke **Antraštė** dialogo lango įveskite antraštės tekstą **Užsakymo išsami informacija** ir pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulį](add-checkout-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
