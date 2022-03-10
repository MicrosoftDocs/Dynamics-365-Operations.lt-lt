---
title: Kokybės susiejimai
description: Šioje temoje aprašoma, kaip galite naudoti kokybės susiejimus, norėdami automatiškai generuoti kokybės užsakymus, susijusius su jūsų „Microsoft Dynamics 365 Supply Chain Management“ pardavimo, pirkimo ir gamybos procesais.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28984730e5660414eec1ba087eb5de1eba4cbbb8
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571934"
---
# <a name="quality-associations"></a>Kokybės susiejimai

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip galite naudoti kokybės susiejimus, norėdami automatiškai generuoti kokybės užsakymus, susijusius su jūsų „Microsoft Dynamics 365 Supply Chain Management“ pardavimo, pirkimo ir gamybos procesais.

Kokybės susiejimas apibrėžia visą toliau nurodytą generuojamo kokybės užsakymo informaciją.

- Operacijos įvykį.
- Prekių bandymų, kuriuos reikia atlikti, rinkinį.
- Priimamas kokybės lygmuo (AQL)
- Pavyzdžių ėmimo planą.

Turite apibrėžti kiekvieno verslo proceso varianto, kuriam reikalingas automatinis kokybės užsakymų generavimas, kokybės susiejimą. Pavyzdžiui, galima generuoti pirkimo užsakymų, sulaikymo užsakymų, pardavimo užsakymų ir gamybos užsakymų verslo procesų kokybės užsakymą.

## <a name="working-with-quality-associations"></a>Darbas su kokybės susiejimais

Verslo procesas, kuris naudoja kokybės susiejimą, gali būti susijęs su įvairiais šaltinio dokumentais, pvz., pirkimo užsakymais, pardavimo užsakymais ar gamybos užsakymais.

Kiekvienas kokybės susiejimo įrašas apibrėžia bandymų rinkinį, AQL ir pavyzdžių ėmimo planą, kuris taikomas generuojamiems kokybės užsakymams. Turite apibrėžti kiekvieno verslo proceso varianto kokybės susiejimo įrašą. Pavyzdžiui, galite nustatyti kokybės susiejimą, kuris generuoja kokybės užsakymą, kai atnaujinamas pirkimo užsakymo produktų kvitas. Atsižvelgiant į vykdymo plano nustatymą, kol yra atviras kokybės užsakymas, paleidimo procesas gali būti užblokuotas. Kitu atveju vėlesni procesai, pavyzdžiui, pirkimo užsakymų SF išrašymas, gali būti užblokuoti.

> [!NOTE]
> Kol yra atidarytų kokybės užsakymų, automatiškai blokuojamas atsargų kiekių išdavimas. Atsižvelgiant į **Visiško blokavimo** laukelio nustatymus **Prekių pavyzdžių** puslapyje, kiekis yra arba kokybės užsakymo kiekis, arba šaltinio dokumento eilutės kiekis. Daugiau informacijos ieškokite Kokybės [prekės bandymo valdymo tikrinimo](quality-item-sampling.md) priemonės.

Nurodyto verslo proceso kokybės susiejimo įrašas identifikuoja įvykį ir sąlygas, kuriems sugeneruotas kokybės užsakymas. Sąlygos gali būti būdingos teritorijai arba juridiniam subjektui. Ardomuosius bandymus apimantis kokybės užsakymas gali būti sugeneruotas tik kai yra turimų įvykio atsargų.

Norėdami dirbti su kokybės susiejimais, **eikite į Atsargų valdymo \> nustatymo kokybės kontrolės \> kokybės \>susiejimus**. Toliau pateikti pavyzdžiai rodo, kaip kokybės susiejimo įrašas apibrėžiamas kiekvieno verslo proceso pokyčiams. Toliau pateiktoje lentelėje apibendrinami kiekvieno pavyzdžio įvykiai ir sąlygos, kuriuos apibrėžia kokybės susiejimo įrašas.

<table>
<thead>
<tr>
<th>Nuorodos tipas</th>
<th>Įvykio tipas</th>
<th>Vykdymas</th>
<th>Įvykio blokavimas</th>
<th>Dokumento nuoroda</th>
</tr>
</thead>
<tbody>
<tr>
<td>Atsargos</td>
<td>Netaikoma</td>
<td>Netaikoma</td>
<td>Nėra</td>
<td>Visi</td>
</tr>
<tr>
<td rowspan="7">Pardavimas</td>
<td rowspan="4">Išrinkimo procesas suplanuotas</td>
<td rowspan="4">Prieš</td>
<td>Nėra</td>
<td rowspan="22">Konkretus ID, Grupė arba tik Viskas.</td>
</tr>
<tr>
<td>Išrinkimo procesas</td>
</tr>
<tr>
<td>Važtaraštis</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="3">Važtaraštis</td>
<td rowspan="3">Prieš</td>
<td>Nėra</td>
</tr>
<tr>
<td>Važtaraštis</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="15">Pirkimas</td>
<td rowspan="7">Kvitų sąrašas</td>
<td rowspan="4">Prieš</td>
<td>Nėra</td>
</tr>
<tr>
<td>Kvitų sąrašas</td>
</tr>
<tr>
<td>Gavimo dokumentas</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="3">Po</td>
<td>Nėra</td>
</tr>
<tr>
<td>Gavimo dokumentas</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="3">Registracija</td>
<td rowspan="3">Netaikoma</td>
<td>Nėra</td>
</tr>
<tr>
<td>Gavimo dokumentas</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="5">Gavimo dokumentas</td>
<td rowspan="3">Prieš</td>
<td>Nėra</td>
</tr>
<tr>
<td>Gavimo dokumentas</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="2">Po</td>
<td>Nėra</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="8">Gamyba</td>
<td rowspan="3">Registracija</td>
<td rowspan="3">Netaikoma</td>
<td>Nėra</td>
<td rowspan="12">Visi</td>
</tr>
<tr>
<td>Pranešti apie pabaigimą</td>
</tr>
<tr>
<td>Pabaigti</td>
</tr>
<tr>
<td rowspan="5">Pranešti apie pabaigimą</td>
<td rowspan="3">Prieš</td>
<td>Nėra</td>
</tr>
<tr>
<td>Pranešti apie pabaigimą</td>
</tr>
<tr>
<td>Pabaigti</td>
</tr>
<tr>
<td rowspan="2">Po</td>
<td>Nėra</td>
</tr>
<tr>
<td>Pabaigti</td>
</tr>
<tr>
<td rowspan="4">Sulaikymas</td>
<td rowspan="3">Pranešti apie pabaigimą</td>
<td rowspan="2">Prieš</td>
<td>Pranešti apie pabaigimą</td>
</tr>
<tr>
<td>Pabaigti</td>
</tr>
<tr>
<td>Po</td>
<td>Pabaigti</td>
</tr>
<tr>
<td>Pabaigti</td>
<td>Prieš</td>
<td>Pabaigti</td>
</tr>
<tr>
<td rowspan="3">Maršruto operacija</td>
<td rowspan="3">Skelbti baigtu</td>
<td rowspan="2">Iki</td>
<td>None</td>
<td rowspan="3">Konkretus ID, Grupė arba Viskas, ir Konkretaus išteklių Grupė arba Viskas</td>
</tr>
<tr>
<td>Skelbti baigtu</td>
</tr>
<tr>
<td>Po</td>
<td>None</td>
</tr>
<tr>
<td rowspan="3">Sudėtinio produkto gamyba</td>
<td>Registracija</td>
<td>Netaikoma</td>
<td rowspan="3">None</td>
<td rowspan="3">Visos</td>
</tr>
<tr>
<td rowspan="2">Skelbti baigtu</td>
<td>Iki</td>
</tr>
<tr>
<td>Po</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Funkcija *Sandėlio procesų kokybės valdymas* įtraukia kokybės užsakymų apdorojimo galimybių, skirtų gamybai, kuriame **Įvykio tipas** nustatytas į *Skelbti baigtu* laukelį ir **Vykdymas** nustatytas į *Po* laukelį ir pirkimui, kai **Įvykio tipas** nustatytas į *Registracija*. Dėl platesnės informacijos, žr. [Kokybės valdymas sandėlio apdorojimams](quality-management-for-warehouses-processes.md).

Toliau pateiktoje lentelėje pateikiama daugiau informacijos apie tai, kaip galima generuoti konkrečių tipų procesų kokybės užsakymus.

<div class="tableSection">
<table>
<thead>
<tr>
<th>Proceso tipas</th>
<th>Kai kokybės užsakymus galima generuoti automatiškai.</th>
<th>Kai kokybės užsakymus galima generuoti, jei reikia ardomojo bandymo.</th>
<th>Sąlygų informacija</th>
<th>Rankinio generavimo informacija</th>
</tr>
</thead>
<tbody>
<tr>
<td>Pirkimo užsakymas</td>
<td>Prieš užregistruojant kvitų sąrašą arba gautos medžiagos kvitą, arba po to.</td>
<td>Užregistravus gautos medžiagos kvitą, nes medžiaga turi būti prieinama ardomajam bandymui.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją, prekę, tiekėją arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pirkimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Sulaikymo užsakymas</td>
<td>Prieš sulaikymo užsakymą nurodant baigtu arba po to.</td>
<td>Kokybės užsakymų, kuriems reikia atlikti ardomuosius bandymus, generuoti negalima. Daroma prielaida, kad sulaikymo užsakymo funkcijos tvarko sunaikintos medžiagos perdavimą.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją, prekę, tiekėją arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis sulaikymo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Pardavimo užsakymas</td>
<td>Prieš siunčiamų prekių suplanuotą paėmimo procesą ar važtaraščio naujinimą.</td>
<td>Atliekant bet kurį veiksmą.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją, prekę, klientą arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pardavimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Gamybos užsakymas</td>
<td>Prieš pranešant apie baigtą gamybos užsakymo kiekį, arba po to.</td>
<td>Pranešus apie baigtą gamybos užsakymo kiekį.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją ar prekę, tiekėją arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis gamybos užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Gamybos užsakymas su maršruto operacija</td>
<td>Prieš baigiant operacijos ataskaitą, arba po to.</td>
<td>Pranešus, kad paskutinės operacijos gamyba baigta.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti konkrečią teritoriją, prekę ar operacijų išteklių, arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis maršruto operaciją, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Inventorizacijos</td>
<td>Kokybės užsakymo negalima automatiškai generuoti atsargų žurnalo operacijai arba perkėlimo užsakymo operacijoms.</td>
<td></td>
<td></td>
<td>Prekės atsargų kiekio kokybės užsakymą reikia kurti rankiniu būdu. Reikia faktiškai turimų atsargų.</td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Automatinio kokybės užsakymų generavimo pavyzdžiai

### <a name="purchasing"></a>Pirkimas

Pirkdami, jei nustatėte lauko **Įvykio tipas** reikšmę *Gavimo dokumentas* ir lauko **Vykdymas** reikšmę *Po*, puslapyje **Kokybės susiejimai** gausite šiuos rezultatus:

- Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė *Taip*, kokybės užsakymas generuojamas kiekvienam dokumentui pagal pirkimo užsakymą, remiantis gautu kiekiu ir prekės pavyzdžių ėmimo parametrais. Kiekvieną kartą, kai pagal pirkimo užsakymą gaunamas kiekis, remiantis naujai gautu kiekiu generuojami nauji kokybės užsakymai.
- Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė *Ne*, kokybės užsakymas generuojamas pirmajam dokumentui pagal pirkimo užsakymą, remiantis gautu kiekiu. Be to, remiantis likusiu kiekiu kuriamas vienas ar daugiau kokybės užsakymų, atsižvelgiant į sekimo dimensijas. Kokybės užsakymai negeneruojami vėlesniems kvitams pagal pirkimo užsakymą.

### <a name="production"></a>Gamyba

Gamybos aplinkoje, jei nustatėte lauko **Įvykio tipas** reikšmę *Gavimo dokumentas* ir lauko **Skelbti baigtu** reikšmę *Po*, puslapyje **Kokybės susiejimai** gausite šiuos rezultatus:

- Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė *Taip*, kokybės užsakymas generuojamas kiekvienam baigtam kiekiui ir pagal prekės pavyzdžių ėmimo parametrus. Kiekvieną kartą, kai pagal gamybos užsakymą kiekis paskelbiamas baigtu, remiantis naujai baigtu kiekiu generuojami nauji kokybės užsakymai. Ši generavimo logika atitinka pirkimą.
- Jei nustatyta parinkties **Pagal atnaujintą kiekį** reikšmė *Ne*, kokybės užsakymas generuojamas pirmą kartą, kai kiekis paskelbiamas baigtu, remiantis baigtu kiekiu. Be to, remiantis likusiu kiekiu kuriamas vienas ar daugiau kokybės užsakymų, atsižvelgiant į prekės pavyzdžių ėmimo sekimo dimensijas. Kokybės užsakymai negeneruojami vėliau baigtiems kiekiams.

<table>
<thead>
<tr>
<th>Kokybės specifikacija</th>
<th>Pagal atnaujintą kiekį</th>
<th>Pagal sekimo dimensiją</th>
<th>Rezultatas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Procentinė reikšmė: 10 %</td>
<td>Taip</td>
<td>
<p>Paketo numeris: ne</p>
<p>Serijos numeris: ne</p>
</td>
<td>
<p>Užsakymo kiekis: 100</p>
<ol>
<li>Paskelbti kaip baigtą 30
<ul>
<li>Kokybės užsakymas #1, skirtas 3 (10 % iš 30)</li>
</ul>
</li>
<li>Paskelbti kaip baigtą 70
<ul>
<li>Kokybės užsakymas #2, skirtas 7 (10 % likusio užsakymo kiekio, kuris šiuo atveju yra lygus 70)</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fiksuotas kiekis: 1</td>
<td>Ne</td>
<td>
<p>Paketo numeris: ne</p>
<p>Serijos numeris: ne</p>
</td>
<td>Užsakymo kiekis: 100
<ol>
<li>Paskelbti kaip baigtą 30
<ul>
<li>Kokybės užsakymas #1, skirtas 1 (pirmajam paskelbtam baigtu kiekiui, kuris turi 1 fiksuotą vertę)</li>
<li>Kokybės užsakymas #2, skirtas 1 (likusiam kiekiui, kuris vis dar turi 1 fiksuotą vertę)</li>
</ul>
</li>
<li>Paskelbti kaip baigtą 10
<ul>
<li>Nėra sukurtų kokybės užsakymų.</li>
</ul>
</li>
<li>Paskelbti kaip baigtą 60
<ul>
<li>Nėra sukurtų kokybės užsakymų.</li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td>Fiksuotas kiekis: 1</td>
<td>Taip</td>
<td>
<p>Paketo numeris: taip</p>
<p>Serijos numeris: taip</p>
</td>
<td>
<p>Užsakymo kiekis: 10</p>
<ol>
<li>Baigta, jei numeris b1, s1 serijos numeris – 3: 1; 1 paketo numeriui b2, s2 serijos numeriui; ir 1 paketo numerio b3, s3 serijos numerio
<ul>
<li>Kokybės užsakymas #1, skirtas 1, paketo numeris #b1, serijos #s1</li>
<li>Kokybės užsakymas #2, skirtas 1, paketo numeris #b2, serijos #s2</li>
<li>Kokybės užsakymas #3, skirtas 1, paketo numeris #b3, serijos #s3</li>
</ul>
</li>
<li>Baigta, jei numeris 2: 1, paketo numeris b4, s4 serijos numeris ir 1 paketo numeriui b5, s5 serijos numeriams
<ul>
<li>Kokybės užsakymas #4, skirtas 1, paketo numeris #b4, serijos #s4</li>
<li>Kokybės užsakymas #5, skirtas 1, paketo numeris #b5, serijos #s5</li>
</ul>
</li>
</ol>
<p><strong>Pastaba:</strong> paketą galima naudoti pakartotinai.</p>
</td>
</tr>
<tr>
<td>Fiksuotas kiekis: 2</td>
<td>Ne</td>
<td>
<p>Paketo numeris: taip</p>
<p>Serijos numeris: taip</p>
</td>
<td>
<p>Užsakymo kiekis: 10</p>
<ol>
<li>Baigta, jei numeris b1, s1 serijos numeris – 3: 1; 1 paketo numeriui b2, s2 serijos numeriui; ir 1 paketo numerio b3, s3 serijos numerio ir 1 paketo numeriui b4, serijiniam numeriui s4
<ul>
<li>Kokybės užsakymas #1, skirtas 1, paketo numeris #b1, serijos #s1</li>
<li>Kokybės užsakymas #2, skirtas 1, paketo numeris #b2, serijos #s2</li>
<li>Kokybės užsakymas #3, skirtas 1, paketo numeris #b3, serijos #s3</li>
<li>Kokybės užsakymas #4, skirtas 1, paketo numeris #b4, serijos #s4</li>
</ul>
<ul>
<li>Kokybės užsakymas #5, skirtas 2, be nuorodos į paketą ir serijos numerį</li>
</ul>
</li>
<li>Baigta, jei 6: 1, paketo numeris b5, s5 serijos numeris; 1 paketo numeriui b6, serijos numeris s6; 1 paketo numeriui b7, serijos numeris s7; 1 paketo numeriui b8, serijos numeris s8; 1 paketo numeriui b9, serijos numeris s9; ir 1 paketo numeriui b10, serijos numeris s10
<ul>
<li>Nėra sukurtų kokybės užsakymų.</li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo procesai](quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
