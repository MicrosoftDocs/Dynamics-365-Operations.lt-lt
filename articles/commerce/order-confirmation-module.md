---
title: Užsakymo patvirtinimo modulis
description: Šiame straipsnyje aprašomi užsakymų patvirtinimo moduliai ir aprašoma, kaip juos naudoti Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 994ec92abc53efeb240bca5dc8d67aabb45fbe55
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845810"
---
# <a name="order-confirmation-module"></a>Užsakymo patvirtinimo modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi užsakymų patvirtinimo moduliai ir aprašoma, kaip juos naudoti Microsoft Dynamics 365 Commerce.

Užsakymo patvirtinimo modulis yra naudojamas siekiant parodyti užsakymo patvirtinimo išsamią informaciją padarius užsakymą. Jis rodo užsakymo patvirtinimo ID, užsakymo kontaktinę informaciją ir kitą išsamią užsakymo informaciją, tokią kaip įsigytos prekės, mokėjimo informacijas, paėmimo parinktys ir siuntimo metodas.

## <a name="order-confirmation-module-properties"></a>Užsakymo patvirtinimo modulio ypatybės

| Ypatybės pavadinimas  | Reikšmės | Aprašymas |
|----------------|--------|-------------|
| Antraštė        | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Užsakymo patvirtinimo modulyje gali būti antraštė. Numatyta, kad naudojama antraštės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Kontaktinis numeris | Tekstas | Galite pateikti su užsakymais susijusių klausimų kontaktinį numerį. |
| Rodyti paėmimo laiko vietos informaciją | Teisinga arba klaidinga | Ši ypatybės yra prieinama „Dynamics 365 Commerce“ 10.0.15 ir vėlesnėse versijose. Kai jis teisingas, jis rodo paėmimo laiko vietos informaciją, jei pateikta paėmimo prekei|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a>Moduliai gali būti naudojami užsakymo patvirtinimo puslapyje

Jums sukūrus užsakymo patvirtinimo puslapį, galite įtraukti kitus būtinus modulius kartu su užsakymo patvirtinimo moduliu. Štai keletas pavyzdžių:

- **Rekomendacijų modulis** – Rekomendacijų modulis gali būti įtrauktas į užsakymo patvirtinimo puslapį siekiant patarti kitus produktus klientui.
- **Reklamos moduliai** – Bet kuris reklamos modulis gali būti įtrauktas į užsakymo patvirtinimo puslapį, kad rodytų reklamos turinį.

## <a name="add-an-order-confirmation-module-to-a-page"></a>Įtraukti užsakymo patvirtinimo modulį į puslapį

Norėdami įtraukti užsakymo patvirtinimo modulį į naują puslapį ir nustatyti reikiamas ypatybes, atlikite šiuos žingsnius.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lange **Naujas šablonas** prie Šablono **pavadinimas** įveskite pavadinimą Užsakymo **patvirtinimo šablonas** ir pasirinkite **Gerai**.
1. Teksto atminties **atminties** atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite numatytąjį puslapio **modulį**, tada pasirinkite **Gerai**.
1. Modulyje **Numatytasis** puslapis esantis **pagrindiniame atminties** atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite užsakymo **patvirtinimo modulį**, tada pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti** ir tada pasirinkite **Peržiūrėti**, kad peržiūrėtumėte šabloną. Užsakymo patvirtinimo modulis nebus sukurtas, nes jam reikia užsakymo patvirtinimo skaičiaus konteksto.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį**, po Puslapio pavadinimas **įveskite** užsakymo **patvirtinimo puslapį ir** pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną** pasirinkite **Užsakymo patvirtinimo šablonas** ir Pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**. 
1. Modulyje **Numatytasis** puslapis esantis **pagrindiniame atminties** atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite užsakymo **patvirtinimo modulį**, tada pasirinkite **Gerai**.
1. Ypatybių juostoje užsakymo patvirtinimo moduliui, pasirinkite **Antraštė** šalia pieštuko simbolio.
1. Laukelyje **Antraštės tekstas** skyriuje **Antraštės** teksto laukelyje, įveskite antraštės tekstą **Užsakymo patvirtinimas** ir tada pasirinkite **Gerai**.
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
