---
title: Įspėjimo modulis
description: Šioje temoje aprašomi įspėjimo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785357"
---
# <a name="alert-module"></a>Įspėjimo modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi įspėjimo moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Naudojant įspėjimo modulį puslapyje rodomi įdėtieji informaciniai pranešimai. Įspėjimo moduliai palaiko tekstinio pranešimo ir saito galimybę. Juos naudojant, visuose el. prekybos svetainės puslapiuose galima rodyti akcijas. 

Įspėjimo moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.

## <a name="examples-of-alert-modules-in-e-commerce"></a>Įspėjimo modulių pavyzdžiai el. prekyboje

Įspėjimo modulius naudojant svetainės antraštėje, visoje svetainėje galima nurodyti akcijas ar pranešimus. Štai keletas pavyzdžių:

„Metinis išpardavimas baigiasi už 10 dienų“

„Daug sutaupykite pasinaudodami priešmokyklinio išpardavimo pasiūlymais. Apsipirkite jau dabar.“

## <a name="alert-module-properties"></a>Įspėjimo modulių ypatybės

| Ypatybės pavadinimas  | Vertė                              | Aprašymas |
|----------------|------------------------------------|-------------|
| Tekstas           | Tekstas                               | Įspėjimo modulyje rodomas tekstinis pranešimas. |
| Teksto išlygiavimas | **Kairėje**, **Dešinėje** arba **Centre** | Reikšmė, apibrėžianti, kaip tekstas lygiuojamas įspėjimo modulyje. |
| Atmesti įspėjimą  | **Teisinga** arba **Klaidinga**              | Jei reikšmė nustatyta kaip **Teisinga**, klientas gali atmesti įspėjimą. |
| Saitas           | URL                                | Nebūtino saito URL. |

## <a name="add-an-alert-module-to-a-page"></a>Įspėjimo modulio įtraukimas į puslapį 

Norėdami į puslapį įtraukti įspėjimo modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite puslapio šabloną, pavadintą **įspėjimo šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite įspėjimo modulį.
1. Šabloną įrašykite ir atrakinkite bei publikuokite. 
1. Naudodami ką tik sukurtą įspėjimo šabloną, sukurkite puslapį, pavadintą **įspėjimo puslapis**. 
1. Naujo puslapio vietoje **Pagrindinis** įtraukite įspėjimo modulį.
1. Įspėjimo modulio parametruose įveskite įspėjimo tekstą. Jei norite įspėjimo modulį tinkinti daugiau, galite redaguoti kitas ypatybes.
1. Puslapį įrašykite ir peržiūrėkite. Puslapio viršuje turėtumėte matyti įspėjimą su jūsų įtrauktu tekstu.
1. Puslapį įrašykite ir atrakinkite bei publikuokite. 

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Karuselės modulis](add-carousel.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Turinio išdėstymo modulis](add-content-placement-modules.md)

[Ypatybių modulis](add-feature-module.md)

[Pagrindinės reklaminės juostos modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)
