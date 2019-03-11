---
title: Pridėtinių išlaidų skaičiavimas
description: Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "335122"
---
# <a name="overhead-calculation"></a>Pridėtinių išlaidų skaičiavimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi įprasti pridėtinių išlaidų skaičiavimo ir paskirstymo procesai.

<a name="term-definition"></a>Termino aprašas
---------------

Pridėtinės išlaidos – tai išlaidos, kurios patirtos siekiant vykdyti verslą, bet kurių negalima tiesiogiai priskirti jokiai konkrečiai verslo veiklai, produktui arba paslaugai. Pridėtinės išlaidos yra labai svarbios generuojant pelną teikiančias veiklas. Toliau pateikiama keletas pridėtinių išlaidų pavyzdžių.

-   Nuoma
-   Elektros energija
-   Administravimo atlyginimai

## <a name="overhead-calculation-overview"></a>Pridėtinių išlaidų skaičiavimo apžvalga
Pridėtinių išlaidų skaičiavimas vykdo išlaidų apskaitos strategijas teisinga tvarka. Jei išlaidų apskaitos strategijos pasikeitė arba nustatyta konkrečių klaidų, kelis kartus galite paleisti to paties ataskaitinio laikotarpio pridėtinių išlaidų skaičiavimą. Kiekvienas pridėtinių išlaidų skaičiavimo vykdymas yra išsaugomas ir jam priskiriamas unikalus versijos ID, kurį naudojant galima palyginti įvairių versijų skaičiavimus. Išlaidų įrašams, sugeneruotiems skaičiuojant pridėtines išlaidas, priskiriama apskaitos data. Ši apskaitos data sutampa su skaičiuojant naudojamo ataskaitinio laikotarpio pabaigos data. Unikalų versijos ID sudaro toliau nurodyti elementai.

-   Versijos tipas
-   Data ir laikas
-   Savikainos apskaitos didžioji knyga
-   Finansiniai metai
-   Ataskaitinis laikotarpis

Pridėtinių išlaidų skaičiavimas vykdomas nepriklausomai nuo versijos. Todėl biudžeto versiją galite skaičiuoti prieš skaičiuodami faktinę versiją. Pridėtinių išlaidų skaičiavimą sudaro keturi veiksmai, kaip pavaizduota tolesnėje iliustracijoje. Atliekant kiekvieną veiksmą sukuriama žurnalo antraštė su žurnalo įrašais. Šioje žurnalo antraštėje išsaugomi kiekvieno skaičiavimo veiksmo įvesties duomenys. Strategijos ir taisyklės pritaikomos kiekvienai žurnalo eilutei , o išlaidų įrašai sugeneruojami kaip išeiga. Todėl visada galite atsekti visą informaciją. 

[![Pridėtinių išlaidų skaičiavimas](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Elektros pridėtinių išlaidų skaičiavimas ir paskirstymas
Finansinėje apskaitoje kai kurios išlaidos, pvz., už elektrą, yra registruojamos kaip fiksuota suma. Todėl nepateikiamos išsamios išlaidų apskaitos valdymo įžvalgos. Tam, kad išlaidų apskaitoje būtų galima pateikti teisingas visų organizacijos vienetų ir lygių valdymo įžvalgas, išlaidų srautas turi būti nukreiptas į visus organizacijos vienetus. Šis srautas turi būti pagrįstas tiksliu suvartojimo įrašu arba teisingu įvertinimu. DK elektros išlaidas galima registruoti, kaip parodyta toliau pateiktoje lentelėje.

<table>
<thead>
<tr>
<th>Ataskaitinė data</th>
<th colspan="2">Išlaidų centras</th>
<th colspan="2">Korespondentinė sąskaita, subsąskaita</th>
<th>Suma apskaitos valiuta</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 m. sausio 3 d.</td>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>1 veiksmas: išlaidų veikimo būdo skaičiavimo apdorojimas

Pagal numatytuosius parametrus išlaidų įrašus importuojant iš šaltinio duomenų, išlaidų apskaitoje jiems priskiriama išlaidų veikimo būdo klasifikacija **Nekategorizuota**. Taikant išlaidų veikimo būdo strategijos taisyklės, išlaidų įrašus galima perklasifikuoti priskiriant klasifikaciją **Fiksuota savikaina** arba **Kintama savikaina**.

#### <a name="define-the-cost-behavior-rule"></a>Išlaidų veikimo būdo taisyklės nustatymas

Kai kuriais atvejais dalis išlaidų yra fiksuotas mokestis, o likusi dalis yra vartojimo išlaidos. Sąskaitos už elektrą dažnai atitinka šį apibrėžimą. Sumokėję tam tikrą fiksuotą mokestį, mokate už suvartojimą kiekį per vieną kilovatvalandę (Kwh). Pvz., jei fiksuotos savikainos mokestis yra 1 000,00, išlaidų veikimo būdo taisyklę reikia nustatyti, kaip nurodyta toliau.

-   Fiksuota suma 1 000,00
    -   0 &lt;= 1 000,00 = fiksuota
    -   1 000,01 &lt; N = kintamasis

##### <a name="journal"></a>Žurnalas

<table>
<thead>
<tr>
<th>Žurnalas</th>
<th>Žurnalo tipas</th>
<th colspan="3">Ataskaitinis kalendorinis laikotarpis</th>
<th>Versija</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Savikainos veikimo būdo skaičiavimo žurnalas</td>
<td>Finansiniai</td>
<td>2017</td>
<td>1 laikotarpis</td>
<td>Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)

<table>
<thead>
<tr>
<th>Ataskaitinė data</th>
<th colspan="2">Išlaidų objektas</th>
<th colspan="2">Savikainos elementas</th>
<th>Savikainos veikimo būdas</th>
<th>Suma</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 m. sausio 3 d.</td>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Nesuklasifikuota</td>
<td>10.000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Savikainos įrašai

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th colspan="2">Savikainos elementas</th>
<th>Savikainos veikimo būdas</th>
<th>Suma</th>
<th>Ataskaitinė data</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Nesuklasifikuota</td>
<td>10.000,00</td>
<td>2017 m. sausio 3 d.</td>
</tr>
<tr>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Nesuklasifikuota</td>
<td>-10,000.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>1000,00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>9,000.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
</tbody>
</table>

Daugiau informacijos ieškokite srityje [Savikainos veikimo būdo strategijos kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)
### <a name="step-2-process-the-cost-distribution-calculation"></a>2 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas

Išlaidų paskirstymas naudojamas perskirstyti išlaidas iš vieno išlaidų objekto į vieną arba kelis kitus išlaidų objektus, taikant atitinkamą paskirstymo bazę. Išlaidų paskirstymas ir išlaidų priskyrimas skiriasi tuo, kad išlaidų paskirstymas vykdomas pirminių išlaidų pirminio išlaidų elemento lygiu.

#### <a name="define-the-cost-distribution-rule"></a>Išlaidų paskirstymo taisyklės nustatymas

Finansinėje apskaitoje išlaidos už elektrą dažnai yra registruojamos kaip fiksuota suma. Išlaidų apskaitoje šis metodas nėra pakankamai aprašytas. Kintama savikaina turėtų būti paskirstyta atskiriems išlaidų objektams teisingu pagrindu. Logiškiausias paskirstymo pagrindas yra elektros suvartojimas (Kwh). Sukuriamas statistinės dimensijos narys pavadinimu Elektra ir įrašomas elektros suvartojimas. Pagal numatytuosius parametrus visus statistinės dimensijos narius galima naudoti kaip paskirstymo pagrindus.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Kwh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>1000</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>0</td>
</tr>
</tbody>
</table>

Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Reikšmė</th>
<th>Paskirstymo koeficientas</th>
<th>Suma</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>1000</td>
<td>(1 000 ÷ 7 000) × 9 000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>6,000</td>
<td>(6 000 ÷ 7 000) × 9 000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>0</td>
<td>(0 ÷ 7 000) × 9 000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

Fiksuota savikaina turi būti tolygiai paskirstyta atskiriems išlaidų objektams, kurie vartojo elektrą. Tai galima pasiekti naudojant statistinės dimensijos narį Elektra paskirstymo pagrindo formulėje: (Elektra &gt; 0,00) Toliau pateikiamoje lentelėje rodomas, kas nutinka elektros suvartojimą pritaikius kaip kintamų savikainų paskirstymo pagrindą.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Formulė</th>
<th>Reikšmė</th>
<th>Paskirstymo koeficientas</th>
<th>Suma</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>{1 000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1 000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>{6 000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1 000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>{0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1 000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Žurnalas

<table>
<thead>
<tr>
<th>Žurnalas</th>
<th>Žurnalo tipas</th>
<th colspan="3">Ataskaitinis kalendorinis laikotarpis</th>
<th>Versija</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Išlaidų paskirstymo skaičiavimo žurnalas</td>
<td>Finansiniai</td>
<td>2017</td>
<td>1 laikotarpis</td>
<td>Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)

<table>
<thead>
<tr>
<th>Ataskaitinė data</th>
<th colspan="2">Išlaidų objektas</th>
<th colspan="2">Savikainos elementas</th>
<th>Savikainos veikimo būdas</th>
<th>Suma</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>1000,00</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Savikainos įrašai

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th colspan="2">Savikainos elementas</th>
<th>Savikainos veikimo būdas</th>
<th>Suma</th>
<th>Ataskaitinė data</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>-1,000.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>500,00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>500,00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC099</td>
<td>Numatytasis išlaidų centras</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>-9,000.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>1,285.71</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>7,714.29</td>
<td>2017 m. sausio 31 d.</td>
</tr>
</tbody>
</table>

Daugiau informacijos ieškokite srityje [Savikainos paskirstymo kūrimas ir priskyrimas savikainos kontrolės įtaisui](tasks/create-assign-cost-distribution-policy-cost-control-unit.md) 

### <a name="step-3-process-the-overhead-rate-calculation"></a>3 veiksmas: pridėtinių išlaidų tarifo skaičiavimo procesas

Pridėtinių išlaidų tarifas naudojamas norint mokestį priskirti vienam arba daugiau konkrečių išlaidų objektų. Mokestis pagrįstas iš anksto nustatytu išlaidų tarifu ir reikšme iš priskirto paskirstymo pagrindo. 

#### <a name="define-the-overhead-rate"></a>Pridėtinių išlaidų tarifo nustatymas

Išlaidų objekto CC001 personalas prisideda prie kelių vidinių projektų. Sukuriamas statistinės dimensijos narys pavadinimu Personalo projektai, kad būtų galima apskaičiuoti suvartojimo reikšmę.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Valandos</th>
</tr>
</thead>
<tbody>
<tr>
<td>1 projektas</td>
<td>1 projektas</td>
<td>3</td>
</tr>
<tr>
<td>2 projektas</td>
<td>2 projektas</td>
<td>1</td>
</tr>
</tbody>
</table>

Išlaidų projektų iš anksto nustatytas išlaidų tarifas nustatytas.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Savikainos elementas</th>
<th>Savikainos veikimo būdas</th>
<th>Vienetai</th>
<th>Tarifas</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>10001</td>
<td>Kintamos išlaidos</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Toliau pateikiamoje lentelėje rodoma, kas nutinka personalo projektus pritaikius kaip kintamų savikainų paskirstymo pagrindą.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Reikšmė</th>
<th>Savikainos elementas</th>
<th>Paskirstymo koeficientas</th>
<th>Suma</th>
</tr>
</thead>
<tbody>
<tr>
<td>1 projektas</td>
<td>1 projektas</td>
<td>3</td>
<td>10001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30,00</td>
</tr>
<tr>
<td>2 projektas</td>
<td>2 projektas</td>
<td>1</td>
<td>10001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Žurnalas

<table>
<thead>
<tr>
<th>Žurnalas</th>
<th>Žurnalo tipas</th>
<th colspan="3">Ataskaitinis kalendorinis laikotarpis</th>
<th>Versija</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Pridėtinių išlaidų tarifo skaičiavimo žurnalas</td>
<td>Finansiniai</td>
<td>2017</td>
<td>1 laikotarpis</td>
<td>Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Žurnalų įrašai (pridėtinių išlaidų skaičiavimo žurnalo įrašai)

<table>
<thead>
<tr>
<th>Ataskaitinė data</th>
<th colspan="2">Išlaidų objektas</th>
<th>Reikšmė</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>1 projektas</td>
<td>1 vidinis projektas</td>
<td>3,00</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>2 projektas</td>
<td>2 vidinis projektas</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Savikainos įrašai

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th colspan="2">Savikainos elementas</th>
<th>Savikainos veikimo būdas</th>
<th>Suma</th>
<th>Ataskaitinė data</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>Personalas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>-30.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>1 projektas</td>
<td>1 vidinis projektas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>30,00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>-10.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>2 projektas</td>
<td>2 vidinis projektas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>10,00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
</tbody>
</table>

Daugiau informacijos ieškokite srityje [Atlikti pridėtinių išlaidų skaičiavimą](cost-rollup.md#perform-overhead-calculation)..

### <a name="step-4-process-the-cost-allocation-calculation"></a>4 veiksmas: išlaidų paskirstymo skaičiavimo apdorojimas

Paskirstymas naudojamas norint išlaidų objekto balansą paskirstyti kitiems išlaidų objektams taikant paskirstymo pagrindą. „Finance and Operations” palaiko abipusio paskirstymo metodą. Taikant abipusio paskirstymo metodą įskaičiuojamos visos papildomų išlaidų objektų tarpusavio paslaugos. Sistema automatiškai nustato teisingą tvarką, kuria reikia atlikti paskirstymą. Išlaidų objekto balansas paskirstomas pagal vieną paskirstymo pagrindą. Palaikomas paskirstymas visoms išlaidų objektų dimensijoms ir jų atitinkamiems nariams. Paskirstymo tvarka priklauso nuo išlaidų kontrolės įtaiso. 

[![Abipusis metodas](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Išlaidų paskirstymo nustatymas

Štai paprastas pavyzdys, kuriame paaiškinama, kaip galite sekti išlaidų srautą. Išlaidų objekto CC001 personalas prisideda prie kelių išlaidų objektų. Sukuriamas statistinės dimensijos narys pavadinimu Personalo paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Personalo paslaugos</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>10</td>
</tr>
</tbody>
</table>

Išlaidų objekto CC002 finansų padalinys prisideda prie kelių išlaidų objektų. Sukuriamas statistinės dimensijos narys pavadinimu Finansų padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Finansų padalinio paslaugos</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>35</td>
</tr>
</tbody>
</table>

Išlaidų objekto CC003 surinkimo padalinys prisideda prie kelių išlaidų objektų. Sukuriamas statistinės dimensijos narys pavadinimu Surinkimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Surinkimo padalinio paslaugos (valandomis)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>60</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>20</td>
</tr>
</tbody>
</table>

Išlaidų objekto CC004 pakavimo padalinys prisideda prie kelių išlaidų objektų. Sukuriamas statistinės dimensijos narys pavadinimu Pakavimo padalinio paslaugos, kad būtų galima apskaičiuoti suvartojimo reikšmę.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Pakavimo padalinio paslaugos (valandomis)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>80</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>15</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Programoje „Finance and Operations“ statistines priemones, pvz., produkto gamybai sugaištų valandų skaičių, galima gauti iš šaltinio duomenų. Norėdami gauti daugiau informacijos, žr. [Statistinių priemonių teikimo įrankio šablonas](statistical-measure-provider-template.md#statistical-measure-provider-template). Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius personalo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Reikšmė</th>
<th>Paskirstymo koeficientas</th>
<th>Suma</th>
<th>Savikainos veikimo būdas</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>35</td>
<td>(35 ÷ 100) × 1 245,71</td>
<td>436.00</td>
<td>Kintamos išlaidos</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>55</td>
<td>(55 ÷ 100) × 1 245,71</td>
<td>685.14</td>
<td>Kintamos išlaidos</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>10</td>
<td>(10 ÷ 100) × 1 245,71</td>
<td>124.57</td>
<td>Kintamos išlaidos</td>
</tr>
</tbody>
</table>

Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius finansų padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Reikšmė</th>
<th>Paskirstymo koeficientas</th>
<th>Suma</th>
<th>Savikainos veikimo būdas</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>65</td>
<td>(65 ÷ 100) × (7 714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Kintamos išlaidos</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>35</td>
<td>(35 ÷ 100) × (7 714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Kintamos išlaidos</td>
</tr>
</tbody>
</table>

Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius surinkimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Reikšmė</th>
<th>Paskirstymo koeficientas</th>
<th>Suma</th>
<th>Savikainos veikimo būdas</th>
</tr>
</thead>
<tbody>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>60</td>
<td>(60 ÷ 80) × (5 297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Kintamos išlaidos</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>20</td>
<td>(20 ÷ 80) × (5 297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Kintamos išlaidos</td>
</tr>
</tbody>
</table>

Toliau pateikiamoje lentelėje parodoma, kas nutinka pritaikius pakavimo padalinio paslaugas kaip visų išlaidų (fiksuotos savikainos ir kintamos savikainos) paskirstymo pagrindą.

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th>Reikšmė</th>
<th>Paskirstymo koeficientas</th>
<th>Suma</th>
<th>Savikainos veikimo būdas</th>
</tr>
</thead>
<tbody>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Fiksuotos išlaidos</td>
</tr>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>80</td>
<td>(80 ÷ 95) × (2 852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Kintamos išlaidos</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>15</td>
<td>(15 ÷ 95) × (2 852,60 + 124,57)</td>
<td>470.08</td>
<td>Kintamos išlaidos</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Žurnalo įrašai (išlaidų objekto balanso žurnalo įrašai)

<table>
<thead>
<tr>
<th>Žurnalas</th>
<th>Žurnalo tipas</th>
<th colspan="3">Ataskaitinis kalendorinis laikotarpis</th>
<th>Versija</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Savikainos paskirstymo žurnalas</td>
<td>Finansiniai</td>
<td>2017</td>
<td>1 laikotarpis</td>
<td>Pridėtinių išlaidų skaičiavimas / 2017-02-01 11:51:00 val. / DK / 2017 m. / 1 laikotarpis</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Žurnalo eilutės

<table>
<thead>
<tr>
<th>Ataskaitinė data</th>
<th colspan="2">Išlaidų objektas</th>
<th colspan="2">Savikainos elementas</th>
<th>Savikainos veikimo būdas</th>
<th>Suma</th>
</tr>
</thead>
<tbody>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC001</td>
<td>Personalas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>500,00</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC001</td>
<td>Personalas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>1,245.71</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC002</td>
<td>Finansai</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>675.00</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC002</td>
<td>Finansai</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>8,150.29</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>713.75</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>5,982.83</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC003</td>
<td>Pakuotės</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>286.25</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>CC003</td>
<td>Pakuotės</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>2,977.17</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>776.36</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>6,994.21</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>2 gamyba</td>
<td>1 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>223.64</td>
</tr>
<tr>
<td>2017 m. sausio 31 d.</td>
<td>2 gamyba</td>
<td>1 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Savikainos įrašai

<table>
<thead>
<tr>
<th colspan="2">Išlaidų objektas</th>
<th colspan="2">Savikainos elementas</th>
<th>Savikainos veikimo būdas</th>
<th>Suma</th>
<th>Ataskaitinė data</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>-500.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>175.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>275.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>50,00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC001</td>
<td>Personalas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>-1,245.71</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>436.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>685.14</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>124.57</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>-675.00</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>438.75</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>236.25</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC002</td>
<td>Finansai</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>-8,150.29</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>5,297.69</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakuotės</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>2,852.60</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>-713.75</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>535.31</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>178.44</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>-5,982.83</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>4,487.12</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>1,495.71</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>-286.25</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>241.05</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Fiksuotos išlaidos</td>
<td>45.20</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>CC003</td>
<td>Surinkimas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>-2,977.17</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>1 gamyba</td>
<td>1 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>2,507.09</td>
<td>2017 m. sausio 31 d.</td>
</tr>
<tr>
<td>2 gamyba</td>
<td>2 produktas</td>
<td>10001</td>
<td>Elektros energija</td>
<td>Kintamos išlaidos</td>
<td>470.08</td>
<td>2017 m. sausio 31 d.</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Išvada
Finansinėje apskaitoje 10 000,00 išlaidos už elektrą registruojamos fiktyviame išlaidų centro ID. Todėl išlaidų buhalteriai žinos, kad šias išlaidas reikia paskirstyti. Išlaidų apskaitoje išlaidų srautas nukreiptas į organizacijos vienetus ir lygius, atsižvelgiant į taikomas strategijas ir taisykles. Kiekviena savikaina yra susieta su paskirstymo pagrindu, kuris yra geriausias išlaidų paskirstymo įvertinimas.

<table>
<thead>
<tr>
<th colspan="2" rowspan="2">Savikainos elementas</th>
<th colspan="9">Išlaidų objektas</th>
<th rowspan="2">Bendroji suma</th>
</tr>
<tr>
<th>CC099</th>
<th>CC001</th>
<th>CC002</th>
<th>CC003</th>
<th>CC004</th>
<th>1 projektas</th>
<th>2 projektas</th>
<th>1 gamyba</th>
<th>2 gamyba</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2">10001 Elektros energija</td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"><strong>0,00</strong></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><strong>30,00</strong></td>
<td style="text-align: right;"><strong>10,00</strong></td>
<td style="text-align: right;"><strong>7.770,57</strong></td>
<td style="text-align: right;"><strong>2.189,43</strong></td>
<td style="text-align: right;"><strong>10.000,00</strong></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;">Nesuklasifikuota</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Fiksuotos išlaidos</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;">776.36</td>
<td style="text-align: right;">223.64</td>
<td style="text-align: right;"><strong>1.000,00</strong></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;">Kintamos išlaidos</td>
<td style="text-align: right;">000</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">0,00</td>
<td style="text-align: right;">30,00</td>
<td style="text-align: right;">10,00</td>
<td style="text-align: right;">6,994.21</td>
<td style="text-align: right;">1,965.79</td>
<td style="text-align: right;"><strong>9.000,00</strong></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Šioje temoje parodytas pirminio išlaidų elemento, 10001 Elektros energija, srautas per išlaidų objektus. Todėl šios pridėtinės išlaidos paskirstomos žemiausiu organizacijos lygiu. Kitaip tariant, išlaidas padengia žemiausio lygio išlaidų objektai. Jei reikia vizualiai pateikto išlaidų srauto tarp išlaidų objektų, galite naudoti išlaidų sumavimo strategijos taisykles, kad vizualiai pateiktumėte išlaidų srautą. Išsamesnės informacijos žr. temoje [Išlaidų sumavimas](cost-rollup.md).



