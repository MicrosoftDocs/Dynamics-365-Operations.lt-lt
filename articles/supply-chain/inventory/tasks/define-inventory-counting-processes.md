---
title: Atsargų skaičiavimo procesų apibrėžimas
description: Šiame straipsnyje aprašoma pagrindinių atsargų inventorizacijos procesų konfigūracija, sukuriant inventorizacijos grupę ir inventorizacijos žurnalą.
author: yufeihuang
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb86c99e74dc8251ed48c0b749c0b0ef1ce75e34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879025"
---
# <a name="define-inventory-counting-processes"></a>Atsargų skaičiavimo procesų apibrėžimas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma pagrindinių atsargų inventorizacijos procesų konfigūracija, sukuriant inventorizacijos grupę ir inventorizacijos žurnalą. Ji taip pat parodo, kaip įgalinti inventorizavimo strategijas sandėlio ir prekės lygiu. Šias užduotis paprastai turėtų atlikti sandėlio prižiūrėtojas. Būtina turėti keletą esamų išleistų produktų ir sandėlių. Jei naudojate demonstracinių duomenų įmonę, šią procedūrą USMF įmonėje galite vykdyti su bet kokia atsargų preke.


## <a name="create-a-counting-group"></a>Kurti inventorizacijos grupę
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargos > Inventorizacijos grupės**.
2. Pasirinkite **Naujas**.
3. Naujos eilutės lauke **Inventorizacijos grupė** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Lauke **Inventorizacijos kodas** pasirinkite parinktį.

    - **Rankinis būdas** – apima eilutes kiekvieną kartą, kai vykdote užduotį. Kitaip tariant, jūs nustatote inventorizacijos grupės inventorizacijos intervalą.  
    - **Laikotarpis** – apima laikotarpio eilutes inventorizacijos žurnale, kai laikotarpio intervalas baigėsi.  
    - **Nulis atsargų** – jei turimos atsargos pasiekia nulį (0), eilutės generuojamos inventorizacijos žurnale, kai vykdoma užduotis. Jei turimos atsargos pasiekia nulį po inventorizacijos, eilutės generuojamos kitą kartą pradėjus inventorizaciją.  
    - **Minimumas** – įtraukia eilutes į inventorizacijos žurnalą jei turimos atsargos yra lygios arba mažesnės nei nurodytas minimumas.  
    - Neprivaloma: jei nurodėte parinktį **Laikotarpis** lauke **Inventorizacijos kodas**, turite įvesti laikotarpio intervalą lauke **Inventorizacijos laikotarpis**. Intervalų vienetas yra dienos.  
    - Kai vykdote užduotį, kuria inventorizacijos žurnale kuriamos naujos eilutės, jos kuriamos šiame lauke nurodytu intervalu, neatsižvelgiant į tai, kaip dažnai vykdote tą pačią užduotį. Pavyzdžiui, jei lauke **Inventorizacijos laikotarpis** nustatysite 7, o žurnalo eilutės paskutinį kartą buvo sugeneruotos skaičiavimui sausio 1 d., jei kitą užduotį pradėsite sausio 5 d., kai nepraėjo septynios dienos, eilutės, skirtos tam laikotarpio intervalui, nebus generuojamos žurnale. Jei užduotį iš naujo pradėsite sausio 8 d., laikotarpio eilutės generuojamos inventorizacijos žurnale, nes jau praėjo 7 dienos.  

6. Pasirinkite **Įrašyti**.

## <a name="create-a-counting-journal-name"></a>Kurti inventorizacijos žurnalo pavadinimą
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Žurnalų pavadinimai > Atsargos**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke **Žurnalo tipas** pasirinkite **Inventorizacija**. Neprivaloma: jei norite, kad, kuriant inventorizacijos žurnalus, būtų generuojama konkreti kvito ID numeracija, galite pasirinkti kitą kvitų serijos ID. Kvitų serijos sukuriamos puslapyje **Numeracijos**.  
6. Lauke **Detalumo lygis** pasirinkite parinktį.  

    - Tai yra informacijos lygis, taikomas, kai užregistruojamas žurnalas.  
    - Neprivaloma: reikšmę galite keisti lauke Rezervavimas. Tai yra būdas, naudojamas rezervuoti prekėms skaičiuojant.   
    - **Rankinis būdas** – prekės rezervuojamos rankiniu būdų rezervavimo formoje.  
    - **Automatiškai** – užsakymo kiekis rezervuojamas iš pasiekiamų ir turimų prekės atsargų.   
    - **Išskleidimas** – rezervavimas yra operacijos bendrojo planavimo dalis.  

7. Pasirinkite **Įrašyti**.

## <a name="set-standard-counting-journal-name"></a>Nustatyti standartinį inventorizacijos žurnalo pavadinimą
1. Naršymo srityje eikite į **Moduliai > Atsargų valdymas > Sąranka > Atsargų ir sandėlio valdymo parametrai**.
2. Pasirinkite skirtuką **Žurnalai**.
3. Lauko **Inventorizacija** išplečiamajame meniu pasirinkite anksčiau sukurtą žurnalą. Šis žurnalas bus numatytasis atsargų žurnalų tipo **Inventorizacija** žurnalo pavadinimas.  
4. Pasirinkite skirtuką **Bendra**. Neprivaloma: pasirinkite šią parinktį, kad užrakintumėte prekę, kai vykdomas inventorizacijos procesas, kad išvengtumėte važtaraščių, išrinkimo dokumentų arba išrinkimo dokumento registravimų atnaujinimų.  

## <a name="set-the-counting-policy-for-an-item"></a>Nustatyti prekės inventorizacijos strategiją
1. Naršymo srityje eikite į **Moduliai > Produkto informacijos valdymas > Produktai > Išleisti produktai**.
2. Sąraše pasirinkite produkto, kuriam norite nustatyti inventorizacijos strategijas, prekės numerio nuorodą. Turite pasirinktį atsargose sekamą prekę. Atsargose nesančio produkto suskaičiuoti negalima. Jei naudojate USMF demonstracinius duomenis, galite pasirinkti prekę A0001.  
3. Pasirinkite **Redaguoti**.
4. Perjunkite skyriaus **Valdyti atsargas** išplėtimą.
5. Lauko **Inventorizacijos grupė** išplečiamajame meniu pasirinkite anksčiau sukurtą inventorizacijos grupę. Šis produktas dabar bus įtraukiamas, kai, naudojant šią skaičiavimo grupę, sukuriamos atsargų inventorizacijos žurnalo eilutės.  
6. Pasirinkite **Įrašyti**.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Nustatyti prekės, esančios konkrečiame sandėlyje, inventorizacijos strategiją
1. Veiksmų srityje spustelėkite **Valdyti atsargas**.
2. Pasirinkite **Sandėlio prekės**.
3. Pasirinkite **Naujas**.
4. Lauko **Sandėlis** išplečiamajame meniu pasirinkite sandėlį, kuriam norite nustatyti konkrečias inventorizacijos strategijas.
5. Lauko **Inventorizacijos grupė** išplečiamajame meniu pasirinkite inventorizacijos grupę. Galite pasirinkti konkrečią inventorizacijos grupę, kuri turėtų būti taikoma prekei konkrečiame jūsų išrinktame sandėlyje. Kai tame sandėlyje bus atliekamas skaičiavimas, ši skaičiavimo strategija bus naudojama vietoj prekės bendrosios skaičiavimo strategijos.  
6. Pasirinkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]