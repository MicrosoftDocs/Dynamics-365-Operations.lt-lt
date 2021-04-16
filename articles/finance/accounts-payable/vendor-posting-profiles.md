---
title: Tiekėjų registravimo šablonai
description: Pagal tiekėjo registravimo šablonus valdomas tiekėjo operacijų registravimas į DK.
author: abruer
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37fb7d2623451313475a6c234e820c7c6295be40
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835489"
---
# <a name="vendor-posting-profiles"></a>Tiekėjų registravimo šablonai

[!include [banner](../includes/banner.md)]

Pagal tiekėjo registravimo šablonus valdomas tiekėjo operacijų registravimas į DK.

<a name="vendor-posting-profiles"></a>Tiekėjų registravimo šablonai
-----------------------

Naudojant tiekėjų registravimo profilius galima didžiosios knygos sąskaitas ir dokumentų parametrus priskirti visiems tiekėjams, tiekėjų grupei arba vienam tiekėjui. Šie parametrai bus naudojami kuriant pirkimo užsakymus, tiekėjo SF ir mokėjimus grynaisiais pinigais. Kai kurioms operacijoms galite pasirinkti tokį registravimo šabloną, kuris skiriasi nuo šiame puslapyje operacijoms nustatytų registravimo šablonų ir yra už juos svarbesnis. Numatytasis registravimo šablonas nustatomas puslapio **Mokėtinų sumų parametrai**„FastTab‟ konteineryje **Didžioji knyga ir PVM**, esančiuose Mokėtinų sumų parametrų puslapyje. Numatytasis registravimo šablonas tada automatiškai įtraukiamas naujų dokumentų antraštėje, kur prireikus jį galite pakeisti kitu registravimo šablonu.

Puslapyje **Operacijų registravimo aprašai** taip pat galite susieti registravimo apibrėžtis su operacijų registravimo tipais. Tiekėjų operacijų registravimą į DK kontroliuoja registravimo apibrėžtys, o ne registravimo profiliai.

## <a name="creating-a-posting-profile"></a>Registravimo profilio kūrimas
### <a name="setup"></a>**Nustatymas**

Nurodykite DK sąskaitas, kurios naudojamos registruojant operacijas, kurios naudoja pasirinktą registravimo profilį. Pasirinkti sąskaitos kodą ir, jei galima, pasirinkto registravimo šablono sąskaitos arba grupės numerį. Vykdant registravimo procedūrą, tinkamiausias kiekvienos operacijos registravimo šablonas randamas pagal toliau nurodytus prioritetus ieškant tiksliausio sąskaitos kodo, sąskaitos numerio arba grupės ir numerio derinio.

| **Sąskaitos kodo** lauko reikšmė. | **Sąskaitos / grupės numerio** lauko reikšmė.        | Ieškos prioritetas |
|------------------------------|---------------------------------------------|-----------------|
| **Lentelė**                    | Konkreti tiekėjo sąskaita                     | 1               |
| **Grupuoti**                    | Tiekėjų grupė, priskirta tiekėjui | 2               |
| **Visos**                      | Tuščias                                       | 3               |

Jei norite, kad visų tiekėjo operacijų registravimo šablonas būtų tas pats, lauke **Sąskaitos kodas** nustatykite tik vieną registravimo šabloną – **Visi**. Norėdami nustatyti registravimo šabloną, nurodykite toliau pateiktas reikšmes.

<table>
<thead>
<tr class="header">
<th>Laukas</th>
<th>Aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Registravimo šablonas</strong></td>
<td>Įveskite registravimo šablono kodą. Pavyzdžiui, galite sukurti du registravimo profilius, kad turėtumėte vieną sąskaitą tiekėjo balansams nacionaline valiuta ir kitą – tiekėjo balansams užsienio valiuta. Vieną sąskaitą galite pavadinti Nacionaline, kitą – Užsienio.</td>
</tr>
<tr class="even">
<td><strong>Aprašymas</strong></td>
<td>Įveskite registravimo profilio aprašą.</td>
</tr>
<tr class="odd">
<td><strong>Sąskaitos kodas</strong></td>
<td>Nurodykite, ar registravimo profilis taikomas konkrečiam tiekėjui, tiekėjų grupei ar visiems tiekėjams.
<ul>
<li><strong>Lentelė</strong> – registravimo profilis taikomas vienam tiekėjui. Lauke <strong>Sąskaita / grupės numeris</strong> pasirinkite tiekėjo sąskaitą.</li>
<li><strong>Grupė</strong> – registravimo profilis taikomas tiekėjų grupei. Lauke <strong>Sąskaita / grupės numeris</strong> pasirinkite tiekėjų grupę.</li>
<li><strong>Visi</strong> – registravimo profilis taikomas visiems tiekėjams. Palikite kauką <strong>Sąskaita / grupės numeris</strong> tuščią.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sąskaitos/grupės Nr.</strong></td>
<td>Jei lauke <strong>Sąskaitos kodas</strong> pasirinkta reikšmė <strong>Lentelė</strong>, pasirinkite tiekėjo, kuris yra susietas su registravimo šablonu, sąskaitos numerį. Jei pasirinkta reikšmė <strong>Grupė</strong>, pasirinkite tiekėjų grupę. Jei pasirinkta <strong>Visi</strong>, šį lauką palikite tuščią.</td>
</tr>
<tr class="odd">
<td><strong>Suminė sąskaita</strong></td>
<td>Pasirinkite DK sąskaitą, kuri bus naudojama kaip tiekėjų, su kuriais susijęs registravimo profilis, suminę sąskaitą. Bus pažymėtas šios pagrindinės sąskaitos parametras <strong>Neleisti įvesti rankiniu būdu</strong>. Jeigu vėliau pašalinsite šią sąskaitą iš registravimo šablono, patvirtinkite parametrą <strong>Neleisti įvesti rankiniu būdu</strong> puslapyje <strong>Pagrindinės sąskaitos</strong>. 
<p><strong>Pastaba.</strong>Jei puslapyje <strong>Didžiosios knygos parametrai</strong> pasirinkta parinktis <strong>Naudoti registravimo apibrėžtis</strong>, tiekėjo SF bus naudojama operacijos registravimo apibrėžtis, o ne suminė sąskaita.</p>
</td>
</tr>
<tr class="even">
<td><strong>Sudengimo sąskaita</strong></td>
<td>Pasirinkite likvidumo DK sąskaitą, naudojamą pinigų srauto prognozėms. Šį lauką galima naudoti tik kai įgalintas pinigų srauto prognozavimas.</td>
</tr>
<tr class="odd">
<td><strong>PVM išankstinai apmokėjimai</strong></td>
<td>Pasirinkite PVM mokėjimų, gaunamų iš anksto, sąskaitą.
<p><strong>Pastaba.</strong> Registravimo šablonas, naudojamas, kai mokėjimas yra pažymėtas kaip išankstinis mokėjimas, pasirenkamas lauke <strong>Registravimo</strong> šablonas su <strong>išankstinio mokėjimo žurnalo kvitu</strong>, esančiame puslapio <strong>Mokėtinų sumų parametrai</strong> srityje <strong>Didžioji knyga ir PVM</strong>.</p>
</td>
</tr>
<tr class="even">
<td><strong>Atvykimas</strong></td>
<td>Pasirinkite DK sąskaitą, kurioje bus registruojama informacija apie nepatvirtintas tiekėjo SF. Informacija įvedama į SF registro žurnalą. Pavyzdžiui, gavus SF SF registre, naudotojas apie tiekėjo SF įveda labai bendrą informaciją. Užregistravus sąskaitų faktūrų registrą, operacijos registruojamos sąskaitoje, kuri įvesta čia ir lauke <strong>Korespondentinė sąskaita</strong>. Patvirtinus sąskaitas faktūras, skola perkeliama iš gavimo sąskaitos į tiekėjo suminę sąskaitą.</td>
</tr>
<tr class="odd">
<td><strong>Korespondentinė sąskaita</strong></td>
<td>Pasirinkite DK sąskaitą, kuri naudojama norint padengti nepatvirtintas tiekėjo SF, kurios atnaujinamos naudojant SF registrą. Korespondentinė sąskaita veikia kaip gavimo sąskaitose užregistruotų operacijų korespondentinė sąskaita. Todėl sąskaitoje yra tiekėjo pirkimų, kurie dar nepatvirtinti.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Lentelių apribojimai**

Operacijoms, kurių registravimo profilis pasirinktasis, nurodykite, ar operacijos bus sudengiamos automatiškai, bus apskaičiuojami delspinigiai ir bus išduodami priminimo laiškai. Taip pat galite pasirinkti sąskaitą, kuri naudojama uždarius operacijas, kurių registravimo profilis pasirinktasis.

Norėdami nustatyti registravimo šabloną, nurodykite toliau pateiktas reikšmes

| Laukas          | Aprašymas                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Atsiskaitymas** | Pasirinkite šią parinktį, kad įgalintumėte automatinį operacijų, kurių registravimo profilis yra šis, sudengimą. Jei ši parinktis atžymėta, sudengti operacijas turite rankiniu būdu puslapyje **Sudengti atidarytas operacijas**. |
| **Atšaukti**     | Pasirinkite šią parinktį, jei norite atšaukti operacijas, kurių registravimo profilis yra šis.                                                                                                               |
| **Uždaryti**      | Pasirinkite registravimo profilį, į kurį bus pakeičiama, kai operacijos, kurioms taikomas šis registravimo profilis, bus uždarytos. Operacija laikoma uždaryta, kai ji yra visiškai sudengta.                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]