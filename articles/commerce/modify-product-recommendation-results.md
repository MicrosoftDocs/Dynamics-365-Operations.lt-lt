---
title: DI-MM pagrįstų produktų rekomendacijų rezultatų koregavimas
description: Šioje temoje paaiškinama, kaip jūsų verslui pritaikyti produkto rekomendacijų rezultatus, pagrįstus dirbtinio intelekto mašininiu mokymu (AI-ML).
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a319007b32a8a52bd4a0c0af337ed8fd4062cfa
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346673"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>DI-MM pagrįstų produktų rekomendacijų rezultatų koregavimas


[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip jūsų verslui pritaikyti produkto rekomendacijų rezultatus, pagrįstus dirbtinio intelekto mašininiu mokymu (AI-ML). 

Įjungus produkto rekomendacijas, numatytieji parametrai įsigalios. Šie parametrai bus naudingi arba galės būti naudingi daugeliu atvejų. Geriausia planuoti skirti kažkiek laiko įvertinant, ar rezultatai atitinka produktų pardavimo pasiūlymą. Prieš vėl atliekant bandymą, rekomenduojame įvertinti kelių dienų rezultatus prieš keičiant parametrus. 

## <a name="understanding-recommendation-list-parameters"></a>Rekomendacijų sąrašo parametrų supratimas

Prieš keisdami parametrus, sužinokite, kaip jie paveiks toliau esančius rezultatus.

### <a name="trending-product-list"></a>Produktų sąrašas „Populiariausi“

Produktų sąraše „Populiariausi“ galima pakeisti du parametrus.

![Sąrašo „Populiariausi“ numatytųjų parametrų pavyzdys](./media/exampletrendingparameters.png)

1. **Įtraukti naujų produktų iš paskutinių X dienų** – produktus, įtrauktus į nurodytą dienų skaičių iki esamos datos, galima naudoti renkant produktų kandidatus. Numatytoji paveikslėlio vertė rodo, kad produktai, esantys 180 dienų, gali būti naudojami populiariausių produktų sąraše.
1. **Įtraukti paskutinių X dienų pardavimą** – pardavimo operacijos, įvykusios nurodytame dienų skaičiuje iki esamos datos, galima naudoti užsakant produktų. Pirmiau nurodyta numatytoji vertė rodo, kad visi produkto pirkimai, atlikti per pastarąsias 30 dienų, bus naudojami nustatant produktų išdėstymą populiariausių produktų sąraše. 

### <a name="best-selling-product-list"></a>Produktų sąrašas „Geriausiai parduodami“

Atsižvelgiant į jūsų verslą, sąrašas „Geriausiai parduodami“ gali duoti kitokių rezultatų nei „Populiariausi“, net jei jie abu užsako produktus naudodamiesi operacijų duomenimis. Kadangi perkamiausi produktai nėra atskiriami pagal asortimento datą, sąraše Perkamiausi vis tiek galima išskirti labai populiarius, senesnius produktus, kurie galbūt nebepatenka į populiariausių sąrašą. 

„Populiariausi“ produktų sąraše galima pakeisti vieną parametrą.

![Sąrašo Perkamiausi numatytojo parametro pavyzdys.](./media/examplebestsellingparameters.PNG)

1. **Įtraukti paskutinių X dienų pardavimą** – pardavimo operacijos, įvykusios nurodytame dienų skaičiuje iki esamos datos, galima naudoti užsakant produktų. Pirmiau nurodyta numatytoji vertė rodo, kad visi produkto pirkimai, atlikti per pastarąsias 30 dienų, bus naudojami nustatant produktų išdėstymą produktų sąraše Perkamiausi. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Produktų įtraukimas į rekomendacijų sąrašus arba pašalinimas iš jų rankiniu būdu

### <a name="for-new-trending-or-best-selling-lists"></a>Sąrašai „Naujas“, „Populiariausi“ arba „Geriausiai parduodami“

1.  Eikite į **Mažmeninė prekyba ir komercija** > **Produkto rekomendacijos** > **Rekomendacijų parametrai**.
1.  Bendrinamų parametrų sąraše pasirinkite **Rekomendacijų sąrašai**.
1.  Pasirinkite sąrašą, į kurį įtrauksite produktus arba iš kurio juos pašalinsite.
1.  Norėdami prie lentelės pridėti produktų, pasirinkite **įtraukti eilutę**. 
1.  Stulpelyje Produktas ieškokite produkto pagal **Pavadinimas** arba **Produkto numeris**.

    ![Produkto paieškos sąraše „Nauji produktai“ pavyzdys.](./media/examplenewlistconfiguration1.png)

1.  Stulpelyje Eilutės tipas pasirinkite vieną iš dviejų parinkčių:
    -   **Įtraukti** – produktas priverstinai įtraukiamas į sąrašo priekį
    -   **Neįtraukti** – produktas neįtraukiamas ir nerodomas sąraše
    
    ![Produkto įtraukimo arba neįtraukimo į sąrašą „Nauji produktai“ pavyzdys.](./media/examplenewlistconfiguration2.png)

1.  Pakeitus **Rodymo tvarka**, bus pakeista produktų žymėjimo tvarka ir sąraše pasirodys **įtraukti**.
    - Jei du produktai turi tokią pačią reikšmę **Rodymo tvarka**, tada galutinė tvarka tų dviejų rezultatų gali skirtis nuo esančios įmonės padalinyje.
1.  Norėdami pašalinti produktus iš lentelės, pasirinkite šalintiną eilutę ir pasirinkite **Pašalinti**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Sąrašai „Žmonėms taip pat patiko“ arba „Kartu taip pat perkama“

Sąrašuose „Kartu taip pat perkama“ arba „Žmonėms taip pat patiko“ naudojamas mašininis mokymas, kuris išanalizuoja vartotojų pirkimo elgseną, kad būtų galima rekomenduoti su pradiniu produktu susijusius produktus, paprastai įsigyjamus kartu. 
 
*Pradinis produktas* yra produktas, kuriam norite generuoti rezultatus. Norėdami rankiniu būdu pakoreguoti rekomendacijų sąrašus, įtraukiate šiam produktui rezultatus arba pašalinate juos. 

Atlikite šiuos veiksmus, kad pradiniam produktui rankiniu būdu įtrauktumėte rezultatų arba juos pašalintumėte:
1.  Pasirinkite **Pradinis produktas**. 
1.  Stulpelyje **Produktas** ieškokite produkto pagal **Pavadinimas** arba **Produkto numeris.**
![Produkto ieškos sąraše Dažnai kartu perkama pavyzdys.](./media/exampleFBTlistconfiguration1.png)
1. Stulpelyje **Eilutės tipas** pasirinkite vieną iš dviejų parinkčių:
    - **Įtraukti** – produktas priverstinai įtraukiamas į sąrašo priekį
    - **Neįtraukti** – produktas neįtraukiamas ir nerodomas sąraše     
![Produkto, esančio sąraše Dažnai kartu perkama, įtraukimo arba neįtraukimo pavyzdys.](./media/exampleFBTlistconfiguration2.png)
1.  Norėdami pašalinti produktus iš lentelės, pasirinkite šalintiną eilutę ir pasirinkite Pašalinti.


## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[„Azure Data Lake Storage“ įgalinimas „Dynamics 365 Commerce“ aplinkoje](enable-adls-environment.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[Personalizuotų rekomendacijų įjungimas](personalized-recommendations.md)

[Personalizuotų rekomendacijų atsisakymas](personalization-gdpr.md)

[Įjungti „apsipirkti panašia mada“ rekomendacijas](shop-similar-looks.md)

[Produktų rekomendacijų įtraukimas į EKA](product.md)

[Rekomendacijų įtraukimas į operacijų ekraną](add-recommendations-control-pos-screen.md)

[Kuruojamų rekomendacijų kūrimas rankiniu būdu](create-editorial-recommendation-lists.md)

[Rekomendacijų su demonstraciniais duomenimis kūrimas](product-recommendations-demo-data.md)

[DUK apie produktų rekomendacijas](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]