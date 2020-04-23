---
title: Produkto konfigūravimo modelių išraiškos ir lentelės apribojimai
description: Šioje temoje apžvelgiamas išraiškos ir lentelės apribojimų naudojimas. Apribojimais valdomos atributo reikšmės, kurias galite pasirinkti konfigūruodami pardavimo užsakymo, pardavimo pasiūlymo, pirkimo užsakymo arba gamybos užsakymo produktus. Galite naudoti išraiškos apribojimus arba lentelės apribojimus atsižvelgdami į tai, kaip norite sukurti apribojimus.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d85d10113e7cc4e95a25efe7fee6d1f23990694
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208482"
---
# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Produkto konfigūravimo modelių išraiškos ir lentelės apribojimai

[!include [banner](../includes/banner.md)]

Šioje temoje apžvelgiamas išraiškos ir lentelės apribojimų naudojimas. Apribojimais valdomos atributo reikšmės, kurias galite pasirinkti konfigūruodami pardavimo užsakymo, pardavimo pasiūlymo, pirkimo užsakymo arba gamybos užsakymo produktus. Galite naudoti išraiškos apribojimus arba lentelės apribojimus atsižvelgdami į tai, kaip norite sukurti apribojimus. 

Apribojimais valdomos atributo reikšmės, kurias galite pasirinkti konfigūruodami pardavimo užsakymo, pardavimo pasiūlymo, pirkimo užsakymo arba gamybos užsakymo produktus. Galite naudoti išraiškos apribojimus arba lentelės apribojimus atsižvelgdami į tai, kaip norite sukurti apribojimus.

## <a name="what-are-expression-constraints"></a>Kas yra išraiškos apribojimai?
Išraiškos apribojimai apibrėžiami išraiška, kurioje naudojami aritmetiniai ir Bulio logikos operatoriai bei funkcijos. Produkto konfigūracijos modelyje rašomas konkretaus komponento išraiškos apribojimas. Kitas komponentas negali jo pakartotinai arba bendrai naudoti. Tačiau komponento išraiškos apribojimai gali nurodyti komponento pakomponenčio atributus.

## <a name="what-are-table-constraints"></a>Kas yra lentelės apribojimai?
Lentelės apribojimais nurodomi konfigūruojant produktą leidžiami atributų reikšmių deriniai. Lentelės apribojimų apibrėžimai gali būti bendrai naudojami. Produkto konfigūracijos modelyje kurdami komponento lentelės apribojimą, pasirenkate lentelės apribojimo apibrėžimą. Norėdami kurti leidžiamus derinius, į komponentus įtraukiate konkrečių tipų atributų. Kiekvienas atributo tipas yra konkrečios reikšmės.

### <a name="example-of-a-table-constraint"></a>Lentelės apribojimo pavyzdys

Šiame pavyzdyje parodoma, kaip galite riboti garsiakalbio konfigūracijas konkrečiomis spintelės apdailomis ir priekinėmis grotelėmis. Pirmoje lentelėje nurodytos spintelių apdailos ir priekinės grotelės, kurias galima konfigūruoti įprastu metu. Reikšmės nustatomos atributų tipuose **Spintelių apdaila** ir **Priekinės grotelės**.

| Atributo tipas | Reikšmės                      |
|----------------|-----------------------------|
| Spintelės apdaila | Juoda, ąžuolo, raudonmedžio, balta |
| Priekinės grotelės    | Juoda, metalo, balta         |

Kitoje lentelėje nurodyti deriniai, kurie nustatyti pagal lentelės apribojimą **Spalva ir apdaila**. Naudodami šį lentelės apribojimą, galite konfigūruoti garsiakalbį, turintį ąžuolinę apdailą ir juodas groteles, raudonmedžio apdailą ir baltas groteles ir t. t.

| Baigti         | Grotelės                       |
|----------------|-----------------------------|
| Ąžuolo            | Juoda                       |
| Palisandro       | Balta                       |
| Balta          | Juoda                       |
| Balta          | Balta                       |
| Juoda          | Juoda                       |
| Juoda          | Metalo                       | 

Galite sukurti pagal sistemas arba vartotojus nustatytus lentelės apribojimus. Daugiau informacijos žr. [Pagal sistemas arba vartotojus nustatyti lentelės apribojimai](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Kokia sintaksė turi būti naudojama apribojimams rašyti?
Rašydami apribojimus turite naudoti optimizuoto modeliavimo kalbos (OML) sintaksę. Sistema naudoja „Microsoft Solver Foundation“ apribojimų sprendimo priemonę apribojimams išspręsti.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Turėčiau naudoti lentelės apribojimus ar išraiškos apribojimus?
Galite naudoti išraiškos apribojimus arba lentelės apribojimus atsižvelgdami į tai, kaip norite konfigūruoti apribojimus. Lentelės apribojimą sudarote matricos pagrindu, o išraiškos apribojimas yra atskiras sakinys. Konfigūruojant produktą nėra svarbu, kokio tipo apribojimas bus naudojamas. Kitame pavyzdyje nurodomi abiejų metodų skirtumai.  

Kai produktą konfigūruojate naudodami šiuos apribojimų nustatymus, galima naudoti toliau nurodytus derinius.

-   Produktas, kurio spalva Juoda, o dydis 30 arba 50
-   Produktas, kurio spalva Raudona, o dydis 20

### <a name="table-constraint-setup"></a>Lentelės apribojimų nustatymas

| Spalva | Dydis |
|-------|------|
| Juoda | 30   |
| Juoda | 50   |
| Raudona   | 20   |

### <a name="expression-constraint-setup"></a>Išraiškos apribojimo nustatymas

(Spalva == "Juoda" & (dydis == "30" | dydis == "50")) | (spalva == "Raudona" & dydis = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Rašydamas išraiškos apribojimus turėčiau naudoti operatorius ar intarpo ženklą?
Galite rašyti išraiškos apribojimą naudodami galimus prefiksų operatorius arba intarpo ženklą. Negalima naudoti intarpo ženklo su operatoriais **Min**, **Max** ir **Abs**. Daugumoje programavimo kalbų šie operatoriai yra standartiniai.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Kokius operatorius ir intarpo ženklus galiu naudoti rašydamas išraiškos apribojimus?
Šiose lentelėse išvardyti operatoriai ir intarpo ženklai, kuriuos galite naudoti produkto konfigūracijos modelyje rašydami komponento išraiškos apribojimą. Pirmoje lentelėje pateiktuose pavyzdžiuose nurodyta, kaip rašyti išraišką naudojant intarpo ženklą arba operatorius.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Operatorius</th>
<th>Aprašymas</th>
<th>Sintaksė</th>
<th>Pavyzdžiai</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implikuoja</td>
<td>Gaunama teisinga, jei pirmoji sąlyga yra klaidinga, jei antroji sąlyga yra teisinga, arba jei pirmoji sąlyga yra klaidinga, o antroji sąlyga yra teisinga.</td>
<td>Implies[a, b], infix: a -: b</td>
<td><ul>
<li><strong>Operatorius:</strong> Implies[x != 0, y &gt;= 0]</li>
<li><strong>Intarpo ženklas:</strong> x != 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Ir</td>
<td>Gaunama teisinga, jei visos sąlygos yra teisingos. Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>Teisinga</strong>.</td>
<td>And[args], infix: a &amp; b &amp; ... &amp; z</td>
<td><ul>
<li><strong>Operatorius:</strong> And[x == 2, y &lt;= 2]</li>
<li><strong>Intarpo ženklas:</strong> x == 2 &amp; y &lt;= 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Arba</td>
<td>Gaunama teisinga, jei bet kuri sąlyga yra teisinga. Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>Klaidinga</strong>.</td>
<td>Or[args], infix: a | b | ... | z</td>
<td><ul>
<li><strong>Operatorius:</strong> Or[x == 2, y &lt;= 2]</li>
<li><strong>Intarpo ženklas:</strong> x == 2 | y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Plius</td>
<td>Naudojant šį operatorių, sąlygos sudedamos. Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>0</strong>.</td>
<td>Plus[args], infix: a + b + ... + z</td>
<td><ul>
<li><strong>Operatorius:</strong> Plus[x, y, 2] == z</li>
<li><strong>Intarpo ženklas:</strong> x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Minus</td>
<td>Naudojant šį operatorių, argumentas paneigiamas. Turi būti nurodyta tik viena sąlyga.</td>
<td>Minus[expr], infix: -expr</td>
<td><ul>
<li><strong>Operatorius:</strong> Minus[x] == y</li>
<li><strong>Intarpo ženklas:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Naudojant šį operatorių, gaunama absoliučioji sąlygos vertė. Turi būti nurodyta tik viena sąlyga.</td>
<td>Abs[expr]</td>
<td><strong>Operatorius:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Laikas</td>
<td>Naudojant šį operatorių, gaunamas sąlygų produktas. Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>1</strong>.</td>
<td>Times[args], infix: a * b * ... * z</td>
<td><ul>
<li><strong>Operatorius:</strong> Times[x, y, 2] == z</li>
<li><strong>Intarpo ženklas:</strong> x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Laipsnis</td>
<td>Naudojant šį operatorių, gaunama eksponentė. Keliama laipsniu iš dešinės į kairę. (Kitaip tariant, šis operatorius susietas su dešine puse.) Todėl <strong>Power[a, b, c]</strong> yra lygu <strong>Power[a, Power[b, c]]</strong>. <strong>Power</strong> gali būti naudojamas tik jei laipsnio rodiklis yra teigiama konstanta.</td>
<td>Power[args], infix: a ^ b ^ ... ^ z</td>
<td><ul>
<li><strong>Operatorius:</strong> Power[x, 2] == y</li>
<li><strong>Intarpo ženklas:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Didžiausia</td>
<td>Naudojant šį operatorių, gaunama didžiausia sąlyga. Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>Begalybė</strong>.</td>
<td>Max[args]</td>
<td><strong>Operatorius:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Mažiausia</td>
<td>Naudojant šį operatorių, gaunama mažiausia sąlyga. Jei sąlygų kiekis yra 0 (nulis), gaunama <strong>Begalybė</strong>.</td>
<td>Min[args]</td>
<td><strong>Operatorius:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Ne</td>
<td>Naudojant šį operatorių, gaunama sąlygos loginė priešingybė. Turi būti nurodyta tik viena sąlyga.</td>
<td>Not[expr], infix: !expr</td>
<td><ul>
<li><strong>Operatorius:</strong> Not[x] &amp; Not[y == 3]</li>
<li><strong>Intarpo ženklas:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Kitos lentelės pavyzdžiuose nurodyta, kaip rašyti intarpo ženklą.


|  Intarpo ženklas   |                                          aprašymas                                          |
|-------------------|-----------------------------------------------------------------------------------------------|
|     x + y + z     |                                           Priedas                                            |
|    x \* y \* z    |                                        Daugyba                                         |
|       x – y       | Dvejetainio nario atimtis atliekama lygiai taip pat, kaip dvejetainio nario sudėtis su neigiamu antru nariu. |
|     x ^ y ^ z     |                          Kėlimas laipsniu, kai susieta su dešine puse                          |
|        !x         |                                          Bulio logika ne                                          |
|      x -: y       |                                      Bulio logikos implikacija                                      |
|         x         |                                               y                                               |
|     x & y & z     |                                          Būlio logika ir                                          |
|    x == y == z    |                                           Lygybė                                            |
|    x != y != z    |                                           Ypatingas                                            |
|  x &lt; y &lt; z  |                                           Mažesnis nei                                           |
|  x &gt; y &gt; z  |                                         Didesnis nei                                          |
| x &lt;= y &lt;= z |                                     Mažiau arba lygu                                     |
| x &gt;= y &gt;= z |                                   Daugiau arba lygu                                    |
|        (x)        |                           Skliausteliuose perrašomas numatytasis pirmumas.                            |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Kodėl išraiškos apribojimai teisingai nepatvirtinami?
Produkto konfigūracijos modelyje negalite naudoti rezervuotų raktažodžių kaip atributų, komponentų ar pakomponenčių sprendimo priemonės pavadinimų.Toliau pateikiamas rezervuotų raktažodžių, kuriuos galite naudoti, sąrašas.

-   Lubos
-   Elementas
-   Lygu
-   Grindys
-   Jei
-   Mažiau
-   Didesnis
-   Implikuoja
-   Žurnalas
-   Maks.
-   Min.
-   Minusas
-   Plius
-   Galia
-   Laikai
-   Tarpsnis
-   Modelis
-   Sprendimas
-   Tikslas


<a name="additional-resources"></a>Papildomi ištekliai
--------

[Kaip sukurti išraiškos apribojimą](tasks/add-expression-constraint-product-configuration-model.md)

[Skaičiavimo įtraukimas į produkto konfigūracijos modelį](tasks/add-calculation-product-configuration-model.md)



