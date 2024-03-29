---
title: Apskaitos paskirstymai ir žurnalo įrašai nemokamo teksto sąskaitoms
description: Apskaitos paskirstymai naudojami apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos įplaukos, mokesčiai ar rinkliavos laisvos formos SF. Kiekviena suma, kurią reikia apskaityti, kai laisvos formos SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5120c4e75e821776201d5add2d498feb94d0297
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778417"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a>Apskaitos paskirstymai ir papildomos knygos įrašai nemokamo teksto sąskaitoms

[!include [banner](../includes/banner.md)]

Apskaitos paskirstymai naudojami apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos įplaukos, mokesčiai ar rinkliavos laisvos formos SF. Kiekviena suma, kurią reikia apskaityti, kai laisvos formos SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.

## <a name="accounting-distributions"></a>Apskaitos paskirstymai

Laisvos formos SF puslapyje galite naudoti šiuos **mygtukus**, norėdami peržiūrėti ir galbūt pakeisti kiekvienos laisvos formos SF sumos apskaitos paskirstymus.

-   **Paskirstyti sumas** –peržiūrėkite ir keiskite apskaitos paskirstymus konkrečioje eilutėje ir visose antrinėse eilutėse, pvz., mokesčių ar rinkliavų. Taip pat galite peržiūrėti ir keisti papildomos eilutės apskaitos paskirstymus **tiesiogiai iš PVM operacijų** puslapio ar išlaidų **operacijų** puslapio.
    -   Keiskite laisvos formos SF antraštės sumas, pvz., rinkliavas arba valiutos sumos apvalinimą.
    -   Keiskite laisvos formos SF eilutės sumas.
-   **Peržiūrėti paskirstymus** – peržiūrėkite visų dokumentų eilučių apskaitos paskirstymus. Negalite keisti apskaitos paskirstymų iš šio rodinio.
    -   Peržiūrėkite antraštės ir eilutės sumas.

## <a name="distributing-amounts"></a>Sumų paskirstymas
Kai įvedate laisvos formos SF, kiekviena suma bus paskirstyta kaip aprašyta toliau.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Piniginės sumos tipas</th>
<th>Iš kur rodoma pagrindinė sąskaita</th>
<th>Pirmenybės tvarka, kuri lemia, kuri numatytoji finansinė dimensija rodoma</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Laisvos formos SF eilutė</td>
<td>Laisvos formos SF eilutės DK sąskaita.</td>
<td><ol>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Jei pagrindinė sąskaita nėra paskirstymo sąskaita, laisvos formos SF eilutėje naudokite finansinės dimensijos numatytąjį šabloną.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</li>
<li>Naudokite numatytąsias finansinės dimensijos vertes iš DK sąskaitos, sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
<tr class="even">
<td>Ilgalaikio turto numerio ir vertinimo modelio derinio laisvos formos SF eilutė
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Pastaba. </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Laisvos formos SF eilutėje pagrindinė sąskaita bus ilgalaikio turto likvidavimo sąskaita.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Laisvos formos SF eilutės DK sąskaita.</td>
<td><ol>
<li>Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</li>
<li>Naudokite numatytąsias finansinės dimensijos vertes iš DK sąskaitos, sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Laisvos formos SF nuolaidos suma</td>
<td>Mokėjimo nuolaidų puslapio laukas Pagrindinė sąskaita, skirta Kliento nuolaidoms.</td>
<td><ol>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Jei pagrindinė sąskaita nėra paskirstymo sąskaita, laisvos formos SF eilutėje naudokite finansinės dimensijos numatytąjį šabloną.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</li>
<li>Naudokite numatytąsias finansinės dimensijos vertes iš DK sąskaitos, sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
<tr class="even">
<td>Laisvos formos SF PVM suma</td>
<td>Mokėtino PVM laukas DK registravimo grupių puslapyje.</td>
<td><ol>
<li>Naudokite finansines dimensijas, apibrėžtas laisvos formos SF eilutės sumoje, arba paskirstymus išlaidų eilutės sumoje.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</li>
<li>Naudokite numatytąsias finansinės dimensijos vertes iš DK sąskaitos, sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Laisvos formos SF išlaidų eilutės suma</td>
<td>Išlaidų kodo puslapio laukas Kredito sąskaita.</td>
<td><ol>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Jei pagrindinė sąskaita nėra paskirstymo sąskaita, laisvos formos SF eilutėje naudokite finansinės dimensijos numatytąjį šabloną.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</li>
<li>Naudokite numatytąsias finansinės dimensijos vertes iš DK sąskaitos, sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Mokesčių paskirstymas
Mokesčių apskaitos paskirstymus galima kurti tik apskaičiavus mokesčius. Norėdami apskaičiuoti PVM, turite atlikti vieną iš šių užduočių laisvos **formos SF** puslapyje:
-   Peržiūrėkite PVM.
-   Peržiūrėkite SF bendrąją sumą.
-   Peržiūrėkite grynųjų pinigų srautą.
-   Peržiūrėkite visos laisvos formos SF apskaitos paskirstymus.
-   Peržiūrėkite papildomos knygos žurnalą.

## <a name="subledger-journals-for-free-text-invoices"></a> Laisvos formos SF papildomos knygos žurnalai
Prieš registruodami laisvos formos SF galite peržiūrėti visą sąskaitos faktūros apskaitos įrašą, kuris apima debetus ir kreditus, kad patikrintumėte, ar sąskaita faktūra registruojama tinkamose sąskaitose. Šis viso apskaitos įrašo rodinys vadinamas papildomos knygos žurnalu. Jei papildomos knygos žurnalo įrašas neteisingas, kai peržiūrite jį prieš įtraukdami laisvos formos SF į žurnalą, negalite keisti papildomos knygos žurnalo įrašo. Bet galite keisti apskaitos paskirstymus arba registravimo šabloną. Apskaitos paskirstymai naudojami norint nustatyti vieną apskaitos įrašo pusę, debetą arba kreditą. Balansavimo papildomos knygos žurnalo sąskaitos įrašas sukuriamas iš registravimo profilių, pvz., iš kliento sąskaitos arba mokesčio.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
