---
title: Turinio bloko modulis
description: Šioje temoje aprašomi turinio bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0a3fd442f20fd40cdf8b845d353ae5d61ce51e29
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797652"
---
# <a name="content-block-module"></a>Turinio bloko modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi turinio bloko moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

Turinio bloko modulis naudojamas produktams ar akcijoms reklamuoti derinant vaizdus ir tekstą. Pavyzdžiui, pardavėjas turinio bloko modulį gali įtraukti į pagrindinį el. prekybos svetainės puslapį, kad reklamuotų naują produktą ir pritrauktų klientų dėmesį.

Turinio bloko modulis grindžiamas duomenimis iš turinio valdymo sistemos (TVS). Tai yra atskiras modulis, nepriklausantis nuo jokių kitų puslapio modulių. Turinio bloko modulį galima įdėti bet kuriame svetainės puslapyje, kuriame pardavėjas nori kažką parduoti ar reklamuoti, (pavyzdžiui, produktus, išpardavimus ar ypatybes).

## <a name="examples-of-content-block-module-in-e-commerce"></a>Turinio bloko modulių pavyzdžiai el. prekyboje

- Turinio bloko modulį galima naudoti pagrindiniame el. prekybos svetainės puslapyje, norint akcentuoti akcijas ir naujus produktus.
- Turinio bloko modulį galima naudoti išsamios produktų informacijos puslapyje, norint parodyti produktų informaciją.
- Kelis turinio bloko modulius galima įdėti į karuselės modulį, norint akcentuoti kelis produktus ar akcijas.

## <a name="content-block-modules-and-themes"></a>Turinio bloko moduliai ir temos

Turinio bloko moduliai gali palaikyti įvairius maketus ir stilius, pagrįstus tema. Pavyzdžiui, „Fabrikam“ tema palaiko tris turinio bloko modulio maketo variantus: pagrindinis, funkcija ir plytelė. Pagrindinis maketas rodo vaizdą fone su teksto perdanga. Funkcijos maketas vaizdą ir tekstą vienas šalia kito. Plytelės maketas leidžia daug turinio blokų plytelės formatu.

Be to, tema gali turėti skirtingų ypatybių kiekvienam maketui. Temo kūrėjas gali sukurti daugiau maketų, kuriuose yra daugiau stilių, naudodamas turinio bloko modulį.

Toliau pateiktame paveiksle parodytas turinio bloko modulis su pagrindiniu maketu.

![Pagrindinės reklaminės juostos modulio pavyzdys](./media/Hero.PNG)

Toliau pateiktame paveiksle parodytas turinio bloko modulis su funkcijos maketu.

![Reklamuojamų produktų modulių pavyzdžiai](./media/Feature.PNG)

## <a name="content-block-module-properties"></a>Turinio bloko modulių ypatybės

| Ypatybės pavadinimas  | Reikšmės | Aprašymas |
|----------------|--------|-------------|
| Vaizdas          | Vaizdo failas | Parodyti produktą ar akciją galima naudojant vaizdą. Vaizdą galima nusiųsti į vaizdų galeriją arba galima naudoti esamą vaizdą. |
| Antraštė        | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Kiekviename pagrindinės reklaminės juostos modulyje gali būti antraštė. Numatyta, kad naudojama antraštės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Pastraipa      | Pastraipos tekstas | Pagrindinės reklaminės juostos moduliai palaiko pastraipos tekstą raiškiojo teksto formatu. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas bei hipersaitai. Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema. |
| Saitas           | Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke** | Pagrindinės reklaminės juostos moduliai palaiko vieną ar kelis raginimo imtis veiksmų saitus. Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma. ARIA žymos turi būti aprašomosios, kad atitiktų pritaikymo neįgaliesiems reikalavimus. Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke. |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a>Turinio bloko modulio ypatybės „Fabrikam“ temoje 

| Ypatybės pavadinimas  | Reikšmės | Aprašymas |
|----------------|--------|-------------|
| Teksto talpinimas | **Kairė**, **Dešinė**, **Centras** | Ši ypatybė nustato teksto ant vaizdo padėtį. Ji taikoma tik pagrindiniame makete. |
| Teksto tema     | **Šviesi** arba **Tamsi** | Pagal fono vaizdą galima nustatyti teksto spalvų schemą. Pavyzdžiui, jei vaizdo fonas yra tamsus, galima taikyti šviesią temą, kad tekstas būtų matomesnis ir būtų pasiektas spalvų kontrasto santykis pritaikymo neįgaliesiems tikslais. Ji taikoma tik pagrindiniame makete.|
| Vaizdų išdėstymas       | **Kairė**, **Dešinė** | Ši ypatybė nurodo, ar vaizdas turi būti teksto kairėje ar dešinėje. Ji taikoma tik funkcijos makete.  |

## <a name="add-a-content-block-module-to-a-new-page"></a>Turinio bloko modulio įtraukimas į naują puslapį

Norėdami į naują puslapį įtraukti pagrindinės reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir sukurkite puslapio šabloną pavadinimu **Turinio bloko šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite pagrindinės reklaminės juostos modulį.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Naudodami ką tik sukurtą pagrindinį šabloną, sukurkite puslapį, pavadintą **Turinio bloko puslapis**.
1. Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.
1. Dialogo lango **Modulio įtraukimas** dalyje **Pasirinkti modulius** pasirinkite pagrindinės reklaminės juostos modulį ir **Gerai**.
1. Kairėje esančiame struktūros medyje pasirinkite turinio bloko modulį.
1. Dešinėje esančioje ypatybių srityje pasirinkite **Įtraukti vaizdą**. Tada pasirinkite esamą vaizdą arba nusiųskite naują.
1. Pasirinkite **Antraštė**.
1. Dialogo lange **Antraštė** įtraukite antraštės tekstą, pasirinkite antraštės lygį ir **Gerai**.
1. Dalyje **Raiškusis tekstas** įtraukite reikiamą tekstą.
1. Pasirinkite **Pridėti saitą**.
1. Dialogo lange **Saitas** įtraukite saito tekstą, saito URL ir saito ARIA žymą, tada pasirinkite **Gerai**.
1. Pasirinkite maketą **Pagrindinis**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Reklaminės juostos modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Teksto bloko modulis](add-content-rich-block.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]