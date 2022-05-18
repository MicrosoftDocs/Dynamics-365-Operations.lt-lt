---
title: Tiesiogiai proporcingas likutinės vertės nusidėvėjimas
description: Šiame straipsnyje apžvelgiamas tiesiogiai proporcingo likutinės vertės nusidėvėjimo metodas.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92941bc679835d38ba47464452315498a70ce2ee
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726703"
---
# <a name="straight-line-life-remaining-depreciation"></a>Tiesiogiai proporcingas likutinės vertės nusidėvėjimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamas tiesiogiai proporcingo likutinės vertės nusidėvėjimo metodas.

Kai nustatote ilgalaikio turto nusidėvėjimo profilį ir puslapio **Nusidėvėjimo profiliai** lauke **Metodas** pasirenkate **Likęs tiesiogiai proporcingas laikas**, ilgalaikio turto nusidėvėjimas, priskirtas nusidėvėjimo profiliui, bus paremtas likusio tiesiogiai proporcingo turto nusidėvėjimo laiko metodu. Paprastai tai būna ta pati nusidėvėjimo suma kiekvienu nusidėvėjimo laikotarpiu. Norėdami nustatyti likusio tiesiogiai proporcingo laiko nusidėvėjimo metodą, taip pat turite pasirinkti puslapio **Nusidėvėjimo šablonai** laukų **Nusidėvėjimo metai** ir **Laikotarpio dažnis** parinktis. Parinktys, prieinamos lauke **Laikotarpio dažnis** skiriasi atsižvelgiant į reikšmę, pasirinktą lauke **Nusidėvėjimo metai**.

## <a name="select-a-depreciation-year"></a>Pasirinkite nusidėvėjimo metus.
Puslapio **Nusidėvėjimo profiliai** lauke **Nusidėvėjimo metai** galite pasirinkti **Kalendoriniai** arba **Ataskaitiniai**. Numatytoji reikšmė yra **Kalendoriniai**. Jūsų pasirinktimi nustatoma, kokios parinktys bus galimos lauke **Laikotarpio dažnis**. Šiame lauke apibrėžiamos kalendorinių metų faktinės nusidėvėjimo registravimo datos ir sumos.

### <a name="calendar"></a>Kalendorius

Jei renkatės **Kalendorius** laukelyje **_Nebegaliojimo metai_*_ , metai nuo sausio 1 iki gruodžio 31 yra apimami, net jei nustatėte mokestinį kalendorių kitaip. _* Kalendoriaus** parinktis naujina nebegaliojimą nuo kiekvienerių metų sausio 1 dienos. Paprastai nusidėvėjimo pagrindas apskaičiuojamas iš balansinės vertės atėmus likvidacinę vertę. Toliau šioje temoje pateiktame pavyzdyje nusidėvėjimo pagrindas yra skaičiavimų stulpelyje nurodytas pirmos išraiškos skaitiklis. Jei kaip nusidėvėjimo metus pasirinksite **Kalendoriniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.

- Pasirinkus **Kasmet**, suma registruojama gruodžio 31 d.
- Pasirinkus **Kas mėnesį**, mėnesio suma registruojama kiekvieno kalendorinio mėnesio pabaigoje.
- Pasirinkus **Kas ketvirtį**, ketvirčio suma registruojama kiekvieno kalendorinio ketvirčio pabaigoje (kovo 31 d., birželio 30 d., rugsėjo 30 d. ir gruodžio 31 d.).
- Tipo **Kas pusmetį** suma yra registruojama kiekvieno kalendorinio pusmečio pabaigoje (birželio 30 d. ir gruodžio 31 d.).
- Pasirinkus **Kasdien**, registruojama kasdienio nusidėvėjimo metodo nusidėvėjimo suma, kiekvieną dieną naudojant vieną operaciją.

Pavyzdžiui, jei pasirenkate **Kasmet**, metinis nusidėvėjimas registruojamas tik vieną kartą, kiekvienų metų gruodžio 31 d. Jei pasirenkate **Kas mėnesį**, mėnesinis nusidėvėjimas registruojamas kiekvieną mėnesį kaip 1/12 metinio nusidėvėjimo sumos dalis.

### <a name="fiscal"></a>Finansiniai

Lauke **Nusidėvėjimo metai** pasirinkus **Finansiniai metai**, likusio tiesiogiai proporcingo laiko nusidėvėjimo metodas. Nusidėvėjimas skaičiuojamas pagal likusius finansinius metus. Pvz., jei finansiniai metai prasideda 2015 m. liepos 1 d. ir baigiasi 2016 m. birželio 30 d., nusidėvėjimas pradedamas skaičiuoti liepos 1 d. Finansiniai metai gali būti ilgesni arba trumpesni nei 12 mėnesių. Koreguojamas kiekvieno ataskaitinio laikotarpio nusidėvėjimas. Kitų finansinių metų trukmė nustatoma pagal ataskaitinius laikotarpius, kurie nustatomi puslapyje **Finansiniai kalendoriai**. Jei kaip nusidėvėjimo metus pasirinksite **Ataskaitiniai**, galimos toliau nurodytos lauko **Laikotarpio dažnis** parinktys.

- **Kasmet** apskaičiuota bendroji finansinių metų nusidėvėjimo suma registruojama kaip viena suma paskutinę finansinių metų dieną.
- **Ataskaitinis laikotarpis** apskaičiuoja bendrąją finansinių metų nusidėvėjimo sumą. Tada ši suma yra sukaupiama per ataskaitinius laikotarpius, kurie nurodomi nustatyto knygos finansinio kalendoriaus puslapyje **Finansiniai kalendoriai**.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Tiesiogiai proporcingo nepasikeitusio ilgalaikio turto nusidėvėjimo pavyzdys
Toliau nurodytos ilgalaikio turto charakteristikos.

| Laukas               | Reikšmė  |
|:---------------------|--------:|
| Įsigijimo savikaina    | 11,000 |
| Likvidacinė vertė       | 1000  |
| Nusidėvėjimo pagrindas   | 10.000 |
| Aptarnavimo laikas metais  | 5      |
| Metinis nusidėvėjimas | 2 000  |

Nusidėvėjimo suma yra ta pati kiekvienais metais: (įsigijimo išlaidos – likvidacinė vertė) ÷ dėvėjimo laikas metais

| Laikotarpis | Metinio nusidėvėjimo sumos skaičiavimas | Balansinės vertė metų pabaigoje |
|:--------:|:-----------------------------------------------|---------------------------------------:|
| 1 metai | (11 000 – 1 000) ÷ 5 = 2 000                  | 9.000                                 |
| 2 metai | (9 000 – 1 000) ÷ 4 = 2 000                   | 7 000                                 |
| 3 metai | (7 000 – 1 000) ÷ 3 = 2 000                   | 5 000                                 |
| 4 metai | (5 000 – 1 000) ÷ 2 = 2 000                   | 3.000                                 |
| 5 metai | (3 000 – 1 000) ÷ 1 = 2 000                   | 1000                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
