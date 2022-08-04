---
title: Registruoti prekes, įgalintas sandėlio valdymo procesams, naudojant prekių gavimo žurnalą
description: Šiame straipsnyje pateikiamas scenarijus, kuris parodo, kaip registruoti prekes naudojant prekių gavimo žurnalą, kai naudojate sandėlio valdymo procesus (WMS).
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5241c982675d6b9a9bc9596b8ac9ed2798903287
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066974"
---
# <a name="register-items-enabled-for-warehouse-management-processes-using-an-item-arrival-journal"></a>Registruoti prekes, įgalintas sandėlio valdymo procesams, naudojant prekių gavimo žurnalą

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje pateikiamas scenarijus, kuris parodo, kaip registruoti prekes naudojant prekių gavimo žurnalą, kai naudojate sandėlio valdymo procesus (WMS). Paprastai tai atlieka gavimo klerkas.

## <a name="enable-sample-data"></a>Duomenų pavyzdžių įgalinimas

Norėdami dirbti naudodami šiame straipsnyje nurodytus pavyzdinius įrašus ir reikšmes, turite naudoti sistemą, kurioje įdiegti standartiniai demonstraciniai duomenys, *ir prieš pradėdami turite pasirinkti USMF* juridinį subjektą.

Vietoj to, galite dirbti pagal šį scenarijų pakeisdami reikšmes iš jūsų duomenų, jeigu turite šiuos duomenis:

- Turite patvirtintą pirkimo užsakymą su atvira pirkimo užsakymo eilute.
- Prekė eilutėje turi būti laikoma atsargose. Ji neturi naudoti produkto variantų ir turėti sekimo dimensijų.
- Prekė turi būti susieta su saugojimo dimensijų grupe, kurioje įgalintas sandėlio valdymo procesas.
- Sandėlis, kuris naudojamas, turi būti įgalintas WMS, o vieta, kurią naudojate gaunant, turi būti kontroliuojama pagal numerio lentelę.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Prekių gavimo žurnalo antraštės, naudojančios sandėlio valdymą, kūrimas

Toliau pateikiamas scenarijus rodo, kaip sukurti prekių gavimo žurnalo antraštę, naudojančią sandėlio valdymą:

1. Įsitikinkite, kad jūsų sistemoje yra patvirtintas pirkimo užsakymas, atitinkantis ankstesniame skyriuje nustatytus reikalavimus. Šis scenarijus naudoja įmonės pirkimo užsakymą, skirtą *„USMF”* įmonei, tiekėjo sąskaitai *1001,* sandėliui *51 su* užsakymo eilute, skirta prekės *„M9200”* numerio *10 PL* (10 padėklų).
1. Pasižymėkite pirkimo užsakymo numerį, kurį naudosite.
1. Eikite į **Atsargų valdymas \> Žurnalo įrašai \> Prekių gavimas \> Prekių gavimas**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Atsidaro **Sandėlio valdymo žurnalo kūrimo** dialogo langas. Pasirinkite žurnalo pavadinimą lauke **Pavadinimas**.
    - Jei naudojate *„USMF”* demonstracinius duomenis, pasirinkite *„WHS”*.
    - Jei naudojate savo duomenis, jūsų pasirinktame žurnale **Tikrinti paėmimo vietą** turi būti nustatyta į *Ne* ir **Sulaikymo valdymas** taip pat nustatytas į *Ne*.
1. Nustatykite **Nuoroda** į *Pirkimo užsakymas*.
1. Nustatykite **Paskyros numeris** į *„1001”*.
1. Nustatykite **Numeris** į pirkimo užsakymo, kurį nurodėte šiam pratimui, numerį.

    ![Prekių pristatymo žurnalas.](../media/item-arrival-journal-header.png "Prekių gavimo žurnalas")

1. Pasirinkite **Gerai** žurnalo antraštės sukūrimui.
1. Skyriuje **Žurnalo eilutės** pasirinkite **Įtraukti eilutę** ir įveskite šiuos duomenis:
    - **Prekės numeris** – Nustatykite į *„M9200”*. **Saitas**, **Sandėlis** ir **Kiekis** bus nustatyti pagal atsargų operacijos duomenis 10 padėklų (1000 vnt.).
    - **Vieta** – Nustatykite į *„001”*. Ši konkreti vieta neseka numerio lentelių.

    ![Prekių gavimo žurnalo eilutė.](../media/item-arrival-journal-line.png "Prekių gavimo žurnalo eilutė")

    > [!NOTE]
    > Lauke **Data** nurodoma data, kada atsargose bus užregistruotas turimas šios prekės kiekis.  
    >
    > Lauką **Partijos ID** užpildys sistema, jei jį galima identifikuoti pagal pateiktą informaciją. Kitu atveju turėsite įvesti jį patys. Tai yra būtinasis laukas, kuris susieja šią registraciją su konkrečia šaltinio dokumento eilute.  

1. Pasirinkite **Patvirtinti** veiksmų srityje. Patikrinama, ar žurnalas parengtas registruoti. Jei patikrinti nepavyksta, norint registruoti žurnalą reikia ištaisyti klaidas.  
1. Atsidaro **Tikrinti žurnalą** dialogo langas. Pasirinkite **Gerai**.
1. Peržiūrėkite pranešimų juostą. Ten turėtų būti pranešimas apie tai, kad operacija baigta.  
1. Veiksmų srityje pasirinkite **Skelbti**.
1. Atsidaro **Skelbti žurnalą** dialogo langas. Pasirinkite **Gerai**.
1. Peržiūrėkite pranešimų juostą. Ten turėtų būti pranešimai apie tai, kad operacija baigta.
1. Veiksmų srityje pasirinkite **Funkcijos > Produkto gavimo kvitas** tam, kad atnaujintumėte pirkimo užsakymo eilutę ir užregistruotumėte produkto gavimo kvitą.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
