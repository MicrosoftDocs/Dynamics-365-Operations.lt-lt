---
title: Produktų rinkinio moduliai
description: Šiame straipsnyje pateikta produktų rinkinio modulių apžvalga Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 05/18/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 02a3d6314729f51d6c1dced5037f78d12355c09a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871664"
---
# <a name="product-collection-modules"></a>Produktų rinkinio moduliai

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikta produktų rinkinio modulių apžvalga Microsoft Dynamics 365 Commerce.

Produkto atradimas yra pirminis įrankis, kurį pardavėjai naudoja įtraukti savo klientus, esančius el. prekybos svetainėje. Produktų rinkinių moduliais pardavėjai gali sukurti įtikinamą apsipirkimo patirtį, suteikdami intuityvią vaizdo sąsają, kurią galima naudoti norint greitai pateikti produktų rinkinius.

Produktų rinkinio moduliai yra fiziniai produktai ir paslaugos svetainėje. Produktų rinkinio modulis paprastai susiejamas su išsamios informacijos puslapiu, kur klientai gali pirkti produktą ar paslaugą arba daugiau sužinoti apie juos. 

Produktų rinkinių šaltiniai gali būti toliau pateikiamų keturių tipų sąrašai.

- Redakciniai produktų sąrašai, nurodyti rankiniu būdu sprendime „Dynamics 365 Commerce“ kaip susiję produktai produktui ar produktų sąrašams
- Algoritminiai sąrašai, pvz., naujų, perkamiausių ar populiariausių produktų sąrašai
- Rekomendacijų sąrašai, pagrįsti mašininiu mokymu
- Personalizavimo sąrašai, palaikantys kliento personalizuotus rezultatus. Klientai turi būti prisijungę prie el. prekybos svetainės, kad matytų personalizuotus rezultatus. Vartotojai svečiai nemato personalizuotų rezultatų. Klientai gali atsisakyti personalizavimo [sąskaitos valdymo puslapyje](account-management.md).

Toliau pateiktame paveikslėlyje vaizduojami skirtingi produktų rinkinių tipai, naudojami el. prekybos svetainėje.

![Skirtingų tipų produktų rinkinių elektroninės prekybos svetainėje pavyzdys.](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Visada naudokite produktų rinkinio modulius, kad būtų rodoma panašaus tipo produktų grupė.

## <a name="product-collection-modules-and-types"></a>Produktų rinkinio moduliai ir tipai

Toliau pateikiamoje lentelėje aprašomi „Dynamics 365 Commerce“ įvairių tipų produktų rinkinių moduliai.

| Produktų atsiėmimo modulis  | Tipas | Aprašymas |
|----------------------------|------|-------------|
| Kategorija                   | Kategorija | Šis modulis rodo kategorijos produktų sąrašą, kaip apibrėžta naršymo kategorijų hierarchijoje, kurią mažmenininkas sukūrė kanalui. |
| Susiję produktai           | Redakcinis | Šiame modulyje pateikiamas autoriaus pasirinkto tipo produktų, kuriuos reklamavimo parduotuvėje vadovas sukonfigūravo kaip susijusius produktus „Commerce“, sąrašas. |
| Ieškos rezultatai             | Ieškos užklausa | Šio tipo produktų rinkinio modulis pateikia produktų sąrašą, kuris geriausiai atitinka ieškos užklausą, įvestą kliento. |
| Kuruotų produktų sąrašai      | Redakcinis | Šis modulis rodo pasirinktinius sąrašus, kuriuos prekybininkai ir redaktoriai sukūrė „Commerce“. |
| Naujos                        | Algoritminis | Šiame modulyje rodomas naujausių produktų, kurie buvo atrinkti į kanalus ir katalogus, sąrašas. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Perkamiausia               | Algoritminis | Šiame modulyje rodomas produktų, kurie išdėstyti pagal didžiausią pardavimo skaičių, sąrašas. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Populiaru                   | Algoritminis | Šiame modulyje rodomas tam tikro laikotarpio perkamiausių produktų sąrašas. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Dažnai perkama kartu | Dirbtinis intelektas / mašininis mokymas | Modulis, kuriame naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti susijusias prekes, kurios dažnai perkamos kartu su konkrečiu produktu. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Žmonėms taip pat patinka           | Dirbtinis intelektas / mašininis mokymas | Šiame modulyje naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti prekes, susijusias su konkrečiu produktu. Šiame sąraše prisiregistravusiam vartotojui gali būti rodomi personalizuoti rezultatai, jei svetainės autorius nustato atitinkamą parinktį. |
| Parinkta jums              | Dirbtinis intelektas / mašininis mokymas | Šiame modulyje naudojamas mašininis mokymas. skirtas analizuoti prisijungusio vartotojo pirkimo modelius ir pateikti personalizuotų rekomendacijų, paremtų šiais pirkimo modeliais. Vartotojui svečiui bus rodomas sutrauktas sąrašas. |

## <a name="supported-modules"></a>Palaikomi moduliai 

Produkto kolekcijos modulis palaiko [greito rodinio modulį](quick-view-module.md), kuris leidžia vartotojams peržiūrėti produkto informaciją ir įtraukti prekes į vežimėlį iš produkto kolekcijos puslapio.

## <a name="add-a-product-collection-module-to-a-category-page"></a>Įtraukti produktų rinkinio modulį į kategorijos puslapį

Norėdami įtraukti produktų rinkinio modulį į kategorijos puslapį, atlikite šiuos veiksmus.

1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį** po Puslapio **pavadinimas** įveskite tinkamą puslapio pavadinimą ir pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną pasirinkite** tą patį šabloną, kuris naudojamas jūsų numatytame kategorijos puslapyje, tada pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**. 
1. Subraštės **atminties** atminties puslapiuose pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite produktų rinkinio **modulį**, tada pasirinkite **Gerai**.  
1. Produktų rinkinio modulio ypatybių srityje pasirinkite **Įtraukti produktų sąrašą**.
1. Dialogo lange **Pasirinkti produktų sąrašo konfigūraciją** pasirinkite sąrašo tipą, sąrašo šaltinį ir įveskite elementų skaičių. Sukonfigūruokite visas kitas pasirinktis, kurias galima naudoti sąrašo tipui. Daugiau informacijos apie sąrašų tipus, žr. toliau pateikiamą lentelę. 
1. Pasirinkite **Gerai**.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Šioje lentelėje pateikiami sąrašų tipai, kuriuos galima pasirinkti dialogo lange **Pasirinkti produktų sąrašo konfigūraciją**.

| Tipas                       | Aprašymas | Naudojimas | Puslapio kontekstas | Konkretus kontekstas | Personalizavimas |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Produktai pagal kategoriją       | Produktų, priklausančių konkrečiai kategorijai, sąrašas. Ši kategorija nustatoma pagal puslapio kontekstą arba pagal kontekstą, kurį pateikia autorius. | Šis sąrašo tipas gali būti naudojamas bet kuriame puslapyje (pvz., pagrindiniame puslapyje, kategorijos puslapyje, rinkodaros puslapyje arba produkto išsamios informacijos puslapyje \[PIIP\]), norint reklamuoti konkrečią produktų kategoriją. | Kategorija nustatoma pagal puslapio kontekstą, jei yra (pvz., pagal kategorijos puslapį) | Autorius gali pateikti tam tikrą kategoriją kaip sąrašo kontekstą. | Netaikoma |
| Susiję produktai           | „Commerce“ pasirinkto tipo produktų, kuriuos reklamavimo parduotuvėje vadovas sukonfigūravo kaip susijusius produktus, sąrašas. | Šis sąrašo tipas visų pirma naudojamas PIIP, tačiau jis gali būti naudojamas bet kuriame puslapyje, jei pateikiamas pirminis produktas. | Produktas pagal puslapį, ryšio tipą (privalomas) | Produktą galima pasirinkti parinkiklyje; naudojamas ryšio tipas. | Netaikoma |
| Kuravo                    | Pasirinktinis sąrašas, kurį prekybininkai ir redaktoriai sukūrė „Commerce“. | Papildytas kategorijos puslapis, pagrindinis puslapis, prikimo užbaigimo bei krepšelio puslapiai ir produkto puslapiai | Netaikoma | Netaikoma | Netaikoma |
| Algoritminis                | <ul><li>**Nauja** – naujausių produktų, kurie buvo atrinkti į kanalus ir katalogus, sąrašas.</li><li>**Perkamiausi** – produktų, kurie išdėstyti pagal didžiausią pardavimų skaičių, sąrašas.</li><li>**Populiaru** – tam tikro laikotarpio perkamiausių produktų sąrašas.</li></ul> | Pagrindinis puslapis, papildytas kategorijos puslapis ir prikimo užbaigimo bei krepšelio puslapiai | Kategorija nustatoma pagal puslapio kontekstą (pvz., pagal kategorijos puslapį) | Kategorija, kurią nustato svetainės autorius | Palaikoma |
| Dažnai perkama kartu | Sąrašas, kuriame naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti susijusias prekes, kurios dažnai perkamos kartu su konkrečiu produktu. | Šis sąrašo tipas taikomas tik krepšelio puslapiui. | Krepšelis | Netaikoma | Palaikoma |
| Žmonėms taip pat patinka           | Sąrašas, kuriame naudojamas mašininis mokymas, skirtas vartotojų pirkimo tendencijoms analizuoti ir rekomenduoti prekes, susijusias su konkrečiu produktu. | Šis sąrašo tipas naudojamas PIIP, kad būtų rodomi kitų klientų įsigyti produktai. | Produkto kontekstas pagal puslapį | Produktas, kurį pateikia svetainės autorius | Palaikoma |
| Parinkta jums              | Sąrašas, kuriame naudojamas mašininis mokymas klientų poreikiams nustatyti. | Šis sąrašo tipas gali būti naudojamas bet kuriame puslapyje. | Netaikoma| Netaikoma | Palaikoma | 

## <a name="additional-resources"></a>Papildomi ištekliai

[Modulių bibliotekos apžvalga](starter-kit-overview.md)

[Karuselės modulis](add-carousel.md)

[Raiškiojo turinio bloko modulis](add-content-rich-block.md)

[Konteinerio modulis](add-container-module.md)

[Pirkimo langelio modulis](add-buy-box.md)

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[Greito rodinio modulis](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
