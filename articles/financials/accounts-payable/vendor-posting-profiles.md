---
title: "Tiekėjų registravimo šablonai"
description: "Pagal tiekėjo registravimo šablonus valdomas tiekėjo operacijų registravimas į DK."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7bf37ff484323fb05a35419889f2f89ab124fb27
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-posting-profiles"></a>Tiekėjų registravimo šablonai

[!include[banner](../includes/banner.md)]


Pagal tiekėjo registravimo šablonus valdomas tiekėjo operacijų registravimas į DK.

<a name="vendor-posting-profiles"></a>Tiekėjų registravimo šablonai
-----------------------

Tiekėjų registravimo profiliai leidžia DK sąskaitas ir dokumentų nuostatas priskirti visiems tiekėjams, tiekėjų grupei arba vienam tiekėjui. Šios nuostatos bus naudojamos kuriant pirkimo užsakymus, tiekėjo SF ir mokėjimus grynaisiais pinigais. Kai kurių operacijų registravimo profilį galite pasirinkti tokį, kuris skiriasi nuo šiame puslapyje operacijoms nustatytų registravimo profilių ir yra už juos svarbesnis. Numatytasis registravimo profilis apibrėžiamas „FastTab‟ DK ir PVM, esančiuose Mokėtinų sumų parametrų puslapyje. Numatytasis registravimo profilis tada automatiškai įtraukiamas naujų dokumentų antraštėje, kur prireikus jį galite pakeisti kitu registravimo profiliu.

Registravimo apibrėžčių puslapyje taip pat galite registravimo apibrėžtis susieti su operacijų registravimo tipais. Tiekėjų operacijų registravimą į DK kontroliuoja registravimo apibrėžtys, o ne registravimo profiliai.

## <a name="creating-a-posting-profile"></a>Registravimo profilio kūrimas
### <a name="setup"></a>**Nustatymas**

Nurodykite DK sąskaitas, kurios naudojamos registruojant operacijas, kurios naudoja pasirinktą registravimo profilį. Pasirinkti sąskaitos kodą ir, jei galima, pasirinkto registravimo šablono sąskaitos arba grupės numerį. Registruojant, tinkamiausias kiekvienos operacijos registravimo profilis randamas pagal toliau nurodytus prioritetus ieškant konkrečiausio sąskaitos kodo, sąskaitos numerio arba grupės ir numerio derinio.

| **Sąskaitos kodo** lauko reikšmė. | **Sąskaitos / grupės numerio** lauko reikšmė.        | Ieškos prioritetas |
|------------------------------|---------------------------------------------|-----------------|
| **Lentelė**                    | Konkreti tiekėjo sąskaita                     | 1               |
| **Grupė**                    | tiekėjų grupė, priskirta tiekėjui | 2               |
| **Visi**                      | Tuščias                                       | 3               |

Jei norite, kad visų tiekėjo operacijų registravimo profilis būtų tas pats, Sąskaitos kodo lauke nustatykite tik vieną registravimo profilį – Visi. Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Laukas</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Registravimo šablonas</strong></td>
<td>Įveskite registravimo šablono kodą. Pavyzdžiui, galite sukurti du registravimo profilius, kad turėtumėte vieną sąskaitą tiekėjo balansams nacionaline valiuta ir kitą – tiekėjo balansams užsienio valiuta. Vieną sąskaitą galite pavadinti Nacionalinė, kitą – Užsienio.</td>
</tr>
<tr class="even">
<td><strong>Aprašymas</strong></td>
<td>Įveskite registravimo profilio aprašą.</td>
</tr>
<tr class="odd">
<td><strong>Sąskaitos kodas</strong></td>
<td>Nurodykite, ar registravimo profilis taikomas konkrečiam tiekėjui, tiekėjų grupei ar visiems tiekėjams.
<ul>
<li><strong>Lentelė</strong> – registravimo profilis taikomas vienam tiekėjui. Sąskaitos / grupės numerio lauke pasirinkite tiekėjo sąskaitą.</li>
<li><strong>Grupė</strong> – registravimo profilis taikomas tiekėjų grupei. Sąskaitos / grupės numerio lauke pasirinkite tiekėjų grupę.</li>
<li><strong>Visi</strong> – registravimo profilis taikomas visiems tiekėjams. Sąskaitos / grupės numerio lauką palikite tuščią.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sąskaitos/grupės Nr.</strong></td>
<td>Jei lauke Sąskaitos kodas pasirinkta Lentelė, pasirinkite tiekėjo, kuris yra susietas su registravimo profiliu, sąskaitos numerį. Jei pasirinkta Grupė, pasirinkite tiekėjų grupę. Jei pasirinkta Visi, šį lauką palikite tuščią.</td>
</tr>
<tr class="odd">
<td><strong>Suminė sąskaita</strong></td>
<td>Pasirinkite DK sąskaitą, kuri bus naudojama kaip tiekėjų, su kuriais susijęs registravimo profilis, suminę sąskaitą.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Pastaba:" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Pastaba</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Jei DK parametrų puslapyje pasirinktas perjungiklis Naudoti registravimo apibrėžtis, vietoj suminės sąskaitos naudojama tiekėjų SF operacijų registravimo apibrėžtis.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Sudengimo sąskaita</strong></td>
<td>Pasirinkite likvidumo DK sąskaitą, naudojamą pinigų srauto prognozėms. Šį lauką galima naudoti tik kai įgalintas pinigų srauto prognozavimas.</td>
</tr>
<tr class="odd">
<td><strong>PVM išankstinai apmokėjimai</strong></td>
<td>Pasirinkite PVM mokėjimų, gaunamų iš anksto, sąskaitą.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Pastaba:" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Pastaba</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Registravimo profilis, naudojamas, kai mokėjimas pažymimas kaip išankstinis mokėjimas, pasirenkamas lauke Registravimo profilis su išankstinio mokėjimo žurnalo kvitu, esančiame Mokėtinų sumų parametrų puslapio srityje DK ir PVM.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Atvykimas</strong></td>
<td>Pasirinkite DK sąskaitą, kurioje bus registruojama informacija apie nepatvirtintas tiekėjo SF. Informacija įvedama į SF registro žurnalą. Pavyzdžiui, gavus SF SF registre, naudotojas apie tiekėjo SF įveda labai bendrą informaciją. Užregistravus SF registrą, operacijos registruojamos sąskaitoje, kuri įvesta čia ir lauke Korespondentinė sąskaita. Patvirtinus SF, skola perkeliama iš sąskaitos Gavimas į tiekėjo suminę sąskaitą.</td>
</tr>
<tr class="odd">
<td><strong>Koresp. sąskaita</strong></td>
<td>Pasirinkite DK sąskaitą, kuri naudojama norint padengti nepatvirtintas tiekėjo SF, kurios atnaujinamos naudojant SF registrą. Korespondentinė sąskaita veikia kaip gavimo sąskaitose užregistruotų operacijų korespondentinė sąskaita. Todėl sąskaitoje yra tiekėjo pirkimų, kurie dar nepatvirtinti.</td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a>**Lentelių apribojimai**

Operacijoms, kurių registravimo profilis pasirinktasis, nurodykite, ar operacijos bus sudengiamos automatiškai, bus apskaičiuojami delspinigiai ir bus išduodami priminimo laiškai. Taip pat galite pasirinkti sąskaitą, kuri naudojama uždarius operacijas, kurių registravimo profilis pasirinktasis.

Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.

| Laukas          | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sudengimas** | Pasirinkite šią parinktį, kad įgalintumėte automatinį operacijų, kurių registravimo profilis yra šis, sudengimą. Jei ši parinktis atžymėta, sudengti operacijas turite rankiniu būdu, naudodami puslapį Sudengti atidarytas operacijas. |
| **Atšaukti**     | Pasirinkite šią parinktį, jei norite atšaukti operacijas, kurių registravimo profilis yra šis.                                                                                                               |
| **Uždaryti**      | Pasirinkite registravimo profilį, į kurį bus pakeičiama, kai operacijos, kurioms taikomas šis registravimo profilis, bus uždarytos. Operacija laikoma uždaryta, kai ji yra visiškai sudengta.                                       |






