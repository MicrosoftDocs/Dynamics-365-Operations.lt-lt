---
title: Vaizdo įrašų leistuvo modulis
description: Šioje temoje aprašomi vaizdo įrašų leistuvo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612682d310362c7523bf08db40faf51c80ea2e3
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411164"
---
# <a name="video-player-module"></a>Vaizdo įrašų leistuvo modulis


[!include [banner](includes/banner.md)]

Šioje temoje aprašomi vaizdo įrašų leistuvo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Vaizdo įrašų leistuvo modulis naudojamas vaizdo įrašų atkūrimo galimybei palaikyti. Jis gali būti įtrauktas į bet kurį puslapį, jei vaizdo įrašo turinys įkeliamas ir pasiekiamas turinio valdymo sistemoje (TVS). Vaizdo įrašų leistuvo modulis palaiko .mp4 medijos tipą.

## <a name="video-player-module"></a>Vaizdo įrašų leistuvo modulis

Naudojant vaizdo įrašų leistuvo modulį, el. prekybos svetainėje galima parodyti vaizdo įrašus. Jis palaiko visas atkūrimo galimybes, pvz., leidimo, pristabdymo, viso dydžio režimo, garso aprašymų ir subtitrų. Vaizdo įrašų leistuvo modulis taip pat palaiko subtitrų tinkinimo galimybę, kad jie atitiktų „Microsoft“ pritaikymo neįgaliesiems standartus. Pavyzdžiui, galite tinkinti šrifto dydį ir fono spalvą.

Vaizdo įrašų leistuvo modulis taip pat palaiko antrinius garso takelius. Įkeliant vaizdo įrašą TVS, taip pat galima įkelti antrinį garso takelį. Tada, jei vartotojas pasirenka antrinį garso takelį, vaizdo įrašų leistuvo modulis gali jį leisti.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Vaizdo įrašų leistuvo modulio pavyzdžiai el. prekyboje

- Mokomieji vaizdo įrašai produktų išsamios informacijos puslapiuose ar rinkodaros puslapiuose
- Reklaminiai vaizdo įrašai arba vaizdo įrašai apie strategijas bet kuriame rinkodaros puslapyje
- Rinkodaros vaizdo įrašai, akcentuojantys produktų ypatybes produktų išsamios informacijos puslapiuose ar rinkodaros puslapiuose

Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio vaizdo įrašų leistuvo modulio pavyzdys.

![Vaizdo įrašų leistuvo modulio pavyzdys](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Vaizdo įrašų leistuvo modulių ypatybės

| Ypatybės pavadinimas         | Vertė                               | aprašymas |
|-----------------------|-------------------------------------|-------------|
| Automatinis paleidimas             | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas paleidžiamas automatiškai. |
| Nutildyti                  | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, garsas yra nutildomas. Numatytoji šio leistuvo reikšmė yra **Klaidinga**. Naršyklėje „Chrome“ automatiškai leidžiami vaizdo įrašai yra nutildyti pagal numatytuosius parametrus, o garsas leidžiamas, tik jei vartotojas pats paleidžia vaizdo įrašą. |
| Ciklas                  | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas vis kartojamas. |
| Publikavimo kanalai                 | Vaizdo įrašo failo kelias ir pavadinimas | Vaizdo įrašo failas, leidžiamas vaizdo įrašų leistuve. |
| Leisti visame ekrane       | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas paleidžiamas viso ekrano režimu. |
| Paleidiklis Leisti / pristabdyti    | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, rodomas vaizdo įrašo leidimo / pristabdymo mygtukas. |
| Vaizdo įrašų leistuvo valdikliai | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, rodomi visi vaizdo įrašų leistuvo valdikliai. Šie valdikliai apima leidimo ir pristabdymo mygtukus, eigos indikatorių bei subtitrų parinktis. |
| Slėpti plakato vaizdą     | **Teisinga** arba **Klaidinga**               | Vaizdo įrašas gali turėti atsklandą. Kai šios ypatybės reikšmė nustatoma kaip **Teisinga**, atsklanda paslepiama. |
| Maskavimo lygis            | Skaičius nuo **0** iki **100** | Maskavimas, taikomas vaizdo įrašui dėl stiliaus. |

## <a name="add-a-video-player-module-to-a-page"></a>Vaizdo įrašų leistuvo modulio įtraukimas į puslapį

> [!NOTE] 
> Prieš kurdami vaizdo įrašų leistuvo modulį, pirmiausia turite įkelti vaizdo įrašą į medijų biblioteką.

Norėdami į naują puslapį įtraukti vaizdo įrašų leistuvo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Vaizdo įrašų leistuvo šablonas** ir pasirinkite **Gerai**.
1. Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.
1. Modulio **Numatytasis puslapis** vietoje **Pagrindinis** pasirinkite daugtaškį (**...**) ir **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Vaizdo įrašų leistuvas**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. 
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Pasirinkti šabloną** pasirinkite vaizdo įrašų leistuvo šabloną, kurį sukūrėte. Dalyje **Puslapio pavadinimas** įveskite **Vaizdo įrašų leistuvo puslapis**, tada pasirinkite **Gerai**.
1. Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Vaizdo įrašų leistuvas**, tada pasirinkite **Gerai**.
1. Vaizdo įrašų leistuvo modulio ypatybių srityje pasirinkite **Įtraukti vaizdo įrašą**.
1. Dialogo lange **Medijos parinkiklis** pasirinkite vaizdo įrašą, tada pasirinkite **Įkelti naują medijos elementą**.
1. Failų naršyklėje pasirinkite vaizdo įrašo failą ir pasirinkite **Atidaryti**.
1. Dialogo lange **Įkelti medijos elementą** įveskite pavadinimą ir kitą reikiamą informaciją, tada pasirinkite **Gerai**.
1. Dialogo lange **Medijos parinkiklis** pasirinkite **Uždaryti**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Puslapyje turėtumėte matyti vaizdo įrašų leistuvo modulį. Keisdami papildomus parametrus, galite tinkinti modulio veikimą.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Reklaminės juostos modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Teksto bloko modulis](add-content-rich-block.md)

[Turinio bloko modulis](add-hero-module.md)
