---
title: Atsargų vertės ataskaitos pavyzdžiai ir logika
description: Šiame straipsnyje pateikiami kai kurie rezultatų, kurie pateikiami kiekvieno tipo atsargų vertės ataskaitoje, pavyzdžiai. Atsargų vertės ataskaitose pateikiama informacija apie faktines ir finansines jūsų atsargų kiekius ir sumas.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e6c6387be5204fde6ebc7a4983567801900974af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877659"
---
# <a name="inventory-value-report-examples-and-logic"></a>Atsargų vertės ataskaitos pavyzdžiai ir logika

[!include [banner](../includes/banner.md)]

Atsargų vertės ataskaitose pateikiama informacija apie faktines ir finansines jūsų atsargų kiekius ir sumas. Šiame straipsnyje pateikiami kai kurie rezultatų, kurie pateikiami kiekvieno tipo atsargų vertės ataskaitoje, pavyzdžiai.

Daugiau informacijos apie tai, kaip generuoti ir naudoti kiekvieną atsargų vertės ataskaitos tipą, ieškokite [atsargų vertės ataskaitose](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Duomenų, naudojamų šiuose pavyzdžiuose, pavyzdys

Šiame straipsnyje pateikti pavyzdžiai pagrįsti atsargų operacijų duomenų pavyzdžiais, aprašytais šiame skyriuje.

### <a name="storage-dimension-setup"></a>Saugyklos dimensijos nustatymas

Pavyzdžio sistemoje yra šie saugyklos dimensijų nustatymai.

| Pavadinimas arba vardas ir pavardė | Aktyvi | Faktinės atsargos | Finansinės atsargos |
|---|---|---|---|
| Vieta | Taip | Taip | Taip |
| Sandėlis | Taip | Taip | Ne |

### <a name="inventory-model"></a>Atsargų modelis

Pavyzdžiui, sistemos išleistų produktų *atsargų modelis yra FIFO*, **·** *o atsargų modelio savikainos laukas nustatytas į Įtraukti fizinę vertę*.

### <a name="inventory-transactions"></a>Atsargų operacijos

Pavyzdyje sistema apima šias išleisto produkto, kurio prekės numeris *B0001, atsargų operacijas*.

| Nuoroda | Svetainė | Sandėlis | Gavimas | Problema | Faktinė data | Finansinė data | Kiekis | Išlaidų suma | Faktinių išlaidų suma |
|---|---|---|---|---|---|---|---|---|---|
| Pirkimo užsakymas | 1 | 11 | Nupirkta | | kovo mėn. 15 d. | kovo mėn. 15 d. | 10 | 1000 | 1000 |
| Pirkimo užsakymas | 2 | 21 | Nupirkta | | kovo mėn. 15 d. | kovo mėn. 15 d. | 10 | 2,000 | 2,000 |
| Pirkimo užsakymas | 1 | 11 | Gauta | | balandžio mėn. 15 d.  | | 5 | | 375 |
| Perkėlimo užsakymas | 1 | 11 | | Parduota | gegužės mėn. 2 d. | gegužės mėn. 2 d. | -5 | -458,33 | -458,33 |
| Perkėlimo užsakymas | 1 | 12 | Nupirkta | | gegužės mėn. 2 d. | gegužės mėn. 2 d. | 5 | 458.33 | 458.33 |
| Pardavimo užsakymas | 1 | 12 | | Parduota | gegužės mėn. 3 d. | gegužės mėn. 3 d. | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Atsargų vertės ataskaitos konfigūravimas

Pavyzdyje sistema apima atsargų vertės ataskaitos konfigūraciją, kuri turi šiuos parametrus:

- **Diapazonas:** *registravimo data*
- **Atsargos:** *taip*
- **Skaičiuoti vidutinę vieneto savikainą:** *taip*
- **Bendras kiekis ir vertė:** *taip*
- **Svetainė, rodinys:** *pasirinkta*
- **Išteklių ID, rodinys:** *taip*
- **Lygis:** *bendrosios sumos*

## <a name="inventory-value-report-example-1"></a>1 atsargų vertės ataskaitos pavyzdys

Toliau pateikiamoje lentelėje ir iliustracijoje pateikiami rezultatai, kai naudojate pavyzdinį duomenų pavyzdį ir ataskaitos konfigūraciją, aprašytus anksčiau šiame straipsnyje.

| Išteklių tipas | Ištekliai | Svetainė | Nuoroda | Atsargos: finansinis kiekis | Atsargos: finansinė suma | Atsargos: faktinis užregistruotas kiekis | Atsargos: faktinė užregistruota suma | Atsargos: kiekis | Atsargos: suma | Vidutinė vieneto savikaina |
|---|---|---|---|---|---|---|---|---|---|---|
| Medžiaga | B0001 | 1 | Pabaigos likutis | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Medžiaga | B0001 | 2 | Pabaigos likutis | 10,00 | 2 000,00 | 0,00 | 0,00 | 10,00 | 2 000,00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standartinė atsargų vertės ataskaita, pvz., 1

Ši iliustracija rodo standartinę **atsargų vertės ataskaitą**, pvz., 1. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Atsargų vertės ataskaita, pvz., 1.](media/inventory-value-report-ex1-small.png "1 atsargų vertės ataskaita")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 1

Toliau pateikta iliustracija rodo **atsargų vertės ataskaitos saugojimo ataskaitą**, pvz., 1. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 1.](media/inventory-value-report-storage-ex1-small.png "Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>2 atsargų vertės ataskaitos pavyzdys

Ši lentelė ir iliustracijos rodo rezultatus, kai naudojate pavyzdinį duomenis, kurie aprašomi anksčiau šiame straipsnyje, tačiau pakeičiate lauko Level vertę į Operacijos ataskaitos konfigūracijoje ir ataskaitos konfigūravimo metu nustatote lauką Nuo datos į kovo 15 d., **·** *·* **·** *kai paleidžiate ataskaitą.*

| Išteklių tipas | Ištekliai | Svetainė | Data | Skaičius | Nuoroda | Atsargos: finansinis kiekis | Atsargos: finansinė suma | Atsargos: faktinis užregistruotas kiekis | Atsargos: faktinė užregistruota suma | Atsargos: kiekis | Atsargos: suma |
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

Ši iliustracija rodo standartinę **atsargų vertės ataskaitą**, pvz., 2. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Atsargų vertės ataskaita, pvz., 2.](media/inventory-value-report-ex2-small.png "2 atsargų vertės ataskaita")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 2

Toliau pateikta iliustracija rodo **atsargų vertės ataskaitos saugojimo ataskaitą**, pvz., 2. (Norėdami atidaryti didesnę versiją pasirinkite pavyzdį.)

[![Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 2.](media/inventory-value-report-storage-ex2-small.png "Atsargų vertės ataskaitos saugojimo ataskaita, pvz., 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>3 atsargų vertės ataskaitos pavyzdys

Rekomenduojama vykdyti atsargų vertės ataskaitas po perskaičiavimo arba atsargų uždarymo, kad būtų galima vykdyti operacijas ir sumas, paveiktas perskaičiavimo ar atsargų uždarymo.

Toliau pateikti poskyriai rodo atsargų vertės ataskaitas, sugeneruotas uždarius atsargas iki gegužės 30 d.

### <a name="example-3-when-the-totals-level-is-used"></a>3 pavyzdys, kai naudojamas bendrųjų sumų lygis

Toliau pateikiamoje lentelėje pateikiami rezultatai, kai naudojate pavyzdinį duomenų ir ataskaitos konfigūraciją, aprašytus anksčiau šiame straipsnyje. (Šioje ataskaitos konfigūracijoje **Lauke** Level nustatyta bendroji *suma*.)

| Išteklių tipas | Ištekliai | Svetainė | Nuoroda | Atsargos: finansinis kiekis | Atsargos: finansinė suma | Atsargos: faktinis užregistruotas kiekis | Atsargos: faktinė užregistruota suma | Atsargos: kiekis | Atsargos: suma | Vidutinė vieneto savikaina |
|---|---|---|---|---|---|---|---|---|---|---|
| Medžiaga | B0001 | 1 | Pabaigos likutis | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Medžiaga | B0001 | 2 | Pabaigos likutis | 10,00 | 2 000,00 | 0,00 | 0,00 | 10,00 | 2 000,00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>3 pavyzdys, kai naudojamas operacijų lygis

Toliau pateikiamoje lentelėje pateikiami rezultatai, kai naudojate pavyzdinį duomenų pavyzdį, kuris aprašytas anksčiau šiame straipsnyje, **·** *tačiau* lauko Lygis vertę pakeičiate į Ataskaitos konfigūracijos operacijos.

| Išteklių tipas | Ištekliai | Svetainė | Data | Skaičius | Nuoroda | Atsargos: finansinis kiekis | Atsargos: finansinė suma | Atsargos: faktinis užregistruotas kiekis | Atsargos: faktinė užregistruota suma | Atsargos: kiekis | Atsargos: suma |
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
