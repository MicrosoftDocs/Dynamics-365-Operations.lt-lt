---
title: "Kliento registravimo šablonai"
description: "Pagal kliento registravimo šablonus valdomas klientų operacijų registravimas į DK."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: b36e75a5f527b41d50cc73e28a0b4e7e5df67e5c
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2017

---

# <a name="customer-posting-profiles"></a>Kliento registravimo šablonai

[!include[banner](../includes/banner.md)]


Pagal kliento registravimo šablonus valdomas klientų operacijų registravimas į DK.

<a name="customer-posting-profiles"></a>Kliento registravimo šablonai
-------------------------

Klientų registravimo profiliai leidžia DK sąskaitas ir dokumentų nuostatas priskirti visiems klientams, klientų grupei arba vienam klientui. Šios nuostatos bus naudojamos kuriant pardavimo užsakymus, laisvos formos SF, mokėjimus grynaisiais pinigais, priminimo laiškus ir delspinigių pažymas. Kai kurių operacijų registravimo šabloną galite pasirinkti tokį, kuris skiriasi nuo šiame puslapyje operacijoms nustatytų registravimo profilių ir yra už juos svarbesnis. 

Numatytasis registravimo profilis apibrėžiamas „FastTab‟ DK ir PVM, esančiuose Gautinų sumų parametrų puslapyje. Numatytasis registravimo profilis tada automatiškai įtraukiamas naujų dokumentų antraštėje, kur prireikus jį galite pakeisti kitu registravimo profiliu.

Registravimo apibrėžčių puslapyje taip pat galite registravimo apibrėžtis susieti su operacijų registravimo tipais. Klientų operacijų registravimą į DK kontroliuoja registravimo apibrėžtys, o ne registravimo profiliai.

## <a name="creating-a-posting-profile"></a>Registravimo profilio kūrimas
Nurodykite DK sąskaitas, kurios naudojamos registruojant operacijas, kurios naudoja pasirinktą registravimo profilį. Pasirinkti sąskaitos kodą ir, jei galima, pasirinkto registravimo šablono sąskaitos arba grupės numerį. Registruojant, tinkamiausias kiekvienos operacijos registravimo profilis randamas pagal toliau nurodytus prioritetus ieškant konkrečiausio sąskaitos kodo, sąskaitos numerio arba grupės ir numerio derinio.

| **Sąskaitos kodo** lauko reikšmė. | **Sąskaitos / grupės numerio** lauko reikšmė.            | Ieškos prioritetas |
|------------------------------|-------------------------------------------------|-----------------|
| **Lentelė**                    | Konkretus kliento kodas                       | 1               |
| **Grupė**                    | Klientų grupė, priskiriama klientui. | 2               |
| **Visi**                      | Tuščias                                           | 3               |

Jei norite, kad visų kliento operacijų registravimo profilis būtų tas pats, Sąskaitos kodo lauke nustatykite tik vieną registravimo profilį – Visi. Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.

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
<td>Įveskite registravimo šablono kodą. Pavyzdžiui, galite sukurti du registravimo profilius, kad turėtumėte vieną sąskaitą kliento balansams nacionaline valiuta ir kitą – kliento balansams užsienio valiuta. Vieną sąskaitą galite pavadinti Nacionalinė, kitą – Užsienio.</td>
</tr>
<tr class="even">
<td><strong>Aprašymas</strong></td>
<td>Įveskite registravimo profilio aprašą. Jis naudojamas tik tada, kai, registravimo profilį peržiūrint šiame puslapyje, norima jį geriau identifikuoti.</td>
</tr>
<tr class="odd">
<td><strong>Sąskaitos kodas</strong></td>
<td>Pasirinkite, ar registravimo profilis bus taikomas atskiram klientui, klientų grupei, ar visiems klientams.
<ul>
<li><strong>Lentelė</strong> – registravimo profilis taikomas vienam klientui. Sąskaitos / grupės numerio lauke pasirinkite kliento sąskaitą.</li>
<li><strong>Grupė</strong> – registravimo profilis taikomas klientų grupei. Sąskaitos / grupės numerio lauke pasirinkite klientų grupę.</li>
<li><strong>Visi</strong> – registravimo profilis taikomas visiems klientams. Sąskaitos / grupės numerio lauką palikite tuščią.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sąskaitos/grupės Nr.</strong></td>
<td>Jei lauke Sąskaitos kodas pasirinkta Lentelė, pasirinkite kliento, kuris yra susietas su registravimo profiliu, sąskaitos numerį. Jei pasirinkta Grupė, pasirinkite klientų grupę. Jei pasirinkta Visi, šį lauką palikite tuščią.</td>
</tr>
<tr class="odd">
<td><strong>Suminė sąskaita</strong></td>
<td>Pasirinkite DK sąskaitą, kuri bus naudojama kaip klientų, kurie susieti su registravimo profiliu, suminė sąskaita.</td>
</tr>
<tr class="even">
<td><strong>Sudengimo sąskaita</strong></td>
<td>Pasirinkite likvidumo DK sąskaitą, naudojamą pinigų srauto prognozėms. Šis laukas bus rodomi tik įgalinus pinigų srauto prognozes.</td>
</tr>
<tr class="odd">
<td><strong>PVM išankstinai apmokėjimai</strong></td>
<td>Pasirinkite mokėjimų, gaunamų iš anksto, PVM sąskaitą.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Pastaba:" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Pastaba</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Naudokite Gautinų sumų parametrų puslapį, norėdami nurodyti registravimo profilį, naudotiną, kai mokėjimas pažymimas kaip išankstinis mokėjimas.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Nuolaidų sąskaitos skolos</strong></td>
<td>Pasirinkite DK sąskaitą, skirtą nuolaidų įsipareigojimams.</td>
</tr>
<tr class="odd">
<td><strong>Priminimo laiškų seka</strong></td>
<td>Pasirinkite priminimo laiškų sekos identifikatorių, naudotiną su klientais, kuriems priskirtas registravimo profilis.</td>
</tr>
<tr class="even">
<td><strong>Palūkanų kodas</strong></td>
<td>Pasirinkite delspinigių kodą, naudotiną skaičiuojant delspinigius klientams, kuriems priskirtas registravimo profilis.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Lentelių apribojimai**

Operacijoms, kurių registravimo profilis pasirinktasis, nurodykite, ar operacijos bus sudengiamos automatiškai, bus apskaičiuojami delspinigiai ir bus išduodami priminimo laiškai. Taip pat galite pasirinkti sąskaitą, kuri naudojama uždarius operacijas, kurių registravimo profilis pasirinktasis.

Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.

| Laukas                 | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Sudengimas**        | Pasirinkite šį perjungiklį, kad įgalintumėte automatinį operacijų, kurių registravimo profilis yra šis, sudengimą. Jei šis perjungiklis atžymėtas, sudengti operacijas turite rankiniu būdu, naudodami puslapį Sudengti atidarytas operacijas arba puslapį Įvesti klientų mokėjimus. |
| **Pomėgiai**          | Pasirinkite šį perjungiklį, jei turėtų būti skaičiuojami klientų sąskaitų, naudojančių šį profilį, nesumokėtų balansų delspinigiai. Jei šis perjungiklis nepažymėtas, šiems klientams delspinigiai nebus skaičiuojami.                                           |
| **Priminimo laiškas** | Pasirinkite šį perjungiklį, jei turėtų būti generuojami klientų sąskaitų, naudojančių šį profilį, priminimo laiškai. Jei šis perjungiklis nepažymėtas, šiems klientams priminimo laiškai nebus generuojami.                                                 |
| **Uždaryti**             | Pasirinkite registravimo profilį, į kurį bus pakeičiama, kai operacijos, kurioms taikomas šis registravimo profilis, bus uždarytos. Operacija laikoma uždaryta, kai ji yra visiškai sudengta.                                                                           |



Daugiau informacijos žr. [Kliento mokėjimų apžvalga](../cash-bank-management/tasks/customer-payment-overview.md).


