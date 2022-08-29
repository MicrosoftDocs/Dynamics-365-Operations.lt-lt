---
title: Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga
description: Šiame straipsnyje pateikta numatytosios kategorijos paieškos puslapio ir ieškos rezultatų puslapio peržiūra Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/30/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: 1f2e4eb8825dd690f926f7f0bdfc39f1eb5fb83c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276379"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a>Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikta numatytosios kategorijos medžiagų puslapio peržiūra ir ieškos rezultatų puslapis Microsoft Dynamics 365 Commerce "e-Commerce".

## <a name="default-category-landing-page"></a>Numatytasis kategorijos nukreipimo puslapis

Numatytasis kategorijos nukreipimo puslapis yra puslapis, į kurį paprastai perkeliami svetainės vartotojai, pasirinkę kategoriją naršymo hierarchijoje. Kategorijos puslapyje galite naršyti bei rikiuoti ir tikslinti į kategorijas suskirstytus produktus.

![Numatytasis kategorijos nukreipimo puslapis.](./media/SimpleCategoryLandingDressCategory.png)

Puslapio viršuje yra antraštė, rodanti visas produktų kategorijas ir kitus puslapius, kuriuos prekybos vadovas suskirstė į kategorijas. Ši konfigūracija atliekama konfigūruojant kanalų naršymo hierarchiją. Puslapio apačioje yra poraštė, kurioje pateikiami spartieji saitai į įvairius straipsnius, kurie gali būti dominamas pagal pardavėją.

Toliau nurodyti esminiai kategorijos komponentai.

- **Produktų išdėstymo plytelėse** rodomi produktai, kuriuos prekybos vadovas nustatė kategorijoje, konfigūruodamas naršymo hierarchiją.
- **Tikslinimo priemonės ir pasirinkimų suvestinė** yra filtrai, kurie nurodo skaičių ir kuriuos naudojant galima tikslinti prekes. Prekybos vadovas juos konfigūruoja konfigūruodamas metaduomenis, susijusius su kanalų kategorijomis ir produktų atributais.
- **Rikiavimo parinktis** svetainės lankytojai naudoja produktams rikiuoti. Numatyta, kad galimos tolesnės rikiavimo parinktys.

    - Kaina – nuo mažiausios iki didžiausios
    - Kaina – nuo didžiausios iki mažiausios
    - Produkto pavadinimas – \[A-Ž\]
    - Produkto pavadinimas – \[Ž-A\]
    - Įverčiai – nuo mažiausio iki didžiausio
    - Įverčiai – nuo didžiausio iki mažiausio

- **Išplėstinės rūšiavimo pasirinktys** naudojamos pagal svetainės reikalavimus, siekiant rūšiuoti produktus naudojant intelektualius kriterijus. Įgalinus [produkto rekomendacijas](product-recommendations.md), galimos šios rūšiavimo pasirinktys. Daugiau informacijos rasite produktų rekomendacijų [tipų](product-recommendations.md#types-of-product-recommendations) straipsnyje.

    - Naujos
    - Geriausia pardavimo kaina
    - Populiaru

- **Skaidymo į puslapius funkcija** svetainės lankytojams leidžia iš vieno į kategorijas suskirstytų produktų rezultatų puslapio pereiti į kitą puslapį.
- **Bendras skaičius** – pateikiamas bendras kategorijoje nustatytų produktų skaičius.

## <a name="enrich-a-category-landing-page"></a>Papildyti kategorijos nukreipimo puslapį

Jei norite, kad kategorijos nukreipimo puslapyje konkreti kategorija būtų labiau pritaikyta, galite tos kategorijos nukreipimo puslapį papildyti. Pavyzdžiui, galite įtraukti rinkodaros vaizdo įrašą ir istorijų apie kategoriją, kad patrauktumėte pirkėjo dėmesį. Norėdami gauti daugiau informacijos, žr. [Kategorijos nukreipimo puslapio papildymas](enrich-category-page.md).

![Papildytas kategorijos nukreipimo puslapis.](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a>Automatinio siūlymo ir ieškos rezultatų puslapiai

Svetainės vartotojai ją gali naršyti eidami į kategoriją iš naršymo hierarchijos arba įvesdami ieškos terminą ieškos lauke.

Vartotojams tik pradėjus vesti tekstą ieškos lauke, jie patiria įtraukiančią automatinio siūlymo funkciją, siūlančią ieškos terminus.

Toliau pateikiami keli pasiūlymų tipai, kurie gali būti rodomi.

- **Raktažodžiai** naudojami norint rasti prekes tarp visų produktų, pateiktų kanale.
- **Produktai** yra tiesioginiai saitai su produktų išsamios informacijos puslapiu.
- **Aprėptos kategorijos Ieškos pasiūlymuose** išvardytos įvairios kategorijos, vartotojams leidžiančios ieškoti raktažodžio konkrečioje kategorijoje.

![Įtraukianti automatinio siūlymo funkcija.](./media/ImmersiveAutoSuggestUX.png)

Kai vartotojai pasirenka vieną iš raktažodžių arba aprėptos kategorijos ieškos pasiūlymų, arba kai nėra pasiūlymų, susijusių su jų įvestu ieškos terminu, jie nukreipiami į ieškos rezultatų puslapį. Norėdami rasti pageidaujamą prekę, tada vartotojai gali naršyti, rikiuoti ir tikslinti ieškos rezultatų sąrašą.

![Ieškos nukreipimas.](./media/SearchLanding.png)

Toliau nurodyti esminiai ieškos rezultatų puslapio komponentai.

- **Produktų išdėstymo plytelėse** rodomi vartotojo ieškos produktai. Numatyta, kad šios plytelės rikiuojamos pagal debesų technologija paremtą vartotojo ieškos aktualumo balą.
- **Tikslinimo priemonės ir pasirinkimų suvestinė** yra filtrai, kurie nurodo skaičių ir kuriuos naudojant galima tikslinti prekes. Prekybos vadovas jas konfigūruoja konfigūruodamas kanalų kategorijų ir produktų atributų metaduomenis.
- **Standartinės rūšiavimo** pasirinktys naudojamos pagal svetainės reikalavimus produktams rūšiuoti. Numatyta, kad galimos tolesnės rikiavimo parinktys.

    - Kaina – nuo mažiausios iki didžiausios
    - Kaina – nuo didžiausios iki mažiausios
    - Produkto pavadinimas – \[A-Ž\]
    - Produkto pavadinimas – \[Ž-A\]
    - Įverčiai – nuo mažiausio iki didžiausio
    - Įverčiai – nuo didžiausio iki mažiausio
    - Numatytasis 
    
    > [!NOTE]
    > Jei **nustatomos naršymo** hierarchijos produktų rodymo užsakymo vertės, rūšiuojant pagal numatytuosius nustatymus **kategorijos puslapyje paisomos rodymo užsakyme apibrėžtos vertės**. Kitu atveju bus rūšiuojant pagal produkto **numerį**.)
    
- **Išplėstinės rūšiavimo pasirinktys** naudojamos pagal svetainės reikalavimus, siekiant rūšiuoti produktus naudojant intelektualius kriterijus. Įgalinus [produkto rekomendacijas](product-recommendations.md), galimos šios rūšiavimo pasirinktys. Daugiau informacijos rasite produktų rekomendacijų [tipų](product-recommendations.md#types-of-product-recommendations) straipsnyje.

    - Naujos
    - Geriausia pardavimo kaina
    - Populiaru

- **Skaidymo į puslapius funkcija** svetainės lankytojams leidžia iš vieno į kategorijas suskirstytų produktų rezultatų puslapio pereiti į kitą puslapį.
- **Bendras skaičius** – pateikiamas bendras kategorijoje nustatytų ir ieškos kriterijus atitinkančių produktų skaičius.

>[!NOTE]
>Šios debesų kompiuterijos ieškos galimybės prieinamos 10.0.8 versijoje. Įsitikinkite, kad dalyje **Prekybos parametrai > Konfigūracijos parametrai** yra įrašas, skirtas „Productsearch.UseAzureSearch” nustatytas kaip „true”. 
![Konfigūracijos parametrai debesies aplinkos ieškoje.](./media/CloudPoweredSearchConfigurationParameters.png)

>Be to, norėdami naudoti išplėstinio rūšiavimo pasirinktis, tokias kaip naujas, geriausias pardavimas ir tendencija, [turite įgalinti produkto rekomendacijas](product-recommendations.md) savo aplinkai. Išplėstinės rūšiavimo pasirinktys galimos naudojant "Commerce SDK" 9.35+ versiją ir "Commerce" versiją 10.0.20.

## <a name="additional-resources"></a>Papildomi ištekliai

[Debesų technologija valdomos ieškos apžvalga](cloud-powered-search-overview.md)

[Pagrindinio puslapio apžvalga](quick-tour-home-page.md)

[Išsamios informacijos apie produktus puslapių apžvalga](quick-tour-pdp.md)

[Krepšelio ir pirkimo užbaigimo puslapių apžvalga](quick-tour-cart-checkout.md)

[Paskyrų tvarkymo puslapių apžvalga](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
