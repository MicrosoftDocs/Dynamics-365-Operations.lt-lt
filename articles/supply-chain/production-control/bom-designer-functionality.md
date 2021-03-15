---
title: KS kūrimo įrankio funkcija
description: Šioje temoje aprašoma, kaip galite naudoti puslapį KS konstruktorius norėdami projektuoti ir dirbti su komplektavimo specifikacijos (KS) medžio struktūromis.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerSetup, BOMDesignerFilterDialog, BOMDesignerBOMVersion, BOMChangeLine
audience: Application User
ms.reviewer: kamaybac
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 07d74d9e02049447c69edf56eb6860a2cb6dc5c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991895"
---
# <a name="bom-designer-functionality"></a>KS kūrimo įrankio funkcija

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip galite naudoti puslapį KS konstruktorius norėdami projektuoti ir dirbti su komplektavimo specifikacijos (KS) medžio struktūromis. Galite spustelėti Nustatymas norėdami pasirinkti įvairias konfigūracijas ir nurodyti, kokia informacija rodoma medžio eilutėse.

Atidarius puslapį **KS konstruktorius** iš puslapio **Išleisti produktai**, rodoma KS hierarchija tų pasirinktos prekės sąskaitų, kurios yra aktyvios ir patvirtintos, numatytąją prekės užsakymo svetainę ir faktinę datą.  

Norėdami keisti pradinį pasirinktą rodinio elementą, spustelėkite **Filtras** . Nustatydami rodymo principą **Pasirinkta / aktyvi arba Pasirinkta**, galite pasirinkti rodinyje naudoti atskirą KS arba maršruto versijas. Galite pasirinkti, kad nepatvirtintos ir neaktyvios KS versijos būtų rodomos arba prižiūrimos KS konstruktoriuje.  

**Pastaba.** Jei atidarysite KS konstruktorių iš **KS** sąrašo puslapio, maršruto informacija nebus rodoma. Šiuo metu pasirinkta KS arba maršruto versija yra KS ir maršruto versijos ypatybė, ir yra taikoma visiems KS konstruktoriaus egzemplioriams.  

Toliau pateikiamuose skyriuose aprašomos funkcijos, esančios įvairiuose KS konstruktoriaus skirtukuose.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>KS struktūros analizavimas naudojant KS konstruktorių
KS konstruktoriuje yra dvi sekcijos.

-   KS struktūros medžio rodinys.
-   Informacijos sekcija, kurioje rodoma išsami pasirinktų duomenų informacija. Pasirinkus mazgą medžio rodinyje, „FastTab“ išsamios informacijos sekcijoje atnaujinami pagal tą mazgą.
    -   **KS eilutės informacija** – rodoma išsami medžio rodinyje pasirinktos KS eilutės informacija.
    -   **Prekės duomenys** – rodoma išsami pagrindinės prekės arba prekės, naudojamos pasirinktame mazge, informacija. Galite spustelėti **Redaguoti išleistą produktą**, jei norite prižiūrėti pasirinktą prekę.
    -   **KS** – rodoma KS, susijusios su pasirinktu mazgu, antraštė.
    -   **Maršrutas** – rodoma maršruto, susijusio su pasirinktu mazgu, antraštė.
    -   **Maršruto operacijos** – rodo maršruto operacijų peržiūrą. Pažymėjus KS eilutę, priskirtą tam tikrai operacijai, operacija pažymėta kaip **Komponentas, reikalingas atliekant operacijas**.

## <a name="selecting-a-bom-and-route"></a>KS ir maršruto pasirinkimas
KS konstruktoriaus antraštėje rodomas filtras, taikomas KS ir maršrutui. Galite keisti filtrą naudodami dialogo langą **Filtras**. Toliau pateikiamoje lentelėje aprašomi šio dialogo lango laukai.

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
<td>Jei pasirinktas baigtas produktas yra bendrasis produktas, galite nurodyti pagrindines pasirinktas aktyvias produkto dimensijas. <strong>Pastaba.</strong> Atidarius ne&#39; bendrojo produkto KS konstruktorių dialogo lange <strong>Filtras</strong>, produkto dimensijų pasirinkti negalima.</td>
</tr>
<tr class="even">
<td>Svetainė</td>
<td>Pakeiskite svetainę, kuriai rodomas KS medis. Numatytoji svetainė yra numatytoji baigtos prekės atsargų svetainė.</td>
</tr>
<tr class="odd">
<td>Rodymo principas</td>
<td>Pasirinkite versijos rodymo principą, taikomą dabartinei KS struktūrai ir dabartiniam maršrutui.
<ul>
<li>Kai nustatytas principas <strong>Aktyvi arba Pasirinkta / aktyvi</strong>, surandama šią dieną galiojanti KS arba maršruto versija.</li>
<li>Kai nustatytas principas <strong>Pasirinkta / Aktyvi arba pasirinkta</strong>, galite pasirinkti KS versiją arba maršruto versiją spustelėdami <strong>KS</strong> &gt; <strong>KS versijos</strong> arba <strong>Maršrutas</strong> &gt; <strong>Maršruto versijos</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versijos data</td>
<td>Įvesti KS ir maršruto versijos datą. Versija rodo, kuri KS versija naudojama tam tikrą dieną pagal versijų datas KS versijų sąrankoje.</td>
</tr>
<tr class="odd">
<td>Pradinis kiekis</td>
<td>Filtruokite versijas pasirinkdami konkretų pradinį kiekį. Nustačius vertę gali būti pasirinktos kitos KS ir maršruto versijos.</td>
</tr>
<tr class="even">
<td>Rodyti tiktai galiojančius</td>
<td>Pažymėjus žymės langelį medžio struktūroje rodomos tik KS eilutės su tinkamomis datomis. Spustelėti KS eilutę dešiniuoju pelės klavišu arba spustelėkite ją dukart, kad atidarytumėte puslapį <strong>KS eilutės redagavimas</strong>, kuriame matysite tos KS eilutės galiojimo datas.</td>
</tr>
</tbody>
</table>

Naudojant KS konstruktorių KS, kurias sudaro vieno ar kelių lygių fiktyvios eilutės, peržiūrėti arba redaguoti, maršrutas, susietas su aukšto lygio preke, paprastai apima visą KS hierarchiją. Norėdami supaprastinti peržiūrą galite užblokuoti aukščiausio lygio maršrutą ekrane spustelėdami **Peržiūra** &gt; **Blokuoti maršrutą**. Norėdami atblokuoti maršrutą, spustelėkite **Peržiūra** &gt; **Atblokuoti maršrutą**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>KS ir KS eilučių pridėjimas ir redagavimas
KS eilutėms arba KS modifikuoti naudokite funkciją **KS eilutės** arba **KS**. Pasirinkus medžio mazgą, mazgo tipas nustato galimas funkcijas.

| Funkcija                            | aprašymas                                                                                               | Mazgo tipas ir sąlygas                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KS eilutės &gt; Redaguoti                 | Atidarykite dialogo langą, kuriame galite redaguoti KS eilutės atributus.                                             | Šią funkciją galima naudoti, kai KS eilutės mazgas pažymėtas.                                                                                                                                                                                                                                   |
| KS eilutės &gt; Naikinti               | Panaikinkite pasirinktos KS eilutę.                                                                  | Šią funkciją galima naudoti, kai KS eilutės mazgas pažymėtas ir KS nėra užblokuota redaguoti.                                                                                                                                                                                             |
| KS eilutės &gt; Įtraukti prieš eilutę      | Atidarykite dialogo langą, kuriame galite pasirinkti produkto variantą įtraukti prieš pasirinktą KS eilutę.         | Šią funkciją galima naudoti, kai KS eilutės mazgas pažymėtas.                                                                                                                                                                                                                                   |
| KS eilutės &gt; Įtraukti į komponentų KS | Atidarykite dialogo langą, kuriame galite pasirinkti produkto variantą įtraukti pasirinktos KS pabaigoje.       | Šią funkciją galima naudoti, kai pažymėtame mazge yra pasirinkta KS eilutė. Jei šios funkcijos nėra, galbūt nėra pasirinkto prekės varianto KS versijos. Tokiu atveju galite spustelėti **KS** &gt; **Kurti versiją**, kad sukurtumėte pažymėto mazgo trūkstamą versiją. |
| KS eilutės &gt; Įtraukti po eilute       | Atidarykite dialogo langą, kuriame galite pasirinkti produkto variantą įtraukti po pasirinkta KS eilute.          | Šią funkciją galima naudoti, kai KS eilutės mazgas pažymėtas.                                                                                                                                                                                                                                   |
| KS &gt; Kurti versiją             | Sukurkite naują pažymėto mazgo produkto varianto KS versiją arba KS.                             | Šią funkciją galima naudoti, jei KS eilutės mazgas, kuris yra pažymėtas, yra susietas su preke, kurios gamybos tipas yra **KS** arba **Formulė**.                                                                                                                                                  |
| BOM &gt; Skaičiavimas                | Atidarykite dialogo langą, kuriame galėsite vykdyti pasirinkto produkto varianto savikainos arba pardavimo kainos skaičiavimą. | Šią funkciją galima naudoti, kai pažymėtas mazgas yra susijęs su KS versija.                                                                                                                                                                                                         |
| KS &gt; Čekis                      | Patvirtinkite ir patikrinkite pasirinktą KS.                                                                      | Šią funkciją galima naudoti, kai pažymėtas mazgas yra susijęs su KS versija.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Medžio rodinio konfigūravimas
Norėdami tinkinti informaciją, rodomą KS konstruktoriaus medžio rodinyje, spustelėkite **Sąranka**.

| Lauko grupė | Prekės/Paslaugos pavadinimas                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KS         | Pasirinkite kriterijus, kuriuos norite rodyti medžio struktūroje, naudodami žymės langelius. KS konstruktorius rodo pasirinktus kriterijus abiejų skirtukų apačioje. |
| Maršrutas       | Pasirinkite norimus rodyti maršrutų kriterijus naudodami žymės langelius.                                                                                    |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]