---
title: "„Kanban“ perkėlimo srities brūkšninių kodų skaitytuvų palaikymas"
description: "„Kanban‟ perkėlimo srityje palaikoma įvestis iš valdiklių brūkšninių kodų skaitytuvo – „kanban‟ užduotį galima Pasirinkti, Pradėti, Baigti ir Ištuštinti."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1dc40de2b77be5c5c2399fd55c3c3bd15a9f24ec
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>„Kanban“ perkėlimo srities brūkšninių kodų skaitytuvų palaikymas

[!include[banner](../includes/banner.md)]


„Kanban‟ perkėlimo srityje palaikoma įvestis iš valdiklių brūkšninių kodų skaitytuvo – „kanban‟ užduotį galima Pasirinkti, Pradėti, Baigti ir Ištuštinti.

<a name="registration-modes"></a>Registravimo režimai
------------------

„FastTab“ skirtuke **Skaitytuvo registravimas** galite pasirinkti registravimo režimą, kuris valdo veiksmą, kai nuskaitote „kanban“ kortelės numerį arba patys įvedate numerį „kanban“ kortelės numerio lauke.
| Nustatyti registravimo režimą | Prekės/Paslaugos pavadinimas                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Paleisti                 | Registruoja „kanban“ perkėlimo užduotį kaip nebaigtą.                                                 |
| Baigti              | Registruoja „kanban“ perkėlimo užduotį kaip baigtą.                                                   |
| Tuščias                 | Registruoja medžiagų sandėliavimo vienetą, „kanban“ kortelėje nurodytą kaip tuščią.              |
| Pasirinkti                | Registruoja „kanban“ kortelės numerį ir automatiškai pasirenka nurodytą užduotį „kanban“ sąraše. |

 
<a name="registration-mode-select"></a>Registravimo režimas Pasirinkti
------------------------

Kai naudojate brūkšninių kodų skaitytuvą, kad pasirinktumėte užduotį, pasikeičia „kanban“ srities rodymo režimas. Dirbant šiuo režimu taikomos toliau nurodytos sąlygos.

-   Rodomos tik nuskaitytos „kanban“ užduotys.
-   Pasirinktos užduoties informacija rodoma „FastTab“ skirtuke **Išsami informacija**.
-   „FastTab“ skirtuke **Pranešimai** rodomi tik pasirinktos užduoties pranešimai.
-   Galite keisti užduoties būseną naudodami funkcijas, esančias dalyje Veiksmų sritis. „Kanban“ perkėlimo sritis tuo metu toliau rodo tik vieną užduotį.
-   Galite patys atnaujinti užduočių sąrašo informaciją dalyje Veiksmų sritis spustelėdami **Atnaujinti** („Shift“ + F5). Atnaujinus informaciją vėl rodomi visi užduoties filtro rezultatai.

## <a name="job-status-and-possible-actions"></a>Užduoties būsena ir galimi veiksmai
Pasirinktos užduoties būsena ir bet kurios iškviestos įvykio užduoties „kanban“ būsena nurodo, ar galima vykdyti užduotį toliau. Toliau pateiktoje lentelėje rodoma informacija apie šias būsenas ir užduotis:
-   Galimos užduočių arba sandėliavimo vienetų, nurodytų užduotyse, būsenos.
-   Kiekviena užduotis, kurią gali atlikti vykdant užduotį.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Užduoties tipas</th>
<th>Užduoties būsena arba sandėliavimo vieneto būsena</th>
<th>Naujinti išrinkimo dokumentą</th>
<th>Paleisti</th>
<th>Atnaujinti registraciją</th>
<th>Baigti</th>
<th>Tuščias</th>
<th>Kurti įvykio „kanban“</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Perkėlimas</td>
<td><ul>
<li>Nesuplanuota</li>
<li>Nėra iškviestų užduočių, arba iškviestų užduočių būsena yra Baigta</li>
</ul></td>
<td>Taip</td>
<td>Taip</td>
<td>Taip</td>
<td>Taip</td>
<td>Ne</td>
<td>Taip</td>
</tr>
<tr class="even">
<td>Perkėlimas</td>
<td><ul>
<li>Nesuplanuota</li>
<li>Iškviestos užduoties būsena nėra Baigta</li>
</ul></td>
<td>Taip</td>
<td>Ne</td>
<td>Taip</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="odd">
<td>Perkėlimas</td>
<td>Vykdoma</td>
<td>Taip</td>
<td>Ne</td>
<td>Taip</td>
<td>Taip</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="even">
<td>Perkėlimas</td>
<td>Atlikta</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Taip</td>
<td>Ne</td>
</tr>
<tr class="odd">
<td>Perkėlimas arba procesas</td>
<td>Tuščias</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="even">
<td>Perkėlimas arba procesas</td>
<td>Nerasta „kanban“ kortelė</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="odd">
<td>Perkėlimas arba procesas</td>
<td>„Kanban“ kortelė rasta, bet ji nepriskirta „kanban“</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="even">
<td>Apdoroti</td>
<td><ul>
<li>Nesuplanuota</li>
<li>Parengta</li>
<li>Vykdoma</li>
</ul></td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
<tr class="odd">
<td>Apdoroti</td>
<td>Atlikta</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
<td>Ne</td>
</tr>
</tbody>
</table>






