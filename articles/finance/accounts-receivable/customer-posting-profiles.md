---
title: Kliento registravimo šablonai
description: Šioje temoje aprašomi kliento registravimo šablonai, kurie kontroliuoja klientų operacijų registravimą DK.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ed5ab24e37c75222080bd242aa72a39ecb476bf
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734638"
---
# <a name="customer-posting-profiles"></a>Kliento registravimo šablonai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomi kliento registravimo šablonai, kurie kontroliuoja klientų operacijų registravimą DK.

## <a name="customer-posting-profiles"></a>Kliento registravimo šablonai

Klientų registravimo profiliai leidžia priskirti DK sąskaitas ir dokumento parametrus visiems klientams, klientų grupei arba vienam klientui. Šie parametrai bus naudojami kuriant pardavimo užsakymų SF, laisvos formos SF, projekto SF, mokėjimo žurnalus, priminimo laiškus ir delspinigių pastabas. 

Numatytasis registravimo šablonas nustatytas gautinų sumų **parametrų puslapio skirtuke** DK **ir PVM**. Tada ji automatiškai įtraukiama į naujų dokumentų antraštę. Jei reikia kito registravimo šablono, galite jį pakeisti. 

Organizacijos, kurios priima išankstinius apmokėjimus iš klientų, dažnai konfigūruoja antrą išankstinių mokėjimų registravimo šabloną ir susieja jį su parametrais kaip numatytąjį išankstinių mokėjimų registravimo šabloną. Daugiau informacijos ieškokite Kliento išankstiniai [mokėjimai](customer-prepayments.md).

Puslapyje **Operacijų registravimo aprašai** taip pat galite susieti registravimo apibrėžtis su operacijų registravimo tipais. Registravimo aprašai naudojami vietoje registravimo šablonų norint valdyti klientų operacijų registravimą DK. Daugiau informacijos ieškokite [Registravimo aprašų pavyzdžiai](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Registravimo profilio kūrimas
Nurodykite DK sąskaitas, kurios naudojamos registruojant operacijas, kurios naudoja pasirinktą registravimo profilį. Pasirinkti sąskaitos kodą ir, jei galima, pasirinkto registravimo šablono sąskaitos arba grupės numerį. Registruojant, tinkamiausias kiekvienos operacijos registravimo profilis randamas pagal toliau nurodytus prioritetus ieškant konkrečiausio sąskaitos kodo, sąskaitos numerio arba grupės ir numerio derinio.

| Sąskaitos kodo lauko reikšmė. | Sąskaitos / grupės numerio lauko reikšmė.                | Ieškos prioritetas |
|--------------------------|-------------------------------------------------|-----------------|
| Lentelė                    | Konkretus kliento kodas                       | 1               |
| Grupuoti                    | Klientų grupė, priskiriama klientui. | 2               |
| Viskas                      | Tuščias                                           | 3               |

Jei norite, kad visų kliento operacijų registravimo šablonas būtų tas pats, nustatykite tik vieną registravimo šabloną, **kur** Lauke Sąskaitos kodas bus **įvesta Viskas**. Norėdami nustatyti registravimo šabloną, nurodykite toliau pateiktas reikšmes.

<table>
<thead>
<tr>
<th>Laukas</th>
<th>Aprašymas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Registravimo profilis</td>
<td>Įveskite registravimo šablono kodą. Pavyzdžiui, galite sukurti du registravimo profilius, kad turėtumėte vieną sąskaitą kliento balansams nacionaline valiuta ir kitą – kliento balansams užsienio valiuta. Vieną sąskaitą galite pavadinti Nacionalinė, kitą – Užsienio.</td>
</tr>
<tr>
<td>Aprašymas</td>
<td>Įveskite registravimo profilio aprašą. Jis naudojamas tik tada, kai, registravimo profilį peržiūrint šiame puslapyje, norima jį geriau identifikuoti.</td>
</tr>
<tr>
<td>Sąskaitos kodas</td>
<td>Pasirinkite, ar registravimo profilis bus taikomas atskiram klientui, klientų grupei, ar visiems klientams.
<ul>
<li><b>Lentelė</b> – registravimo profilis taikomas vienam klientui. Lauke Sąskaitos/grupės numeris <b>pasirinkite kliento</b> sąskaitą.</li>
<li><b>Grupė</b> – registravimo profilis taikomas klientų grupei. Lauke Sąskaitos/grupės numeris <b>pasirinkite klientų</b> grupę.</li>
<li><b>Visi</b> – registravimo profilis taikomas visiems klientams. Palikite kauką <b>Sąskaita / grupės numeris</b> tuščią.</li>
</ul>
</td>
</tr>
<tr>
<td>Sąskaitos/grupės Nr.</td>
<td>Jei <b>lauke</b> Sąskaitos kodas pasirinkta <b>lentelė</b>, pasirinkite su registravimo šablonu susieto kliento sąskaitos numerį. Jei <b>pasirinkta</b> Grupė, pasirinkite klientų grupę. Jei pasirinkta <b>Visi</b>, šį lauką palikite tuščią.</td>
</tr>
<tr>
<td>Suminė sąskaita</td>
<td>Pasirinkite pagrindinę sąskaitą, kuri bus naudojama kaip klientų, susijusių su registravimo šablonu, gautinų sumų prekybos sąskaita. Ši sąskaita yra kliento balanso <b>registravimo</b> tipo sąskaita.</td>
</tr>
<tr>
<td>Mokėjimų likvidumo sąskaita</td>
<td>Pasirinkite likvidumo DK sąskaitą, naudojamą pinigų srauto prognozėms. Šis laukas bus rodomas tik įgalinus pinigų srautų prognozes.</td>
</tr>
<tr>
<td>PVM išankstinai apmokėjimai</td>
<td><p>Pasirinkite mokėjimų, gaunamų iš anksto, PVM sąskaitą.</p>
<p><strong>Pastaba:</strong> norėdami nurodyti registravimo <b>šabloną, kuris</b> naudojamas, kai mokėjimas pažymimas kaip išankstinis apmokėjimas, naudokite puslapį Gautinų sumų parametrai.</p>
</td>
</tr>
<tr>
<td>Nuolaidų sąskaitos skolos</td>
<td>Pasirinkite DK sąskaitą, skirtą nuolaidų įsipareigojimams.</td>
</tr>
<tr>
<td>Priminimo laiškų seka</td>
<td>Pasirinkite priminimo laiškų sekos identifikatorių, naudotiną su klientais, kuriems priskirtas registravimo profilis.</td>
</tr>
<tr>
<td>Palūkanų kodas</td>
<td>Pasirinkite delspinigių kodą, naudotiną skaičiuojant delspinigius klientams, kuriems priskirtas registravimo profilis.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Registravimo pavyzdžiai

Toliau pateikiamoje lentelėje pateikiami numatytųjų registravimo tipų, kurių pagrindinės sąskaitos ir aprašymai yra pavyzdiniai, pavyzdžiai. Stulpelis **Debetas/** kreditas nurodo, ar operacija paprastai gali būti debetas, ar kreditas, arba, kai kuriais atvejais, gali registruoti vieną iš šių operacijų. Kliringo **sąskaitos** stulpelis nurodo, kad registravimo tipas yra tarpuskaitos sąskaita. Tai reiškia, kad šioje sąskaitoje užregistruota suma automatiškai atšaukiama, kai užregistruojama vėlesnė operacija. 

| Registravimo tipas | Pagrindinės sąskaitos pavyzdys | Pagrindinės sąskaitos pavadinimo pavyzdys | Kodo tipas | Debetas / kreditas | Tarpuskaitos sąskaita | Aprašymas |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Kliento balansas | 130100 | Gautinų sumų prekyba | Turtas | Abu | Ne | Lauke Su suvestinėje sąskaita **nurodykite** sąskaitą.|
| Jokia | 110110 | Banko kodas | Turtas | Abu | Ne | Nurodykite pagrindinę sąskaitą mokėjimo **likvidumo sąskaitoje**. Ši sąskaita nėra naudojama registruoti. Jis naudojamas tik pinigų srautų prognozei. |
| PVM išankstinai apmokėjimai | 202900 | PVM tarpuskaita | Įsipareigojimai | Abu | Taip | Pasirinkite mokėjimų, gaunamų iš anksto, PVM sąskaitą. |
| Nuolaidų sąskaitos skolos | 250600 | Atidėtos įplaukos ir nuolaidos | Įsipareigojimai | Abu | Taip | Pasirinkti nuolaidų įsipareigojimų DK sąskaitą.|     

### <a name="table-restrictions"></a>Lentelių apribojimai

Operacijoms, kurių registravimo profilis pasirinktasis, nurodykite, ar operacijos bus sudengiamos automatiškai, bus apskaičiuojami delspinigiai ir bus išduodami priminimo laiškai. Taip pat galite pasirinkti sąskaitą, kuri naudojama uždarius operacijas, kurių registravimo profilis pasirinktasis.

Norėdami nustatyti savo registravimo profilį, nurodykite toliau pateiktas reikšmes.

| Laukas                 | Prekės/Paslaugos pavadinimas                                           |
|-----------------------|-------------------------------------------------------|
| Setlmentas        | Pasirinkite šį perjungiklį, kad įgalintumėte automatinį operacijų, kurių registravimo profilis yra šis, sudengimą. Jei šis perjungimo langas išvalytas, turite rankiniu būdu sudengti operacijas, naudodami puslapį **Sudengti** atviras operacijas arba **kliento mokėjimų enter** puslapį. |
| Pomėgiai          | Pasirinkite šį perjungiklį, jei turėtų būti skaičiuojami klientų sąskaitų, naudojančių šį profilį, nesumokėtų balansų delspinigiai. Jei šis perjungiklis nepažymėtas, šiems klientams delspinigiai nebus skaičiuojami.                                           |
| Priminimo laiškas | Pasirinkite šį perjungiklį, jei turėtų būti generuojami klientų sąskaitų, naudojančių šį profilį, priminimo laiškai. Jei šis perjungiklis nepažymėtas, šiems klientams priminimo laiškai nebus generuojami.                                                 |
| Uždaryti             | Pasirinkite registravimo profilį, į kurį bus pakeičiama, kai operacijos, kurioms taikomas šis registravimo profilis, bus uždarytos. Operacija laikoma uždaryta, kai ji yra visiškai sudengta.             |



Daugiau informacijos žr. [Kliento mokėjimų apžvalga](../cash-bank-management/tasks/customer-payment-overview.md).



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
