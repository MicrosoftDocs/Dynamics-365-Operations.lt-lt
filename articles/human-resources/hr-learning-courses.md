---
title: Mokymų kursų nustatymas
description: Žmogiškųjų išteklių administratoriai ir vadovai kursų funkcijas gali naudoti siekdami tvarkyti informaciją apie darbuotojams siūlomą mokymą.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 45466b8f52ddc261737da7474767c21f5bd331f8
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689893"
---
# <a name="set-up-training-courses"></a>Mokymų kursų nustatymas


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Žmogiškųjų išteklių administratoriai ir vadovai kursų funkcijas gali naudoti siekdami tvarkyti informaciją apie darbuotojams siūlomą mokymą.

##  <a name="set-up-prerequisites"></a>Nustatyti būtinąsias sąlygas

Prieš kuriant kursus, reikia turėti ir nustatyti toliau pateiktą informaciją.
-   **Kursų tipai**

Ši informacija yra nebūtina informacija, kurią galite nurodyti apie kursus. Jei žinote, kad įvesite šią kursų informaciją, turėtumėte ją nustatyti prieš sukurdami kursų įrašus.
-   **Auditorijų grupės**
-   **Kursų grupės**
-   **Kursų vietos**
-   **Auditorijos**
-   **Dėstytojai**

## <a name="course-types"></a>Kursų tipai
Kursų tipus galite naudoti kursams pagal kurso struktūrą arba turinį suskirstyti. Kurti kursų tipus galite **Kursų tipų** puslapyje. Kurdami kurso įrašą turite pasirinkti kursų tipą.

## <a name="course-setup-type"></a>Kursų nustatymo tipas
Šioje lentelėje išvardijami trys kursų nustatymo tipai. Kurso struktūra yra nustatoma pritaikius nustatymo tipus.

<table>
<thead>
<tr class="header">
<th>Nustatymo tipas</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Stand.</strong></td>
<td>Pasirinkite šį tipą tiems kursams, kurių darbotvarkė nebus sudaryta kiekvienai dienai. Tai yra numatytasis nustatymo tipas kuriant naują kursą.</td>
</tr>
<tr class="even">
<td><strong>Darbotvarkė</strong></td>
<td>Pasirinkite šį tipą, norėdami planuoti kurso, kuris vyksta kelias dienas, kiekvienos dienos informaciją.</td>
</tr>
<tr class="odd">
<td><strong>Darbotvarkė + sesija</strong></td>
<td>Pasirinkite šį tipą sudėtingesniems kursams. Pavyzdžiui, kurso darbotvarkę galite suskirstyti į specializacijas ir sesijas.
<ul>
<li><strong>Specializacija</strong> – specializacijos yra konkrečios kurso objekto sritys.</li>
<li><strong>Sesijos</strong>: specializacijos padalinamos pritaikius sesijas, o sesijos gali padėti identifikuoti konkrečius procesus arba technikas, susijusias su kiekviena specializacija.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Kurso užduotys
Su visais kursais galite atlikti toliau nurodytas užduotis.
- Registruoti dalyvius.
- Nurodyti paskutinę registracijos datą.
- Nustatyti mažiausią ir didžiausią dalyvių skaičių.
- Priskirti kurso vietą ir auditoriją.
- Kurso dalyviams rekomenduoti viešbučius.
- Kurti kurso aprašą, kurį galima vėliau paskelbti **Darbuotojų savitarnoje**

  >**Pastaba.** Kursą panaikinti galite tik jei niekas į jį neužsiregistravo. 

## <a name="course-statuses"></a>Kurso būsenos
Šioje lentelėje pateikiamos galimos kurso būsenos ir veiksmai, kuriuos galite atlikti su konkrečios būsenos kursu.

<table>
<thead>
<tr class="header">
<th>Būsena</th>
<th>Veiksmai</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Sukurta</strong></td>
<td><ul>
<li>Įvesti ir modifikuoti kurso informaciją.</li>
<li>Kurso būseną keisti į <strong>Atidarytas</strong> – tada darbuotojai galės registruotis į kursą.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Atidaryti</strong></td>
<td><ul>
<li>Registruoti dalyvius į kursą.</li>
<li>Šalinti dalyvius iš kurso.</li>
<li>Patvirtinti kurso dalyvius.</li>
<li>Pakeisti kurso būseną į <strong>Uždarytas</strong> arba <strong>Atšauktas</strong>.</li>
<li>Planuoti dalyvių, kurių būsena <strong>Patvirtintas</strong>, klausimynus.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Uždaryta</strong></td>
<td>Galite iš naujo atidaryti kursą.</td>
</tr>
<tr class="even">
<td><strong>Atšaukta</strong></td>
<td>Galite iš naujo atidaryti kursą.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Kurso dalyviai
Kurso dalyviai yra darbuotojai, dalyvaujantys mokymo kursuose arba renginyje. Galite užregistruoti dalyvius tik į atvirus kursus. Mažiausias ir didžiausias leistinas registruoti į kursą dalyvių skaičius nustatytas puslapio **Kursai** „FastTab“ skirtuke **Bendra**.

## <a name="workflow"></a>Darbo eiga

Darbuotojų, kurie į kursą registruojasi per puslapį **Darbuotojų savitarna**, registraciją galima nukreipti pro darbo eigą, kad būtų patvirtinta. Galite priskirti darbo eigą puslapio **Kursai** „FastTab‟ **Bendra**.







[!INCLUDE[footer-include](../includes/footer-banner.md)]
