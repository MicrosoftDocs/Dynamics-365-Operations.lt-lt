---
title: "Sąskaita faktūra ir važtaraštis numeravimo Latvijai ir Lietuvai"
description: "Šioje temoje aiškinama, kaip nustatyti sąskaitų faktūrų ir važtaraščių numeracijas, ir kaip nustatyti savarankiškai numeravimo dokumentų intervalus."
author: ShylaThompson
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LtInvoiceAutoNumberingGroups, LtInvoiceAutonumberingTable, NumberSequenceTableListPage
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 268484
ms.assetid: d7ff8162-bd5c-4582-a18a-144ce5e4c06f
ms.search.region: Latvia, Lithuania
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c36db28260fc081f5667149bb52f9d3df0369490
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-and-packing-slip-numbering-for-latvia-and-lithuania"></a>Sąskaita faktūra ir važtaraštis numeravimo Latvijai ir Lietuvai

Šioje temoje aiškinama, kaip nustatyti sąskaitų faktūrų ir važtaraščių numeracijas, ir kaip nustatyti savarankiškai numeravimo dokumentų intervalus.

Juridiniams asmenims, kurie turi pirminį adresą į Latviją ar Lietuvą, galite nustatyti sąlyginio numeravimo SF ir važtaraščių, kuris yra pagrįstas priskirti vartotoją arba jų grupę.

## <a name="set-up-number-sequences-for-invoices-and-packing-slips"></a>Sąskaitų faktūrų ir važtaraščių numeracijų nustatymas
Jūs galite nustatyti unikalių dokumentų numeracijas pagrindinių duomenų ir operacijų užrašai. Jei savo šalies ar regiono institucijų darbuotojams organizacijoje konkrečiam dokumentui numeraciją arba formatu, numeraciją galima susieti su dokumento tipą. Kiekvieno dokumento numeraciją galite priskirti vartotoją arba jų grupę. Tokiu būdu, tik paskirtą vartotojo arba vartotojų grupės priskirti serijos numeriai į dokumentą. Galite nustatyti numeraciją SF ir važtaraščių ant to **SF numeravimo nustatymas** puslapis. (Spustelėkite **organizacijos administracijos**&gt;**skaičių sekas**&gt;**SF numeravimo nustatymas**.) Naudoti informaciją toliau pateiktoje lentelėje užpildykite laukus dėl to **SF numeravimo nustatymas** puslapis.

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
<td>Įveskite prefiksą dokumentų numeracija.</td>
</tr>
<tr class="even">
<td>Modulis</td>
<td>Pasirinkite modulį, kuris bus naudojamas serijos. Pasirinkto modulio nustato pasirinktis, kurias galima naudoti su <strong>tipo</strong> srityje. Klientų sąskaitų-faktūrų ir kliento važtaraščiai, <strong>prekybos</strong> šioje srityje.</td>
</tr>
<tr class="odd">
<td>Numeracijos kodas</td>
<td>Pasirinkite į duomenų sritį, kai prašoma serijos numeracijos kodą.</td>
</tr>
<tr class="even">
<td>Tipas</td>
<td>Pasirinkite, ar numeracija taikoma sąskaitų-faktūrų arba važtaraščių.</td>
</tr>
<tr class="odd">
<td>Sąskaitos kodas</td>
<td>Pasirinkite, kaip taikoma SF numerių serijos. Galimos toliau nurodytos pasirinktys:
<ul>
<li><strong>Stalo</strong> – serijos galima tik vartotojas, kuris pažymėtas su <strong>kodas</strong> srityje.</li>
<li><strong>Grupė</strong> – serijos yra vartotojų grupę, kuri yra pasirinkta ir <strong>kodas</strong> srityje.</li>
<li><strong>Visi</strong> -serijos yra prieinama visiems naudotojams.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kodas</td>
<td>Pasirinkite vartotoją arba jų grupę, priskirtą numerių serijos SF numeracijos ID.</td>
</tr>
<tr class="odd">
<td>Paskutinė data</td>
<td>Numerių serijos atnaujinimo data.</td>
</tr>
<tr class="even">
<td>Tęsti</td>
<td>Pasirinkite šią parinktį Norėdami ieškoti numerių serijos, kuri prie pasirinkto vartotojo arba vartotojų grupės.</td>
</tr>
</tbody>
</table>

## <a name="set-up-document-selfnumbering-ranges"></a>Nustatyti dokumento selfnumbering diapazonai
Galite priskirti konkrečių numerių sekas SF ir važtaraščių, kurie yra generuojami dėl **gautinos sąskaitos**, **mokėtinos sumos**, **atsargų valdymo**, ir **projektų valdymo ir apskaitos** modulių. Taip pat galite nurodyti atskirus skirtingiems vartotojams ir vartotojų grupes, klientų grupes ir tiekėjų grupių ar sandėlių numeracijas. Norėdami nustatyti kliento SF ir tiekėjo SF numeraciją, naudokite su **skaitikliai valdymo** puslapis. (Spustelėkite **organizacijos administracijos**&gt;**skaičių sekas**&gt;**skaitikliai valdymo**.) Rodoma numeracija vartotoją arba jų grupę arba specifinėmis pirkėjų grupėmis ir tiekėjų grupes. Naudoti informaciją toliau pateiktoje lentelėje užpildykite laukus dėl to **skaitikliai valdymo** puslapis.

| Laukas          | aprašymas                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Modulis         | Pasirinkite modulio, skirto pasirinktoje numeracijoje.                                                                                 |
| Sąskaitos kodas   | Pasirinkite, ar Numeracijos kodas taikomas visiems įrašams pasirinkto modulio arba modulio konkrečiai grupei.                     |
| Kodas           | Pasirinkite pasirinkto modulio kodas. **Pastaba:** į **kodas** lauką galima tik tada, kai **grupės** pažymėtas ir **sąskaitos kodas** srityje. |
| Tipas           | Pasirinkite numerį ir dokumento tipą: **SF** ar **važtaraščio**.                                                                         |
| Automatinis numeravimas | Pasirinkite šią parinktį, kad automatiškai suteikia numerį dokumentą. Rankiniu būdu galite pažymėti arba išvalyti šį variantą už atskirus dokumentus.       |

Norėdami gauti informacijos apie tai, kaip rankiniu būdu skaičius SF ir važtaraščių, pamatyti [(EEU) redaguoti pardavimo užsakymų SF ID,](https://ax.help.dynamics.com/en/?post_type=incsub_wiki&p=1162853&preview=true).

## <a name="affected-processes"></a>Įtakos procesai
Šių dokumentų antraštėse atnaujinamos SF ir pakuotės lapelis numeraciją:

-   Pardavimo užsakymai
-   Pirkimo užsakymai
-   Laisvos formos sąskaitos faktūros
-   Projekto SF pasiūlymai

Registruojant šiuos dokumentus, galite pasirinkti tam tikra skaičių seka, kad **numeravimas** srityje:

-   Pardavimo važtaraščio
-   Pardavimams registruoti SF
-   Pirkimo registravimo važtaraštis
-   Perkant tiekėjo SF
-   Registruoti projekto SF pasiūlymus
-   Registruoti laisvos formos SF

Be to, žemiau yra blankais, **dokumentai atnaujinti** srityje:

-   Pirkimo tiekėjo SF, forma,
-   Pardavimo važtaraščio registravimo forma,
-   Pardavimo SF formos komandiravimo,
-   Pirkimo registravimo produkto gavimo formą.

Į "**dokumentai atnaujinti**" lauko įtaka į "**dokumento statusas**"laukas"**pakavimo važtaraščio žurnalą**"ir"**SF žurnalas**". Ant **važtaraščio** kūrybą, su "**dokumento statusas**"lauko vertė yra lygi"**nė vienas**". Jei yra **važtaraščio** buvo pasirinkta lauke "**dokumentai atnaujinti**"tada savo"**dokumento būsena**"būtų"**Broken**"ir kad"**dokumento būsena**", **važtaraščio** kur viskas bus "**atšaukta**".


