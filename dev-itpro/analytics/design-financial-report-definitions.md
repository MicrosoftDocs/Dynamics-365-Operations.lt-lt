---
title: "Finansinių ataskaitų dizaino įrankio ataskaitų aprašai"
description: "Šiame straipsnyje pateikiama informacija apie ataskaitų aprašus. Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas. Ataskaitos aprašas taip pat teikia pasirinkčių ir parametrų, kuriuos galite naudoti norėdami tinkinti ataskaitą."
author: RobinARH
manager: AnnBe
ms.date: 2016-03-07 18 - 58 - 18
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: Management Reporter, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 
ms.dyn365.ops.version: 
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81ac503410e51672c2f97a76d37d4c567832912f
ms.lasthandoff: 03/29/2017


---

# <a name="report-definitions-in-financial-report-designer"></a>Finansinių ataskaitų dizaino įrankio ataskaitų aprašai

Šiame straipsnyje pateikiama informacija apie ataskaitų aprašus. Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas. Ataskaitos aprašas taip pat teikia pasirinkčių ir parametrų, kuriuos galite naudoti norėdami tinkinti ataskaitą. 

Ataskaitos aprašas yra ataskaitos komponentas (arba kūrimo blokas), kuriame naudojamas eilutės aprašas, stulpelio aprašas ir ataskaitos kūrimui skirtas pasirinktinis ataskaitų medžio aprašas. Ataskaita apibrėžimo pateikiama parinktis ir parametrus, galite tinkinti ataskaitą. Apibrėžę eilučių aprašus ir stulpelių aprašus, turite juos sujungti į ataskaitos aprašą. Šiuo metu taip pat nustatomi kiti aprašų aspektai, pavyzdžiui, išsamumo lygis ir ataskaitos data. Tada galite įrašyti ir generuoti ataskaitą. Finansinės ataskaitos siūlo tokius išsamumo lygius.

-   Finansinis
-   Finansinis ir Sąskaitos
-   Finansinis, Sąskaitos ir Operacijos

Tačiau, atsižvelgiant į tai, kaip duomenys saugomi „Microsoft Dynamics“ ERP sistemoje, išsami operacijos informacija ataskaitose gali būti neteikiama.

## <a name="create-a-report-definition"></a>Ataskaitos aprašo kūrimas
1.  Ataskaitų konstruktoriuje, meniu **Failas**, spustelėkite **Naujas**, ir tada pasirinkite **Ataskaitos aprašas**.
2.  Nurodyti atitinkamą informaciją skirtukuose **Ataskaita**, **Išeiga ir paskirstymas**, **Antraštės ir poraštės** ir **Parametrai**.

## <a name="contents-of-a-report-definition"></a>Ataskaitos aprašo turinys
Toliau pateikiamoje lentelėje aprašomi ataskaitos aprašo skirtukai ir kaip naudojama informacija.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tabuliavimo ženklas</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ataskaita</td>
<td>Ataskaitos kūrimas, konfigūravimas arba esamos ataskaitos modifikavimas.</td>
</tr>
<tr class="even">
<td>Išeiga ir paskirstymas</td>
<td>Pakeiskite ataskaitos išeigos tipą ir paskirties vietą.</td>
</tr>
<tr class="odd">
<td>Antraštės ir poraštės</td>
<td>Apibrėžkite ir suformatuokite ataskaitos antraštes ir poraštes. Pavyzdžiui, galite pridėti prie antraštės arba poraštės teksto arba vaizdų. Finansinės ataskaitos palaiko .bmp, .jpg ir .png vaizdų failus. Taip pat galite pridėti automatinio teksto kodų kitai informacijai įterpti pavyzdžiui, įmonės pavadinimą, ataskaitos pavadinimą arba puslapio numerį.</td>
</tr>
<tr class="even">
<td>Parametrai</td>
<td>Nurodykite ataskaitos aprašo parametrus, pavyzdžiui, šiuos parametrus.
<ul>
<li>Formatavimas ir sumos apvalinimas</li>
<li>Informacijos ataskaitų formatas</li>
<li>Ataskaitų medžių formatas</li>
<li>Išimčių ataskaitos generavimas</li>
<li>Valiutos konvertavimo nurodymas</li>
<li>Tarpinė suma ir sąskaitos informacijos filtravimas</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Finansinė atskaitomybė už Microsoft Dynamics 365 operacijoms](financial-reporting-intro.md)


