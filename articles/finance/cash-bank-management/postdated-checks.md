---
title: Vėlesni čekiai
description: Šiame straipsnyje pateikta informacija apie palaikymą dėl vėlesnių čekių „Microsoft“ „Dynamics 365 Finance“. Vėlesni čekiai yra čekiai, išrašomi norint atlikti ir gauti mokėjimus ateityje. Todėl čekio negalima išgryninti iki nurodytos datos.
author: ShylaThompson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e937361802aa1443f3e2ef9f3bb95d3f4966da7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815793"
---
# <a name="postdated-checks"></a>Vėlesni čekiai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie palaikymą dėl vėlesnių čekių. Vėlesni čekiai yra čekiai, išrašomi norint atlikti ir gauti mokėjimus ateityje. Todėl čekio negalima išgryninti iki nurodytos datos.

„Dynamics 365 Finance“ palaiko visą vėlesnių čekių valdymo ciklą ir gautinose sumos, ir mokėtinose sumose, kaip parodyta pateiktoje lentelėje.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenarijus</th>
<th>Išsami informacija</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vėlesnių čekių nustatymas</td>
<td>Turite nustatyti naują mokėjimo būdą ir nurodyti reguliarią mokėjimo procedūrą išrašytų čekių, gautų čekių ir išskaitomo mokesčio atsiskaitymo sąskaitoms.</td>
</tr>
<tr class="even">
<td>Vėlesnio tiekėjo čekio užregistravimas</td>
<td>Registruokite vėlesnių čekių, išrašytų tiekėjui, išsamią informaciją. Užregistravus mokėjimą tiekėjo įsipareigojimai pripažįstami, bet banko sąskaita nėra dar kredito sąskaita. Vietoj to, šiuo tikslu naudojama atsiskaitymo sąskaita. </td>
</tr>
<tr class="odd">
<td>Registruoti kliento vėlesnį čekį</td>
<td>Užregistruokite išsamią vėlesnio iš kliento gauto čekio informaciją. Užregistravus mokėjimą kliento gaunama suma yra kreditas, bet banko sąskaita dar nėra debeto sąskaita. Vietoj to, šiuo tikslu naudojama atsiskaitymo sąskaita.</td>
</tr>
<tr class="even">
<td>Vėlesnio kliento arba tiekėjo čekio pakeitimo užregistravimas</td>
<td>
Jei pamesite arba sugadinsite pradinį čekį tiekėjui arba gautą iš kliento, galėsite išduoti pakeitimo vėlesnį čekį. Kai užregistruosite išsamią čekio informaciją, pateikite nuorodą į pradinį čekį ir nurodykite, kad naujasis čekis yra pradinio čekio pakaitalas. Taip pat galite užregistruoti pakeitimo čekį.</td>
</tr>
<tr class="odd">
<td>Kliento vėlesnio čekio perkėlimas tiekėjui</td>
<td>Kai gaunate vėlesnį čekį iš kliento, galite perduoti čekį tiekėjui kaip mokėjimą.</td>
</tr>
<tr class="even">
<td>Vėlesnio kliento arba tiekėjo čekio sudengimas</td>
<td>Sudenkite kliento arba tiekėjo vėlesnį čekį, užregistruotą tarpinėje sąskaitoje, kaip čekio terminas galiausiai sueis. Sudengus čekį, banko sąskaita galiausiai yra debetas ar kreditas, pagal atsiskaitymo sąskaitą, kuri buvo naudota anksčiau.</td>
</tr>
<tr class="odd">
<td>Vėlesnio tiekėjo čekio atšaukimas</td>
<td>Galite atšaukti paskelbtą paskesnį čekį šiomis situacijomis: - Čekį grąžina bankas.
- Čekis taikomas netinkamai sąskaitai faktūrai.
- Mokėjimas grynaisiais pinigais atliktas pagal čekį.
  </td>
  </tr>
  <tr class="even">
  <td>Vėlesnio čekio mokėjimo stabdymas</td>
  <td>Galite sustabdyti mokėjimą vėlesniame čekyje, kuris buvo išduotas tiekėjui dėl tokių priežasčių, kaip nepakankamos lėšos, sutarties su tiekėju sąlygų pakeitimai, tiekėjo prekių su defektais atsiuntimas arba prekių gražinimas tiekėjui. Galite sustabdyti tik neapmokėtų čekių mokėjimą.</td>
  </tr>
  </tbody>
  </table>



Daugiau informacijos ieškokite šiose temose:

[Vėlesnių čekių nustatymas](tasks/set-up-postdated-checks.md)

[Registruoti kliento vėlesnį čekį](tasks/register-post-postdated-check-customer.md)

[Vėlesnio čekio iš kliento sudengimas](tasks/settle-postdated-check-customer.md)

[Registruoti tiekėjo vėlesnį čekį](tasks/register-post-postdated-check-vendor.md) 

[Vėlesnio tiekėjo čekio sudengimas](tasks/settle-postdated-check-vendor.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]