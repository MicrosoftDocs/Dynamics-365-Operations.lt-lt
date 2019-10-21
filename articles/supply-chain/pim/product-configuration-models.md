---
title: Produkto konfigūracijos modelių apžvalga
description: Šiame straipsnyje nurodomos produkto konfigūracijos modeliams svarbios sąlygos ir sąvokos. Naudodami produkto konfigūracijos modelius galite kurti nepatentuotų produktų struktūrą, kurią naudojant galima sukonfigūruoti daug vieno produkto variantų.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 883337979201b3059b301b7aebf9952a70016989
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250627"
---
# <a name="product-configuration-models-overview"></a>Produkto konfigūracijos modelių apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje nurodomos produkto konfigūracijos modeliams svarbios sąlygos ir sąvokos. Naudodami produkto konfigūracijos modelius galite kurti nepatentuotų produktų struktūrą, kurią naudojant galima sukonfigūruoti daug vieno produkto variantų.

Produkto konfigūracijos modeliai yra skirti nepatentuotų produktų struktūrai atvaizduoti. Kai nustatote produkto konfigūracijos modelį, galite sukonfigūruoti atskirą produkto variantą su unikaliomis komplektavimo specifikacijomis ir maršrutu. Produktų konfigūravimo modeliai naudoja tiek deklaratyvius apribojimus, tiek būtinus skaičiavimus, kuriais tvarko ryšius ir apribojimus tarp skirtingų produktų variantų. Galite konfigūruoti pardavimo užsakymų elementus, pardavimo pasiūlymus, pirkimo ir gamybos užsakymus. Šioje lentelėje pateikiami apribojimais pagrįsti terminai ir koncepcijos.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Komponentai</td>
<td>Komponentai yra pagrindiniai produkto konfigūracijos modelio kūrimo blokai. Komponentai rodomi naudojant medžio struktūrą puslapyje <strong>Produkto konfigūravimo pagal apribojimus modelio informacija</strong>. Komponentus gali sudaryti toliau nurodyti elementai.
<ul>
<li>Atributai</li>
<li>Apribojimai</li>
<li>Skaičiavimai</li>
<li>Subkomponentai</li>
<li>Vartotojo reikalavimai</li>
<li>KS eilutės</li>
<li>Maršruto operacijos</li>
</ul></td>
</tr>
<tr class="even">
<td>Atributai</td>
<td>Atributais vadinamos visos produkto konfigūracijos modelio funkcijos. Atributus galite naudoti nurodydami funkcijas, kurias galima pasirinkti, kai sukonfigūruojamas atskiras produktas. Atributai naudojami apribojimuose ir sąlygose. Kai atributai yra sukuriami ir pridedami prie produkto konfigūracijos modelio, nurodomi susiję atributų tipai. Atributui gali būti priskirta numatytoji vertė. Numatytoji vertė yra naudojama konfigūracijos vartotojo sąsajoje (UI), kai konfigūruojamas produkto konfigūracijos modelis. Galite nurodyti, kad atributas yra privalomas, tik skaitomas arba paslėptas.
<ul>
<li><strong>Privaloma</strong> – kai produktas konfigūruojamas, atributui turi būti nustatyta reikšmė.</li>
<li><strong>Tik skaityti</strong> – atributo reikšmė rodoma konfigūracijos seanso metu, tačiau ji negali būti keičiama.</li>
<li><strong>Paslėpta</strong> – atributo reikšmė yra įtraukta į apribojimus ir sąlygas, bet nerodoma konfigūracijos seanso metu.</li>
</ul>
Taip pat galite nurodyti atributo sąlygas. Jei sąlygos įvykdytos, privalomam atributui turi būti įvesta vertė. Sąlygos yra išraiškos, kurias turi atitikti atributai, KS eilutės ir maršruto operacijos, kurios turi būti įtrauktos į produkto konfigūracijos modelį. Bet kuris atributas, kuris yra nurodomas sąlygose, tampa privalomas. Rekomenduojame skirtuke <strong>Atributai</strong> atributus pasirinkti kaip privalomus. Tokiu būdu atpažinti privalomus atributus bus lengviau. Atributo vertės yra svarbios pakartotinai naudojamų konfigūracijų dalys. Atributo reikšmės sistemoje naudojamos siekiant nustatyti, ar konfigūracija atitinka pasirinkimus, kuriuos vartotojas atliko konfigūracijos seanso metu.</td>
</tr>
<tr class="odd">
<td>Atributų tipai</td>
<td>Atributų tipai nustato atributų duomenų tipų rinkinius, kurie naudojami produkto konfigūracijos modelyje. Naudojami toliau nurodyti atributų tipai.
<ul>
<li><strong>Sveikasis skaičius</strong> su intervalu arba be jo</li>
<li><strong>Dešimtainis</strong></li>
<li><strong>Tekstas</strong> su fiksuotu sąrašu arba be jo</li>
<li><strong>Bulio logika</strong></li>
</ul>
Jei atributo tipas yra <strong>Bulio logika</strong>, <strong>Sveikasis skaičius</strong> su intervalu arba <strong>Tekstas</strong> su fiksuotu sąrašu, nustatant produkto konfigūracijos modelį galima naudoti reikšmių rinkinį. <strong>Pastaba.</strong> Produktų konfigūravimo sprendimų priemonė atpažįsta tik šiuos atributų tipus: <strong>Bulio logika</strong>, <strong>Tekstas</strong> su fiksuotu sąrašu ir <strong>Sveikasis skaičius</strong> su intervalu. Todėl tik šių atributų tipai gali būti naudojami išraiškos apribojimuose ir sąlygose.</td>
</tr>
<tr class="even">
<td>Apribojimai</td>
<td>Apribojimais vadinami produkto modelio konfigūracijos apribojimai. Apribojimai naudojami siekiant užtikrinti, kad būtų pasirinktos tik tinkamos reikšmės, kai konfigūruojamas produktas. Apribojimai gali būti išraiškos arba lentelės apribojimai.
<ul>
<li>Išraiškos apribojimai gali būti naudojami tik su susijusiais komponentais. Komponento išraiškos apribojimai gali nurodyti komponento pakomponenčio atributus. Produktų konfigūravimo sprendimų priemonė naudojama siekiant išspręsti apribojimus, ir rašydami apribojimus turite naudoti sprendimų priemonės sintaksę. Daugiau informacijos rasite naudodami temos saitą apie išraiškos apribojimus ir lentelių apribojimus.</li>
<li>Lentelės apribojimai turi būti nurodomi prieš juos taikant produkto konfigūracijos modelio komponentui. Lentelės apribojimai gali būti nustatomi vartotojui arba sistemai. Vartotojo apibrėžtos lentelės apribojimas yra matricos tipas, kuris gali būti naudojamas derinių rinkinio atributo reikšmėms apibūdinti, kurios yra apibrėžiamos atributo tipo. Pavyzdžiui, jei gaminami garsiakalbiai, naudotojo apibrėžto lentelės apribojimo matricoje gali būti stulpeliai, skirti garsiakalbio apdailai ir grotelėms.</li>
</ul>
<strong>Pavyzdys</strong> Garsiakalbių apdailos yra keturios: juoda, ąžuolo, palisandro ir balta. Garsiakalbiai gali turėti vienas iš trijų priekinių grotelių: juodas, metalo arba baltas. Juodos gali būti visos grotelės, tačiau kitos apdailos naudojamos tik tam tikroms grotelėms. Toliau pateiktoje lentelėje rodomas informacijos, rodomos skirtuke <strong>Leistini deriniai</strong>, puslapyje <strong>Redaguoti lentelės apribojimą</strong> pavyzdys.
<table>
<thead>
<tr class="header">
<th>Spintelės apdaila</th>
<th>Priekinės grotelės</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Juoda</td>
<td>Juoda</td>
</tr>
<tr class="even">
<td>Juoda</td>
<td>Metalo</td>
</tr>
<tr class="odd">
<td>Juoda</td>
<td>Balta</td>
</tr>
<tr class="even">
<td>Ąžuolo</td>
<td>Juoda</td>
</tr>
<tr class="odd">
<td>Palisandro</td>
<td>Balta</td>
</tr>
<tr class="even">
<td>Balta</td>
<td>Juoda</td>
</tr>
<tr class="odd">
<td>Balta</td>
<td>Balta</td>
</tr>
</tbody>
</table>
Sistemos apibrėžtas lentelės apribojimas apibūdina sąsają tarp atributo tipo ir lauko „Finance and Operations‟ lentelėje. Sistemos apibrėžtas lentelės apribojimas dinamiškai susieja atributo tipą su lauku. Saitas leidžia atributui produkto konfigūracijos modelyje atspindėti Tiekimo grandinės valdymo lentelės lauko duomenis.</td>
</tr>
<tr class="odd">
<td>Skaičiavimai</td>
<td>Skaičiavimai papildo apribojimus. Skaičiavimą galite naudoti norėdami atlikti tipų <strong>Dešimtainis</strong> ir <strong>Sveikasis skaičius</strong> atributų aritmetines operacijas, susijusias su tipų <strong>Tekstas</strong> su fiksuotu sąrašu ir <strong>Bulio logika</strong> atributais. Skaičiavimas turi paskirties atributą, kuriame bus saugomas skaičiavimo išraiškos rezultatas. Skaičiavimo išraiška kuriama naudojant išraiškų rengyklę.</td>
</tr>
<tr class="even">
<td>Subkomponentai</td>
<td>Pakomponenčius atspindi produktų konfigūracijos modelio medžio struktūra. Pakomponenčius galite naudoti, kad sukurtumėte produkto konfigūracijos modelio struktūrą. Pakomponenčiai suteikia galimybę susieti esamus komponentus. Todėl naudojant pakomponenčius skatinamas pakartotinis komponentų panaudojimas keliuose produkto konfigūracijos modeliuose. Pakomponenčio puslapyje <strong>KS eilutės informacija</strong> galite pasirinkti atskirą pakomponenčio reikšmę. Taip pat gali pasirinkti atributą. kuriam reikšmė buvo parinkta, kai buvo nustatomas produkto konfigūracijos modelis. Kad įtrauktumėte produktą kaip komponentą arba pakomponentį, kai kuriate produktą, puslapyje <strong>Kurti produktą</strong> turite nurodyti toliau pateiktą informaciją.
<ul>
<li>Lauke <strong>Produkto tipas</strong> pasirinkite <strong>Prekė</strong>.</li>
<li>Lauke <strong>Produkto potipis</strong> pasirinkite <strong>Bendrasis produktas</strong>.</li>
<li>Lauke <strong>Konfigūravimo technologija</strong> pasirinkite <strong>Konfigūravimas pagal apribojimus</strong>.</li>
</ul>
Peržiūrėti, ar išleistas produktas gali būti naudojamas kaip komponentas arba pakomponentis, galite peržiūrėti puslapio <strong>Išleisto produkto informacija</strong> skirtuke <strong>Bendra</strong>. Jei lauke <strong>Konfigūravimo technologija</strong> pasirinkta <strong>Konfigūravimas pagal apribojimus</strong>, produktą galima naudoti kaip komponentą ar pakomponentį. Pakomponenčius galite paslėpti, kad konfigūracijos seanso metu jie nebūtų rodomi naudotojui. Atributai, pakomponenčiai ir vartotojo reikalavimai, kurie yra susiję su pakomponenčiais, taip pat paslėpti.</td>
</tr>
<tr class="odd">
<td>Vartotojo reikalavimai</td>
<td>Vartotojo reikalavimai apibūdina abstrakciją tarp vartotojo reikalavimų, tam tikrų komponentų ir atributų. Jūs negalite susieti naudotojo reikalavimo ir prekės. Pavyzdžiui, klientas perka namų kino sistemą. Pardavėjas gali pasiteirauti, koks kliento kambario dydis, kuriame jis planuoja įrengti sistemą, kad nustatytų, kokio galingumo sistema geriausiai atitiktų jo poreikius. Šiame pavyzdyje kambario dydis gali tapti vartotojo reikalavimu, kuris suteiks galimybę nustatyti atitinkamas atributo vertes tam tikram komponentui. Kad konfigūracijos seanso metu vartotojas nematytų reikalavimų, galite juos paslėpti. Atributai, pakomponenčiai ir vartotojo reikalavimai, kurie yra susiję su vartotojo reikalavimais, taip pat paslėpti. Norėdami kontroliuoti arba paslėpti vartotojo reikalavimus, galite įrašyti sąlygą, Sąlyga turi būti įrašyta naudojant optimizavimo modeliavimo kalbos (OML) sintaksę.</td>
</tr>
<tr class="even">
<td>KS eilutės</td>
<td>KS eilutės rodo atskiras komponentų medžiagas produkto konfigūracijos modelyje. Puslapyje <strong>KS eilutės informacija</strong> galima pasirinkti visas prekes. Sąlyga gali būti pridėta į KS eilutę, kad KS eilutės, kurios yra parenkamos atskiram produkto variantui, skirtųsi atsižvelgiant į naudotojo pasirinktį, kai produkto konfigūracijos modelis buvo nustatytas. Sąlygos yra išraiškos, kurias turi atitikti atributai, KS eilutės ir maršruto operacijos, kurios turi būti įtrauktos į produkto konfigūracijos modelį. Puslapyje <strong>KS eilutės informacija</strong> galite pasirinkti atskirą reikšmę. Taip pat galite susieti su atributu, kuriam reikšmė buvo parinkta, kai buvo nustatomas produkto konfigūracijos modelis.</td>
</tr>
<tr class="odd">
<td>Maršruto operacijos</td>
<td>Puslapyje <strong>Maršruto operacijos informacija</strong> galite pasirinkti atskirą reikšmę. Taip pat galite susieti su atributu, kuriam reikšmė buvo parinkta, kai buvo nustatomas produkto konfigūracijos modelis. Sąlygos rašomos kaip išraiškos apribojimai. Sąlygos yra išraiškos, kurias turi atitikti atributai, KS eilutės ir maršruto operacijos, kurios turi būti įtrauktos į produkto konfigūracijos modelį.</td>
</tr>
</tbody>
</table>





