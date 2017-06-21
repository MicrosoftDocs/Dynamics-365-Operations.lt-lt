---
title: "Smulkios išlaidos (skirta Rytų Europai)"
description: "Šioje temoje pateikiama informacija apie smulkių išlaidų funkciją, kuri vartotojams Estijoje, Lietuvoje, Čekijos Respublikoje,Vengrijoje, Latvijoje, Lenkijoje ir Rusijoje suteikia galimybę sistemoje nurodyti grynųjų pinigų operacijas."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268504
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7acabdec9133b4b4cc8fc8861ee097aa2a00e191
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="petty-cash-for-eastern-europe"></a>Smulkios išlaidos (skirta Rytų Europai)

[!include[banner](../includes/banner.md)]


Šioje temoje pateikiama informacija apie smulkių išlaidų funkciją, kuri vartotojams Estijoje, Lietuvoje, Čekijos Respublikoje,Vengrijoje, Latvijoje, Lenkijoje ir Rusijoje suteikia galimybę sistemoje nurodyti grynųjų pinigų operacijas.

Smulkių išlaidų funkciją galite naudoti norėdami automatizuoti grynųjų pinigų gavimo ir išlaidų operacijas, pirminių dokumentų kūrimą ir susijusių ataskaitų spausdinimą. Smulkių išlaidų funkcija suteikia galimybę atlikti toliau nurodytas operacijas.

-   Sukurti turimo grynųjų pinigų turto gavimo iš išlaidų sąskaitą.
-   Generuoti tipines grynųjų pinigų formas: grynųjų pinigų kompensacijos kvitus, grynųjų pinigų išmokėjimo kvitus ir grynųjų pinigų kvitų registracijos žurnalą.
-   Valdyti didžiausią grynųjų pinigų sumą, leidžiamą atliekant operacijas su klientais, tiekėjais ir t. t.
-   Sistemoje nurodyti grynųjų pinigų operacijas įvairiomis valiutomis.
-   Konvertuoti grynųjų pinigų operacijų sumas užsienio valiuta į numatytąją valiutą ir pateikti apskaitos ataskaitas.
-   Generuoti **kasos knygos** ir kasininko darbo ataskaitas.

## <a name="prerequisites"></a>Būtinieji komponentai
Norėdami naudoti smulkių išlaidų funkciją, turite atlikti toliau nurodytas būtinas užduotis.

-   Nustatyti grynųjų pinigų sąskaitas.
-   Nustatyti grynųjų pinigų registravimo šablonus.
-   Nustatyti grynųjų pinigų dokumentų numeravimo numeracijas.
-   Nustatyti grynųjų pinigų ir banko valdymo parametrų numatytąsias vertes.
-   Nustatyti grynųjų pinigų žurnalų pavadinimus DK.

### <a name="set-up-cash-accounts"></a>Nustatyti grynųjų pinigų sąskaitas

Norėdami nustatyti grynųjų pinigų sąskaitą, atidarykite **Grynųjų pinigų valdymas** &gt; **Banko sąskaitos** &gt; **Grynųjų pinigų sąskaitos** ir įveskite toliau nurodytą informaciją.

| Laukas                 | aprašymas                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| Grynieji pinigai                  | Įveskite kodą grynųjų pinigų sąskaitai (grynieji pinigai) identifikuoti.                                                                    |
| Vardas                  | Įveskite grynųjų pinigų sąskaitos aprašą.                                                                             |
| Valiuta              | Pasirinkite grynųjų pinigų operacijų numatytosios valiutos kodą.                                                              |
| Numeracijų grupė | Jei grynųjų pinigų dokumentų numeravimas turi skirtis nuo parametruose nurodyto numeravimo, įveskite kodą. |
| Daugiau valiutų       | Pažymėkite šį žymės langelį, norėdami leisti registruoti valiutas, kurios skiriasi nuo apskaitos valiutos.                     |
| Neigiami grynieji         | Pažymėkite šį žymės langelį, norėdami leisti neigiamus balansus bet kokia valiuta.                                               |

Norėdami nustatyti grynųjų pinigų sąskaitos grynųjų pinigų balanso kontrolės taisykles, nustatykite grynųjų pinigų sąskaitą ir tada veiksmų srities skirtuko **Grynųjų pinigų sąskaita** grupėje **Balanso limitas** spustelėkite **Balanso limitas**. Įveskite toliau nurodytą informaciją.

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
<td>Valiutos tipas</td>
<td>Pasirinkite valiutos tipą.
<ul>
<li><strong>Apskaitos valiuta</strong> – naudokite pagrindinės įmonės valiutos kodą.</li>
<li><strong>Nurodyta valiuta</strong> – naudokite valiutos kodą, kuris skiriasi nuo pagrindinės įmonės valiutos kodo.</li>
</ul></td>
</tr>
<tr class="even">
<td>Valiuta</td>
<td>Jei lauke <strong>Valiutos tipas</strong> pasirinkote <strong>Nurodyta valiuta</strong>, pasirinkite valiutos kodą. Šio lauko naudoti negalima, jei lauke <strong>Valiutos tipas</strong> pasirinkote <strong>Apskaitos valiuta</strong>.</td>
</tr>
<tr class="odd">
<td>Balanso limito tipas</td>
<td>Pasirinkti vieną galimų verčių.
<ul>
<li><strong>Didžiausia</strong> – grynųjų pinigų balansas negali viršyti grynųjų pinigų sąskaitos lauke <strong>Balanso limitas</strong> nurodytos sumos (viršutinė riba).</li>
<li><strong>Mažiausia</strong> – grynųjų pinigų balansas negali būti mažesnis nei grynųjų pinigų sąskaitos lauke <strong>Balanso limitas</strong> nurodyta suma (apatinė riba).</li>
</ul></td>
</tr>
<tr class="even">
<td>Tikrinti balanso limitą</td>
<td>Pasirinkite, kas bus atliekama grynųjų pinigų dokumentų tvirtinimo proceso metu, jei grynųjų pinigų sąskaitos lauke <strong>Balanso limitas</strong> nurodyta suma viršijama.
<ul>
<li><strong>Leisti</strong> – limitą galima viršyti.</li>
<li><strong>Įspėjimas</strong> – limitą galima viršyti, bet vartotojui rodomas įspėjimas. Grynųjų pinigų dokumentas patvirtintas.</li>
<li><strong>Klaida</strong> – limito viršyti negalima. Vartotojui rodomas klaidos pranešimas, o grynųjų pinigų dokumentas nėra patvirtinamas.</li>
</ul>
Daugiau informacijos apie grynųjų pinigų dokumentų tvirtinimo procesą žr. tolesniame šios temos skyriuje &quot;Grynųjų pinigų tvirtinimas ir registravimas&quot;.</td>
</tr>
<tr class="odd">
<td>Balanso limitas</td>
<td>Įveskite grynųjų pinigų sąskaitos balanso limitą. Suma turi būti rodoma jūsų nurodyta valiuta.</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a>Grynųjų pinigų registravimo šablonų nustatymas

Grynųjų pinigų registravimo šablonai apibrėžia registravimą DK. Norėdami nustatyti grynųjų pinigų registravimo šabloną, atidarykite **Grynųjų pinigų** **ir banko valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų registravimo šablonai** ir pasirinkite arba sukurkite registravimo šabloną. Įveskite toliau nurodytą informaciją.

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
<td>Galioja</td>
<td>Nurodykite, ar registravimo šablonas taikomas konkrečiai grynųjų pinigų sąskaitai ar visoms grynųjų pinigų sąskaitoms.
<ul>
<li><strong>Lentelė</strong> – jei yra registravimo šablono eilutė, skirta grynųjų pinigų sąskaitai, ta eilutė naudojama registruojant grynųjų pinigų operaciją.</li>
<li><strong>Visi</strong> – nėra registravimo šablono eilutės, skirtos grynųjų pinigų sąskaitai.</li>
</ul></td>
</tr>
<tr class="even">
<td>Grynieji pinigai</td>
<td>Jei lauke <strong>Galioja</strong> pasirinkote parinktį <strong>Lentelė</strong>, nurodykite grynųjų pinigų sąskaitą. Šis laukas lieka neužpildytas, jei lauke <strong>Galioja</strong> pasirinkote parinktį <strong>Visi</strong>.</td>
</tr>
<tr class="odd">
<td>DK sąskaita</td>
<td>Įveskite DK sąskaitos numerį, kuris bus naudojamas grynųjų pinigų sąskaitos suminė sąskaita.</td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a>Grynųjų pinigų dokumentų numeracijos nustatymas

Norėdami nustatyti grynųjų pinigų dokumentų numeracijas, atidarykite **Grynųjų pinigų valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų ir banko valdymo parametrai**. Skirtuke **Numeracija** nurodykite numeracijos kodus, skirtus dokumentams **Grynųjų pinigų kompensacijos kvitai**, **Grynųjų pinigų išmokėjimo kvitai**, **Grynųjų pinigų koregavimo kvitas** ir **Derinimas dėl valiutos kurso** bei **Grynųjų pinigų ataskaitos numeris**.

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a>Grynųjų pinigų ir banko valdymo parametrų numatytųjų verčių nustatymas

Norėdami nustatyti smulkių išlaidų funkcijos grynųjų pinigų ir banko valdymo parametrų numatytąsias vertes, atidarykite **Grynųjų pinigų valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų ir banko valdymo parametrai**. Skirtuke **Grynieji pinigai** įveskite tolesnę informaciją.

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
<td>Grynieji pinigai</td>
<td>Pasirinkite numatytąją žurnalų grynųjų pinigų sąskaitą.</td>
</tr>
<tr class="even">
<td>Grynųjų registravimas</td>
<td>Įveskite numatytąjį grynųjų pinigų registravimo šabloną, naudojamą, jei joks kitas registravimo šablonas nenurodytas.</td>
</tr>
<tr class="odd">
<td>Panaudotų kvitų kontrolė</td>
<td>Pasirinkite, kas bus atliekama, jei tikrinant grynųjų pinigų dokumento numerį rasti pasikartojantys numeriai.
<ul>
<li>Neleisti dubliuoti</li>
<li>Neleisti daryti kopijų finansiniuose metuose</li>
<li>Leisti dubliavimą</li>
<li>Perspėjimas apie dublikatus</li>
</ul></td>
</tr>
<tr class="even">
<td>Tikrinti operacijų limitą</td>
<td>Nurodykite, kad nutinka, jei viršijama operacijų su sąveikos objektais riba.
<ul>
<li><strong>Leisti</strong> – limitą galima viršyti.</li>
<li><strong>Įspėjimas</strong> – limitą galima viršyti, bet vartotojui rodomas įspėjimas. Operacija užregistruota.</li>
<li><strong>Klaida</strong> – limito viršyti negalima. Vartotojui rodomas klaidos pranešimas, o operacija nėra registruojama.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tikrinimo metodas</td>
<td>Pasirinkite tikrinimo metodą, naudojamą limitą viršijančioms operacijų sumoms kontroliuoti.
<ul>
<li><strong>Operacija</strong> – atliekamas kiekvienos operacijos tikrinimas.</li>
<li><strong>Sutartis</strong> – atliekamas kiekvienos operacijos, turinčios nurodytą sutartį su sąveikos objektu, tikrinimas.</li>
</ul></td>
</tr>
<tr class="even">
<td>Operacijų limitas</td>
<td>Įveskite didžiausią sumą, leidžiamą operacijose, kurios turi sąveikos objektų grynaisiais.</td>
</tr>
<tr class="odd">
<td>Registravimas ankstesne data</td>
<td>Pažymėkite šį žymės langelį, kad leistumėte registruoti grynųjų pinigų operacijas ankstesne nei vėliausios grynųjų pinigų operacijos data.</td>
</tr>
<tr class="even">
<td>Dimensijos</td>
<td>Įveskite dimensijas laukuose <strong>Padalinio kodas</strong>, <strong>Analizės kodas</strong> ir <strong>Paskirties kodas</strong>. Ši informacija bus nurodyta grynųjų pinigų dokumentų spausdinimo formoje.</td>
</tr>
<tr class="odd">
<td>Naudoti patvirtinimo būseną</td>
<td>Pažymėkite šį žymės langelį , kad būtų naudojama papildoma būsena <strong>patvirtinta</strong>, kai patvirtinate grynųjų pinigų dokumentus. (Daugiau informacijos žr. skyriuje &quot;Grynųjų pinigų operacijų tvirtinimas ir registravimas&quot;.)</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a>Grynųjų pinigų žurnalų pavadinimų nustatymas DK

Norėdami kurti grynųjų pinigų operacijų registravimo žurnalą, atidarykite **DK** &gt; **Žurnalo sąranka** &gt; **Žurnalų pavadinimai** ir sukurkite naują įrašą. Lauke **Žurnalo tipas** nurodykite **Grynieji pinigai**. Pagal poreikį nustatykite kitus numatytuosius žurnalo parametrus.

## <a name="daily-cash-operations-via-a-slip-journal"></a>Kasdienės grynųjų pinigų operacijos naudojant važtaraščių žurnalą
Jei norite kurti grynųjų pinigų dokumentą naudodami važtaraščių žurnalą, atidarykite **Grynųjų pinigų ir banko valdymas** &gt; **Grynųjų pinigų operacijos** &gt; **Važtaraščių žurnalas** ir sukurkite naują žurnalą. Veiksmų srityje spustelėkite **Eilutės**. Įtraukite naują eilutę ir įveskite tolesnę informaciją.

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
<td>Data</td>
<td>Įveskite operacijos datą.</td>
</tr>
<tr class="even">
<td>Paskyra</td>
<td>Pasirinkite grynųjų pinigų sąskaitą. Pagal numatytuosius parametrus grynųjų pinigų sąskaita nurodoma grynųjų pinigų ir banko valdymo parametruose.</td>
</tr>
<tr class="odd">
<td>aprašymas</td>
<td>Įveskite operacijos paaiškinamąjį tekstą.</td>
</tr>
<tr class="even">
<td>Debetas Kreditas</td>
<td>Įveskite grynųjų pinigų dokumento sumą viename iš šių laukų.
<ul>
<li><strong>Debetas</strong> – naudokite šį lauką norėdami registruoti grynųjų pinigų kvitus ir grynųjų pinigų kompensacijos kvitą.</li>
<li><strong>Kreditas</strong> – naudokite šį lauką norėdami registruoti grynųjų pinigų išlaidas ir grynųjų pinigų kompensacijos kvitą.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Korespondentinės sąskaitos tipas Korespondentinė sąskaita</td>
<td>Pasirinkite korespondentinės sąskaitos tipą ir korespondentinės sąskaitos numerį.</td>
</tr>
<tr class="even">
<td>Valiuta</td>
<td>Pasirinkite operacijos valiutos kodą.</td>
</tr>
<tr class="odd">
<td>Kvitas</td>
<td>Šis laukas užpildomas automatiškai, atsižvelgiant į žurnalo sąranką.</td>
</tr>
<tr class="even">
<td>Užsakymo numeris</td>
<td>Jei nenustatyta jokia kita grynųjų pinigų sąskaitos numeracija, šis laukas užpildomas automatiškai, atsižvelgiant į parametruose nurodytą numeraciją. Pagal poreikį šiame lauke galite neautomatiškai įvesti užsakymo numerį. Siekiant užtikrinti grynųjų pinigų dokumentų numeravimo nuoseklumą, taikoma ši kontrolė: grynųjų pinigų dokumento, kurio operacijos data ankstesnė, numeris negali būti didesnis nei grynųjų pinigų dokumento, kurio operacijos data vėlesnė, numerį. Jei ši kontrolė jums nereikalinga, grynųjų pinigų ir banko valdymo parametruose pažymėkite žymės langelį <strong>Registravimas ankstesne data</strong>.</td>
</tr>
<tr class="odd">
<td>Patvirtinimo būsena</td>
<td>Pradinė operacijos būsena yra <strong>Nėra</strong>. Daugiau informacijos apie tai, kaip nustatyti operacijos būseną, žr. skyriuje &quot;Grynųjų pinigų operacijų tvirtinimas ir registravimas&quot;.</td>
</tr>
<tr class="even">
<td>Dokumento tipas </td>
<td>Šis skirtuko <strong>Grynųjų pinigų užsakymas</strong> laukas užpildomas automatiškai, atsižvelgiant į įvestą grynųjų pinigų dokumento sumą.
<ul>
<li><strong>Grynųjų pinigų kompensacijos kvitas</strong> – ši vertė naudojama, jei sumą įvedėte grynųjų pinigų sąskaitos lauke <strong>Debetas</strong>.</li>
<li><strong>Grynųjų pinigų išmokėjimo kvitas</strong> – ši vertė naudojama, jei sumą įvedėte grynųjų pinigų sąskaitos lauke <strong>Kreditas</strong>.</li>
<li><strong>Pataisymas</strong> – įvedėte neigiamą sumą grynųjų pinigų sąskaitos lauke <strong>Debetas</strong> arba <strong>Kreditas</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PVM grupė</td>
<td>Nurodykite PVM grupę, naudojamą operacijos mokesčiams skaičiuoti.</td>
</tr>
<tr class="even">
<td>Prekės PVM grupė</td>
<td>Nurodykite prekės PVM grupę, naudojamą operacijos mokesčiams skaičiuoti.</td>
</tr>
<tr class="odd">
<td>Priežastis</td>
<td>Skirtuke <strong>Grynųjų pinigų užsakymas</strong> įveskite tekstą, aprašantį operacijos subjektą. Šis tekstas bus spausdinamas grynųjų pinigų kvito ataskaitos formoje.</td>
</tr>
<tr class="even">
<td>Dokumento data</td>
<td>Įveskite pradinio dokumento, kuris yra operacijos priežastis (pvz., išankstinės ataskaitos, SF arba užsakymo), aprašą, numerį ir datą.</td>
</tr>
<tr class="odd">
<td>Atstovo tipas</td>
<td>Šiame lauke galima naudoti toliau nurodytas vertes.
<ul>
<li><strong>Darbuotojas</strong> – peržvalgoje <strong>Atstovas</strong> pateikiamas darbuotojų sąrašas, jei laukas <strong>Korespondentinė sąskaita</strong> nustatytas į parinktį <strong>DK</strong> arba <strong>Bankas</strong>, arba sąveikos objekto kontaktinių asmenų sąrašas, jei laukas <strong>Korespondentinė sąskaita</strong> nustatytas į parinktį <strong>Klientas</strong> arba <strong>Tiekėjas</strong>. Norėdami nustatyti atstovus, pasirinkite <strong>Pagrindinis</strong> &gt; <strong>Sąranka</strong> &gt; <strong>Kontaktai</strong> &gt; <strong>Kontaktinis asmuo</strong>.</li>
<li><strong>Kita</strong> – peržvalgoje <strong>Atstovas</strong> pateikiamas kitų klientų sąrašas. Norėdami nustatyti gavėjus, kurių nėra lentelėje <strong>Klientai</strong> arba <strong>Tiekėjai</strong>, pasirinkite <strong>DK</strong> &gt; <strong>Gavėjai</strong>. Šį tipą galima naudoti tik Latvijoje. (Turi būti suaktyvinta konfigūracija <strong>CSELatvia</strong>.)</li>
<li><strong>Tiekėjas</strong> – peržvalgoje <strong>Atstovas</strong> pateikiamas tiekėjų sąrašas. Norėdami nustatyti tiekėjus, pasirinkite <strong>Mokėtinos sumos</strong> &gt; <strong>Tiekėjai</strong>.</li>
<li><strong>Klientas</strong> – peržvalgoje <strong>Atstovas</strong> pateikiamas klientų sąrašas. Norėdami nustatyti klientus, pasirinkite <strong>Gautinos sumos</strong> &gt; <strong>Klientai</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Atstovas</td>
<td>Pasirinkite atstovą, kurio tipą nurodėte lauke <strong>Atstovo tipas</strong>.</td>
</tr>
<tr class="odd">
<td>Asmens vardas</td>
<td>Šis laukas užpildomas automatiškai, atsižvelgiant laukus <strong>Korespondentinė sąskaita</strong> ir <strong>Atstovas</strong>. Ši informacija bus nurodyta grynųjų pinigų kvitų spausdinimo formoje.</td>
</tr>
<tr class="even">
<td>Tapatybės kortelė</td>
<td>Šis laukas užpildomas automatiškai, atsižvelgiant į kontaktinio asmens (atstovo) tapatybės kortelės duomenis. Jei laukas <strong>Korespondentinės sąskaitos tipas</strong> nustatytas į parinktį <strong>Avanso turėtojas</strong>, o laukas <strong>Korespondentinė sąskaita</strong> nustatytas į darbuotojo numerį, grynųjų pinigų gavimas arba išlaidos gali būti priskiriamos darbuotojui. Šiuo atveju laukas <strong>Tapatybės kortelė</strong> užpildomas automatiškai naudojant tapatybės kortelės duomenis iš lentelės <strong>Darbuotojai</strong> (<strong>Personalo apskaita</strong> &gt; <strong>Darbuotojų lentelė</strong>).</td>
</tr>
<tr class="odd">
<td>Paskirtis</td>
<td>Lentelėje <strong>Paskirtis</strong> nurodykite vieną arba daugiau operacijos sumos paskirties kodų. Pasirinkite paskirties kodą lauke <strong>Paskirtis</strong> ir įveskite paaiškinimą lauke <strong>Operacijos tekstas</strong>. Lauke <strong>Suma</strong> įveskite sumą operacijos valiuta. Lauke <strong>Procentas</strong> rodomas paskirties sumos ir bendros operacijos sumos koeficientas procentais.</td>
</tr>
<tr class="even">
<td>Likutis</td>
<td>Apskaičiuojama likusi suma. Atkreipkite dėmesį, kad visą operacijos sumą reikia priskirti paskirties kodams.</td>
</tr>
<tr class="odd">
<td>Tarnautojai</td>
<td>Skirtuke <strong>Tarnautojai</strong> nurodykite atsakingų asmenų (Direktorius, Vyr. buhalteris ir Kasininkas) vardus ir pavardes. Lauko <strong>Pareigos</strong> vertės nustatomos pagal tarnautojų nustatymą puslapio <strong>Tarnautojai</strong> skirtukuose <strong>Bendra</strong> ir <strong>DK</strong> (<strong>Pagrindinis</strong> &gt; <strong>Sąranka</strong> &gt; <strong>Kontaktai</strong> &gt; <strong>Tarnautojai</strong>).</td>
</tr>
<tr class="even">
<td>Išankstinis mokėjimas</td>
<td>Pasirinkite šį žymės langelį, jei operacija yra išankstinis mokėjimas.</td>
</tr>
<tr class="odd">
<td>Registravimo šablonas</td>
<td>Įveskite grynųjų pinigų sąskaitos registravimo šabloną. Pagal numatytuosius parametrus naudojamas grynųjų pinigų ir banko valdymo parametruose nurodytas registravimo šablonas.</td>
</tr>
<tr class="even">
<td>Koresp. registravimo šablonas</td>
<td>Įveskite pasirinktos korespondentinės sąskaitos registravimo šabloną.</td>
</tr>
<tr class="odd">
<td>Bendra suma</td>
<td>Puslapio apačioje esančios laukų grupės <strong>Bendra suma</strong> lauke <strong>Komp.</strong> rodoma bendra apskaičiuota visų grynųjų pinigų kompensacijos kvitų, įvestų dabartiniame žurnale, suma, o lauke <strong>Išm.</strong> rodoma bendra visų grynųjų pinigų išmokėjimo kvitų suma.</td>
</tr>
</tbody>
</table>

Norėdami patikrinti žurnalo įrašus, veiksmų srityje spustelėkite **Tikrinti**.

## <a name="daily-cash-operations-via-a-general-journal"></a>Kasdienės grynųjų pinigų operacijos naudojant bendrąjį žurnalą
Jei norite kurti grynųjų pinigų operaciją naudodami bendrąjį žurnalą, atidarykite **DK** &gt; **Žurnalo įrašai** &gt; **Bendrieji žurnalai** ir sukurkite naują žurnalą. Veiksmų srityje spustelėkite **Eilutės**. Įtraukite naują eilutę ir įveskite tolesnę informaciją.

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
<td>Data</td>
<td>Įveskite operacijos datą.</td>
</tr>
<tr class="even">
<td>Kodo tipas</td>
<td>Pasirinkite <strong>Smulkios išlaidos</strong>.</td>
</tr>
<tr class="odd">
<td>Paskyra</td>
<td>Pasirinkite grynųjų pinigų sąskaitos numerį.</td>
</tr>
<tr class="even">
<td>Operacijos tekstas</td>
<td>Įveskite operacijos paaiškinamąjį tekstą.</td>
</tr>
<tr class="odd">
<td>Debetas Kreditas</td>
<td>Įveskite grynųjų pinigų dokumento sumą viename iš šių laukų.
<ul>
<li><strong>Debetas</strong> – naudokite šį lauką norėdami registruoti grynųjų pinigų kvitus ir grynųjų pinigų kompensacijos kvitą.</li>
<li><strong>Kreditas</strong> – naudokite šį lauką norėdami registruoti grynųjų pinigų išlaidas ir grynųjų pinigų kompensacijos kvitą.</li>
</ul></td>
</tr>
<tr class="even">
<td>Korespondentinės sąskaitos tipas Korespondentinė sąskaita</td>
<td>Pasirinkite korespondentinės sąskaitos tipą ir korespondentinės sąskaitos numerį.</td>
</tr>
<tr class="odd">
<td>Valiuta</td>
<td>Pasirinkite operacijos valiutos kodą.</td>
</tr>
</tbody>
</table>

Skirtuke **SF** galite nurodyti pasirinktos sąskaitos ir korespondentinės sąskaitos registravimo šablonus. Jei užregistruota operacija yra išankstinis mokėjimas, skirtuke **Mokėjimas** pažymėkite žymės langelį **Išankstinis mokėjimas**. Laukų grupėje **Atstovas** užpildykite laukus, kaip tai atlikote važtaraščių žurnalo eilutėse, kad spausdintumėte ataskaitą **Grynieji pinigai**. Norėdami patikrinti žurnalo įrašus, veiksmų srityje spustelėkite **Tikrinti**.

## <a name="cash-transaction-approval-and-posting"></a>Grynųjų pinigų operacijos tvirtinimas ir registravimas
Galima taikyti šias grynųjų pinigų operacijų būsenas: **Nėra**, **Patikrinta**, **Patvirtinta** ir **Atmesta**. Skirtuko **Grynieji pinigai** „FastTab“ **Tvirtinimas** (**Grynųjų pinigų ir banko valdymas** &gt; **Sąranka** &gt; **Grynųjų pinigų ir banko valdymo parametrai**) parametras **Naudoti patvirtinimo būseną** suteikia galimybę suaktyvinti dvi papildomas būsenas: **Patvirtinta** ir **Atmesta**. Tvirtinimas yra tinkamas, kai grynųjų pinigų dokumentai išduodami, o grynųjų pinigų gavimas arba išlaidos padalijamos dviem darbuotojams: buhalteriui ir kasininkui. Funkcija **Iš naujo nustatyti būseną** keičia dabartinę operacijos būseną. **Patvirtinta** tampa **Patikrinta**, o **Patikrinta** tampa **Nėra**. Grynųjų pinigų žurnalo įrašus galima redaguoti tik kai būsena yra **Nėra**. Grynųjų pinigų operacijas galima atmesti tik kai operacijos būsena yra **Patikrinta** . Atmesti grynųjų pinigų dokumentai įtraukiami į ataskaitą **Grynųjų pinigų dokumentų registracijos žurnalas**, bet jie nėra nurodyti ataskaitoje **Kasos knyga**. Norėdami patvirtinti operaciją, pasirinkite atitinkamą važtaraščių žurnalo eilutę ir tada spustelėkite **Dokumentų tvirtinimas** &gt; **Tvirtinti**. Sugeneruojamas užsakymo numeris, atsižvelgiant į nurodytą numeraciją. Operacijos būsena pasikeičia į **Patvirtinta** ir žurnalo eilutės redaguoti nebegalima. Grynųjų pinigų sąskaitos balansas lieka nepakitęs. Norėdami atmesti grynųjų pinigų dokumentą, spustelėkite **Dokumentų tvirtinimas** &gt; **Atmesti**. Šią parinktį galima taikyti tik būsenos **Patvirtinta** dokumentams. Norėdami patvirtinti operaciją, pasirinkite atitinkamą važtaraščių žurnalo eilutę ir tada spustelėkite **Dokumentų tvirtinimas** &gt; **Tvirtinti**. Būsena **Patvirtinta** nurodo, grynųjų pinigų lėšos yra gautos arba išleistos. Grynųjų pinigų balansas pakeistas. Grynųjų pinigų operaciją galima registruoti. Norėdami atšaukti būseną **Patvirtinta** ir iš naujo nustatyti būseną **Nėra**, spustelėkite **Dokumentų tvirtinimas** &gt; **Iš naujo nustatyti būseną**. Galima registruoti tik patvirtintas grynųjų pinigų operacijas. Norėdami registruoti žurnalą, spustelėkite **Registruoti** &gt; **Registruoti**.

## <a name="print-a-cash-order"></a>Grynųjų pinigų užsakymo spausdinimas
Norėdami spausdinti grynųjų pinigų užsakymą, pasirinkite važtaraščių žurnalo eilutę ir tada veiksmų srityje spustelėkite **Spausdinti** &gt; **Grynųjų pinigų užsakymo ataskaita**. Sistema sugeneruoja grynųjų pinigų kompensacijos kvito arba grynųjų pinigų išmokėjimo kvito spausdinimo formą, atsižvelgiant į tai, suma įvesta pasirinktos eilutės lauke **Debetas**, ar lauke **Kreditas**.

-   Jei suma įvesta lauke **Debetas**: grynųjų pinigų kompensacijos kvitas
-   Jei suma įvesta lauke **Kreditas**: grynųjų pinigų išmokėjimo kvitas

Važtaraščių žurnalo eilutes, kurių būsena **Patikrinta**, **Patvirtinta** arba **Atmesta**, galima spausdinti. Taip pat galite spausdinti grynųjų pinigų užsakymo dokumentus pasirinkę **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Grynųjų pinigų užsakymai**.

## <a name="periodic-tasks"></a>Periodinės užduotys
Toliau nurodytas užduotis galima atlikti pasirinkus **Grynųjų pinigų ir banko valdymas** &gt; **Periodinės užduotys**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Periodinė užduotis</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tikrinti balanso limitą</td>
<td>Patikrinkite pasirinktos grynųjų pinigų sąskaitos balansą nurodytą dieną ir pateikite rezultatą informaciniame pranešime. Skaičiuojant balansą įtraukiamos tik patvirtintos operacijos. Operacijos, kurios pažymėtos kaip <strong>Atlyginimams</strong>, neįtraukiamos.</td>
</tr>
<tr class="even">
<td>Grynųjų balanso perskaičiavimas</td>
<td>Naudokite šią užduotį, norėdami įsitikinti, grynųjų pinigų sąskaitų DK balansai neviršija grynųjų pinigų balanso.</td>
</tr>
<tr class="odd">
<td>Grynųjų pinigų ataskaitos kūrimas (skirta tik Lenkijai)</td>
<td>Sukurkite <strong>grynųjų pinigų</strong> ataskaitą. <strong>Grynųjų pinigų</strong> ataskaitos numeris sugeneruojamas pagal lauke <strong>Ataskaitos numeris</strong> nustatytą numeraciją. Užduoties dialogo lango lauke <strong>Pabaigos data</strong> nurodykite vėliausią dieną, iki kurios atliktos operacijos įtraukiamos į <strong>grynųjų pinigų</strong> ataskaitą. Naudokite funkciją <strong>Filtras</strong> skirtuke <strong>Įtrauktini įrašai</strong>, kad nurodytumėte papildomus grynųjų pinigų operacijų pasirinkimo ribojimo kriterijus. Šie kriterijai gali apimti grynųjų pinigų sąskaitos numerius ir valiutų kodus. Lauke <strong>Sukūrė</strong> pasirinkite už ataskaitos kūrimą atsakingą vartotoją. Norėdami peržiūrėti kuriamą <strong>grynųjų pinigų</strong> ataskaitą, naudokite puslapio <strong>Grynųjų pinigų sąskaitos</strong> mygtuką <strong>Grynųjų pinigų ataskaitos</strong>.</td>
</tr>
<tr class="even">
<td>Grynieji pinigai – derinimo dėl valiutos kurso FIFO ir LIFO (skirta tik Lenkijai)</td>
<td>Apskaičiuokite derinimą dėl valiutos kurso pagal Lenkijoje taikomus standartus. Naudokite funkciją <strong>Filtras</strong> skirtuke <strong>Įtrauktini įrašai</strong>, kad nurodytumėte grynųjų pinigų sąskaitą, kurios užduotį norite vykdyti. Pasirinkite žymės langelį <strong>Perskaičiavimas</strong>, norėdami visiškai perskaičiuoti visų atvirų laikotarpių derinimo dėl valiutos kurso skirtumą. Toliau parodoma, kai skaičiuojamas derinimas dėl valiutos kurso, kai naudojami metodai „pirmasis į, pirmasis iš“ (FIFO) ir „paskutinysis į, pirmasis iš“ (LIFO).
<ul>
<li><strong>FIFO metodas</strong> – sistema ieško išlaidų operacijos, kurios operacijos data ankstesnė (mažesnis užsakymo numeris) ir sudengia ją naudodama gavimo operaciją, kurios operacijos data ankstesnė (mažesnis užsakymo numeris).</li>
<li><strong>LIFO metodas</strong> – sistema ieško išlaidų operacijos, kurios operacijos data vėlesnė (didesnis užsakymo numeris) ir sudengia ją naudodama gavimo operaciją, kurios operacijos data vėlesnė (didesnis užsakymo numeris).</li>
</ul>
Sudengta suma nurodoma puslapio <strong>Grynųjų pinigų operacija</strong> lauke <strong>Sudengta valiuta</strong>. Jei nustatytas derinimo dėl valiutos kurso skirtumas, suma rodoma lauke <strong>Derinimo dėl valiutos kurso suma</strong>, o dokumento tipo <strong>Valiutos kursų skirtumas</strong> operacija sugeneruojama lentelėje <strong>Grynųjų pinigų operacija</strong>. Pelno / nuostolių operacijų DK sąskaitos nustatomos lentelėje <strong>Valiuta</strong> (<strong>Valiutos kurso finansinis pelnas</strong> ir <strong>Valiutos kurso finansiniai nuostoliai</strong>).</td>
</tr>
<tr class="odd">
<td>Užsienio valiutos kurso pasikeitimas – grynieji pinigai</td>
<td>Naudokite šią užduotį, kad ataskaitos dieną balansas numatytąja valiuta būtų pakankamas, kai operacijos įvedamos užsienio valiutomis. Naudokite funkciją <strong>Filtras</strong> skirtuke <strong>Įtrauktini įrašai</strong>, kad nurodytumėte grynųjų pinigų sąskaitą, kurios užduotį norite vykdyti. Užduoties dialogo lange naudokite laukus <strong>Iš valiutos</strong> ir <strong>Į valiutą</strong>, kad nurodytumėte operacijos valiutas. Sistema palygina sumą valiuta, kuri buvo konvertuota naudojant valiutos kursą pasirinktą dieną, su suma numatytąja valiuta. Abiejų sumų skirtumas (neįskaitant ankstesnio derinimo dėl valiutos kurso) yra apskaičiuotas derinimas dėl valiutos kurso. Ši užduotis sukuria patvirtintą grynųjų pinigų operaciją, kurios tipas <strong>Derinimas dėl valiutos kurso</strong>. DK operacija suformuojama naudojant grynųjų pinigų DK sąskaitą ir DK sąskaitą, nurodytą lentelės <strong>Valiuta</strong> lauke <strong>Nerealizuotas pelnas</strong> arba <strong>Nerealizuoti nuostoliai</strong>.</td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a>Užklausos ir ataskaitos
| Užklausa arba ataskaita                             | aprašymas                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Grynųjų pinigų operacijų rodinys                        | Tvarkydami važtaraščių žurnalo eilutę, naudokite veiksmų mygtuką **Užklausos**, kad peržiūrėtumėte DK operacijas, grynųjų pinigų balansą ir kitą informaciją.                                                                                  |
| Operacija grynaisiais                              | Pasirinkite **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Grynųjų pinigų operacijos**, kad peržiūrėtumėte grynųjų pinigų operacijas. Naudokite funkciją **Filtras**, kad nurodytumėte papildomus grynųjų pinigų operacijų pasirinkimo ribojimo kriterijus. |
| Registravimo žurnalas (skirta Estijai, Rusijai) | Ataskaitoje, kurią galima peržiūrėti pasirinkus **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Registravimo žurnalas**, nurodomi visi išduoti grynųjų pinigų kompensavimo ir grynųjų pinigų išmokėjimo kvitai.                                   |
| Kasos knyga (skirta Latvijai, Lietuvai, Rusijai)     | Ataskaitoje, kurią galima peržiūrėti pasirinkus **Grynųjų pinigų ir banko valdymas** &gt; **Užklausos ir ataskaitos** &gt; **Kasos knygos ataskaita**, nurodomi faktiniai grynųjų pinigų lėšų perkėlimai (gavimai ir išlaidos).                                                            |






