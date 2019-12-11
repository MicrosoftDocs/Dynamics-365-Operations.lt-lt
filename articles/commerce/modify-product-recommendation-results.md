---
title: Tvarkyti AI-ML pagrįstų produktų rekomendacijų rezultatus
description: Šioje temoje paaiškinama, kaip jūsų verslui pritaikyti produkto rekomendacijų rezultatus, pagrįstus dirbtinio intelekto mašininiu mokymu (AI-ML).
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770075"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a>Tvarkyti AI-ML pagrįstų produktų rekomendacijų rezultatus

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip jūsų verslui pritaikyti produkto rekomendacijų rezultatus, pagrįstus dirbtinio intelekto mašininiu mokymu (AI-ML). 

Įjungus produkto rekomendacijas, numatytieji parametrai įsigalios. Šie parametrai bus naudingi arba galės būti naudingi daugeliu atvejų. Geriausia planuoti skirti kažkiek laiko įvertinant, ar rezultatai atitinka produktų pardavimo pasiūlymą. Prieš vėl atliekant bandymą, rekomenduojame įvertinti kelių dienų rezultatus prieš keičiant parametrus. 

## <a name="understanding-recommendation-list-parameters"></a>Rekomendacijų sąrašo parametrų supratimas

Prieš keisdami parametrus, sužinokite, kaip jie paveiks toliau esančius rezultatus.

### <a name="trending-product-list"></a>Populiariausių produktų sąrašas

Produktų sąraše **Populiaru** yra du parametrai, kuriuos galima keisti: ![Sąrašo Populiariu numatytųjų parametrų pavyzdys](./media/exampletrendingparameters.png)
1. **Įtraukti naujų produktų iš paskutinių X dienų** – produktus, įtrauktus į nurodytą dienų skaičių iki esamos datos, galima naudoti renkant produktų kandidatus. Numatytoji paveikslėlio vertė rodo, kad produktai, esantys 180 dienų, gali būti naudojami populiariausių produktų sąraše.
1. **Įtraukti paskutinių X dienų pardavimą** – pardavimo operacijos, įvykusios nurodytame dienų skaičiuje iki esamos datos, galima naudoti užsakant produktų. Pirmiau nurodyta numatytoji vertė rodo, kad visi produkto pirkimai, atlikti per pastarąsias 30 dienų, bus naudojami nustatant produktų išdėstymą populiariausių produktų sąraše. 

### <a name="best-selling-product-list"></a>Perkamiausių produktų sąrašas

Atsižvelgiant į jūsų verslą, perkamiausių produktų rezultatai gali skirtis nuo populiariausių produktų, net jei abiems naudojami operacijų duomenys užsakyti produktų. Kadangi perkamiausi produktai nėra atskiriami pagal asortimento datą, sąraše Perkamiausi vis tiek galima išskirti labai populiarius, senesnius produktus, kurie galbūt nebepatenka į populiariausių sąrašą. 

Produktų sąraše **Perkamiausi** yra vienas parametras, kurį galima pakeisti:

![Sąrašo Perkamiausi numatytojo parametro pavyzdys](./media/examplebestsellingparameters.PNG)
1. **Įtraukti paskutinių X dienų pardavimą** – pardavimo operacijos, įvykusios nurodytame dienų skaičiuje iki esamos datos, galima naudoti užsakant produktų. Pirmiau nurodyta numatytoji vertė rodo, kad visi produkto pirkimai, atlikti per pastarąsias 30 dienų, bus naudojami nustatant produktų išdėstymą produktų sąraše Perkamiausi. 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>Produktų įtraukimas į rekomendacijų sąrašus arba pašalinimas iš jų rankiniu būdu

### <a name="for-new-trending-or-best-selling"></a>Sąrašams Nauja, Populiaru arba Perkamiausi

1.  Eikite į **„Retail“** > **Produktų rekomendacijos** > **Rekomendacijų parametrai**.
1.  Mažmeninės prekybos bendrai naudojamų parametrų sąraše pasirinkite **Rekomendacijų sąrašai**.
1.  Pasirinkite sąrašą, į kurį įtrauksite produktus arba iš kurio juos pašalinsite.
1.  Norėdami prie lentelės pridėti produktų, pasirinkite **įtraukti eilutę**. 
1.  Stulpelyje Produktas suraskite produktą pagal **pavadinimą** arba **produkto numerį.**
![Produkto ieškos sąraše Nauji produktai pavyzdys](./media/examplenewlistconfiguration1.png)
1.  Stulpelyje Eilutės tipas pasirinkite vieną iš dviejų parinkčių:
    -   **Įtraukti** – produktas priverstinai įtraukiamas į sąrašo priekį
    -   **Neįtraukti** – produktas nerodomas sąraše ![Naujų produktų sąrašo įtraukimo ir neįtraukimo pavyzdys](./media/examplenewlistconfiguration2.png)
1.  Pakeitus **Rodymo tvarka**, bus pakeista produktų žymėjimo tvarka ir sąraše pasirodys **įtraukti**.
    - Jei du produktai turi tokią pačią reikšmę **Rodymo tvarka**, tada galutinė tvarka tų dviejų rezultatų gali skirtis nuo esančios įmonės padalinyje.
1.  Norėdami pašalinti produktus iš lentelės, pasirinkite šalintiną eilutę ir pasirinkite **Pašalinti**.


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>Sąrašai Žmonėms, taip pat patiko ar Dažnai kartu perkama

Atsižvelgiant į sąrašus **Dažnai kartu perkama** ir **Žmonės taip pat patiko**, mašininis mokymas yra naudojamas vartotojų pirkimo tendencijoms analizuoti, kad būtų rekomenduojami susiję produktai, kurie paprastai įsigijami kartu su unikaliu pradiniu produktu. 
 
**Pradinis produktas** yra produktas, kuriam norite generuoti rezultatus. Norėdami rankiniu būdu pakoreguoti rekomendacijų sąrašus, įtraukiate šiam produktui rezultatus arba pašalinate juos. 

Atlikite šiuos veiksmus, kad pradiniam produktui rankiniu būdu įtrauktumėte rezultatų arba juos pašalintumėte:
1.  Pasirinkite **Pradinis produktas**. 
1.  Stulpelyje **Produktas** ieškokite produkto pagal **Pavadinimas** arba **Produkto numeris.**
![Produkto ieškos sąraše Dažnai kartu perkama pavyzdys](./media/exampleFBTlistconfiguration1.png)
1. Stulpelyje **Eilutės tipas** pasirinkite vieną iš dviejų parinkčių:
    - **Įtraukti** – produktas priverstinai įtraukiamas į sąrašo priekį
    - **Neįtraukti** – produktas neįtraukiamas ir nerodomas sąraše     
![Produkto, esančio sąraše Dažnai kartu perkama, įtraukimo arba neįtraukimo pavyzdys](./media/exampleFBTlistconfiguration2.png)
1.  Norėdami pašalinti produktus iš lentelės, pasirinkite šalintiną eilutę ir pasirinkite Pašalinti.


## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų rekomendacijų apžvalga](product-recommendations.md)

[Įjungti produktų rekomendacijas](enable-product-recommendations.md)

[ĮProduktų rekomendacijų sąrašų įtraukimas į puslapius](add-reco-list-to-page.md)
