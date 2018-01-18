---
title: "Numatytosios korespondentinės sąskaitos pardavėjo sąskaitų faktūrų žurnalams ir sąskaitų faktūrų patvirtinimo žurnalams"
description: "Ši tema padės jums nuspręsti, kur priskirti numatytąsias sąskaitas sąskaitų faktūrų žurnaluose."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf7af869e44a60d07d66e83bfb55bd0cc7edfb91
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a>Numatytosios korespondentinės sąskaitos pardavėjo sąskaitų faktūrų žurnalams ir sąskaitų faktūrų patvirtinimo žurnalams

[!include[banner](../includes/banner.md)]




Numatytosios korespondentinės naudojamos su šiais pardavėjo sąskaitų faktūrų žurnalų puslapiais:

-   SF žurnalas
-   SF patvirtinimo žurnalas

Naudokite šią lentelę, kai reikia nuspręsti, kur priskirti numatytąsias sąskaitas sąskaitų faktūrų žurnaluose.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Nustatyti numatytąsias korespondentines sąskaitas čia</th>
<th>Kur yra teikiamos numatytosios sąskaitos</th>
<th>Kaip ši parinktis įtakoja apdorojimą</th>
<th>Kada naudoti šią parinktį</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Tiekėjų grupė</strong> – nustatykite numatytuosius korespondentines sąskaitas tiekėjų grupėms <strong>Numatytieji sąskaitos nustatymai</strong> puslapyje, kurį galite atidaryti <strong>Tiekėjų grupių</strong> puslapyje.</td>
<td><ul>
<li>Tiekėjo kodas</li>
<li>Tiekėjų sąskaitų žurnalų įrašai tiekėjų grupėje, jei numatytosios sąskaitos nėra nurodytos tiekėjų sąskaitoms</li>
</ul></td>
<td>Numatytosios korespondentinės sąskaitos tiekėjų grupėms rodomos kaip numatytosios korespondentinės sąskaitos tiekėjams <strong>Numatytosios sąskaitos nustatymų</strong> puslapyje. Šį puslapį galite atidaryti iš <strong>Visi tiekėjai</strong> sąrašo puslapio.</td>
<td>Naudokite šią parinktį, jei paprastai mokate už tos pačios rūšies prekes iš tos pačios tiekėjų grupės.</td>
</tr>
<tr class="even">
<td><strong>Tiekėjo sąskaita</strong> – nustatykite numatytąsias sąskaitas tiekėjo sąskaitoms <strong>Numatytieji sąskaitos nustatymai</strong> puslapyje, kurį galite atidaryti <strong>Tiekėjų</strong> puslapyje.</td>
<td>Tiekėjo sąskaitos žurnalo įrašai</td>
<td>Numatytosios korespondentinės sąskaitos tiekėjų sąskaitoms rodomos kaip numatytosios korespondentinės sąskaitos tiekėjų žurnalo įrašams.</td>
<td>Naudokite šią parinktį, jei paprastai mokate už tos pačios rūšies prekes iš tų pačių tiekėjų.</td>
</tr>
<tr class="odd">
<td><strong>Žurnalų pavadinimai</strong> – nustatykite numatytąsias korespondentines sąskaitas žurnaluose <strong>Žurnalų pavadinimai</strong> puslapyje. Pasirinkite <strong>Fiksuota korespondentinė sąskaita</strong> parinktį. Atkreipkite dėmesį, kad negalite nurodyti numatytųjų korespondentinių sąskaitų žurnalo pavadinimuose, jei žurnalo pavadinimų žurnalo tipas yra <strong>Sąskaitų faktūrų registras</strong> arba <strong>Patvirtinimas</strong>.</td>
<td><ul>
<li>Žurnalo antraštė, kurioje naudojamas žurnalo pavadinimas</li>
<li>Žurnalo įrašai žurnaluose, kuriuose naudojamas žurnalo pavadinimas</li>
</ul></td>
<td>Jei pasirinktas <strong>Fiksuota korespondentinė sąskaita</strong> puslapis iš <strong>Žurnalų pavadinimai</strong>, žurnalo pavadinimo korespondentinė sąskaita yra viršesnė už numatytąją korespondentinę sąskaitą tiekėjui arba tiekėjų grupei.</td>
<td>Naudokite šią parinktį, norėdami sukurti konkrečių išlaidų ir išlaidų, kurios priskiriamos konkrečioms sąskaitoms, žurnalus, nepriklausomai nuo tiekėjo ar tiekėjų grupės, kuriai priklauso tiekėjas.</td>
</tr>
<tr class="even">
<td><strong>Žurnalų pavadinimai</strong> – nustatykite numatytąsias korespondentines sąskaitas žurnaluose <strong>Žurnalų pavadinimai</strong> puslapyje. Ištrinkite <strong>Fiksuota korespondentinė sąskaita</strong> parinktį. Atkreipkite dėmesį, kad negalite nurodyti numatytųjų korespondentinių sąskaitų žurnalo pavadinimuose, jei žurnalo pavadinimų žurnalo tipas yra <strong>Sąskaitų faktūrų registras</strong> arba <strong>Patvirtinimas</strong>.</td>
<td><ul>
<li>Žurnalo antraštė</li>
<li>Žurnalo įrašai žurnaluose, kuriuose naudojamas žurnalo pavadinimas</li>
</ul></td>
<td>Šie numatytieji įrašai naudojami žurnalo antraštės puslapiuose, o korespondentinė sąskaita žurnalo antraštės puslapyje naudojama kaip numatytasis įrašas žurnalo kvitų puslapiuose. Numatytosios sąskaitos iš <strong>Žurnalo pavadinimų </strong>puslapio naudojamos tik tada, jei nėra sukurtos numatytosios sąskaitos tiekėjo sąskaitai.</td>
<td>Naudokite šią parinktį, norėdami nustatyti numatytąsias sąskaitas, kurios naudojamos, kai nepriskirta numatytojo tiekėjo korespondentinė sąskaita.</td>
</tr>
<tr class="odd">
<td><strong>Žurnalo antraštė</strong> – nustatykite numatytąją korespondentinę sąskaitą žurnalui kaip numatytąją įrašą žurnalo kvitų puslapiuose. Atkreipkite dėmesį, kad negalite nurodyti numatytųjų korespondentinių sąskaitų žurnalo antraštėje, jei žurnalo pavadinimų žurnalo tipas yra <strong>Sąskaitų faktūrų registras</strong> arba <strong>Patvirtinimas</strong>.</td>
<td>Žurnalo įrašai žurnale</td>
<td>Numatytoji korespondentinė sąskaita žurnalui naudojama kaip numatytasis įrašas žurnalo kvitų puslapiuose.</td>
<td>Naudokite šią parinktį, norėdami paspartinti duomenų įvedimą, jei dauguma įrašų žurnale turi tą pačią korespondentinę sąskaitą.</td>
</tr>
</tbody>
</table>






