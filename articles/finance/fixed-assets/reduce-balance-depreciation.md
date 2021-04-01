---
title: Mažėjančio balanso nusidėvėjimas
description: Šiame straipsnyje apžvelgtas nusidėvėjimo Mažėjančios vertės metodas.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69228aec217826780ceb91771028a6a5a180d037
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220990"
---
# <a name="reduce-balance-depreciation"></a>Mažėjančio balanso nusidėvėjimas

[!include [banner](../includes/banner.md)]

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

Lauke Nusidėvėjimo metai pasirinkus Finansiniai metai, naudojamas tiesios eilutės nusidėvėjimo metodas. Jis apskaičiuojamas remiantis finansiniais metais, kurie nustatomi puslapyje Didžioji knyga pasirinkto finansinio kalendoriaus puslapyje Finansinių metų kalendoriai. Pavyzdžiui, jei finansiniai metai prasideda liepos 1 d. ir baigiasi kitų metų birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d. Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių. Koreguojamas kiekvieno ataskaitinio laikotarpio nusidėvėjimas. Kitų finansinių metų ilgis priklauso nuo ataskaitinių laikotarpių, kuriuos nustatote, kai puslapyje Finansiniai kalendoriai kuriate naujus finansinius metus.


Pasirinkus Finansiniai metai, lauke Laikotarpio dažnis galimos šios pasirinktys:

-   Kasmet bendroji finansinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę finansinių metų dieną.
-   Ataskaitinis laikotarpis – registruojama bendroji finansinių metų nusidėvėjimo suma, paskirstyta į ataskaitinius laikotarpius, kurie nurodomi pagal puslapyje Didžioji knyga pasirinktą finansinį kalendorių arba pagal pasirinktą ilgalaikio turto knygos kalendorių.

## <a name="example-of-reducing-balance-depreciation"></a>Mažėjančios vertės nusidėvėjimo pavyzdys

Tarkime, kad ilgalaikio turto įsigijimo kaina yra 11 000, likvidacinė vertė yra 1000, o nusidėvėjimo procento koeficientas yra 30. 

Naudojant metodą Mažėjanti vertė, 30 procentų nusidėvėjimo pagrindo (iš balansinės vertės atėmus likvidacinę vertę) yra apskaičiuojami ankstesnio nusidėvėjimo laikotarpio pabaigoje. Pirmų trijų metų nusidėvėjimas rodomas toliau pateikiamoje lentelėje.

| Laikotarpis | Metinio nusidėvėjimo sumos skaičiavimas | Balansinės vertė metų pabaigoje |
|--------|-------------------------------------------|---------------------------------------|
| 1 metai | (11 000 - 1 000) \* 30% = 3000           | (11 000 - 1000) - 3000 = 7000      |
| 2 metai | (7000 - 1000) \* 30% = 1800            | (7000 -1800) = 5200                |
| 3 metai | (5200 - 1000) \* 30% = 1260            | (5200 - 1260) = 3940               |


-







[!INCLUDE[footer-include](../../includes/footer-banner.md)]