---
title: Ataskaitos komponentų tvarkymas ataskaitų dizaino įrankyje
description: Šiame straipsnyje paaiškinama, kaip ataskaitų dizaino įrankyje tvarkyti esamas ataskaitas, kūrimo blokus ir objektus.
author: aprilolson
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a94a88114072792243026e441e6c5a62ee80fc56
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802694"
---
# <a name="organize-report-components-in-report-designer"></a>Ataskaitos komponentų tvarkymas ataskaitų dizaino įrankyje

[!include [banner](../includes/banner.md)]

Sukūrus kūrimo blokus ir sugeneravus ataskaitas, patartina šiuos objektus sutvarkyti, kad vartotojai galėtų juos lengviau rasti. Šiame straipsnyje paaiškinama, kaip ataskaitų dizaino įrankyje tvarkyti esamas ataskaitas, kūrimo blokus ir objektus.

Galite pervardyti aplankus, ataskaitas, kūrimo blokus ir kitus objektus ataskaitų konstruktoriuje, kad padėtų tvarkyti savo failus. Atsižvelgiant į pervardijamo objekto tipą, gali reikėti atnaujinti susiejimus su šiuo objektu.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Pervardyti aplanką ar kūrimo bloką ataskaitų konstruktoriuje
Ataskaitų konstruktoriuje galite pervardyti aplankus, ataskaitų aprašus, eilutės apibrėžimus, stulpelių apibrėžimus ir ataskaitų medžio apibrėžimus.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Pervardyti aplanką ar kūrimo bloką ataskaitų konstruktoriuje

1. Ataskaitų konstruktoriuje naudokite naršymo sritį, kad rastumėte pervardytiną aplanką ar objektą.
2. Dešiniuoju pelės klavišu spustelėkite aplanką arba objektą ir tada spustelėkite **Pervardyti**. Naršymo srities laukas **Pavadinimas** tampa aktyvus.
3. Įveskite naują pavadinimą ir tada paspauskite **Įvesti**.
4. Jei kūrimo blokas yra eilutės aprašas, stulpelio aprašas arba ataskaitų medžio aprašas, turite atnaujinti kitus kūrimo blokus, susietus su šiuo kūrimo bloku. Dešiniuoju pelės klavišu spustelėkite kūrimo bloką, pervardytą atliekant 3 veiksmą, pasirinkite **Susiejimai** ir tada pasirinkite sąrašo elementą, kad jį atnaujintumėte.
5. Kartokite 4 veiksmą, kol visi susieti elementai bus atnaujinti.

## <a name="create-and-manage-report-groups"></a>Ataskaitų grupių kūrimas ir valdymas
Galite grupuoti ataskaitų aprašus, kad sukurtumėte kelias ataskaitas tuo pačiu metu. Kad galėtumėte kurti, modifikuoti, naikinti ir generuoti ataskaitų grupes, turite turėti dizainerio arba administratoriaus vaidmenį. Vartotojai, turintys generatorius vaidmenį, gali generuoti ataskaitų grupes ir taip pat modifikuoti ataskaitų grupių vartotojo ataskaitų aprašų nustatymą.

### <a name="create-a-report-group"></a>Ataskaitų grupės kūrimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.
2. Meniu Failas **spustelėkite** Nauja ataskaitos **grupės** &gt; **apibrėžtis, kad** peržiūros programos lange atidarytumėte naują ataskaitų grupę. Taip pat galite spustelėti **ataskaitos grupės mygtuką**  ![Ataskaitos grupė.](media/report-group.gif "Ataskaitų grupė") įrankių juostoje.
3. Spustelėkite skirtuką **Ataskaitų** grupė. Norėdami nepaisyti atskiros ataskaitos aprašų informacijos, kad būtų galima generuoti šią ataskaitą, **pažymėkite žymės langelį Perrašyti įmonę,** informaciją ir datos parametrus atskiruose ataskaitų aprašuose. Įmonės pavadinimo, išsamumo lygio, laikinojo parametro ir datos informacija įvedama automatiškai, bet jūs galite ją naujinti.
4. Norėdami generuoti kelias ataskaitas, kuriose parodytos ataskaitų valiutos, pažymėkite žymės **langelį Įtraukti visas ataskaitų** valiutas. Tada, peržiūrint ataskaitą, žiniatinklio peržiūros programoje spustelėjus mygtuką **Valiuta** bus rodomi keli rodiniai.
5. Lauke **Grupės ataskaitos** spustelėkite **Įtraukti** ir pasirinkite ataskaitas, kurias norite įtraukti į ataskaitų grupę. Norėdami dialogo lange **Įtraukti** pasirinkti kelias ataskaitas, pažymėkite ataskaitas laikydami nuspaudę klavišą CTRL. Pasirinkę ataskaitas, spustelėkite **Gerai**.
6. Spustelėkite **Failas** &gt; **Įrašyti**, kad įrašytumėte naują ataskaitų grupę.

### <a name="modify-a-report-group"></a>Ataskaitų grupės modifikavimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.
2. Dukart spustelėkite ataskaitų grupę, kurią norite modifikuoti.
3.  **Ataskaitų grupės skirtuke** atlikite norimus pakeitimus.
4. Meniu **Failas** spustelėkite **Įrašyti**, kad įrašytumėte modifikuotą ataskaitų grupę, taip pat galite spustelėti **Įrašyti** mygtuką ![Įrašyti.](media/save.gif "Įrašyti"). įrankių juostoje.

> [NOTE] Jei suplanavote ataskaitas, kad jos būtų generuojamos nustatytais intervalais, galite nepaisyti šių parametrų ir sugeneruoti ataskaitą nedelsiant.

### <a name="generate-a-report-group-report"></a>Ataskaitų grupės ataskaitos generavimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.
2. Atidarykite ataskaitų grupę, kurią norite generuoti.
3. Spustelėkite mygtuką **Generuoti ataskaitą** . ![...](media/generate-report.gif "Generuoti ataskaitą") ataskaitų generavimui.

### <a name="delete-a-report-group"></a>Ataskaitų grupės panaikinimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.
2. Dešiniuoju pelės klavišu spustelėkite ataskaitos grupę, kurią norite naikinti, ir tada pasirinkite **Naikinti**.
3. Kai pasirodo patvirtinimo pranešimas, spustelėkite **Taip**.

## <a name="report-group-tab-controls"></a>Ataskaitų grupės skirtuko valdikliai
Toliau pateikiamoje lentelėje aprašomi skirtuko Ataskaitos **grupė** valdikliai.

<table>
<thead>
<tr>
<th>Valdiklis</th>
<th>Aprašymas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Perrašyti įmonės, išsamios informacijos ir datos parametrus kiekvienos ataskaitos apraše</td>
<td>Pažymėkite šį žymės langelį, jei norite nepaisyti atskirų šios ataskaitų grupės ataskaitų aprašų, kad būtų galima tik šias ataskaitas generuoti.</td>
</tr>
<tr>
<td>Įmonės pavadinimas</td>
<td>Pasirinkite įmonę, kuri bus naudojama ataskaitoms generuoti.</td>
</tr>
<tr>
<td>Detalumo lygis</td>
<td>Nurodykite ataskaitų informacijos išsamumo lygį.
<ul>
<li><strong>Finansai</strong>− aukšto lygio suvestinė ataskaita. Negalima&#39; detalizuoti iki sąskaitų ir dimensijų, išskyrus tas sąskaitas ir dimensijas, kurios įtrauktos naudojant ataskaitų medį.</li>
<li><strong>Finansinė &amp; sąskaitos</strong> − ataskaita, kurioje yra aukšto lygio suvestinė ir išsami sąskaitos informacija.</li>
<li><strong>Finansinė, sąskaitos &amp; operacijų</strong> − ataskaita, kurioje yra aukšto lygio suvestinė ir išsami operacijų informacija.</li>
</ul></td>
</tr>
<tr>
<td>Laikinoji</td>
<td>Nurodykite ataskaitų veiklų tipus.
<ul>
<li><strong>Tik užregistruota veikla</strong> − įtraukti tik finansiniuose duomenyse užregistruotas operacijas ir balansus.</li>
<li><strong>Užregistruota ir neužregistruota veikla</strong> − įtraukti visas finansiniuose duomenyse įvestas ir užregistruotas operacijas bei balansus.</li>
<li><strong>Tik neužregistruota veikla</strong> − įtraukti tik finansiniuose duomenyse įvestas, bet dar neužregistruotas, operacijas.</li>
</ul></td>
</tr>
<tr>
<td>Apima visas ataskaitų valiutas</td>
<td>Čia išvardytos visos papildomos ataskaitų valiutos, sukonfigūruotos jūsų Microsoft Dynamics "365" finansų sistemoje. Pažymėkite šį žymės langelį, jei norite generuoti papildomas ataskaitas nurodytose valiutose. Norėdami šias ataskaitas peržiūrėti žiniatinklio peržiūros programoje, spustelėkite mygtuką <strong>Valiuta</strong> ir pasirinkite valiutą.</td>
</tr>
<tr>
<td>Ataskaitos aprašo datos informacija neįrašyta</td>
<td><ul>
<li>Pagrindinis laikotarpis</li>
<li>Pagrindiniai metai</li>
<li>Įtrauktas laikotarpis</li>
</ul>
Su ataskaitos aprašu įrašomi tik numatytieji pagrindinio laikotarpio parametrai.</td>
</tr>
<tr>
<td>Ataskaitos aprašo datos informacija įrašyta</td>
<td><ul>
<li>Ataskaitos data</li>
<li>Numatytasis pagrindinis laikotarpis</li>
</ul></td>
</tr>
<tr>
<td>Grupės ataskaitos</td>
<td>Įtraukite, pašalinkite ir pertvarkykite ataskaitų grupės ataskaitas.
<ul>
<li>Norėdami įtraukti ataskaitų aprašų į ataskaitų grupę, dukart spustelėkite ataskaitų grupę, kad ją atidarytumėte, tada spustelėkite <strong>Įtraukti</strong>. Pasirinkite į ataskaitų grupę norimas įtraukti ataskaitas, tada spustelėkite <strong>Gerai</strong>.</li>
<li>Norėdami pašalinti ataskaitą iš ataskaitų grupės, pasirinkite ją ir spustelėkite <strong>Pašalinti</strong>.</li>
<li>Norėdami modifikuoti, kokia tvarka ataskaitos bus generuojamos, sąraše pasirinkite ataskaitą ir tada spustelėkite <strong>Perkelti aukštyn</strong> arba <strong>Perkelti žemyn</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinės ataskaitos](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
