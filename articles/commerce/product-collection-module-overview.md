---
title: Produktų rinkinio moduliai
description: Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų rinkinio modulių apžvalga.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785472"
---
# <a name="product-collection-modules"></a>Produktų rinkinio moduliai  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje pateikiama „Microsoft Dynamics 365 Commerce“ produktų rinkinio modulių apžvalga.

## <a name="overview"></a>Peržiūrėti

Produkto atradimas yra pirminis įrankis, kurį pardavėjai naudoja įtraukti savo klientus, esančius el. prekybos svetainėje. Produktų rinkinių moduliais pardavėjai gali sukurti įtikinamą apsipirkimo patirtį, suteikdami intuityvią vaizdo sąsają, kurią galima naudoti norint greitai pateikti produktų rinkinius.

Produktų rinkinio moduliai yra fiziniai produktai ir paslaugos svetainėje. Produktų rinkinio modulis paprastai susiejamas su išsamios informacijos puslapiu, kur klientai gali pirkti produktą ar paslaugą arba daugiau sužinoti apie juos. 

Produktų rinkinių šaltiniai gali būti trijų tipų sąrašai:

- Redakciniai produktų sąrašai, nurodyti rankiniu būdu sprendime „Dynamics 365 Retail“ kaip susiję produktai produktui ar produktų sąrašams
- Algoritminiai sąrašai, pvz., naujų, perkamiausių ar populiariausių produktų sąrašai
- Rekomendacijų sąrašai, pagrįsti mašininiu mokymu

Toliau pateiktame paveikslėlyje vaizduojami skirtingi produktų rinkinių tipai, naudojami el. prekybos svetainėje.

![Skirtingų tipų produktų rinkinių el. prekybos svetainėje pavyzdys](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Visada naudokite produktų rinkinio modulius, kad būtų rodoma panašiaus tipo ar temos produktų grupė.

## <a name="product-collection-modules-and-types"></a>Produktų rinkinio moduliai ir tipai

Toliau pateikiamoje lentelėje aprašomi „Dynamics 365 Commerce“ įvairių tipų produktų rinkinių moduliai.

| Produktų atsiėmimo modulis  | Tipas | Aprašymas |
|----------------------------|------|-------------|
| Naršymas kategorijose            | Redakcinis | Šio tipo produktų rinkinio modulyje naudojama naršymo kategorijų hierarchija, kurią mažmeninės prekybos kanalui sukūrė pardavėjas, kad būtų rodomas produktų, siūlomų konkrečioje svetainės kategorijoje, naršymo srautas. |
| Ieškos rezultatai             | Ieškos užklausa | Šio tipo produktų rinkinio modulis pateikia produktų sąrašą, kuris geriausiai atitinka ieškos užklausą, įvestą kliento. |
| Susiję produktai           | Redakcinis | Šio tipo produktų rinkinio modulis pateikia produktų, kuriuos prekybos vadybininkas sukonfigūravo kaip susijusius produktus „Retail“ programoje, sąrašą, skirtą ryšio tipui, kurį pasirinko autorius. |
| Kuruotų produktų sąrašai      | Redakcinis | Šio tipo produktų rinkinio modulis pateikia pasirinktinius sąrašus, kuriuos prekybininkai ir redaktoriai sukūrė „Retail“ programoje. |
| Naujos                        | Algoritminis | Šio tipo produktų rinkinio modulis pateikia naujausių produktų, kurie buvo atrinkti į kanalus ir katalogus, sąrašą. |
| Perkamiausia               | Algoritminis | Šio tipo produktų rinkinio modulis pateikia produktų, kurie yra suskirstyti pagal didžiausią pardavimo skaičių, sąrašą. |
| Populiaru                   | Algoritminis | Šio tipo produktų rinkinio modulis pateikia tam tikro laikotarpio parduodamiausių produktų sąrašą. |
| Dažnai perkama kartu | Dirbtinis intelektas / mašininis mokymas | Šio tipo produktų rinkinio modulyje naudojamas mašininis mokymas analizuoti vartotojų pirkimo tendencijas ir rekomenduoti susijusias prekes, kurios dažnai perkamos kartu su nurodytu produktu. |
| Žmonėms taip pat patinka           | Dirbtinis intelektas / mašininis mokymas | Šio tipo produktų rinkinio modulyje naudojamas mašininis mokymas analizuoti vartotojų pirkimo tendencijas ir rekomenduoti prekes, susijusias su nurodytu produktu. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Įtraukti produktų rinkinio modulį į kategorijos puslapį

Norėdami įtraukti produktų rinkinio modulį į kategorijos puslapį, atlikite šiuos veiksmus.

1. Būdami „Dynamics 365 Commerce“ eikite į savo svetainę ir sukurkite puslapį, kuriame naudojamas tas pats šablonas kaip numatytajame kategorijos puslapyje.
1. Puslapio struktūroje pasirinkite atkarpą **Antrinė poraštė**, pasirinkite daugtaškio mygtuką (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite **Konteineris** ir pasirinkite **Gerai**.
1. Pasirinkite daugtaškio mygtuką konteinerio modulyje ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite **Produkto rinkinys** ir pasirinkite **Gerai**.
1. Konfigūruokite parametrus pasirinkdami reikiamą duomenų šaltinį ir produktų rinkinio įvestis.
1. Produktų rinkinio modulio ypatybių srityje pasirinkite **Įtraukti produktų sąrašą**.
1. Dialogo lange **Pasirinkti produktų sąrašo konfigūraciją** pasirinkite sąrašo tipą, įveskite elementų skaičių ir pasirinkite bet kurias kitas sąrašo tipui galimas pasirinktis. Daugiau informacijos apie sąrašų tipus, žr. toliau pateikiamą lentelę. 
1. Pasirinkite **Gerai**.
1. Puslapį įrašykite, tada įrašykite ir atrakinkite.

Šioje lentelėje pateikiami sąrašų tipai, kuriuos galima pasirinkti dialogo lange **Pasirinkti produktų sąrašo konfigūraciją**.
   
| Tipas                       | Aprašymas | Bendroji praktika | Kontekstas, kuris gali būti gaunamas iš puslapio konteksto | Kontekstas, su kuriuo autorius gali perrašyti puslapio kontekstą |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Produktai pagal kategoriją       | Produktų, priklausančių konkrečiai kategorijai, sąrašas. Ši kategorija nustatoma pagal puslapio kontekstą arba pagal kontekstą, kurį pateikia autorius. | Papildytas kategorijos puslapis, pagrindinis puslapis, prikimo užbaigimo bei krepšelio puslapiai ir produkto puslapiai | Kategorija | Kategorija, kurią nustato autorius |
| Susiję produktai           | Produktų, kuriuos prekybos vadybininkas konfigūruoja ryšio tipui kaip „Retail“ susijusius produktus, sąrašas. | Produkto puslapis, pagrindinis puslapis, norų sąrašo puslapis ir kliento paskyros puslapis | Produktų, ryšių tipas (privalomas)  | Produktų, ryšių tipai |
| Kuravo                    | Tinkintas sąrašas, kurį sukūrė prekybininkai ir redaktoriai „Retail“ programoje. | Papildytas kategorijos puslapis, pagrindinis puslapis, prikimo užbaigimo bei krepšelio puslapiai ir produkto puslapiai | Netaikoma | Sąrašo parinkiklis |
| Pagal algoritmą                | <ul><li>**Nauja** – naujausių produktų, kurie buvo atrinkti į kanalus ir katalogus, sąrašas.</li><li>**Perkamiausi** – produktų, kurie išdėstyti pagal didžiausią pardavimų skaičių, sąrašas.</li><li>**Populiaru** – tam tikro laikotarpio parduodamiausių produktų sąrašas.</li></ul> | Pagrindinis puslapis, papildytas kategorijos puslapis ir prikimo užbaigimo bei krepšelio puslapiai | Kategorija | Kategorija, kurią nustato autorius |
| Dažnai perkama kartu | Sąrašas, kuriame naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti susijusias prekes, kurios dažnai perkamos kartu su konkrečiu produktu. | Produktų puslapiai ir pirkimo užbaigimo bei krepšelio puslapiai | Produktas, krepšelis | Įtraukti krepšelį |
| Žmonėms taip pat patinka           | Sąrašas, kuriame naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti prekes, susijusias su konkrečiu produktu. | Produktų puslapiai ir pirkimo užbaigimo bei krepšelio puslapiai | Produktas, krepšelis | Netaikoma |

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbo pradžios rinkinio apžvalga](starter-kit-overview.md)

[Karuselės modulis](add-carousel.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Turinio išdėstymo modulis](add-content-placement-modules.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)
