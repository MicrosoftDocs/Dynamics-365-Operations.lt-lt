---
title: "Sumažinti vertės nusidėvėjimas"
description: "Šiame straipsnyje apžvelgtas nusidėvėjimo Mažėjančios vertės metodas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: 0dede1cabccf672475ea242f05d5de06dc8e78c5
ms.lasthandoff: 03/31/2017


---

# <a name="reduce-balance-depreciation"></a>Sumažinti vertės nusidėvėjimas

Šiame straipsnyje apžvelgtas nusidėvėjimo Mažėjančios vertės metodas.

Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio Nusidėvėjimo šablonai lauke Metodas pasirinkus Mažėjantis balansas, šiam nusidėvėjimo šablonui priskirto turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu.

Norėdami nustatyti mažėjančio balanso nusidėvėjimą, turite pasirinkti ir puslapio Nusidėvėjimo šablonai „FastTab“ skirtuko Bendra laukuose. Pirmiausia lauke Nusidėvėjimo metai pasirinkite metus. Priklausomai nuo jūsų pasirinkimo, lauke Laikotarpio dažnis atsiranda kitos pasirinktys, kaip paaiškinta kituose skyriuose. 

Taip pat turite įvesti nusidėvėjimo profilio lauko Procentas reikšmę. Pasirinkus pasirinktį Visiškas nusidėvėjimas, likęs nusidėvėjimo pagrindas paimamas iš paskutinio nusidėvėjimo laikotarpio ir gali sudaryti didelę sumą. Kai kurios šalys / regionai nenaudoja perjungimo į tiesią eilutę metodo. Perjungimas įvyksta, kai alternatyvaus nusidėvėjimo metodo suma didesnė arba lygi pirminio nusidėvėjimo šablono sumai ir nusidėvėjimo suma yra alternatyvaus metodo suma. 

Kadangi turtas, remiantis procentinės išraiškos apskaičiavimais, niekada visiškai nenusidėvės, norėdami, kad būtų įvykdytas visiškas turto nusidėvėjimas, turite pasirinkti pasirinktį Visiškas nusidėvėjimas.

## <a name="select-a-depreciation-year"></a>Pasirinkti nusidėvėjimo metus.
Puslapio Nusidėvėjimo šablonai lauke Nusidėvėjimo metai galite pasirinkti Kalendorius arba Finansiniai metai. Nuo jūsų pasirinkimo priklausys, kokios pasirinktys bus galimos lauke Laikotarpio dažnis. Numatytoji pasirinktis yra Kalendorius.

### <a name="calendar"></a>Kalendorius

Pasirinktis Kalendorius kasmet sausio 1 d. atnaujina nusidėvėjimo pagrindą (paprastai tai būna suma, gauta iš balansinės vertės atėmus likvidacinę vertę). Toliau šioje temoje pateiktame mažėjančio balanso nusidėvėjimo pavyzdyje nusidėvėjimo pagrindas yra stulpelyje Skaičiavimas nurodytas pirmos skaičiavimo išraiškos skaitiklis. 

Jei pasirinksite Kalendorius, lauke Laikotarpio dažnis galimos toliau nurodytos pasirinktys, nurodančios kalendorinių metų faktines nusidėvėjimo registravimo datas ir sumas.

-   Kasmet registruojama gruodžio 31 d.
-   Kas mėnesį mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.
-   Kas ketvirtį ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).
-   Kas pusmetį pusmečio suma yra registruojama kiekvieno kalendorinio pusmečio pabaigoje (birželio 30 d. ir gruodžio 31 d.).
-   Kasdien registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.

Pavyzdžiui, jei pasirenkate Kasmet, metinis nusidėvėjimas registruojamas tik vieną kartą, kiekvienų metų gruodžio 31 d. Jei pasirenkate Kas mėnesį, mėnesisnis nusidėvėjimas registruojamas kiekvieną mėnesį kaip 1/12 metinio nusidėvėjimo sumos dalis.

### <a name="fiscal"></a>Finansiniai

Lauke Nusidėvėjimo metai pasirinkus Finansiniai metai, naudojamas tiesios eilutės nusidėvėjimo metodas. Jis apskaičiuojamas remiantis finansiniais metais, kurie nustatomi puslapyje Didžioji knyga pasirinkto finansinio kalendoriaus puslapyje Finansinių metų kalendoriai. Pvz., finansinių metų liepos 1 d. iki birželio 30 d., nusidėvėjimo skaičiavimo prasideda liepos 1 d. Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių. Koreguojamas kiekvieno ataskaitinio laikotarpio nusidėvėjimas. Kitų finansinių metų ilgis priklauso nuo ataskaitinių laikotarpių, kuriuos nustatote, kai puslapyje Finansiniai kalendoriai kuriate naujus finansinius metus.


Pasirinkus Finansiniai metai, lauke Laikotarpio dažnis galimos šios pasirinktys:

-   Kasmet bendroji finansinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę finansinių metų dieną.
-   Ataskaitinis laikotarpis – registruojama bendroji finansinių metų nusidėvėjimo suma, paskirstyta į ataskaitinius laikotarpius, kurie nurodomi pagal puslapyje Didžioji knyga pasirinktą finansinį kalendorių arba pagal pasirinktą ilgalaikio turto knygos kalendorių.

## <a name="example-of-reducing-balance-depreciation"></a>Mažėjančios vertės nusidėvėjimo pavyzdys

Tarkime, kad ilgalaikio turto įsigijimo kaina yra 11 000, likvidacinė vertė yra 1000, o nusidėvėjimo procento koeficientas yra 30. 

Naudojant metodą Mažėjanti vertė, 30 procentų nusidėvėjimo pagrindo (iš balansinės vertės atėmus likvidacinę vertę) yra apskaičiuojami ankstesnio nusidėvėjimo laikotarpio pabaigoje. Pirmų trijų metų nusidėvėjimas rodomas toliau pateikiamoje lentelėje.

| Laikotarpis | Metinio nusidėvėjimo sumos skaičiavimas | Balansinės vertė metų pabaigoje |
|--------|-------------------------------------------|---------------------------------------|
| 1 metai | (11,000 - 1,000) \* 30% = 3,000           | (11 000 - 1000) - 3000 = 7000      |
| 2 metai | (7,000 - 1,000) \* 30% = 1,800            | (7000 -1800) = 5200                |
| 3 metai | (5,200 - 1,000) \* 30% = 1,260            | (5200 - 1260) = 3940               |

 
-




