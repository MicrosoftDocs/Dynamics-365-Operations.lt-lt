---
title: Ataskaitos komponentų tvarkymas ataskaitų dizaino įrankyje
description: Sukūrus kūrimo blokus ir sugeneravus ataskaitas, patartina šiuos objektus sutvarkyti, kad vartotojai galėtų juos lengviau rasti. Šiame straipsnyje paaiškinama, kaip ataskaitų dizaino įrankyje tvarkyti esamas ataskaitas, kūrimo blokus ir objektus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 58525da35eb9e9376cb5793ad6c6fa45b9de42e6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685816"
---
# <a name="organize-report-components-in-report-designer"></a>Ataskaitos komponentų tvarkymas ataskaitų dizaino įrankyje

[!include [banner](../includes/banner.md)]

Sukūrus kūrimo blokus ir sugeneravus ataskaitas, patartina šiuos objektus sutvarkyti, kad vartotojai galėtų juos lengviau rasti. Šiame straipsnyje paaiškinama, kaip ataskaitų dizaino įrankyje tvarkyti esamas ataskaitas, kūrimo blokus ir objektus.

Galite pervardyti aplankus, ataskaitas, kūrimo blokus ir kitus objektus ataskaitų dizaino įrankyje, kad būtų lengviau sutvarkyti failus. Atsižvelgiant į pervardijamo objekto tipą, gali reikėti atnaujinti susiejimus su šiuo objektu.

## <a name="rename-a-folder-or-building-block-in-report-designer"></a>Aplanko arba kūrimo bloko pervardijimas ataskaitų konstruktoriuje
Ataskaitų dizaino įrankyje galite pervardyti aplankus, ataskaitų, eilučių, stulpelių ir ataskaitų medžių aprašus.

### <a name="rename-a-folder-or-building-block-in-report-designer"></a>Aplanko arba kūrimo bloko pervardijimas ataskaitų dizaino įrankyje

1. Norėdami rasti pervardytiną aplanką arba objektą naudokite ataskaitų dizaino įrankio naršymo sritį.
2. Dešiniuoju pelės klavišu spustelėkite aplanką arba objektą ir tada spustelėkite **Pervardyti**. Naršymo srities laukas **Pavadinimas** tampa aktyvus.
3. Įveskite naują pavadinimą ir tada paspauskite Įvesti.
4. Jei kūrimo blokas yra eilutės aprašas, stulpelio aprašas arba ataskaitų medžio aprašas, turite atnaujinti kitus kūrimo blokus, susietus su šiuo kūrimo bloku. Dešiniuoju pelės klavišu spustelėkite kūrimo bloką, pervardytą atliekant 3 veiksmą, pasirinkite **Susiejimai** ir tada pasirinkite sąrašo elementą, kad jį atnaujintumėte.
5. Kartokite 4 veiksmą, kol visi susieti elementai bus atnaujinti.

## <a name="create-and-manage-report-groups"></a>Ataskaitų grupių kūrimas ir valdymas
Galite grupuoti ataskaitų aprašus, kad sukurtumėte kelias ataskaitas tuo pačiu metu. Kad galėtumėte kurti, modifikuoti, naikinti ir generuoti ataskaitų grupes, turite turėti dizainerio arba administratoriaus vaidmenį. Vartotojai, turintys generatorius vaidmenį, gali generuoti ataskaitų grupes ir taip pat modifikuoti ataskaitų grupių vartotojo ataskaitų aprašų nustatymą.

### <a name="create-a-report-group"></a>Ataskaitų grupės kūrimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.
2. Meniu **Failas** spustelėkite **Naujas** &gt; **Ataskaitų grupės aprašas**, kad atidarytumėte naują ataskaitų grupę peržiūros programos lange. Taip pat įrankių juostoje galite spustelėti mygtuką **Ataskaitų grupė** ![Ataskaitų grupė](media/report-group.gif "Ataskaitų grupė").
3. Spustelėkite skirtuką **Ataskaitų grupė**. Norėdami perrašyti atskirų ataskaitų aprašų informaciją, kad galėtumėte generuoti šią ataskaitą, pažymėkite žymės langelį **Perrašyti atskirų ataskaitų aprašų įmonės, išsamios informacijos ir datos parametrus**. Įmonės pavadinimo, išsamumo lygio, laikinojo parametro ir datos informacija įvedama automatiškai, bet jūs galite ją naujinti.
4. Pažymėkite žymės langelį **Įtraukti visas ataskaitų valiutas**, jei norite sugeneruoti kelias ataskaitas, kuriose rodomos tos ataskaitų valiutos. Tada, peržiūrint ataskaitą, žiniatinklio peržiūros programoje spustelėjus mygtuką **Valiuta** bus rodomi keli rodiniai.
5. Lauke **Grupės ataskaitos** spustelėkite **Įtraukti** ir pasirinkite ataskaitas, kurias norite įtraukti į ataskaitų grupę. Norėdami dialogo lange **Įtraukti** pasirinkti kelias ataskaitas, pažymėkite ataskaitas laikydami nuspaudę klavišą CTRL. Pasirinkę ataskaitas, spustelėkite **Gerai**.
6. Spustelėkite **Failas** &gt; **Įrašyti**, kad įrašytumėte naują ataskaitų grupę.

### <a name="modify-a-report-group"></a>Ataskaitų grupės modifikavimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.
2. Dukart spustelėkite ataskaitų grupę, kurią norite modifikuoti.
3. Skirtuke **Ataskaitų grupė** atlikite norimus keitimus.
4. Meniu **Failas** spustelėkite **Įrašyti**, kad įrašytumėte modifikuotą ataskaitų grupę. Taip pat įrankių juostoje galite spustelėti mygtuką **Įrašyti** ![Įrašyti](media/save.gif "Įrašyti").

> [PASTABA] Jei suplanavote ataskaitas generuoti tam tikrais intervalais, galite nepaisyti šių parametrų ir generuoti ataskaitą iš karto.

### <a name="generate-a-report-group-report"></a>Ataskaitų grupės ataskaitos generavimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.
2. Atidarykite ataskaitų grupę, kurią norite generuoti.
3. Norėdami generuoti ataskaitas, spustelėkite mygtuką **Generuoti ataskaitą** ![Generuoti ataskaitą](media/generate-report.gif "Generuoti ataskaitą").

### <a name="delete-a-report-group"></a>Ataskaitų grupės panaikinimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite **Ataskaitų grupės**.
2. Dešiniuoju pelės klavišu spustelėkite ataskaitos grupę, kurią norite naikinti, ir tada pasirinkite **Naikinti**.
3. Kai pasirodo patvirtinimo pranešimas, spustelėkite **Taip**.

## <a name="report-group-tab-controls"></a>Ataskaitų grupės skirtuko valdikliai
Toliau pateikiamoje lentelėje aprašomi skirtuko **Ataskaitų grupė** valdikliai.

<table>
<thead>
<tr>
<th>Valdiklis</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr>
<td>Nepaisyti įmonės, išsamios informacijos ir datos parametrų iš atskirų ataskaitų aprašų</td>
<td>Pažymėkite šį žymės langelį norėdami nepaisyti atskirų šios ataskaitų grupės ataskaitų aprašų generuojant tik šias ataskaitas.</td>
</tr>
<tr>
<td>Įmonės pavadinimas</td>
<td>Pasirinkite įmonę, kuri bus naudojama ataskaitoms generuoti.</td>
</tr>
<tr>
<td>Detalumo lygis</td>
<td>Nurodykite ataskaitų informacijos išsamumo lygį.
<ul>
<li><strong>Finansai</strong>− aukšto lygio suvestinė ataskaita. Negalima detalizuoti iki sąskaitų ir dimensijų, išskyrus tas sąskaitas ir dimensijas, kurios įtrauktos naudojant ataskaitų medį.</li>
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
<td>Jei jūsų „Microsoft Dynamics“ ERP sistemoje yra papildomų sukonfigūruotų ataskaitų valiutų, jos pateikiamos čia. Pažymėkite šį žymės langelį, jei norite, kad papildomos ataskaitos būtų generuojamos nurodyta valiuta. Norėdami šias ataskaitas peržiūrėti žiniatinklio peržiūros programoje, spustelėkite mygtuką <strong>Valiuta</strong> ir pasirinkite valiutą.</td>
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
