---
title: Medijos galerijos modulis
description: Šis skyrius aprašo medijos galerijos modulius ir tia, kaip įtraukti juos į vietos puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 647387bafe8866cb1bee8c57675629af796f33e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414443"
---
# <a name="media-gallery-module"></a>Medijos galerijos modulis

[!include [banner](includes/banner.md)]

Šis skyrius aprašo medijos galerijos modulius ir tia, kaip įtraukti juos į vietos puslapius „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Peržiūra

Medijos galerijos moduliai rodo vieną ar keletą paveikslėlių galerijos peržiūroje. Medijos galerijos moduliai palaiko miniatūros vaizdus, kurie gali būti tvarkomi horizontaliai (kaip toliau esantis paveikslėlis) ar vertikaliai (kaip stulpelis šalia paveikslėlio). Medijos galerijos moduliai taip pat pateikia galimybes, kurios įjungia paveikslėlio priartinimą (pagerintą) ar peržiūrą visame ekrane. Tam, kad būtų sukurtas medijos galerijos režime, paveikslėlis turi būti prieinamas prekybos sveitainės kūrimo įrankyje „Media Library“. Šiuo metu medijos galerijos moduliai palaiko tik paveikslėlius.

Nustatytame režime, medijos galerijos modulis naudoja produkto ID, kuris yra prieinamas iš produkto informacijos puslapio turinio (PDP) tam, kad sukūrtų atitinkamus produkto paveikslėlius. Prekybos štabe medijos failo kelias turi būti nustatytas visiems produktams. Paveikslėliai turi būti po to atnaujinti į vietos kūrimo įrankį „Media Library“ pagal failo kelią, kuris buvo nustatytas produktams prekybos štabe. Šie paveikslėliai apima produktų paveikslėlius ir visus produkto variantus. Dėl išsamesnės informacijos apie tai, kaip įkelti paveikslėlius į svetainės kūrimo įrankį „Media Library“, žr. [Įkelti paveikslėlius](dam-upload-images.md).

Kitu atveju, medijos galerijos modulis gali talpinti visą išdirbtą paveikslėlių rinkinį paveikslėlio galerijos puslapyje, kuriame nėra jokių priklausinių nuo produkto ID ar puslapio konteksto. Šiuo atveju, paveikslėliai turi būti įkelti į svetainės kūrimo įrankį „Media Library“ ir nurodyti svetainės kūrimo įrankyje.

Čia yra keletas panaudojimo pavyzdžių medijos galerijos moduliams:

- Produkto paveikslėlių kūrimas PDP
- Produkto paveikslėlių kūrimas produkto komercijos puslapyje
- Išdirbto paveikslėlių rinkinio rodymas komercijos puslapyje, tokiame kaip galerijos puslapis

Šiame pavyzdiniame tolesniame paveikslėlyje, pirkimo laukelis PDP talpina produkto paveikslėlį naudodamas medijos galerijos modulį.

![Įsigijimo laukelio pavyzdys produkto informacijos puslapyje talpina produkto paveikslėlius naudodamas medijos galerijos modulį](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Medijos galerijos ypatybės

| Ypatybės pavadinimas | Reikšmės | aprašymas |
|---------------|--------|-------------|
| Vaizdo šaltinis | **Puslapio kontekstas** ar **Produkto ID** | Nustatytoji vertė yra **Puslapio kontekstas**. Jei **Puslapio kontekstas** yra pasirinktas, modulis tikisi, kad puslapis pateiks produkto ID informaciją. Jei **Produkto ID** yra pasirinktas, produkto ID paveikslėliui turi būti patvirtintas kaip  **Produkto ID** ypatybės vertė. Ši savybė yra prieinama 10.0.12 prekybos versijoje. |
| Produkto ID | Produkto ID | Ši ypatybė yra taikoma tik, jei **Paveikslėlio šaltinio** ypatybės vertė yra **Produkto ID**. |
| Vaizdo mastelio keitimas | **Pagal liniją** ar **Konteineris** | Ši ypatybė leidžia vartotojui priartini paveikslėlius medijos galerijos modulyje. Paveikslėlis gali būti priartintas pagal liniją ar atskirame konteineryje šalia paveikslėlio. Ši savybė yra prieinama 10.0.12 prekybos versijoje. |
| Priartinimo skalė | Dešimtainis skaičius | Ši ypatybė nurodo skalės faktorių paveikslėlių priartinimui. Pavyzdžiui, jei vertė yra nustatyta į **2,5**, paveikslėlis yra priartinamas 2,5 karto.|
| Visas ekranas | **Teisinga** arba **Klaidinga** | Ši ypatybė nurodo, ar paveikslėliai gali būti peržiūrimi visame ekrane. Visame ekrane paveikslėliai gali taip pat būti toliau padidinami, jei priartinimo savybė yra įjungta. Ši savybė yra prieinama 10.0.13 prekybos versijoje. |
| Vaizdai | Svetainės kūrimo įrankyje „Media Library“ pasirinkti paveikslėliai | Kartu su kūrimu iš produkto, paveikslėliai gali būti išdirbami medijos galerijos moduliui. Šie paveikslėliai bus pridėti prie bet kurio gaminio prieinamų paveikslėlių. Ši savybė yra prieinama 10.0.12 prekybos versijoje. |
| Miniatiūros orientacija | **Vertikaliai** ar **Horizontaliai** | Ši ypatybė nurodo, ar miniatiūros paveikslėliai turi būti rodomi vertikalioje ar horizontalioje juostoje. |

Toliau pateiktas paveikslėlis rodo medijos galerijos modulio pavyzdį, kuriame visas ekranas ir priartinimo parinktys yra prieinamos.

![Medijos galerijos modulio pavyzdys, kuriame visas ekranas ir priartinimo parinktys yra prieinamos.](./media/ecommerce-media-zoom.png)

Tolesnis paveikslėlis rodo medijos galerijos modulio pavyzdį, kuris išdirbo paveikslėlius (tai yra, nurodyti paveikslėliai nepriklauso nuo produkto ID ar puslapio konteksto).

![Medijos galerijos modulio pavyzdys, kuris išdirbo paveikslėlius](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>„Commerce Scale Unit“ sąveika

Kai paveikslėlio šaltinis kyla iš puslapio konteksto, produkto ID iš PDP yra naudojamas paveikslėlių gavimui. Medijos galerijos modulis gauna paveikslėlio failo kelią produktams naudodamas „Commerce Scale Unit“ programą programavimo sąsajas (API). Paveikslėliai yra tuomet ištraukiami iš „Media Library“ tam, kad galėtų būti sukuriami modulyje.

## <a name="add-a-media-gallery-module-to-a-page"></a>Įtraukti medijos galerijos modulį į puslapį

Tam, kad įtrauktumėte medijos galerijos modulį į puslapio komerciją, atlikite šiuos žingsnius.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. **Naujo šablono** teksto laukelyje, skyriuje **Šablono pavadinimas** įveskite **Komercijos šablono** ir tuomet pasirinkite **Gerai**.
1. Vietoje **Pagrindinė dalis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.
1. Nustatytojo puslapio **Pagrindinis** vietoje pasirinkite elipsę (**...**), ir tuomet pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. **Pasirinkite šabloną** teksto laukelyje, pasirinkite **Komercijos šablono** šabloną. Skyriuje **Puslapio pavadinimas**, įveskite **Medijos galerijos puslapis** ir tuomet pasirinkite **Gerai**.
1. Naujo puslapio vietoje **Pagrindinis** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Vietoje **Konteineris** pasirinkite daugtaškį (**...**), tada – **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Medijos galerija**, tada pasirinkite **Gerai**.
1. Ypatybių juostoje medijos galerijos modulyje, skyriuje **Paveikslėlio šaltinis** pasirinkite **ProduktoID**. Tuomet, **Produkto ID** laukelyje, įveskite produkto ID.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**. Turėtumėte matyti produkto paveikslėlius galerijos peržiūroje.
1. Tam, kad naudotumėte tik išdirbtus paveikslėlius, ypatybių juostoje skyriuje **Paveikslėlio šaltinis** pasirinkite **ProduktoID**. Tuomet skyriuje **Paveikslėliai**, pasirinkite **Įtraukti paveikslėlį** tiek kartų, kiek reikia tam, kad įtrauktumėte paveikslėlius iš „Media Library“.
1. Nustatykite papildomas ypatybes, kurias norite nustatyti, tokias kaip **Paveikslėlio priartinimas**, **Priartinimo faktorius** ir **Miniatiūros orientacija**.
1. Jums pabaigus, pasirinkite **Įrašyti**, pasirinkite **Baigti redagavimą** puslapio tikrinimui ir tuomet pasirinkite **Publikuoti** publikavimui.

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Konteinerio modulis](add-container-module.md)

[Vaizdų nusiuntimas](dam-upload-images.md)
