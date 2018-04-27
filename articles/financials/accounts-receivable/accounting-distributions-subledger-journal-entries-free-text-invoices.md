---
title: "Apskaitos paskirstymai ir papildomos knygos žurnalo įrašai, skirti laisvos formos SF"
description: "Apskaitos paskirstymai naudojami apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos įplaukos, mokesčiai ar rinkliavos laisvos formos SF. Kiekviena suma, kurią reikia apskaityti, kai laisvos formos SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d13fbd98597fc8138bfb4d549608d75f790e0e52
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a>Apskaitos paskirstymai ir papildomos knygos žurnalo įrašai, skirti laisvos formos SF

[!INCLUDE [banner](../includes/banner.md)]

Apskaitos paskirstymai naudojami apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos įplaukos, mokesčiai ar rinkliavos laisvos formos SF. Kiekviena suma, kurią reikia apskaityti, kai laisvos formos SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.

<a name="accounting-distributions"></a>Apskaitos paskirstymai
------------------------

Laisvos formos SF puslapyje naudodami toliau nurodytus mygtukus galite peržiūrėti ir, galbūt, keisti kiekvienos laisvos formos SF nurodytos sumos apskaitos paskirstymus.

-   **Paskirstyti sumas** –peržiūrėkite ir keiskite apskaitos paskirstymus konkrečioje eilutėje ir visose antrinėse eilutėse, pvz., mokesčių ar rinkliavų. Antrinės eilutės apskaitos paskirstymus taip pat galite peržiūrėti ir keisti tiesiogiai iš PVM operacijų puslapio arba Išlaidų operacijų puslapio.
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
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</li>
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
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Laisvos formos SF nuolaidos suma</td>
<td>Puslapio Mokėjimo nuolaidos laukas Pagrindinė sąskaita, skirta kliento nuolaidoms.</td>
<td><ol>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Jei pagrindinė sąskaita nėra paskirstymo sąskaita, laisvos formos SF eilutėje naudokite finansinės dimensijos numatytąjį šabloną.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
<tr class="even">
<td>Laisvos formos SF PVM suma</td>
<td>Mokėtino PVM laukas DK registravimo grupių puslapyje.</td>
<td><ol>
<li>Naudokite finansines dimensijas, apibrėžtas laisvos formos SF eilutės sumoje, arba paskirstymus išlaidų eilutės sumoje.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Laisvos formos SF išlaidų eilutės suma</td>
<td>Kredito sąskaitos laukas Išlaidų kodo puslapyje.</td>
<td><ol>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Jei pagrindinė sąskaita nėra paskirstymo sąskaita, laisvos formos SF eilutėje naudokite finansinės dimensijos numatytąjį šabloną.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes laisvos formos SF eilutėje.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš DK sąskaitos Sąskaitų plano puslapyje.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Mokesčių paskirstymas
Mokesčių apskaitos paskirstymus galima kurti tik apskaičiavus mokesčius. Norėdami skaičiuoti PVM, turite atlikti vieną iš toliau pateiktų užduočių formoje Laisvos formos SF.
-   Peržiūrėkite PVM.
-   Peržiūrėkite SF bendrąją sumą.
-   Peržiūrėkite grynųjų pinigų srautą.
-   Peržiūrėkite visos laisvos formos SF apskaitos paskirstymus.
-   Peržiūrėkite papildomos knygos žurnalą.

## <a name="subledger-journals-for-free-text-invoices"></a> Laisvos formos SF papildomos knygos žurnalai
Prieš registruodami laisvos formos SF galite peržiūrėti visą sąskaitos faktūros apskaitos įrašą, kuris apima debetus ir kreditus, kad patikrintumėte, ar sąskaita faktūra registruojama tinkamose sąskaitose. Šis viso apskaitos įrašo rodinys vadinamas papildomos knygos žurnalu. Jei papildomos knygos žurnalo įrašas neteisingas, kai peržiūrite jį prieš įtraukdami laisvos formos SF į žurnalą, negalite keisti papildomos knygos žurnalo įrašo. Bet galite keisti apskaitos paskirstymus arba registravimo šabloną. Apskaitos paskirstymai naudojami norint nustatyti vieną apskaitos įrašo pusę, debetą arba kreditą. Balansavimo papildomos knygos žurnalo sąskaitos įrašas sukuriamas iš registravimo profilių, pvz., iš kliento sąskaitos arba mokesčio.




