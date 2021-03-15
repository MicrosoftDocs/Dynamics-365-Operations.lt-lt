---
title: Algalapio pradžios balansų įvedimas
description: Temoje aprašomi pradžios balansų įvedimo veiksmai įvedant pajamų kodus, atskaitymus, išmokas ir mokesčius. Ši informacija yra naudinga partneriams perkeliant duomenis naujo algalapio diegimui iš kitos sistemos.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8443bc5c63a90d80757ab4b7507502497c2aaa69
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797789"
---
# <a name="enter-payroll-beginning-balances"></a>Algalapio pradžios balansų įvedimas

[!include [banner](../../includes/banner.md)]

Temoje aprašomi pradžios balansų įvedimo veiksmai įvedant pajamų kodus, atskaitymus, išmokas ir mokesčius. Ši informacija yra naudinga partneriams, kurie perkelia duomenis naujo algalapio diegimui iš kitos sistemos. Kad pasiruoštume pradžios algalapių balansų įvedimui, patikriname šią informaciją:

- Ar į sistemą įvesti ir pasiekiami darbuotojo įrašai
- Darbuotojams nustatyti ir priskirti šie duomenys:

    - Mokėjimo ciklai ir mokėjimo laikotarpiai
    - Pajamų kodai
    - Mokesčiai
    - Išmokos ir atskaitymai

- Įmonė turėjo pasirinkti datą, nuo kurios galima nustatyti algalapio pradžios balansus.
- Buvo surinkta informacija apie visas pajamas, išmokas / atskaitymus, išmokos įmokas, darbuotojo mokamus mokesčius ir darbdavio mokamus mokesčius bei sumas nuo metų pradžios iš senesnės versijos sistemos.

Planuodami įvesti pradžios balansus, apsvarstykite, kiek išsamūs duomenys turėtų būti. Dauguma įmonių įveda vieną, konsoliduotą sumą nuo metų pradžios iki dabartinės datos. Tačiau jei reikia išsamesnės informacijos, balansus galima įvesti nurodant ketvirčio pokyčius. Pagal reikalingą informacijos detalumo lygį nustatoma, kiek mokėjimo išrašų reikės rankiniu būdu sukurti kiekvienam darbininkui. Vienai sumai nuo metų pradžios iki dabartinės datos kiekvienam darbuotojui reikia rankiniu būdu sukurti tiktai vieną išrašą. Kad tai atliktumėte, naudokite sumas nuo metų pradžios iki dabartinės datos, pateikiamas ankstesnės sistemos galutinio mokėjimo išraše, kaip naujoje algalapio sistemoje įvestą sumą.

Šiame pavyzdyje parodyta, kaip galite įvesti darbuotojo algalapio pradžios balansus, įskaitant pajamų kodus, išmokas / atskaitymus ir mokesčius. Realioje situacijoje turėtumėte kiekvieno uždarbio kodo, išmokos atskaitymo, išmokos įmokos, darbuotojo mokamo mokesčio ir darbdavio mokamo mokesčio eilutės elementą su įvesta suma nuo metų pradžios iki dabartinės datos. Naudodami šį kodų ir sumų sąrašą, atlikite veiksmus, skirtus rankiniu būdu sukurti pajamų ir mokėjimo išrašą su išjungta apskaita, kad algalapio tikslu galėtumėte perkelti pradžios balansus. Apskaitą išjungti reikia todėl, kad šis pradžios balanso mokėjimo išrašas nebūtų užregistruotas didžiojoje knygoje. Tai buvo padaryta senesnės versijos sistemoje ir veiks naujojoje sistemoje, jums nustačius pradžios balansus didžiojoje knygoje.

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a>A. Kaip nustatyti pajamų kodus, kurie bus naudojami algalapių pradžios balansuose

Įvedę algalapio pradžios balansus, įsitikinkite, kad pajamų kodai, kuriuos naudosite, sukonfigūruoti su įjungta parinktimi „Leisti redaguoti pajamų išrašo tarifus“. Tai leis jums rankiniu būdu įvesti sumą iš senesnės versijos sistemos. 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a>B. Pajamų išrašo kūrimas darbuotojui, turinčiam pradžios balansą

Šis veiksmas rankiniu būdu sukuria paskutinio mokėjimo laikotarpio senesnės versijos sistemoje pajamų išrašą kiekvienam darbininkui, ir taip sukuriamos pajamų išrašo eilutės naujoje algalapio sistemoje. Įveskite po vieną eilutę kiekvienam pajamų kodui, sumas nuo metų pradžios iki dabartinės datos ir valandas. Toliau pateikiami pavyzdiniai veiksmai.

1. Atidarykite puslapį **Visi pajamų išrašai** ir spustelėkite **Naujas**.

    Įveskite toliau nurodytą informaciją. 

    | Laukas      | Vertė                 |
    |------------|-----------------------|
    | Darbininkas     | Michael Redmond       |
    | Mokėjimo ciklas  | sm                    |
    | Mokėjimo laikotarpis | 2017.06.16–2017.06.30 |

2. Skirtuke **Pajamų išrašo eilutė** įveskite toliau nurodytą informaciją.

    1 eilutė: skirtukas **Pajamų išrašo eilutė**

    | Laukas            | Vertė       |
    |------------------|-------------|
    | Pajamų kodas    | Reguliarus mokėjimas |
    | Kiekis         | 1.00        |
    | Tarifas             | 30,000      |
    | Skirtukas Eilutės informacija |             |
    | Rankinis           | (pažymėta)    |

    2 eilutė: skirtukas **Pajamų išrašo eilutė**

    | Laukas            | Vertė    |
    |------------------|----------|
    | Pajamų kodas    | Premija    |
    | Kiekis         | 1.0000   |
    | Tarifas             | 4250.00  |
    | Skirtukas Eilutės informacija |          |
    | Neautomatinis           | (pažymėta) |

    3 eilutė: skirtukas **Pajamų išrašo eilutė**

    | Laukas           | Vertė      |
    |-----------------|------------|
    | Pajamų kodas   | Komisiniai |
    | Kiekis        | 1.0000     |
    | Tarifas            | !,299,00   |
    | Tarifas            | 1,299.00   |
    | Skirtukas Eilutės informacija |            |
    | Neautomatinis          | (Pažymėta)   |

    > [!NOTE]
    > Norint įvesti kiekvieno darbininko algalapio pradžios balansus, labai svarbu kiekvienos pajamų išrašo eilutės skirtuko **Eilutės informacija** slankiklį **Neautomatiškai** nustatyti į parinktį **Taip**.

3. Srityje **Veiksmas** spustelėkite **Išleisti pajamų išrašą** JAV – FED – ER – FICA.
4. Srityje **Veiksmas** spustelėkite **Mokėjimo išrašas**, kad atidarytumėte puslapį **Generuoti mokėjimo išrašus** ir nustatykite, kaip nurodyta toliau.

    | Laukas              | Vertė     |
    |--------------------|-----------|
    | Mokėjimo data       | 6/30/2017 |
    | Mokėjimo vykdymo tipas   | Neautomatinis    |
    | Išjungti apskaitą |   Taip     |

    > [!NOTE] 
    > Tai galima padaryti, tik kai nustatytas vykdymo tipas yra Rankiniu būdu ir kai vartotojas nori išjungti mokėjimo vykdymo apskaitą.

    Spustelėkite **Gerai** ir uždarykite **sistemos pranešimą**.

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a>Kodėl generuojant mokėjimo išrašus slankiklis turi būti nustatytas į parinktį Taip?

Slankiklį nustačius į parinktį **Taip**, mokėjimo išrašo eilutės nėra paskirstomos didžiojoje knygoje. DK sumos atnaujintos anksčiau, kai buvo įvesti sąskaitos balansai iš senesnės versijos sistemos. Įvedus algalapio pradžios balansus galima generuoti ataskaitas, apimančias informaciją iš ankstesnių metų, taip pat ataskaitas išmokų ir mokesčių riboms nustatyti.

### <a name="c-create-pay-statements-for-employees"></a>C. Darbuotojų mokėjimo išrašų kūrimas

Sugeneravę mokėjimo išrašus, turinčius pradžios balansus, turite patikrinti, kad mokėjimo išrašuose tiksliai atsispindėtų algalapio duomenys. Taip pat turite rankiniu būdu atnaujinti išmokų ir mokesčių informaciją, kad sutaptų su ankstesnės algalapio sistemos reikšmėmis. Patikrinę, ar sumos iš ankstesnio algalapio sistemos sutampa su dabartinio mokėjimo išrašo sumomis, turite užbaigti mokėjimo išrašus.

1. Atidarykite puslapį **Visi mokėjimo išrašai**.
2. Pažymėkite paskutinį sugeneruotą Michael Redmond mokėjimo išrašą
3. Spustelėkite **Redaguoti**, kad atidarytumėte puslapį **Mokėjimo išrašas**.
4. Atidarykite skirtuką **Išmokų atskaitymai** ir įveskite toliau nurodytą informaciją.

    | Laukas             | Vertė            |
    |-------------------|------------------|
    | Išmoka           | Atskaitoma suma |
    | 401 000              | Dalyvauja      |
    | Dantų gydymas            | SubSp            |
    | Išlaidos priklausomojo sveikatos priežiūrai | Dalyvauja      |
    | Regėjimas            | SupSp            |

5. Skirtuke **Išmokų įmokos** įveskite toliau nurodytą informaciją.

    | Laukas   | Vertė               |
    |---------|---------------------|
    | Išmoka | Įnašo suma |
    | 401 000    | Dalyvauja         |
    | Dantų gydymas  | SubSp               |
    | Regėjimas  | SubSp               |

6. Skirtuke **Mokesčių atskaitymai** įveskite toliau nurodytą informaciją.

    | Laukas           | Vertė            |
    |-----------------|------------------|
    | Mokesčio kodas        | Atskaitoma suma |
    | JAV – FED – ER – FICA | 1600.00          |
    | JAV – FED – ER – MEDI | 825.75           |

7. Skirtuke **Mokesčių įmokos** įveskite toliau nurodytą informaciją.
8. Spustelėkite **Skaičiuoti**.

    > [!IMPORTANT] 
    > Patikrinkite bendrąsias mokėjimo išrašo sumas, kad jos atitiktų darbininko sumas nuo metų pradžios iki dabartinės datos iš senesnės versijos sistemos. Galbūt prieš pereidami prie kito veiksmo norėsite stabtelėti ir atlikti bendrą visų mokėjimo išrašų patikrinimą. Patikrinę, peržiūrėkite visus mokėjimo išrašus ir juos užbaikite.

Tą patį procesą prireikus galima atlikti ketvirčio pokyčių atžvilgiu visiems ankstesniems kiekvienų metų ketvirčiams. Šito reikia tik tada, jei klientui reikia peržiūrėti duomenis pagal ketvirtį negrįžtant prie ankstesnės versijos sistemos.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Jei suklysite įvesdami pradžios balansus darbuotojui

Galima atšaukti ir iš naujo įvesti operacijas. Norėdami atšaukti operaciją, turite atlikti toliau nurodytus veiksmus puslapyje **Visi mokėjimo išrašai**.

1. Spustelėkite **Atšaukti**.
2. Spustelėkite **Taip**, kai rodomas šis pranešimas: „Atšaukus šį mokėjimo išrašą, norint jį patikslinti, bus sukurtas atšaukimo mokėjimo išrašas Nei vieno iš šių mokėjimo išrašų redaguoti negalima. Ar norite atšaukti šį mokėjimo išrašą?“ rodomas. 

Atšaukus mokėjimo išrašą galima generuoti naują darbuotojo mokėjimo išrašą iš anksčiau sukurto pajamų išrašo. Prieš generuojant naują mokėjimo išrašą būtinai ištaisyti neteisingas pajamų išrašo eilutes, o tada generuoti naują mokėjimo išrašą su teisingomis sumomis. 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]