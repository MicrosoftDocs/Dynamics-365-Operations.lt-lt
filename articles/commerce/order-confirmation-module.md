---
title: Užsakymo patvirtinimo modulis
description: Šioje temoje aprašomi užsakymo patvirtinimo modeliai ir jis aprašo, kaip juos naudoti „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972753"
---
# <a name="order-confirmation-module"></a>Užsakymo patvirtinimo modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi užsakymo patvirtinimo modeliai ir jis aprašo, kaip juos naudoti „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Užsakymo patvirtinimo modulis yra naudojamas siekiant parodyti užsakymo patvirtinimo išsamią informaciją padarius užsakymą. Jis rodo užsakymo patvirtinimo ID, užsakymo kontaktinę informaciją ir kitą išsamią užsakymo informaciją, tokią kaip įsigytos prekės, mokėjimo informacijas, paėmimo parinktys ir siuntimo metodas.

## <a name="order-confirmation-module-properties"></a>Užsakymo patvirtinimo modulio ypatybės

| Ypatybės pavadinimas  | Reikšmės | Aprašymas |
|----------------|--------|-------------|
| Antraštė        | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Užsakymo patvirtinimo modulyje gali būti antraštė. Numatyta, kad naudojama antrašės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Kontaktinis numeris | Tekstas | Galite pateikti su užsakymais susijusių klausimų kontaktinį numerį. |
| Rodyti paėmimo laiko vietos informaciją | Teisinga arba klaidinga | Ši ypatybės yra prieinama „Dynamics 365 Commerce“ 10.0.15 ir vėlesnėse versijose. Kai jis teisingas, jis rodo paėmimo laiko vietos informaciją, jei pateikta paėmimo prekei|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Moduliai gali būti naudojami užsakymo patvirtinimo puslapyje

Jums sukūrus užsakymo patvirtinimo puslapį, galite įtraukti kitus būtinus modulius kartu su užsakymo patvirtinimo moduliu. Štai keletas pavyzdžių:

- **Rekomendacijų modulis** – Rekomendacijų modulis gali būti įtrauktas į užsakymo patvirtinimo puslapį siekiant patarti kitus produktus klientui.
- **Reklamos moduliai** – Bet kuris reklamos modulis gali būti įtrauktas į užsakymo patvirtinimo puslapį, kad rodytų reklamos turinį.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Įtraukti užsakymo patvirtinimo modulį į puslapį

Norėdami įtraukti užsakymo patvirtinimo modulį į naują puslapį ir nustatyti reikiamas ypatybes, atlikite šiuos žingsnius.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Teksto laukelyje **Naujas šablonas** skyriuje **Šablono pavadinimas**, įtveskite pavadinimą **Užsakymo patvirtinimo šablonas** ir tada pasirinkite **Gerai**.
1. Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.
1. Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.
1. Teksto laukelyje **Įtraukite modulį** pasirinkite **Užsakymo patvirtinimo** modulis ir tada rinkitės **Gerai**.
1. Pasirinkite **Įrašyti** ir tada pasirinkite **Peržiūrėti**, kad peržiūrėtumėte šabloną. Užsakymo patvirtinimo modulis nebus sukurtas, nes jam reikia užsakymo patvirtinimo skaičiaus konteksto.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Teksto laukelyje **Pasirinkti šabloną** rinkitės **Užsakymo patvirtinimo šablonas**. Skyriuje **Puslapio pavadinimas**, įveskite **Užsakymo patvirtinimo puslapis** ir tada pasirinkite **Gerai**.
1. Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.
1. Teksto laukelyje **Įtraukite modulį** pasirinkite **Užsakymo patvirtinimo** modulis ir tada rinkitės **Gerai**.
1. Ypatybių juostoje užsakymo patvirtinimo moduliui, pasirinkite **Antraštė** šalia pieštuko simbolio.
1. Laukelyje **Antraštės tekstas** skyriuje **Antraštės** teksto laukelyje, įtveskite antraštės tekstą **Užsakymo patvirtinimas** ir tada pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Mokėjimo modulis](payment-module.md)

[Siuntimo adreso modulis](ship-address-module.md)

[Pristatymo parinkčių modulis](delivery-options-module.md)

[Paėmimo informacijos modulis](pickup-info-module.md)

[Dovanų kortelės modulis](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]