--- 
title: "Registruoti prekės, kurios pagrindinė sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą"
description: "Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai modulyje Atsargų valdymas naudojate „pagrindinį sandėliavimą‟."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 1c367ebcd57fc2dd534587aa96349e48756c1bb6
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a>Registruoti prekės, kurios pagrindinė sandėliavimo funkcija įjungta, prekes naudojant prekių gavimo žurnalą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra jums parodo, kaip registruoti prekes, naudojant prekių gavimo žurnalą, kai modulyje Atsargų valdymas naudojate „pagrindinį sandėliavimą‟. Paprastai tai atlieka gavimo klerkas. Galite vykdyti šią procedūrą demonstracinių duomenų įmonėje USMF, naudodami rodomas pavyzdines reikšmes.  Jei nenaudojate USMF, prieš pradėdami šį vadovą turite turėti patvirtintą pirkimo užsakymą su atidaryta pirkimo užsakymo eilute. Prekė eilutėje turi būti laikoma atsargose, nenaudoti produktų variantų ir neturėti sekimo dimensijų. Taip pat prekės turi būti susietos su saugojimo dimensijų grupe, kurioje aktyvūs teritorija ir sandėlis.


## <a name="create-item-arrival-journal-header"></a>Kurti prekių gavimo žurnalo antraštę
1. Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekių gavimas > Prekių gavimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
    * Jei naudojate USMF, galite surinkti WHS. Jei naudojate kitus duomenis, žurnalas, kurio pavadinimą pasirinkote, turi turėti toliau nurodytas ypatybes: Tikrinti paėmimo vietą turi būti nustatyta į Ne ir Sulaikymo valdymas turi būti nustatyta į Ne.  
4. Lauke Važtaraštis surinkite reikšmę.
    * Tai yra važtaraščio ID iš tiekėjo išduoto važtaraščio. Pridėkite unikalų numerį.  
5. Lauke Numeris pasirinkite pirkimo užsakymą.
6. Spustelėkite GERAI.

## <a name="add-lines-to-item-arrival-journal"></a>Į prekių gavimo žurnalą pridėti eilučių
1. Spustelėkite Funkcijos.
2. Spustelėkite Kurti eilutes.
    * Į šį žurnalą eilutes galima įvesti rankiniu būdu arba sukurti automatiškai. Bus parodyta, kaip sukurti automatiškai.  
3. Pažymėkite arba atžymėkite žymės langelį Inicijuoti kiekį.
    * Kiekis žurnalo eilutėse bus inicijuojamas su kiekiu, neužregistruotu pirkimo užsakymo eilutėje.  
4. Spustelėkite GERAI.

## <a name="post-the-journal"></a>Registruoti žurnalą
1. Spustelėkite Registruoti.
2. Spustelėkite GERAI.

## <a name="generate-the-product-receipt"></a>Generuoti produkto gavimo kvitą
1. Spustelėkite Funkcijos.
2. Spustelėkite Produkto gavimo kvitas.
3. Spustelėkite GERAI.


