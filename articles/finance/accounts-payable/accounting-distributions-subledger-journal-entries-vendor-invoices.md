---
title: Apskaitos paskirstymai ir žurnalo įrašai pardavėjo sąskaitoms
description: Apskaitos paskirstymai naudojami siekiant apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos išlaidos, mokesčiai ar rinkliavos tiekėjo SF. Kiekviena suma, kurią reikia apskaityti, kai tiekėjo SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fecdafe8765121d6d54389a70e6c2e497a03611a
ms.sourcegitcommit: 43d0555c17a0643c9e5ba3bc2da3ce5f80754642
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/18/2022
ms.locfileid: "8325973"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Apskaitos paskirstymai ir žurnalo įrašai pardavėjo sąskaitoms

[!include [banner](../includes/banner.md)]

Apskaitos paskirstymai naudojami siekiant apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos išlaidos, mokesčiai ar rinkliavos tiekėjo SF. Kiekviena suma, kurią reikia apskaityti, kai tiekėjo SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus. 

## <a name="accounting-distributions"></a>Apskaitos paskirstymai 

Puslapyje Tiekėjo SF naudodami toliau nurodytus mygtukus galite peržiūrėti ir galbūt modifikuoti kiekvienos tiekėjo SF nurodytos sumos apskaitos paskirstymus.
-   **Paskirstyti sumas** – peržiūrėkite ir modifikuokite apskaitos paskirstymus konkrečioje eilutėje ir visose antrinėse eilutėse, pvz., mokesčių ar rinkliavų. Antrinės eilutės apskaitos paskirstymus taip pat galite peržiūrėti ir keisti tiesiogiai iš PVM operacijų puslapio arba Išlaidų operacijų puslapio.
    -   Modifikuokite tiekėjo SF antraštės sumas, pvz., rinkliavas arba valiutos sumos apvalinimą.
    -   Modifikuokite tiekėjo SF eilučių sumas.
-   **Peržiūrėti paskirstymus** – peržiūrėkite visų dokumentų eilučių apskaitos paskirstymus. Negalite modifikuoti apskaitos paskirstymų iš šio rodinio.
    -   Peržiūrėkite antraštės ir eilutės sumas.

Jei tiekėjo SF nurodomas pirkimo užsakymas, galite skaidyti ir modifikuoti apskaitos paskirstymus eilutėse, kuriose nurodomos nelaikomos prekės. Panaikinti apskaitos paskirstymą taip pat galite, jei tiekėjo SF eilutėje nenurodyta pirkimo užsakymo eilutė. Negalite skaidyti arba naikinti išlaidų, mokesčių ir eilutės nuolaidų eilučių. Galite modifikuoti DK sąskaitą, bet negalite keisti sumų arba procentinių dydžių.
> [!NOTE]                                                                                                                                 
> Jei pirminėje eilutėje yra nelaikoma prekė, o apskaitos paskirstymai padalyti, antrinė eilutė bus automatiškai padalyta, kad atitiktų pirminės eilutės finansines dimensijas. Antrinės eilutės apskaitos paskirstymų negalima dalyti papildomai arba naikinti, bet, priklausomai nuo antrinės eilutės nustatymo, galbūt galite modifikuoti antrinės eilutės apskaitos paskirstymų DK sąskaitą.

## <a name="distributing-amounts"></a>Sumų paskirstymas
Kai įvedate tiekėjo SF, kiekviena suma bus paskirstyta kaip aprašyta toliau.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tiekėjo SF eilutės tipas</th>
<th>Pirmenybės tvarka, kuri lemia, iš kur rodoma pagrindinė sąskaita</th>
<th>Pirmenybės tvarka, kuri lemia, kuri numatytoji finansinė dimensija rodoma</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Laikomas produktas</td>
<td><ol>
<li>Pirkimo užsakymo eilutės apskaitos paskirstymas.</li>
<li>Laukas **Pagrindinė** sąskaita, kai pirkimo išlaidos produktui yra pasirinktas **registravimo** puslapyje.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes tiekėjo SF.</li>
</ol></td>
</tr>
<tr class="even">
<td>Įsigijimo kategorija arba nelaikomas produktas</td>
<td><ol>
<li>Pirkimo užsakymo eilutės apskaitos paskirstymas, jei tiekėjo SF eilutėje nurodoma pirkimo užsakymo eilutė.</li>
<li>Laukas **Pagrindinė** sąskaita, kai pirkimo išlaidos išlaidoms yra pasirinktas **registravimo** puslapyje.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes tiekėjo SF.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos, sąskaitų **plano** puslapyje.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Ilgalaikis turtas</td>
<td><ol>
<li>Pirkimo užsakymo eilutės apskaitos paskirstymas, jei tiekėjo SF eilutėje nurodoma pirkimo užsakymo eilutė.</li>
<li>Jei **įsigijimas** pasirinktas operacijos **tipo lauke** **Tiekėjo** SF puslapyje, pagrindinės sąskaitos laukas, **·** **kai įsigijimas** pasirinktas ilgalaikio **turto registravimo šablonų** puslapyje.</li>
<li>Jei **lauke Operacijos** tipas pasirinktas Įsigijimo **koregavimas**, pagrindinės sąskaitos laukas, **·** **·** **kai ilgalaikio turto registravimo šablonų puslapyje pasirinktas įsigijimo koregavimas.**</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos, sąskaitų **plano** puslapyje.</li>
</ol></td>
</tr>
<tr class="even">
<td>Tiekėjo SF eilutėje nurodytas projektas</td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Jei **projekto** grupių puslapio **lauke Registruoti išlaidas –** **prekę** pasirinktas balansas, pagrindinės sąskaitos laukas, **·** **kai** išlaidos pasirinktos **DK registravimo nustatymo** puslapyje.</li>
<li>Jei **dk registravimo nustatymo** puslapyje **·** **pasirinktas** pelno ir nuostolio laukas Registruoti išlaidas – prekę, laukas Pagrindinė sąskaita, **·** **kai išlaidos –** **prekė pasirinkta DK registravimo nustatymo** puslapyje.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Eilutės nuolaida</td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Pagrindinės **sąskaitos laukas**, **kai nuolaida** pasirinkta registravimo **puslapyje**.</li>
<li>Jei registravimo šablone neapibrėžta nuolaidos pagrindinė sąskaita, išplėstinės kainos apskaitos paskirstymas pirkimo užsakymo eilutėje.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite tiekėjo SF eilutės finansinės dimensijos reikšmes.</li>
<li>Naudokite numatytąsias finansinių dimensijų reikšmes iš pagrindinės sąskaitos, sąskaitų **plano** puslapyje.</li>
</ol></td>
</tr>
<tr class="even">
<td>Pirkimo mokestis, įvedamas pirkimo **užsakymo eilutės** skirtuke Kaina ir nuolaida</td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Išplėstinės kainos apskaitos paskirstymas pirkimo užsakymo eilutėje.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Eilutės mokestis</td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Jei **DK** sąskaita pasirenkama išlaidų kodo **puslapio lauke** **Debeto** tipas, skirtuko **Išlaidų** kodas lauke **Debeto** sąskaita.</li>
<li>Jei **prekė** pasirinkta išlaidų kodo **puslapio** lauke **Debeto tipas**, išplėstinės kainos, pirkimo užsakymo eilutėje, apskaitos paskirstymas.</li>
<li>Jei **klientas /** tiekėjas pasirinktas **lauke** **Debeto tipas išlaidų kodų** puslapyje, **laukas Kredito sąskaita** išlaidų **kodų** puslapyje.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinių dimensijų reikšmes iš pagrindinės sąskaitos, sąskaitų **plano** puslapyje.</li>
</ol></td>
</tr>
<tr class="even">
<td>Mokestis su šia sąlyga:
<ul>
<li>Didžiosios knygos parametrų puslapyje pasirinkta parinktis Taikyti **JAV mokesčių** taisykles.</li>
</ul></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Išplėstinės kainos arba mokesčio apskaitos paskirstymas.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mokestis su šiomis sąlygomis:
<ul>
<li>Parinktis Taikyti JAV mokesčių taisykles išvalyta DK **parametrų** puslapyje.</li>
<li>PVM **grupės** naudojimo mokesčio laukas yra išvalytas PVM **grupių** puslapyje.</li>
</ul></td>
<td><ol>
<li>Jei mokesčio sumą galima susigrąžinti, dk **registravimo** grupių puslapio lauke **Gautinas** PVM.</li>
<li>Jei susigrąžinti mokesčio sumos negalima, išplėstinė kaina arba mokesčio apskaitos paskirstymas.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos arba mokesčio apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos, sąskaitų **plano** puslapyje.</li>
</ol></td>
</tr>
<tr class="even">
<td>Mokestis su šiomis sąlygomis:
<ul>
<li>Parinktis Taikyti JAV mokesčių taisykles išvalyta DK **parametrų** puslapyje.</li>
<li>PVM **grupės** puslapyje pasirinktas PVM grupės laukas **Naudojimo** mokestis.</li>
</ul></td>
<td><ol>
<li>Jei mokesčio sumą galima susigrąžinti, dk **registravimo** grupių puslapio lauke **Gautinas** PVM.</li>
<li>Jei mokesčio sumos negalima susigrąžinti, DK **registravimo** grupių puslapio laukas Naudoti **mokesčio** išlaidas.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos arba mokesčio apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos, sąskaitų **plano** puslapyje.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Antraštės mokestis</td>
<td><ol>
<li>Jei **DK** sąskaita pasirenkama išlaidų **kodo puslapio lauke** **Debeto** tipas, skirtuko **Išlaidų** kodas lauke **Debeto** sąskaita.</li>
<li>Jei **klientas /** tiekėjas pasirinktas **išlaidų** **kodo** puslapio debeto tipo lauke, **tai** – išlaidų kodo puslapio **laukas Kredito** sąskaita.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Naudokite finansinės dimensijos numatytojo šablono reikšmes iš tiekėjo SF antraštės.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos, sąskaitų **plano** puslapyje.</li>
</ol></td>
</tr>
<tr class="even">
<td>Antraštės nuolaida</td>
<td><ol>
<li>Tiekėjo **SF nuolaidos registravimo tipo** pagrindinės sąskaitos laukas Automatinių **operacijų** sąskaitų puslapyje **.**</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos, sąskaitų **plano** puslapyje.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Mokesčių paskirstymas

Mokesčių apskaitos paskirstymus galima kurti tik apskaičiavus mokesčius. Norėdami skaičiuoti PVM, turite atlikti vieną iš toliau nurodytų užduočių puslapyje Tiekėjo SF.
-   Peržiūrėkite SF bendrąją sumą.
-   Peržiūrėkite PVM.
-   Peržiūrėkite papildomos knygos žurnalą.
-   Peržiūrėkite visos tiekėjo SF apskaitos paskirstymus.
-   Sulaikykite tiekėjo SF.
-   Registruokite tiekėjo SF.

## <a name="subledger-journals-for-vendor-invoices"></a>Tiekėjo SF papildomos knygos žurnalai
Prieš registruodami tiekėjo SF galite peržiūrėti visą sąskaitos faktūros apskaitos įrašą, kuris apima debetus ir kreditus, kad patikrintumėte, ar sąskaita faktūra registruojama tinkamose sąskaitose. Šis viso apskaitos įrašo rodinys vadinamas papildomos knygos žurnalu. 

Jei papildomos knygos žurnalo įrašas neteisingas, kai peržiūrite jį prieš įtraukdami tiekėjo SF į žurnalą, negalite modifikuoti papildomos knygos žurnalo įrašo. Bet galite modifikuoti apskaitos paskirstymus arba registravimo šabloną. Apskaitos paskirstymai naudojami norint nustatyti vieną apskaitos įrašo pusę, debetą arba kreditą. Balansavimo papildomos knygos žurnalo sąskaitos įrašas sukuriamas naudojant registravimo profilius, pvz., iš tiekėjo sąskaitos arba mokesčio.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
