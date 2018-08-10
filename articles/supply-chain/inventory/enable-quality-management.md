---
title: "Kokybės valdymo peržiūra"
description: "Šioje temoje aprašoma, kaip galima naudoti kokybės valdymą „Microsoft Dynamics 365 for Finance and Operations“, siekiant pagerinti tiekimo grandinės produktų kokybę."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 79b3127f726a08cc24c20145b5ad9969157a899c
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="quality-management-overview"></a>Kokybės valdymo peržiūra

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip galima naudoti kokybės valdymą „Microsoft Dynamics 365 for Finance and Operations“, siekiant pagerinti tiekimo grandinės produktų kokybę.

Kokybės valdymas gali padėti valdyti apgręžimo laiką tvarkant neatitinkančius produktus, neatsižvelgiant į kilmę. Kadangi diagnozės tipai yra susiję su koregavimo ataskaitomis, „Microsoft Dynamics 365 for Finance and Operations‟ gali planuoti užduotis ir jomis taisyti problemas bei neleisti joms pasikartoti.

Be funkcijų, skirtų valdyti neatitikimui, kokybės valdymas apima funkcijas, skirtas problemoms sekti pagal jų tipą (net vidaus problemoms) ir sprendimams identifikuoti kaip trumpalaikiams ar ilgalaikiams. Statistika apie pagrindinius našumo indikatorius (KPI) teikia įžvalgų apie ankstesnių neatitikimo problemų istoriją ir sprendimus, kurie buvo naudojami joms taisyti. Galite naudoti praeities duomenis ir peržiūrėti ankstesnių kokybės priemonių efektyvumą bei nustatyti tinkamas priemones, kurios bus naudojamos ateityje.

Kai nustatote kokybės susiejimą, „Finance and Operations‟ gali generuoti įvairių verslo procesų, įvykių ir sąlygų kokybės užsakymus. Kokybės susiejimas gali apimti konkrečią prekę, konkrečią prekių grupę arba visas prekes.

## <a name="examples-of-the-use-of-quality-management"></a>Kokybės valdymo naudojimo pavyzdžiai
Kokybės valdymas yra lankstus ir gali būti diegiamas įvairiais būdais, siekiant atitikti konkrečių tiekimo grandinės operacijų lygių reikalavimus. Toliau pateikti pavyzdžiai iliustruoja galimą šių funkcijų naudojimą.

-   Pagal iš anksto nustatytus kriterijus automatiškai paleisti kokybės kontrolės procesą (sandėlyje registravus pirkimo užsakymą iš konkretaus tiekėjo).
-   Tikrinimo metu blokuoti atsargas, siekiant neleisti naudoti nepatvirtintų atsargų (visiškas pirkimo užsakymų kiekių blokavimas).
-   Kaip kokybės susiejimo dalį naudoti prekių pavyzdžių ėmimą, siekiant apibrėžti dabartinių faktinių atsargų, kurias reikia tikrinti, sumą. Pavyzdžių ėmimas gali būti paremtas fiksuotais kiekiais arba procentine dalimi.
-   kurkite dalinių kvitų kokybės užsakymus. Norėdami kurti kokybės užsakymą, pagrįstą faktiškai su užsakymu gautu kiekiu, formoje **Prekės pavyzdžio ėmimas** turite pažymėti žymės langelį **Pagal atnaujintą kiekį**.
-   Kurti testų tipus, apimančius minimalias, maksimalias ir paskirties testo reikšmes, ir atlikti kokybės–kiekybės tikrinimą su iš anksto nustatytais tikrinimo rezultatais.
-   Nurodyti priimtiną kokybės lygį (AQL), siekiant kontroliuoti leistinus kokybės matavimo nuokrypius.
-   Nurodyti išteklius, kurių reikia tikrinimo operacijai, pvz., tikrinimo sritį ir tikrinimo priemones.

## <a name="working-with-quality-associations"></a>Darbas su kokybės susiejimais
Verslo procesas, kuris naudoja kokybės susiejimą, gali būti susijęs su įvairiais šaltinio dokumentais, pvz., pirkimo užsakymais, pardavimo užsakymais ar gamybos užsakymais.

Kiekvienas kokybės susiejimo įrašas apibrėžia bandymų rinkinį, AQL ir pavyzdžių ėmimo planą, kuris taikomas generuojamiems kokybės užsakymams. Turite apibrėžti kiekvieno verslo proceso varianto kokybės susiejimo įrašą. Pavyzdžiui, galite nustatyti kokybės susiejimą, kuris generuoja kokybės užsakymą, kai atnaujinamas pirkimo užsakymo produktų kvitas. Atsižvelgiant į vykdymo plano sąranką, esant atidarytam kokybės užsakymui, gali būti blokuojamas pats paleidimo procesas, arba gali būti blokuojami tolesni procesai, pvz., pirkimo užsakymų SF išrašymas.

**Pastaba.** Kol yra atidarytų kokybės užsakymų, automatiškai blokuojamas atsargų kiekių išdavimas. Atsižvelgiant į **Visiško blokavimo** nuostatą **Prekių pavyzdžių** puslapyje, kiekis yra arba kokybės užsakymo kiekis, arba šaltinio dokumento eilutės kiekis.

Nurodyto verslo proceso kokybės susiejimo įrašas identifikuoja įvykį ir sąlygas, kuriems sugeneruotas kokybės užsakymas. Sąlygos gali būti būdingos teritorijai arba juridiniam subjektui. Ardomuosius bandymus apimantis kokybės užsakymas gali būti sugeneruotas tik kai yra turimų įvykio atsargų.

Toliau pateikti pavyzdžiai iliustruoja, kaip kokybės susiejimo įrašas apibrėžiamas kiekvieno verslo proceso pokyčiams. Toliau pateiktoje lentelėje apibendrinami kiekvieno pavyzdžio įvykiai ir sąlygos, kuriuos apibrėžia kokybės susiejimo įrašas.

<table>
<tbody>
<tr>
<th>Nuorodos tipas</th>
<th>Įvykio tipas</th>
<th>Vykdymas</th>
<th>Įvykio blokavimas</th>
<th>Dokumento nuoroda</th>
</tr>
<tr>
<td>Atsargos</td>
<td>Netaikoma</td>
<td>Netaikoma</td>
<td>Nėra</td>
<td>Visi</td>
</tr>
<tr>
<td rowspan="7">Pardavimas</td>
<td rowspan="4">Išrinkimo procesas suplanuotas</td>
<td rowspan="4">Prieš</td>
<td>Nėra</td>
<td rowspan="22">Konkretus ID, Grupė arba tik Viskas.</td>
</tr>
<tr>
<td>Išrinkimo procesas</td>
</tr>
<tr>
<td>Važtaraštis</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="3">Važtaraštis</td>
<td rowspan="3">Prieš</td>
<td>Nėra</td>
</tr>
<tr>
<td>Važtaraštis</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="15">Pirkimas</td>
<td rowspan="7">Kvitų sąrašas</td>
<td rowspan="4">Prieš</td>
<td>Nėra</td>
</tr>
<tr>
<td>Kvitų sąrašas</td>
</tr>
<tr>
<td>Gavimo dokumentas</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="3">Po</td>
<td>Nėra</td>
</tr>
<tr>
<td>Gavimo dokumentas</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="3">Registracija</td>
<td rowspan="3">Netaikoma</td>
<td>Nėra</td>
</tr>
<tr>
<td>Gavimo dokumentas</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="5">Gavimo dokumentas</td>
<td rowspan="3">Prieš</td>
<td>Nėra</td>
</tr>
<tr>
<td>Gavimo dokumentas</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="2">Po</td>
<td>Nėra</td>
</tr>
<tr>
<td>PVM sąskaita faktūra</td>
</tr>
<tr>
<td rowspan="8">Gamyba</td>
<td rowspan="3">Registracija</td>
<td rowspan="3">Netaikoma</td>
<td>Nėra</td>
<td rowspan="12">Visi</td>
</tr>
<tr>
<td>Pranešti apie pabaigimą</td>
</tr>
<tr>
<td>Pabaigti</td>
</tr>
<tr>
<td rowspan="5">Pranešti apie pabaigimą</td>
<td rowspan="3">Prieš</td>
<td>Nėra</td>
</tr>
<tr>
<td>Pranešti apie pabaigimą</td>
</tr>
<tr>
<td>Pabaigti</td>
</tr>
<tr>
<td rowspan="2">Po</td>
<td>Nėra</td>
</tr>
<tr>
<td>Pabaigti</td>
</tr>
<tr>
<td rowspan="4">Sulaikymas</td>
<td rowspan="3">Pranešti apie pabaigimą</td>
<td rowspan="2">Prieš</td>
<td>Pranešti apie pabaigimą</td>
</tr>
<tr>
<td>Pabaigti</td>
</tr>
<tr>
<td>Po</td>
<td>Pabaigti</td>
</tr>
<tr>
<td>Pabaigti</td>
<td>Prieš</td>
<td>Pabaigti</td>
</tr>
<tr>
<td rowspan="3">Maršruto operacija</td>
<td rowspan="3">Pranešti apie pabaigimą</td>
<td rowspan="2">Prieš</td>
<td>Nėra</td>
<td rowspan="3">Konkretus ID, Grupė arba Viskas, ir Konkretaus ištekliaus, Grupė arba Viskas</td>
</tr>
<tr>
<td>Pranešti apie pabaigimą</td>
</tr>
<tr>
<td>Po</td>
<td>Nėra</td>
</tr>
<tr>
<td rowspan="3">Sudėtinio produkto gamyba</td>
<td>Registracija</td>
<td>Netaikoma</td>
<td rowspan="3">Nėra</td>
<td rowspan="3">Visi</td>
</tr>
<tr>
<td rowspan="2">Pranešti apie pabaigimą</td>
<td>Prieš</td>
</tr>
<tr>
<td>Po</td>
</tr>
</tbody>
</table>

Toliau pateiktoje lentelėje pateikiama daugiau informacijos apie tai, kaip galima generuoti konkrečių tipų procesų kokybės užsakymus.
<div class="tableSection">

<table>
<tbody>
<tr>
<th>Proceso tipas</th>
<th>Kai kokybės užsakymus galima generuoti automatiškai.</th>
<th>Kai kokybės užsakymus galima generuoti, jei reikia ardomojo bandymo.</th>
<th>Sąlygų informacija</th>
<th>Rankinio generavimo informacija</th>
</tr>
<tr>
<td>Pirkimo užsakymas</td>
<td>Prieš užregistruojant kvitų sąrašą arba gautos medžiagos kvitą, arba po to.</td>
<td>Užregistravus gautos medžiagos kvitą, nes medžiaga turi būti prieinama ardomajam bandymui.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, tiekėją arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pirkimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Sulaikymo užsakymas</td>
<td>Prieš sulaikymo užsakymą nurodant baigtu arba po to.</td>
<td>Kokybės užsakymų, kuriems reikia atlikti ardomuosius bandymus, generuoti negalima. Daroma prielaida, kad sulaikymo užsakymo funkcijos tvarko sunaikintos medžiagos perdavimą.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, tiekėją arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis sulaikymo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Pardavimo užsakymas</td>
<td>Prieš siunčiamų prekių suplanuotą paėmimo procesą ar važtaraščio naujinimą.</td>
<td>Atliekant bet kurį veiksmą.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę, klientą arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis pardavimo užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Gamybos užsakymas</td>
<td>Prieš pranešant apie baigtą gamybos užsakymo kiekį, arba po to.</td>
<td>Pranešus apie baigtą gamybos užsakymo kiekį.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis gamybos užsakymą, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Gamybos užsakymas su maršruto operacija</td>
<td>Prieš baigiant operacijos ataskaitą, arba po to.</td>
<td>Pranešus, kad paskutinės operacijos gamyba baigta.</td>
<td>Kokybės užsakymo reikalavimas gali rodyti tam tikrą teritoriją, prekę ar operacijų išteklių, arba šių sąlygų derinį.</td>
<td>Rankiniu būdu sugeneruotas kokybės užsakymas, rodantis maršruto operaciją, gali naudoti kokybės susiejimo įrašo informaciją, pvz., bandymų pavyzdžių ėmimo planą.</td>
</tr>
<tr>
<td>Atsargos</td>
<td>Kokybės užsakymo negalima automatiškai generuoti atsargų žurnalo operacijai arba perkėlimo užsakymo operacijoms.</td>
<td></td>
<td></td>
<td>Prekės atsargų kiekio kokybės užsakymą reikia kurti rankiniu būdu. Reikia faktiškai turimų atsargų.</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a>Kokybės valdymo puslapiai
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Puslapis</th>
<th>Prekės/Paslaugos pavadinimas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kokybės susiejimai</td>
<td>Žr. ankstesnius šio straipsnio skyrius.</td>
<td>Kokybės susiejimas apibrėžia visą toliau nurodytą generuojamo kokybės užsakymo informaciją.
<ul>
<li>Operacijos įvykį.</li>
<li>Prekių bandymų, kuriuos reikia atlikti, rinkinį.</li>
<li>AQL.</li>
<li>Pavyzdžių ėmimo planą.</li>
</ul>
Turite apibrėžti kiekvieno verslo proceso varianto, kuriam reikalingas automatinis kokybės užsakymų generavimas, kokybės susiejimą. Pavyzdžiui, galima generuoti pirkimo užsakymų, sulaikymo užsakymų, pardavimo užsakymų ir gamybos užsakymų verslo procesų kokybės užsakymą.</td>
</tr>
<tr class="even">
<td>Testai</td>
<td>Naudokite šį puslapį atskiriems tikrinimams, kuriais nustatoma, ar produktai atitinka kokybės reikalavimus, nustatyti ir peržiūrėti. Bandymų grupei galite priskirti vieną arba kelis atskirus bandymus. Šiuo atveju taip pat nurodote konkretaus bandymo informaciją, pvz., priimtinas matavimo reikšmes. Matavimo reikšmės naudojamos atliekant kiekybinius bandymus, o bandymų kintamieji naudojami atliekant kokybinius bandymus.
<ul>
<li>Kiekybinio bandymo tipas yra <strong>Sveikasis skaičius</strong> arba <strong>Trupmena</strong> ir taip pat nustatytas jo matavimo vienetas. Kokybės specifikacijos ir bandymų rezultatai išreiškiami skaičiais.</li>
<li>Kokybinio bandymo tipas yra <strong>Pasirinktinis</strong>. Kokybės bandymams reikia pateikti papildomos informacijos apie bandymų kintamąjį, kuris vertinamas ir jo sunumeruotas parinktis. Kokybės specifikacijos ir bandymų rezultatai išreiškiami atsižvelgiant į rezultatą.</li>
</ul></td>
<td>Gamybos įmonė atlieka du įsigytų medžiagų bandymus: kiekybinį bandymą dėl medžiagos kokybės ir kokybinį bandymą dėl pakuotės sugadinimo. Įmonė nurodo papildomos informacijos, susijusios su kokybės tikrinimu, pateikdama tikrinimo kintamąjį (pažeista pakuotė) ir jo rezultatus. Įmonė naudoja <strong>Bandymų grupių</strong> puslapį, kad bandymų grupei priskirtų šiuos du bandymus ir nurodytų konkretaus bandymo informaciją. Tikrinimų grupė priskiriama kokybės užsakymui tam, kad įmonė galėtų pateikti dviejų tikrinimų rezultatų ataskaitą.</td>
</tr>
<tr class="odd">
<td>Bandymo grupės</td>
<td>Naudodami šį puslapį galite nustatyti, redaguoti ir peržiūrėti bandymų grupei priskirtas bandymų grupes bei atskirus bandymus. Viršutinėje srityje rodomos tikrinimų grupės, o apatinėje srityje rodomi pasirinktai tikrinimų grupei priskirti tikrinimai. Bandymų grupei priskiriate keletą strategijų, pvz., pavyzdžių ėmimo planą, AQL ir ardomojo bandymo reikalavimą. Kai bandymų grupei priskiriate atskirą bandymą, apibrėžiate papildomą informaciją, pvz., seką, dokumentus ir galiojimo datas. Atliekant kiekybinį bandymą, jūsų apibrėžta informacija taip pat apima priimtinas matavimo reikšmes. Atliekant kokybinį bandymą, informacija apima bandymo kintamąjį ir numatytąjį rezultatą. Kokybės užsakymui priskirta bandymų grupė apibrėžia numatytąjį konkrečios prekės bandymų, kuriuos reikia atlikti, rinkinį. Tačiau kokybės užsakymo bandymus galite pridėti, naikinti arba keisti. Pateikiami kiekvieno kokybės užsakymo tikrinimo rezultatai.</td>
<td>Gamybos įmonė apibrėžia kiekvieno kokybės gairių varianto tikrinimų grupę. Įvairios bandymų grupės atspindi pavyzdžių ėmimo planų skirtumus, bandymų, kuriuos reikia atlikti vienu metu, rinkinius, AQL ir kitus veiksnius. Taip pat skirasi kiekybinių bandymų priimtinos matavimo reikšmės. Kad galiotų įmonės kokybės gairės, ji kiekvienai taisyklei priskiria bandymų grupę, kad <strong>Kokybės susiejimų</strong> puslapyje būtų automatiškai generuojami kokybės užsakymai, ir taip pat bandymų grupę priskiria rankiniu būdu sukurtiems kokybės užsakymams.</td>
</tr>
<tr class="even">
<td>Prekių kokybės grupės</td>
<td>Naudodami šį puslapį galite nustatyti, redaguoti ir peržiūrėti kokybės grupei priskirtas prekes arba kokybės grupes, priskirtas prekei. Kokybės grupė nurodo bendruosius prekių tikrinimo reikalavimus. <strong>Bandymų grupių</strong> puslapyje apibrėžę bandymų reikalavimus, galite apibrėžti taisykles, skirtas automatiškai generuoti kokybės užsakymams. Kad procesas būtų paprastesnis, nenustatinėkite taisyklių atskiroms prekėms. Vietoj to taisykles apibrėžiate kokybės grupei, naudodami <strong>Kokybės susiejimų</strong> puslapį. Taip pat galite naudoti pasirinktos kokybės grupės <strong>Prekių kokybės grupių</strong> puslapį, kad tai grupei priskirtumėte aktualias prekes. Taip pat galite naudoti pasirinktos prekės <strong>Prekių kokybės grupių</strong> puslapį, kad tai prekei priskirtumėte aktualias kokybės grupes.</td>
<td>Gamybos įmonė perka įvairių žaliavų, kurių gaunamų objektų patikrinimo bandymų reikalavimai tokie patys. Įmonė apibrėžia kokybės grupę ir tada tai grupei priskiria prekių numerius, susietus su žaliavomis. Vėliau įmonė perka naują žaliavos tipą, kurio bandymų reikalavimai tokie patys. Užuot nustatydama naujosios medžiagos naujus bandymų reikalavimus, įmonė naujos medžiagos prekės numerį prideda į esamą kokybės grupę. Ta pati gamybos įmonė taip pat gamina prekes, kurių gamybos bandymų reikalavimai tokie patys, ir siunčia prekes, kurių tie patys reikalavimai bandymams prieš siuntimą. Įmonė apibrėžia dvi papildomas kokybės grupes ir tada kiekvienai grupei priskiria atitinkamus prekių numerius.</td>
</tr>
<tr class="odd">
<td>Bandymo kintamieji</td>
<td>Naudokite šį puslapį, kad apibrėžtumėte ir peržiūrėtumėte kintamuosius, susietus su kokybiniu bandymu. Apibrėžiate kiekvieno kintamojo sunumeruotus rezultatus, atitinkančius galimas parinktis. Bandymai nustatomi <strong>Bandymų</strong> puslapyje. Kokybinių bandymų tipą turite nustatyti į <strong>Parinktis</strong>. Naudokite <strong>Bandymų grupių</strong> puslapį, kad atskiram bandymui priskirtumėte bandymo kintamąjį.</td>
<td>Gamybos įmonė, kepanti sausainius, naudoja galutinio produkto bandymą. Šis bandymas turi keletą kintamųjų. Vienas kintamasis yra skonis, ir galimi šio kintamojo rezultatai yra „geras“ ir „blogas“. Antras kintamasis yra spalva, ir galimi rezultatai yra „per tamsūs“, „per šviesūs“ ir „tinkami“.</td>
</tr>
<tr class="even">
<td>Bandymo kintamųjų rezultatai</td>
<td>Naudokite šį puslapį galimiems bandymų kintamojo, susieto su kokybiniu bandymu, bandymų rezultatams nustatyti, redaguoti ir peržiūrėti. Kiekvienam rezultatui priskiriate <strong>teigiamą</strong> arba <strong>neigiamą</strong> būseną. Turite apibrėžti kiekvieno kokybinio bandymo, kuris apibrėžtas puslapyje <strong>Bandymai</strong>, kintamąjį ir jo rezultatus. (Kokybinių bandymų tipas puslapyje <strong>Bandymai</strong> nustatytas į <strong>Parinktis</strong>. Naudokite puslapį <strong>Bandymų grupės</strong>, kad atskiram kokybiniam bandymui priskirtumėte bandymų kintamąjį ir numatytąjį rezultatą.</td>
<td>Gamybos įmonė, kepanti sausainius, naudoja galutinio produkto bandymą. Šis bandymas turi keletą kintamųjų. Vienas kintamasis yra skonis, ir galimi šio kintamojo rezultatai yra „geras“ ir „blogas“. Antras kintamasis yra spalva, ir galimi rezultatai yra „per tamsūs“, „per šviesūs“ ir „tinkami“. Kiekvienam rezultatui priskiriama <strong>teigiama</strong> arba <strong>neigiama</strong> būsena. Kiekvieno kintamojo tikrinimo metu tikrintojas pateikia tikrinimo rezultatų ataskaitą, joje nurodydamas vieną iš rezultatų.</td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a>Papildomi ištekliai
--------

[Kokybės valdymo procesai](quality-management-processes.md)

[Neatitikimo valdymo įgalinimas](enable-nonconformance-management.md)

