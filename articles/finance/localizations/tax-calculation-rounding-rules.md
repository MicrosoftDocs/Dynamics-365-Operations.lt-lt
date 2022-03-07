---
title: Mokesčių skaičiavimo apvalinimo taisyklės
description: Šioje temoje pateikiama informacija apie mokesčių skaičiavimo tarnybos mokesčių skaičiavimo parametrų apvalinimo taisykles.
author: kailiang
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 38760879d84d8262cc1e8395c59bcbc0429bc753
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7347690"
---
# <a name="tax-calculation-rounding-rules"></a>Mokesčių skaičiavimo apvalinimo taisyklės

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie mokesčių skaičiavimo darbo mokesčių skaičiavimo parametrų apvalinimo taisykles.

> [!NOTE] 
> Kai mokesčių skaičiavimo tarnyba įgalinta, **Mokesčių kodo** ir **Mokesčių pardavimo grupės** puslapiai negalioja.

Galite peržiūrėti mokesčių skaičiavimo tarnybos apvalinimo taisyklių konfigūraciją **PVM apvalinimo taisyklės** skyriuje **Skaičiavimas** „FastTab“ **Bendri** skirtuke **mokesčių skaičiavimo parametrų** puslapio (**Mokesčio** \> **nustatymas** \> **Mokesčio konfigūracija** \> **Mokesčio skaičiavimo parametrai**).

[![Apvalinimo taisyklės konfigūracija mokesčių skaičiavimo parametrų puslapyje](./media/tax-calculation-parameters-calculation-1.png)](./media/tax-calculation-parameters-calculation-1.png)

Laukeliai **Apvalinimo tikslumo** ir **apvalinimo metodo** nustato, kaip apvalinama mokesčių skaičiavimo tarnybos apskaičiuotos mokamos sumos.

## <a name="rounding-precision"></a>Apvalinimo tikslumas

Apvalinimo **tikslumo laukai** palaiko vertę, kurios vieta iki šešių dešimtainių dalių. Pavyzdžiui, jei lauke **Apvalinimo tikslumas** į **0,000000**, pskaičiuotos sumos apvalinama iki šešių dešimtainių dalių, tada išsiunčiama „Microsoft Dynamics 365 Finance“. Pavyzdžiui, jei naudojamas **įprastas** apvalinimo metodas, suma apvalinama **987,1234567**, kad **987,123457**.

> [!NOTE]
> Finansai apvalinama pagal valiutos apvalinimo taisykles. Todėl operacijoms rodomos ir įrašytos mokesčių sumos yra paveikiamos ir mokesčių skaičiavimo apvalinimo taisyklių, ir valiutos apvalinimo taisyklių.

## <a name="rounding-method"></a>Apvalinimo metodas

Mokesčių skaičiavimo apvalinimo metodą galima konfigūruoti kiekvienam juridiniam subjektui. Lauke **Apvalinimo metodas** galite pasirinkti iš trijų pasirinkčių: **Įprasta**, **Žemyn** ir **Apvalinimas**.

### <a name="rounding-example"></a>Apvalinimo pavyzdys

Šioje lentelėje pateikiamas pavyzdys, kuriame parodyta, kaip apvalinama **987,345** suma, taikant skirtingus apvalinimo tikslumo ir apvalinimo metodų derinius.

<table>
<thead>
<tr>
<th rowspan="2">Apvalinimo metodas</th>
<th colspan="8">Apvalinimo tikslumas</th>
</tr>
<tr>
<th>0,00</th>
<th>0.01</th>
<th>0.10</th>
<th>1.00</th>
<th>10,00</th>
<th>0.02</th>
<th>0.05</th>
<th>0.25</th>
</tr>
</thead>
<tbody>
<tr>
<td>Normalus</td>
<td>987.35</td>
<td>987.35</td>
<td>987.30</td>
<td>987.00</td>
<td>990.00</td>
<td>987.34</td>
<td>987.35</td>
<td>987.25</td>
</tr>
<tr>
<td>Žemyn</td>
<td>987.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.00</td>
<td>980.00</td>
<td>987.34</td>
<td>987.30</td>
<td>987.25</td>
</tr>
<tr>
<td>Į didesnę pusę</td>
<td>988.00</td>
<td>987.35</td>
<td>987.40</td>
<td>988.00</td>
<td>990.00</td>
<td>987.36</td>
<td>987.35</td>
<td>987.50</td>
</tr>
</tbody>
</table>

Mokesčių sumų skaičiavimo ir apvalinimo logiką galima konfigūruoti pagal apmokestinimo taisykles.

## <a name="rounding-by"></a>Apvalinama pagal 

Laukelyje **Apvalinama pagal**, pasirinkite apvalinimo principą, kuris taikomas mokesčiams. Galimos toliau nurodytos parinktys:

- **Mokesčių kodai** – apvalinti mokesčio sumą kiekvieno mokesčio kodo viduje.
- **Mokesčių kodų kombinacijos** – apvalinti mokesčio sumą eilutės mokesčių kodo kombinacijoje.

## <a name="calculation-method"></a>Skaičiavimo metodas

Laukelyje **Skaičiavimo metodas** rinkitės, ar mokesčiai sąskaitoms turi būti skaičiuojami kiekvienai eilutei ar visoms. Galimos toliau nurodytos parinktys:

- **Eilutė** – skaičiuoti kiekvieno eilutės mokesčio sumą. Kiekvienos eilutės mokesčio suma nesudėta pagal kitų eilučių mokesčių sumą.
- **Bendroji suma** – apskaičiuoti mokesčio sumą visose vieno dokumento eilutėse.

### <a name="rounding-calculation-example"></a>Skaičiavimo pavyzdžio apvalinimas

Šiame pavyzdyje pateikiami skirtingi skaičiavimai, kuriuos galima atlikti vienai SF, skirtingiems apvalinimo pagal **Apvalinimas pagal** ir **verčių skaičiavimas**. Pavyzdžiui, yra šis nustatymas:

- SF yra keturios eilutės.
- Yra du mokesčių kodai: **PVM1** (10 procentų) ir **PVM2** (10 procentų).
- Apvalinimo tikslumas nustatytas **0,01**.
- Apvalinimo metodas nustatytas kaip **Apvalinimas**.

#### <a name="rounding-by--tax-codes-and-calculation-method--line"></a>Apvalinimas pagal = Mokesčių kodai ir skaičiavimo metodas = eilutė

| Eilutės numeris | Grynoji eilutės suma | Nustatyti mokesčių kodai | Mokesčio suma prieš apvalinti | Suapvalinta mokesčių suma |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | 1 PVM                 | 1.111                      | 1.12               |
| 2           | 22,22           | PVM1; 2 PVM           | 2,222; 2,222               | 2,23; 2,23         |
| 3           | 33.33           | 1 PVM                 | 3.333                      | 3.34               |
| 4           | 44.44           | PVM1; 2 PVM           | 4,444; 4;444               | 4,45; 4,45         |

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--line"></a>Apvalinimas pagal = Mokesčių kodų kombinacijos ir skaičiavimo metodas = eilutė

| Eilutės numeris | Grynoji eilutės suma | Nustatyti mokesčių kodai | Mokesčio suma prieš apvalinti | Suapvalinta mokesčių suma |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | 1 PVM                 | 1.111                      | 1.12               |
| 2\*         | 22,22           | PVM1; 2 PVM           | 2,222; 2,222               | 2,23; 2,22         |
| 3           | 33.33           | 1 PVM                 | 3.333                      | 3.34               |
| 4\*\*       | 44.44           | PVM1; 2 PVM           | 4,444; 4;444               | 4,45; 4,44         |

\*2 eilutė = \[22,22 × (10 procentų + 10 procentų) \] = 2,23 + 2,22

\*\* Eilutė 4 = Apvalinimas\[44,44 × (10 procentai + 10 procentai)\] = 4,45 + 4,44

#### <a name="rounding-by--tax-codes-and-calculation-method--total"></a>Apvalinimas pagal = Mokesčių kodai ir skaičiavimo metodas = Iš viso

| Eilutės numeris | Grynoji eilutės suma | Nustatyti mokesčių kodai | Mokesčio suma prieš apvalinti | Suapvalinta mokesčių suma |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1           | 11.11           | 1 PVM\*               | 1.111                      | 1.12               |
| 2           | 22,22           | 1 PVM\*; 2 PVM\*\*     | 2,222; 2,222               | 2,22; 2,23         |
| 3           | 33.33           | 1 PVM\*               | 3.333                      | 3.33               |
| 4           | 44,44           | 1 PVM\*; 2 PVM\*\*     | 4,444; 4;444               | 4,44; 4,44         |

\* PVM 1(eilutė 1, Line 2, Line 3, eilutė 4) = Apvalinimas\[(11,11 + 22,22 + 33,33 + 44,44) × 10 procentai\] = 1,12 + 2,22 + 3,33 + 4,44

\*\*PVM2(2 eilutė, 4 eilutė) = \[apvalinimas (22,22 + 44,44) × 10 procentų \] = 2,23 + 4,44

#### <a name="rounding-by--tax-code-combinations-and-calculation-method--total"></a>Apvalinimas pagal = Mokesčių kodų kombinacijos ir skaičiavimo metodas = Iš viso

| Eilutės numeris | Grynoji eilutės suma | Nustatyti mokesčių kodai | Mokesčio suma prieš apvalinti | Suapvalinta mokesčių suma |
|-------------|-----------------|----------------------|----------------------------|--------------------|
| 1\*         | 11.11           | 1 PVM                 | 1.111                      | 1.12               |
| 2\*\*       | 22.22           | PVM1; 2 PVM           | 2,222; 2,222               | 2,23; 2,22         |
| 3\*         | 33.33           | 1 PVM                 | 3.333                      | 3.33               |
| 4\*\*       | 44,44           | PVM1; 2 PVM           | 4,444; 4;444               | 4,44; 4,45         |

\* eilutė 1, eilutė 3 = Apvalinimas\[(11,11 + 33,33) × 10 procentų\] = 1,12 + 3,33

\*\* eilutė 2, eilutė 4 = apvalinimas\[(22,22 + 44,44) × (10 procentų + 10 procentų)\] = 2,23 + 2,22 + 4,44 + 4,45

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
