---
title: "Algalapio pradžios balansų įvedimas"
description: "Temoje aprašomi pradžios balansų įvedimo veiksmai įvedant pajamų kodus, atskaitymus, išmokas ir mokesčius. Ši informacija yra naudinga partneriams perkeliant duomenis naujo algalapio diegimui iš kitos sistemos."
author: kherr
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 911a51e2498800e7ee7b1562b66c56967eef0505
ms.openlocfilehash: e6213d2e01445b78c6d8f98fc6a55f7c551231b5
ms.contentlocale: lt-lt
ms.lasthandoff: 06/19/2017


---

# <a name="enter-payroll-beginning-balances"></a>Algalapio pradžios balansų įvedimas

[!include[banner](../../includes/banner.md)]]

Temoje aprašomi pradžios balansų įvedimo veiksmai įvedant pajamų kodus, atskaitymus, išmokas ir mokesčius. Ši informacija yra naudinga partneriams, kurie perkelia duomenis naujo algalapio diegimui iš kitos sistemos. Kad pasiruoštume pradžios algalapių balansų įvedimui, patikriname šią informaciją:

> * Ar į sistemą įvesti ir pasiekiami darbuotojo įrašai
> * Darbuotojams nustatyti ir priskirti šie duomenys:

> > * Mokėjimo ciklai ir mokėjimo laikotarpiai
> > * Pajamų kodai
> > * Mokesčiai
> > * Išmokos ir atskaitymai

> * Įmonė turėjo pasirinkti datą, nuo kurios galima nustatyti algalapio pradžios balansus.

> * Buvo surinkta informacija apie visas pajamas, išmokas / atskaitymus, išmokos įmokas, darbuotojo mokamus mokesčius ir darbdavio mokamus mokesčius bei sumas nuo metų pradžios iš senesnės versijos sistemos.

Planuodami įvesti pradžios balansus, apsvarstykite, kiek išsamūs duomenys turėtų būti. Dauguma įmonių įveda vieną, konsoliduotą sumą nuo metų pradžios iki dabartinės datos. Tačiau jei reikia išsamesnės informacijos, balansus galima įvesti nurodant ketvirčio pokyčius. Pagal reikalingą informacijos detalumo lygį nustatoma, kiek mokėjimo išrašų reikės rankiniu būdu sukurti kiekvienam darbininkui. Vienai sumai nuo metų pradžios iki dabartinės datos kiekvienam darbuotojui reikia rankiniu būdu sukurti tiktai vieną išrašą. Kad tai atliktumėte, naudokite sumas nuo metų pradžios iki dabartinės datos, pateikiamas ankstesnės sistemos galutinio mokėjimo išraše, kaip naujoje algalapio sistemoje įvestą sumą.

Šiame pavyzdyje parodyta, kaip galite įvesti darbuotojo algalapio pradžios balansus, įskaitant pajamų kodus, išmokas / atskaitymus ir mokesčius. Realioje situacijoje turėtumėte kiekvieno uždarbio kodo, išmokos atskaitymo, išmokos įmokos, darbuotojo mokamo mokesčio ir darbdavio mokamo mokesčio eilutės elementą su įvesta suma nuo metų pradžios iki dabartinės datos. Naudodami šį kodų ir sumų sąrašą, atlikite veiksmus, skirtus rankiniu būdu sukurti pajamų ir mokėjimo išrašą su išjungta apskaita, kad algalapio tikslu galėtumėte perkelti pradžios balansus.  Apskaitą išjungti reikia todėl, kad šis pradžios balanso mokėjimo išrašas nebūtų užregistruotas didžiojoje knygoje. Tai buvo padaryta senesnės versijos sistemoje ir veiks naujojoje sistemoje, jums nustačius pradžios balansus didžiojoje knygoje.

> [!NOTE] 
> Jei norite atkurti tuos pačius toliau pateiktus veiksmus, galite naudoti demonstracinius duomenis. Demonstracinius duomenis galima atsisiųsti PartnerSource

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
| Kiekis         | 1,00        |
| Diapazonas             | 30 000      |
| Skirtukas Eilutės informacija |             |
| Neautomatinis           | (pažymėta)    |

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
> Norint įvesti kiekvieno darbininko algalapio pradžios balansus, labai svarbu kiekvienos pajamų išrašo eilutės skirtuke **Eilutės informacija** pažymėti žymės langelį Rankiniu būdu.

3. Srityje **Veiksmas** spustelėkite **Išleisti pajamų išrašą** JAV – FED – ER – FICA.

4. Srityje **Veiksmas** spustelėkite **Mokėjimo išrašas**, kad atidarytumėte puslapį **Generuoti mokėjimo išrašus** ir nustatykite, kaip nurodyta toliau.

| Laukas              | Vertė     |
|--------------------|-----------|
| Mokėjimo data       | 6/30/2017 |
| Mokėjimo vykdymo tipas   | Neautomatinis    |
| Išjungti apskaitą | (pažymėta)  |

> [!NOTE] 
> Tai galima padaryti, tik kai nustatytas vykdymo tipas yra Rankiniu būdu ir kai vartotojas nori išjungti mokėjimo vykdymo apskaitą.

Spustelėkite **Gerai** ir uždarykite **sistemos pranešimą**.

#### <a name="why-disable-accounting-checkbox-needs-to-be-turned-on-when-generating-pay-statements"></a>Kodėl generuojant mokėjimo išrašus turi būti įjungtas žymės langelis Išjungti apskaitą?
Tai padeda išvengi mokėjimo išrašo eilučių paskirstymo ir užregistravimo didžiojoje knygoje. Juk nenorite užregistruoti šio pradžios balanso mokėjimo išrašo, nes jo reikšmės jau yra didžiojoje knygoje iš senesnės versijos sistemos. Šis balanso įkėlimas naudojamas tiktai ataskaitų teikimo ir apribojimo tikslais.

### <a name="c-create-pay-statements-for-employees"></a>C. Darbuotojų mokėjimo išrašų kūrimas
Sugeneravę mokėjimo išrašus, turinčius pradžios balansus, turite patikrinti, kad mokėjimo išrašuose tiksliai atsispindėtų algalapio duomenys. Taip pat turite rankiniu būdu atnaujinti išmokų ir mokesčių informaciją, kad sutaptų su ankstesnės algalapio sistemos reikšmėmis. Patikrinę, ar sumos iš ankstesnio algalapio sistemos sutampa su dabartinio mokėjimo išrašo sumomis, turite užbaigti mokėjimo išrašus.

1. Atidarykite puslapį **Visi mokėjimo išrašai**.

2. Pažymėkite paskutinį sugeneruotą Michael Redmond mokėjimo išrašą

3. Spustelėkite **Redaguoti**, kad atidarytumėte puslapį **Mokėjimo išrašas**.

4. Atidarykite skirtuką **Išmokų atskaitymai** ir įveskite toliau nurodytą informaciją.

| Laukas                           | Vertė            |
|---------------------------------|------------------|
| Išmoka                         | Atskaitoma suma |
| 401 000 | Dalyvauja              | 3000.00          |
| Dantų gydymas | SubSp                  | 495,00           |
| Išlaidos priklausomojo sveikatos priežiūrai | Dalyvauja | 2500.00          |
| Regėjimas | SupSp                  | 500,00           |

5. Skirtuke **Išmokų atskaitymai** įveskite toliau nurodytą informaciją. 

| Laukas                           | Vertė            |
|---------------------------------|------------------|
| Išmoka                         | Atskaitoma suma |
| 401 000 | Dalyvauja              | 3000.00          |
| Dantų gydymas | SubSp                  | 495,00           |
| Išlaidos priklausomojo sveikatos priežiūrai | Dalyvauja | 2500.00          |
| Regėjimas | SupSp                  | 500,00           |

6. Skirtuke **Išmokų įmokos** įveskite toliau nurodytą informaciją.

| Laukas              | Vertė               |
|--------------------|---------------------|
| Išmoka            | Įnašo suma |
| 401 000 | Dalyvauja | 3000,00             |
| Dantų gydymas | SubSp     | 495,00              |
| Regėjimas | SubSp     | 500,00              |

7. Skirtuke **Mokesčių atskaitymai** įveskite toliau nurodytą informaciją.

| Laukas           | Vertė            |
|-----------------|------------------|
| Mokesčio kodas        | Atskaitoma suma |
| JAV – FED – ER – FICA | 1600.00          |
| JAV – FED – ER – MEDI | 825.75           |

8. Skirtuke **Mokesčių įmokos** įveskite toliau nurodytą informaciją.

9. Spustelėkite **Skaičiuoti**.
> [!IMPORTANT] 
> Patikrinkite bendrąsias mokėjimo išrašo sumas, kad jos atitiktų darbininko sumas nuo metų pradžios iki dabartinės datos iš senesnės versijos sistemos. Galbūt prieš pereidami prie kito veiksmo norėsite stabtelėti ir atlikti bendrą visų mokėjimo išrašų patikrinimą. Patikrinę, peržiūrėkite visus mokėjimo išrašus ir juos užbaikite.

Tą patį procesą prireikus galima atlikti ketvirčio pokyčių atžvilgiu visiems ankstesniems kiekvienų metų ketvirčiams. Šito reikia tik tada, jei klientui reikia peržiūrėti duomenis pagal ketvirtį negrįžtant prie ankstesnės versijos sistemos.

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a>Jei suklysite įvesdami pradžios balansus darbuotojui
Galima atšaukti ir iš naujo įvesti operacijas. Norėdami atšaukti operaciją, turite atlikti toliau nurodytus veiksmus puslapyje **Visi mokėjimo išrašai**.

1. Spustelėkite **Atšaukti**.

2. Spustelėkite **Taip**, kai rodomas šis pranešimas: „Atšaukus šį mokėjimo išrašą, norint jį patikslinti, bus sukurtas atšaukimo mokėjimo išrašas Nei vieno iš šių mokėjimo išrašų redaguoti negalima. Ar norite atšaukti šį mokėjimo išrašą?“ rodomas. 

Atšaukę mokėjimo išrašą, galite darbininkui sugeneruoti naują mokėjimo išrašą iš pajamų išrašo, kurį anksčiau sukūrėte vadovaudamiesi anksčiau šioje temoje pateikta procedūra „Pajamų išrašų ir mokėjimo išrašų, kurie turi pradžios balansus, generavimas“. Prieš generuodami naują mokėjimo išrašą, įsitikinkite, kad ištaisėte neteisingas pajamų išrašo eilutes, tada pakartokite šioje temoje aprašytą procedūrą „Mokėjimo išrašų, kurie turi išmokų ir mokesčių pradžios balansus, naujinimas“.

