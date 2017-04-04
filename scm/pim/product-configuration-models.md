---
title: "Gaminių konfigūravimo modelių apžvalga"
description: "Šiame straipsnyje apibrėžiama terminų ir sąvokų, kurios yra susijusios su produkto konfigūracijos modelius. Produkto konfigūracijos modeliai leidžia kurti generinį vaistą struktūrą, kad būtų galima sukonfigūruoti daug prekių dimensijų kombinacijoje vieno produkto."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 4031
ms.assetid: 70b968e8-e550-4731-823d-d713b8910f7b
ms.search.region: Global
ms.author: yuyus
ms.dyn365.intro: Feb-16
ms.dyn365.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 15af90d007d77a490db7cb540ef96b4104dbba7e
ms.lasthandoff: 03/31/2017


---

# <a name="product-configuration-models-overview"></a>Gaminių konfigūravimo modelių apžvalga

Šiame straipsnyje apibrėžiama terminų ir sąvokų, kurios yra susijusios su produkto konfigūracijos modelius. Produkto konfigūracijos modeliai leidžia kurti generinį vaistą struktūrą, kad būtų galima sukonfigūruoti daug prekių dimensijų kombinacijoje vieno produkto.

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
Jei atributo tipas yra <strong>Bulio logika</strong>, <strong>Sveikasis skaičius</strong> su intervalu arba <strong>Tekstas</strong> su fiksuotu sąrašu, nustatant produkto konfigūracijos modelį galima naudoti reikšmių rinkinį. <strong>Pastaba:</strong> produkto konfigūracijos problemas pripažįsta tik šių atributų tipų: <strong>Bulio logikos</strong>, <strong>tekstas</strong> su fiksuotame sąraše, ir <strong>sveikojo skaičiaus</strong> su įvairiais. Todėl tik šių atributų tipai gali būti naudojami išraiškos apribojimuose ir sąlygose.</td>
</tr>
<tr class="even">
<td>Apribojimai</td>
<td>Apribojimais vadinami produkto modelio konfigūracijos apribojimai. Apribojimai naudojami siekiant užtikrinti, kad būtų pasirinktos tik tinkamos reikšmės, kai konfigūruojamas produktas. Apribojimai gali būti išraiškos arba lentelės apribojimai.
<ul>
<li>Išraiškos apribojimai gali būti naudojami tik su susijusiais komponentais. Komponento išraiškos apribojimai gali nurodyti komponento pakomponenčio atributus. Produktų konfigūravimo sprendimų priemonė naudojama siekiant išspręsti apribojimus, ir rašydami apribojimus turite naudoti sprendimų priemonės sintaksę. Daugiau informacijos rasite naudodami wiki nuorodą apie išraiškos apribojimus ir lentelių apribojimus.</li>
<li>Kol jie gali būti taikomas produkto konfigūracijos modelio komponentas, reikia apibrėžti lentelės apribojimuose. Lentelės apribojimuose gali būti arba apibrėžta vartotojo, ar sistemos. Vartotojo apibrėžtos lentelės apribojimas yra matricos tipas, kuris gali būti naudojamas derinių rinkinio atributo reikšmėms apibūdinti, kurios yra apibrėžiamos atributo tipo. Pavyzdžiui, jei gaminami garsiakalbiai, naudotojo apibrėžto lentelės apribojimo matricoje gali būti stulpeliai, skirti garsiakalbio apdailai ir grotelėms.</li>
</ul>
<strong>Pavyzdys</strong> Garsiakalbių apdailos yra keturios: juoda, ąžuolo, palisandro ir balta. Garsiakalbiai gali būti viena iš trijų priekinės grotelės: juodos, metalo arba balta. Juoda apdaila yra skirta visų groteles, bet kiti apdailos tik specialios grotelės. Toliau pateiktoje lentelėje rodomas informacijos, rodomos skirtuke <strong>Leistini deriniai</strong>, puslapyje <strong>Redaguoti lentelės apribojimą</strong> pavyzdys.
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
Sistemos lentelės apribojimų atstovauja atributo tipo ir Dynamics "365" dėl operacijų lentelė laukas atvaizdis. Sistemos lentelės apribojimų dinamiškai nuorodos atributo tipo lauką. Nuoroda leidžia produkto konfigūracijos modelis atspindi duomenų lauko Dynamics "365" dėl operacijos stalo atributas.</td>
</tr>
<tr class="odd">
<td>Skaičiavimai</td>
<td>Skaičiavimai yra priedas prie apribojimus. Skaičiavimus galite atlikti aritmetinius veiksmus su atributus, <strong>dešimtainis</strong> ir <strong>sveikojo skaičiaus</strong> rūšys arba loginių operacijų, apimančių atributus, bet ir į <strong>teksto</strong> su fiksuotame sąraše ir <strong>Bulio logikos</strong> tipai. Skaičiavimas turi paskirties atributą, kuriame bus saugomas skaičiavimo išraiškos rezultatas. Skaičiavimo išraiška kuriama naudojant išraiškų rengyklę.</td>
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
<td>Vartotojo reikalavimai apibūdina abstrakciją tarp vartotojo reikalavimų, tam tikrų komponentų ir atributų. Jūs negalite susieti naudotojo reikalavimo ir prekės. Pavyzdžiui, klientas perka namų kino sistemą. Pardavėjas gali pasiteirauti, koks kliento kambario dydis, kuriame jis planuoja įrengti sistemą, kad nustatytų, kokio galingumo sistema geriausiai atitiktų jo poreikius. Šiame pavyzdyje patalpos dydis gali būti naudotojo reikalavimas, kuris padėtų nustatyti tinkamą konkretaus komponento atributo reikšmę. Naudotojo reikalavimus galite paslėpti, kad konfigūracijos seanso metu naudotojui jie nebūtų rodomi. Atributai, pakomponenčiai ir vartotojo reikalavimai, kurie yra susiję su vartotojo reikalavimais, taip pat paslėpti. Norėdami kontroliuoti arba paslėpti vartotojo reikalavimus, galite įrašyti sąlygą, Sąlyga turi būti įrašyta naudojant optimizavimo modeliavimo kalbos (OML) sintaksę.</td>
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




