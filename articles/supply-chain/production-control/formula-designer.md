---
title: Formulės konstruktorius
description: Šioje temoje paaiškinama, kaip naudoti formulių kūrimo priemonę analizuojant ir tvarkant formules medžio rodinyje.
author: johanhoffmann
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf45fdf44e6d060ee16edf1a6628c5ffd9920dcb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566839"
---
# <a name="formula-designer"></a>Formulės konstruktorius

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip naudoti formulių kūrimo priemonę analizuojant ir tvarkant formules medžio rodinyje.

Kai puslapyje **Išleisti produktai** atidarote puslapį **Formulių kūrimo priemonė**, kairiojoje srityje esančiame medyje rodomas sudėtinių produktų sąrašas ir išleisto produkto ingredientų hierarchija. Struktūra išvedama iš aktyvių ir patvirtintų pasirinktos prekės ir ingredientų, numatytosios prekės užsakymo vietos ir faktinės datos formulių hierarchijos.

Spustelėję **Sąranka** galite pasirinkti įvairias konfigūracijas ir nurodyti, kokia informacija rodoma medžio eilutėse.

Norėdami keisti pradinį pasirinktą rodinio elementą, spustelėkite **Filtras** . Nustatydami rodymo principą **Pasirinkta / aktyvi** arba **Pasirinkta**, galite pasirinkti rodinyje naudoti atskirą formulę arba maršruto versijas. Galite pasirinkti, kad nepatvirtintos ir neaktyvios formulės versijos būtų rodomos arba prižiūrimos formulės konstruktoriuje.  

> [!NOTE]
> Jei puslapį **Formulės konstruktorius** atidarysite iš sąrašo puslapio **Komplektavimo specifikacijos**, maršruto informacija nebus rodoma. Šiuo metu pasirinkta formulė arba maršruto versija taikoma visiems formulės konstruktoriaus egzemplioriams.  

Toliau pateikiamuose skyriuose aprašomos galimos KS konstruktoriaus funkcijos.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Formulės struktūros analizavimas naudojant formulės konstruktorių
Formulės konstruktoriuje yra dvi sekcijos.

-   Formulės struktūros medžio rodinys.
-   Informacijos sekcija, kurioje rodoma išsami pasirinktų duomenų informacija. Pasirinkus mazgą medžio rodinyje, „FastTab“ išsamios informacijos sekcijoje atnaujinami pagal tą mazgą.
    -   **Formulės eilutės informacija** – rodoma išsami medžio rodinyje pasirinktos formulės eilutės informacija.
    -   **Prekės duomenys** – rodoma išsami pagrindinės prekės arba prekės, naudojamos pasirinktame mazge, informacija. Galite spustelėti **Redaguoti išleistą produktą**, jei norite prižiūrėti pasirinktą prekę.
    -   **Formulė** – rodoma formulės, susijusios su pasirinktu mazgu, antraštė.
    -   **Maršrutas** – rodoma maršruto, susijusio su pasirinktu mazgu, antraštė.
    -   **Maršruto operacijos** – rodoma maršruto operacijų peržiūra. Pažymėjus komplektavimo specifikacijos (KS) eilutę, priskirtą tam tikrai operacijai, operacija pažymima kaip **Komponentas, reikalingas atliekant operacijas**.

## <a name="select-a-formula-and-route"></a>Pasirinkite formulę ir maršrutą
Formulės konstruktoriaus antraštėje rodomas filtras, taikomas formulei ir maršrutui. Galite keisti filtrą naudodami dialogo langą **Filtras**. Toliau pateikiamoje lentelėje aprašomi šio dialogo lango laukai.

<table>
<thead>
<tr class="header">
<th>Laukas</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Produktų dimensijos</td>
<td>Jei pasirinktas baigtas produktas yra bendrasis produktas, galite nurodyti pagrindines pasirinktas aktyvias produkto dimensijas. Atkreipkite dėmesį, kad atidarius ne&#39; bendrojo produkto formulės konstruktorių dialogo lange <strong>Filtras</strong> produkto dimensijų pasirinkti negalima.</p></td>
</tr>
<tr class="even">
<td>Svetainė</td>
<td>Pakeiskite svetainę, kuriai rodomas ingrediento medis. Numatytoji svetainė yra numatytoji baigtos prekės atsargų svetainė.</td>
</tr>
<tr class="odd">
<td>Rodymo principas</td>
<td><p>Pasirinkite versijos rodymo principą, kuris taikomas dabartinei formulės struktūrai ir dabartiniam maršrutui.</p>
<ul>
<li>Kai nustatytas principas <strong>Aktyvi</strong> arba <strong>Pasirinkta / aktyvi</strong>, surandama šią dieną galiojanti formulė arba maršruto versija.</li>
<li>Kai nustatytas principas <strong>Pasirinkta / Aktyvi</strong> arba <strong>Pasirinkta</strong>, spustelėdami <strong>Formulė</strong> &gt; <strong>Formulės versijos</strong> arba <strong>Maršrutas</strong> &gt; <strong>Maršruto versijos</strong> galite pasirinkti formulės versiją arba maršruto versiją.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versijos data</td>
<td>Įveskite formulės ir maršruto versijos datą. Versija rodo, kuri formulės versija naudojama tam tikrą dieną pagal versijų datas formulės versijų sąrankoje.</td>
</tr>
<tr class="odd">
<td>Pradinis kiekis</td>
<td>Filtruokite versijas pasirinkdami konkretų pradinį &quot;kiekį&quot; („nuo“). Nustačius vertę gali būti pasirinktos kitos formulės ir maršruto versijos.</td>
</tr>
<tr class="even">
<td>Rodyti tiktai galiojančius</td>
<td>Pažymėjus žymės langelį medžio struktūroje rodomos tik tos formulės eilutės, kurių datos tinkamos. Spustelėkite formulės eilutę dešiniuoju pelės klavišu arba spustelėkite ją dukart, kad atidarytumėte puslapį <strong>Formulės eilutės redagavimas</strong>, kuriame matysite tos formulės eilutės galiojimo datas.</td>
</tr>
</tbody>
</table>

Naudojant formulės konstruktorių formulėms, kurias sudaro vieno ar kelių lygių fiktyvios eilutės, peržiūrėti arba redaguoti, maršrutas, susietas su aukšto lygio preke, paprastai apima visą formulės hierarchiją. Norėdami supaprastinti peržiūrą galite užblokuoti aukščiausio lygio maršrutą ekrane spustelėdami **Peržiūra** &gt; **Blokuoti maršrutą**. Norėdami atblokuoti maršrutą, spustelėkite **Peržiūra** &gt; **Atblokuoti maršrutą**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Formulių ir formulių eilučių įtraukimas ir redagavimas
Formulių eilutėms arba formulėms modifikuoti naudokite funkciją **Formulės eilutės** arba **Formulė**. Pasirinkus medžio mazgą nuo mazgo tipo priklausys galimos funkcijos.

| Funkcija                            | aprašymas                                                                                               | Mazgo tipas ir sąlygas |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| KS eilutės &gt; Redaguoti                 | Atidarykite dialogo langą, kuriame galite redaguoti formulės eilutės atributus.                                         | Šią funkciją galima naudoti, kai formulės eilutės mazgas pažymėtas. |
| KS eilutės &gt; Naikinti               | Panaikinkite pasirinktos formulės eilutę.                                                          | Šią funkciją galima naudoti, kai formulės eilutės mazgas pažymėtas ir formulė nėra užblokuota redaguoti. |
| KS eilutės &gt; Įtraukti prieš eilutę      | Atidarykite dialogo langą, kuriame galite pasirinkti produkto variantą įtraukti prieš pasirinktą formulės eilutę.     | Šią funkciją galima naudoti, kai formulės eilutės mazgas pažymėtas. |
| KS eilutės &gt; Įtraukti į komponentų KS | Atidarykite dialogo langą, kuriame galite pasirinkti produkto variantą įtraukti pasirinktos formulės pabaigoje.   | Šią funkciją galima naudoti, kai pažymėtame mazge yra pasirinkta formulės eilutė. Jei šios funkcijos nėra, galbūt nėra pasirinkto prekės varianto formulės versijos. Tokiu atveju spustelėję **Formulė** &gt; **Kurti versiją** galite sukurti pažymėto mazgo trūkstamą versiją. |
| KS eilutės &gt; Įtraukti po eilute       | Atidarykite dialogo langą, kuriame galite pasirinkti produkto variantą įtraukti po pasirinktos formulės eilutės.      | Šią funkciją galima naudoti, kai formulės eilutės mazgas pažymėtas. |
| Formulė &gt; Kurti versiją         | Sukurkite naują pažymėto mazgo produkto varianto formulės versiją arba formulę.                     | Šią funkciją galima naudoti, jei formulės eilutės mazgas, kuris yra pažymėtas, yra susietas su preke, kurios gamybos tipas yra **KS** arba **Formulė**. |
| Formulė &gt; Skaičiavimas            | Atidarykite dialogo langą, kuriame galėsite vykdyti pasirinkto produkto varianto savikainos arba pardavimo kainos skaičiavimą. | Šią funkciją galima naudoti, kai pažymėtas mazgas yra susijęs su formulės versija. |
| Formulė &gt; Tikrinti                  | Patvirtinkite ir patikrinkite pasirinktą formulę.                                                                  | Šią funkciją galima naudoti, kai pažymėtas mazgas yra susijęs su formulės versija. |

## <a name="configuring-the-tree-view"></a>Medžio rodinio konfigūravimas
Norėdami tinkinti informaciją, rodomą formulės konstruktoriaus medžio rodinyje, spustelėkite **Sąranka**.


| Lauko grupė |                                                                          aprašymas                                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     KS     | Pasirinkite kriterijus, kuriuos norite rodyti medžio struktūroje, naudodami žymės langelius. Formulės konstruktorius pasirinktus kriterijus rodo abiejų skirtukų apačioje. |
|    Maršrutas    |                                           Pasirinkite norimus rodyti maršrutų kriterijus naudodami žymės langelius.                                           |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]