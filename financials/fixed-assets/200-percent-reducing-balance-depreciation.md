---
title: "200 procentų mažėjančios vertės metodas"
description: "Šiame straipsnyje apžvelgiamas 200 % nusidėvėjimo mažėjančios vertės metodas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 617d643517f4c40d6e870d1e7e676b0be28092dd
ms.lasthandoff: 03/31/2017


---

# <a name="200-percent-reducing-balance-depreciation"></a>200 procentų mažėjančios vertės metodas

Šiame straipsnyje apžvelgiamas 200 % nusidėvėjimo mažėjančios vertės metodas.

Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirinkus reikšmę **200 % mažėjanti vertė**, šiam nusidėvėjimo šablonui priskirto ilgalaikio turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu. Procentas apskaičiuojamas remiantis ilgalaikio turto dėvėjimo laiku. Pavyzdžiui, jei turto dėvėjimo laikas yra penkeri metai, apskaičiuotas procentas yra 40 procentai (200 % ÷ 5). 

Šis metodas dar vadinamas dvigubos mažėjančios vertės metodu.

Norėdami nustatyti 200 % mažėjančios metodą, taip pat turite pasirinkti puslapio **Nusidėvėjimo šablonai** laikų **Nusidėvėjimo metai** ir **Laikotarpio dažnis** parinktis. Pasirinktys, prieinamos lauke **Laikotarpio dažnis** skiriasi atsižvelgiant į vertę, pasirinktą lauke **Nusidėvėjimo metai**.

## <a name="select-a-depreciation-year"></a>Pasirinkite nusidėvėjimo metus.
Puslapio **Nusidėvėjimo profiliai** lauke **Nusidėvėjimo metai** galite pasirinkti **Kalendoriniai** arba **Ataskaitiniai**. Numatytoji reikšmė yra **Kalendoriniai**. 

Jūsų pasirinktimi nustatoma, kokios parinktys bus galimos lauke **Laikotarpio dažnis**. Šiame lauke apibrėžiamos kalendorinių metų faktinės nusidėvėjimo registravimo datos ir sumos.

### <a name="calendar"></a>Kalendorius

**Nusidėvėjimo metų** lauke galite palikti numatytąją reikšmę – **Kalendoriniai**. 

Parinktimi **Kalendoriniai** nusidėvėjimo pagrindas atnaujinamas kiekvienų metų sausio 1 d. Paprastai, nusidėvėjimas yra grynosios buhalterinės vertės atėmus likvidacinę vertę. Toliau šioje temoje pateiktuose pavyzdžiuose nusidėvėjimo pagrindas yra skaičiavimų stulpelyje nurodytas pirmos išraiškos skaitiklis. 

Jei kaip nusidėvėjimo metus pasirinksite **Kalendoriniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.

-   Pasirinkus **Kasmet**, suma registruojama gruodžio 31 d.
-   Pasirinkus **Kas mėnesį**, mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.
-   Pasirinkus **Kas ketvirtį**, ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).
-   Pasirinkus **Kas pusmetį**, pusmečio suma yra registruojama kalendorinį pusmetį (birželio 30 d. ir gruodžio 31 d.).
-   Pasirinkus **Kasdien**, registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.

### <a name="fiscal"></a>Finansiniai

Lauke **Nusidėvėjimo metai** pasirinkus parinktį **Finansiniai**, 200 % mažėjančios vertės nusidėvėjimas skaičiuojamas pagal nurodyto knygos finansinio kalendoriaus finansinius metus arba pagal finansinį kalendorių, pasirinktą puslapyje **Didžioji knyga**. Ataskaitiniai kalendoriai nustatomi **Ataskaitinių kalendorių** puslapyje. 

Pvz., finansinių metų liepos 1 d. iki birželio 30 d., nusidėvėjimo skaičiavimo prasideda liepos 1 d. Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių. Koreguojamas kiekvieno laikotarpio nusidėvėjimas. Kitų ataskaitinių metų trukmė nustatoma pagal laikotarpių sąranką puslapyje **Ataskaitiniai kalendoriai**. 

Kai kaip nusidėvėjimo metai pasirinkta **Finansiniai**, galimos šios lauko **Laikotarpio dažnis** parinktys:

-   **Kasmet** apskaičiuota bendroji finansinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę finansinių metų dieną.
-   Pasirinkus **Ataskaitinis laikotarpis**, rodoma apskaičiuota bendroji ataskaitinių metų nusidėvėjimo suma. Ši suma kaupiama per ataskaitinius laikotarpius, apibrėžtus **Ataskaitinių kalendorių** puslapyje.

## <a name="example-of-200-reducing-balance-depreciation"></a>200% mažėjančios vertės nusidėvėjimo pavyzdys
|                                |        |
|--------------------------------|--------|
| Įsigijimo savikaina               | 11 000 |
| Likvidacinė vertė                  | 1000 |
| Nusidėvėjimo pagrindas              | 10.000 |
| Aptarnavimo laikas metais             | 5      |
| Metinio nusidėvėjimo procentas | 40 %    |

Naudojant 200 % mažėjančios vertės metodą, 200 procentų padalijami iš dėvėjimo metų skaičiaus. Kad būtų nustatyta nusidėvėjimo per metus suma, gauta procentinė dalis bus padauginta iš ilgalaikio turto balansinės vertės.

| Laikotarpis | Metinio nusidėvėjimo sumos skaičiavimas | Knygos vertė             | Balansinės vertė metų pabaigoje |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 1 metai | (11 000 – 1000) × 40 % = 4000                | 11 000 – 4000 = 7000 | 11 000 – 1000 – 4000 = 6000        |
| 2 metai | 6000 × 40 % = 2400                           | 7000 – 2400 = 4600  | 6000 – 2400 = 3600                 |
| 3 metai | 3600 × 40 % = 1440                           | 4600 – 1440 = 3160  | 3600 – 1440 = 2160                 |

> [!NOTE] 
> Paprastai, kai suma, kuri apskaičiuojama naudojant 200 % mažėjančios vertės nusidėvėjimo metodas tampa mažesnė nei suma, kuri būtų apskaičiuota naudojant metodą, yra konvertavimo į tiesią eilutę metodo už likusį.


