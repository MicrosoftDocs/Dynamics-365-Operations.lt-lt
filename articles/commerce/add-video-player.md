---
title: Vaizdo įrašų leistuvo modulis
description: Šioje temoje aprašomi vaizdo įrašų leistuvo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 12/02/2019
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
ms.openlocfilehash: 1c78583f39dbacdc7b38e89c33e67ae23731bf8a
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885906"
---
# <a name="video-player-module"></a>Vaizdo įrašų leistuvo modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi vaizdo įrašų leistuvo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Vaizdo įrašų leistuvo moduliai naudojami vaizdo įrašų atkūrimo galimybei palaikyti. Parduotuvės darbo pradžios rinkinyje pateikiami du vaizdo įrašų leistuvo moduliai: aplinkos vaizdo įrašų leistuvo modulis ir vaizdo įrašų leistuvo modulis. Abu leistuvai palaiko medijos tipą .mp4.

## <a name="ambient-video-player-module"></a>Aplinkos vaizdo įrašų leistuvo modulis

Aplinkos vaizdo įrašų leistuvo modulis palaiko trumpus informacinius vaizdo įrašus. Jis turėtų būti naudojamas vaizdo įrašams, kurių trukmė yra mažiau nei penkios sekundės. Šis leistuvas palaiko ribotą kiekį vaizdo įrašų atkūrimo galimybių, pvz., leidimą ir pristabdymą.

### <a name="examples-of-ambient-video-player-modules-in-e-commerce"></a>Aplinkos vaizdo įrašų leistuvo modulio pavyzdžiai el. prekyboje

- Trumpi informaciniai vaizdo įrašai, pagrindiniame puslapyje akcentuojantys naujus produktus
- Trumpi informaciniai vaizdo įrašai, produktų išsamios informacijos puslapyje akcentuojantys produktų ypatybes

### <a name="ambient-video-player-module-properties"></a>Aplinkos vaizdo įrašų leistuvo modulių ypatybės

| Ypatybės pavadinimas     | Vertė                 | Aprašymas |
|-------------------|-----------------------|-------------|
| Automatinis paleidimas          | **Teisinga** arba **Klaidinga** | Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas paleidžiamas automatiškai. |
| Nutildyti              | **Teisinga** arba **Klaidinga** | Kai reikšmė nustatoma kaip **Teisinga**, garsas yra nutildomas. Numatytoji šio leistuvo reikšmė yra **Teisinga**. Naršyklėje „Google Chrome“ automatiškai leidžiami vaizdo įrašai yra nutildyti pagal numatytuosius parametrus, o garsas leidžiamas, tik jei vartotojas pats paleidžia vaizdo įrašą. |
| Ciklas              | **Teisinga** arba **Klaidinga** | Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas vis kartojamas. |
| Publikavimo kanalai             |  Vaizdo įrašo failo kelias ir pavadinimas | Vaizdo įrašo failas, kurį leidžia vaizdo įrašų leistuvas. |
| Atkūrimo valdikliai | **Teisinga** arba **Klaidinga** | Kai reikšmė nustatoma kaip **Teisinga**, rodomas vaizdo įrašo leidimo / pristabdymo mygtukas. Jei reikšmė nustatyta kaip **Klaidinga**, leidimo / pristabdymo mygtukas nerodomas, tačiau vartotojai vaizdo įrašą vis tiek gali pristabdyti ir tęsti naudodami klaviatūrą. |

## <a name="video-player-module"></a>Vaizdo įrašų leistuvo modulis

Naudojant vaizdo įrašų leistuvo modulį, el. prekybos svetainėje galima parodyti vaizdo įrašus. Jis palaiko visas atkūrimo galimybes, pvz., leidimo, pristabdymo, viso dydžio režimo ir subtitrų. Vaizdo įrašų leistuvo modulis taip pat palaiko subtitrų tinkinimo galimybę, kad jie atitiktų „Microsoft“ pritaikymo neįgaliesiems standartus. Pavyzdžiui, galite tinkinti šrifto dydį ir fono spalvą.

Vaizdo įrašų leistuvo modulis taip pat palaiko antrinius garso takelius. Nusiunčiant vaizdo įrašą, taip pat galima nusiųsti antrinį garso takelį. Tada, jei vartotojas pasirenka antrinį garso takelį, vaizdo įrašų leistuvo modulis gali jį leisti.

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
| Atkūrimo valdikliai     | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, rodomas vaizdo įrašo leidimo / pristabdymo mygtukas. Jei reikšmė nustatyta kaip **Klaidinga**, leidimo / pristabdymo mygtukas nerodomas, tačiau vartotojai vaizdo įrašą vis tiek gali pristabdyti ir tęsti naudodami klaviatūrą. |
| Leisti visame ekrane       | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, vaizdo įrašas paleidžiamas viso ekrano režimu. |
| Valdikliai              | **Teisinga** arba **Klaidinga**               | Kai reikšmė nustatoma kaip **Teisinga**, rodomi visi valdikliai. Šie valdikliai apima leidimo ir pristabdymo mygtukus, eigos indikatorių bei subtitrus. |
| Slėpti atsklandą     | **Teisinga** arba **Klaidinga**               | Vaizdo įrašas gali turėti atsklandą. Kai šios ypatybės reikšmė nustatoma kaip **Teisinga**, atsklanda paslepiama. |
| Maskavimo lygis            | Skaičius nuo **0** iki **100** | Maskavimas, taikomas vaizdo įrašui dėl stiliaus. |
| Viso ekrano piktogramos stilius | **Kvadratas** arba **Rodyklė**             | Vaizdo įrašų leistuve rodomos viso ekrano piktogramos stilius. |

## <a name="add-a-video-player-module-to-a-page"></a>Vaizdo įrašų leistuvo modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti vaizdo įrašų leistuvo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite puslapio šabloną, pavadintą **vaizdo įrašų leistuvo šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį.
1. Konteinerio modulyje įtraukite vaizdo įrašų leistuvo ir aplinkos vaizdo įrašų leistuvo modulius.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Naudodami ką tik sukurtą vaizdo įrašų leistuvo šabloną, sukurkite puslapį, pavadintą **vaizdo įrašų leistuvo puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite aplinkos vaizdo įrašų leistuvo modulį.
1. Aplinkos vaizdo įrašų leistuvo parametruose nueikite į **Medija** ir nusiųskite vaizdo įrašo failą. Pagal poreikį galite keisti ypatybes **Automatinis paleidimas**, **Kartoti** ir kt.
1. Puslapį įrašykite ir peržiūrėkite.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite vaizdo įrašų leistuvo modulį.
1. Vaizdo įrašų leistuvo parametruose nueikite į **Medija** ir nusiųskite vaizdo įrašo failą.
1. Puslapį įrašykite ir peržiūrėkite. Puslapyje turėtumėte matyti abu vaizdo įrašų leistuvo modulius. Keisdami papildomus parametrus, galite tinkinti kiekvieno modulio veikimą.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Įspėjimo modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Turinio išdėstymo modulis](add-content-placement-modules.md)

[Funkcijos modulis](add-feature-module.md)

[Pagrindinės reklaminės juostos modulis](add-hero-module.md)
