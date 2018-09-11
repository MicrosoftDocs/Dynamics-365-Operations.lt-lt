--- 
title: "Apibrėžti atsargų skaičiavimo procesus"
description: "Ši procedūra, kurdama inventorizacijos grupę ir inventorizacijos žurnalą, apžvelgia pagrindinių atsargų inventorizacijos procesų konfigūraciją."
author: MarkusFogelberg
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountGroup, InventJournalName, InventParameters, EcoResProductDetailsExtended, InventItemLocation, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c14c846c55a3d821945160835817cd4f467deda9
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="define-inventory-counting-processes"></a>Apibrėžti atsargų skaičiavimo procesus

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra, kurdama inventorizacijos grupę ir inventorizacijos žurnalą, apžvelgia pagrindinių atsargų inventorizacijos procesų konfigūraciją. Ji taip pat parodo, kaip įgalinti invetorizavimo strategijas sandėlio ir prekės lygiu. Šias užduotis paprastai turėtų atlikti sandėlio prižiūrėtojas. Būtina turėti keletą esamų išleistų produktų ir sandėlių. Jei naudojate demonstracinių duomenų įmonę, šią procedūrą USMF įmonėje galite vykdyti su bet kokia atsargų preke.


## <a name="create-a-counting-group"></a>Kurti inventorizacijos grupę
1. Pasirinkite Atsargų valdymas > Nustatymas > Atsargų paskirstymas > Inventorizacijos grupės.
2. Spustelėkite Naujas.
3. Lauke Inventorizacijos grupė surinkite reikšmę.
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Inventorizacijos kodas pasirinkite parinktį.
    * Neautomatiškai – įtraukia eilutes kiekvieną kartą vykdant užduotį. Kitaip tariant, jūs nustatote inventorizacijos grupės inventorizacijos intervalą.  Laikotarpis – pasibaigus laikotarpio intervalui įtraukia laikotarpio eilutes į inventorizacijos žurnalą.   Nulis atsargų – jei turimos prekės atsargos pasiekia nulį (0), vykdant užduotį eilutės generuojamos inventorizacijos žurnale. Jei turimos atsargos pasiekia nulį po inventorizacijos, eilutės generuojamos kitą kartą pradėjus inventorizaciją.   Mažiausia – įtraukia eilutes į inventorizacijos žurnalą, jei turimos prekės atsargos lygios arba mažesnės už nurodytą mažiausią kiekį.  
    * Neprivaloma: jei lauke Inventorizacijos kodas nurodėte Laikotarpis, lauke Inventorizacijos laikotarpis turite įvesti laikotarpio intervalą. Intervalų vienetas yra dienos.  
    * Kai vykdote užduotį, kuria inventorizacijos žurnale kuriamos naujos eilutės, jos kuriamos šiame lauke nurodytu intervalu, neatsižvelgiant į tai, kaip dažnai vykdote tą pačią užduotį. Pvz., kai skaičiavimo laikotarpis yra nustatytas į 7 ir žurnalo eilutės paskutinį kartą buvo sugeneruotos ir suskaičiuotos sausio 1 d., jei sausio 5 d. pradedama kita užduotis, dar nebus praėjusios septynios dienos ir todėl žurnale už tą laikotarpio intervalą eilučių nesugeneruota. Jei užduotį iš naujo pradėsite sausio 8 d., laikotarpio eilutės generuojamos inventorizacijos žurnale, nes jau praėjo 7 dienos.  
6. Spustelėkite Įrašyti.

## <a name="create-a-counting-journal-name"></a>Kurti inventorizacijos žurnalo pavadinimą
1. Pasirinkite Atsargų valdymas > Sąranka > Žurnalų pavadinimai > Atsargos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Žurnalo tipas pasirinkite „Inventorizacijos‟.
    * Neprivaloma: jei norite, kad, kuriant inventorizacijos žurnalus, būtų generuojama konkreti kvito ID numeracija, galite pasirinkti kitą kvitų serijos ID. Kvitų serijos kuriamos puslapyje Numeracijos.  
6. Lauke Informacijos lygis pasirinkite parinktį.
    * Tai yra informacijos lygis, taikomas, kai užregistruojamas žurnalas.  
    * Neprivaloma: reikšmę galite keisti lauke Rezervavimas. Tai yra būdas, naudojamas rezervuoti prekėms skaičiuojant.   
    * Rankin. – prekės rezervuojamos rankiniu būdu formoje Rezervavimas.   Automat. – užsakymo kiekis rezervuojamas iš turimų galimos prekės atsargų.   Išskleidimas – rezervavimas yra operacijos bendrojo planavimo dalis.  
7. Spustelėkite Įrašyti.

## <a name="set-standard-counting-journal-name"></a>Nustatyti standartinį inventorizacijos žurnalo pavadinimą
1. Pasirinkite Atsargų valdymas > Nustatymas > Atsargų ir sandėlio valdymo parametrai.
2. Spustelėkite skirtuką Žurnalai.
3. Lauke Inventorizacija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Pasirinkite žurnalą, kurį sukūrėte anksčiau.
    * Šis žurnalas tada bus numatytasis skaičiavimo tipo atsargų žurnalų pavadinimas.  
5. Spustelėkite skirtuką Bendra.
    * Neprivaloma: pasirinkite šią parinktį norėdami inventorizacijos metu prekes blokuoti norint uždrausti atnaujinti važtaraščius, išrinkimo dokumentus ar išrinkimo dokumentų registracijas.  

## <a name="set-the-counting-policy-for-an-item"></a>Nustatyti prekės inventorizacijos strategiją
1. Eikite į Produkto informacijos valdymas > Produktai > Patvirtinti produktai.
2. Sąraše spustelėkite ant produkto, kuriam norite nustatyti inventorizacijos strategijas, prekės numerio saito.
    * Atkreipkite dėmesį, kad reikia pasirinkti prekę, kuri yra sekama atsargose. Atsargose nesančio produkto suskaičiuoti negalima. Jei naudojate USMF demonstracinius duomenis, galite pasirinkti prekę A0001.  
3. Spustelėkite Redaguoti.
4. Perjunkite dalies Valdyti atsargas išplėtimą.
5. Lauke Inventorizacijos grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše spustelėkite ant savo anksčiau sukurtos inventorizacijos grupės.
    * Šis produktas dabar bus įtraukiamas, kai, naudojant šią skaičiavimo grupę, sukuriamos atsargų inventorizacijos žurnalo eilutės.  
7. Spustelėkite Įrašyti.

## <a name="set-the-counting-policy-for-an-item-in-a-specific-warehouse"></a>Nustatyti prekės, esančios konkrečiame sandėlyje, inventorizacijos strategiją
1. Veiksmų srityje spustelėkite Valdyti atsargas.
2. Spustelėkite Sandėlio prekės.
3. Spustelėkite Naujas.
4. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše pasirinkite sandėlį, kuriam norite nustatyti konkrečias inventorizacijos strategijas.
6. Lauke Inventorizacijos grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše pasirinkite inventorizacijos grupę
    * Čia galite pasirinkti konkrečią skaičiavimo grupę, kurią reikėtų taikyti prekei konkrečiame jūsų pasirinktame sandėlyje. Kai tame sandėlyje bus atliekamas skaičiavimas, ši skaičiavimo strategija bus naudojama vietoj prekės bendrosios skaičiavimo strategijos.  
8. Spustelėkite Įrašyti.


