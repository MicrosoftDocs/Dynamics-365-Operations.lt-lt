---
title: "Tiesiogiai proporcingas nusidėvėjimas"
description: "Šiame straipsnyje apžvelgiamas tiesiogiai proporcingo nusidėvėjimo metodas."
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
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b41901d573e977a89fcd1a7c1ebf7185e162c654
ms.openlocfilehash: ae213018f5aeb24af21d95e4f0fbc1ca8e858fdc
ms.lasthandoff: 03/31/2017


---

# <a name="straight-line-service-life-depreciation"></a>Tiesiogiai proporcingas nusidėvėjimas

Šiame straipsnyje apžvelgiamas tiesiogiai proporcingo nusidėvėjimo metodas.

Kai nustatote ilgalaikio turto nusidėvėjimo šabloną ir puslapio Nusidėvėjimo šablonai lauke Metodas pasirenkate Tiesiogiai proporcingas dėvėjimo laikas, turto, kuriam priskirtas šis nusidėvėjimo šablonas, nusidėvėjimo skaičiavimas bus paremtas bendra turto dėvėjimo laiko trukme. Paprastai tai būna ta pati nusidėvėjimo suma kiekvienu nusidėvėjimo laikotarpiu. 

Nusidėvėjimo sumos skirtumas, apskaičiuotas remiantis tiesiogiai proporcingu dėvėjimo laiko likutinės vertės metodu ir tiesiogiai proporcingu dėvėjimo laiko metodu, atsiranda tuomet, jei yra užregistruotas ilgalaikio turto koregavimas. 

Norėdami nustatyti tiesiogiai proporcingo laiko nusidėvėjimo metodą, taip pat turite pasirinkti puslapio Nusidėvėjimo šablonai laukų Nusidėvėjimo metai ir Laikotarpio dažnis parinktis.

## <a name="select-a-depreciation-year"></a>Pasirinkti nusidėvėjimo metus.
Puslapio Nusidėvėjimo šablonai lauke Nusidėvėjimo metai galite pasirinkti Kalendorius arba Finansiniai metai. Nuo jūsų pasirinkimo priklausys, kokios pasirinktys bus galimos lauke Laikotarpio dažnis. Numatytoji pasirinktis yra Kalendorius.

### <a name="calendar"></a>Kalendorius

Jei pasirenkamas Kalendorius, metais laikomas laikotarpis nuo sausio 1 d. iki gruodžio 31 d., net jei finansinį kalendorių esate nustatę kitaip. 

Pasirinktis Kalendorius kasmet sausio 1 d. atnaujina nusidėvėjimo pagrindą (paprastai tai būna suma, gauta iš balansinės vertės atėmus likvidacinę vertę). Toliau šioje temoje pateiktuose pavyzdžiuose nusidėvėjimo pagrindas yra skaičiavimų stulpelyje nurodytas pirmos išraiškos skaitiklis. 

Jei pasirinksite Kalendorius, lauke Laikotarpio dažnis galimos toliau nurodytos pasirinktys, nurodančios kalendorinių metų faktines nusidėvėjimo registravimo datas ir sumas.
-   Pasirinkus Kasmet, suma registruojama gruodžio 31 d.
-   Kas mėnesį mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.
-   Kas ketvirtį ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).
-   Tipo Kas pusmetį suma yra registruojama kiekvieno kalendorinio pusmečio pabaigoje (birželio 30 d. ir gruodžio 31 d.).
-   Kasdien registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.

Pavyzdžiui, jei pasirenkate Kasmet, metinis nusidėvėjimas registruojamas tik vieną kartą, kiekvienų metų gruodžio 31 d. Jei pasirenkate Kas mėnesį, mėnesisnis nusidėvėjimas registruojamas kiekvieną mėnesį kaip 1/12 metinio nusidėvėjimo sumos dalis.

### <a name="fiscal"></a>Finansiniai

Lauke Nusidėvėjimo metai pasirinkus Finansiniai metai, naudojamas tiesiogiai proporcingo dėvėjimo laiko nusidėvėjimo metodas. Tai apskaičiuojama pagal finansinius metus, apibrėžtus knygos finansiniame kalendoriuje arba puslapyje DK pasirinktame finansiniame kalendoriuje. Finansiniai kalendoriai nustatomi puslapyje Finansiniai kalendoriai.

Pvz., finansinių metų liepos 1 d. iki birželio 30 d., nusidėvėjimo skaičiavimo prasideda liepos 1 d. Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių. Automatiškai koreguojamas kiekvieno ataskaitinio laikotarpio nusidėvėjimas. Kitų finansinių metų ilgis priklauso nuo ataskaitinių laikotarpių, kuriuos nustatote, kai formoje Finansiniai kalendoriai kuriate naujus finansinius metus. 

Pasirinkus Finansiniai metai, lauke Laikotarpio dažnis galimos šios pasirinktys:
-   Kasmet rodoma apskaičiuota bendroji finansinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę finansinių metų dieną.
-   Ataskaitinis laikotarpis apskaičiuoja bendrą finansinių metų nusidėvėjimo sumą, kuri sukaupiama per ataskaitinius laikotarpius, nurodytus finansinio kalendoriaus formoje Finansiniai kalendoriai.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Pavyzdys: tiesiogiai proporcingo nepasikeitusio ilgalaikio turto nusidėvėjimas
Tarkime, kad ilgalaikio turto charakteristikos yra tokios, kaip nurodyta toliau.

|                     |        |
|---------------------|--------|
| Įsigijimo savikaina    | 11 000 |
| Likvidacinė vertė       | 1000  |
| Nusidėvėjimo pagrindas   | 10.000 |
| Aptarnavimo laikas metais  | 5      |
| Metinis nusidėvėjimas | 2 000  |

Kasmet gaunate tą pačią nusidėvėjimo sumą. (Įsigijimo išlaidos – likvidacinė vertė) / dėvėjimo laiko metais

| Laikotarpis | Metinio nusidėvėjimo sumos skaičiavimas | Balansinė vertė metų pabaigoje |
|--------|-------------------------------------------|---------------------------------------|
| 1 metai | (11 000 – 1 000) / 5 = 2 000              | 9000                                 |
| 2 metai | (11 000 – 1 000) / 5 = 2 000              | 7000                                 |
| 3 metai | (11 000 – 1 000) / 5 = 2 000              | 5000                                 |
| 4 metai | (11 000 – 1 000) / 5 = 2 000              | 3.000                                 |
| 5 metai | (11 000 – 1 000) / 5 = 2 000              | 1000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a>Pavyzdys: tiesiogiai proporcingas pasikeitusio turto nusidėvėjimas

Tarkime, kad per 2 metus to paties ilgalaikio turto įsigijimo suma pakoreguojama 4 000. 

Įsigijimo koregavimo dėvėjimo laikas yra toks pat kaip ir ilgalaikio turto dėvėjimo laikas. Jis pradedamas skaičiuoti įsigijus. Metų pabaigoje balansinė vertė išlieka 5 ir atitinka įsigijimo koregavimo balansinę vertę. Laikotarpio nusidėvėjimas apskaičiuojamas taip, kaip parodyta toliau pateiktoje lentelėje.

| Laikotarpis | Metinio nusidėvėjimo sumos skaičiavimas | Balansinės vertė metų pabaigoje |
|--------|-------------------------------------------|---------------------------------------|
| 1 metai | 10 000 / 5 = 2 000                        | 11 000 – 2 000 = 9 000                |
| 2 metai | 4 000 (įsigijimo koregavimas)            | 9 000 + 4 000 =13 000                 |
| 2 metai | 14 000 / 5 = 2 800                        | 13 000 – 2 800 = 10 200               |
| 3 metai | 14 000 / 5 = 2 800                        | 10 200 – 2 800 = 7 400                |
| 4 metai | 14 000 / 5 = 2 800                        | 7 400 – 2 800 = 4 600                 |
| 5 metai | 14 000 / 5 = 2 800                        | 4 600 - 2 800 = 1 800                 |
| 6 metai | Likusių 800\*                           | 1 800 – 800 = 1 000                   |

\*Likusi suma yra mažesnė nei nusidėvėjimo suma, priimamas tik likusios sumos atėmus likvidacinę vertę.




