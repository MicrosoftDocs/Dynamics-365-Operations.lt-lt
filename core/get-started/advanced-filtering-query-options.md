---
title: "Pažangi filtravimo ir užklausos sintaksė"
description: "Šiame straipsnyje aprašomos filtravimo ir užklausos parinktys, kurios galimos naudojant atitikmenų operatorių Išplėstinio filtro / rūšiavimo dialogo lange."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5ee7a04572e350a7c08d0418bade6d332aa920c6
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-filtering-and-query-syntax"></a>Pažangi filtravimo ir užklausos sintaksė

Šiame straipsnyje aprašomos filtravimo ir užklausos parinktys, kurios galimos naudojant atitikmenų operatorių Išplėstinio filtro / rūšiavimo dialogo lange.

<a name="advanced-query-syntax"></a>Išplėstinės užklausos sintaksę
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Sintaksė</th>
<th>Simbolio aprašymas</th>
<th>aprašymas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>vertė</em></td>
<td>Lygi įvestai vertei</td>
<td>Įveskite vertę, kurią norite rasti.</td>
<td><strong>Smith</strong> mano &quot;Smith&quot;.</td>
</tr>
<tr class="even">
<td>! <em>vertė</em> (šauktukas)</td>
<td>Nelygi įvestai vertei</td>
<td>Prieš vertę, kurią norite pašalinti, įveskite šauktuko ženklą.</td>
<td><strong>! Smith</strong> randa visas reikšmes, išskyrus &quot;Smith&quot;.</td>
</tr>
<tr class="odd">
<td><em>„Nuo“ vertė</em>..<em>„Iki“ vertė</em> (dvigubas taškas)</td>
<td>Vertė, esanti tarp dviejų įvestų verčių, atskirtų dvigubais taškais.</td>
<td>Įveskite vertę Nuo, tada du taškus, tada vertę Iki.</td>
<td><strong>1..10</strong> nustato visas reikšmes nuo 1 iki 10. Vis dėlto į eilutę laukas, <strong>a. C</strong> randa visas reikšmes, kurie prasideda &quot;A&quot; ir &quot;B&quot;, ir vertes, kurios yra tiksliai lygi &quot;C&quot;. Pavyzdžiui, ši užklausa nerasite &quot;Ca&quot;. Rasti visas reikšmes nuo &quot;A*&quot; per &quot;C*&quot;, tipo <strong>A.. D</strong>.</td>
</tr>
<tr class="even">
<td>..<em>vertė</em> (dvigubas taškas)</td>
<td>Mažesnė nei įvesta vertė arba lygi įvestai vertei</td>
<td>Įveskite du taškus, tada vertę.</td>
<td><strong>.. 1000</strong> randa bet kokį skaičių, kuris yra mažesnis ar lygus 1000, pvz., &quot;100&quot;, &quot;999.95&quot;, ir &quot;1000&quot;.</td>
</tr>
<tr class="odd">
<td><em>vertė</em>.. dvigubas laikotarpis</td>
<td>Didesnė nei įvesta vertė arba lygi įvestai vertei</td>
<td>Įveskite vertę, tada du taškus.</td>
<td><strong>1000..</strong> Randa bet kokį skaičių, kuris yra didesnis arba lygus 1000, pvz., &quot;1000&quot;, &quot;1,000.01&quot;, ir &quot;1 000 000&quot;.</td>
</tr>
<tr class="even">
<td>&gt;<em>vertė</em> (didesnis kaip ženklas)</td>
<td>Didesnė už įvestą vertę</td>
<td>Tipo didesnis kaip ženklas (<strong>&gt;</strong>) ir tada vertę.</td>
<td><strong>&gt;1000</strong> randa bet kokį skaičių, kuris yra didesnis nei 1000, pvz., &quot;1000.01&quot;, &quot;20 000&quot;, ir &quot;1 000 000&quot;.</td>
</tr>
<tr class="odd">
<td>&lt;<em>vertė</em> (mažiau nei ženklas)</td>
<td>Mažesnė už įvestą vertę</td>
<td>Įveskite mažiau nei ženklas (<strong>&lt;</strong>) ir tada vertę.</td>
<td><strong>&lt;1000</strong> randa bet kokį skaičių, kuris yra mažesnis nei 1000, pvz., &quot;999,99&quot;, &quot;1&quot;, ir &quot;-200&quot;.</td>
</tr>
<tr class="even">
<td><em>vertė</em>* (žvaigždutė)</td>
<td>Prasideda įvesta verte</td>
<td>Įveskite pradžios vertę ir žvaigždutę (<strong>*</strong>).</td>
<td><strong>S *</strong> suranda bet kurią eilutę, prasideda &quot;S&quot;, pvz., &quot;Stokholmo&quot;, &quot;Sidnėjaus&quot;, ir &quot;San Francisco&quot;.</td>
</tr>
<tr class="odd">
<td>*<em>value</em> (asterisk)</td>
<td>Baigiasi įvesta verte</td>
<td>Įveskite žvaigždutę ir pabaigos vertę.</td>
<td><strong>* Rytų</strong> suranda bet kurią eilutę, baigiasi &quot;Rytų&quot;, pvz., &quot;Šiaurės&quot; ir &quot;Pietryčių&quot;.</td>
</tr>
<tr class="even">
<td>*<em>vertė</em>* (žvaigždutė)</td>
<td>Įeina įvesta vertė</td>
<td>Įveskite žvaigždutę, tada vertę ir kitą žvaigždutę.</td>
<td><strong>*TH*</strong> suranda bet kurią eilutę, yra &quot;th&quot;, pvz., &quot;Šiaurės&quot; ir &quot;Pietryčių&quot;.</td>
</tr>
<tr class="odd">
<td>? klaustuko ženklas</td>
<td>Turi vieną ar daugiau nežinomų simbolių</td>
<td>Įveskite klaustuko ženklą nežinomo vertės simbolio vietoje.</td>
<td><strong>SM? th</strong> mano &quot;Smith&quot; ir &quot;Smyth&quot;.</td>
</tr>
<tr class="even">
<td><em>vertė</em>,<em>vertė</em> (kablelis)</td>
<td>Ieškoma verčių, atskirtų kableliais</td>
<td>Įveskite visus kriterijus ir atskirkite juos kableliais.</td>
<td><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;. <strong>10, 20, 30, 100</strong> nustato tiksliai &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr class="odd">
<td>(<span class="code">SQL sakinys</span>) (SQL sakinys tarp skliaustelių)</td>
<td>Ieškoma užklausos, atitinkančios nustatytą</td>
<td>Įveskite užklausą kaip SQL sakinį tarp skliaustelių.</td>
<td><strong><span class="code">(duomenų šaltinis. Lauko pavadinimas! = &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>A</td>
<td>Šiandienos data</td>
<td>Įveskite <strong>T</strong>.</td>
<td><strong>T</strong> atitinka šiandienos datą.</td>
</tr>
<tr class="odd">
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metodas tarp skliaustelių)</td>
<td>Ieškoma vertė arba diapazonas verčių, kurias nurodo <strong>SysQueryRangeUtil</strong> metodo parametras</td>
<td>Įveskite <strong>SysQueryRangeUtil</strong> metodą su parametrais, nurodančiais vertę arba verčių diapazoną.</td>
<td><ol>
<li>Spustelėkite <strong>gautinos sąskaitos</strong>&gt;<strong>sąskaitas faktūras</strong>&gt;<strong>atidaryti kliento SF</strong>.</li>
<li>Paspauskite Ctrl + Shift + F3, kad atidarytumėte puslapį <strong>Užklausa</strong>.</li>
<li>Skirtuke <strong>Diapazonas</strong> spustelėkite <strong>Pridėti</strong>.</li>
<li>Lauke <strong>Lentelė</strong> pasirinkite <strong>Atviros kliento operacijos</strong>.</li>
<li>Lauke <strong>Laukas</strong> pasirinkite <strong>Terminas</strong>.</li>
<li>Lauke <strong>Kriterijai</strong> įveskite <strong>(yearRange(-2,0))</strong>.</li>
<li>Spustelėkite <strong>GERAI</strong>. Sąrašo puslapis atnaujinamas ir pateikiamos įvestus kriterijus atitinkančios SF. Šiame pavyzdyje sąrašo puslapyje rodomos SF, kurias reikėjo apmokėti ankstesniais dvejais metais.</li>
</ol>
Jei reikia papildomos informacijos apie <strong>SysQueryRangeUtil</strong> datos metodus, žr. lentelę kitame skyriuje, kuriame pateikta ir keletas pavyzdžių.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Išplėstinės datos užklausos, kurios naudoja SysQueryRangeUtil metodus
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metodas</th>
<th>Prekės/Paslaugos pavadinimas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Diena (_relativeDays = 0)</td>
<td>Randama data, susijusi su seanso data. Teigiamos vertės reiškia būsimas datas, o neigiamos vertės reiškia praeities datas.</td>
<td><ul>
<li><strong>Rytojaus diena</strong> – įveskite <strong>(Day(1))</strong>.</li>
<li><strong>Šiandiena</strong> – įveskite <strong>(Day(0))</strong>.</li>
<li><strong>Vakar diena</strong> – įveskite <strong>(Day(-1))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom = 0, _relativeDaysTo = 0)</td>
<td>Randamos datos, susijusios su seanso data. Teigiamos vertės reiškia būsimas datas, o neigiamos vertės reiškia praeities datas.</td>
<td><ul>
<li><strong>Pastarosios 30 dienų</strong> – įveskite <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Ankstesnės 30 dienų ir ateinančios 30 dienų</strong> – įveskite <strong>(DayRange(-30,30))</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</td>
<td>Randamos visos datos, kurios yra vėlesnės nei nurodytos santykinės datos.</td>
<td><ul>
<li><strong>Daugiau nei 30 dienų nuo šiol</strong> – įveskite <strong>(GreaterThanDate(30))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>Randami visi datos / laiko įrašai, kurie yra vėlesni už dabartinį laiką.</td>
<td><ul>
<li><strong>Visos būsimos datos / laikai</strong> – įveskite <strong>(GreaterThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Randamos visos datos, kurios yra ankstesnės nei nurodyta santykinė data.</td>
<td><ul>
<li><strong>Mažiau nei septynios dienas nuo šiol</strong> – įveskite <strong>(LessThanDate(7))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>Randami visi datos / laiko įrašai, kurie yra ankstesni už dabartinį laiką.</td>
<td><ul>
<li><strong>Visos praeities datos / laikai</strong> – įveskite <strong>(LessThanUtcNow())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom = 0, _relativeTo = 0)</td>
<td>Randamos datos pagal mėnesius, susijusius su dabartiniu mėnesiu.</td>
<td><ul>
<li><strong>Du praėję mėnesiai</strong> – įveskite <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Ateinantys trys mėnesiai</strong> – įveskite <strong>(MonthRange(0,3))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Randamos datos pagal metus, susijusius su dabartiniais metais.</td>
<td><ul>
<li><strong>Ateinantys metai</strong> – įveskite <strong>(YearRange(0, 1))</strong>.</li>
<li><strong>Ankstesni metai</strong> – įveskite <strong>(YearRange(-1,0))</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>




