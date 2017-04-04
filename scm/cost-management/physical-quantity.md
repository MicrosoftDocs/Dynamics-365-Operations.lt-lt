---
title: "Atsargų objekto vertės"
description: "Šiame straipsnyje pateikiama informacija apie tai, kaip apskaičiuojamos atsargų objektą vertės."
author: YuyuScheller
manager: AnnBe
ms.date: 2015-12-07 09 - 09 - 05
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 8898d5d91ffb4f73ea68f1251e1a99440e81bcd4
ms.lasthandoff: 03/29/2017


---

# <a name="inventory-object-values"></a>Atsargų objekto vertės

Šiame straipsnyje pateikiama informacija apie tai, kaip apskaičiuojamos atsargų objektą vertės. 

Nauja funkcija, kuri pavadinta ** fizikinį ** galite matyti konkrečius atsargų objekto vertės. Išlaidų objektas atitinka objekto lygį, kuriame atliekama atsargų apskaita. Daugiau informacijos apie išlaidų objektus rasite [Išlaidų objektai](cost-object.md). Norėdami matyti reikšmes, konkrečius atsargų objektą, spustelėkite **fizikinį** ant to **išlaidų objektu** puslapis. Štai kaip aprašo objekto vertė apskaičiuojama: atsargų objektas. Vertė = išlaidų objektu. Vidutinė vieneto savikaina x atsargų objektas. Kiekis pavyzdys rodo, kaip skaičiuojamos atsargos objekto ir išlaidų objekto vertės. Registruoti du prekės A produkto gavimo įvykiai.

-   Važtaraštis 1: kiekis = 100 vnt., suma = $1,000.00, svetainės = 1, sandėlio = 11, serijos Nr. = B1
-   Važtaraštis 2: kiekis = 50 vnt., suma = $800.00, svetainės = 1, sandėlio = 11, serijos Nr. = B2

Toliau pateikiamoje lentelėje rodomas išlaidų objekto skaičiavimo rezultatas. Rezultatą galite peržiūrėti **Išlaidų objekto** puslapyje.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekto tipas</th>
<th>Prekės numeris</th>
<th>Svetainė</th>
<th>Kiekis</th>
<th>Atsargų vienetas</th>
<th>Vertė</th>
<th>Vidutinė vieneto savikaina</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Išlaidų objektas</td>
<td>A</td>
<td>1</td>
<td>150</td>
<td>Vnt.</td>
<td><p>1 800,00 $</p></td>
<td><p>12,00 $</p></td>
</tr>
</tbody>
</table>

Toliau pateikiamoje lentelėje rodomas atsargų objekto skaičiavimo rezultatas. Rezultatą galite peržiūrėti **Išlaidų objekto** puslapyje spustelėję **Fizinis kiekis**.

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekto tipas</th>
<th>Prekės numeris</th>
<th>Svetainė</th>
<th>Sandėlis</th>
<th>Paketo nr.</th>
<th>Kiekis</th>
<th>Atsargų vienetas</th>
<th>Vertė</th>
<th>Vidutinė vieneto savikaina</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Atsargų objektas</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B1</td>
<td>100</td>
<td>Vnt.</td>
<td><p>1 200,00 $</p></td>
<td><p>12,00 $</p></td>
</tr>
<tr class="even">
<td>Atsargų objektas</td>
<td>A</td>
<td>1</td>
<td>11</td>
<td>B2</td>
<td>50</td>
<td>Vnt.</td>
<td><p>600,00 $</p></td>
<td><p>12,00 $</p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Cost objects](cost-object.md)

[Cost entries](cost-entries.md)

[Kas yra naujas ir pasikeitusias Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)


