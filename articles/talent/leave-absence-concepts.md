---
title: Atostogų ir neatvykimo koncepcijos
description: Šioje temoje aprašomos atostogų ir neatvykimo koncepcijos ir kaip nustatomi nebuvimo balansai.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 96e3aa74e513a2421b04bac049400cf71042e2c8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518634"
---
# <a name="leave-and-absence-concepts"></a>Atostogų ir neatvykimo koncepcijos

[!include[banner](../includes/banner.md)]

Koncepcijos ir terminai, aprašyti šioje temoje, gali padėti jums nustatyti, kaip darbuotojui skiriama laisvo laiko ir kaip skaičiuojami to darbuotojo laiko balansai. Daugiau informacijos apie atostogas ir neatvykimo valdymą, rasite temoje [Atostogų ir neatvykimo valdymas](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Atostogų plano informacija

### <a name="start-date"></a>Pradžios data

Pradžios data – data, kai pradedamas kaupimo apdorojimas. Pradžios data taip pat naudojama kaip sukakties data, naudojama apskaičiuoti perkeliamas sumas.

## <a name="accruals"></a>Kaupimai

Kaupimai nustato, kada ir kaip dažnai darbuotojui skiriamas laisvas laikas. Strategijos apie tai, kaip suteikiamas sukauptas laikas, ir strategijos apie proporcingą paskirstymą apibrėžtos dalyje **Kaupimai** nustatant atostogų ir neatvykimo planą.

### <a name="accrual-frequency"></a>Kaupimo dažnumas

Kaupimo dažnumas apibrėžia, kaip dažnai sukaupiamos arba skiriamos atostogos. Galimos toliau nurodytos parinktys.

- Kasdienis
- Savaitinis
- Kas dvi savaites
- Kas pusę mėnesio
- Mėnesinis
- Kas ketvirtį
- Kas pusmetį
- Kasmet
- Joks

### <a name="accrual-period-basis"></a>Kaupimo laikotarpio pagrindas

Kaupimo laikotarpio pagrindas nustato datą, naudojamą skaičiuojant kaupimo laikotarpius. Galimos toliau nurodytos parinktys.

- **Plano pradžios data**
- **Darbuotojo konkreti data** – pasirinkus šią pasirinktį, vertė nustato pradinės datos vertės šaltinį, kuris naudojamas apskaičiuoti kaupimo laikotarpius. Galimos toliau nurodytos parinktys.

    - Pasirinktinis
    - Jubiliejaus data
    - Pradinio įdarbinimo data
    - Paaukštinimo data
    - Patikslinta darbininko darbo pradžios data
    - Darbininko darbo pradžios data

### <a name="accrual-award-date"></a>Kaupimų skyrimo data

Kaupimo skyrimo data nustato, kada darbuotojui skiriamas laisvas laikas. Galimos toliau nurodytos parinktys.

- **Kaupimo laikotarpio pabaigos data** – darbuotojui bus skirtas laisvas laikas suteikimo laikotarpio paskutinę dieną.

    Tam, kad būtų sukaupta teisinga suma, kaupimo procesas turi apimti visą laikotarpį. Pavyzdžiui, kaupimo laikotarpis yra nuo 2018 m. sausio 1 d. iki 2018 m. sausio 31 d. Šiuo atveju norint įtraukti sausį, kaupimo apdorojimas turi vykti 2018 m. vasario 1 d.

- **Kaupimo laikotarpio pradžios data** – darbuotojui bus skirtas laisvas laikas suteikimo laikotarpio pirmą dieną.

### <a name="accrual-policy-on-enrollment"></a>Kaupimo strategija užregistruojant darbuotoją

Kaupimo strategija užregistruojant darbuotoją apibrėžia, kaip skaičiuojamas kaupimas, kai darbuotojas užregistruojamas kaupimo laikotarpio viduryje. Galimos toliau nurodytos parinktys.

- **Proporcingai paskirstytas** – datų intervalas nuo užregistravimo datos iki pradžios datos naudojamas siekiant nustatyti dienų skirtumas. Šis skirtumas taikomas, kai apdorojami kaupimai.
- **Visas kaupimas** – visa sukaupta suma, atsižvelgiant į pakopą, skiriama pirmojo kaupimo apdorojimo metu.
- **Nėra kaupimo** – jokio kaupimo neskiriama iki kito kaupimo laikotarpio.

### <a name="accrual-policy-on-unenrollment"></a>Kaupimo strategija išregistruojant darbuotoją

Kaupimo strategija išregistruojant darbuotoją apibrėžia, kaip skaičiuojamas kaupimas, kai darbuotojas išregistruojamas kaupimo laikotarpio viduryje. Galimos toliau nurodytos parinktys.

- **Proporcingai paskirstytas** – datų intervalas nuo užregistravimo datos iki pradžios datos naudojamas siekiant nustatyti dienų skirtumas. Šis skirtumas taikomas, kai apdorojami kaupimai.
- **Visas kaupimas** – visa sukaupta suma, atsižvelgiant į pakopą, skiriama pirmojo kaupimo apdorojimo metu.
- **Nėra kaupimo** – jokio kaupimo neskiriama iki kito kaupimo laikotarpio.

## <a name="accrual-schedule"></a>Kaupimo grafikas

Kaupimo grafikas nustato, kaip darbuotojas kaups laisvą laiką ir kokią sumą tas darbuotojas sukaups ir perkels į priekį. Galima kurti pakopas, kad laisvas laikas būtų skiriamas remiantis skirtingais lygiais.

### <a name="months-of-service"></a>Tarnybos mėnesiai

**Dirbtų mėnesių** vertė nustato mažiausią mėnesių, kuriuos darbuotojas turi dirbti norėdamas įgyti teisę į kaupimus, skaičių. Jei darbuotojams netaikomas minimalus laikotarpis, nustatykite vertę kaip **0**.

### <a name="hours-worked"></a>Dirbtos valandos

**Dirbtų valandų** vertė nustato mažiausią skaičių valandų, kurias darbuotojas turi dirbti per kaupimo laikotarpį norėdamas įgyti teisę į kaupimus. Jei darbuotojams netaikomas minimalus laikotarpis, nustatykite vertę kaip **0**.

### <a name="accrual-amount"></a>Kaupimo suma

Sukaupta suma yra valandų ar dienų, kurias darbuotojai sukaups per laikotarpį, suma. Laikotarpis paremtas kaupimo dažnumu.

### <a name="minimum-balance"></a>Mažiausias likutis

Neigiama minimalaus balanso vertė gali būti naudojama, jei darbuotojams leidžiama prašyti daugiau atostogų nei jie yra sukaupę.

### <a name="maximum-carry-forward"></a>Maksimalus perkeliamas balansas

Apdorojant kaupimą bus pakoreguoti atostogų balansai, kurie viršija maksimalų perkėlimo balansą praėjus metams nuo pradžios datos.

### <a name="grant-amount"></a>Paskirtoji suma

Paskirtoji suma yra pradinis skaičių valandų ar dienų, kurios paskiriamos darbuotojui, kai jis pirmą kartą įtraukiamas į atostogų planą. Suma nekaupiama kiekvieną kaupimo laikotarpį.

## <a name="enrollments-and-balances"></a>Registracijos ir balansai

### <a name="enrollment-date"></a>Registracijos data

Registracijos data nurodo, kada darbuotojas gali pradėti kaupti laisvą laiką. Pvz., jei darbuotojas įtraukiamas į atostogų planą 2018 m. birželio 15 dieną, jis negali kaupti jokio laisvo laiko iki 2018 m. birželio 15 d.

### <a name="current-balance"></a>Dabartinis balansas

Esamas balansas – tai atostogų laikas, kuris yra galimas prašant laisvo laiko. Ši suma apima kaupimus, patvirtintus prašymus ir koregavimus iki dabartinės datos.

### <a name="current-balance-examples"></a>Esamo balanso pavyzdžiai

#### <a name="annual-plan"></a>Metinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Metinis            | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2019 m. sausio 1 dieną (2019-01-01), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Pageidaujama suma | Esamas balansas (2019-01-01) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Esamas balansas (160) = sukaupta suma (200) – pageidaujama suma (40)

#### <a name="semimonthly-plan"></a>Pusmėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kas pusę mėnesio       | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2018 m. gegužės 1 dieną (2018-05-01), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Pageidaujama suma | Esamas balansas (2019-01-01) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Esamas balansas (22) = sukaupta suma (5 x 6) – pageidaujama suma (8)

#### <a name="monthly-plan"></a>Mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kas pusę mėnesio       | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2018 m. gegužės 1 dieną (2018-05-01), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Pageidaujama suma | Esamas balansas (2019-01-01) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Esamas balansas (7) = sukaupta suma (5 x 3) – pageidaujama suma (8)

### <a name="forecasted-balance"></a>Prognozuojamas balansas

*Prognozuojamas balansas* yra atostogų suma, kuri bus galima tam tikrą dieną ateityje. Sukauptos sumos ir perkeliamų balansų koregavimai prognozuojami iki tos datos.

Naudojama ši formulė:

Prognozuojamas pirmadienio balansas = esamas balansas – prašymai + sukaupta suma – perkeliamo balanso koregavimas

### <a name="forecasted-balance-examples"></a>Prognozuojamo balanso pavyzdžiai

#### <a name="annual-plan"></a>Metinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Metinis            | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2019 m. vasario 15 dieną (2019-02-15), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Dabartinis balansas | Prognozuojamas balansas (2019-02-15) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Prognozuojamas balansas (40) = sukaupta suma (20) + esamas balansas (40) – perkeliamo balanso koregavimas (20)

#### <a name="semimonthly-plan"></a>Pusmėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kas pusę mėnesio       | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2019 m. vasario 15 dieną (2019-02-15), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Dabartinis balansas | Prognozuojamas balansas (2019-02-15) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Prognozuojamas balansas (35) = sukaupta suma (5 x 3) + esamas balansas (40) – perkeliamo balanso koregavimas (20)

#### <a name="monthly-plan"></a>Mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Registracijos data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas | Kaupimų skyrimo data    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Kas pusę mėnesio       | Plano pradžios data      | Kaupimo laikotarpio pabaiga |

Kaupimai apdorojami 2019 m. vasario 15 dieną (2019-02-15), kad būtų įtraukiamas visas laikotarpis.

**Rezultatai**

| Kaupimo suma | Mažiausias likutis | Maksimalus perkeliamas balansas | Dabartinis balansas | Prognozuojamas balansas (2019-02-15) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Prognozuojamas balansas (30) = sukaupta suma (10 x 1) + esamas balansas (40) – perkeliamo balanso koregavimas (20)

### <a name="proration-balance-examples"></a>Proporcingo paskirstymo balanso pavyzdžiai

#### <a name="prorated-monthly-plan"></a>Proporcingai paskirstytas mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mėnesinis           | Plano pradžios data      |

**Rezultatai**

| Darbuotojas            | Tarnybos mėnesiai | Registracijos data | Pradžios data | Kaupimo suma | Kaupimo apdorojimas | Likutis |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Viso kaupimo mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mėnesinis           | Plano pradžios data      |

**Rezultatai**

| Darbuotojas            | Tarnybos mėnesiai | Registracijos data | Pradžios data | Kaupimo suma | Kaupimo apdorojimas | Likutis |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>„Nėra kaupimo“ mėnesinis planas

**Plano nustatymas**

| Plano pradžios data | Kaupimo dažnumas | Kaupimo laikotarpio pagrindas |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mėnesinis           | Plano pradžios data      |

**Rezultatai**

| Darbuotojas            | Tarnybos mėnesiai | Registracijos data | Pradžios data | Kaupimo suma | Kaupimo apdorojimas | Likutis |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,00    |
