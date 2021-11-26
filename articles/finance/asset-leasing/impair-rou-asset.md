---
title: Naudojimo teise valdomo turto nuvertėjimas
description: Šioje temoje aprašomos funkcijos, kurios įrašo vertės sumažėjimą ir koreguoja apskaitos standartų kodifikavimo temos Nr. 842 (ASC 842) veiklos nuomos turto nusidėvėjimo grafiką.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 816f65cff77339ef8684c0449ed2e5f0762b17a2e22174412d5ea9f2a1a62069
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723828"
---
# <a name="impair-right-of-use-assets"></a>Naudojimo teise valdomo turto nuvertėjimas

[!include [banner](../includes/banner.md)]

Jei naudojimo teise valdomo turto apskaitinė vertė nėra atlygintina, jums gali tekti tikrinti, ar turto vertė sumažėjo. Jei nustatote, kad turto vertė sumažėjo, turto nuoma gali įrašyti vertės sumažėjimą ir atitinkamai koreguoti nusidėvėjimo grafiką. Šioje temoje aprašomos funkcijos, kurios įrašo vertės sumažėjimą ir koreguoja apskaitos standartų kodifikavimo temos Nr. 842 (ASC 842) veiklos nuomos nusidėvėjimo grafiką. Tas pats metodas taikomas ir tarptautinio finansinės atskaitomybės standarto Nr. 16 (IFRS 16) nuomai.

Likęs naudojimo teise valdomo turto likutis bus amortizuotas tiesiogiai, atsižvelgiant į likusių laikotarpių skaičių, nepriklausomai nuo to, ar nuoma buvo klasifikuojama kaip finansinė nuoma pagal IFRS 16, ar veiklos nuoma pagal ASC 842.

## <a name="impair-an-rou-asset"></a>Naudojimo teise valdomo turto nuvertėjimas

1. Atidarykite nuvertėjusią nuomą ir pasirinkite **Knygos**.
2. Veiksmų srityje pasirinkite **Nuvertėjimas**.
3. Pasirodžiusiame dialogo lango lauke **Nuvertėjimo suma** įveskite turto nuvertėjimo sumą. Norėdami sumažinti naudojimo teise valdomą turtą, turite įvesti teigiamą vertę.
4. Lauke **Operacijos data** įveskite datą, nuo kurios turi būti užregistruotas nuvertėjimo įrašas.
5. Lauke **Likę laikotarpiai** įveskite likusį mėnesių skaičių, kurį norite amortizuoti.
6. Įjunkite parametrą **Registruoti**, jei norite, kad sistema automatiškai registruotų nuvertėjimo išlaidų žurnalo įrašą. Jei šis parametras paliekamas išjungtas, sistema sukuria įrašą, bet jo neužregistruoja. Tada galite užregistruoti įrašą puslapyje **Turto nuomos žurnalai**.
7. Norėdami peržiūrėti siūlomą įrašą prieš jį sukurdami arba registruodami, nustatykite parinktį **Peržiūrėti prieš registruojant** į parametrą **Taip**.
8. Nustatykite parinktį **Uždaryti knygą** į parametrą **Taip**, kad uždarytumėte nuomos knygą. Šio veiksmo grąžinti negalima. Įrašų negalima registruoti pagal uždarytą nuomą, o uždarytos nuomos koreguoti negalima.
9. Pasirinkite **Gerai**, norėdami sukurti arba užregistruoti nuvertėjimo įrašą.
10. Norėdami peržiūrėti nuvertėjimo turto nusidėvėjimo grafiką, atidarykite tos nuomos knygos turto nusidėvėjimo grafiką. Dabar turtas nuvertės tiesiogiai per mėnesių, kuriuos įvedėte lauke **Likę laikotarpiai** skaičių.
11. Norėdami peržiūrėti žalos išlaidų žurnalo įrašą, nuvertėjimo nuomos knygos veiklos srityje pasirinkite **Turto nuomos žurnalas**. Sistema sukuria žurnalo įrašą, kuris debetuoja nuvertėjimo išlaidų registravimo sąskaitą ir kreditus nuomos turto registravimo sąskaitoje.
12. Norėdami peržiūrėti naują naudojimo teise valdomo turto balansinę vertę, nuomos knygos veiksmų srityje pasirinkite **Turto operacijos**.

## <a name="example-of-rou-asset-impairment"></a>Naudojimo teise valdomo turto nuvertėjimo pavyzdys

Šiame pavyzdyje nuoma yra nespecializuotas turtas, kuris neperleidžia nuosavybės ar nesuteikia nuomininkui pirkimo galimybės.

### <a name="setup"></a>Sąranka

Toliau esančiose lentelėse rodomos reikšmės, kurios yra nustatytos šio pavyzdžio nuomos skirtukuose **Bendra** ir **Mokėjimo grafiko eilutės**.

**Skirtukas Bendra**

| Laukas                      | Reikšmė            |
|----------------------------|------------------|
| Turto tikroji vertė    | 600,000          |
| Apskaičiuota skolinimosi palūkanų norma | 7 %               |
| Sujungimo intervalas       | Kasmet         |
| Turto naudingo naudojimo laikas (mėnesiais) | 600              |
| Anuiteto tipas               | Įprastas anuitetas |
| Pradžios data          | 2019-01-01       |

**Skirtukas Mokėjimo grafiko eilutės**

| Laukas             | Reikšmė      |
|-------------------|------------|
| Pradžios data        | 2019-01-01   |
| Laikotarpio intervalas   | Mėnesinis    |
| Laikotarpiai           | 120        |
| Pabaigos data          | 2028-12-31 |
| Mokėjimo dažnumas | Kasmet   |
| Mokėjimo suma    | 10,000     |

### <a name="steps"></a>Žingsniai

1. Sukūrę nuomą, kaip anksčiau aprašyta šioje temoje, eikite į nuomos knygą ir patvirtinkite mokėjimo grafiką. Tada registruokite pradinį pripažinimo žurnalo įrašą. Pradinis naudojimo teise valdomo turto ir nuomos įsipareigojimas turėtų būti 70 235,81 USD. Šiame pavyzdyje nuoma buvo klasifikuojama kaip veiklos nuomos pagal ASC 842.
2. Vykdyti paketinio žurnalo procesą tris kartus, kad būtų imituotas trejų metų laikotarpis, skirtas nuomos mokėjimams, palūkanų išlaidoms ir nusidėvėjimo išlaidoms.
3. Baigę vykdyti visas tris paketines užduotis, grįžkite į nuomos knygą ir atidarykite atsakomybės bei turto operacijų lenteles, kad peržiūrėtumėte dabartinę naudojimo teise valdomo turto ir nuomos įsipareigojimo balansinę vertę. Po trejų metų įsipareigojimo vertė turėtų būti maždaug 53 893,00 USD, o turto vertė turėtų būti maždaug 53 893,00 USD. 

    Po trejų metų įmonė patikrina nuvertėjimą ir nustato, kad naudojimo teise valdomas turtas nuvertėjo 35 000 USD. Dabar turite įrašyti šį nuvertėjimą.
    
4. Atidarykite nuomos knygą, tada veiksmų srityje pasirinkite **Nuvertėjimas**.
5. Puslapyje **Nuvertėjimo parametrai** įveskite toliau nurodytą informaciją.

    | Laukas                  | Reikšmė    |
    |------------------------|----------|
    | Nuvertėjimo suma      | 35,000   |
    | Operacijos data       | 2022-01-01 |
    | Likę laikotarpiai      | 84       |
    | Skelbti                   | Taip      |
    | Peržiūrėti prieš registruojant | Ne.       |
    | Uždaryti knygą             | Ne       |

6. Buvo sukurtas ir užregistruotas nuvertėjimo išlaidų žurnalo įrašas. Norėdami jį peržiūrėti, eikite į turto nuomos žurnalą nuomos knygoje. Atkreipkite dėmesį, kad nuvertėjimo suma buvo debetuota į nuvertėjimo išlaidų registravimo sąskaitą, o naudojimo teise valdomo turto registravimo sąskaita buvo kredituota.
7. Norėdami peržiūrėti grynąjį nuvertėjimo poveikį, atidarykite atsakomybės ir turto operacijų lenteles. Atkreipkite dėmesį, kad dėl nuvertėjimo išlaidų sumažėjo naudojimo teise valdomas turtas, bet nuomos įsipareigojimo apskaitinė vertė nepasikeitė.

Šis nuvertėjimas turi dar vieną poveikį, kurį reikia apsvarstyti. Kadangi dabar naudojimo teise valdomo turto suma yra daug mažesnė už nuomos įsipareigojimą, suma turi būti nusidėvėti kitaip nei anksčiau. Tiksliau sakant, turtas dabar apskaičiuojamas tiesiogiai per likusius 84 nuomos mėnesius, pradedant operacijos data.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]