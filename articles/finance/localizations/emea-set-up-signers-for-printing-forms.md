---
title: Spausdintų formų pasirašančiųjų nustatymas
description: Jei pagrindinis juridinio subjekto adresas yra Čekijos Respublikoje, Estijoje, Vengrijoje, Lietuvoje, Latvijoje, Lenkijoje arba Rusijoje, galite nustatyti klientų ir tiekėjų, kurie spausdina dokumentus, pvz., SF ir grynųjų pinigų užsakymus, pasirašančiuosius ir pareigas.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 263464
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 64868aa08201fa3df99cd86fa6ef5231a9347151
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408246"
---
# <a name="set-up-signers-for-print-forms"></a>Spausdintų formų pasirašančiųjų nustatymas

[!include [banner](../includes/banner.md)]

Jei pagrindinis juridinio subjekto adresas yra Čekijos Respublikoje, Estijoje, Vengrijoje, Lietuvoje, Latvijoje, Lenkijoje arba Rusijoje, galite nustatyti klientų ir tiekėjų, kurie spausdina dokumentus, pvz., SF ir grynųjų pinigų užsakymus, pasirašančiuosius ir pareigas.

<a name="set-up-default-values"></a>Numatytųjų verčių nustatymas
---------------------

Norėdami nustatyti įmonės spausdinamų dokumentų pasirašančiuosius naudokite puslapį **Tarnautojai**. Atsižvelgiant į dokumento tipą, galite nustatyti tiek įmonės, tiek klientų arba tiekėjų pasirašančiuosius ir jų pareigas. Toliau pateikiamoje lentelėje aprašomi puslapio **Tarnautojai** skirtukai.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Skirtukas</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bendra</td>
<td>Įtraukite pasirašančiųjų, kurie gali pasirašyti visų tipų spausdintus dokumentus, pareigas ir susijusią informaciją (direktorius ir vyriausiasis buhalteris).</td>
</tr>
<tr class="even">
<td>DK</td>
<td>Įtraukite pasirašančiųjų, kurie gali pasirašyti toliau nurodytus vidinius finansinius dokumentus, susijusius su pinigų srautu, pareigas ir susijusią informaciją.
<ul>
<li>Grynųjų kvitai</li>
<li>Išankstinė ataskaita</li>
<li>Kasos knygos puslapis</li>
<li>Skaičiavimo išrašas</li>
<li>Atidėjimai<em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Pardavimo užsakymai</td>
<td>Įtraukite pasirašančiųjų, kurie gali pasirašyti toliau nurodytus išeinančius pirminius dokumentus, susijusius su klientais, pareigas ir susijusią informaciją.
<ul>
<li>Mokėjimo SF</em></li>
<li>PVM sąskaita faktūra</li>
<li>Faktūra<em></li>
<li>SF – kredito pažyma</li>
<li>Faktūra – kredito pažyma</em></li>
<li>Mokesčių operacijos faktūra (klientas)<em></li>
</ul></td>
</tr>
<tr class="even">
<td>Pirkimo užsakymai</td>
<td>Įtraukite pasirašančiųjų, kurie gali pasirašyti toliau nurodytus įeinančius pirminius dokumentus, susijusius su tiekėjais, pareigas ir susijusią informaciją.
<ul>
<li>PVM sąskaita faktūra</li>
<li>Faktūra</em></li>
<li>SF – kredito pažyma</li>
<li>Faktūra – kredito pažyma<em></li>
<li>Mokėjimo SF</em></li>
<li>Mokesčių operacijos faktūra (tiekėjas)<em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Atsargų prekės valdymas</td>
<td>Įtraukite pasirašančiųjų, kurie gali pasirašyti toliau nurodytus sandėlio dokumentus, kai materialusis turtas išduodamas klientui arba gaunamas iš tiekėjo, pareigas ir susijusią informaciją.
<ul>
<li>Pardavimo užsakymo išdavimo kvitas (M-15)</em></li>
<li>Komp. kvitas / gavimo užsakymas</li>
<li>Perkėlimo užsakymo išdavimo kvitas (M-15)*</li>
</ul></td>
</tr>
</tbody>
</table>

\* Šis dokumento tipas pasiekiamas tik juridiniams subjektams, kurių pagrindinis adresas yra Rusijoje. Toliau pateikiamoje lentelėje aprašomi puslapio **Tarnautojai** laukai.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Laukas</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pozicija</td>
<td>Pasirinkite pasirašančiojo registravimo pareigas.</td>
</tr>
<tr class="even">
<td>Vardas</td>
<td>Pasirinkite pasirašančiojo registravimo vardą. Sąrašo vardai pateikiami iš lentelės Kontaktai arba lentelės Darbuotojai, atsižvelgiant į pasirašančiojo tipą (t. y. atsižvelgiant į tai, ar pažymėtas žymės langelis <strong>Mūsų</strong>). Jei pasirašančiojo vardo sąraše nėra, patys įveskite pasirašančiojo vardą ir pavardę.</td>
</tr>
<tr class="odd">
<td>Pareigos</td>
<td>Pasirinkite pasirašančiojo pareigas. Jei pasirašančiojo pareigų sąraše nėra, patys įveskite pasirašančiojo pareigas.</td>
</tr>
<tr class="even">
<td>Sąskaitos kodas</td>
<td>Pasirinkite, ar pasirašantysis gali pasirašyti visus pasirinkto dokumento tipo dokumentus, ar tik konkretaus kliento arba tiekėjo dokumentus.</td>
</tr>
<tr class="odd">
<td>Sąskaitos ryšys</td>
<td>Pasirinkite kliento arba tiekėjo sąskaitą, susijusią su pasirinktu sąskaitos kodu. Šis laukas galimas, tik jei lauke <strong>Sąskaitos kodas</strong> pasirinkote <strong>Įrašas</strong>.</td>
</tr>
<tr class="even">
<td>Mūsų</td>
<td>Pasirinktas žymės langelis rodo, kad pareigos yra vidinės.</td>
</tr>
<tr class="odd">
<td>Susiejimas su sandėliu</td>
<td>Pasirinkite, ar pasirašantysis yra priskirtas visiems sandėliams, ar tik tam tikram sandėliui. Galimos toliau nurodytos pasirinktys:
<ul>
<li><strong>Visi</strong> – pasirašantysis priskirtas visiems sandėliams.</li>
<li><strong>Įrašas</strong> – pasirašantysis priskirtas konkrečiam sandėliui.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sandėlis</td>
<td>Pasirinkite sandėlio kodą, nurodantį sandėlį, kuriam pasirašantysis yra priskirtas. Šis laukas galimas, tik jei lauke <strong>Susiejimas su sandėliu</strong> pasirinkote <strong>Įrašas</strong>.</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a>Tarnautojų numeracijos kodo nustatymas
Puslapio **Juridiniai subjektai** dalyje **Numeracijos** galite tarnautojams priskirti numeracijos kodą. Pasirinkite nuorodos **Tarnautojų seanso ID** numeracijos kodą.

## <a name="modify-signers-in-primary-documents"></a>Pasirašančiųjų keitimas pirminiuose dokumentuose
Funkcija Tarnautojai nurodo numatytuosius iš anksto nustatytus pasirašančiuosius iš lentelės Tarnautojai. Puslapio **Registravimo SF** skirtuke **Tarnautojai** galite keisti pasirašančiojo vardą ir pareigas pirminiame dokumente, kai dokumento tipas yra vienas iš toliau nurodytųjų.

-   Kliento SF
-   Tiekėjo SF
-   Siuntimo perkėlimo užsakymas
-   Grynųjų užsakymas

**Pastaba.** Užregistravus dokumentą, tarnautojų redaguoti negalima.



