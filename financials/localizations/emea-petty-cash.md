---
title: "Smulkių pinigų Rytų Europai"
description: "Šioje temoje pateikta informacija apie kasos funkcijas, kurios leidžia vartotojams – Estijoje, Lietuvoje, Čekijoje, Vengrijoje, Latvijoje, Lenkijoje ir Rusijoje atspindėtų grynųjų pinigų operacijų sistemos."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268504
ms.assetid: ff2ea7b0-8de2-48c5-8f9f-5d95d9924925
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: e843abff91f74ff8c2c577f499fa829821fc56ee
ms.lasthandoff: 03/31/2017


---

# <a name="petty-cash-for-eastern-europe"></a>Smulkių pinigų Rytų Europai

Šioje temoje pateikta informacija apie kasos funkcijas, kurios leidžia vartotojams – Estijoje, Lietuvoje, Čekijoje, Vengrijoje, Latvijoje, Lenkijoje ir Rusijoje atspindėtų grynųjų pinigų operacijų sistemos.

Kasos funkcija galite automatizuoti veiklos pajamas ir išlaidas, pinigų, pirminių dokumentų kūrimo ir susijusių ataskaitų spausdinimas. Kasos funkcija leidžia atlikti šiuos darbus:

-   Sąskaitos gavimo ir išlaidų piniginių turto.
-   Generuoti tipiškų pinigų formų: grynųjų pinigų kompensacijos kvitus, grynųjų pinigų išmokėjimo kvitus ir įregistruoti grynųjų pinigų kvitus leidinyje.
-   Kontroliuoti maksimali pinigų suma, kurią leidžiama registruoti operacijas su klientais, tiekėjais ir pan.
-   Atspindi pinigų operacijas įvairiomis valiutomis, sistemoje.
-   Konvertuoti grynųjų pinigų operacijų sumas užsienio valiuta su numatytąja valiuta pateikti apskaitos ataskaitų.
-   Sugeneruoti per **kasos knyga** ir kasos darbo ataskaitas.

## <a name="prerequisites"></a>Būtinieji komponentai
Prieš pradėdami naudoti funkciją smulkių pinigų, jūs turite užpildyti šias būtinas sąlygas:

-   Nustatyti pinigų sąskaitas.
-   Nustatyti pinigų registravimo šablonų.
-   Nustatyti numeraciją grynųjų pinigų dokumentų numeravimas.
-   Nustatyti numatytąsias vertes, grynaisiais pinigais ir banko valdymo parametrus.
-   Nustatyti grynųjų pinigų žurnalų pavadinimai paprastai knygos.

### <a name="set-up-cash-accounts"></a>Nustatyti pinigų sąskaitos

Norėdami nustatyti pinigų, atidaryti **pinigų ir banko valdymo**&gt;**banko sąskaitų**&gt;**iždo sąskaitos**, ir įveskite šią informaciją.

| Laukas                 | aprašymas                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| Grynieji pinigai                  | Įvesti kodą, identifikuosiantį grynųjų pinigų sąskaitos (grynaisiais pinigais).                                                                    |
| Vardas                  | Įveskite grynųjų pinigų sąskaitą.                                                                             |
| Valiuta              | Pasirinkite numatytąjį valiutos kodą už grynųjų pinigų operacijas.                                                              |
| Numeracijų grupė | Jei grynųjų pinigų dokumentų numeravimas neturi skirtis nuo numeravimas tai nurodyta, įvesti kodą. |
| Daugiau valiutų       | Pažymėkite šį žymės langelį norint leisti valiutomis, kurios skiriasi nuo numatytąja valiuta turi būti registruojama.                     |
| Neigiami grynieji         | Pažymėkite šį žymės langelį norint leisti neigiamą grynųjų pinigų balansą bet kuria valiuta.                                               |

Nustatyti pinigų likučio kontrolės taisykles grynųjų pinigų sąskaitos, pasirinkite grynųjų pinigų sąskaitą, ir tada, ir veiksmų srityje, apie į **grynųjų pinigų sąskaitos** skirtuke, be į **balanso riba** grupės, spustelėkite **balanso riba**. Įveskite toliau nurodytą informaciją.

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
<td>Pasirinkite valiutos rūšį:
<ul>
<li><strong>Numatytąja valiuta</strong> – naudoti pagrindinio įmonės valiutos kodas.</li>
<li><strong>Nurodyta valiuta</strong> – naudoti valiutos kodą, kuris skiriasi nuo pagrindinio įmonės valiutos kodas.</li>
</ul></td>
</tr>
<tr class="even">
<td>Valiuta</td>
<td>Jei pasirinkote <strong>nurodyta valiuta</strong>, kad <strong>valiutos tipo</strong> pasirinkite valiutos kodas. Šis laukas negalimas, jei pasirinkote <strong>numatytąja valiuta</strong>, kad <strong>valiutos rūšį</strong> srityje.</td>
</tr>
<tr class="odd">
<td>Balanso limito tipas</td>
<td>Pasirinkite vieną iš galimos reikšmės:
<ul>
<li><strong>Maksimalus</strong> – grynųjų pinigų balansas neturėtų būti leidžiama viršyti, <strong>balanso riba</strong> suma grynųjų pinigų sąskaitos (viršutinė riba).</li>
<li><strong>Minimalus</strong> – grynųjų pinigų balansas neturėtų būti leidžiama toliau eiti į <strong>balanso riba</strong> suma grynųjų pinigų sąskaitos (jungiasi iš apačios).</li>
</ul></td>
</tr>
<tr class="even">
<td>Tikrinti balanso limitą</td>
<td>Pasirinkite, kas įvyksta piniginių dokumentų patvirtinimo procesas, jei su <strong>balanso riba</strong> suma viršijo grynųjų pinigų sąskaitą:
<ul>
<li><strong>Priimti</strong> – riba gali būti viršyta.</li>
<li><strong>Įspėjimas</strong> -riba gali būti viršyta, bet vartotojas gauna įspėjimą. Grynųjų pinigų dokumentas yra patvirtinta arba patvirtinta.</li>
<li><strong>Klaida</strong> – limitas negali būti viršytas. Vartotojas gauna klaidos pranešimą, ir grynųjų pinigų dokumentas nėra patvirtinta arba patvirtinta.</li>
</ul>
Ieškokite daugiau informacijos apie grynųjų pinigų dokumentų patvirtinimo procesas, kad &quot;grynųjų pinigų operacijų patvirtinimo ir registravimo&quot; skyriuje, šioje temoje.</td>
</tr>
<tr class="odd">
<td>Balanso limitas</td>
<td>Įveskite apribojimą grynųjų pinigų sąskaitos likutį. Suma turėtų būti valiuta, kurią nurodėte.</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a>Pinigais, registravimo šablonų nustatymas

Pinigais, registravimo šablonus apibrėžti registravimus į DK. Norėdami nustatyti registravimo šablonas pinigų, eikite į **pinigų****ir banko valdymo**&gt;**nustatymo**&gt;**pinigų registravimo šablonus**, ir pasirinkite arba sukuriate registravimo šabloną. Įveskite toliau nurodytą informaciją.

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
<td>Pasirinkti, ar registravimo šablonas taikomas konkrečių išmokų sąskaitoje arba visų grynųjų pinigų sąskaitų:
<ul>
<li><strong>Stalas</strong> – jei yra registravimo profilis linija grynųjų pinigų sąskaitos, šios eilutės lėšos naudojamos grynųjų pinigų operacijų registravimui.</li>
<li><strong>Visi</strong> -nėra registravimo profilis linijos grynųjų pinigų sąskaitos.</li>
</ul></td>
</tr>
<tr class="even">
<td>Grynieji pinigai</td>
<td>Jei pasirinkote <strong>stalo</strong>, kad <strong>galioja</strong> nurodykite grynųjų pinigų sąskaitą. Šis laukas paliekamas tuščias, jei pasirinkote <strong>visus</strong>, į <strong>galioja</strong> srityje.</td>
</tr>
<tr class="odd">
<td>DK sąskaita</td>
<td>Įveskite DK sąskaitą, skirtą naudoti kaip galutinę ataskaitą grynųjų pinigų sąskaitos numerį.</td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a>Grynųjų pinigų dokumentų numeracijų nustatymas

Nustatyti grynųjų dokumentų numeracijas, eikite į **pinigų ir banko valdymo**&gt;**nustatymo**&gt;**grynaisiais pinigais ir banko valdymo parametrai**. Dėl į **skaičių seka** skirtuko lape nurodyti numeracijos kodus, su **grynųjų pinigų kompensacijos kvitus**, **grynųjų pinigų išmokėjimo kvitus**, **pinigų korekcija kuponą**, ir **valiutos kurso** dokumentus, ir **grynųjų pinigų ataskaitos numeris**.

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a>Nustatyti numatytąsias vertes, grynaisiais pinigais ir banko valdymo parametrai

Nustatyti numatytąsias vertes, grynaisiais pinigais ir banko valdymo parametrų kasos funkcijoms, pereikite prie **pinigų ir banko sąskaitos tvarkymo**&gt;**nustatymo**&gt;**grynųjų pinigų ir banko valdymo parametrai**. Dėl to **pinigų** skirtuko lape įveskite šią informaciją.

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
<td>Pasirinkite numatytąjį grynųjų pinigų sąskaitos žurnaluose.</td>
</tr>
<tr class="even">
<td>Grynųjų registravimas</td>
<td>Įveskite registravimo šabloną, kuris yra naudojamas, jei nenurodytas joks kitą registravimo šabloną numatytasis pinigų.</td>
</tr>
<tr class="odd">
<td>Panaudotų kvitų kontrolė</td>
<td>Pasirinkite, kas įvyksta pinigų dokumento numerį patikrinimo metu radus Pasikartojantys skaičiai:
<ul>
<li>Neleisti dubliuoti</li>
<li>Atmesti kopijų per finansinius metus</li>
<li>Leisti dubliavimą</li>
<li>Perspėjimas apie dublikatus</li>
</ul></td>
</tr>
<tr class="even">
<td>Tikrinti operacijų limitą</td>
<td>Nurodykite, kas kyla, jei viršijamas operacijų su sąveikos objektai:
<ul>
<li><strong>Priimti</strong> – riba gali būti viršyta.</li>
<li><strong>Įspėjimas</strong> -riba gali būti viršyta, bet vartotojas gauna įspėjimą. Operacija užregistruota.</li>
<li><strong>Klaida</strong> – limitas negali būti viršytas. Vartotojas gauna klaidos pranešimą, ir operacija nėra paskelbtas.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tikrinimo metodas</td>
<td>Pasirinkite tikrinimo metodas, naudojamas kontrolės viršijamos ribinės sumos operacijoms:
<ul>
<li><strong>Operacija</strong> – patvirtinimo daroma už sandorį</li>
<li><strong>Sutarties</strong> – patvirtinimo daroma už sandorį, kuriame yra nurodytas sutartyje su sąveikos objektu.</li>
</ul></td>
</tr>
<tr class="even">
<td>Operacijų limitas</td>
<td>Įveskite didžiausią leistiną operacijų su sąveikos objektai grynaisiais pinigais.</td>
</tr>
<tr class="odd">
<td>Registravimas ankstesne data</td>
<td>Pažymėkite šį žymės langelį, kad įgalintumėte grynųjų pinigų operacijos turi būti registruojamos iki paskutinės dienos grynųjų pinigų operacijos.</td>
</tr>
<tr class="even">
<td>Dimensijos</td>
<td>Įveskite matmenis į <strong>skyriaus kodas</strong>, <strong>analizės kodas</strong>, ir <strong>paskirties kodas</strong> laukus. Grynųjų pinigų dokumentų spausdinimo formos atspindi šią informaciją.</td>
</tr>
<tr class="odd">
<td>Naudoti patvirtinimo būseną</td>
<td>Pažymėkite šį žymės langelį norint naudoti papildomą būseną, <strong>patvirtino</strong>, atliekant grynųjų dokumentų patvirtinimo procesą. (Daugiau informacijos ieškokite į &quot;grynųjų pinigų operacijų patvirtinimo ir registravimo&quot; skirsnyje.)</td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a>Nustatyti grynųjų pinigų žurnalų pavadinimai paprastai knygos

Sukurti grynųjų pinigų operacijų registravimo žurnalą, pereikite prie **bendrosios knygos**&gt;**žurnalo nustatymą**&gt;**žurnalų pavadinimai**, ir sukurti naują įrašą. – Į **žurnalo tipą** nurodykite **pinigų**. Nustatyti kitus parametrus, numatytasis žurnalo kiek reikės.

## <a name="daily-cash-operations-via-a-slip-journal"></a>Dienos grynųjų pinigų operacijas, važtaraščio žurnalą
Sukurti pinigų dokumentą per važtaraščio žurnalą, pereikite prie **pinigų ir banko sąskaitos tvarkymo**&gt;**grynųjų pinigų sandoriai**&gt;**važtaraščio žurnalą**, ir sukurti naują žurnalą. Veiksmų srityje spustelėkite **linijos**. Pridėti naują eilutę ir įveskite toliau nurodytą informaciją.

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
<td>Pasirinkite grynųjų pinigų sąskaitą. Pagal numatytuosius nustatymus išmokų sąskaitoje nurodyta grynųjų pinigų ir banko valdymo parametrus.</td>
</tr>
<tr class="odd">
<td>aprašymas</td>
<td>Įveskite operacijos paaiškinantis tekstas.</td>
</tr>
<tr class="even">
<td>Debetas kreditas</td>
<td>Grynųjų pinigų dokumente sumą įrašykite vieną iš šių laukų:
<ul>
<li><strong>Debeto</strong> – Naudokite šį lauką norėdami registruoti piniginių įplaukų ir piniginių kompensacijų kvitų.</li>
<li><strong>Kredito</strong> – Naudokite šį lauką norėdami registruoti grynųjų išlaidų ir grynųjų pinigų išmokėjimo kvitą.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Korespondentinės sąskaitos tipas korespondentinė sąskaita</td>
<td>Pasirinkite korespondentinę sąskaitą, kuri tipo ir kompensuoti sąskaitos numerį.</td>
</tr>
<tr class="even">
<td>Valiuta</td>
<td>Pasirinkite operacijos valiutos kodas.</td>
</tr>
<tr class="odd">
<td>Kvitas</td>
<td>Šiame lauke užpildomas automatiškai, remiantis žurnalo nustatyme.</td>
</tr>
<tr class="even">
<td>Užsakymo numeris</td>
<td>Jei nėra kitų numeracija nustatyta grynųjų pinigų sąskaitos, šiame lauke automatiškai įvedama, pagal numeraciją, kuri yra nurodyta. Galite patys įvesti užsakymo numerį į šį lauką kiek reikės. Siekiant užkirsti kelią inconsistence iš grynųjų pinigų dokumentų numeravimas, taikyti šią kontrolę: grynųjų pinigų dokumentas, kuris buvo anksčiau operacijos skaičius negali būti didesnis nei skaičius pinigų dokumentą, kuris turi vėlesnį operacija. Jei jums nereikia šį valdiklį, pasirinkite į <strong>skelbti anksčiau</strong> pinigų ir banko valdymo parametrai esantis žymės langelis.</td>
</tr>
<tr class="odd">
<td>Patvirtinimo būsena</td>
<td>Pirmosios operacijos būsena yra <strong>nei viena</strong>. Ieškokite informacijos, kaip nustatyti operacijos būseną, kad &quot;grynųjų pinigų operacijų patvirtinimo ir registravimo&quot; skyriuje.</td>
</tr>
<tr class="even">
<td>Dokumento tipas </td>
<td>Šį lauką su <strong>grynųjų pinigų užsakymas</strong> tab užpildomas automatiškai pagal kiekį, kurį įvedėte grynųjų pinigų dokumentas:
<ul>
<li><strong>Grynųjų pinigų kvito</strong> – Ši reikšmė naudojama, jei įvedėte suma į <strong>debeto</strong> lauko grynųjų pinigų sąskaitos.</li>
<li><strong>Grynųjų pinigų išmokėjimo kvitą</strong> – Ši reikšmė naudojama, jei įvedėte suma ir <strong>kredito</strong> lauko grynųjų pinigų sąskaitos</li>
<li><strong>Korekcija</strong> – į arba įvesti neigiamą likvidacinę sumą, <strong>debeto</strong> lauko arba <strong>kredito</strong> lauko grynųjų pinigų sąskaitos.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PVM grupė</td>
<td>Nurodyti operacijos mokesčius apskaičiuoti PVM grupę.</td>
</tr>
<tr class="even">
<td>Prekės PVM grupė</td>
<td>Nurodyti prekės PVM grupė apskaičiuoti mokesčius veikimą.</td>
</tr>
<tr class="odd">
<td>Priežastis</td>
<td>Dėl to <strong>grynųjų pinigų užsakymas</strong> skirtuką, įveskite tekstą, kurį apibūdina sandorio objektas. Šis tekstas bus spausdinamas grynųjų pinigų kvito ataskaitos formą.</td>
</tr>
<tr class="even">
<td>Dokumento data</td>
<td>Įveskite aprašymą, numeris ir data, pagrindinis dokumentas, yra priežastis, dėl sandorio (pvz., išankstinių ataskaitų, SF ar užsakymo).</td>
</tr>
<tr class="odd">
<td>Atstovo tipas</td>
<td>Šį lauką galima naudoti šias vertes:
<ul>
<li><strong>Darbuotojas</strong> – <strong>atstovas</strong> peržvalgos yra darbuotojų sąrašą, jei į <strong>korespondentinė sąskaita</strong> laukas yra nustatytas <strong>knygos</strong> ar <strong>banko</strong>, arba sąrašas pagal sąveikos objekto kontaktinius asmenis, jei su <strong>korespondentinė sąskaita</strong> laukas yra nustatytas <strong>klientų</strong> ar <strong>tiekėjo</strong>. Norėdami nustatyti atstovai, eikite į <strong>pagrindinio</strong>&gt;<strong>nustatymo</strong>&gt;<strong>Kontaktai</strong>&gt;<strong>Kontaktinis asmuo</strong>.</li>
<li><strong>Kitos</strong> – <strong>atstovas</strong> peržvalgos yra kitų klientų sąrašas. Nustatyti imtuvai, kurie nerodomi, <strong>klientų</strong> ar <strong>pardavėjai</strong> lentelėje, eikite į <strong>DK</strong>&gt;<strong>imtuvai</strong>. Šis tipas yra galimas tik Latvijoje. (Kad <strong>CSELatvia</strong> turėtų būti įgalinti konfigūracijos raktą.)</li>
<li><strong>Tiekėjas</strong> – <strong>atstovas</strong> peržvalgos yra tiekėjų sąrašas. Norėdami nustatyti tiekėjų, eikite į <strong>mokėtinos sumos</strong>&gt;<strong>pardavėjai</strong>.</li>
<li><strong>Klientų</strong> – <strong>atstovas</strong> peržvalgos yra pirkėjų sąrašas. Pirkėjų nustatymas, eikite į <strong>gautinos sąskaitos</strong>&gt;<strong>klientų</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Atstovas</td>
<td>Pasirinkite tipą, kurį nurodėte atstovas į <strong>tipiška rūšis</strong> srityje.</td>
</tr>
<tr class="odd">
<td>Asmens vardas</td>
<td>Šis laukas užpildomas automatiškai, remiantis į <strong>korespondentinė sąskaita</strong> ir <strong>atstovas</strong> laukus. Grynųjų pinigų kvituose spausdinimo formą atspindi šią informaciją.</td>
</tr>
<tr class="even">
<td>Tapatybės kortelė</td>
<td>Šiame lauke užpildomas automatiškai, remiantis kontaktinio asmens (atstovo) asmens tapatybės kortelės duomenų. Jei su <strong>korespondentinės sąskaitos tipas</strong> laukas yra nustatytas <strong>iš anksto laikiklis</strong>, ir <strong>korespondentinė sąskaita</strong> laukas yra nustatytas darbuotojo numerį, pinigų įplaukos ar išlaidos gali būti padaryta iš arba darbuotojui. Šiuo atveju į <strong>tapatybės kortelę</strong> laukas užpildomas automatiškai, naudojant duomenis iš asmens tapatybės kortelės, <strong>darbuotojo</strong> lentelės (<strong>personalo apskaitos</strong>&gt;<strong>darbuotojų lentelėje</strong>).</td>
</tr>
<tr class="odd">
<td>Paskirtis</td>
<td>Į, <strong>tikslas</strong> lentelė, nurodyti vieną ar daugiau paskirties vietų kodai sandorio sumos. Pažymėkite paskirties vietos kodą, į <strong>tikslas</strong> lauko ir paaiškinimą dėl <strong>operacijos tekstas</strong> srityje. – Į <strong>sumos</strong> įveskite sumą sandorio valiuta. Į <strong>proc</strong> lauko rodo, procentais, paskirties sumą iš viso sandorio sumos santykis.</td>
</tr>
<tr class="even">
<td>Likutis</td>
<td>Likusią sumą, kuri skaičiuojama. Atkreipkite dėmesį, kad visos sandorio sumos turi būti priskirtos paskirties vietų kodai.</td>
</tr>
<tr class="odd">
<td>Tarnautojai</td>
<td>Dėl to <strong>pareigūnų</strong> skirtuko lape nurodyti atsakingų asmenų vardai ir pavadinimai: direktorius, Vyriausiasis buhalteris ir kasininkas. Į <strong>pozicijos</strong> reikšmės nustatomos nustatymą, pareigūnai apie į <strong>bendrojo</strong> ir <strong>knygos</strong> skirtukų į <strong>pareigūnų</strong> puslapis (<strong>pagrindinio</strong>&gt;<strong>sąrankos</strong>&gt;<strong>Kontaktai</strong>&gt;<strong>pareigūnų</strong>).</td>
</tr>
<tr class="even">
<td>Išankstinis mokėjimas</td>
<td>Pažymėti šį žymės langelį, jei sandoris yra išankstinis.</td>
</tr>
<tr class="odd">
<td>Registravimo šablonas</td>
<td>Įveskite registravimo šabloną grynųjų pinigų sąskaitą. Pagal numatytuosius nustatymus naudojamas registravimo šablonas, nenurodytas grynųjų pinigų ir banko valdymo parametrų.</td>
</tr>
<tr class="even">
<td>Koresp. registravimo šablonas</td>
<td>Įveskite registravimo šablonas pasirinktas korespondentinę sąskaitą.</td>
</tr>
<tr class="odd">
<td>Bendra suma</td>
<td>– Į <strong>bendra suma</strong> laukų grupėje puslapio apačioje, <strong>kelion</strong> sumai, kuri apskaičiuojama už visų grynųjų pinigų kompensacijos kvitų, yra įrašytas šiame žurnale, lauke ir <strong>Disb</strong> lauke nustatytas bendras visų grynųjų pinigų išmokėjimo kvitus.</td>
</tr>
</tbody>
</table>

Norėdami patikrinti žurnalo įrašus, į veiksmų sritį, spustelėkite **patvirtinti**.

## <a name="daily-cash-operations-via-a-general-journal"></a>Dienos grynųjų pinigų operacijas per bendrąjį žurnalą
Sukurti atlikti grynųjų pinigų sandorių per bendrąjį žurnalą, pereikite prie **bendrosios knygos**&gt;**žurnalo įrašus**&gt;**bendrųjų žurnalų**, ir sukurti naują žurnalą. Veiksmų srityje spustelėkite **linijos**. Pridėti naują eilutę ir įveskite toliau nurodytą informaciją.

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
<td>Pasirinkite <strong>kasos</strong>.</td>
</tr>
<tr class="odd">
<td>Paskyra</td>
<td>Pasirinkite grynųjų pinigų sąskaitos numerį.</td>
</tr>
<tr class="even">
<td>Operacijos tekstas</td>
<td>Įveskite operacijos paaiškinantis tekstas.</td>
</tr>
<tr class="odd">
<td>Debetas kreditas</td>
<td>Grynųjų pinigų dokumente sumą įrašykite vieną iš šių laukų:
<ul>
<li><strong>Debeto</strong> – Naudokite šį lauką norėdami registruoti piniginių įplaukų ir piniginių kompensacijų kvitų.</li>
<li><strong>Kredito</strong> – Naudokite šį lauką norėdami registruoti grynųjų išlaidų ir grynųjų pinigų išmokėjimo kvitą.</li>
</ul></td>
</tr>
<tr class="even">
<td>Korespondentinės sąskaitos tipas korespondentinė sąskaita</td>
<td>Pasirinkite korespondentinę sąskaitą, kuri tipo ir kompensuoti sąskaitos numerį.</td>
</tr>
<tr class="odd">
<td>Valiuta</td>
<td>Pasirinkite operacijos valiutos kodas.</td>
</tr>
</tbody>
</table>

Dėl to **SF** pažymėtame lape galite nurodyti registravimo šablonų pasirinktą sąskaitą ir korespondentinę sąskaitą. Jei registruoti operaciją išankstinį apmokėjimą, pažymėkite į **išankstinio mokėjimo** žymės langelį į **mokėjimo** tab. – Į **atstovas** laukų grupėje, užpildykite laukus kaip tu slydimo žurnalo eilutėms, spausdinti, **pinigų** ataskaita. Norėdami patikrinti žurnalo įrašus, į veiksmų sritį, spustelėkite **patvirtinti**.

## <a name="cash-transaction-approval-and-posting"></a>Grynųjų pinigų operacijos patvirtinimas ir registravimas
Už grynųjų pinigų sandorius, gali būti taikomos šių būsenų: **nėra**, **patvirtino**, **patvirtinta**, ir **atmesta**. A **naudoti patvirtinti būsenos** parametro, **patvirtinimo** FastTab, į **pinigų** skirtuką ne **pinigų ir banko sąskaitos tvarkymo**&gt;**sąrankos**&gt;**grynaisiais pinigais ir banko valdymo parametrai** leidžia įjungti papildomą būsena: **patvirtinta** ir **atmesta**. Patvirtinimas yra tinkama kai pinigais dokumentai išduodami, ir pinigų įplaukų ar išlaidų dalijasi du darbuotojai: buhalteris ir kasininkas. Ir **iš naujo būsena** funkciją keičia dabartinės operacijos būsena. **Patvirtinti** tampa **patvirtino**, ir **patvirtino** tampa **niekas**. Pinigų žurnalo įrašus galima redaguoti tik tada, kai būsena yra **nei viena**. Grynųjų pinigų operacijos gali būti atmestas, tik jei operacijos būsena yra **patvirtino**. Atmestas pinigais dokumentai yra įtraukti į į **grynųjų dokumentų registracijos žurnalas** ataskaitą, bet jie yra ne atsispindi ir **kasos knyga** ataskaita. Patvirtinti sandorį, pasirinkite atitinkamą slydimo žurnalo eilutę, o tada spustelėkite **dokumentų patvirtinimo**&gt;**patvirtinti**. Užsakymo numeris yra sukurtas, remiantis nurodytos numeracijos. Operacijų būsena pakeista į **patvirtino**, ir jūs nebegalite redaguoti žurnalo eilutės. Grynųjų pinigų sąskaitos balansas išlieka nepakitęs. Atsisakyti pinigų dokumentą, spustelėkite **dokumentų patvirtinimo**&gt;**atmesti**. Ši parinktis galima tik tiems dokumentams, kurie turi **patvirtino** statusas. Patvirtinti operaciją, pasirinkite atitinkamą slydimo žurnalo eilutę, ir spustelėkite **dokumentų patvirtinimo**&gt;**tvirtinti**. Į **patvirtinta** būsena rodo, kad pinigų lėšos buvo gautos arba išeikvota. Grynųjų pinigų balansas pasikeičia. Grynųjų pinigų operacijos gali būti registruojamos. Atšaukti yra **patvirtinta** statusą ir nustatyti iš naujo būseną į **nė vienas**, spustelėkite **dokumentų patvirtinimo**&gt;**iš naujo būsena**. Tik patvirtinti grynųjų pinigų operacijos gali būti registruojamos. Jei norite užregistruoti žurnalą, spustelėkite **po**&gt;**po**.

## <a name="print-a-cash-order"></a>Spausdinti grynųjų pinigų užsakymas
Spausdinti grynųjų pinigų užsakymas, pasirinkite slydimo žurnalo eilutę, ir tada į veiksmų sritį, spustelėkite **spausdinti**&gt;**grynųjų pinigų užsakymo ataskaitos**. Sistema sugeneruoja grynųjų kvito arba grynųjų pinigų išmokėjimo kvitą, priklausomai nuo to, ar suma įrašoma į spausdinimo formą į **debeto** lauko, arba **kredito** lauko pasirinktos eilutės:

-   Jei yra daug, kad **debeto** srityje: grynųjų pinigų kvito
-   Jei yra daug, kad **kredito** srityje: grynųjų pinigų išmokėjimo kvitą

Slydimo žurnalo eilutėms, kurios pažymėtos **patvirtino**, **patvirtinta**, arba **atmesta** būsena gali būti spausdinami. Taip pat galite spausdinti pinigų užsakymo dokumentus **pinigų ir banko sąskaitos tvarkymo**&gt;**Inquires ir ataskaitos**&gt;**grynųjų pinigų užsakymas**.

## <a name="periodic-tasks"></a>Periodinės užduotys
Šias užduotis gali būti atliekama **pinigų ir banko valdymo**&gt;**periodines užduotis**.

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
<td>Patikrinti pasirinkto grynųjų pinigų sąskaitos likutį nurodytą dieną, ir parodyti jos rezultatą informacinis pranešimas. Tik patvirtintas operacijas galima suskaičiuoti balansą skaičiavimo. Operacijos, kurios pažymėtos kaip <strong>už darbo užmokesčio</strong> nelaikomi.</td>
</tr>
<tr class="even">
<td>Grynųjų balanso perskaičiavimas</td>
<td>Naudokite šią užduotį užtikrinti, kad DK likučiai grynųjų pinigų sąskaitų tinka grynųjų pinigų balansas.</td>
</tr>
<tr class="odd">
<td>Grynųjų pinigų ataskaitos kūrimas (Lenkija)</td>
<td>Kurti su <strong>pinigų</strong> ataskaita. Į <strong>pinigų</strong> ataskaitos numeris yra sukuriamas pagal numeraciją, kuri yra nustatyta <strong>ataskaitos numeris</strong>. Dialogo lange užduoties, be to <strong>iki šiol</strong>, pasirinkti paskutinę datą, kurioje pinigų operacijas skaičiuoti už į <strong>pinigų</strong> ataskaita. Naudoti su <strong>filtras</strong> veikia ir <strong>įrašus įtraukti</strong> tab, jei norite nurodyti papildomų kriterijų, apribojantį grynųjų pinigų operacijos parinkimas. Šie kriterijai gali būti grynųjų pinigų sąskaitų numerius ir valiutos kodus. – Su <strong>sukurti</strong> pasirinkite vartotojo, kuris yra atsakingas už ataskaitos kūrimas. Norėdami peržiūrėti į <strong>pinigų</strong> ataskaitą, sukurtą, naudoti su <strong>grynųjų pinigų ataskaitos</strong> mygtuką į <strong>iždo sąskaitos</strong> puslapis.</td>
</tr>
<tr class="even">
<td>Pinigai - valiutos koregavimo FIFO ir LIFO (Lenkija)</td>
<td>Apskaičiuokite už Lenkijos standartų derinimas dėl valiutos kurso. Naudoti su <strong>filtras</strong> veikia ir <strong>įrašus įtraukti</strong> tab, jei norite nurodyti pinigų sąskaitą, vykdyti užduotis. Pasirinkite į <strong>perskaičiavimą</strong> žymės langelį, kad tai visiškai perskaičiavimas keitimo reguliavimo skirtumas už visus atvirus laikotarpius. Štai kaip apskaičiuojama valiutos kurso kai pirmasis, pirmas iš (FIFO), Paskutinis, pirmas (FIFO) metodai naudojami produktai:
<ul>
<li><strong>FIFO metodas</strong> – sistema ieško išlaidų operacijas, ankstesnės operacijos datos (mažesnės eilės numeris) ir nusėda su gavimo operaciją, kuriame yra ankstesnės operacijos datos (mažesnės eilės numeris).</li>
<li><strong>LIFO metodas</strong> – sistema ieško išlaidų operaciją, kurią turi vėlesnės operacijos data (didesnės eilės numeris) ir nusėda su gavimo operaciją, kurios yra vėlesnės operacijos data (didesnės eilės numeris).</li>
</ul>
Atsiskaityta suma atsispindi ir <strong>atsiskaitoma valiuta</strong> lauko ir <strong>grynųjų pinigų operacijos</strong> puslapis. Jei valiutos kurso koregavimas, suma atsispindi į <strong>valiutos kurso sumą</strong> srityje, ir operacijos, kurios, <strong>valiutos kurso skirtumas</strong> dokumento tipą gaminama su <strong>grynųjų pinigų operacijos</strong> stalo. Pelno/nuostolio operacijų DK sąskaitas išdėstyti į <strong>valiuta</strong> lentelės (<strong>kursas finansines pelno</strong> ir <strong>kursas finansinių nuostolių</strong>).</td>
</tr>
<tr class="odd">
<td>Užsienio valiutos kurso pasikeitimas – grynieji pinigai</td>
<td>Naudokite šią užduotį atskaitomybės datą įvedus operacijas užsienio valiuta yra tolygios pusiausvyros numatytąja valiuta. Naudoti su <strong>filtras</strong> veikia ir <strong>įrašus įtraukti</strong> tab, jei norite nurodyti pinigų sąskaitą, vykdyti užduotis. Dialogo lange užduoties, naudoti su <strong>nuo valiutos</strong> ir <strong>į valiutos</strong> laukus ir taip nurodysite sandorio valiutų. Sistemą galima palyginti ta valiuta, kuri buvo pakeista naudojant valiutos kurso pasirinktai dienai suma numatytąja valiuta. Skirtumas tarp šių dviejų sumų (išskyrus ankstesnės valiutos kurso) yra apskaičiuotas valiutos kurso. Šią užduotį sukuria patvirtintose grynųjų pinigų operacijos, kad <strong>valiutos kurso</strong> tipo. DK operacijos susidaro naudojant DK sąskaitą pinigų ir DK sąskaita, kuri nurodyta <strong>nerealizuoto pelno</strong> ar <strong>nerealizuota neigiama įtaka</strong>, į <strong>valiuta</strong> lentelę.</td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a>Užklausos ir ataskaitos
| Užklausą ar ataskaitą                             | aprašymas                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Grynųjų pinigų operacijos Rodyti                        | Slydimo žurnalo eilutei, naudoti su **tyrimai** mygtuką veiksmų srityje Peržiūrėti DK operacijas, grynųjų pinigų balansas ir kita informacija.                                                                                  |
| Operacija grynaisiais                              | Eikite į **pinigų ir banko valdymo**&gt;**užklausų ir ataskaitų**&gt;**grynųjų pinigų sandorius** Peržiūrėti grynųjų pinigų operacijos. Naudoti su **filtras** funkcija nustatyti papildomų kriterijų, apribojantį grynųjų pinigų operacijos parinkimas. |
| (Estija, Rusija), registracijos žurnalas | D. ataskaitos **pinigų ir banko valdymo**&gt;**užklausų ir ataskaitų**&gt;**registracijos žurnalas** atspindi visų grynųjų pinigų kompensacijos ir grynųjų pinigų išmokėjimo kvitus, kurie buvo išduoti.                                   |
| Kasos knyga (, Latvija, Lietuva, Rusija)     | D. ataskaitos **pinigų ir banko valdymo**&gt;**užklausų ir ataskaitų**&gt;**kasos knygoje ataskaita** atspindi faktiniai pinigų fondo judėjimas (įplaukos ir išlaidos).                                                            |




