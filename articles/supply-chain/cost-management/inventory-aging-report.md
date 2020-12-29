---
title: Atsargų skirstymo pagal terminus ataskaitos pavyzdžiai ir logika
description: Šioje temoje pateikiami pavyzdžiai, rodantys, kaip interpretuoti atsargų skirstymo pagal terminus ataskaitos rezultatus.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6e708e4dc818f20fc8d835053da75c2fe9c98f6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433574"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Atsargų skirstymo pagal terminus ataskaitos pavyzdžiai ir logika

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami pavyzdžiai, rodantys, kaip interpretuoti **Atsargų skirstymas pagal terminus** ataskaitos rezultatus. Ši ataskaita sugrupuoja turimos pasirinktos prekės arba prekių grupės kiekį ir atsargų vertes į kelių laikotarpių rinkinius. Šioje temoje taip pat parodoma vidinė ataskaitos logika.

Šioje temoje pateikiami rezultatai rodo rezultatus, kurie pateikiami standartinėje **Atsargų skirstymas pagal terminus** ataskaitoje. Tačiau bendrai rekomenduojame naudoti [Atsargų skirstymo pagal terminus ataskaitos saugyklos](inventory-aging-report-storage.md) versiją, ypač jei turite daug prekių ir sandėlių, kuriuos reikia sutvarkyti. Atsargų skirstymo pagal terminus ataskaitos saugykla išsaugo kiekvieną jūsų sukurtą ataskaitą, parodo rezultatus kaip interaktyvų puslapį ir diagramą ir leidžia eksportuoti visas įrašytas ataskaitas.

## <a name="sample-data-that-is-used-in-these-examples"></a>Duomenų, naudojamų šiuose pavyzdžiuose, pavyzdys

Šios temos pavyzdžiai pagrįsti atsargų operacijų duomenų pavyzdžiu, aprašytu šioje dalyje.

### <a name="storage-dimension-setup"></a>Saugyklos dimensijos nustatymas

Pavyzdžio sistemoje yra šie saugyklos dimensijų nustatymai.

| Pavadinimas arba vardas ir pavardė      | Aktyvi | Faktinės atsargos | Finansinės atsargos |
|-----------|--------|--------------------|---------------------|
| Vieta      | Taip    | Taip                | Taip                 |
| Sandėlis | Taip    | Taip                | nr.                  |

### <a name="inventory-model"></a>Atsargų modelis

Pavyzdinėje sistemoje išleistų produktų atsargų modelis yra *FIFO*, o **Savikaina** atsargų modelio parametras yra *Apima faktinę vertę*.

### <a name="inventory-transactions"></a>Atsargų operacijos

Pavyzdžio sistemoje yra šios išleisto produkto atsargų operacijos, kurio prekės numeris *1000*.

| Nuoroda      | Vieta | Sandėlis | Gavimas   | Išdavimas | Faktinė data | Fin. data | Kiekis | Išlaidų suma | Fakt. išlaidų suma |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Pirkimo užsakymas | 1    | 11        | Nupirkta |       | 15 m. kovo mėn.      | 15 m. kovo mėn.       | 10       | 1000       | 1000                |
| Pirkimo užsakymas | 2    | 21        | Nupirkta |       | 15 m. kovo mėn.      | 15 m. kovo mėn.       | 10       | 2,000       | 2,000                |
| Pirkimo užsakymas | 1    | 11        | Gauta  |       | 15 m. balandžio mėn.      |                | 5        |             | 375                  |
| Perkėlimo užsakymas | 1    | 11        |           | Parduota  | 2 m. gegužės mėn.         | 2 m. gegužės mėn.          | -5       | -458,33     | -458,33              |
| Perkėlimo užsakymas | 1    | 12        | Nupirkta |       | 2 m. gegužės mėn.         | 2 m. gegužės mėn.          | 5        | 458.33      | 458.33               |
| Pardavimo užsakymas    | 1    | 12        |           | Parduota  | 3 m. gegužės mėn.         | 3 m. gegužės mėn.          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Kaip apskaičiuojami kiekvieno laikotarpio rinkinio kiekiai ir sumos

Naudodami ankstesniuose skyriuose aprašytus duomenų pavyzdžius, galite paleisti **Atsargų skirstymas pagal terminus** ataskaitą, nustatytą pagal šiuos parametrus:

- **Nuo datos:** *2020 m. gegužės 9 d.*
- **Vieta:** *Rodinys*
- **Sandėlis:** *Ne*
- **Prekės numeris:** *Iš viso*
- **Skirstymo pagal terminus laikotarpis:** nustatykite šį lauką, kad būtų generuojami mėnesio rinkiniai.

Šiuo atveju sugeneruotos ataskaitos turinys bus panašus į šį pavyzdį.

<table>
<thead>
<tr>
    <th rowspan="2">Prekės Nr.</th>
    <th rowspan="2">Vieta</th>
    <th rowspan="2">Turimas kiekis</th>
    <th rowspan="2">Turima vertė</th>
    <th rowspan="2">Atsargų vertės kiekis</th>
    <th rowspan="2">Atsargų vertė</th>
    <th rowspan="2">Vidutinė vieneto savikaina</th>
    <th colspan="2">2020-05-01–2020-05-08 </th>
    <th colspan="2">2020-04-01–2020-04-30</th>
    <th colspan="2">2020-03-01–2020-03-31</th>
</tr>
<tr>
    <th>P1:Kiekis</th>
    <th>P1:Suma</th>
    <th>P2:Kiekis</th>
    <th>P2:Suma</th>
    <th>P3:Kiekis</th>
    <th>P3:Suma</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 bendros sumos</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Atkreipkite dėmesį į šią išsamią informaciją šio pavyzdžio ataskaitoje:

- **Atsargų vertės kiekis**, **Atsargų vertė** ir **Vidutinė vieneto savikaina** ataskaitoje rodomos vertės yra finansinių atsargų dimensijų ( šiuo atveju, **Vieta**) vertės.

    Pavyzdžiui, 1-oje vietoje ataskaitoje pateikiama ši informacija:

    - **Atsargų verčių kiekis** vertė yra *14* (= 10 + 5 – 5 + 5 – 1).
    - **Atsargų vertė** vertė yra *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).
    - **Vidutinė vieneto savikaina** vertė yra *91,67*.
    - **Turima vertė** vertė ir **Suma** vertė kiekviename laikotarpio rinkinyje yra apskaičiuojama naudojant **Vidutinė vieneto savikaina** vertę.

- Ši ataskaita apibrėžia turimą kiekvieno laikotarpio rinkinio kiekį apibendrindama bendrą gautų atsargų kiekį kiekvienam laikotarpio rinkiniui. Tada taikoma pirmas ateina, pirmas išeina (FIFO) principas norint atskaityti visą išduotą kiekį, neatsižvelgiant į atsargų modelį, kurį naudoja prekės.

Jei tą pačią ataskaitą paleidote iš naujo, šį kartą nustatykite tiek **Vieta**, tiek **Sandėlis** laukus į *Peržiūrėti*, kad nauja ataskaita būtų panaši į toliau pateiktą pavyzdį.

<table>
<thead>
<tr>
    <th rowspan="2">Prekės Nr.</th>
    <th rowspan="2">Vieta</th>
    <th rowspan="2">Sandėlis</th>
    <th rowspan="2">Turimas kiekis</th>
    <th rowspan="2">Turima vertė</th>
    <th rowspan="2">Atsargų vertės kiekis</th>
    <th rowspan="2">Atsargų vertė</th>
    <th rowspan="2">Vidutinė vieneto savikaina</th>
    <th colspan="2">2020-05-01–2020-05-08 </th>
    <th colspan="2">2020-04-01–2020-04-30</th>
    <th colspan="2">2020-03-01–2020-03-31</th>
</tr>
<tr>
    <th>P1:Kiekis</th>
    <th>P1:Suma</th>
    <th>P2:Kiekis</th>
    <th>P2:Suma</th>
    <th>P3:Kiekis</th>
    <th>P3:Suma</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 bendros sumos</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Šį kartą 1-a vieta yra padalinama į dvi eiles: vieną 11-am sandėliui ir vieną 12-am sandėliui. Tačiau **Atsargų vertės kiekis**, **Atsargų vertė** ir **Vidutinė vieneto savikaina** vertės yra tos pačios, nes **Sandėlis** nėra finansinė atsargų dimensija.

Be to, atkreipkite dėmesį, kad 1-os vietos kiekio paskirstymas skiriasi. Pirmoje jūsų paleistoje ataskaitoje sistema nepaisė perkėlimo užsakymo, įvykusio toje pačioje vietoje, ir išskaitė pardavimo sąskaitos faktūros kiekį iš **2020-03-01-2020-03-31** laikotarpio rinkinį 1-oje vietoje. Tačiau naujoje ataskaitoje sistema išskaito pardavimo sąskaitos faktūros kiekį iš **2020-05-01–2020-05-08** laikotarpio rinkinio 12-ame sandėlyje.

## <a name="effects-of-inventory-closing"></a>Atsargų uždarymo pasekmės

Jeigu įvykdėte atsargų uždarymą gegužės mėnesiui, o tada dar kartą paleidote ankstesnę ataskaitą, bet nustatėte **Nuo datos** lauką į *2020 m. gegužės 31 d.*, pastebėsite šiuos rezultatus:

- **Atsargų vertė** ir **Vidutinė vieneto savikaina** vertės atnaujintos.
- **Turima vertė** vertė ir visos **Suma** vertės kiekviename laikotarpio rinkinyje yra atitinkamai atnaujinamos.

Naujoji ataskaita bus panaši į toliau pateiktą pavyzdį.

<table>
<thead>
<tr>
    <th rowspan="2">Prekės Nr.</th>
    <th rowspan="2">Vieta</th>
    <th rowspan="2">Sandėlis</th>
    <th rowspan="2">Turimas kiekis</th>
    <th rowspan="2">Turima vertė</th>
    <th rowspan="2">Atsargų vertės kiekis</th>
    <th rowspan="2">Atsargų vertė</th>
    <th rowspan="2">Vidutinė vieneto savikaina</th>
    <th colspan="2">2020-05-01–2020-05-31 </th>
    <th colspan="2">2020-04-01–2020-04-30</th>
    <th colspan="2">2020-03-01–2020-03-31</th>
</tr>
<tr>
    <th>P1:Kiekis</th>
    <th>P1:Suma</th>
    <th>P2:Kiekis</th>
    <th>P2:Suma</th>
    <th>P3:Kiekis</th>
    <th>P3:Suma</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0,00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 bendros sumos</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>
