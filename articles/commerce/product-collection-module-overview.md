---
title: Produktų rinkinio moduliai
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų rinkinio modulių apžvalga.
author: v-chgri
manager: annbe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 31307035014f2fae6146f33bc23e3e06103f82eb
ms.sourcegitcommit: c237123ad94d9418994ac095fbd8634c05a927b1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/08/2020
ms.locfileid: "2943268"
---
# <a name="product-collection-modules"></a>Produktų rinkinio moduliai

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų rinkinio modulių apžvalga.

## <a name="overview"></a>Peržiūrėti

Produkto atradimas yra pirminis įrankis, kurį pardavėjai naudoja įtraukti savo klientus, esančius el. prekybos svetainėje. Produktų rinkinių moduliais pardavėjai gali sukurti įtikinamą apsipirkimo patirtį, suteikdami intuityvią vaizdo sąsają, kurią galima naudoti norint greitai pateikti produktų rinkinius.

Produktų rinkinio moduliai yra fiziniai produktai ir paslaugos svetainėje. Produktų rinkinio modulis paprastai susiejamas su išsamios informacijos puslapiu, kur klientai gali pirkti produktą ar paslaugą arba daugiau sužinoti apie juos. 

Produktų rinkinių šaltiniai gali būti toliau pateikiamų keturių tipų sąrašai.

- Redakciniai produktų sąrašai, nurodyti rankiniu būdu sprendime „Dynamics 365 Retail“ kaip susiję produktai produktui ar produktų sąrašams
- Algoritminiai sąrašai, pvz., naujų, perkamiausių ar populiariausių produktų sąrašai
- Rekomendacijų sąrašai, pagrįsti mašininiu mokymu
- Personalizavimo sąrašai, palaikantys kliento personalizuotus rezultatus. Klientai turi būti prisijungę prie el. prekybos svetainės, kad matytų personalizuotus rezultatus. Vartotojai svečiai nemato personalizuotų rezultatų. Klientai gali atsisakyti personalizavimo [sąskaitos valdymo puslapyje](account-management.md).

Toliau pateiktame paveikslėlyje vaizduojami skirtingi produktų rinkinių tipai, naudojami el. prekybos svetainėje.

![Skirtingų tipų produktų rinkinių el. prekybos svetainėje pavyzdys](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Visada naudokite produktų rinkinio modulius, kad būtų rodoma panašaus tipo produktų grupė.

## <a name="product-collection-modules-and-types"></a>Produktų rinkinio moduliai ir tipai

Toliau pateikiamoje lentelėje aprašomi „Dynamics 365 Commerce“ įvairių tipų produktų rinkinių moduliai.

| Produktų atsiėmimo modulis  | Tipas | Aprašymas |
|----------------------------|------|-------------|
| Kategorija                   | Kategorija | Šiame modulyje rodomas tam tikros kategorijos produktų sąrašas, apibrėžtas naršymo kategorijų hierarchijoje, kurią pardavėjas sukūrė mažmeninės prekybos kanalui. |
| Susiję produktai           | Redakcinis | Šis modulis pateikia produktų, kuriuos prekybos vadybininkas sukonfigūravo kaip susijusius produktus programoje „Retail“, sąrašą, skirtą ryšio tipui, kurį pasirinko autorius. |
| Kuruotų produktų sąrašai      | Redakcinis | Šiame modulyje rodomi tinkinti sąrašai, kuriuos sukūrė prekybininkai ir redaktoriai programoje „Retail“. |
| Naujos                        | Algoritminis | Šiame modulyje rodomas naujausių produktų, kurie buvo atrinkti į kanalus ir katalogus, sąrašas. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Perkamiausia               | Algoritminis | Šiame modulyje rodomas produktų, kurie išdėstyti pagal didžiausią pardavimo skaičių, sąrašas. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Populiaru                   | Algoritminis | Šiame modulyje rodomas tam tikro laikotarpio parduodamiausių produktų sąrašas. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Dažnai perkama kartu | Dirbtinis intelektas / mašininis mokymas | Modulis, kuriame naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti susijusias prekes, kurios dažnai perkamos kartu su konkrečiu produktu. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Žmonėms taip pat patinka           | Dirbtinis intelektas / mašininis mokymas | Šiame modulyje naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti prekes, susijusias su konkrečiu produktu. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Parinkta jums              | Dirbtinis intelektas / mašininis mokymas | Šiame modulyje naudojamas mašininis mokymas. skirtas analizuoti prisijungusio vartotojo pirkimo modelius ir pateikti personalizuotų rekomendacijų, paremtų šiais pirkimo modeliais. Vartotojui svečiui bus rodomas sutrauktas sąrašas. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Įtraukti produktų rinkinio modulį į kategorijos puslapį

Norėdami įtraukti produktų rinkinio modulį į kategorijos puslapį, atlikite šiuos veiksmus.

1. Būdami „Dynamics 365 Commerce“ eikite į savo svetainę ir sukurkite puslapį, kuriame naudojamas tas pats šablonas kaip numatytajame kategorijos puslapyje.
1. Puslapio struktūroje pasirinkite atkarpą **Antrinė poraštė**, pasirinkite daugtaškio mygtuką (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite **Konteineris** ir pasirinkite **Gerai**.
1. Pasirinkite daugtaškio mygtuką konteinerio modulyje ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite **Produkto rinkinys** ir pasirinkite **Gerai**.  
![Produktų rinkinio modulio vediklio srauto pavyzdys](./media/productCollectionModule.png)
1. Konfigūruokite parametrus pasirinkdami reikiamą duomenų šaltinį ir produktų rinkinio įvestis.
1. Produktų rinkinio modulio ypatybių srityje pasirinkite **Įtraukti produktų sąrašą**.
1. Dialogo lange **Pasirinkti produktų sąrašo konfigūraciją** pasirinkite sąrašo tipą, įveskite elementų skaičių ir pasirinkite bet kurias kitas sąrašo tipui galimas pasirinktis. Daugiau informacijos apie sąrašų tipus, žr. toliau pateikiamą lentelę. 
1. Pasirinkite **Gerai**.
1. Puslapį įrašykite, tada įrašykite ir atrakinkite.

Šioje lentelėje pateikiami sąrašų tipai, kuriuos galima pasirinkti dialogo lange **Pasirinkti produktų sąrašo konfigūraciją**.

| Tipas                       | Aprašymas | Naudojimas | Puslapio kontekstas | Konkretus kontekstas | Personalizavimas |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Produktai pagal kategoriją       | Produktų, priklausančių konkrečiai kategorijai, sąrašas. Ši kategorija nustatoma pagal puslapio kontekstą arba pagal kontekstą, kurį pateikia autorius. | Šis sąrašo tipas gali būti naudojamas bet kuriame puslapyje (pvz., pagrindiniame puslapyje, kategorijos puslapyje, rinkodaros puslapyje arba produkto išsamios informacijos puslapyje \[PIIP\]), norint reklamuoti konkrečią produktų kategoriją. | Kategorija nustatoma pagal puslapio kontekstą, jei yra (pvz., pagal kategorijos puslapį) | Autorius gali pateikti tam tikrą kategoriją kaip sąrašo kontekstą. | Netaikoma |
| Susiję produktai           | Produktų, kuriuos prekybos vadybininkas sukonfigūravo kaip ryšio tipo susijusius produktus programoje „Retail“, sąrašas. | Šis sąrašo tipas visų pirma naudojamas PIIP, tačiau jis gali būti naudojamas bet kuriame puslapyje, jei pateikiamas pirminis produktas. | Produktas pagal puslapį, ryšio tipą (privalomas) | Produktą galima pasirinkti parinkiklyje; naudojamas ryšio tipas. | Netaikoma |
| Kuravo                    | Tinkintas sąrašas, kurį sukūrė prekybininkai ir redaktoriai „Retail“ programoje. | Papildytas kategorijos puslapis, pagrindinis puslapis, prikimo užbaigimo bei krepšelio puslapiai ir produkto puslapiai | Netaikoma | Netaikoma | Netaikoma |
| Algoritminis                | <ul><li>**Nauja** – naujausių produktų, kurie buvo atrinkti į kanalus ir katalogus, sąrašas.</li><li>**Perkamiausi** – produktų, kurie išdėstyti pagal didžiausią pardavimų skaičių, sąrašas.</li><li>**Populiaru** – tam tikro laikotarpio parduodamiausių produktų sąrašas.</li></ul> | Pagrindinis puslapis, papildytas kategorijos puslapis ir prikimo užbaigimo bei krepšelio puslapiai | Kategorija nustatoma pagal puslapio kontekstą (pvz., pagal kategorijos puslapį) | Kategorija, kurią nustato svetainės autorius | Palaikoma |
| Dažnai perkama kartu | Sąrašas, kuriame naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti susijusias prekes, kurios dažnai perkamos kartu su konkrečiu produktu. | Šis sąrašo tipas taikomas tik krepšelio puslapiui. | Krepšelis | Netaikoma | Palaikoma |
| Žmonėms taip pat patinka           | Sąrašas, kuriame naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti prekes, susijusias su konkrečiu produktu. | Šis sąrašo tipas naudojamas PIIP, kad būtų rodomi kitų klientų įsigyti produktai. | Produkto kontekstas pagal puslapį | Produktas, kurį pateikia svetainės autorius | Palaikoma |
| Parinkta jums              | Sąrašas, kuriame naudojamas mašininis mokymas klientų poreikiams nustatyti. | Šis sąrašo tipas gali būti naudojamas bet kuriame puslapyje. | Netaikoma| Netaikoma | Palaikoma | 

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Karuselės modulis](add-carousel.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Turinio išdėstymo modulis](add-content-placement-modules.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Produktų rekomendacijų apžvalga](product-recommendations.md)
