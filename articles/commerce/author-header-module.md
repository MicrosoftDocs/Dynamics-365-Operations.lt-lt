---
title: Antraštės modulis
description: Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411223"
---
# <a name="header-module"></a>Antraštės modulis

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi antraštės moduliai ir tai, kaip juos kurti puslapio antraštėse „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūrėti

„Dynamics 365 Commerce“ puslapio antraštę sudaro keli moduliai, pavyzdžiui, antraštė, naršymo meniu, ieška, reklaminė juosta, sutikimo naudoti slapukus moduliai. 

Antraštės modulyje yra svetainės logotipas, saitai į naršymo hierarchiją, saitai į kitus svetainės puslapius, krepšelio simbolis, pageidavimų sąrašo simbolis, prisijungimo parinktys ir ieškos juosta. Antraštės modulis automatiškai optimizuojamas įrenginiui, kuriame peržiūrima svetainė (kitais žodžiais, stacionariam įrenginiui arba mobiliajam įrenginiui). Pavyzdžiui, mobiliajame įrenginyje naršymo juosta sutraukiama į mygtuką **Meniu** (kuris kartais vadinamas *mėsainio stiliaus meniu*).

Toliau pateiktame paveikslėlyje parodytas pagrindiniame puslapyje esančio antraštės modulio pavyzdys.

![Antraštės modulio pavyzdys](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Antraštės modulio ypatybės

Antraštės modulis palaiko ypatybes **Logotipo vaizdas**, **Logotipo saitas** ir **Mano paskyros saitai**. 

Ypatybės **Logotipo vaizdas** ir **Logotipo saitas** naudojamos logotipui puslapyje apibrėžti. Daugiau informacijos žr. [Logotipo pridėjimas](add-logo.md). 

Ypatybę **Mano paskyros saitai** galima naudoti norint apibrėžti paskyros puslapius, kurių sparčiuosius saitus svetainės savininkas nori rodyti antraštėje.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduliai, esantys antraštės modulyje

Antraštės modulyje galima naudoti tolesnius modulius.

- **Naršymo meniu** – naršymo meniu vaizduojama kanalo naršymo hierarchija ir kiti statiniai naršymo saitai. Kanalo naršymo hierarchiją galima konfigūruoti programoje „Dynamics 365 Commerce“. Naršymo meniu turi ypatybę **Naršymo šaltinis**, kuri naudojama norint apibrėžti mažmeninės prekybos serverio naršymo meniu elementus ir statinio meniu elementus kaip šaltinį. Jei statinio meniu elementai apibrėžiami kaip šaltinis, svetainėje gali būti pateikiami susiję saitai į kitus puslapius. Sukonfigūruoti elementai tada rodomi kaip antraštės naršymo elementai. 

- **Ieška** – ieškos modulyje vartotojai gali įvesti ieškos terminus, kad galėtų ieškoti produktų. Numatytojo ieškos puslapio URL ir ieškos užklausos parametrai turi būti pateikti **Svetainės parametrai \> Plėtiniai**. Ieškos modulyje yra ypatybių, kurios leidžia nerodyti ieškos mygtuko arba pažymėti, kaip pageidaujate. Ieškos modulis taip pat palaiko automatinio pasiūlymo parinktis, pavyzdžiui, produktų, raktažodžių ar kategorijų ieškos rezultatus.

- **Krepšelio piktograma** – krepšelio piktogramos modulis vaizduoja krepšelio piktogramą, rodančią krepšelyje esančių prekių skaičių bet kuriuo metu. Daugiau informacijos žr. [Krepšelio piktogramos modulis](cart-icon-module.md).

## <a name="create-a-header-module-for-a-page"></a>Puslapio antraštės modulio kūrimas

Norėdami sukurti antraštės modulį, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Puslapio fragmentai** ir pasirinkite **Naujas**, kad sukurtumėte naują fragmentą.
1. Dialogo lange **Naujas puslapio fragmentas** pasirinkite modulį **Konteineris**, įveskite puslapio fragmento pavadinimą ir pasirinkite **Gerai**.
1. Pasirinkite lizdą **Numatytasis konteineris**, tada dešinėje esančioje ypatybių srityje nustatykite ypatybės **Plotis** vertę **Užpildyti konteinerį**.
1. Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulius **Reklaminė juosta** ir **Sutikimas dėl slapukų**, tada pasirinkite **Gerai**.
1. Vietoje **Numatytasis konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Pasirinkite vietą **Konteineris**, tada dešinėje esančioje ypatybių srityje nustatykite ypatybės **Plotis** vertę **Užpildyti konteinerį**.
1. Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Antraštė**, tada pasirinkite **Gerai**.
1. Antraštės modulio vietoje **Naršymo meniu** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo meniu** ir **Gerai**.
1. Naršymo meniu modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.
1. Antraštės modulio vietoje **Ieška** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Paieška**, tada pasirinkite **Gerai**.
1. Ieškos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes.
1. Antraštės modulio vietoje **Krepšelio piktograma** pasirinkite daugtaškį (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Krepšelio piktograma**, tada pasirinkite **Gerai**.
1. Krepšelio piktogramos modulio ypatybių srityje pagal poreikį sukonfigūruokite ypatybes. Jei norite, kad krepšelio piktogramoje būtų rodoma krepšelio santrauka (taip pat žinoma kaip mini krepšelis), kai vartotojai užveda žymeklį, pasirinkite **Rodyti mini krepšelį**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Norėdami padėti užtikrinti, kad antraštė būtų rodoma kiekviename puslapyje, kiekviename sukurtame svetainės puslapio šablone atlikite tolesnius veiksmus.

1. Modulio **Numatytasis puslapis** vietoje **Antraštė** įtraukite jūsų sukurtą poraštės fragmentą.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Krepšelio modulis](add-cart-module.md)

[Krepšelio piktogramos modulis](cart-icon-module.md)

[Pirkimo užbaigimo modulis](add-checkout-module.md)

[Užsakymo patvirtinimo modulis](order-confirmation-module.md)

[Antraštės modulis](author-header-module.md)

[Poraštės modulis](author-footer-module.md)
