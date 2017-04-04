---
title: "Konfigūruoti programą laukų pavadinimai sandėliavimas App"
description: "Šioje temoje aprašoma, kaip nustatyti ir konfigūruoti sandėlio programos laukų pavadinimai ir prioritetų Dynamics 365 operacijoms."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigūruoti programą laukų pavadinimai sandėliavimas App

Šioje temoje aprašoma, kaip nustatyti ir konfigūruoti sandėlio programos laukų pavadinimai ir prioritetų Dynamics 365 operacijoms. 

**Pastaba:** Ši tema skirta sandėlio valdymo funkcijos. Tai netaikoma atsargų valdymo funkcijos. Dinamika 365 operacijų - sandėliavimo yra programa, kuri galite naudoti sandėlio užduotims atlikti. Jūs galite nustatyti ir konfigūruoti laukų pavadinimai, kuriuos naudoja programėlės, taip pat konfigūruoti laukų pavadinimai turėtų būti priskirtos prioritetinės. Šioje temoje aiškinama, kaip nustatyti ir konfigūruoti šių sandėlio programos laukų pavadinimai ir prioritetus, ir kaip jie yra naudojami Dynamics 365 operacijų - sandėliavimo. Išsamią informaciją apie tai, kaip sukonfigūruoti ryšį su Dynamics 365 operacijų - sandėliavimo, ieškokite pamoka [įdiegti ir konfigūruoti Dynamics 365 operacijų - sandėliavimo](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Konfigūruoti sandėlio programos laukų pavadinimus
===================================

Kai naudojate Dynamics 365 operacijų - sandėliavimo mobiliajame įrenginyje, galite konfigūruoti kaip metaduomenys turi būti rodomas ant jūsų prietaiso, **sandėlio programos laukų pavadinimai** puslapis. Nauja įmonė Dynamics 365 operacijoms, pasirinkite **sukurti numatytąjį nustatymą** generuoti visų laukų pavadinimus, kad bus naudojamos sandėlio mobiliųjų įrenginių darbo eigas, ir tada priskirti norimą įvesties režimą ir įvesties tipo jiems. Po to, kai buvo sukurtas visų laukų pavadinimai, galite pasirinkti šias įvesties parinktis.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parinktis</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pageidaujamas įvesties režimas</td>
<td>Ši opcija nusako ar skenavimo laukas ar Rankinės įvesties įvesties lauke turi būti rodoma pasirinkto lauko pavadinimą. Tai naudinga atskirti laukai priklauso jei brūkšniniai kodai naudojami lauko. <strong>Pastaba:</strong> laukų pavadinimai su pageidaujamą įvesties režimas nustatytas <strong>nuskaitymo</strong>, galite įvesti informaciją rankiniu būdu jei brūkšniniame kode yra neįskaitomas arba sugadintas.</td>
</tr>
<tr class="even">
<td>Įvedimo tipas</td>
<td>Ši opcija nusako, kokia įvesties tipas turėtų būti naudojami pasirinkto lauko pavadinimą. Galimos keturios pasirinktys:
<ul>
<li><strong>Atrankos</strong> - parinkčių sąrašas. Laukų pavadinimai su šia galimybe yra neredaguojami.</li>
<li><strong>Data</strong> - laukų pavadinimai, nurodyti data bus rodomi datos formatą su etikete. Tai padeda matyti įvesti datos formato sandėlio darbuotojams. Laukų pavadinimai su šia galimybe yra neredaguojami.</li>
<li><strong>Alfa</strong> - pasirinkus prietaiso klaviatūra bus naudojamas rankiniu būdu įvesti informaciją programėlėje. Klaviatūros patirtimi gali kisti, priklausomai nuo to, kuris įrenginys naudojamas.</li>
<li><strong>Skaitmeniniai</strong> -, laukų pavadinimų, naudoti skaitinius duomenis tik, galite pasirinkti šią parinktį Rodyti pasirinktinį skaičių klaviatūroje vietoj įrenginį klaviatūros įvesties lauke.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigūruoti sandėlio programa lauke prioritetas
======================================

Dėl to **sandėlio programa lauke prioritetas** puslapyje, galite įdėti laukų pavadinimus į skirtingų prioritetinių grupių. Tai leidžia spręsti, kokia informacija turėtų būti rodomas puslapyje pagrindinis uždavinys, kai sandėlio darbuotojai atlieka užduotis naudodami programėlę. Jei spustelėsite **sukurti numatytąjį nustatymą**, bus sukurtas numatytasis rinkinys prioritetinių grupių. Yra galimybė sukurti prioritetinių grupių, tiek, kiek reikia, bet tik trys prioritetinės grupės bus rodomas užduočių puslapyje. Dynamics 365 operacijoms siunčiant metaduomenų į programėlę, ji bus priskirti kiekvieną lauką Santykinis prioriteto priklausomai nuo savo prioritetų grupės, ir programėlė rodys pirmą trijų prioritetinių grupių, esančių užduočių puslapio metaduomenys. Likusi didžios metaduomenų pasirodys antrinės informacijos puslapyje. Šioje lentelėje yra penkių prioritetinių grupių pavyzdys.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritetinė grupė</th>
<th>Priskirti laukai</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Svarba – 10</td>
<td><ul>
<li>Produktas</li>
<li>Kiekis</li>
<li>Matavimo vienetas</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioritetas 20</td>
<td><ul>
<li>Klasterio pareigos</li>
<li>Klasteris</li>
</ul></td>
</tr>
<tr class="odd">
<td> 30 prioritetinių</td>
<td><ul>
<li>Prekės aprašas</li>
</ul></td>
</tr>
<tr class="even">
<td> Prioritetas 40</td>
<td><ul>
<li>Konfigūravimas</li>
<li>Spalva</li>
<li>Dydis</li>
<li>Stilius</li>
</ul></td>
</tr>
<tr class="odd">
<td> Prioritetas 50</td>
<td><ul>
<li>Buvimo vieta</li>
<li>Numerio lentelė</li>
</ul></td>
</tr>
</tbody>
</table>

Pavyzdžiui, kai sandėlio darbuotojas atlieka užduotį mobiliajame įrenginyje, jei metaduomenimis, kurie bus rodomi programėlėje susideda iš šių laukų:

-   Produktas
-   Kiekis
-   Matavimo vienetas
-   Prekės aprašas
-   Dydis ir vieta

Remiantis aukščiau lentelėje sandėlio app lauko prioritetas, šios 3 eilutės informacija bus rodomas užduočių puslapyje:

-   1 eilutėje: Prekė, kiekis, matavimo vienetas
-   2 eilėje: Prekės aprašymas
-   Eilutės 3: dydis

Likusių metaduomenis, pvz., vieta, nebus rodomas puslapyje užduotis, tačiau bus rodomi išsamios informacijos puslapį. Sužinoti daugiau ir pamatyti, kaip vartotojo sąsaja, kreiptis į blog post [apie Dynamics 365 operacijų - sandėliavimo](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Įdiegti ir konfigūruoti Microsoft Dynamics 365 operacijoms – sandėliavimo](install-configure-warehousing-app.md)


