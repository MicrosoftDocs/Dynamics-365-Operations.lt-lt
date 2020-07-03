---
title: Reklaminės juostos modulis
description: Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: dae824cdbaaf56f85f125c5f36aaa56171bbd6bc
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411370"
---
# <a name="promo-banner-module"></a>Reklaminės juostos modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi reklaminės juostos moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

## <a name="overview"></a>Peržiūrėti

Reklaminės juostos moduliai naudojami, kad puslapyje būtų rodomi įdėtieji informaciniai pranešimai. Juos naudojant, visuose el. prekybos svetainės puslapiuose galima rodyti akcijas. 

Reklaminės juostos moduliai palaiko tekstinio pranešimo ir saito galimybę. Jei į reklaminės juostos modulį įtraukiami keli pranešimai, ji tampa besisukančia karuselės juosta, todėl vartotojai gali eiti per visus pranešimus. 

Reklaminės juostos moduliai grindžiami turinio valdymo sistemos (TVS) duomenimis ir jų galima įdėti bet kuriame puslapyje.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Reklaminės juostos el. prekyboje naudojimo pavyzdžiai

Reklamines juostas galima naudoti svetainės antraštėje, kad būtų rodomos visos svetainės akcijos ar pranešimai, kaip pateikiama šiuose pavyzdžiuose.

„Metinis išpardavimas baigiasi už 10 dienų“

„Daug sutaupykite pasinaudodami priešmokyklinio išpardavimo pasiūlymais. Apsipirkite jau dabar.“

„Apsipirkite per Padėkos dienos IŠPARDAVIMĄ!“ 

Toliau pateiktame vaizde parodytas reklaminės juostos pavyzdys.

![Reklaminės juostos modulio pavyzdys](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Reklaminės juostos modulio ypatybės

| Ypatybės pavadinimas             | Vertė                              | aprašymas |
|---------------------------|------------------------------------|-------------|
| Juostos pranešimai           | Tekstas ir saitai                     | Teksto ir saitų masyvas. |
| Automatinis paleidimas                  | **Teisinga** arba **Klaidinga**              | Reikšmė, nurodanti, ar pranešimai automatiškai atlieka visą ciklą, jei sukonfigūruoti keli pranešimai. |
| Skaidrių perėjimo intervalas | Milisekundžių skaičius (ms)      | Intervalas, naudojamas norint peržiūrėti pranešimus. |
| Leisti atmesti             | **Teisinga** arba **Klaidinga**              | Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti įspėjimą. |
| Karuselės peleko rodymas     | **Teisinga** arba **Klaidinga**              | Reikšmė, nurodanti, ar reikia rodyti karuselės pelekus, kad klientai galėtų rankiniu būdu pereiti per kelis reklaminės juostos elementus. |
| Teksto išlygiavimas            | **Kairėje**, **Dešinėje** arba **Centre** | Teksto lygiuotė reklaminės juostos modulyje. |
| Saitas                      | A URL                              | Nebūtino saito URL. |

## <a name="add-a-promo-banner-module-to-a-page"></a>Reklaminės juostos modulio įtraukimas į puslapį 

Norėdami į puslapį įtraukti reklaminės juostos modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Reklaminės juostos šablonas** ir pasirinkite **Gerai**.
1. Dalyje **Puslapio kontūras** įtraukite **Numatytasis puslapis** modulį į atkarpą **Pagrindinis tekstas**. 
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį. 
1. Naudodami ką tik sukurtą šabloną, sukurkite puslapį, pavadintą **Reklaminės juostos puslapis**. 
1. Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį. 
1. Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti konteineris**.
1. Dalyje **Puslapio kontūras** įtraukite reklaminės juostos modulį į konteinerio modulį.
1. Reklaminės juostos parametruose įtraukite vieną arba kelis reklaminės juostos pranešimus. Kiekvienas pranešimas gali turėti tekstą kartu su saitu. Jei norite modulį tinkinti daugiau, galite redaguoti kitas ypatybes.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Puslapio viršuje turėtumėte matyti įspėjimą su jūsų įtrauktu tekstu.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

> [!NOTE]
> Reklaminė juosta paprastai naudojama puslapio antraštės atkarpoje arba paantraštės atkarpoje.


## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Karuselės modulis](add-carousel.md)

[Teksto bloko modulis](add-content-rich-block.md)

[Turinio bloko modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)
