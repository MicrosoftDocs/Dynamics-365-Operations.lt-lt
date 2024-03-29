---
title: Dvigubos ataskaitos
description: Šiame straipsnyje pateikiamas pavyzdys, kuriame parodyta, kaip galite įvykdyti tarptautinių finansinių ataskaitų standartinių (IFRS) ataskaitų ir privalomos turto ataskaitų reikalavimus.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9941d0bb251a95a71338c59f6eaa4bb9a505a5b5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886377"
---
# <a name="dual-reporting"></a>Dvigubos ataskaitos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiamas pavyzdys, kuriame parodyta, kaip galite įvykdyti tarptautinių finansinių ataskaitų standartinių (IFRS) ataskaitų ir privalomos turto ataskaitų reikalavimus. Reikia supažindinti su Microsoft Dynamics 365 finansų registravimo sluoksniais, todėl pavyzdį bus lengviau suprasti.

## <a name="example"></a>Pavyzdys

Toliau pateiktame pavyzdyje pateikiama nuomos sutartis pagal privalomųjų ataskaitų reikalavimus, naudojant ir grynaisiais pinigais paremtą metodą, ir IFRS ataskaitų metodus. Įmonė turi sudaryti tris knygas, kad būtų atsižvelgta ir į Italijos įstatymų reikalavimus, ir į IFRS 16 reikalavimus. Vienos knygos reikia dėl IFRS 16, vienos – įstatymų reikalavimams, o dar vienos – tam, kad būtų automatiškai atšaukiami įstatyminiai registravimai. Knygos nustatomos taip, kaip parodyta toliau esančiose lentelėse.

**IFRS 16 knyga**

IFRS 16 knyga nustatoma taip, kad atitiktų IFRS 16 apskaitos standartą. Visi įrašai, užregistruoti šioje knygoje, bus registruojami pasirinktiniame sluoksnyje.

| Pavadinimas / vardas ir (arba) pavardė                                    | aprašymas    |
|-----------------------------------------|----------------|
| Knygos tipas                               | 16-asis TFAS        |
| Knygos aprašymas                        | 16-asis TFAS        |
| Registravimo sluoksnis                           | 1 pasirinktinis sluoksnis |
| Nuomos tipas                              | Finance        |
| Apskaitos sistema                    | 16-asis TFAS        |
| Nuomos termino / naudingo naudojimo laiko nustatymas         | 0,00           |
| Dabartinės vertės / turto tikrosios vertės nustatymas | 0,00           |
| Trumpojo laikotarpio ribinė reikšmė                    | 12             |
| Mažos vertės ribinė reikšmė                     | 5,000.00       |
| Mokėti tiekėjui                           | Ne             |

**Įstatyminė knyga**

Įstatyminė knyga yra grynaisiais pinigais paremta knyga, kai įmonė apskaito nuomos išlaidas kaip grynaisiais pinigais kiekvieną mėnesį mokamą sumą. Ši knyga nesukurs naudojimo teise valdomo turto arba nuomos įsipareigojimo.

| Pavadinimas / vardas ir (arba) pavardė                                    | aprašymas |
|-----------------------------------------|-------------|
| Knygos tipas                               | Įstatyminė   |
| Knygos aprašymas                        | Vietos GAAP  |
| Registravimo sluoksnis                           | Dabartiniai     |
| Nuomos tipas                              | Automatinis   |
| Apskaitos sistema                    | Grynųjų pinigų bazė  |
| Nuomos termino / naudingo naudojimo laiko nustatymas         | 0,00        |
| Dabartinės vertės / turto tikrosios vertės nustatymas | 0,00        |
| Trumpojo laikotarpio ribinė reikšmė                    | 0           |
| Mažos vertės ribinė reikšmė                     | 0           |
| Mokėti tiekėjui                           | Ne          |

**Įstatyminė atšaukimo knyga**

Įstatyminė atšaukimo knyga nustatoma taip pat, kaip įstatyminė knyga.

| Pavadinimas / vardas ir (arba) pavardė                                    | aprašymas                    |
|-----------------------------------------|--------------------------------|
| Knygos tipas                               | Įstatyminė – atšaukimo           |
| Knygos aprašymas                        | Knyga, skirta įstatyminei knygai atšaukti |
| Registravimo sluoksnis                           | 1 pasirinktinis sluoksnis                 |
| Nuomos tipas                              | Automatinis                      |
| Apskaitos sistema                    | Grynųjų pinigų bazė                     |
| Nuomos termino / naudingo naudojimo laiko nustatymas         | 0,00                           |
| Dabartinės vertės / turto tikrosios vertės nustatymas | 0,00                           |
| Trumpojo laikotarpio ribinė reikšmė                    | 0                              |
| Mažos vertės ribinė reikšmė                     | 0                              |
| Mokėti tiekėjui                           | Ne                             |

Šiam pavyzdžiui sukurta nuomos sutartis, kurios parametrai skirtukuose **Bendra** ir **Mokėjimo grafiko eilutės** nurodyti toliau.

**Skirtukas Bendra**

| Laukas                      | Reikšmė            |
|----------------------------|------------------|
| Apskaičiuota skolinimosi palūkanų norma | 5 %               |
| Pradžios data          | 2020-01-01         |
| Nuomos grupė                | Pastatai        |
| Tiekėjas                     | 1001             |
| Turto tikroji vertė    | 245,000          |
| Turto naudingo naudojimo laikas          | 120              |
| Anuiteto tipas               | Įprastas anuitetas |
| Sujungimo intervalas       | Mėnesinis          |

**Skirtukas Mokėjimo grafiko eilutės**

| Laukas             | Reikšmė      |
|-------------------|------------|
| Pradžios data        | 2020-01-01   |
| Laikotarpio intervalas   | Mėnesiai     |
| Laikotarpiai           | 24         |
| Pabaigos data          | 2020-12-31 |
| Mokėjimo dažnumas | Mėnesinis    |
| Mokėjimo suma    | 1000      |

Norėdami apskaityti šią nuomą dviejose sistemose, naudokite dabartinį registravimo sluoksnį ir pasirinktinį registravimo sluoksnį. Šioje lentelėje pateikiamas kiekvieno žurnalo įrašo, kurio reikia norint sąžiningai pateikti kiekvieno ataskaitų standarto finansinius duomenis, pavyzdys. Po to pateikiamas išsamus kiekvieno žurnalo įrašo už pirmą nuomos mėnesį aprašas.

<table>
<thead>
<tr>
<th rowspan='3'>Sąskaitos numeris</th>
<th rowspan='3'>aprašymas</th>
<th colspan='3'>Įstatyminė knyga (dabartinis sluoksnis)</th>
<th rowspan='3'>Dabartinio sluoksnio bendroji suma</th>
<th>Atšaukimo knyga (pasirinktinis sluoksnis)</th>
<th colspan='4'>IFRS 16 knyga (pasirinktinis sluoksnis)</th>
<th rowspan='3'>Dabartinio sluoksnio ir pasirinktinio sluoksnio bendroji suma</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Nuomos išlaidos</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>-1,000.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Banko mokestis</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>PVM išlaidos</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Tarpuskaitos sąskaita</td>
<td>-1,000.00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>-1,000.00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Mokėtinos sumos</td>
<td></td>
<td>–1 008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Naudojimo teise valdomas turtas</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Finansinės nuomos įsipareigojimas</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>–22 794,00</td>
<td>1,000.00</td>
<td>–94,97</td>
<td></td>
<td>–21 888,87</td>
</tr>
<tr>
<td>8</td>
<td>Palūkanų išlaidos</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Grynieji pinigai</td>
<td></td>
<td></td>
<td>–1 008,00</td>
<td>–1 008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>–1 008,00</td>
</tr>
<tr>
<td>10</td>
<td>Likvidavimo išlaidos</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Sukauptas nusidėvėjimas</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>–949,75</td>
<td>–949,75</td>
</tr>
</tbody>
</table>

Kaip nurodyta pirmiau pateiktoje lentelėje, reikia pateikti tris knygas, kad būtų galima deklaruoti ir įstatymines ataskaitas, ir IFRS ataskaitas.

- Įstatyminėje knygoje įrašomas nuomos mokestis pagal dabartinio sluoksnio grynaisiais pinigais paremtą apskaitą.
- Įstatyminėje atšaukimo knygoje atšaukiami įstatyminio žurnalo įrašai.
- IFRS 16 knygoje sukuriami žurnalo įrašai, kurie reikalingi pagal IFRS 16.

Nuomą turite įvesti tik vieną kartą. Tada galite atidaryti puslapį **Knygos**, kad matytumėte visas su nuoma susijusias knygas.

> [!NOTE]
> Kai kuriate knygas, visos trys turi būti susietos su tuo pačiu nuomos įrašu.

Pirmajame žurnalo įraše įrašomos nuomos išlaidos pagal įstatyminę knygą. Mokėjimus galite kurti kaip paketą arba pasirinkdami mokėjimo grafiką įstatyminėje knygoje.

Šiam pavyzdžiui sukurtas tolesnis įstatyminės knygos žurnalo įrašas iš mokėjimų grafiko.

### <a name="lease-payment--1312020--je-100"></a>Nuomos mokestis – 2020-01-31 – JE 100

| Kodo tipas | Sąskaitos numeris | Sluoksnis   | Sąskaitos aprašas | Debetas    | Kreditas   |
|--------------|----------------|---------|---------------------|----------|----------|
| Didžioji knyga       | 1              | Dabartiniai | Nuomos išlaidos       | 1,000.00 |          |
| Didžioji knyga       | 4              | Dabartiniai | Tarpuskaitos sąskaita    |          | 1,000.00 |

Mokėtinų sumų klerkas, naudodamas standartines „Dynamics 365“ funkcijas, sukuria sąskaitą faktūrą, skirtą sumokėti už nuomą nenaudojant turto nuomos funkcijos. Tačiau, užuot kaip debeto sąskaitą pasirinkęs **Nuomos išlaidos**, mokėtinų sumų klerkas pasirenka tarpuskaitos sąskaitą, kad sugeneruotų tolesnį įrašą.

### <a name="ap-process--1312020--je-110"></a>AP procesas – 2020-01-31 – JE 110

| Kodo tipas | Sąskaitos numeris | Sluoksnis   | Sąskaitos aprašas | Debetas    | Kreditas   |
|--------------|----------------|---------|---------------------|----------|----------|
| Didžioji knyga       | 4              | Dabartiniai | Tarpuskaitos sąskaita    | 1,000.00 |          |
| Didžioji knyga       | 2              | Dabartiniai | Banko mokestis            | 3.00     |          |
| Didžioji knyga       | 3              | Dabartiniai | PVM išlaidos         | 5.00     |          |
| Tiekėjas       | 5              | Dabartiniai | Mokėtinos sumos    |          | 1,008.00 |

Kai išrašas išduodamas tiekėjui, vadovaukitės įprastu mokėjimo procesu. Šio proceso metu sugeneruojamas tolesnis žurnalo įrašas.

### <a name="cash-payment--1312020--je-120"></a>Mokėjimas grynaisiais pinigais – 2020–01-31 JE 120

| Kodo tipas | Sąskaitos numeris | Sluoksnis   | Sąskaitos aprašas | Debetas    | Kreditas   |
|--------------|----------------|---------|---------------------|----------|----------|
| Tiekėjas       | 5              | Dabartiniai | Mokėtinos sumos    | 1,008.00 |          |
| Bankas         | 9              | Dabartiniai | Grynieji pinigai                |          | 1,008.00 |

Šiuo metu esate visiškai apskaitę šią nuomą pagal privalomuosius ataskaitų reikalavimus ir galite generuoti bandomąjį balansą naudodami dabartinį sluoksnį. Sistema pateikia bandomąjį balansą su tolesniais duomenimis.

<table>
<thead>
<tr>
<th rowspan='3'>Sąskaitos numeris</th>
<th rowspan='3'>aprašymas</th>
<th colspan='3'>Įstatyminė knyga (dabartinis sluoksnis)</th>
<th rowspan='3'>Dabartinio sluoksnio bendroji suma</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
<th>Dr (Cr)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Nuomos išlaidos</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Banko mokestis</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>PVM išlaidos</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Tarpuskaitos sąskaita</td>
<td>-1,000.00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Mokėtinos sumos</td>
<td></td>
<td>–1 008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Naudojimo teise valdomas turtas</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Finansinės nuomos įsipareigojimas</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Palūkanų išlaidos</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Grynieji pinigai</td>
<td></td>
<td></td>
<td>–1 008,00</td>
<td>–1 008,00</td>
</tr>
<tr>
<td>10</td>
<td>Likvidavimo išlaidos</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Sukauptas nusidėvėjimas</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Jei norite naudoti IFRS 16 skaičius ir vykdyti tą patį bandomąjį balansą, įstatyminio apskaitos žurnalo įrašai turi būti atšaukti, o IFRS 16 žurnalo įrašai – registruojami. Kad galėtumėte atšaukti įstatyminio žurnalo įrašus, šiame pavyzdyje yra pateikta įstatyminė atšaukimo knyga, kurios nustatymai tokie patys, kaip įstatyminės knygos, tačiau priešingas registravimo šablonas. Pavyzdžiui, įstatyminėje knygoje *debetuojama* nuomos išlaidų sąskaita, tačiau atšaukimo knygoje ši sąskaita bus *kredituojama*. Šiuos ryšius lengva apibrėžti turto nuomos registravimo sąskaitose, esančiose puslapyje **Turto nuomos parametrai** (**Turto nuoma \> Sąranka \> Turto nuomos parametrai**).

Kai tas pats procesas, kuris buvo naudojamas įstatyminei knygai, naudojamas atšaukimo knygai, sukuriamas tolesnis žurnalo įrašas. Skirtumas yra tas, kad atšaukimo knygoje rezervuojami atšaukiami įrašai iš įstatyminės knygos. Atšaukiami įrašai taip pat sukuriami pasirinktiniame sluoksnyje. Kai bandomasis balansas vykdomas dabartiniame sluoksnyje, atšaukiami žurnalo įrašai neįtraukiami.

### <a name="lease-payment--1312020--je-130"></a>Nuomos mokestis – 2020-01-31 – JE 130

| Kodo tipas | Sąskaitos numeris | Sluoksnis  | Sąskaitos aprašas | Debetas    | Kreditas   |
|--------------|----------------|--------|---------------------|----------|----------|
| Didžioji knyga       | 4              | Pasirinktinis | Tarpuskaitos sąskaita    | 1,000.00 |          |
| Didžioji knyga       | 1              | Pasirinktinis | Nuomos išlaidos       |          | 1,000.00 |

Kai jau pašalinsite įstatyminio žurnalo įrašus, užsakysite visus žurnalo įrašus, kurių IFRS 16 knygoje reikalaujama pagal IFRS 16. Šie įrašai apima pradinį naudojimo teise valdomo turto ir įsipareigojimo pripažinimą bei palūkanų ir nusidėvėjimo įrašą.

### <a name="initial-recognition--112020--je-140"></a>Pradinis pripažinimas – 2020-01-01 – JE 140

| Kodo tipas | Sąskaitos numeris | Sluoksnis  | Sąskaitos aprašas      | Debetas     | Kreditas    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Didžioji knyga       | 6              | Pasirinktinis | Naudojimo teise valdomas turtas                | 22,793.90 |           |
| Didžioji knyga       | 7              | Pasirinktinis | Finansinės nuomos įsipareigojimas |           | 22,793.90 |

Nuomos mokestis registruojamas taip, kaip kiti nuomos mokesčiai. Tarpuskaitos sąskaitos naudojimo priežastis – užtikrinti, kad grynieji pinigai būtų kredituoti tik vieną kartą.

### <a name="lease-payment--1312020--je-150"></a>Nuomos mokestis – 2020-01-31 – JE 150

| Kodo tipas | Sąskaitos numeris | Sluoksnis  | Sąskaitos aprašas      | Debetas    | Kreditas   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Didžioji knyga       | 7              | Pasirinktinis | Finansinės nuomos įsipareigojimas | 1,000.00 |          |
| Didžioji knyga       | 4              | Pasirinktinis | Tarpuskaitos sąskaita         |          | 1,000.00 |

Palūkanų sąnaudų žurnalo įrašas generuojamas iš įsipareigojimo amortizacijos grafiko.

### <a name="interest-expense--1312020--je-160"></a>Palūkanų sąnaudos – 2020-01-31 – JE 160

| Kodo tipas | Sąskaitos numeris | Sluoksnis  | Sąskaitos aprašas      | Debetas | Kreditas |
|--------------|----------------|--------|--------------------------|-------|--------|
| Didžioji knyga       | 8              | Pasirinktinis | Palūkanų išlaidos         | 94.97 |        |
| Didžioji knyga       | 7              | Pasirinktinis | Finansinės nuomos įsipareigojimas |       | 94.97  |

Nusidėvėjimo išlaidų žurnalo įrašas generuojamas iš turto nusidėvėjimo grafiko.

### <a name="depreciation-expense--1312020--je-170"></a>Nusidėvėjimo išlaidos – 2020-01-31 – JE 170

| Kodo tipas | Sąskaitos numeris | Sluoksnis  | Sąskaitos aprašas      | Debetas  | Kreditas |
|--------------|----------------|--------|--------------------------|--------|--------|
| Didžioji knyga       | 10             | Pasirinktinis | Likvidavimo išlaidos     | 949.75 |        |
| Didžioji knyga       | 11             | Pasirinktinis | Sukauptas nusidėvėjimas |        | 949.75 |

Kai bus sukurti ir užregistruoti visi šie žurnalo įrašai, matysite tolesnes „1 pasirinktinio sluoksnio“ reikšmes. Atkreipkite dėmesį, kad į paskutinį stulpelį įtrauktas banko mokestis, pridėtinės vertės mokesčio (PVM) išlaidos ir grynųjų pinigų sumažinimas iš ankstesnio sluoksnio, tačiau jis neapima privalomųjų ataskaitų žurnalo įrašų. Todėl galite išnaudoti dvigubų ataskaitų galimybes. Dabar įmonė tiesiog turi vykdyti bandomąjį balansą ir sujungti dabartinį sluoksnį su standartiniu sluoksniu, kad sukurtų IFRS bandomąjį balansą.

| Sąskaitos Nr. | aprašymas              | Įstatyminė knyga\-Dabartinis sluoksnis\-JE\-100\-Dr \(Cr\) | Įstatyminė knyga\-Dabartinis sluoksnis\-JE\-110\-Dr \(Cr\) | Įstatyminė knyga\-Dabartinis sluoksnis\-JE\-120\-Dr \(Cr\) | Dabartinis sluoksnis \- Bendroji suma | - | Atšaukimo knyga\-Pasirinktinis sluoksnis\-JE\-130\-Dr \(Cr\) | IFRS 16 knyga\-Pasirinktinis sluoksnis\-JE\-140\-Dr \(Cr\) | IFRS 16 knyga\-Pasirinktinis sluoksnis\-JE\-150\-Dr \(Cr\) | IFRS 16 knyga\-Pasirinktinis sluoksnis\-JE\-160\-Dr \(Cr\) | IFRS 16 knyga\-Pasirinktinis sluoksnis\-JE\-170\-Dr \(Cr\) | Pasirinktinis sluoksnis \+ Dabartinis sluoksnis \- Bendroji suma |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Nuomos išlaidos            | 1,000 \. 00                                         |                                                   |                                                   | 1,000 \. 00               |   | \-1000                                         |                                                |                                                |                                                |                                                | 0 \. 00                                   |
| 2          | Banko mokestis                 |                                                   | 3 \. 00                                             |                                                   | 3 \. 00                   |   |                                                 |                                                |                                                |                                                |                                                | 3 \. 00                                   |
| 3          | PVM išlaidos              |                                                   | 5 \. 00                                             |                                                   | 5 \. 00                   |   |                                                 |                                                |                                                |                                                |                                                | 5 \. 00                                   |
| 4          | Tarpuskaitos sąskaita         | \-1000\.00                                       | 1,000 \. 00                                         |                                                   | 0 \. 00                   |   | 1000                                           |                                                | \-1000                                        |                                                |                                                | 0 \. 00                                   |
| 5          | Mokėtinos sumos         |                                                   | \-1008\.00                                       | 1,008 \. 00                                         | 0 \. 00                   |   |                                                 |                                                |                                                |                                                |                                                | 0 \. 00                                   |
| 6          | Naudojimo teise valdomas turtas                |                                                   |                                                   |                                                   | 0 \. 00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793 \. 90                              |
| 7          | Finansinės nuomos įsipareigojimas |                                                   |                                                   |                                                   | 0 \. 00                   |   |                                                 | \-22 794                                       | 1000                                          | \-94\.97                                       |                                                | \-21 888\.87                            |
| 8          | Palūkanų išlaidos         |                                                   |                                                   |                                                   | 0 \. 00                   |   |                                                 |                                                |                                                | 94 \. 97                                         |                                                | 94 \. 97                                  |
| 9          | Grynieji pinigai                     |                                                   |                                                   | \-1008\.00                                       | \-1008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1008\.00                             |
| 10         | Likvidavimo išlaidos     |                                                   |                                                   |                                                   | 0 \. 00                   |   |                                                 |                                                |                                                |                                                | 949 \. 75                                        | 949 \. 75                                 |
| 11         | Sukauptas nusidėvėjimas |                                                   |                                                   |                                                   | 0 \. 00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
