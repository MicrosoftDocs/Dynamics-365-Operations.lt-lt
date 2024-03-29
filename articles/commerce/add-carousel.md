---
title: Karuselės modulis
description: Šiame straipsnyje aprašomi duomenų bazės moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 8bf9f7294dfbb4e16814dbdfb27bf646fcb5f4b1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275833"
---
# <a name="carousel-module"></a>Karuselės modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi duomenų bazės moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Naudojant karuselės modulį kelios reklaminės prekės (įskaitant išraiškingus veiksmus) įdedamos į rotacinę karuselės reklaminę juostą, kurią klientai gali naršyti. Pavyzdžiui, karuselės modulį naudodamas pagrindiniame puslapyje pardavėjas gali parodyti kelis naujus produktus ar akcijas.

Į karuselės modulį galite įtraukti turinio bloko modulius. Tada karuselės modulio ypatybėmis apibrėžiama, kaip šie moduliai vaizduojami.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Karuselės modulių pavyzdžiai el. prekyboje

- Karuselę su keliais reklaminiais moduliais galima naudoti pagrindiniame puslapyje.
- Karuselę su keliais reklaminiais moduliais galima naudoti produkto išsamios informacijos puslapyje.
- Karuselę galima naudoti bet kuriame rinkodaros puslapyje norint reklamuoti kelias akcijas ar produktus.

Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio karuselės modulio pavyzdys. Šiame karuselės modulyje yra keli turinio blokų elementai.

![Karuselės modulio pavyzdys.](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Karuselės modulio ypatybės

| Ypatybės pavadinimas             | Reikšmė                 | Aprašas |
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
