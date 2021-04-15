---
title: Poraštės modulis
description: Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d6e7b0ad4fe0723575a0ec55a9b02d110568db58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797238"
---
# <a name="footer-module"></a>Poraštės modulis  

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi poraštės moduliai ir tai, kaip juos kurti programoje „Microsoft Dynamics 365 Commerce“.

Poraštės modulis yra specialus konteineris, kuriame laikomi moduliai, rodomi puslapio poraštėje. Pavyzdžiui, jame gali būti saitų su įvairiais svetainės puslapiais, pvz., puslapiais **Susisiekite su mumis** ir **Parduotuvės strategijos**.

Toliau pateiktame paveikslėlyje parodytas svetainės puslapyje esančio poraštės modulio pavyzdys.

![Poraštės modulio pavyzdys](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Poraštės modulių ypatybės 

Kaip ir dauguma konteinerių, poraštės modulis palaiko antraštės ir pločio ypatybes. Jis taip pat palaiko kelių poraštės kategorijos modulių įtraukimo galimybę. Kiekvienas įtrauktas poraštės kategorijos modulis poraštės modulyje vaizduojamas kaip stulpelis.

## <a name="modules-available-in-a-footer-module"></a>Poraštės modulyje esantys moduliai

**Poraštės elementai** – poraštės elementų modulyje gali būti antraštė, vaizdas ir saitas. Antraštė gali būti naudojama atskirai arba kartu su vaizdu ir saitu. Kiekvieną poraštės saitą galima sukonfigūruoti taip, kad jame būtų tik tekstas (pavyzdžiui, saitai „Susisiekite su mumis“ ir „Privatumas“), arba kad jame būtų ir tekstas, ir vaizdas (pavyzdžiui, socialinės medijos saitai).

**Grįžti į viršų** – grįžimo į viršų modulis suteikia saitą greitai pereiti į puslapio viršų. Būtina paskirties vieta. Numatytoji paskirties vietos reikšmė yra \#, kuri vartotoją perkelia į puslapio viršų.

## <a name="create-a-footer-module"></a>Kurti poraštės modulį

1. Eikite į **Fragmentai** ir tuomet pasirinkite **Naujas** tam, kad sukurtumėte naują fragmentą.
1. Dialogo lange **Naujas fragmentas** pasirinkite **Konteinerio** modulį, įveskite fragmento pavadinimą ir pasirinkite **Gerai**.
1. Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Poraštės kategorija** ir **Gerai**.
1. Vietoje **Poraštės kategorija** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Poraštės elementas** ir **Gerai**.
1. Pasirinkite vietą **Poraštės elementas**, tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite antraštę, saitą ir saito tekstą bei vaizdą.
1. Norėdami įtraukti daugiau poraštės elementų, kiekvienam elementui pakartokite 5–7 veiksmus.
1. Norėdami į poraštę įtraukti saitą „grįžti į viršų“, pasirinkite vietoje **Poraštės kategorija** esantį daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Atgal į pradžią** ir **Gerai**.
1. Pasirinkite vietą **Atgal į pradžią**, tada dešinėje esančioje ypatybių srityje pagal poreikį sukonfigūruokite tekstą ir kitas modulio ypatybes.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.

1. Modulio **Numatytasis puslapis** vietoje **Poraštė** įtraukite jūsų sukurtą poraštės fragmentą.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Fragmentą įtraukdami į puslapio šablonus padedate užtikrinti, kad poraštė bus vaizduojama kiekviename puslapyje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]