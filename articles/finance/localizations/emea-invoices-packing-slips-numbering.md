---
title: SF ir važtaraščių numeravimas (Latvija ir Lietuva)
description: Šiame straipsnyje paaiškinama, kaip nustatyti SF ir važtaraščių numeraciją, ir kaip nustatyti dokumentų savęs numeracijos diapazonus.
author: AdamTrukawka
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Latvia, Lithuania
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 268484
ms.search.form: LtInvoiceAutoNumberingGroups, LtInvoiceAutonumberingTable, NumberSequenceTableListPage
ms.openlocfilehash: 172377a5a1ec87fe0c74f0068a78cc3c6accd774
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337373"
---
# <a name="invoice-and-packing-slip-numbering-for-latvia-and-lithuania"></a>SF ir važtaraščių numeravimas (Latvija ir Lietuva)

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti SF ir važtaraščių numeraciją, ir kaip nustatyti dokumentų savęs numeracijos diapazonus.

Jei juridinio subjekto pagrindinis adresas yra Latvijoje arba Lietuvoje, galite nustatyti sąlyginę SF ir važtaraščių numeravimo funkciją, pagrįstą priskirtu vartotoju arba vartotojų grupe.

## <a name="set-up-number-sequences-for-invoices-and-packing-slips"></a>SF ir važtaraščių numeracijos nustatymas
Galite nustatyti unikalias dokumentų numeracijas, skirtas bendrųjų duomenų įrašams ir operacijų įrašams. Jei jūsų šalies ar regiono mokesčių rinkėjai jūsų organizacijai priskiria specifinę dokumentų numeraciją arba formatą, galite numeraciją susieti su dokumento tipu. Kiekvieną dokumentų numeraciją galite priskirti vartotojui arba vartotojų grupei. Tokiu būtu tik pasirinktas vartotojas arba vartotojų grupė gali priskirti sekos numerius dokumentui. SF ir važtaraščių numeracijas galite nustatyti puslapyje **SF numeravimo nustatymas**. (Spustelėkite **Organizacijos administravimas** &gt; **Numeracijos** &gt; **SF numeravimo nustatymas**.) Naudokite tolesnėje lentelėje pateiktą informaciją, kad užpildytumėte puslapio **SF numeravimo nustatymas** laukus.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Laukas</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Numeravimas</td>
<td>Įveskite dokumentų numeracijos priešvardį.</td>
</tr>
<tr class="even">
<td>Modulis</td>
<td>Pasirinkite modulį, kuris naudos numerių seką. Pasirinktas modulis nustato, kokias parinktis galima pasirinkti lauke <strong>Tipas</strong>. Jei tvarkote kliento SF ir kliento važtaraščius, šiame lauke pasirinkite <strong>Pardavimas</strong>.</td>
</tr>
<tr class="odd">
<td>Numeracijos kodas</td>
<td>Pasirinkite duomenų srities, kuriai numerių seka taikoma, numeracijos kodą.</td>
</tr>
<tr class="even">
<td>Tipas</td>
<td>Pasirinkite, ar numeracija taikoma SF, ar važtaraščiams.</td>
</tr>
<tr class="odd">
<td>Sąskaitos kodas</td>
<td>Pasirinkite, kaip numerių seka taikoma SF. Galimos toliau nurodytos pasirinktys:
<ul>
<li><strong>Lentelė</strong> – numerių seką gali naudoti tik lauke <strong>Kodas</strong> pasirinktas vartotojas.</li>
<li><strong>Grupė</strong> – numerių seką gali naudoti lauke <strong>Kodas</strong> pasirinkta vartotojų grupė.</li>
<li><strong>Visi</strong> – numerių seką gali naudoti visi vartotojai.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kodas</td>
<td>Pasirinkite vartotojo arba vartotojų grupės, kuriai numerių seka priskirta SF sunumeruoti, ID.</td>
</tr>
<tr class="odd">
<td>Paskutinė data</td>
<td>Diena, kurią numerių seka buvo paskutinį kartą atnaujinta.</td>
</tr>
<tr class="even">
<td>Tęsti</td>
<td>Pasirinktie šią parinktį, kad ieškotumėte numerių sekos, kuri priskirta pasirinktam vartotojui arba vartotojų grupei.</td>
</tr>
</tbody>
</table>

## <a name="set-up-document-self-numbering-ranges"></a>Automatinio dokumento numeravimo diapazonų nustatymas
Galite priskirti konkrečias numerių sekas SF ir važtaraščiams, kurie yra generuojami moduliuose **Gautinos sumos**, **Mokėtinos sumos**, **Atsargų valdymas** ir **Projektų valdymas ir apskaita**. Taip pat galite nurodyti atskiras numeracijas ir priskirti skirtingiems vartotojams ir vartotojų grupėms, klientų ir tiekėjų grupėms arba sandėliams. Norėdami nustatyti kliento SF ir tiekėjo SF numeracijas, naudokite puslapį **Skaitiklių valdymas**. (Spustelėkite **Organizacijos administravimas** &gt; **Numeracijos** &gt; **Skaitiklių valdymas**.) Numeraciją galite nustatyti pagal vartotoją ar vartotojų grupę arba pagal konkrečias klientų grupes ir tiekėjų grupes. Naudokite tolesnėje lentelėje pateiktą informaciją, kad užpildytumėte laukus puslapyje **Skaitiklių valdymas**.

| Laukas          | aprašymas                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Modulis         | Pasirinkite modulį, kuriam taikoma pasirinkta numeracija.                                                                                 |
| Sąskaitos kodas   | Pasirinkite, ar numeracijos kodas taikomas visiems pasirinkto modulio įrašams, ar konkrečiai modulio grupei.                     |
| Kodas           | Pasirinkite pasirinkto modulio kodą. **Pastaba.** Lauką **Kodas** galima naudoti tik jei lauke **Sąskaitos kodas** pasirinkta parinktis **Grupė**. |
| Tipas           | Pasirinkite dokumento tipą, kurį reikia numeruoti: **SF** arba **Važtaraštis**.                                                                         |
| Automatinis numeravimas | Pažymėkite šią parinktį, jei norite dokumentui numerį priskirti automatiškai. Galite neautomatiškai pažymėti arba atžymėti šią parinktį atskiriems dokumentams.       |

Norėdami gauti informacijos apie tai, kaip patiems numeruoti sąskaitas faktūras ir važtaraščius, žr. [Rytų Europos pardavimo užsakymų sąskaitų faktūrų ID redagavimas](emea-edit-invoice-id-sales-orders.md).

## <a name="affected-processes"></a>Paveikti procesai
Toliau pateiktų dokumentų antraštės atnaujinamos naudojant SF ir važtaraščių numeraciją.

-   Pardavimo užsakymai
-   Pirkimo užsakymai
-   Laisvos formos sąskaitos faktūros
-   Projekto SF pasiūlymai

Kai registruojate toliau nurodytus dokumentus, galite pasirinkti konkrečia numeraciją lauke **Numeravimas**.

-   Pardavimo važtaraštis
-   Pardavimo registravimo SF
-   Pirkimo registravimo produkto gavimo dokumentas
-   Pirkimo tiekėjo SF
-   Registruoti projekto SF pasiūlymus
-   Registruoti laisvos formos SF

Be to, toliau nurodytos formos pateikiamos lauke **Dokumentai atnaujinti**.

-   Pirkimo tiekėjo SF forma
-   Pardavimo važtaraščio registravimo forma
-   Pardavimo registravimo SF forma
-   Pirkimo registravimo produkto gavimo dokumento forma

Laukas **Dokumentai naujinti** turi įtakos puslapių **Važtaraščių žurnalas** ir **SF žurnalas** lauko **Dokumento būsena** rodiniui. Kai kuriamas **Važtaraštis**, lauko **Dokumento būsena** reikšmė yra **Nėra**. Jei lauke **Dokumentai naujinti** buvo pasirinktas bet koks **Važtaraštis**, tada jo **Dokumento būsena** bus **Sugadintas**, o **važtaraščio** **Dokumento būsena** toje vietoje, kurioje jis buvo sukurtas, bus **Atšaukta**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
