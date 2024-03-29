---
title: Mobiliųjų įrenginių nustatymas darbui sandėlyje
description: Šiame straipsnyje aprašoma, kaip konfigūruoti meniu elementus, kuriuos sandėlio darbuotojai naudoja dirbdami mobiliuoju įrenginiu.
author: Mirzaab
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem, WHSRFSysDirSort, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef392fd744a68c54bc0438152b3487233ac5c7f3
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070356"
---
# <a name="set-up-mobile-devices-for-warehouse-work"></a>Mobiliųjų įrenginių nustatymas darbui sandėlyje

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti meniu elementus, kuriuos sandėlio darbuotojai naudoja dirbdami mobiliuoju įrenginiu.

> [!NOTE]
> Šis straipsnis taikomas sandėlio valdymo funkcijoms. Jis netaikomas atsargų valdymo funkcijoms. Sandėlio mobiliojo įrenginio meniu rodomi meniu elementai yra sukonfigūruoti puslapyje **Mobiliojo įrenginio meniu elementai**. Kadangi meniu elementus galima įtraukti į skirtingus meniu, lengva sukonfigūruoti meniu struktūras, kad tam tikri vartotojai susidurtų tik su konkrečių tipų darbais. Galite konfigūruoti meniu elementus norėdami atlikti šias užduotis:

- Apdoroti užklausą arba vykdyti veiklą, pvz., spausdinti žymę, generuoti numerių lenteles, paleisti gamybos užsakymą arba greitai peržvelgti informaciją apie vietoje esančias prekes.
- Kurti darbą, kuris bus atliekamas kitame procese. Pavyzdžiui, pirkimo užsakymo prekės gavimas gali sukurti atidėjimo darbą kitam darbuotojui.
- Atlikti darbą, kuris buvo sukurtas kito proceso (esamą darbą), pvz., atidėjimo darbo, sukurto gavus prekę pagal pirkimo užsakymą.

Norėdami kurti veiklos ar užklausos meniu elementą, nustatykite lauko **Režimas** vertę į **Netiesioginis**. Tada tampa galimas parinkčių **Veiklos kodas** sąrašas, kad galėtumėte pasirinkti užklausą arba veiklą, kuriai skirtas meniu elementas. Norėdami sukurti meniu elementą sandėlio darbui generuoti, nustatykite lauko **Režimas** vertę į **Darbas**. Taps galimas parinkčių **Darbo kūrimo procesas** sąrašas. Norėdami sukurti meniu elementą siekiant apdoroti esamą sandėlio darbą, nustatykite lauko **Režimas** vertę į **Darbas**, tada nustatykite parinkties **Naudoti esamą darbą** vertę **Taip**. 

> [!NOTE]
> Gali būti galimi papildomi meniu elementų laukai, atsižvelgiant į pasirinktą meniu elementą ir tai, ar meniu elementas naudojamas norint atlikti esamą darbą. Informacijos apie papildomų laukų pasirinktis žr. šio straipsnio skyriuje „Papildomos meniu elementų parinktys“.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Veiklų ir užklausų meniu elementų konfigūravimas

Jei meniu elemento laukas **Režimas** nustatytas kaip **Netiesioginis**, galite sukurti meniu elementą, kad būtų galima atlikti bendrą veiklą arba užklausą, kuri nekuria darbo. Tokios veiklos pavyzdžiai gali būti pakartotinis numerio lentelių žymių spausdinimas ir užklausa dėl vietoje esančių prekių. Toliau pateiktoje lentelėje nurodytos galimos parinktys.

| Parinktis | Prekės/Paslaugos pavadinimas |
|---|---|
| Nėra | Ši numatytoji reikšmė neįgalina veiklos ar užklausos. |
| Apie | Peržiūrėkite informaciją apie sistemą, pvz., versijos numerį, sandėlio ID ir koks darbuotojas tuo metu yra prisijungęs. |
| Keisti sandėlį | Pakeiskite sandėlį, prie kurio prisijungęs darbuotojas. |
| Vietos užklausa | Peržiūrėkite informaciją apie visas vietoje esančias prekes ir kiekius. |
| Numerio lentelės užklausa | Peržiūrėkite prekių kiekį numerio lentelėje ir numerio lentelės vietą. |
| Pradėti gamybos užsakymą | Paleiskite gamybos užsakymą. |
| Gamybos nurašymas | Įveskite atliekų, sukurtų vykdant kiekvienos komplektavimo specifikacijos (KS) eilutės gamybą, kiekį. |
| Paskutinis produkcijos padėklas | Nurodykite, kad gamybos užsakymui buvo pagamintas paskutinis prekių padėklas ir kad reikia atnaujinti gamybos užsakymo būseną nurodant ją kaip **Paskelbta, kad užbaigta**. Grąžinama gamybos metu nepanaudotų žaliavų būsena iš **Paimta** į **Užsakyta**, o prekes galima grąžinti į atsargas. |
| Prekės užklausa | Nuskaitykite prekę ir nustatykite, kurioje sandėlio vietoje ji yra. Ši užklausa pateikia visas nuskaitytos prekės vietas ir kiekius. |
| Spausdinti žymą iš naujo | Perspausdinkite numerio lentelės žymę. |
| Numerio lentelės versija | Kurkite pirminę numerio lentelę sujungdami kelias toje pačioje vietoje esančias numerių lenteles. Ši parinktis naudinga perkeliant kelias numerių lenteles vienu metu. Kai perkeliama pirminė numerio lentelė, prieš išrenkant prekes iš kiekvienos numerio lentelės reikia suskaidyti numerio lentelę. <p></p>**Patarimas.** Norėdami perkelti pirminę numerio lentelę, turite naudoti mobilųjį įrenginį, konfigūruotą kurti perkėlimo darbus. |
| Numerio lentelių grupavimas | Suskaidykite sudėtinę numerio lentelę, kad galėtumėte išrinkti prekes iš ją sudarančių numerių lentelių. |
| Vairuotojo registravimas | Jei naudojate modulį Transportavimo valdymas, užregistruokite vairuotojo atvykimą nuskaitydami siunčiamo krovinio ID, paskyros ID arba siuntos ID. Norint naudoti šią parinktį krovinį reikia priskirti paskyrai, o krovinio būsena turi būti **Pakrauta**. |
| Vairuotojo išregistravimas | Užregistruokite, kad vairuotojas baigė savo paskyrimą. |
| Valyti numeravimo talpyklą | Naikinkite numeracijos numerius iš numeracijos talpyklos. Šią veiklą paprastai atlieka sistemos administratorius šalindamas kaupimo talpykloje problemas, kai naudojami mobilieji įrenginiai. |
| Keisti paketo perdavimą | Leiskite darbuotojui nurodyti prekės paketo perdavimo kodą ir paketą. Ši pasirinktis atnaujina nurodytą paketo perdavimo kodą. |
| Rodyti atidarytą užduočių sąrašą | Rodyti galimų darbų sąrašą tam tikram vartotojui. Tada vartotojas galės pasirinkti atliktiną darbą ir bus nukreiptas į jį. Šis sąrašas skirtas žiūrėti planšetiniuose įrenginiuose, kurių ekrano įstrižainė – 7 coliai ar daugiau. Jums pasirinkus šią parinktį, tampa galimi meniu elementai **Redaguoti užklausą** ir **Laukų sąrašas**. Puslapyje **Redaguoti užklausą** galima nustatyti darbo, rodomo sąraše, kriterijus. Puslapyje **Laukų sąrašas** galima pasirinkti darbų sąraše rodomus laukus. Pavyzdžiui, galima sumažinti rodomų laukų skaičių, kad vartotojas galėtų greičiau pažymėti tinkamiausią darbo elementą. „FastTab“ skirtuko **Bendra** lauke **Įrašų puslapyje** taip pat galima pasirinkti, kiek darbo įrašų rodoma viename puslapyje. Jei pažymėta parinktis **Leisti vartotojams filtruoti darbą pagal operacijos tipą**, darbų sąraše bus rodomas valdiklis **Filtruoti darbą**, kurį naudodamas vartotojas gali filtruoti darbą pagal operacijos tipą. Vartotojas darbų sąraše matys tik tuos darbus, prie kurių prieiti jis turi teisę. Reikia įsitikinti, kad vartotojai turi teisę prieiti prie vieno ar daugiau vartotojo nurodytų meniu elementų, kurie palaiko konkrečius darbo klasės tipus, prie kurių jie galėtų prieiti. Teisės taip pat patikrinamos, kai vartotojas mėgina atlikti darbą iš sąrašo.|
| Kurti perkėlimo užsakymą iš numerio lentelių | Tai leidžia sandėlio darbuotojams kurti ir apdoroti perkėlimo užsakymus tiesiai iš sandėlio valdymo mobiliųjų įrenginių programėlės. Sandėlio darbuotojai pirmiausia pasirenka paskirties sandėlį, o tada gali nuskaityti vieną ar daugiau numerio lentelių naudodami programą. Kai sandėlio darbuotojas pasirenka **Užbaigti užsakymą**, paketinė užduotis sukuria reikiamą perkėlimo užsakymą ir užsakymo eilutes pagal turimas atsargas, užregistruotas toms numerio lentelėms. Daugiau informacijos žr. [Perkėlimo užsakymų kūrimas iš sandėlio programos](create-transfer-order-from-warehouse-app.md)

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Meniu elementų konfigūravimas siekiant kurti darbą kitam darbuotojui ar procesui

Galite nustatyti meniu elementą, kuris kuria darbą kitam darbuotojui, kai mobiliajame įrenginyje bus atliktas pradinis veiksmas. Pavyzdžiui, kai vienas darbuotojas naudoja mobilųjį įrenginį prekei priimti, kitam darbuotojui sukuriamas atidėjimo darbas. Norėdami nustatyti meniu elementą, kuris sukuria darbą, puslapio **Mobiliojo įrenginio meniu elementai** lauke **Režimas** pasirinkite **Darbas**. Toliau pateiktoje lentelėje lauko **Darbo kūrimo procesas** parinktys grupuojamos pagal darbo užsakymo tipą.

<table>
<tbody>
<tr>
<th>Darbo užsakymo tipas</th>
<th>Parinktis</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
<tr>
<td rowspan="8">Pirkimo užsakymas</td>
<td>Gaunama pirkimo užsakymo eilutė</td>
<td>Registruokite prekės kiekio gavimą naudodami pirkimo užsakymo numerį ir pirkimo užsakymo eilutės numerį bei kurkite atidėjimo darbą kitam darbuotojui.</td>
</tr>
<tr>
<td>Gaunama ir atidedama pirkimo užsakymo eilutė</td>
<td>Registruokite prekės kiekio gavimą naudodami pirkimo užsakymo numerį ir pirkimo užsakymo eilutės numerį bei atidėkite prekes. Abu veiksmus atlieka tas pats darbuotojas.</td>
</tr>
<tr>
<td>Gaunama pirkimo užsakymo prekė</td>
<td>Registruokite prekės kiekio gavimą pagal pirkimo užsakymą užregistruodami pirkimo užsakymo eilutės numerį ir prekės numerį bei kurkite atidėjimo darbą kitam darbuotojui.</td>
</tr>
<tr>
<td>Pirkimo užsakymo prekės gavimas ir atidėjimas</td>
<td>Registruokite pirkimo užsakymo prekės kiekio gavimą registruodami pirkimo užsakymo numerį ir atidėkite prekę. Abu veiksmus atlieka tas pats darbuotojas.</td>
</tr>
<tr>
<td>Gaunama numerio lentelė</td>
<td>Priimkite gaunamą išankstinį siuntimo pranešimą (ASN) naudodami numerio lentelės ID.</td>
</tr>
<tr>
<td>Numerio lentelės gavimas ir atidėjimas</td>
<td>Priimkite ir atidėkite gaunamą išankstinį siuntimo pranešimą (ASN) naudodami numerio lentelės ID.</td>
</tr>
<tr>
<td>Krovinio prekės gavimas</td>
<td>Registruokite krovinio kiekio gavimą naudodami krovinio ID ir sukurkite atidėjimo darbą kitam darbuotojui. Prekės numeris ir produkto dimensijos atitinka gavimą pagal pirkimo užsakymo eilutes.</td>
</tr>
<tr>
<td>Krovinio prekės gavimas ir atidėjimas</td>
<td>Registruokite krovinio gavimą naudodami krovinio ID ir atidėkite prekes. Prekės numeris ir produkto dimensijos atitinka gavimą pagal pirkimo užsakymo eilutes. Abu veiksmus atlieka tas pats darbuotojas.</td>
</tr>
<tr>
<td rowspan="2">Grąžinimo užsakymas</td>
<td>Grąžinimo užsakymo gavimas</td>
<td>Registruokite prekės kiekio gavimą registruodami RMA numerį ir sukurkite atidėjimo darbą kitam darbuotojui.</td>
</tr>
<tr>
<td>Grąžinimo užsakymo gavimas ir atidėjimas</td>
<td>Registruokite prekės kiekio gavimą registruodami RMA numerį ir atidėkite prekes. Abu veiksmus atlieka tas pats darbuotojas.</td>
</tr>
<tr>
<td rowspan="6">Perkėlimo užsakymas</td>
<td>Gaunama perkėlimo užsakymo prekė</td>
<td>Registruokite prekės kiekio gavimą ir sukurkite atidėjimo darbą kitam darbuotojui.

<strong>Pastaba:</strong> naudokite šią pasirinktį tik jei prekės buvo išsiųstos iš sandėlio, kuris neįgalintas naudoti sandėlio valdymo procesuose (WMS).</td>
</tr>
<tr>
<td>Perkėlimo užsakymo prekės gavimas ir atidėjimas</td>
<td>Registruokite prekės kiekio gavimą ir atidėkite prekes. Abu veiksmus atlieka tas pats darbuotojas.

<strong>Pastaba:</strong> naudokite šią pasirinktį tik jei prekės buvo išsiųstos iš sandėlio, kuris neįgalintas naudoti sandėlio valdymo procesuose (WMS).</td>
</tr>
<tr>
<td>Gaunama perkėlimo užsakymo eilutė</td>
<td>Registruokite prekės kiekio gavimą ir sukurkite atidėjimo darbą kitam darbuotojui.</td>
</tr>
<tr>
<td>Perkeliama ir atidedama pirkimo užsakymo eilutė</td>
<td>Registruokite prekės kiekio gavimą ir atidėkite prekes. Abu veiksmus atlieka tas pats darbuotojas.</td>
</tr>
<tr>
<td>Gaunama numerio lentelė</td>
<td>Priimkite gaunamą išankstinį siuntimo pranešimą (ASN) naudodami numerio lentelės ID.</td>
</tr>
<tr>
<td>Numerio lentelės gavimas ir atidėjimas</td>
<td>Priimkite ir atidėkite gaunamą išankstinį siuntimo pranešimą (ASN) naudodami numerio lentelės ID.</td>
</tr>
<tr>
<td rowspan="4">Gamyba</td>
<td>Skelbti baigtu</td>
<td>Registruokite pabaigtos prekės, baigtos gamybai, kiekį ir sukurkite atidėjimo darbą kitam darbuotojui. Šis kiekis gali būti visas suplanuotas gamybos kiekis arba jo dalis.</td>
</tr>
<tr>
<td>Ataskaita, kaip baigta ir atidėta</td>
<td>Registruokite baigtos prekės kiekį, kuris buvo baigtas gamybai, ir atidėkite prekes. Šis kiekis gali būti visas suplanuotas gamybos kiekis arba jo dalis. Abu veiksmus atlieka tas pats darbuotojas.</td>
</tr>
<tr>
<td>„Kanban“</td>
<td>Nurodykite, kad „kanban“ yra baigtas, ir sukurkite atidėjimo darbą kitam darbuotojui.</td>
</tr>
<tr>
<td>„Kanban“ atidėtas</td>
<td>Nurodykite, kad „kanban“ yra baigtas, ir atidėkite prekes. Abu veiksmus atlieka tas pats darbuotojas.</td>
</tr>
<tr>
<td rowspan="5">Atsargos</td>
<td>Perkėlimas</td>
<td>Registruokite, kad prekės buvo perkeltos iš vienos vietos į kitą. Darbuotojas nurodo vietą, iš kurios prekės buvo perkeltos, ir vietą, į kurią jos buvo perkeltos.</td>
</tr>
<tr>
<td>Sulaikymas</td>
<td>Pakeiskite turimų atsargų būseną numerio lentelėje arba vietoje, kad sugadintos arba trūkstamos atsargų prekės būtų nepasiekiamos.</td>
</tr>
<tr>
<td>Judėjimas pagal šabloną</td>
<td>Perkelkite prekes iš vienos vietos į kitą pusiau automatiniu būdu. Darbuotojas pasirenka vietą, iš kurios reikia perkelti prekes, o sistema naudodama vietos nurodymą nustato, kur prekes reikia perkelti.</td>
</tr>
<tr>
<td>Ilgalaikio turto perkėlimas</td>
<td>Registruokite, kad prekės buvo perkeltos iš vieno sandėlio į kitą. Šiai parinkčiai reikia, kad darbuotojui būtų leidžiama dirbti abiejuose sandėliuose.

<strong>Pastaba.</strong> Šiam meniu elementui reikia numatytojo atsargų pervedimo žurnalo, kurio lauko <strong>Kvito išrašymas</strong> vertė nustatyta kaip <strong>Registravimas</strong>.</td>
</tr>
<tr>
<td>Numerio lentelės įkėlimas</td>
<td>Naudokite šią parinktį, kai nustatote&#39; savo sandėlį pirmą kartą. Nuskaitykite visas numerių lenteles visose sandėlio vietose. Tokios vietos turi būti kontroliuojamos numerio lentelių. Šios parinkties naudoti negalite&#39;, jei atsargų rezervavimo hierarchijoje <strong>Serijos numeris</strong> arba <strong>Paketo numeris</strong> yra aukščiau už <strong>Vieta</strong>.</td>
</tr>
<tr>
<td rowspan="3">Ciklo skaičiavimas</td>
<td>Koregavimo taikymas</td>
<td>Didinkite prekių kiekį atsargose. Nurodykite vietą, numerio lentelę, prekę, kiekį, matavimo vienetą ir būseną.</td>
</tr>
<tr>
<td>Koregavimas atšaukimas</td>
<td>Mažinkite prekių kiekį atsargose. Nurodykite atsargų vietą, numerio lentelę, prekę, kiekį, matavimo vienetą ir būseną.</td>
</tr>
<tr>
<td>Atrinkti ciklo skaičiavimą</td>
<td>Paleiskite skaičiavimą vietoje. Darbuotojas turi suskaičiuoti visas vietoje esančias prekes. Jei skaičiavimo rezultatas yra mažesnis nei lauktas kiekis, trūkstamas kiekis laikomas nuostoliu.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Meniu elementų konfigūravimas esamam darbui apdoroti
Be meniu elementų sandėlio darbams kurti nustatymo, galite nustatyti meniu elementus darbui, kuris jau sukurtas, apdoroti. Nustatykite lauko **Režimas** vertę į **Darbas** ir pasirinkite parinktį **Naudoti esamą darbą**. Skirtuke **Bendra** tampa galimos papildomos galimybės. Galite valdyti prieigą prie meniu elemento priskirdami vieną ar daugiau darbo klasių „FastTab“ skirtuke **Darbo klasė**. Darbo klasės apibrėžia darbą, kurį galima apdoroti naudojantis meniu elementu. Darbo klases taip pat galima naudoti siekiant suteikti prieigą prie konkretaus vartotojo vaidmenų arba atskirti skirtingų tipų operacijų vykdymą. Toliau pateiktoje lentelėje aprašomos galimos parinktys. Parinktį galima pasirinkti puslapio **Mobiliojo įrenginio meniu elementai** lauke **Nukreipė**. 

<table>




<thead>
<tr class="header">
<th>Parinktis</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nėra</td>
<td>Pagal šią numatytąją reikšmę&#39; darbas neapdorojamas.</td>
</tr>
<tr class="even">
<td>Sistemos nurodyta</td>
<td>„Supply Chain Management“ valdo darbo, priskirto darbuotojui, tipą ir tvarką, kuria darbuotojas atlieka darbą. Kai pasirenkate šią parinktį, veiksmų srityje galite pasirinkti <strong>Sistemos nurodytas darbas</strong>, kad atidarytumėte puslapį <strong>Sistemos nurodyta rikiavimo tvarka</strong>, kuriame galite nustatyti darbo rūšiavimo kriterijus. Rūšiavimo kriterijai kontroliuoja tvarką, kuria darbuotojas atlieka darbą. Galite pridėti tiek kriterijų, kiek reikia.</td>
</tr>
<tr class="odd">
<td>Vartotojo nurodyta</td>
<td>Darbuotojas pasirenka darbą, kuris bus atliekamas, ir tvarką, kuria jį reikia atlikti.</td>
</tr>
<tr class="even">
<td>Vartotojų grupavimas</td>
<td>Darbuotojas grupuoja darbus rankiniu būdu. Ši parinktis naudinga, kai, pavyzdžiui, darbuotojas vietoje gali išrinkti kelias prekes vienu metu. Baigęs visų reikiamų prekių išrinkimą, darbuotojas gali atidėti prekes.</td>
</tr>
<tr class="odd">
<td>Sistemos grupavimas</td>
<td>„Supply Chain Management“ grupuoja darbuotojo darbus pagal nurodytą lauką. Pavyzdžiui, išrinkimo darbai grupuojami, kai darbuotojas nuskaito siuntos ID, krovinio ID ar bet kokią reikšmę, kuri gali susieti kiekvieną darbo vienetą. Jei pasirenkate šią parinktį, būtini yra šie laukai:
<ul>
<li><strong>Sistemos grupavimo laukas</strong> – pasirinkite lauką, kurį darbuotojas nuskaito norėdamas grupuoti darbus.</li>
<li><strong>Sistemos grupavimo žyma</strong> – įveskite tekstą, nurodantį darbuotojui, ką reikia nuskaityti norint grupuoti darbus.</li>
</ul></td>
</tr>
<tr class="even">
<td>Patikrinta vartotojo nurodymu</td>
<td>Darbuotojas pasirenka darbą, kurį reikia atlikti, kai darbas susietas su didesniu objektu, pvz., kroviniu arba siunta. Darbuotojas nustato tvarką, kuria išrenkamos prekės. Jei pasirenkate šią parinktį, būtini yra šie laukai:
<ul>
<li><strong>Patikrintas vartotojo nurodymu laukas</strong> – pasirinkite lauką, kurį darbuotojas nuskaito norėdamas grupuoti darbus.</li>
<li><strong>Patikrinta vartotojo nurodymu žymė</strong> – įvesdami tekstą nurodykite darbuotojui, ką reikia nuskaityti, kai išrinkimo darbus grupuoja sistema.</li>
</ul>
Ši parinktis naudinga, kai, pavyzdžiui, kroviniui išdėstyti keli padėklai. Jei lauke <strong>Patikrinta vartotojo nurodymu</strong> pasirinksite <strong>LoadId</strong>, darbuotojas galės išrinkti bet kokį su kroviniu susietą padėklą. Darbuotojui pateikiamas klaidos pranešimas, jei jis nuskaito prekę, nesusietą&#39; su kroviniu.</td>
</tr>
<tr class="odd">
<td>Klasterio paėmimas</td>
<td>Darbuotojas grupuoja darbus į klasterius. Klasteriai suteikia darbuotojui galimybę išrinkti prekes iš vienos vietos keliems darbo užsakymams vienu metu.</td>
</tr>
<tr class="even">
<td>Ciklo skaičiavimo grupavimas</td>
<td>Darbuotojas pasirenka zoną, darbo telkinį arba vietą, o „Supply Chain Management“ paskirsto darbus pagal pasirinkimą. Jei pasirinksite šią parinktį, veiksmo srityje galėsite spustelėti <strong>Ciklo skaičiavimas</strong> ir nurodyti papildomą rodytiną informaciją. Taip pat galite nurodyti, kiek kartų darbuotojas turi kartoti skaičiavimą, jei randama skirtumų.</td>
</tr>
 <tr class="odd">
<td>Transportuojamų krovinių krovimas</td>
<td>Naudodamiesi šia funkcija keli sandėlio darbuotojai vieno arba kelių visiškai arba iš dalies išsiųstų krovinių atsargas gali krauti į tą patį sunkvežimį arba į skirtingus sunkvežimius.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Papildomos meniu elementų parinktys
Puslapyje **Mobiliojo įrenginio meniu elementai** galimos papildomos meniu elementų parinktys. Pasirinktys gali skirtis, atsižvelgiant į procesą, kuriam konfigūruojate meniu elementą. 

Pateiktoje lentelėje aprašomos šios pasirinktys.

<table>




<thead>
<tr class="header">
<th>Laukas</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Leisti skaidyti darbą</td>
<td>Pasirinkę šią parinktį leisite vartotojams dėti darbo užsakymo prekes į daugiau nei vieną paskirties numerio lentelę. Ši parinktis naudinga, jei, pavyzdžiui, paskirties numerio lentelė yra pilna ir darbuotojas turi įtraukti likusias prekes į kitą numerio lentelę. Pasirinkdamas <strong>Pilnas</strong> darbuotojas gali nurodyti, kad numerio lentelė yra pilna, ir sustabdyti išrinkimo darbų gavimą joje. Tada rodoma išrinktų prekių padėjimo vieta, o jau atliktas išrinkimo darbas perkeliamas į naują darbo užsakymą. Likę paskirties numerio lentelės išrinkimo darbai lieka pradiniame darbo užsakyme.</td>
</tr>
<tr class="even">
<td>Fiksavimas</td>
<td>Pasirinkę šią parinktį leisite darbuotojams nurodyti vietą, kuri perrašo siūlomą išdėstymo arba pakrovimo vietą. Visi likę atidėjimo darbai nukreipiami į naująją vietą. Ši parinktis naudinga, jei, pavyzdžiui, darbuotojas, kuris turi padėti 1 užsakymo prekes į išdėstymo vietą prie 1 rampos, to atlikti negali, nes iš tos vietos dar nepašalintas pirmesnis krovinys. Užuot laukęs, kol atsilaisvins išdėstymo vieta 1 rampoje, darbuotojas gali nuspręsti naudoti išdėstymo vietą 2 rampoje. Tokiu atveju darbuotojas perrašo siūlomą išdėstymo vietą. Tada visų likusių darbo užsakymo prekių padėjimo vieta pakeičiama į 2 rampos išdėstymo vietą. Jei pasirinksite šią pasirinktį, turite nustatyti lauką <strong>Užfiksavęs asmuo</strong>.</td>
</tr>
<tr class="odd">
<td>Užfiksavęs asmuo</td>
<td>Jei naudojate&#39; fiksavimo funkciją, reikia nurodyti, ar fiksuoti pagal siuntą, ar pagal krovinį.</td>
</tr>
<tr class="even">
<td>Audito šablono ID</td>
<td>Pasirinkite darbo audito šabloną, kuris pertrauks šio meniu elemento darbo procesą, kad būtų galima atlikti kitą operaciją. Pavyzdžiui, jei šis meniu elementas skirtas gaunamam darbui, audito šablone gali būti reikalaujama, kad darbuotojas tikrintų temperatūrą pristatymo konteineryje. Taškas, kai procesas pertraukiamas, nurodytas audito šablone. Šis taškas gali būti, pvz., darbo pradžia ar pabaiga arba laikas, kai pasikeičia jo būsena.</td>
</tr>
<tr class="odd">
<td>Klasterio šablono ID</td>
<td>Pasirinkite klasterio profilį, kuris bus naudojamas klasterio išrinkimui. Tarp galimų klasterio profilio parametrų galima nurodyti, ar reikia kurti klasterius automatiškai, kokie darbo vienetų, kuriuos galima jam priskirti, padėčių pavadinimai, kada reikia skaidyti klasterius į atskirus vienetus ir ar reikia tikrinti. Šis laukas galimas tik lauke <strong>Nukreipė</strong> pasirinkus <strong>Klasterio paėmimas</strong>.</td>
</tr>
<tr class="even">
<td>Pirmiausia apskaičiuoti bendrą prekių kiekį</td>
<td>Pasirinkite šią parinktį, jei norite, kad skaičiuodamas darbuotojas iš pradžių privalėtų skaičiuoti visą kiekį. Jei aptinkamas skirtumas, darbuotojas turi suteikti daugiau informacijos, pvz., nurodyti numerio lentelės numerį, paketo numerį ir serijos numerius.</td>
</tr>
<tr class="odd">
<td>Kurti perkėlimą</td>
<td>Pažymėkite šią parinktį, jei norite, kad darbuotojas galėtų kurti perkėlimo darbą, bet nebūtų reikalaujama, kad toks darbas būtų atliekamas nedelsiant. Ši parinktis naudinga, jei, pavyzdžiui, buvo atliktas kokybės tikrinimas ir inspektorius nori, kad prekė būtų perkelta iš kokybės tikrinimo srities.</td>
</tr>
<tr class="even">
<td>Krypties kodas</td>
<td>Jei norite naudoti konkretų vietos nurodymą, pasirinkite nurodymo kodą, susietą su vietos nurodymu. Šis laukas galimas, kai kuriate darbą, o darbo kūrimo procesas – <strong>Judėjimas pagal šabloną</strong>.</td>
</tr>
<tr class="odd">
<td>Išjungti ciklų skaičiavimo ribines vertes</td>
<td>Pažymėkite šią parinktį, jei norite nepaisyti ciklo skaičiavimo ribinių reikšmių. Jei pažymite šią parinktį, viršijus ribines reikšmes ciklo skaičiavimo darbas&#39; nekuriamas.</td>
</tr>
<tr class="even">
<td>Rodyti paketo perdavimo kodą</td>
<td>Pasirinkite šią parinktį, kad būtų rodomi paketų perdavimo kodai. Pavyzdžiui, paketų perdavimo kodai gali būti rodomi, kai gaunate grąžintą paketą. Tada darbuotojai gali įvertinti paketo būseną arba kokybę ir pasirinkti reikiamą kodą. Paketo perdavimo kodo taisyklės lemia, ar paketas bus pasiekiamas kitiems sandėlio procesams. Jei nepasirinksite&#39; šios parinkties, bus naudojamas vienas iš šių paketo perdavimo kodų.
<ul>
<li>Jei gaunate naują paketo numerį, numatytasis paketo perdavimo kodas, nurodytas prekės modelių grupėje.</li>
<li>Paketo perdavimo kodas, kuris jau priskirtas paketui.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rodyti perdavimo kodą</td>
<td>Pasirinkite šią parinktį, kad būtų rodomi perdavimo kodai. Pavyzdžiui, perdavimo kodai gali būti rodomi, kai gaunate grąžinamas prekes. Tada darbuotojai gali įvertinti prekių būseną arba kokybę ir pasirinkti reikiamą kodą. Perdavimo kodo taisyklės lemia, ar prekės bus pasiekiamos kitiems sandėlio procesams.</td>
</tr>
<tr class="even">
<td>Rodyti atsargų būseną</td>
<td>Pažymėkite šią parinktį, kad būtų rodoma atsargose esančių prekių būsena. Ši parinktis galima visuose meniu elementuose, naudojančiuose esamą darbą, išskyrus ciklo skaičiavimą.</td>
</tr>
<tr class="odd">
<td>Rodyti paėmimo ekrano suvestinę</td>
<td>Pažymėkite šią parinktį, kad būtų rodoma pasirinkto darbo užsakymo išrinkimo darbo suvestinė. Ši suvestinė rodoma, kol darbo užsakyme neapdorojama pirma darbo eilutė.</td>
</tr>
<tr class="even">
<td>Generuoti numerio lentelę</td>
<td>Pažymėkite šią parinktį, kad būtų kuriamas unikalus numerio lentelės numeris pagal pasirinktą numeraciją. Pavyzdžiui, galite sugeneruoti pagal pirkimo užsakymus gautų prekių numerio lentelę.</td>
</tr>
<tr class="odd">
<td>Grupinis atidėjimas</td>
<td>Pažymėkite šią parinktį, jei norite grupuoti atidėjimo darbus. Ši parinktis galima, jei darbus sugrupavo darbuotojas arba „Supply Chain Management“. Kai darbuotojas baigia visus išrinkimo darbus grupėje, tai pačiai grupei sukuriamas atidėjimo darbas.</td>
</tr>
<tr class="even">
<td>Atsargų koregavimo tipai</td>
<td>Pasirinkite atsargų koregavimo tipą, kuris lemia atsargų skaičiavimo žurnalą, naudojamą koregavimui registruoti, ir ar reikia šalinti rezervacijas. Šis laukas galimas tik darbo kūrimo procesuose <strong>Koregavimo taikymas</strong> arba <strong>Koregavimo atšaukimas</strong>.</td>
</tr>
<tr class="odd">
<td>Nepaisyti paketo numerio</td>
<td>Pažymėkite šią parinktį, kad darbuotojai, nurodantys kiekį kaip baigtą gamybos užsakyme, galėtų įvesti kitokį paketo numerį nei gamybos užsakymui priskirtas gamybos numeris.</td>
</tr>
<tr class="even">
<td>Nepaisyti paskirties numerio lentelės</td>
<td>Pasirinkę šią parinktį leisite darbuotojams nurodyti kitą paskirties numerio lentelę nei siūloma paskirties numerio lentelė. Naudokite šią parinktį, jei pirmasis darbo užsakymo išrinkimas yra skirtas visam prekės kiekiui numerio lentelėje. Ši parinktis naudinga, pavyzdžiui, naudojant padėklą pakartotinai.</td>
</tr>
<tr class="odd">
<td>Paimti ir pakuoti</td>
<td>Pasirinkę šią parinktį leisite darbuotojams sujungti pardavimo užsakymo arba krovinio darbus į vieną darbo vienetą. Darbuotojas gali atlikti tik pardavimo užsakymo arba krovinio darbą. Ši parinktis naudinga, jei, pavyzdžiui, turite didinti pardavimo užsakymo kiekį po pardavimo užsakymo krovinio, siuntos ir darbo sukūrimo. Ši parinktis galima, kai meniu elementas naudoja esamą darbą ir darbą nukreipia vartotojas arba sistema.</td>
</tr>
<tr class="even">
<td>Paimti seniausią paketą</td>
<td>Nurodykite, ar darbuotojas pirmiausia turi išrinkti seniausią vietoje esantį paketą. Galimos toliau nurodytos pasirinktys:
<ul>
<li><strong>Nėra</strong> – darbuotojas gali išrinkti bet kokį vietoje esantį paketą. Darbuotojui nepateikiamas joks pranešimas.</li>
<li><strong>Įspėjimas</strong> – darbuotojas gali išrinkti bet kurį vietoje esantį paketą, bet pateikiamas įspėjamasis pranešimas, jei tai nėra&#39; seniausias paketas.</li>
<li><strong>Priversti</strong> – darbuotojas privalo išrinkti seniausią vietoje esantį paketą. Darbuotojui pateikiamas klaidos pranešimas, jei paketas nėra&#39; seniausias paketas. <strong>Pastaba.</strong> Ši parinktis aktuali tik jei <strong>Paketo numeris</strong> vertė yra žemesnė nei <strong>Vieta</strong> prekei priskirtoje rezervavimo hierarchijoje.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Spausdinti žymą</td>
<td>Pažymėkite šią parinktį, kad darbuotojai galėtų spausdinti numerio lentelės etiketes.</td>
</tr>
<tr class="even">
<td>Sistemos grupavimo laukas</td>
<td>Pasirinkite lauką, kuris lems, kaip „Supply Chain Management“ grupuos išrinkimo darbus darbuotojams. Pavyzdžiui, jei pasirinksite lauką <strong>ShipmentId</strong>, norėdamas grupuoti išrinkimo darbus, darbuotojas nuskaitys siuntos ID. Tada visi siuntos darbai priskiriami darbuotojui. Šiam laukui reikia sukurti meniu elementą, kuris naudos esamus sistemos sugrupuotus darbus. Taip pat turite lauke <strong>Sistemos grupavimo žyma</strong> įvesti tekstą, nurodantį darbuotojui, ką reikia nuskaityti.</td>
</tr>
<tr class="odd">
<td>Sistemos grupavimo žyma</td>
<td>Įvesdami tekstą nurodykite darbuotojui, ką reikia nuskaityti, kai išrinkimo darbus grupuoja „Supply Chain Management“. Pavyzdžiui, jei naudojate&#39; lauką <strong>ShipmentId</strong> norėdami grupuoti išrinkimo darbus pagal siuntą, lauke galite įvesti <strong>Siuntos ID</strong>. Šiam laukui reikia sukurti meniu elementą, kuris naudos esamus sistemos sugrupuotus darbus. Be to, lauke <strong>Sistemos grupavimas</strong> reikia pasirinkti lauką, pagal kurį grupuosite.</td>
</tr>
<tr class="even">
<td>Naudoti numatytuosius duomenis</td>
<td>Pasirinkite šią parinktį, kad veiksmų srityje įgalintumėte mygtuką <strong>Numatytieji duomenys</strong>, skirtą pasirinkti laukams, kuriuose bus rodomi duomenys, įprastai reikalingi darbuotojui kasdieniame jo darbe. Ši parinktis naudinga, jei, pavyzdžiui, darbuotojas dažnai išrenka prekes iš tos pačios vietos. Galite pasirinkti lauką <strong>Vieta iš</strong>, kad pagal numatytuosius parametrus būtų rodoma vieta.</td>
</tr>
<tr class="odd">
<td>Patikrinimo vartotojo nurodymu laukas</td>
<td>Pasirinkite lauką, kurį darbuotojas nuskaitys norėdamas grupuoti darbus. Pavyzdžiui, jei pasirenkate <strong>LoadId</strong>, darbuotojas galės išrinkti bet kokį darbą, susietą su pasirinktu kroviniu. Taip pat turite lauke <strong>Patikrinimo vartotojo nurodymu žymė</strong> įvesti tekstą, nurodantį darbuotojui, ką reikia nuskaityti.</td>
</tr>
<tr class="even">
<td>Patikrinimo vartotojo nurodymu žymė</td>
<td>Įveskite tekstą, kuriuo darbuotojui bus nurodoma, ką reikia nuskaityti, kai išrinkimo darbai grupuojami pagal patvirtintą vartotojo nurodytą lauką. Pavyzdžiui, jei naudojate lauką <strong>LoadId</strong> norėdami grupuoti krovinio išrinkimo darbus, lauke galite įvesti <strong>Krovinio ID</strong>.</td>
</tr>
<tr class="odd">
<td>Darbo šablono kodas</td>
<td>Pasirinkite darbo šabloną, kuris sukurs proceso darbą. Pavyzdžiui, jei gaunate pirkimo užsakymo prekę, atidėjimo darbas bus sukurtas remiantis darbo šablonu. Jei nepasirinksite&#39; darbo šablono, „Supply Chain Management“ priskirs šabloną pagal užklausos kriterijus. Daugiau informacijos apie darbo šablonus žr. <a href="control-warehouse-location-directives.md">Sandėlio darbo kontroliavimas darbo šablonais ir vietų nurodymais</a>.</td>
<tr class="even">
<td>Rodyti darbo eilučių sąrašą</td>
<td>Pasirinkite parinktį, nurodančią, kaip darbuotojai galės peržiūrėti ir sąveikauti su šiuo metu pasirinkto paėmimo darbo eilutėmis. Daugiau informacijos apie šią parinktį žr. <a href="pick-line-overview.md">Mobiliojo įrenginio meniu elemento nustatymas paėmimo eilučių peržiūrai pateikti</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Reikalavimas, kad išrinkdami prekes darbuotojai patvirtintų produktą, vietą arba kiekį

Galite nustatyti darbo patvirtinimus, kuriuose reikalaujama, kad atlikdamas darbus sandėlyje darbuotojas mobiliuoju įrenginiu registruotų vietą arba kiekį. Darbo patvirtinimai padeda užtikrinti, kad darbuotojas būtų reikiamoje vietoje arba dirbtų su reikiamu prekių kiekiu. Be to, galite nustatyti, kad „Supply Chain Management“ automatiškai patvirtintų darbuotojo registraciją. Jei įjungsite automatinį patvirtinimą, negalėsite kartu reikalauti vietos arba kiekio patvirtinimo. Darbo patvirtinimai apima produktus ir produktų variantus. Be to, galite registruoti patvirtinimus nuskaitydami brūkšninį kodą. Norėdami patvirtinti produktus ir produktų variantus, turite įvesti produkto arba produkto varianto ID. Šis ID gali būti produkto ID, produkto ieškos ID, išorinis ID, GTIN arba brūkšninis kodas. Kai įvedate ID arba nuskaitote brūkšninį kodą, mobiliajame įrenginyje rodomos produkto varianto dimensijos. 

Toliau pateikiamoje lentelėje aprašomi įvairūs darbo tipai, su kuriais galite naudoti darbo patvirtinimus.

| Parinktis | Prekės/Paslaugos pavadinimas |
|------------------------|----------------------------------------------------------------------------|
| Paimti | Reikalauti patvirtinimo, kai išrenkamos prekės. |
| Dėti | Reikalauti patvirtinimo, kai prekės dedamos vietoje. |
| Skaičiavimas | Reikalauti patvirtinimo skaičiuojant ciklą. |
| Koregavimai | Reikalauti patvirtinimo koreguojant atsargų kiekius. |
| Pasirinktinai | Reikalauti patvirtinti pasirinktinį darbą. |
| Sulaikymas | Reikalauti patvirtinimo perkeliant prekes į sulaikymo zoną. |
| Numerio lentelės kūrimas | Reikalauti patvirtinimo, kai prekės konsoliduojamos kuriant numerio lentelę. |
| Spausdinti | Reikalauti patvirtinimo spausdinant numerio lentelės etiketes. |
| Būsenos keitimas | Reikalauti patvirtinimo keičiant atsargų būseną. |

> [!NOTE]
> Produkto patvirtinimo galima reikalauti tik tada, jei darbo tipas – paėmimas ir padėjimas.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Nustatyti mobiliojo įrenginio meniu elementą pirkimo užsakymo tipo darbui atlikti](tasks/set-up-mobile-device-menu.md)
- [Mobiliojo įrenginio meniu elemento gautoms prekėms registruoti nustatymas](tasks/set-up-mobile-device-menu-item-register-received-items.md)
- [Atsargų būsenos](../inventory/inventory-statuses.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
