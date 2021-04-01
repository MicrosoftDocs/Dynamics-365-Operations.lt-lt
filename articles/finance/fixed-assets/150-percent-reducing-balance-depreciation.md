---
title: 150 procentų mažėjančios vertės metodas
description: Šiame straipsnyje apžvelgtas 150 % nusidėvėjimo mažėjančios vertės metodas.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4edc868b76d466c41be8036b962730db90eeb68a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249442"
---
# <a name="150-percent-reducing-balance-depreciation"></a>150 procentų mažėjančios vertės metodas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgtas 150 % nusidėvėjimo mažėjančios vertės metodas.

Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirinkus reikšmę **150 % mažėjanti vertė**, šiam nusidėvėjimo šablonui priskirto ilgalaikio turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu. Šis procentas apskaičiuojamas remiantis ilgalaikio turto dėvėjimo laiku. Pavyzdžiui, jei turto dėvėjimo laikas yra penkeri metai, apskaičiuotas procentas yra 30 procentų (150 %÷5). 

Norėdami nustatyti 150 % mažėjančios metodą, taip pat turite pasirinkti puslapio **Nusidėvėjimo šablonai** laikų **Nusidėvėjimo metai** ir **Laikotarpio dažnis** parinktis. Parinktys, prieinamos lauke **Laikotarpio dažnis** skiriasi atsižvelgiant į reikšmę, pasirinktą lauke **Nusidėvėjimo metai**.

## <a name="selection-of-depreciation-year"></a>Nusidėvėjimo metų pasirinkimas
Puslapio **Nusidėvėjimo profiliai** lauke **Nusidėvėjimo metai** galite pasirinkti **Kalendoriniai** arba **Ataskaitiniai**. 

Numatytoji reikšmė yra **Kalendoriniai**. Jūsų pasirinktimi nustatoma, kokios parinktys bus galimos lauke **Laikotarpio dažnis**. Šiame lauke apibrėžiamos kalendorinių metų faktinės nusidėvėjimo registravimo datos ir sumos.

### <a name="calendar"></a>Kalendorius

**Nusidėvėjimo metų** lauke galite palikti numatytąją reikšmę – **Kalendoriniai**. 

Parinktimi **Kalendoriniai** nusidėvėjimo pagrindas atnaujinamas kiekvienų metų sausio 1 d. Paprastai nusidėvėjimo pagrindas apskaičiuojamas iš balansinės vertės atėmus likvidacinę vertę. Toliau šioje temoje pateiktuose pavyzdžiuose nusidėvėjimo pagrindas yra skaičiavimų stulpelyje nurodytas pirmos išraiškos skaitiklis. 

Jei kaip nusidėvėjimo metus pasirinksite **Kalendoriniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.

-   Pasirinkus **Kasmet**, suma registruojama gruodžio 31 d.
-   Pasirinkus **Kas mėnesį**, mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.
-   Pasirinkus **Kas ketvirtį**, ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).
-   Pasirinkus **Kas pusmetį**, pusmečio suma yra registruojama kalendorinį pusmetį (birželio 30 d. ir gruodžio 31 d.).
-   Pasirinkus **Kasdien**, registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.

### <a name="fiscal"></a>Finansiniai

Lauke **Nusidėvėjimo metai** pasirinkus parinktį **Finansiniai**, 150 % mažėjančios vertės nusidėvėjimas skaičiuojamas pagal nurodyto knygos finansinio kalendoriaus finansinius metus arba pagal finansinį kalendorių, pasirinktą puslapyje **Didžioji knyga**. Ataskaitiniai kalendoriai nustatomi **Ataskaitinių kalendorių** puslapyje. 

Pavyzdžiui, jei finansiniai metai prasideda liepos 1 d. ir baigiasi kitų metų birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d. Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių. Koreguojamas kiekvieno laikotarpio nusidėvėjimas. Kitų ataskaitinių metų trukmė nustatoma pagal laikotarpių sąranką puslapyje **Ataskaitiniai kalendoriai**. 

Jei kaip nusidėvėjimo metus pasirinksite **Ataskaitiniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.

-   Pasirinkus **Kasmet**, bendroji ataskaitinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę ataskaitinių metų dieną.
-   Pasirinkus **Ataskaitinis laikotarpis**, rodoma apskaičiuota bendroji ataskaitinių metų nusidėvėjimo suma. Ši suma kaupiama per ataskaitinius laikotarpius, apibrėžtus **Ataskaitinių kalendorių** puslapyje.

## <a name="example-of-150-reducing-balance-depreciation"></a>150% mažėjančios vertės nusidėvėjimo pavyzdys

|                                |        |
|--------------------------------|--------|
| Įsigijimo savikaina               | 11 000 |
| Likvidacinė vertė                  | 1000  |
| Nusidėvėjimo pagrindas              | 10.000 |
| Aptarnavimo laikas metais             | 5      |
| Metinio nusidėvėjimo procentas | 30 %    |

150 % mažinančio balanso metodas padalija 150 procentų iš paslaugų gyvavimo metų. Kad būtų nustatyta nusidėvėjimo per metus suma, gauta procentinė dalis bus padauginta iš ilgalaikio turto balansinės vertės.

| Laikotarpis | Metinio nusidėvėjimo sumos skaičiavimas | Knygos vertė             | Balansinės vertė metų pabaigoje |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 1 metai | (11 000 – 1 000) × 30 % = 3 000                | 11 000 – 3 000 = 8 000 | 11 000 – 1 000 – 3 000 = 7 000        |
| 2 metai | 7 000 × 30 % = 2 100                           | 8 000 – 2 100 = 5 900  | 7 000 – 2 100 = 4 900                 |
| 3 metai | 4 900 × 30 % = 1 470                           | 5 900 – 1 470 = 4 430  | 4 900 – 1 470 = 3 430                 |

> [!NOTE]
> Paprastai, kai suma, kuri apskaičiuojama naudojant 150 % mažėjančios vertės nusidėvėjimo metodą, tampa mažesnė nei suma, kuri būtų apskaičiuota naudojant tiesiogiai proporcingą metodą, visam likusiam laikotarpiui pereinama prie tiesiogiai proporcingo metodo.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]