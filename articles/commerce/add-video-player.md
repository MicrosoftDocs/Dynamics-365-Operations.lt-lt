---
title: Vaizdo įrašų leistuvo modulis
description: Šioje temoje aprašomi vaizdo įrašų leistuvo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025664"
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

### <a name="video-player-module-properties"></a>Vaizdo įrašų leistuvo modulių ypatybės

| Ypatybės pavadinimas         | Vertė                               | Aprašymas |
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

1. Sukurkite puslapio šabloną, pavadintą **vaizdo įrašų leistuvo šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.
1. Konteinerio modulyje įtraukite vaizdo įrašų leistuvo ir aplinkos vaizdo įrašų leistuvo modulius.
1. Baikite šablono redagavimą ir publikuokite.
1. Naudodami ką tik sukurtą vaizdo įrašų leistuvo šabloną, sukurkite puslapį, pavadintą **vaizdo įrašų leistuvo puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite vaizdo įrašų leistuvo modulį.
1. Vaizdo įrašų leistuvo modulio ypatybių srityje pasirinkite **Įtraukti vaizdo įrašą**.
1. Dialogo lange **Medijos parinkiklis** pasirinkite vaizdo įrašą, tada pasirinkite **Įkelti naują medijos elementą**.
1. Puslapį įrašykite ir peržiūrėkite. Puslapyje turėtumėte matyti vaizdo įrašų leistuvo modulį. Keisdami papildomus parametrus, galite tinkinti modulio veikimą.
1. Baikite puslapio redagavimą ir publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Reklaminės juostos modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Teksto bloko modulis](add-content-rich-block.md)

[Turinio bloko modulis](add-hero-module.md)
