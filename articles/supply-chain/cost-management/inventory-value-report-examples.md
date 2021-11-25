---
title: Atsargų vertės ataskaitos pavyzdžiai ir logika
description: Šioje temoje pateikiami keli rezultatų, pateikiamų kiekvieno tipo atsargų vertės ataskaitoje, pavyzdžiai. Atsargų vertės ataskaitose pateikiama informacija apie faktines ir finansines jūsų atsargų kiekius ir sumas.
author: banluo-ms
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: banluo
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4ad85058c8743895185d3da2e8975711f1e3bc2c
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798408"
---
# <a name="inventory-value-report-examples-and-logic"></a>Atsargų vertės ataskaitos pavyzdžiai ir logika

[!include [banner](../includes/banner.md)]

Atsargų vertės ataskaitose pateikiama informacija apie faktines ir finansines jūsų atsargų kiekius ir sumas. Šioje temoje pateikiami keli rezultatų, pateikiamų kiekvieno tipo atsargų vertės ataskaitoje, pavyzdžiai.

Daugiau informacijos apie tai, kaip generuoti ir naudoti kiekvieno tipo atsargų vertės ataskaitą, ieškokite [Inventory value reports](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Duomenų, naudojamų šiuose pavyzdžiuose, pavyzdys

Šios temos pavyzdžiai pagrįsti atsargų operacijų duomenų pavyzdžiu, aprašytu šioje dalyje.

### <a name="storage-dimension-setup"></a>Saugyklos dimensijos nustatymas

Pavyzdžio sistemoje yra šie saugyklos dimensijų nustatymai.

| Pavadinimas arba vardas ir pavardė | Aktyvi | Faktinės atsargos | Finansinės atsargos |
|---|---|---|---|
| Vieta | Taip | Taip | Taip |
| Sandėlis | Taip | Taip | nr. |

### <a name="inventory-model"></a>Atsargų modelis

Sistemos pavyzdyje išleistų produktų atsargų modelis yra *FIFO*, o atsargų modelio **laukas Savikaina nustatytas kaip Įtraukti** *faktinę vertę*.

### <a name="inventory-transactions"></a>Atsargų operacijos

Sistemos pavyzdyje yra šios išleisto produkto, kurio prekės numeris *yra B0001, atsargų* operacijos.

| Nuoroda | Teritorija | Sandėlis | Gavimas | Problema | Faktinė data | Finansinė data | Kiekis | Išlaidų suma | Faktinių išlaidų suma |
|---|---|---|---|---|---|---|---|---|---|
| Pirkimo užsakymas | 1 | 11 | Nupirkta | | kovo mėn. 15 d. | kovo mėn. 15 d. | 10 | 1000 | 1000 |
| Pirkimo užsakymas | 2 | 21 | Nupirkta | | kovo mėn. 15 d. | kovo mėn. 15 d. | 10 | 2,000 | 2,000 |
| Pirkimo užsakymas | 1 | 11 | Gauta | | balandžio mėn. 15 d.  | | 5 | | 375 |
| Perkėlimo užsakymas | 1 | 11 | | Parduota | gegužės mėn. 2 d. | gegužės mėn. 2 d. | -5 | -458,33 | -458,33 |
| Perkėlimo užsakymas | 1 | 12 | Nupirkta | | gegužės mėn. 2 d. | gegužės mėn. 2 d. | 5 | 458.33 | 458.33 |
| Pardavimo užsakymas | 1 | 12 | | Parduota | gegužės mėn. 3 d. | gegužės mėn. 3 d. | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Atsargų vertės ataskaitos konfigūracija

Sistemos pavyzdyje yra atsargų vertės ataskaitos konfigūracija, turinti šiuos parametrus:

- **Diapazonas:** *registravimo data*
- **Atsargos:** *Taip*
- **Skaičiuoti vidutinę vieneto savikainą:** *Taip*
- **Bendras kiekis ir vertė:** *Taip*
- **Svetainė, rodinys:** *pasirinkta*
- **Ištekliaus ID, rodinys:** *Taip*
- **Lygis:** *bendrosios sumos*

## <a name="inventory-value-report-example-1"></a>1 atsargų vertės ataskaitos pavyzdys

Šioje lentelėje ir iliustracijose rodomi rezultatai, kai naudojate duomenų pavyzdžius ir ataskaitos konfigūraciją, aprašytus anksčiau šioje temoje.

| Išteklių tipas | Ištekliai | Teritorija | Nuoroda | Atsargos: finansinis kiekis | Atsargos: finansinė suma | Atsargos: faktinis užregistruotas kiekis | Atsargos: faktinė užregistruota suma | Atsargos: kiekis | Atsargos: suma | Vidutinė vieneto savikaina |
|---|---|---|---|---|---|---|---|---|---|---|
| Medžiaga | B0001 | 1 | Pabaigos likutis | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Medžiaga | B0001 | 2 | Pabaigos likutis | 10,00 | 2 000,00 | 0,00 | 0,00 | 10,00 | 2 000,00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standartinė atsargų vertės ataskaita, pvz., 1

Šioje iliustracijoje parodyta standartinė **atsargų vertės** ataskaita, pvz., 1. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Atsargų vertės ataskaita, pvz., 1.](media/inventory-value-report-ex1-small.png "Atsargų vertės ataskaita, pvz., 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 1

Šioje iliustracijoje parodyta **atsargų vertės ataskaitos saugojimo** ataskaita, pvz., 1. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 1.](media/inventory-value-report-storage-ex1-small.png "Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>2 atsargų vertės ataskaitos pavyzdys

Šioje lentelėje ir iliustracijose rodomi rezultatai, kai naudojate duomenų pavyzdžius, aprašytus anksčiau šioje temoje, bet ataskaitos konfigūracijoje pakeičiate lauko Lygis reikšmę **·** į *·* Operacijos, o **·** paleidę ataskaitą nustatote lauką Nuo datos į *kovo 15* d.

| Išteklių tipas | Ištekliai | Teritorija | Data | Skaičius | Nuoroda | Atsargos: finansinis kiekis | Atsargos: finansinė suma | Atsargos: faktinis užregistruotas kiekis | Atsargos: faktinė užregistruota suma | Atsargos: kiekis | Atsargos: suma |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Medžiaga | B0001 | 1 | 3/15/2021 | 00000126 | Pirkimo užsakymas | 0,00 | 0,00 | 10,00 | 1,000.00 | **10.00** | **1,000.00** |
| Medžiaga | B0001 | 1 | 3/15/2021 | 00000126 | Pirkimo užsakymas | 10,00 | 1,000.00 | -10.00 | -1,000.00 | **0.00** | **0.00** |
| Medžiaga | B0001 | 1 | 4/15/2021 | 00000128 | Pirkimo užsakymas | 0,00 | 0,00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Medžiaga | B0001 | 1 | 5/2/2021 | 000003 | Perkėlimo užsakymo siuntimas | –5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |
| Medžiaga | B0001 | 1 | 5/2/2021 | 000003 | Perkėlimo užsakymo gavimas | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Medžiaga | B0001 | 1 | 5/3/2021 | 000835 | Pardavimo užsakymas | 0,00 | 0,00 | –1,00 | -91,67 | **-1.00** | **-91.67** |
| Medžiaga | B0001 | 1 | 5/3/2021 | 000835 | Pardavimo užsakymas | –1,00 | -91,67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Medžiaga | B0001 | 2 | 3/15/2021 | 00000127 | Pirkimo užsakymas | 0,00 | 0,00 | 10,00 | 2 000,00 | **10.00** | **2,000.00** |
| Medžiaga | B0001 | 2 | 3/15/2021 | 00000127 | Pirkimo užsakymas | 10,00 | 2 000,00 | -10.00 | -2000,00. | **0.00** | **0.00** |
| Medžiaga | B0001 | 2 | 5/2/2021 | 000003 | Perkėlimo užsakymo siuntimas | 5.00 | 458.33 | 0,00 | 0,00 | **5.00** | **458.33** |
| Medžiaga | B0001 | 2 | 5/2/2021 | 000003 | Perkėlimo užsakymo gavimas | –5,00 | -458,33 | 0,00 | 0,00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Standartinė atsargų vertės ataskaita, pvz., 2

Šioje iliustracijoje parodyta standartinė **atsargų vertės** ataskaita, pvz., 2. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Atsargų vertės ataskaita, pvz., 2.](media/inventory-value-report-ex2-small.png "Atsargų vertės ataskaita, pvz., 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 2

Šioje iliustracijoje parodyta **atsargų vertės ataskaitos saugojimo** ataskaita, pvz., 2. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 2.](media/inventory-value-report-storage-ex2-small.png "Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>3 atsargų vertės ataskaitos pavyzdys

Rekomenduojame paleisti atsargų vertės ataskaitas po perskaičiavimo arba atsargų uždarymo, kad turėtumėte operacijas ir sumas, kurioms turi įtakos perskaičiavimas arba atsargų uždarymas.

Tolesniuose poskyriuose rodomos atsargų vertės ataskaitos, sugeneruotos uždarius atsargas iki gegužės 30 d.

### <a name="example-3-when-the-totals-level-is-used"></a>3 pavyzdys, kai naudojamas sumavimo lygis

Šioje lentelėje pateikiami rezultatai, kai naudojate duomenų pavyzdžius ir ataskaitos konfigūraciją, aprašytus anksčiau šioje temoje. (Toje ataskaitos konfigūracijoje **Lygio** laukas nustatytas kaip Sumos *·* .)

| Išteklių tipas | Ištekliai | Teritorija | Nuoroda | Atsargos: finansinis kiekis | Atsargos: finansinė suma | Atsargos: faktinis užregistruotas kiekis | Atsargos: faktinė užregistruota suma | Atsargos: kiekis | Atsargos: suma | Vidutinė vieneto savikaina |
|---|---|---|---|---|---|---|---|---|---|---|
| Medžiaga | B0001 | 1 | Pabaigos likutis | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Medžiaga | B0001 | 2 | Pabaigos likutis | 10,00 | 2 000,00 | 0,00 | 0,00 | 10,00 | 2 000,00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>3 pavyzdys, kai naudojamas operacijų lygis

Šioje lentelėje pateikiami rezultatai, kai naudojate duomenų pavyzdžius, aprašytus anksčiau šioje temoje, bet ataskaitos konfigūracijoje lauko Lygis reikšmę keičiate **·** į *·* Operacijos.

| Išteklių tipas | Ištekliai | Teritorija | Data | Skaičius | Nuoroda | Atsargos: finansinis kiekis | Atsargos: finansinė suma | Atsargos: faktinis užregistruotas kiekis | Atsargos: faktinė užregistruota suma | Atsargos: kiekis | Atsargos: suma |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Medžiaga | B0001 | 1 | 3/15/2021 | 00000126 | Pirkimo užsakymas | 0,00 | 0,00 | 10,00 | 1,000.00 | 10,00 | 1,000.00 |
| Medžiaga | B0001 | 1 | 3/15/2021 | 00000126 | Pirkimo užsakymas | 10,00 | 1,000.00 | -10.00 | -1,000.00 | 0,00 | 0,00 |
| Medžiaga | B0001 | 1 | 4/15/2021 | 00000128 | Pirkimo užsakymas | 0,00 | 0,00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Medžiaga | B0001 | 1 | 5/2/2021 | 000003 | Perkėlimo užsakymo siuntimas | –5,00 | -458,33 | 0,00 | 0,00 | –5,00 | -458,33 |
| Medžiaga | B0001 | 1 | 5/2/2021 | 000003 | Perkėlimo užsakymo gavimas | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Medžiaga | B0001 | 1 | 5/3/2021 | 000835 | Pardavimo užsakymas | 0,00 | 0,00 | –1,00 | -91,67 | –1,00 | -91,67 |
| Medžiaga | B0001 | 1 | 5/3/2021 | 000835 | Pardavimo užsakymas | –1,00 | -91,67 | 1.00 | 91.67 | 0,00 | 0,00 |
| Medžiaga | B0001 | 1 | 5/31/2021 | 000835 | Pardavimo užsakymas | 0,00 | -8.33 | 0,00 | 0,00 | 0,00 | -8.33 |
| Medžiaga | B0001 | 1 | 5/31/2021 | 000003 | Perkėlimo užsakymo siuntimas | 0,00 | -41.67 | 0,00 | 0,00 | 0,00 | -41.67 |
| Medžiaga | B0001 | 1 | 5/31/2021 | 000003 | Perkėlimo užsakymo gavimas | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Medžiaga | B0001 | 2 | 3/15/2021 | 00000127 | Pirkimo užsakymas | 0,00 | 0,00 | 10,00 | 2 000,00 | 10,00 | 2 000,00 |
| Medžiaga | B0001 | 2 | 3/15/2021 | 00000127 | Pirkimo užsakymas | 10,00 | 2 000,00 | -10.00 | -2000,00. | 0,00 | 0,00 |
| Medžiaga | B0001 | 2 | 5/2/2021 | 000003 | Perkėlimo užsakymo siuntimas | 5.00 | 458.33 | 0,00 | 0,00 | 5.00 | 458.33 |
| Medžiaga | B0001 | 2 | 5/2/2021 | 000003 | Perkėlimo užsakymo gavimas | –5,00 | -458,33 | 0,00 | 0,00 | –5,00 | -458,33 |
| Medžiaga | B0001 | 2 | 5/31/2021 | 000003 | Perkėlimo užsakymo siuntimas | 0,00 | 41.67 | 0,00 | 0,00 | 0,00 | 41.67 |
| Medžiaga | B0001 | 2 | 5/31/2021 | 000003 | Perkėlimo užsakymo gavimas | 0,00 | -41.67 | 0,00 | 0,00 | 0,00 | -41.67 |
