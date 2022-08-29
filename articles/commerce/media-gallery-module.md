---
title: Medijos galerijos modulis
description: Šiame straipsnyje aprašomi laikmenų galerijas moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5e2d0a4422341badee906c71bebdd491e18a38cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273464"
---
# <a name="media-gallery-module"></a>Medijos galerijos modulis

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašomi laikmenų galerijas moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

Medijos galerijos moduliai rodo vieną ar keletą paveikslėlių galerijos peržiūroje. Medijos galerijos moduliai palaiko miniatūros vaizdus, kurie gali būti tvarkomi horizontaliai (kaip toliau esantis paveikslėlis) ar vertikaliai (kaip stulpelis šalia paveikslėlio). Medijos galerijos moduliai taip pat pateikia galimybes, kurios įjungia paveikslėlio priartinimą (pagerintą) ar peržiūrą visame ekrane. Tam, kad būtų sukurtas medijos galerijos režime, paveikslėlis turi būti prieinamas prekybos svetainės kūrimo įrankyje „Media Library“. Šiuo metu medijos galerijos moduliai palaiko tik paveikslėlius.

Nustatytame režime, medijos galerijos modulis naudoja produkto ID, kuris yra prieinamas iš produkto informacijos puslapio turinio (PDP) tam, kad sukurtų atitinkamus produkto paveikslėlius. Prekybos štabe medijos failo kelias turi būti nustatytas visiems produktams. Paveikslėliai turi būti po to atnaujinti į vietos kūrimo įrankį „Media Library“ pagal failo kelią, kuris buvo nustatytas produktams prekybos štabe. Šie paveikslėliai apima produktų paveikslėlius ir visus produkto variantus. Dėl išsamesnės informacijos apie tai, kaip įkelti paveikslėlius į svetainės kūrimo įrankį „Media Library“, žr. [Įkelti paveikslėlius](dam-upload-images.md).

Kitu atveju, medijos galerijos modulis gali talpinti visą išdirbtą paveikslėlių rinkinį paveikslėlio galerijos puslapyje, kuriame nėra jokių priklausinių nuo produkto ID ar puslapio konteksto. Šiuo atveju, paveikslėliai turi būti įkelti į svetainės kūrimo įrankį „Media Library“ ir nurodyti svetainės kūrimo įrankyje.

Čia yra keletas panaudojimo pavyzdžių medijos galerijos moduliams:

- Produkto paveikslėlių kūrimas PDP
- Produkto paveikslėlių kūrimas produkto komercijos puslapyje
- Išdirbto paveikslėlių rinkinio rodymas komercijos puslapyje, tokiame kaip galerijos puslapis

Šiame pavyzdiniame tolesniame paveikslėlyje, pirkimo laukelis PDP talpina produkto paveikslėlį naudodamas medijos galerijos modulį.

![Įsigijimo laukelio pavyzdys produkto informacijos puslapyje talpina produkto paveikslėlius naudodamas medijos galerijos modulį.](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Medijos galerijos ypatybės

| Ypatybės pavadinimas | Reikšmės | Aprašas |
|---------------|--------|-------------|
| Vaizdo šaltinis | **Puslapio kontekstas** ar **Produkto ID** | Nustatytoji vertė yra **Puslapio kontekstas**. Jei **Puslapio kontekstas** yra pasirinktas, modulis tikisi, kad puslapis pateiks produkto ID informaciją. Jei **Produkto ID** yra pasirinktas, produkto ID paveikslėliui turi būti patvirtintas kaip  **Produkto ID** ypatybės vertė. Ši savybė yra prieinama 10.0.12 prekybos versijoje. |
| Produkto ID | Produkto ID | Ši ypatybė yra taikoma tik, jei **Paveikslėlio šaltinio** ypatybės vertė yra **Produkto ID**. |
| Vaizdo mastelio keitimas | **Pagal liniją** ar **Konteineris** | Ši ypatybė leidžia vartotojui priartini paveikslėlius medijos galerijos modulyje. Paveikslėlis gali būti priartintas pagal liniją ar atskirame konteineryje šalia paveikslėlio. Ši savybė yra prieinama 10.0.12 prekybos versijoje. |
| Mastelio koeficientas | Dešimtainis skaičius | Ši ypatybė nurodo skalės faktorių paveikslėlių priartinimui. Pavyzdžiui, jei vertė yra nustatyta į **2,5**, paveikslėlis yra priartinamas 2,5 karto. |
| Visas ekranas | **Teisinga** arba **Klaidinga** | Ši ypatybė nurodo, ar paveikslėliai gali būti peržiūrimi visame ekrane. Visame ekrane paveikslėliai gali taip pat būti toliau padidinami, jei priartinimo savybė yra įjungta. Ši savybė yra prieinama „Commerce“ versijos 10.0.13 leidime. |
| Padidinta vaizdo kokybė | Skaičius nuo 1 iki 100, nurodantis procentą ir pasirinktas naudojant sekimo juostos valdiklį | Ši ypatybė nurodo paveikslėlio kokybę, pagal ką galima keisti mastelį. Galima nustatyti 100 procentų norint užtikrinti, kad tolintas vaizdas visada naudos didžiausią galimą skiriamąją gebą. Ši ypatybė netaikoma PNG failams, nes jie naudoja nesąnaudingą formatą. Ši savybė yra prieinama „Commerce“ versijos 10.0.19 leidime. |
| Vaizdai | Svetainės kūrimo įrankyje „Media Library“ pasirinkti paveikslėliai | Kartu su kūrimu iš produkto, paveikslėliai gali būti išdirbami medijos galerijos moduliui. Šie paveikslėliai bus pridėti prie bet kurio gaminio prieinamų paveikslėlių. Ši savybė yra prieinama 10.0.12 prekybos versijoje. |
| Miniatiūros orientacija | **Vertikaliai** ar **Horizontaliai** | Ši ypatybė nurodo, ar miniatiūros paveikslėliai turi būti rodomi vertikalioje ar horizontalioje juostoje. |
| Slėpti varianto bendrojo produkto vaizdus | **Teisinga** arba **Klaidinga** | Jei ši ypatybė nustatyta kaip Teisinga, pasirinkus variantą bendrojo produkto vaizdai **paslėpti**, nebent variante nėra vaizdų. Ši ypatybė neturi įtakos produktams, kurie neturi variantų. |
| Atnaujinti dimensijų pasirinkimo medijas | **Teisinga** arba **Klaidinga** | Jei ši ypatybė nustatyta kaip **Teisinga**, media bibliotekos vaizdai bus atnaujinti pasirinkus bet kokią dimensiją (pvz., spalvą, stilių arba dydį) ir jei vaizdas yra galimas. Ši ypatybė padeda supaprastinti naršymo patirtį, nes reikia pasirinkti ne visas produkto varianto dimensijas, kad būtų galima atnaujinti atitinkamą vaizdą. Ši ypatybė prieinama skirtuke **Papildoma**. |

> [!IMPORTANT]
> Dimensijų **pasirinkimo ypatybėje atnaujinti mediją** galima naudoti kaip „Commerce" 10.0.21 versiją. Tam reikia, kad būtų įdiegta „Commerce“ modulio bibliotekos paketo versija 9.31.

Toliau pateiktas paveikslėlis rodo medijos galerijos modulio pavyzdį, kuriame visas ekranas ir priartinimo parinktys yra prieinamos.

![Medijos galerijos modulio pavyzdys, kuriame visas ekranas ir priartinimo parinktys yra galimos.](./media/ecommerce-media-zoom.png)

Tolesnis paveikslėlis rodo medijos galerijos modulio pavyzdį, kuris išdirbo paveikslėlius (tai yra, nurodyti paveikslėliai nepriklauso nuo produkto ID ar puslapio konteksto).

![Medijos galerijos modulio pavyzdys, kuris išdirbo paveikslėlius.](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>„Commerce Scale Unit“ sąveika

Kai paveikslėlio šaltinis kyla iš puslapio konteksto, produkto ID iš PDP yra naudojamas paveikslėlių gavimui. Medijos galerijos modulis gauna paveikslėlio failo kelią produktams naudodamas „Commerce Scale Unit“ programą programavimo sąsajas (API). Paveikslėliai yra tuomet ištraukiami iš „Media Library“ tam, kad galėtų būti sukuriami modulyje.

## <a name="add-a-media-gallery-module-to-a-page"></a>Įtraukti medijos galerijos modulį į puslapį

Tam, kad įtrauktumėte medijos galerijos modulį į puslapio komerciją, atlikite šiuos žingsnius.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Dialogo lange **Naujas šablonas**, po Šablono **pavadinimu**, įveskite **Rinkodaros šabloną** ir pasirinkite **Gerai**.
1. Teksto atminties **atminties** atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Numatytasis** puslapis, tada pasirinkite **Gerai**.
1. Numatytojo **puslapio** pagrindiniame atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte šabloną, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį,** po Puslapio pavadinimas **įveskite** Media **galerija** puslapį ir pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną pasirinkite** rinkodaros šabloną **, kurį sukūrėte**, tada pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**. 
1. Naujo puslapio **pagrindiniame** atrinkinyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite medijų galerija **modulį**, tada pasirinkite **Gerai**.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
