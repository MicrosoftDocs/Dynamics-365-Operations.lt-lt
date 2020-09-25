---
title: Darbo paskirstymo struktūros šablonų vaidmenų nustatymas
description: Šioje temoje pateikiama informacija apie vaidmenų informacijos nustatymą darbo paskirstymo struktūros šablonuose.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760616"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Darbo paskirstymo struktūros šablonų vaidmenų nustatymas

[!include [banner](../includes/banner.md)]

Projektų vadovai gali nustatyti darbo paskirstymo struktūros (WBS) šablonus, kuriuos jie gali taikyti kurdami naujų projektų WBS. Kurdami šabloną projektų vadovai gali įtraukti vaidmenų. Naudodami tolesnę procedūrą galite WBS šablonui priskirti vaidmenį. 

1. Pasirinkite **Projektų valdymas ir apskaita** > **Nustatymas** > **Projektai** > **Darbo paskirstymo struktūrų šablonai**.
2. Prie pasirinkto WBS šablono pasirinkite **Išsami informacija**.
3. Sąraše pasirinkite užduotį, tada lauke **Vaidmuo** pasirinkite užduočiai priskirtiną vaidmenį.

## <a name="work-with-a-wbs"></a>Darbas su WBS

Galite sukurti naują WBS arba WBS galite nukopijuoti iš esamo WBS šablono. Priskirdamas vaidmenis naujoms WBS užduotims projekto vadovas gali lengvai valdyti išteklius. Vaidmenis galima pakeisti gavus išteklių arba identifikavus patvirtintą išteklių darbui su užduotimi. Toks lankstumas projektų vadovams leidžia atlikti tolesnes užduotis.

- Identifikuoti, kiek išteklių reikia WBS darbo paketams.
- Įvertinti projekto išlaidas.
- Nustatyti preliminarų biudžetą.
- Pagal vaidmenis ir išteklius įvertinti veiklos trukmę.
- Pagal turimą projektų informaciją kurti projektų valdymo planų.

Siekiant geriau išnaudoti išteklių funkcijas, į WBS įtraukta papildomų parinkčių.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parinktis</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Išteklių priskyrimas</td>
<td>Peržiūrėkite priskirtus WBS užduočių išteklius, datas, valandų skaičių ir rezervavimo tipą.</td>
</tr>
<tr class="even">
<td>Automatiškai generuoti komandą</td>
<td>Naudodami su užduotimi susietus vaidmenis automatiškai įtraukite suplanuotų išteklių. „Finance‟ suplanuotų išteklių siūlo automatiškai, naudodama kelių kriterijų sprendimų analizę pagal vaidmenis. Kai nustatyti WBS užduočių vaidmenys bei pastangos (valandos) ir atlaisvinta struktūra, pasirinkite <strong>Automatiškai generuoti komandą</strong>. Reikiamas suplanuotų išteklių skaičius įtraukiamas į WBS ir skirtuką <strong>Projekto komanda ir planavimas</strong>.</td>
</tr>
<tr class="odd">
<td>Išteklius (išplečiamasis sąrašas)</td>
<td>Puslapyje <strong>Paleisti išteklių priskyrimą</strong> pagal nurodytą trukmę galite pasirinkti, ar išteklius planuoti tiksliai, ar apytiksliai. Galite koreguoti rodinio parametrus ir matyti bei nustatyti išteklių veiklų trukmę. Naudodami tolesnes parinktis, išteklius galite pasirinkti ir priskirti darbo paketų lygiu.
<ul>
<li><strong>Priimti</strong> – patvirtinti ištekliaus, priskirto užduočiai, keitimus.</li>
<li><strong>Atšaukti</strong> – atšaukti ištekliaus, priskirto užduočiai, keitimus.</li>
<li><strong>Priskirti automatiškai</strong> – automatiškai parenkamas ir pasirinktai užduočiai priskiriamas galimas personalo išteklius su atitinkamu vaidmeniu.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ atnaujinimas, 2 etapas**.
2. Pasirinkite **Planas** > **Veiklos** > **Darbo paskirstymo struktūra**.
3. Pasirinkdami **Naujas** į WBS įtraukite tolesnes pirmo lygio veiklas.

    - Inicijavimas
    - Planavimas
    - Vykdoma
    - Stebėjimas ir valdymas
    - Artimas

4. Kaip parodyta tolesnėje iliustracijoje, nustatykite datas ir pastangas (valandas).

    [![Datų ir pastangų nustatymas](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Pasirinkite užduoties eilutę **Inicijavimas**, tada lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.
6. Pasirinkite **Publikuoti**.
7. Toje pačioje eilutėje, lauke **Išteklius** pasirinkite **Danielis Goldschmidtas**, o tada – **Patvirtinti**.
8. Pasirinkite užduoties eilutę **Planavimas**, tada lauke **Vaidmuo** pasirinkite **Verslo analitikas**.
9. Pasirinkite **Publikuoti**, tada – **Automatiškai generuoti komandą**.
10. Pasirodžiusiame pranešimo lange pasirinkite **Taip**.
11. Įsitikinkite, ar lauko **Išteklius** reikšmė yra **1 verslo analitikas**.
12. Atidarykite ištekliaus **1 verslo analitikas** peržvalgą ir pasirinkite **Paleisti išteklių priskyrimus**. Tada užduočiai parinkite darbuotoją.
13. Pasirinkite **Apytiksliai priskirti** &gt; **Visas pajėgumas**.

    > [!NOTE] 
    > Įspėjimo, kad nurodytas išteklius dabar yra 2, negaunate, nes išteklių skaičius lieka 1.

14. Puslapyje **Darbo paskirstymo struktūra** patikrinkite WBS išteklių priskyrimą ir pasirinkite **Įrašyti**.
