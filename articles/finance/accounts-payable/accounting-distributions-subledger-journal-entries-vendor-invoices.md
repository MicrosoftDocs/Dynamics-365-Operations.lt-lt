---
title: Apskaitos paskirstymai ir žurnalo įrašai pardavėjo sąskaitoms
description: Apskaitos paskirstymai naudojami siekiant apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos išlaidos, mokesčiai ar rinkliavos tiekėjo SF. Kiekviena suma, kurią reikia apskaityti, kai tiekėjo SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da15f27c7fef6367eacc83271419b633c0cbb245
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012293"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Apskaitos paskirstymai ir žurnalo įrašai pardavėjo sąskaitoms

[!include [banner](../includes/banner.md)]

Apskaitos paskirstymai naudojami siekiant apibrėžti, kaip suma bus apskaitoma, pvz., kaip bus apskaitomos išlaidos, mokesčiai ar rinkliavos tiekėjo SF. Kiekviena suma, kurią reikia apskaityti, kai tiekėjo SF įtraukiama į žurnalą, turės vieną ar kelis apskaitos paskirstymus. 

<a name="accounting-distributions"></a>Apskaitos paskirstymai 
-------------------------

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
<li>Laukas Pagrindinė sąskaita, kai puslapyje Registravimas pasirinkta Produkto pirkimo išlaidos.</li>
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
<li>Laukas Pagrindinė sąskaita, kai puslapyje Registravimas pasirinkta Išlaidų pirkimo išlaidos.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Naudokite numatytąsias finansines dimensijos reikšmes tiekėjo SF.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Ilgalaikis turtas</td>
<td><ol>
<li>Pirkimo užsakymo eilutės apskaitos paskirstymas, jei tiekėjo SF eilutėje nurodoma pirkimo užsakymo eilutė.</li>
<li>Formos Tiekėjo SF lauke Operacijos tipas pasirinkus Įsigijimas, laukas Pagrindinė sąskaita, kai puslapyje Ilgalaikio turto registravimo šablonai pasirinkta Įsigijimas.</li>
<li>Lauke Operacijos tipas pasirinkus Įsigijimo koregavimas, laukas Pagrindinė sąskaita, kai puslapyje Ilgalaikio turto registravimo šablonai pasirinkta Įsigijimo koregavimas.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</li>
</ol></td>
</tr>
<tr class="even">
<td>Tiekėjo SF eilutėje nurodytas projektas</td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Puslapio Projektų grupės lauke Registruoti išlaidas – Prekė pasirinkus Balansas, laukas Pagrindinė sąskaita, kai puslapyje Registravimo DK nustatymai pasirinkus Išlaidos.</li>
<li>Puslapio Projektų grupės lauke Registruoti išlaidas – Prekė pasirinkus Pelnas ir nuostolis, laukas Pagrindinė sąskaita, kai puslapyje Registravimo DK nustatymai pasirinkus Išlaidos – Prekė.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Eilutės nuolaida</td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodyta pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Laukas Pagrindinė sąskaita, kai puslapyje Registravimas pasirinkta Nuolaida.</li>
<li>Jei registravimo šablone neapibrėžta nuolaidos pagrindinė sąskaita, išplėstinės kainos apskaitos paskirstymas pirkimo užsakymo eilutėje.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės apskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite tiekėjo SF eilutės finansinės dimensijos reikšmes.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</li>
</ol></td>
</tr>
<tr class="even">
<td>Pirkimo mokestis, įvestas pirkimo užsakymo eilutės skirtuke Kaina ir nuolaida</td>
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
<li>Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta DK sąskaita, puslapio Išlaidų kodas laukas Debeto sąskaita.</li>
<li>Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta Prekė, išplėstinės kainos apskaitos paskirstymas pirkimo užsakymo eilutėje.</li>
<li>Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta Klientas/tiekėjas, puslapio Išlaidų kodas laukas Kredito sąskaita.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</li>
</ol></td>
</tr>
<tr class="even">
<td>Mokestis su šia sąlyga:
<ul>
<li>DK parametrų puslapyje pasirinkta pasirinktis taikyti JAV apmokestinimo taisykles.</li>
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
<li>DK parametrų puslapyje išvalyta pasirinktis taikyti JAV apmokestinimo taisykles.</li>
<li>PVM grupės laukas Naudojimo mokestis išvalomas puslapyje PVM grupės.</li>
</ul></td>
<td><ol>
<li>Jei mokesčio sumą galima susigrąžinti, puslapio DK registravimo grupės laukas Gautinas PVM.</li>
<li>Jei susigrąžinti mokesčio sumos negalima, išplėstinė kaina arba mokesčio apskaitos paskirstymas.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos arba mokesčio apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</li>
</ol></td>
</tr>
<tr class="even">
<td>Mokestis su šiomis sąlygomis:
<ul>
<li>DK parametrų puslapyje išvalyta pasirinktis taikyti JAV apmokestinimo taisykles.</li>
<li>PVM grupės laukas Naudojimo mokestis pasirenkamas puslapyje PVM grupės.</li>
</ul></td>
<td><ol>
<li>Jei mokesčio sumą galima susigrąžinti, puslapio DK registravimo grupės laukas Gautinas PVM.</li>
<li>Jei mokesčio sumos negalima susigrąžinti, puslapio DK registravimo grupės laukas Naudojimo mokesčio išlaidos.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos arba mokesčio apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Antraštės lygmenyje pateikiamos išlaidos</td>
<td><ol>
<li>Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta DK sąskaita, puslapio Išlaidų kodas laukas Debeto sąskaita.</li>
<li>Jei formos Išlaidų kodas lauke Debeto tipas pasirinkta Klientas/tiekėjas, puslapio Išlaidų kodas laukas Kredito sąskaita.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Jei pagrindinė sąskaita yra paskirstymo sąskaita, naudokite numatytąją reikšmę iš paskirstymo sąskaitos apibrėžimo.</li>
<li>Naudokite finansinės dimensijos numatytojo šablono reikšmes iš tiekėjo SF antraštės.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</li>
</ol></td>
</tr>
<tr class="even">
<td>Antraštės nuolaida</td>
<td><ol>
<li>Puslapio Automatinių operacijų sąskaitos registravimo tipo Tiekėjo SF nuolaida laukas Pagrindinė sąskaita.</li>
</ol></td>
<td><ol>
<li>Jei sąskaitos faktūros eilutėje nurodoma pirkimo užsakymo eilutė, naudokite pirkimo užsakymo eilutės sąskaitos paskirstymą.</li>
<li>Naudokite finansines dimensijas iš išplėstinės kainos apskaitos paskirstymų tiekėjo SF eilutėje.</li>
<li>Naudokite finansinės dimensijos reikšmes iš tiekėjo SF eilutės.</li>
<li>Naudokite numatytąsias finansinės dimensijos reikšmes iš pagrindinės sąskaitos puslapyje Sąskaitų planas.</li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a>Mokesčių paskirstymas
------------------

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