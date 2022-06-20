---
title: PVM skaičiavimas ir apvalinimas
description: Šiame straipsnyje pateikiama PVM skaičiavimo ir apvalinimo apžvalga bei paaiškinami PVM skaičiavimo ir apvalinimo nustatymo parametrai.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939239"
---
# <a name="sales-tax-calculation-and-rounding"></a>PVM skaičiavimas ir apvalinimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta PVM skaičiavimo ir apvalinimo " Microsoft Dynamics 365 Finance" apžvalga. Taip pat paaiškinama, kokie parametrai naudojami PVM skaičiavimo ir apvalinimo nustatyme, ir kaip šie parametrai veikia kartu.

## <a name="parameters"></a>Parametrai

Keletas parametrų kontroliuoja PVM skaičiavimą ir apvalinimą:

- **Skaičiavimo būdas** – šis parametras nustatytas DK **parametrų** puslapyje ir nurodo, ar mokesčio bazinė suma skaičiuojama pagal dokumentą, ar pagal eilutę. Jei PVM **kodo bazinės** **ribinės** vertės parametras nustatytas kaip Grynoji SF balanso suma, mokesčio bazinė suma visada skaičiuojama pagal dokumentą, neatsižvelgiant į šio parametro nustatymą.
- **Apvalinimas** pagal – šis parametras nustatomas PVM grupei ir nurodo, ar mokesčio suma apvalinama pagal PVM kodą, ar pagal PVM kodo derinį.
- **Šaltinis** – šis parametras nustatytas PVM kodui ir nurodo, kaip apskaičiuojama mokesčių suma. Daugiau informacijos ieškokite LAUKO [Šaltinis PVM skaičiavimo metodus](sales-tax-calculation-methods-origin-field.md).
- **Bazinė bazinė** ribinė vertė – šis parametras nustatytas PVM kodui ir nurodo, kuri suma naudojama norint pasirinkti atitinkamus mokesčių tarifus **PVM kodų reikšmių** puslapyje. Daugiau informacijos žr. [PVM tarifų nustatymas pagal bazinės ribos ir skaičiavimo metodus](marginal-base-field.md).
- **PVM apvalinimo** taisyklė – šis parametras nustatytas PVM kodui ir nurodo, kaip apvalinama nustatyta PVM suma, įskaitant apvalinimo tikslumą ir apvalinimo metodą.

Likusioje šio straipsnio dalyje pateikiami įprasti PVM skaičiavimo ir apvalinimo pavyzdžiai, naudojantys ankstesnių parametrų derinį.

## <a name="scenario-for-the-examples"></a>Pavyzdžių scenarijus

- Apmokestinamame dokumente yra dvi eilutės, o kiekvienos eilutės mokesčio pagrindas yra 42,42.
- Kiekvienai eilutei nustatomi du PVM kodai: 1 PVM kodas ir 2 PVM kodas.
- 1 mokesčio kodo ir 2 mokesčio kodo mokesčio tarifas yra 10 procentų.
- Į kainą neįtraukti mokesčiai.
- Apvalinimo tikslumas yra 0,01.
- Apvalinimo būdas yra **Apvalinimas**.

## <a name="example-1"></a>1 pavyzdys

### <a name="parameter-values"></a>Parametrų vertės

| Skaičiavimo būdas | Apvalinama pagal    | Kilmė                   | Bazinės ribos       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Eilutė               | PVM kodas | Grynosios sumos procentai | Grynoji kiekvienos eilutės suma |

### <a name="calculation-and-rounding-behavior"></a>Skaičiavimo ir apvalinimo būdas

| Eilutės numeris | PVM kodas | Sumos šaltinis | PVM suma |
| ------------| ---------------| --------------| -----------------|
| 1           | Kodas 1         | 42.42         | 4.25             |
| 1           | Kodas 2         | 42.42         | 4.25             |
| 2           | Kodas 1         | 42.42         | 4.25             |
| 2           | Kodas 2         | 42.42         | 4.25             |

Mokesčio bazinė suma skaičiuojama pagal eilutę:

- **1 eilutė:** 42,42
- **2 eilutė:** 42,42

Mokesčio suma apskaičiuojama pagal PVM kodą:

- **Eilutė 1:**

    - 1 PVM kodo mokesčio suma = 42,42 &times; 10 procentų = 4,242
    - 2 PVM kodo mokesčio suma = 42,42 &times; 10 procentų = 4,242

- **Eilutė 2:**

    - 1 PVM kodo mokesčio suma = 42,42 &times; 10 procentų = 4,242
    - 2 PVM kodo mokesčio suma = 42,42 &times; 10 procentų = 4,242

Mokesčio suma yra suapvalinta pagal PVM kodą:

- **Eilutė 1:**

    - Suapvalinta mokesčio suma, skirta PVM kodui 1 = 4,25
    - Suapvalinta mokesčio suma 2 PVM kodui = 4,25

- **Eilutė 2:**

    - Suapvalinta mokesčio suma, skirta PVM kodui 1 = 4,25
    - Suapvalinta mokesčio suma 2 PVM kodui = 4,25

## <a name="example-2"></a>2 pavyzdys

### <a name="parameter-values"></a>Parametrų vertės

| Skaičiavimo būdas | Apvalinama pagal    | Kilmė                   | Bazinės ribos                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Eilutė/suma         | PVM kodas | Grynosios sumos procentai | Grynoji SF balanso suma |

### <a name="calculation-and-rounding-behavior"></a>Skaičiavimo ir apvalinimo būdas

| Eilutės numeris | PVM kodas | Sumos šaltinis | PVM suma |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kodas 1         | 42.42         | 4.25             |
| 1           | Kodas 2         | 42.42         | 4.25             |
| 2           | Kodas 1         | 42.42         | 4.24             |
| 2           | Kodas 2         | 42.42         | 4.24             |

Mokesčio pagrindas apskaičiuojamas pagal dokumentą:

- Mokesčio bazinė suma = 42,42 + 42,42 = 84,84

Mokesčio suma apskaičiuojama pagal PVM kodą:

- 1 PVM kodo mokesčio suma = 84,84 &times; 10 procentų = 8,484
- 2 PVM kodo mokesčio suma = 84,84 &times; 10 procentų = 8,484

Mokesčio suma yra suapvalinta pagal PVM kodą:

- Suapvalinta mokesčio suma 1 PVM kodui = 8,49
- Suapvalinta mokesčio suma 2 PVM kodui = 8,49

Suapvalinta mokesčio suma paskirstoma kiekvienai PVM kodo eilutei:

- Paskirstykite suapvalinto mokesčio sumą 1 (8.49) kodui 1 (4.25) ir 2 eilutei (4.24).
- Paskirstykite suapvalinto mokesčio sumą 2 (8.49) kodui 1 (4.25) ir 2 eilutei (4.24).

## <a name="example-3"></a>3 pavyzdys

### <a name="parameter-values"></a>Parametrų vertės

| Skaičiavimo būdas | Apvalinama pagal    | Kilmė                              | Bazinės ribos       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Eilutė               | PVM kodas | Apskaičiuoti grynosios sumos procentai | Grynoji kiekvienos eilutės suma |

### <a name="calculation-and-rounding-behavior"></a>Skaičiavimo ir apvalinimo būdas

| Eilutės numeris | PVM kodas | Sumos šaltinis | PVM suma |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kodas 1         | 42.42         | 4.72             |
| 1           | Kodas 2         | 42.42         | 4.72             |
| 2           | Kodas 1         | 42.42         | 4.72             |
| 2           | Kodas 2         | 42.42         | 4.72             |

Mokesčio bazinė suma skaičiuojama pagal eilutę:

- **1 eilutė:** 42,42
- **2 eilutė:** 42,42

Mokesčio suma apskaičiuojama pagal PVM kodą:

- **Eilutė 1:**

    - 1 PVM kodo mokesčio suma = 42,42 &times; 10 &divide; procentų (1 – 10 procentų) = 4,7133
    - 2 PVM kodo mokesčio suma = 42,42 &times; 10 &divide; procentų (1 – 10 procentų) = 4,7133

- **Eilutė 2:**

    - 1 PVM kodo mokesčio suma = 42,42 &times; 10 &divide; procentų (1 – 10 procentų) = 4,7133
    - 2 PVM kodo mokesčio suma = 42,42 &times; 10 &divide; procentų (1 – 10 procentų) = 4,7133

Mokesčio suma yra suapvalinta pagal PVM kodą:

- **Eilutė 1:**

    - Suapvalinta mokesčio suma, skirta PVM kodui 1 = 4,72
    - Suapvalinta mokesčio suma 2 PVM kodui = 4,72

- **Eilutė 2:**

    - Suapvalinta mokesčio suma, skirta PVM kodui 1 = 4,72
    - Suapvalinta mokesčio suma 2 PVM kodui = 4,72

## <a name="example-4"></a>4 pavyzdys

### <a name="parameter-values"></a>Parametrų vertės

| Skaičiavimo būdas | Apvalinama pagal    | Kilmė                              | Bazinės ribos                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Eilutė/suma         | PVM kodas | Apskaičiuoti grynosios sumos procentai | Grynoji SF balanso suma |

### <a name="calculation-and-rounding-behavior"></a>Skaičiavimo ir apvalinimo būdas

| Eilutės numeris | PVM kodas | Sumos šaltinis | PVM suma |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kodas 1         | 42.42         | 4.72             |
| 1           | Kodas 2         | 42.42         | 4.72             |
| 2           | Kodas 1         | 42.42         | 4.71             |
| 2           | Kodas 2         | 42.42         | 4.71             |

Mokesčio pagrindas apskaičiuojamas pagal dokumentą:

- Mokesčio bazinė suma = 42,42 + 42,42 = 84,84

Mokesčio suma apskaičiuojama pagal PVM kodą:

- 1 PVM kodo mokesčio suma = 84,84 &times; 10 &divide; procentų (1 – 10 procentų) = 9,4267
- 2 PVM kodo mokesčio suma = 84,84 &times; 10 &divide; procentų (1 – 10 procentų) = 9,4267

Mokesčio suma yra suapvalinta pagal PVM kodą:

- Suapvalinta mokesčio suma 1 PVM kodui = 9,43
- Suapvalinta mokesčio suma 2 PVM kodui = 9,43

Suapvalinta mokesčio suma paskirstoma kiekvienai PVM kodo eilutei:

- Paskirstykite mokesčio sumą 1 (9.43) 1 eilutei (4.72) ir 2 eilutei (4.71).
- Paskirstykite mokesčio sumą 2 (9.43) 1 eilutei (4.72) ir 2 eilutei (4.71).

## <a name="example-5"></a>5 pavyzdys

### <a name="parameter-values"></a>Parametrų vertės

| Skaičiavimo būdas | Apvalinama pagal                | Kilmė                   | Bazinės ribos       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Eilutė               | PVM kodo kombinacija | Grynosios sumos procentai | Grynoji kiekvienos eilutės suma |

### <a name="calculation-and-rounding-behavior"></a>Skaičiavimo ir apvalinimo būdas

| Eilutės numeris | PVM kodas | Sumos šaltinis | PVM suma |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kodas 1         | 42.42         | 4.25             |
| 1           | Kodas 2         | 42.42         | 4.24             |
| 2           | Kodas 1         | 42.42         | 4.24             |
| 2           | Kodas 2         | 42.42         | 4.24             |

Mokesčio bazinė suma skaičiuojama pagal eilutę:

- **1 eilutė:** 42,42
- **2 eilutė:** 42,42

Mokesčio suma apskaičiuojama pagal PVM kodą:

- **Eilutė 1:**

    - 1 PVM kodo mokesčio suma = 42,42 &times; 10 procentų = 4,242
    - 2 PVM kodo mokesčio suma = 42,42 &times; 10 procentų = 4,242

- **Eilutė 2:**

    - 1 PVM kodo mokesčio suma = 42,42 &times; 10 procentų = 4,242
    - 2 PVM kodo mokesčio suma = 42,42 &times; 10 procentų = 4,242

Mokesčių suma yra suapvalinta pagal PVM kodo kombinaciją:

- Bendra PVM suma = 4,242 + 4,242 + 4,242 + 4,242 = 16,968, suapvalinama iki 16,97

Suapvalinta mokesčio suma paskirstoma kiekvienai PVM kodo eilutei:

- Paskirstykite PVM sumą (16,97) 1 eilutei ir 2 eilutei:

    - **Eilutė 1:**

        - 1 PVM kodo mokesčio suma = 4,25
        - 2 PVM kodo mokesčio suma = 4,24

    - **Eilutė 2:**

        - 1 PVM kodo mokesčio suma = 4,24
        - 2 PVM kodo mokesčio suma = 4,24

## <a name="example-6"></a>6 pavyzdys

### <a name="parameter-values"></a>Parametrų vertės

| Skaičiavimo būdas | Apvalinama pagal                | Kilmė                   | Bazinės ribos                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Eilutė/suma         | PVM kodo kombinacija | Grynosios sumos procentai | Grynoji SF balanso suma |

### <a name="calculation-and-rounding-behavior"></a>Skaičiavimo ir apvalinimo būdas

| Eilutės numeris | PVM kodas | Sumos šaltinis | PVM suma |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kodas 1         | 42.42         | 4.25             |
| 1           | Kodas 2         | 42.42         | 4.24             |
| 2           | Kodas 1         | 42.42         | 4.24             |
| 2           | Kodas 2         | 42.42         | 4.24             |

Mokesčio pagrindas apskaičiuojamas pagal dokumentą:

- Mokesčio bazinė suma = 42,42 + 42,42 = 84,84

Mokesčio suma apskaičiuojama pagal PVM kodą:

- 1 PVM kodo mokesčio suma = 84,84 &times; 10 procentų = 8,484
- 2 PVM kodo mokesčio suma = 84,84 &times; 10 procentų = 8,484

Mokesčių suma yra suapvalinta pagal PVM kodo kombinaciją:

- Bendra PVM suma = 8,484 + 8,484 = 16,968, kuri suapvalinama iki 16,97

Suapvalinta mokesčio suma paskirstoma kiekvienai PVM kodo eilutei:

- Paskirstykite PVM sumą (16,97) 1 eilutei ir 2 eilutei:

    - **Eilutė 1:**

        - 1 PVM kodo mokesčio suma = 4,25
        - 2 PVM kodo mokesčio suma = 4,24

    - **Eilutė 2:**

        - 1 PVM kodo mokesčio suma = 4,24
        - 2 PVM kodo mokesčio suma = 4,24

## <a name="example-7"></a>7 pavyzdys

### <a name="parameter-values"></a>Parametrų vertės

| Skaičiavimo būdas | Apvalinama pagal                | Kilmė                              | Bazinės ribos       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Eilutė               | PVM kodo kombinacija | Apskaičiuoti grynosios sumos procentai | Grynoji kiekvienos eilutės suma |

### <a name="calculation-and-rounding-behavior"></a>Skaičiavimo ir apvalinimo būdas

| Eilutės numeris | PVM kodas | Sumos šaltinis | PVM suma |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kodas 1         | 42.42         | 4.72             |
| 1           | Kodas 2         | 42.42         | 4.71             |
| 2           | Kodas 1         | 42.42         | 4.71             |
| 2           | Kodas 2         | 42.42         | 4.72             |

Mokesčio bazinė suma skaičiuojama pagal eilutę:

- **1 eilutė:** 42,42
- **2 eilutė:** 42,42

Mokesčio suma apskaičiuojama pagal PVM kodą:

- **Eilutė 1:**

    - 1 PVM kodo mokesčio suma = 42,42 &times; 10 &divide; procentų (1 – 10 procentų) = 4,7133
    - 2 PVM kodo mokesčio suma = 42,42 &times; 10 &divide; procentų (1 – 10 procentų) = 4,7133

- **Eilutė 2:**

    - 1 PVM kodo mokesčio suma = 42,42 &times; 10 &divide; procentų (1 – 10 procentų) = 4,7133
    - 2 PVM kodo mokesčio suma = 42,42 &times; 10 &divide; procentų (1 – 10 procentų) = 4,7133

Mokesčių suma yra suapvalinta pagal PVM kodo kombinaciją:

- Bendra PVM suma = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, kuri suapvalinama iki 18,86

Suapvalinta mokesčio suma paskirstoma kiekvienai PVM kodo eilutei:

- Paskirstykite PVM sumą (18.86) 1 eilutei ir 2 eilutei:

    - **Eilutė 1:**

        - 1 PVM kodo mokesčio suma = 4,72
        - 2 PVM kodo mokesčio suma = 4,71

    - **Eilutė 2:**

        - 1 PVM kodo mokesčio suma = 4,71
        - 2 PVM kodo mokesčio suma = 4,72

## <a name="example-8"></a>8 pavyzdys

### <a name="parameter-values"></a>Parametrų vertės

| Skaičiavimo būdas | Apvalinama pagal                | Kilmė                              | Bazinės ribos                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Eilutė/suma         | PVM kodo kombinacija | Apskaičiuoti grynosios sumos procentai | Grynoji SF balanso suma |

### <a name="calculation-and-rounding-behavior"></a>Skaičiavimo ir apvalinimo būdas

| Eilutės numeris | PVM kodas | Sumos šaltinis | PVM suma |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kodas 1         | 42.42         | 4.72             |
| 1           | Kodas 2         | 42.42         | 4.71             |
| 2           | Kodas 1         | 42.42         | 4.71             |
| 2           | Kodas 2         | 42.42         | 4.72             |

Mokesčio pagrindas apskaičiuojamas pagal dokumentą:

- Mokesčio bazinė suma = 42,42 + 42,42 = 84,84

Mokesčio suma apskaičiuojama pagal PVM kodą:

- 1 PVM kodo mokesčio suma = 84,84 &times; 10 &divide; procentų (1 – 10 procentų) = 9,4267
- 2 PVM kodo mokesčio suma = 84,84 &times; 10 &divide; procentų (1 – 10 procentų) = 9,4267

Mokesčių suma yra suapvalinta pagal PVM kodo kombinaciją:

- Bendra PVM suma = 9,4267 + 9,4267 = 18,8534, kuris suapvalinamas iki 18,86

Suapvalinta mokesčio suma paskirstoma kiekvienai PVM kodo eilutei:

- Paskirstykite PVM sumą (18.86) 1 eilutei ir 2 eilutei:

    - **Eilutė 1:**

        - 1 PVM kodo mokesčio suma = 4,72
        - 2 PVM kodo mokesčio suma = 4,71

    - **Eilutė 2:**

        - 1 PVM kodo mokesčio suma = 4,71
        - 2 PVM kodo mokesčio suma = 4,72

## <a name="additional-resources"></a>Papildomi ištekliai

- [PVM skaičiavimo metodai lauke Kilmė](sales-tax-calculation-methods-origin-field.md)
- [PVM tarifai pagal bazinę ribą ir skaičiavimo metodus](marginal-base-field.md)
- [PVM kodų skaičiavimo parinktys Visa suma ir Intervalas](whole-amount-interval-options-sales-tax-codes.md)
