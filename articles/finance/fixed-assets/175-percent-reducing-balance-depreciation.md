---
title: 175 proc. mažėjančios vertės nusidėvėjimas
description: Šiame straipsnyje pateikiama 175 procentų mažėjančios vertės nusidėvėjimo metodo apžvalga.
author: moaamer
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68c10a1fe221731f7304fc0da92ed314b66dc13f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870197"
---
# <a name="175-percent-reducing-balance-depreciation"></a>175 proc. mažėjančios vertės nusidėvėjimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama 175 procentų mažėjančios vertės nusidėvėjimo metodo apžvalga.

Nustačius ilgalaikio turto nusidėvėjimo šabloną ir puslapio **Nusidėvėjimo šablonai** lauke **Metodas** pasirinkus reikšmę **175 % mažėjanti vertė**, šiam nusidėvėjimo šablonui priskirto ilgalaikio turto nusidėvėjimo procentas yra toks pat kiekvienu nusidėvėjimo laikotarpiu. 

Norėdami nustatyti 175 % mažėjančios metodą, taip pat turite pasirinkti puslapio **Nusidėvėjimo šablonai** laikų **Nusidėvėjimo metai** ir **Laikotarpio dažnis** parinktis. Parinktys, prieinamos lauke **Laikotarpio dažnis** skiriasi atsižvelgiant į reikšmę, pasirinktą lauke **Nusidėvėjimo metai**.

## <a name="select-a-depreciation-year"></a>Pasirinkite nusidėvėjimo metus.
Puslapio **Nusidėvėjimo profiliai** lauke **Nusidėvėjimo metai** galite pasirinkti **Kalendoriniai** arba **Ataskaitiniai**. Numatytoji reikšmė yra **Kalendoriniai**. 

Jūsų pasirinktimi nustatoma, kokios parinktys bus galimos lauke **Laikotarpio dažnis**. Šiame lauke apibrėžiamos kalendorinių metų faktinės nusidėvėjimo registravimo datos ir sumos.

### <a name="calendar"></a>Kalendorius

**Nusidėvėjimo metų** lauke galite palikti numatytąją reikšmę – **Kalendoriniai**. 

Parinktimi **Kalendoriniai** nusidėvėjimo pagrindas atnaujinamas kiekvienų metų sausio 1 d. Paprastai nusidėvėjimo pagrindas apskaičiuojamas iš balansinės vertės atėmus likvidacinę vertę. Toliau šiame straipsnyje pateiktiuose pavyzdžiuose nusidėvėjimo pagrindas yra stulpelyje Skaičiavimas, nurodytas pirmos skaičiavimo išraiškos skaitiklis. 

Jei kaip nusidėvėjimo metus pasirinksite **Kalendoriniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.

-   Pasirinkus **Kasmet**, suma registruojama gruodžio 31 d.
-   Pasirinkus **Kas mėnesį**, mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.
-   Pasirinkus **Kas ketvirtį**, ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).
-   Pasirinkus **Kas pusmetį**, pusmečio suma yra registruojama kalendorinį pusmetį (birželio 30 d. ir gruodžio 31 d.).
-   Pasirinkus **Kasdien**, registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.

### <a name="fiscal"></a>Finansiniai

Lauke **Nusidėvėjimo metai** pasirinkus parinktį **Finansiniai**, 175 % mažėjančios vertės nusidėvėjimas skaičiuojamas pagal nurodyto knygos finansinio kalendoriaus finansinius metus arba pagal finansinį kalendorių, pasirinktą puslapyje **Didžioji knyga**. Ataskaitiniai kalendoriai nustatomi **Ataskaitinių kalendorių** puslapyje. Daugiau informacijos rasite [Ataskaitiniai kalendoriai, ataskaitiniai metai ir laikotarpiai](../budgeting/fiscal-calendars-fiscal-years-periods.md).

Pavyzdžiui, jei finansiniai metai prasideda liepos 1 d. ir baigiasi kitų metų birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d. Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių. Kiekvieno laikotarpio nusidėvėjimas koreguojamas automatiškai, o kitų ataskaitinių metų trukmė nustatoma pagal puslapyje **Ataskaitiniai kalendoriai** nustatytus laikotarpius. 

Jei kaip nusidėvėjimo metus pasirinksite **Ataskaitiniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.

-   Pasirinkus **Kasmet**, bendroji ataskaitinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę ataskaitinių metų dieną.
-   **Ataskaitinis laikotarpis** apskaičiuoja bendrąją ataskaitinių metų nusidėvėjimo sumą. Ši suma kaupiama per ataskaitinius laikotarpius, apibrėžtus **Ataskaitinių kalendorių** puslapyje.

## <a name="example-of-175-reducing-balance-depreciation"></a>175% mažėjančios vertės nusidėvėjimo pavyzdys

| Laukas                          | Reikšmė  |
|--------------------------------|--------|
| Įsigijimo savikaina               | 11,000 |
| Likvidacinė vertė                  | 1000  |
| Nusidėvėjimo pagrindas              | 10.000 |
| Aptarnavimo laikas metais             | 5      |
| Metinio nusidėvėjimo procentas | 35 %    |

175 % mažinančio balanso nusidėvėjimo metodas padalija 175 procentų iš paslaugų gyvavimo metų. Kad būtų nustatyta nusidėvėjimo per metus suma, gauta procentinė dalis bus padauginta iš ilgalaikio turto balansinės vertės.

| Laikotarpis | Metinio nusidėvėjimo sumos skaičiavimas | Knygos vertė                  | Balansinės vertė metų pabaigoje |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| 1 metai | (11,000 – 1,000) × 35% = 3,500                | 11,000 – 3,500 = 7,500      | 11,000 – 1,000 – 3,500 = 6,500        |
| 2 metai | 6,500 × 35% = 2,275                           | 7,500 – 2,275 = 5,225       | 6,500 – 2,275 = 4,225                 |
| 3 metai | 4,225 × 35% = 1,478.75                        | 5,225 – 1,478.75 = 3,746.25 | 4,225 – 1,478.75 = 2,746.25           |

> [!NOTE] 
> Paprastai, kai suma, kuri apskaičiuojama naudojant 175 % mažėjančios vertės nusidėvėjimo metodą, tampa mažesnė nei suma, kuri būtų apskaičiuota naudojant tiesiogiai proporcingą metodą, visam likusiam laikotarpiui pereinama prie tiesiogiai proporcingo metodo.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
