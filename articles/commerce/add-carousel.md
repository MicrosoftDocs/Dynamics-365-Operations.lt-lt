---
title: Karuselės modulis
description: Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785242"
---
# <a name="carousel-module"></a>Karuselės modulis

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Naudojant karuselės modulį kelios reklaminės prekės įdedamos į karuselę, kurią klientai gali naršyti. Tai yra specialus konteinerio modulis, kuriame yra kitų modulių. Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.

Į karuselės modulį galite įtraukti pagrindinės reklaminės juostos ir ypatybių modulius. Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Karuselės modulių pavyzdžiai el. prekyboje

- Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.
- Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.
- Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.

## <a name="carousel-module-properties"></a>Karuselės modulio ypatybės

| Ypatybės pavadinimas             | Vertė                                | Aprašymas |
|---------------------------|--------------------------------------|-------------|
| Automatinis paleidimas                  | **Teisinga** arba **Klaidinga**                | Jei reikšmė nustatoma kaip **Teisinga**, nuo vienos prekės prie kitos karuselėje pereinama automatiškai. Jei reikšmė nustatoma kaip **Klaidinga**, prie kitos prekės nepereinama, nebent klientas nuo vienos prekės prie kitos pereina klaviatūra ar pele. |
| Skaidrių perėjimo intervalas | Reikšmė sekundėmis                   | Perėjimo nuo vienos prekės prie kitos intervalas. |
| Perėjimo animacija      | **Slinkimas** arba **Išnykimas**                | Perėjimo efektas. |
| Plotis                     | **Priderinti prie konteinerio** arba **Užpildyti ekraną** | Jei reikšmė nustatoma kaip **Priderinti prie konteinerio**, karuselės prekių plotį riboja karuselė. Jei reikšmė nustatoma kaip **Užpildyti ekraną**, prekių pločio karuselė neriboja ir jas galima vaizduoti viso ekrano režimu. Keisdami reikšmę, galite pasiekti norimą išdėstymą. |

## <a name="add-a-carousel-module-to-a-page"></a>Karuselės modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti karuselės modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Sukurkite puslapio šabloną, pavadintą **karuselės šablonas**.
1. Numatytojo puslapio vietoje **Pagrindinis** įtraukite karuselės modulį.
1. Į karuselės modulį įtraukite pagrindinės reklaminės juostos modulį.
1. Į karuselės modulį įtraukite ypatybių modulį.
1. Šabloną įrašykite ir atrakinkite bei publikuokite. 
1. Naudodami ką tik sukurtą karuselės šabloną, sukurkite puslapį, pavadintą **karuselės puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite karuselės modulį.
1. Karuselės modulio ypatybę **Plotis** nustatykite kaip **Užpildyti ekraną**. 
1. Ypatybę **Perėjimo animacija** nustatykite kaip **Slinkimas**.
1. Į karuselės modulį įtraukite pagrindinės reklaminės juostos modulį.
1. Pagrindinės reklaminės juostos modulyje įtraukite vaizdą ir antraštę, tada pasirinkite **Įrašyti**.
1. Į karuselės modulį įtraukite ypatybių modulį.
1. Ypatybių modulyje įtraukite vaizdą, antraštę ir teksto pastraipą.
1. Puslapį įrašykite ir peržiūrėkite. Puslapyje turėtų būti rodoma karuselė su dviem moduliais (pagrindinės reklaminės juostos moduliu ir ypatybių moduliu). Norėdami pasiekti norimą rezultatą, galite keisti papildomas karuselės, pagrindinės reklaminės juostos ir ypatybių modulių ypatybes.
1. Puslapį įrašykite ir atrakinkite bei publikuokite.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Įspėjimo modulis](add-alert.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Turinio išdėstymo modulis](add-content-placement-modules.md)

[Ypatybių modulis](add-feature-module.md)

[Pagrindinės reklaminės juostos modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)
