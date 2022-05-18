---
title: Sudėjimo intervalų funkcija
description: Šioje temoje pateikiama informacija, kuri padės pasirinkti tarp mėnesinio, ketvirtinio, pusmetinio ir metinio sudėjimo intervalų.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d1b8af3d5f8f6a6812fe309f57f682d0c5023d00
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710448"
---
# <a name="compounding-interval-functionality"></a>Sudėjimo intervalų funkcija

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje pateikiama informacija, kuri padės pasirinkti tarp mėnesinio, ketvirtinio, pusmetinio ir metinio sudėjimo intervalų. Sudėjimo intervalų funkcija naudojama norint nustatyti, kiek turi būti sudėjimo laikotarpių per nuomos mokėjimo grafiko metus. Kiekviename iš keturių šioje temoje pateiktų pavyzdžių vaizduojama, kaip atrodys skirtingo intervalo nuomos mokėjimų grafikas.

Negalite pasirinkti sudėjimo intervalo, kuris yra retesnis nei nuomos mokėjimo dažnumas. Pavyzdžiui, ketvirtinio sudėjimo intervalo negalima naudoti su mėnesiniu mokėjimo dažnumu, o metinio sudėjimo intervalo negalima naudoti su pusmetiniu mokėjimo dažnumu. Jei bandote pasirinkti sudėjimo intervalą, kuris yra retesnis nei nuomos mokėjimo dažnumas, pateikiamas klaidos pranešimas.

> [!NOTE]
> Visuose keturiuose šioje temoje pateiktuose pavyzdžiuose sudėjimo intervalas atitinka mokėjimo dažnumą.

## <a name="examples"></a>Pavyzdžiai

### <a name="setup-for-all-four-leases"></a>Visų keturių nuomų sąranka

Toliau esančiose lentelėse rodomos reikšmės, kurios yra nustatytos visų pavyzdžiuose naudojamų keturių nuomų skirtukuose **Bendra** ir **Mokėjimo grafiko eilutės**.

**Skirtukas Bendra**

| Laukas                      | Reikšmė                        |
|----------------------------|------------------------------|
| Apskaičiuota skolinimosi palūkanų norma | **5 %**                       |
| Anuiteto tipas               | **Įprastas anuitetas**         |
| Sujungimo intervalas       | Žr. atskirus pavyzdžius. |
| Mokėjimo dažnumas          | **Mėnesinis**                  |
| Pradžios data          | **2020-01-01**                 |

**Skirtukas Mokėjimo grafiko eilutės**

| Laukas             | Reikšmė                        |
|-------------------|------------------------------|
| Pradžios data        | **2020-01-01**                 |
| Laikotarpiai           | **120**                      |
| Laikotarpio intervalas   | **Mėnesiai**                   |
| Pabaigos data          | **2029-12-31**               |
| Mokėjimo dažnumas | Žr. atskirus pavyzdžius. |
| Mokėjimo suma    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>1 nuoma: mėnesinis sudėjimo intervalas ir mėnesinis mokėjimo dažnumas

Šioje lentelėje pateikiami pirmieji 12 mokėjimo grafiko mėnesių. Įsidėmėkite toliau pateiktą informaciją.

- Stulpelyje Laikotarpis reikšmė padidėja 1 kiekvieną mėnesį, nes kiekvienas mėnuo yra naujas sudėjimo intervalas.
- Stulpelyje Dabartinė reikšmė esančioje formulėje koeficientas padalijamas iš 12, nes per metus yra 12 sudėjimo laikotarpių. Laipsnio rodiklis (t. y., viršutinio indekso skaičius) yra lygus stulpelio Laikotarpis reikšmei.

| Laikotarpis | Mėnuo | Data       | Mokėjimo suma | Dabartinė vertė                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 2020-01-31  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>1</sup> = 49 792,53  |
| 2      | 2     | 2020-02-29  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>2</sup> = 49 585,92  |
| 3      | 3     | 2020-03-31  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>3</sup> = 49 380,17  |
| 4      | 4     | 2020-04-30  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>4</sup> = 49 175,28  |
| 5      | 5     | 2020-05-31  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>5</sup> = 48 971,23  |
| 6      | 6     | 2020-06-30  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>6</sup> = 48 768,03  |
| 7      | 7     | 2020-07-31  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>7</sup> = 48 565,67  |
| 8      | 8     | 2020-08-31  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>8</sup> = 48 364,15  |
| 9      | 9     | 2020-09-30  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>9</sup> = 48 163,47  |
| 10     | 10    | 2020-10-31 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>10</sup> = 47 963,62 |
| 11     | 11    | 2020-11-30 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>11</sup> = 47 764,61 |
| 12     | 12    | 2020-12-31 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>12</sup> = 47 566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>2 nuoma: ketvirtinis sudėjimo intervalas ir ketvirtinis mokėjimo dažnumas

Šioje lentelėje pateikiami pirmieji 12 mokėjimo grafiko mėnesių. Įsidėmėkite toliau pateiktą informaciją.

- Stulpelyje Laikotarpis reikšmė padidėja 1 kas tris mėnesius (tai yra, kas ketvirtį), nes kiekvienas ketvirtis yra naujas sudėjimo intervalas.
- Stulpelyje Dabartinė reikšmė esančioje formulėje koeficientas padalijamas iš 4, nes per metus yra keturi sudėjimo laikotarpiai. Laipsnio rodiklis yra lygus stulpelio Laikotarpis reikšmei.

| Laikotarpis | Mėnuo | Data       | Mokėjimo suma | Dabartinė vertė                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 2020-01-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 2020-02-29  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 2020-03-31  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 49 382,72 |
| 2      | 4     | 2020-04-30  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 2020-05-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 2020-06-30  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 48 773,05 |
| 3      | 7     | 2020-07-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 2020-08-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 2020-09-30  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 48 170,92 |
| 4      | 10    | 2020-10-31 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 2020-11-30 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 2020-12-31 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 47 576,21 |

> [!NOTE]
> Jei anuiteto tipas pakeičiamas į **Laikotarpio pradžios anuitetas**, mokėjimas mokamas ketvirčio pradžioje, o ne ketvirčio pabaigoje.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>3 nuoma: pusmetinis sudėjimo intervalas ir pusmetinis mokėjimo dažnumas

Šioje lentelėje pateikiami pirmieji 12 mokėjimo grafiko mėnesių. Įsidėmėkite toliau pateiktą informaciją.

- Stulpelyje Laikotarpis reikšmė padidėja 1 kas šešis mėnesius (tai yra, kas pusmetį), nes kiekvienas pusmetis yra naujas sudėjimo intervalas.
- Stulpelyje Dabartinė reikšmė esančioje formulėje koeficientas padalijamas iš 2, nes per metus yra du sudėjimo laikotarpiai. Laipsnio rodiklis yra lygus stulpelio Laikotarpis reikšmei.

| Laikotarpis | Mėnuo | Data       | Mokėjimo suma | Dabartinė vertė                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 2020-01-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 2020-02-29  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 2020-03-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 2020-04-30  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 2020-05-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 2020-06-30  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 48 780,49 |
| 2      | 7     | 2020-07-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 2020-08-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 2020-09-30  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 2020-10-31 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 2020-11-30 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 2020-12-31 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 47 590,72 |

> [!NOTE]
> Jei anuiteto tipas pakeičiamas į **Laikotarpio pradžios anuitetas**, mokėjimas mokamas sausio ir liepos mėn., o ne birželio ir gruodžio mėn.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>4 nuoma: metinis sudėjimo intervalas ir metinis mokėjimo dažnumas

Šioje lentelėje pateikiami pirmieji 12 mokėjimo grafiko mėnesių. Įsidėmėkite toliau pateiktą informaciją.

- Stulpelyje Laikotarpis reikšmė padidėja 1 kas 12 mėn. (tai yra, kas metus), nes kiekvieni metai yra naujas sudėjimo intervalas.
- Stulpelyje Dabartinė reikšmė esančioje formulėje koeficientas padalijamas iš 1, nes per metus yra vienas sudėjimo laikotarpis. Laipsnio rodiklis yra lygus stulpelio Laikotarpis reikšmei.

| Laikotarpis | Mėnuo | Data       | Mokėjimo suma | Dabartinė vertė                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 2020-01-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 2020-02-29  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 2020-03-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 2020-04-30  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 2020-05-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 2020-06-30  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 2020-07-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 2020-08-31  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 2020-09-30  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 2020-10-31 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 2020-11-30 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 2020-12-31 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 47 619,05 |

> [!NOTE]
> Jei anuiteto tipas pakeičiamas į **Laikotarpio pradžios anuitetas**, mokėjimas mokamas sausio mėn., o ne gruodžio mėn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
