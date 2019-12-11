---
title: Ypatybių modulis
description: Šioje temoje aprašomi ypatybių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785290"
---
# <a name="feature-module"></a>Ypatybių modulis 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi ypatybių moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Ypatybių modulis naudojamas produktams ar akcijoms reklamuoti derinant vaizdus ir tekstą. Pavyzdžiui, pardavėjas ypatybių modulį gali įtraukti į produkto išsamios informacijos puslapį, kad galėtų akcentuoti produkto ypatybes.

Ypatybių modulis grindžiamas duomenimis iš turinio valdymo sistemos (TVS). Tai yra atskiras modulis, nepriklausantis nuo jokių kitų puslapio modulių. Ypatybių modulį galima įdėti bet kuriame svetainės puslapyje, kuriame pardavėjas nori kažką parduoti ar reklamuoti, (pavyzdžiui, produktus, išpardavimus ar ypatybes).

## <a name="examples-of-feature-modules-in-e-commerce"></a>Ypatybių modulių pavyzdžiai el. prekyboje

Ypatybių modulį galima naudoti tolesniuose puslapiuose.

- Produktų išsamios informacijos puslapyje, norint parodyti produktų ypatybes
- Pagrindiniame puslapyje, norint reklamuoti produktus
- Kategorijos puslapyje, norint akcentuoti produktų kategoriją

## <a name="feature-module-properties"></a>Ypatybių modulio ypatybės

| Ypatybės pavadinimas     | Reikšmės | Aprašymas |
|-------------------|--------|-------------|
| Vaizdas             | Vaizdo failas | Parduoti produktą ar parodyti akciją galima naudojant vaizdą. Vaizdą galima nusiųsti į vaizdų galeriją arba galima naudoti esamą vaizdą. |
| Antraštė           | Antraštės tekstas ir antraštės žymė (**H1**, **H2**, **H3**, **H4**, **H5** arba **H6**) | Kiekviename funkcijų modulyje gali būti antraštė. Numatyta, kad naudojama antrašės žymė **H2**. Tačiau žymę galima pakeisti, kad ji atitiktų pritaikymo neįgaliesiems reikalavimus. |
| Pastraipa         | Pastraipos tekstas | Ypatybių moduliai palaiko pastraipos tekstą raiškiojo teksto formatu. Palaikomos kelios pagrindinės raiškiojo teksto galimybės, pvz., paryškintasis, pabrauktasis ir pasvirasis tekstas bei hipersaitai. Kai kurias iš šių galimybių gali perrašyti moduliui pritaikoma puslapio tema. |
| Saitas              | Saito tekstas, saito URL, „Accessible Rich Internet Applications“ (ARIA) žyma ir **Saitą atidaryti naujame skirtuke** | Ypatybių moduliai palaiko vieną ar kelis raginimo imtis veiksmų saitus. Jei įtraukiamas saitas, reikalingas saito tekstas, URL ir ARIA žyma. ARIA žymos turi būti aprašomosios, kad atitiktų pritaikymo neįgaliesiems reikalavimus. Saitus galima konfigūruoti taip, kad jie būtų atidaromi naujame skirtuke. |
| Vaizdų išdėstymas   | **Dešinėje**, **Kairėje**, **Viršuje** arba **Apačioje** | Ši ypatybė nustato vaizdo padėtį teksto atžvilgiu. Pavyzdžiui, jei pasirenkama **Dešinėje**, vaizdas rodomas teksto dešinėje. |
| Vaizdo stulpelio dydis | Reikšmė nuo **1** iki **12** | Ši ypatybė nustato vaizdo dydį teksto atžvilgiu. Dydis išreiškiamas kaip puslapio stulpelių skaičius. Puslapyje yra 12 stulpelių. Numatyta, kad vaizdas ir tekstas yra vienodo dydžio (po šešis stulpelius). Tačiau dydį galima koreguoti pagal poreikį. |

## <a name="add-a-feature-module-to-a-new-page"></a>Ypatybių modulio įtraukimas į naują puslapį 

Norėdami į naują puslapį įtraukti ypatybių modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Nueikite į **Šablonai** ir sukurkite puslapio šabloną pavadinimu **ypatybių šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite ypatybių modulį.
1. Šabloną įrašykite ir atrakinkite bei publikuokite.
1. Naudodami ką tik sukurtą ypatybių šabloną, sukurkite puslapį, pavadintą **ypatybių puslapis**.
1. Numatytojo puslapio vietoje **Pagrindinis** pasirinkite daugtaškio mygtuką (**...**) ir **Įtraukti modulį**.
1. Dialogo lango **Modulio įtraukimas** dalyje **Pasirinkti modulius** pasirinkite ypatybių modulį ir **Gerai**.
1. Kairėje esančiame struktūros medyje pasirinkite ypatybių modulį.
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

[Pagrindinės reklaminės juostos modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)
