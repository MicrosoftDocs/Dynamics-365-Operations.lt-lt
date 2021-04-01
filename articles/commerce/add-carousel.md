---
title: Karuselės modulis
description: Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 5333ecd7a1fe4f60684fa5f5bb3ac9f98efde6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206516"
---
# <a name="carousel-module"></a>Karuselės modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi karuselės moduliai ir tai, kaip jų įtraukti į „Microsoft Dynamics 365 Commerce“ svetainių puslapius.

Naudojant karuselės modulį kelios reklaminės prekės (įskaitant išraiškingus veiksmus) įdedamos į rotacinę karuselės reklaminę juostą, kurią klientai gali naršyti. Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.

Į karuselės modulį galite įtraukti turinio bloko modulius. Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Karuselės modulių pavyzdžiai el. prekyboje

- Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.
- Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.
- Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.

Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio karuselės modulio pavyzdys. Šiame karuselės modulyje yra keli turinio blokų elementai.

![Karuselės modulio pavyzdys](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Karuselės modulio ypatybės

| Ypatybės pavadinimas             | Vertė                 | aprašymas |
|---------------------------|-----------------------|-------------|
| Automatinis paleidimas                  | **Teisinga** arba **Klaidinga** | Jei reikšmė nustatoma kaip **Teisinga**, nuo vienos prekės prie kitos karuselėje pereinama automatiškai. Jei reikšmė nustatoma kaip **Klaidinga**, prie kitos prekės nepereinama, nebent klientas nuo vienos prekės prie kitos pereina klaviatūra ar pele. |
| Skaidrių perėjimo intervalas | Reikšmė sekundėmis    | Perėjimo nuo vienos prekės prie kitos intervalas. |
| Perėjimo tipas           | **Slinkimas** arba **Išnykimas** | Perėjimo poveikis tarp prekių. |
| Slėpti karuselės sukimo priemonę     | **Teisinga** arba **Klaidinga** | Jei reikšmė nustatyta kaip **Teisinga**, karuselės pelekas ir sekos indikatorius yra paslėpti. |
| Karuselės atmetimo leidimas    | **Teisinga** arba **Klaidinga** | Jei reikšmė nustatyta kaip **Teisinga**, klientai gali atmesti karuselę. |

## <a name="add-a-carousel-module-to-a-page"></a>Karuselės modulio įtraukimas į puslapį

Norėdami į naują puslapį įtraukti karuselės modulį ir nustatyti reikiamas ypatybes, atlikite tolesnius veiksmus.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lango **Naujas šablonas** dalyje **Šablono pavadinimas** įveskite **Karuselės šablonas** ir pasirinkite **Gerai**.
1. Srityje **Pagrindinė dalis** įtraukite modulį **Numatytasis modulis**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.  
1. Naudodami ką tik sukurtą karuselės šabloną, sukurkite puslapį, pavadintą **Karuselės puslapis**.
1. Naujo puslapio vietoje **Pagrindinis** įtraukite konteinerio modulį. 
1. Dešiniojoje srityje nustatykite **Plotis** vertę, kad galėtumėte **Užpildyti ekraną**.
1. Dalyje **Puslapio kontūras** įtraukite karuselės modulį į konteinerio modulį.
1. Į karuselės modulį įtraukite turinio bloko modulį. Nustatykite turinio bloko modulio ypatybes pateikdami **Antraštė**, **Saitas**, **Išdėstymas** ir kitas ypatybes.
1. Įtraukite ir konfigūruokite kitą turinio bloko modulį.
1. Pagal pageidavimą, nustatykite kitas karuselės modulio ypatybes.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Puslapyje turėtų būti rodoma karuselė su dviem moduliais (pagrindinės reklaminės juostos moduliu ir ypatybių moduliu). Norėdami pasiekti norimą rezultatą, galite keisti papildomas karuselės, pagrindinės reklaminės juostos ir ypatybių modulių ypatybes.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Reklaminės juostos modulis](add-alert.md)

[Teksto bloko modulis](add-content-rich-block.md)

[Turinio bloko modulis](add-hero-module.md)

[Vaizdo įrašų leistuvo modulis](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]