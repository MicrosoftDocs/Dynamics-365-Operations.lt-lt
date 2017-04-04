---
title: "Nustatyti prenumeratorių spausdinimo formų"
description: "Juridiniams asmenims – Čekijos Respublikos, Estijos, Vengrijos, Lietuvos, Latvijos, Lenkijos ir Rusijos, norite paskirti ne signatarų ir pavadinimų pirkėjams ir tiekėjams, kad spausdinti dokumentus pvz., SF ir pinigų pavedimai."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 263464
ms.assetid: 7213914a-ecb6-4711-99fe-4e11867aaf4d
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 45d2facde1e5502f4a5863863554a486916c26cd
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-signers-for-print-forms"></a>Nustatyti prenumeratorių spausdinimo formų

Juridiniams asmenims – Čekijos Respublikos, Estijos, Vengrijos, Lietuvos, Latvijos, Lenkijos ir Rusijos, norite paskirti ne signatarų ir pavadinimų pirkėjams ir tiekėjams, kad spausdinti dokumentus pvz., SF ir pinigų pavedimai.

<a name="set-up-default-values"></a>Numatytųjų verčių nustatymas
---------------------

Norėdami nustatyti prenumeratorių dokumentų, kad įmonė spausdina, naudoti su **pareigūnų** puslapis. Jūs galite nustatyti pasirašiusiuosius asmenis ir jų pavadinimai įmonės ir klientų ar tiekėjų, atsižvelgiant į dokumento tipą. Šioje lentelėje aprašomi skirtukai dėl to **pareigūnų** puslapis.

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
<td>Pridėti pozicijų ir susijusios informacijos apie pasirašiusiuosius asmenis (direktorius ir Vyriausiasis buhalteris) kurie gali pasirašyti spausdinimo dokumentus visų rūšių.</td>
</tr>
<tr class="even">
<td>DK</td>
<td>Pridėti poziciją ir susijusi informacija apie pasirašiusiuosius asmenis, kurie gali pasirašyti šie vidaus finansinius dokumentus, susijusios su pinigų srautų:
<ul>
<li>Grynųjų kvitai</li>
<li>Išankstinė ataskaita</li>
<li>Kasos knygos puslapis</li>
<li>Skaičiavimo išrašas</li>
<li>Atidėjimų *</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pardavimo užsakymai</td>
<td>Pridėti pozicijų ir susijusios informacijos pasirašančių asmenų gali pasirašyti šiuos išeinančius pirminės dokumentus, susijusius su klientais:
<ul>
<li>SF mokėjimo *</li>
<li>PVM sąskaita faktūra</li>
<li>Faktūros *</li>
<li>SF – kredito pažyma</li>
<li>Faktūra – kredito-Pastaba *</li>
<li>Mokesčių operacijos faktūra (klientas) *</li>
</ul></td>
</tr>
<tr class="even">
<td>Pirkimo užsakymai</td>
<td>Pridėti pozicijų ir susijusios informacijos pasirašančių asmenų gali pasirašyti šiuos gaunamus pirminius dokumentus, kurie yra susiję su tiekėjų:
<ul>
<li>PVM sąskaita faktūra</li>
<li>Faktūros *</li>
<li>SF – kredito pažyma</li>
<li>Faktūra – kredito-Pastaba *</li>
<li>SF mokėjimo *</li>
<li>Mokesčių operacijos faktūra (tiekėjas) *</li>
</ul></td>
</tr>
<tr class="odd">
<td>Atsargų prekės valdymas</td>
<td>Pridėti pozicijų ir susijusios informacijos pasirašančių asmenų gali pasirašyti šiuos sandėlio dokumentus, kai materialus turtas yra klientui išduota arba gauta iš tiekėjo:
<ul>
<li>Išduoti kvitą pardavimo užsakymo (M-15) *</li>
<li>RMB. kvitas/gavimo užsakymas</li>
<li>Išduoti kvitą už pavedimą (M-15) *</li>
</ul></td>
</tr>
</tbody>
</table>

\*Šis dokumento tipas yra galimas tik juridiniai asmenys, kurie turi savo pagrindinį adresą Rusijoje. Toliau pateiktoje lentelėje apibūdinami laukai, dėl to **pareigūnų** puslapis.

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
<td>Pasirinkite pasirašančio asmens pavadinime.</td>
</tr>
<tr class="even">
<td>Vardas</td>
<td>Pasirinkite pasirašančio asmens pavadinimas. Sąraše pavadinimai kilę iš kontaktų lentele arba lentele darbuotojai, priklausomai nuo pasirašantis asmuo (t. y. priklausomai nuo to, ar su <strong>mūsų</strong> yra pažymėtas žymės langelis). Jei sąraše nėra pasirašančio asmens vardas, įvesti rankiniu būdu pasirašančio asmens vardas, pavardė.</td>
</tr>
<tr class="odd">
<td>Pareigos</td>
<td>Pasirinkite pasirašančio asmens pareigos. Jei sąraše nėra pasirašančio asmens pavadinimas, įvesti rankiniu būdu pasirašančio asmens pavadinimas.</td>
</tr>
<tr class="even">
<td>Sąskaitos kodas</td>
<td>Pasirinkti, ar į pasirašantysis gali pasirašyti visus dokumentus pasirinktą dokumento tipą, ar tik dokumentų tam tikram klientui arba tiekėjui.</td>
</tr>
<tr class="odd">
<td>Sąskaitos ryšys</td>
<td>Pasirinkite kliento ar tiekėjo sąskaitą, kuri yra susijusi su pasirinktos sąskaitos kodą. Šį lauką galima naudoti tik pasirinkus <strong>įrašas</strong>, kad <strong>sąskaitos kodas</strong> srityje.</td>
</tr>
<tr class="even">
<td>Mūsų</td>
<td>Pasirinktas žymės langelis rodo, kad padėtis yra vidaus.</td>
</tr>
<tr class="odd">
<td>Susiejimas su sandėliu</td>
<td>Pasirinkite, ar pasirašančio priskirtas visus sandėlius ar tik konkretų sandėlį. Galimos toliau nurodytos pasirinktys:
<ul>
<li><strong>Visi</strong> – pasirašantis asmuo priskiriamas visų sandėlių.</li>
<li><strong>Įrašas</strong> – pasirašantis asmuo priskiriamas konkretų sandėlį.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sandėlis</td>
<td>Pasirinkite sandėlio kodas, atitinkantis sandėlį, kad pasirašantis asmuo yra priskirtas. Šį lauką galima naudoti tik pasirinkus <strong>įrašas</strong>, kad <strong>susiejimas su sandėliu</strong> srityje.</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a>Nustatyti numeracijos kodą pareigūnams
Numeracijos kodą gali skirti pareigūnus, **skaičių sekas** skyriuje, **juridinių asmenų** puslapis. Pasirinkite numeracijos kodą, kad **pareigūnų seanso ID** nuoroda.

## <a name="modify-signers-in-primary-documents"></a>Modifikuoti prenumeratorių pirminių dokumentų
Pareigūnų funkcijas rodo iš anksto nustatytą numatytąjį prenumeratorių pareigūnų lentelę. Dėl į **registruojant SF** puslapis, apie į **pareigūnų** tab, keičiant pasirašančio asmens vardas ir čempionų titulą pagrindinis dokumentas dėl nurodytų dokumentų tipų:

-   Kliento SF
-   Tiekėjo SF
-   Siuntimo perkėlimo užsakymas
-   Grynųjų užsakymas

**Pastaba:** užregistravus dokumentą, pareigūnai negali būti redaguojami.


