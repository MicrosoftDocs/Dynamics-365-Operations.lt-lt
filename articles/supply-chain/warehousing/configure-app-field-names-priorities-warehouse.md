---
title: Programos „Warehousing“ laukų pavadinimų konfigūravimas
description: Šioje temoje aprašoma, kaip nurodyti ir konfigūruoti sandėlio programos laukų pavadinimus ir prioritetus programoje „Dynamics 365 Supply Chain Management“.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a3251368e92eb2e24eb9e64bb615027d038ff660
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251090"
---
# <a name="configure-app-field-names-in-warehousing-app"></a>Programos „Warehousing“ laukų pavadinimų konfigūravimas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip nurodyti ir konfigūruoti sandėlio programos laukų pavadinimus ir prioritetus programoje „Dynamics 365 Supply Chain Management“. 

**Pastaba.** Ši tema taikoma sandėlio valdymo funkcijoms. Ji netaikoma atsargų valdymo funkcijoms. „Warehousing” yra programa, kurią galite naudoti sandėlio užduotims atlikti. Galite nurodyti ir konfigūruoti programoje naudojamų laukų pavadinimus, taip pat galite konfigūruoti prioritetą, kuriam laukų pavadinimai turėtų būti priskirti. Šioje temoje paaiškinama, kaip nurodyti ir konfigūruoti šiuos sandėlio programos laukų pavadinimus bei prioritetus ir kaip jie naudojami „Warehousing“. Išsamios informacijos apie tai, kaip konfigūruoti ryšį su „Warehousing“ žr. mokymo programoje [„Warehousing“ diegimas ir konfigūravimas](install-configure-warehousing-app.md).

## <a name="configure-warehouse-app-field-names"></a>Sandėlio programos laukų pavadinimų konfigūravimas

Naudodami „Warehousing“ savo mobiliajame įrenginyje galite konfigūruoti, kaip metaduomenys turėtų būti rodomi puslapyje **Sandėlio programos laukų pavadinimai**. Naujoje įmonėje pasirinkite **Kurti numatytąją sąranką**, kad sugeneruotumėte visų laukų pavadinimus, kurie bus naudojami sandėlio mobiliųjų įrenginių darbo eigose, ir tada jiems priskirkite pageidaujamą įvesties režimą ir įvesties tipą. Sugeneravę visų laukų pavadinimus, galite pasirinkti toliau nurodytas įvesties parinktis.

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
<td>Ši parinktis nurodo, ar pasirinktam lauko pavadinimui turi būti priskirtas ir rodomas nuskaitymo laukas, ar neautomatinės įvesties laukas. Tai naudinga norint laukus atskirti pagal tai, ar juose naudojami brūkšniniai kodai. <strong>Pastaba.</strong> Kai pageidaujamas laukų pavadinimų įvesties režimas nustatytas į parinktį <strong>Nuskaitymas</strong>, galite įvesti informaciją neautomatiškai, jei brūkšninis kodas yra neįskaitomas arba pažeistas.</td>
</tr>
<tr class="even">
<td>Įvedimo tipas</td>
<td>Ši parinktis nurodo, koks įvesties tipas turėtų būti priskirtas pasirinktam lauko pavadinimui. Galima pasirinkti iš keturių toliau pateiktų parinkčių.
<ul>
<li><strong>Pasirinkimas</strong> - pateiktas parinkčių, kurias galima pasirinkti, sąrašas. Nustačius šią parinktį laukų pavadinimų redaguoti negalima.</li>
<li><strong>Data</strong> - laukų pavadinimuose, kurie nurodyti kaip data, bus rodomas datos formatas su žyma. Tokiu būdu sandėlio darbuotojai gali matyti, kokiu formatu įvesti datą. Nustačius šią parinktį laukų pavadinimų redaguoti negalima.</li>
<li><strong>Raidinis</strong> - jei pasirinkta ši parinktis, programoje įvedant informaciją neautomatiškai bus naudojama įrenginio klaviatūra. Klaviatūros patirtį galima keisti, atsižvelgiant į naudojamą įrenginį.</li>
<li><strong>Skaitinis</strong> - jei laukų pavadinimuose nustatyta tik skaitinių duomenų įvestis, galite pasirinkti šią parinktį, kad būtų rodoma pasirinktinė skaitinė klaviatūra su įvesties lauku, o ne įrenginio klaviatūra.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Sandėlio programos laukų prioriteto konfigūravimas

Puslapyje **Sandėlio programos laukų prioritetas** laukų pavadinimus galite suskirstyti į skirtingas prioritetų grupes. Tokiu būdu galima pasirinkti, kokia informacija turėtų būti rodomas pagrindiniame užduočių puslapyje, kai sandėlio darbuotojai atlieka užduotis naudodami programą. Jei spustelėsite **Kurti numatytąją sąranką**, bus sugeneruotas numatytasis prioritetų grupių sąrašas. Galima kurti tiek prioritetų grupių, kiek norima, bet užduočių puslapyje bus rodomos tik trys prioritetų grupės. Kai sistema siunčia metaduomenis į programą, kiekvienam laukui ji priskirs santykinį prioritetą, atsižvelgiant į lauko prioriteto grupę, o programos užduočių puslapyje bus rodomos pirmosios trys prioritetų grupės, esančios metaduomenyse. Kiti perviršio metaduomenys bus rodomi antriniame informacijos puslapyje. Tolesnėje lentelėje pateikiamas penkių prioritetų grupių pavyzdys.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritetų grupė</th>
<th>Priskirti laukai</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> 10 prioritetas</td>
<td><ul>
<li>Produktas</li>
<li>Kiekis</li>
<li>Matavimo vienetas</li>
</ul></td>
</tr>
<tr class="even">
<td> 20 prioritetas</td>
<td><ul>
<li>Klasterio pareigos</li>
<li>Klasteris</li>
</ul></td>
</tr>
<tr class="odd">
<td> 30 prioritetas</td>
<td><ul>
<li>Prekės aprašas</li>
</ul></td>
</tr>
<tr class="even">
<td> 40 prioritetas</td>
<td><ul>
<li>Konfigūravimas</li>
<li>Spalva</li>
<li>Dydis</li>
<li>Stilius</li>
</ul></td>
</tr>
<tr class="odd">
<td> 50 prioritetas</td>
<td><ul>
<li>Buvimo vieta</li>
<li>Numerio lentelė</li>
</ul></td>
</tr>
</tbody>
</table>

Pvz., kai sandėlio darbuotojas atlieka užduotį mobiliajame įrenginyje, jei metaduomenys, kurie bus rodomi programoje, apima toliau nurodytus laukus.

-   Produktas
-   Kiekis
-   Matavimo vienetas
-   Prekės aprašas
-   Dydis ir vieta

Atsižvelgiant į sandėlio programos laukų prioriteto nustatymą ankstesnėje lentelėje, užduočių puslapyje bus rodomos 3 toliau pateiktos informacijos eilutės.

-   1 eilutė: prekė, kiekis, matavimo vienetas
-   2 eilutė: prekės aprašas
-   3 eilutė: dydis

Likę metaduomenys, pvz., vieta, užduočių puslapyje rodomi nebus, bet bus rodomi informacijos puslapyje. Norėdami sužinoti daugiau ir pamatyti vartotojo sąsajos pavyzdžių žr. tinklaraščio įrašą [Pranešimas apie „Finance and Operations“ – versiją „Warehousing“](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)

<a name="additional-resources"></a>Papildomi ištekliai
--------

[„Microsoft Dynamics 365 for Finance and Operations – Warehousing“ diegimas ir konfigūravimas](install-configure-warehousing-app.md)
