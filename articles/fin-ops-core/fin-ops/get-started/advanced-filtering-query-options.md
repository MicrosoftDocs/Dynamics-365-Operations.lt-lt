---
title: Išplėstinio filtravimo ir užklausų sintaksė
description: Šioje temoje aprašomos filtravimo ir užklausos parinktys, kurios pasiekiamos naudojant dialogo langą Išplėstinis filtravimas / rūšiavimas arba filtro srityje esantį atitikimo operatorių, arba tinklelio stulpelių antraščių filtrus.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 650f1c209b1797973634c788645a4659bff28f13
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798676"
---
# <a name="advanced-filtering-and-query-syntax"></a>Išplėstinio filtravimo ir užklausų sintaksė

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos filtravimo ir užklausos parinktys, kurios pasiekiamos naudojant dialogo langą Išplėstinis filtravimas / rūšiavimas arba filtro srityje esantį **atitikimo** operatorių, arba tinklelio stulpelių antraščių filtrus.

## <a name="advanced-query-syntax"></a>Išplėstinės užklausos sintaksė

<table>
<thead>
<tr>
<th>Sintaksė</th>
<th>Simbolio aprašymas</th>
<th>aprašymas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>vertė</em></td>
<td>Lygi įvestai vertei</td>
<td>Įveskite vertę, kurią norite rasti.</td>
<td>Įvedus <strong>Smith</strong> randama &quot;Smith&quot;.</td>
</tr>
<tr>
<td>!<em>vertė</em> (šauktuko ženklas)</td>
<td>Nelygi įvestai vertei</td>
<td>Prieš vertę, kurią norite pašalinti, įveskite šauktuko ženklą.</td>
<td>Įvedus <strong>!Smith</strong> randamos visos vertės, išskyrus &quot;Smith&quot;.</td>
</tr>
<tr>
<td><em>„Nuo“ vertė</em>..<em>„Iki“ vertė</em> (dvigubas taškas)</td>
<td>Vertė, esanti tarp dviejų įvestų verčių, atskirtų dvigubais taškais.</td>
<td>Įveskite vertę Nuo, tada du taškus, tada vertę Iki.</td>
<td>Įvedus <strong>1..10</strong> randamos visos vertės nuo 1 iki 10. Tačiau eilutės lauke <strong>A..C</strong> atsiranda visos vertės, prasidedančios &quot;A&quot; ir &quot;B&quot;, ir vertės, tiksliai lygios &quot;C&quot;. Pvz., pagal šią užklausą nebus rasta &quot;Ca&quot;. Norėdami surasti visas vertes įskaitytinai nuo &quot;A<em>&quot; iki &quot;C</em>&quot;, įrašykite <strong>A..D</strong>.</td>
</tr>
<tr>
<td>..<em>vertė</em> (dvigubas taškas)</td>
<td>Mažesnė nei įvesta vertė arba lygi įvestai vertei</td>
<td>Įveskite du taškus, tada vertę.</td>
<td>Įvedus <strong>..1000</strong> randamas bet kuris skaičius, mažesnis nei 1000 arba lygus 1000, pvz., &quot;100&quot;, &quot;999,95&quot; ir &quot;1000&quot;.</td>
</tr>
<tr>
<td><em>vertė</em>.. dvigubas laikotarpis</td>
<td>Didesnė nei įvesta vertė arba lygi įvestai vertei</td>
<td>Įveskite vertę, tada du taškus.</td>
<td><strong>1000..</strong> randamas bet kuris skaičius, didesnis nei 1000 arba lygus 1000, pvz., &quot;1000&quot;, &quot;1000,01&quot; ir &quot;1 000 000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>vertė</em> („daugiau nei“ ženklas)</td>
<td>Didesnė už įvestą vertę</td>
<td>Įveskite „daugiau nei“ ženklą (<strong>&gt;</strong>), tada – vertę.</td>
<td>Įvedus <strong>&gt; 1000</strong> randamas bet kuris skaičius, kuris yra didesnis nei 1000, pvz., &quot;1000,01&quot;, &quot;20 000&quot;, and &quot;1 000 000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>vertė</em> („mažiau nei“ ženklas)</td>
<td>Mažesnė už įvestą vertę</td>
<td>Įveskite „mažiau nei“ ženklą (<strong>&lt;</strong>), tada – vertę.</td>
<td>Įvedus <strong>&lt; 1000</strong> randamas bet kuris skaičius, kuris yra mažesnis nei 1000, pvz., &quot;999,99&quot;, &quot;1&quot; ir &quot;-200&quot;.</td>
</tr>
<tr>
<td><em>vertė</em>* (žvaigždutė)</td>
<td>Prasideda įvesta verte</td>
<td>Įveskite pradžios vertę, tada – žvaigždutę (<strong>*</strong>).</td>
<td>Įvedus <strong>S*</strong> randama bet kuri eilutė, prasidedanti &quot;S&quot;, pvz.,  &quot;Stockholm&quot;, &quot;Sydney&quot; ir &quot;San Francisco&quot;.</td>
</tr>
<tr>
<td>*<em>vertė</em> (žvaigždutė)</td>
<td>Baigiasi įvesta verte</td>
<td>Įveskite žvaigždutę ir pabaigos vertę.</td>
<td>Įvedus <strong>*east</strong> randamos visos eilutės, besibaigiančios &quot;east&quot;, pvz., &quot;Northeast&quot; ir &quot;Southeast&quot;.</td>
</tr>
<tr>
<td>*<em>vertė</em>* (žvaigždutė)</td>
<td>Įeina įvesta vertė</td>
<td>Įveskite žvaigždutę, tada vertę ir kitą žvaigždutę.</td>
<td>Įvedus <strong>*th*</strong> randamos visos eilutės, kuriose yra &quot;th&quot;, pvz. &quot;Northeast&quot; ir &quot;Southeast&quot;.</td>
</tr>
<tr>
<td>? klaustuko ženklas</td>
<td>Turi vieną ar daugiau nežinomų simbolių</td>
<td>Įveskite klaustuko ženklą nežinomo vertės simbolio vietoje.</td>
<td>Įvedus <strong>Sm?th</strong> randama &quot;Smith&quot; ir &quot;Smyth&quot;.</td>
</tr>
<tr>
<td><em>vertė</em>,<em>vertė</em> (kablelis)</td>
<td>Ieškoma verčių, atskirtų kableliais</td>
<td>Įveskite visus kriterijus ir atskirkite juos kableliais.</td>
<td><strong>Įvedus A, D, F, G</strong> surandama būtent &quot;A&quot;, &quot;D&quot;, &quot;F&quot; ir &quot;G&quot;. <strong>Įvedus 10, 20, 30, 100</strong> surandama būtent &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr>
<td>"" (dvi dvigubos kabutės)</td>
<td>Tuščios reikšmės gretinimas</td>
<td>Jei norite tame lauke filtruodami rasti tuščias reikšmes , iš eilės įveskite dvi dvigubas kabutes.</td>
<td>Naudojant dvi iš eilės įvestas dvigubas kabutes (<strong>""</strong>), randamos eilutės, kuriose dabartinio stulpelio reikšmių nėra.</td>
</tr>
<tr>
<td>(<span class="code">„Finance and Operations” užklausa</span>) („Finance and Operations” užklausa skliausteliuose)</td>
<td>Ieškoma užklausos, atitinkančios nustatytą</td>
<td>Įveskite užklausą kaip SQL sakinį tarp skliaustelių naudodami „Finance and Operations” užklausos kalbą.</td>
  <td><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong><br><br> 
       tai pavyzdys sintaksės, naudojamos šakninio duomenų šalitinio lauko ir kito duomenų šaltinio (skirto puslapiui Visi klientai) lauko filtro sąlygai</td>
</tr>
<tr>
<td>A</td>
<td>Šiandienos data</td>
<td>Įveskite <strong>T</strong>.</td>
<td><strong>T</strong> atitinka šiandienos datą.</td>
</tr>
<tr>
<td>(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> metodas tarp skliaustelių)</td>
<td>Ieškoma vertė arba diapazonas verčių, kurias nurodo <strong>SysQueryRangeUtil</strong> metodo parametras</td>
<td>Įveskite <strong>SysQueryRangeUtil</strong> metodą su parametrais, nurodančiais vertę arba verčių diapazoną.</td>
<td>
<ol>
<li>Spustelėkite <strong>Gautinos sumos</strong> &gt; <strong>Sąskaitos faktūros</strong> &gt; <strong>Atviros kliento SF</strong>.</li>
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
<thead>
<tr>
<th>Metodas</th>
<th>Prekės/Paslaugos pavadinimas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr>
<td>Diena (_relativeDays = 0)</td>
<td>Randama data, susijusi su seanso data. Teigiamos vertės reiškia būsimas datas, o neigiamos vertės reiškia praeities datas.</td>
<td>
<ul>
<li><strong>Rytojaus diena</strong> – įveskite <strong>(Day(1))</strong>.</li>
<li><strong>Šiandiena</strong> – įveskite <strong>(Day(0))</strong>.</li>
<li><strong>Vakar diena</strong> – įveskite <strong>(Day(-1))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom = 0, _relativeDaysTo = 0)</td>
<td>Randamos datos, susijusios su seanso data. Teigiamos vertės reiškia būsimas datas, o neigiamos vertės reiškia praeities datas.</td>
<td>
<ul>
<li><strong>Pastarosios 30 dienų</strong> – įveskite <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Ankstesnės 30 dienų ir ateinančios 30 dienų</strong> – įveskite <strong>(DayRange(-30,30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays = 0) GreaterThanUtcDate (_relativeDays = 0)</td>
<td>Randamos visos datos, kurios yra vėlesnės nei nurodytos santykinės datos.</td>
<td>
<ul>
<li><strong>Daugiau nei 30 dienų nuo šiol</strong> – įveskite <strong>(GreaterThanDate(30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Randami visi datos / laiko įrašai, kurie yra vėlesni už dabartinį laiką.</td>
<td>
<ul>
<li><strong>Visos būsimos datos / laikai</strong> – įveskite <strong>(GreaterThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Randamos visos datos, kurios yra ankstesnės nei nurodyta santykinė data.</td>
<td>
<ul>
<li><strong>Mažiau nei septynios dienas nuo šiol</strong> – įveskite <strong>(LessThanDate(7))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Randami visi datos / laiko įrašai, kurie yra ankstesni už dabartinį laiką.</td>
<td>
<ul>
<li><strong>Visos praeities datos / laikai</strong> – įveskite <strong>(LessThanUtcNow())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom = 0, _relativeTo = 0)</td>
<td>Randamos datos pagal mėnesius, susijusius su dabartiniu mėnesiu.</td>
<td>
<ul>
<li><strong>Du praėję mėnesiai</strong> – įveskite <strong>(MonthRange(-2,0))</strong>.</li>
<li><strong>Ateinantys trys mėnesiai</strong> – įveskite <strong>(MonthRange(0,3))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Randamos datos pagal metus, susijusius su dabartiniais metais.</td>
<td>
<ul>
<li><strong>Ateinantys metai</strong> – įveskite <strong>(YearRange(0, 1))</strong>.</li>
<li><strong>Ankstesni metai</strong> – įveskite <strong>(YearRange(-1,0))</strong>.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]