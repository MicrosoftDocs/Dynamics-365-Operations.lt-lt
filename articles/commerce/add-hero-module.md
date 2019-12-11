---
title: Pagrindinės reklaminės juostos modulis
description: Šioje temoje aprašomi pagrindinės reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785400"
---
# <a name="hero-module"></a>Pagrindinės reklaminės juostos modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi pagrindinės reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Pagrindinės reklaminės juostos modulis naudojamas produktams ar akcijoms reklamuoti derinant vaizdus ir tekstą. Pavyzdžiui, pardavėjas pagrindinės reklaminės juostos modulį gali įtraukti į pagrindinį el. prekybos svetainės puslapį, kad reklamuotų naują produktą ir pritrauktų klientų dėmesį.

Pagrindinės reklaminės juostos modulis grindžiamas duomenimis iš turinio valdymo sistemos (TVS). Tai yra atskiras modulis, nepriklausantis nuo jokių kitų puslapio modulių. Pagrindinės reklaminės juostos modulį galima įdėti bet kuriame svetainės puslapyje, kuriame pardavėjas nori kažką parduoti ar reklamuoti, (pavyzdžiui, produktus, išpardavimus ar ypatybes).

## <a name="examples-of-hero-module-in-e-commerce"></a>Pagrindinės reklaminės juostos modulio pavyzdžiai el. prekyboje

- Pagrindinės reklaminės juostos modulį galima naudoti pagrindiniame el. prekybos svetainės puslapyje, norint akcentuoti akcijas ir naujus produktus.
- Pagrindinės reklaminės juostos modulį galima naudoti išsamios produktų informacijos puslapyje, norint parodyti produktų informaciją.
- Kelis pagrindinės reklaminės juostos modulius galima įdėti į karuselės modulį, norint akcentuoti kelis produktus ar akcijas.

## <a name="hero-module-properties"></a>Pagrindinės reklaminės juostos modulių ypatybės

| Ypatybės pavadinimas  | Reikšmės | Aprašymas |
|----------------|--------|-------------|
| Vaizdas          | Vaizdo failas | Parodyti produktą ar akciją galima naudojant vaizdą. Vaizdą galima nusiųsti į vaizdų galeriją arba galima naudoti esamą vaizdą. |
| Antraštė        | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Kiekviename pagrindinės reklaminės juostos modulyje gali būti antraštė. Numatyta, kad naudojama antrašės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Pastraipa      | Pastraipos tekstas | Pagrindinės reklaminės juostos moduliai palaiko pastraipos tekstą raiškiojo teksto formatu. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas bei hipersaitai. Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema. |
| Saitas           | Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke** | Pagrindinės reklaminės juostos moduliai palaiko vieną ar kelis raginimo imtis veiksmų saitus. Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma. ARIA žymos turi būti aprašomosios, kad atitiktų pritaikymo neįgaliesiems reikalavimus. Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke. |
| Teksto talpinimas | **Viršuje kairėje**, **Viršuje dešinėje**, **Viršuje centre**, **Apačioje kairėje**, **Apačioje dešinėje**, **Apačioje centre**, **Centre kairėje**, **Centre dešinėje** arba **Pačiame centre** | Ši ypatybė nustato vaizdo padėtį teksto atžvilgiu. Pavyzdžiui, jei pasirenkama **Dešinėje**, vaizdas rodomas teksto dešinėje. |
| Teksto tema     | **Šviesi** arba **Tamsi** | Pagal fono vaizdą galima nustatyti teksto spalvų schemą. Pavyzdžiui, jei vaizdo fonas yra tamsus, galima taikyti šviesią temą, kad tekstas būtų matomesnis ir būtų pasiektas spalvų kontrasto santykis pritaikymo neįgaliesiems tikslais. |
| Perėjimas       | **Teisinga** arba **Klaidinga** | Siekiant pasiekti spalvų kontrasto santykius pritaikymo neįgaliesiems tikslais, vaizdui galima taikyti perėjimą. |

## <a name="add-a-hero-module-to-a-new-page"></a>Pagrindinės reklaminės juostos modulio įtraukimas į naują puslapį

Norėdami į naują puslapį įtraukti pagrindinės reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Nueikite į **Šablonai** ir sukurkite puslapio šabloną pavadinimu **pagrindinės reklaminės juostos šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite pagrindinės reklaminės juostos modulį.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Naudodami ką tik sukurtą pagrindinės reklaminės juostos šabloną, sukurkite puslapį, pavadintą **pagrindinės reklaminės juostos puslapis**.
1. Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.
1. Dialogo lango **Modulio įtraukimas** dalyje **Pasirinkti modulius** pasirinkite pagrindinės reklaminės juostos modulį ir **Gerai**.
1. Kairėje esančiame struktūros medyje pasirinkite pagrindinės reklaminės juostos modulį.
1. Dešinėje esančioje ypatybių srityje pasirinkite **Įtraukti vaizdą**. Tada pasirinkite esamą vaizdą arba nusiųskite naują.
1. Pasirinkite **Antraštė**.
1. Dialogo lange **Antraštė** įtraukite antraštės tekstą, pasirinkite antraštės lygį ir **Gerai**.
1. Dalyje **Raiškusis tekstas** įtraukite reikiamą tekstą.
1. Pasirinkite **Įtraukti veiksmo saitą**.
1. Dialogo lange **Veiksmo saitas** įtraukite saito tekstą, saito URL ir saito ARIA žymą, tada pasirinkite **Gerai**.
1. Įrašykite puslapį ir peržiūrėkite keitimus.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Įspėjimo modulis](add-alert.md)

[Karuselės modulis](add-carousel.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Turinio išdėstymo modulis](add-content-placement-modules.md)

[Funkcijos modulis](add-feature-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)
