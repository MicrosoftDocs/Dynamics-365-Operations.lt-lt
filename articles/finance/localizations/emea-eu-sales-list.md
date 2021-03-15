---
title: ES pardavimo sąrašo ataskaitos
description: Šiame straipsnyje pateikta informacija apie Europos Sąjungos (ES) Pardavimo sąrašo ataskaitas.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EUSalesList
audience: Application User
ms.reviewer: kfend
ms.custom: 12811
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1e9a566b7dc4dc2ed1970294a22e72b0bd21a7c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003012"
---
# <a name="eu-sales-list-reporting"></a>ES pardavimo sąrašo ataskaitos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie Europos Sąjungos (ES) Pardavimo sąrašo ataskaitas.

<a name="eu-sales-list-reporting"></a>ES pardavimo sąrašo ataskaitos
-----------------------

Tiekėjas, tiekiantis įmonėms, įsteigtoms Europos Sąjungoje (ES), prekes ar paslaugas ES viduje, turi pateikti į Vidaus tiekimo deklaraciją (ES pardavimo sąrašą arba ESL). Apskritai ESL būtina pateikta mokesčių inspekcijoms ne vėliau kaip paskutinę mėnesio po kalendorinio laikotarpio, kurį apima ESL, dieną. Tiekėjas turi ant ESL nurodyti savo pridėtinės vertės mokesčio (PVM) identifikavimo numerį ir taip pat nurodyti tokią informaciją pagal klientą.

-   ES kliento PVM identifikavimo numerį
-   Bendroji vidaus tiekimo ES klientams per tą laikotarpį prekių ir paslaugų vertė. Tiekėjas taip pat turi atskirti bendrąjį prekių tiekimą ir trišalės prekybos tiekimą. Trišalės prekybos operacija apima tiesioginį prekių pristatymą iš tiekėjo tiekėjo jo klientui, kai abi šalys yra registruotos kitose ES valstybėse narėse.

Naudodami ESL kiekvienos ES valstybės šalies narės mokesčių inspekcija gali tikrinti, ar sumokėtas PVM už kiekvieną ES vidaus operaciją. Sąrašai ir PVM deklaracijos kartu leidžia ES valstybėms narėms keistis informacija apie prekių srautą visoje ES.

## <a name="overview-of-the-eu-sales-list-reporting-process"></a>ES pardavimų sąrašo ataskaitų teikimo proceso apžvalga
Galite atlikti šias užduotis, susijusias su ES pardavimų sąrašo ataskaitų teikimu.

-   Rinkti informaciją apie ES vidaus prekybos operacijas. ES vidaus prekybos operacija gali būti pardavimo sąskaita faktūra, laisvos formos sąskaita faktūra, projekto sąskaita faktūra arba tiekėjo sąskaita faktūra. Operacija identifikuojama pagal kitos sandorio šalies valstybę / regioną. Skirtingų tipų ES vidaus prekybos operacijos surenkamos į ES pardavimų sąrašo lentelę, kurioje jos pateikiamos bendra forma. Kiekvienas ESL lentelės įrašas rodo vieną operaciją, ir jį sudaro kitos sandorio šalies PVM identifikatorius ir bendra prekių ir paslaugų vertė.
-   (Nebūtina) Peržiūrėti **ES pardavimų sąrašo** ataskaitą. Tam tikro laikotarpio ataskaitą **ES pardavimų sąrašas** galite peržiūrėti ir patvirtinti „Microsoft Excel“ darbaknygės forma.
-   Generuoti **ES pardavimo sąrašo** ataskaitą. **ES pardavimų sąrašo** ataskaita generuojama kaip tam tikro formato, kuris priklauso nuo kiekvienos ES valstybės narės, elektroninis failas. Apskritai **ES pardavimų sąrašo** ataskaitoje yra pagrindinė informacija apie ataskaitą teikiančią šalį ir prekių ir paslaugų vertę. Informacija yra sugrupuota pagal valstybę ir kitos sandorio šalies PVM identifikatorių.
-   Uždaryti ES pardavimo sąrašo ataskaitos laikotarpį. Sugeneravus **ES pardavimų sąrašo** ataskaitą ir pateikus ją institucijoms, galima pažymėti ESL lentelės įrašus **Uždaryta**. Šios operacijos nebus įtrauktos į papildomas ataskaitas.

## <a name="prerequisites"></a>Būtinieji komponentai
Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategorija</th>
<th>Būtinoji sąlyga</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Sąranka:</strong> juridinis subjektas</td>
<td>Pagrindinis juridinio subjekto adresas turi būti ES valstybėje narėje. Puslapyje <strong>Juridiniai subjektai</strong> (spustelėkite <strong>Organizacijos administravimas</strong> &gt; <strong>Organizacijos</strong> &gt; <strong>Juridiniai subjektai</strong>) pasirinkite savo juridinį subjektą. FastTab <strong>Adresai</strong> sukurkite adresą, pasirinkite valstybę / regioną ir kitus adreso komponentus pažymėkite, kad adresas <strong>Pagrindinis</strong>. FastTab <strong>Mokesčių registracija</strong> lauke <strong>Mokesčių mokėtojo kodas</strong> nurodykite savo įmonės mokesčių mokėtojo kodą.</td>
</tr>
<tr class="even">
<td><strong>Sąranka:</strong> neapmokestinimo identifikavimo parametrai</td>
<td>Nustatykite neapmokestinimo identifikavimo parametrus puslapyje <strong>Valstybės / regiono parametrai</strong> (spustelėkite <strong>Mokestis</strong> &gt; <strong>Sąranka</strong> &gt; <strong>PVM</strong> &gt; <strong>Valstybės / regiono parametrai</strong>). Puslapyje sukurkite kiekvienos valstybės / regiono, kuriame sandorio šalių, įrašą ir nurodykite tokią informaciją.
<ul>
<li><strong>Valstybė / regionas</strong> – pasirinkite valstybę / regioną, kurią norite susieti su neapmokestinimo identifikavimu.</li>
<li><strong>PVM</strong> – įveskite pasirinktos valstybės / regiono neapmokestinimo identifikavimo numerį (t. y. neapmokestinimo numerio prefiksą).</li>
<li><strong>Tikrinti neapmokestinimo numerį</strong> – pažymėkite šį žymės langelį, jei norite patikrinti pasirinktos valstybės / regiono neapmokestinimo identifikavimo duomenis.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Sąranka: </strong>Neapmokestinimo numeriai</td>
<td>Sukurkite savo kitų sandorio šalių neapmokestinimo numerius puslapyje <strong>Neapmokestinimo numeriai</strong> (spustelėkite <strong>Mokestis</strong> &gt; <strong>Sąranka</strong> &gt; <strong>PVM</strong> &gt; <strong>Neapmokestinimo numeriai</strong>). Puslapyje sukurkite kiekvieno neapmokestinimo numerio įrašą ir nurodykite tokią informaciją.
<ul>
<li><strong>Valstybė / regionas </strong>– pasirinkite valstybę / regioną, kuriame kita sandorio šalis registruota kaip mokesčių mokėtoja.</li>
<li><strong>Neapmokestinimo numeris</strong> – įveskite kitos sandorio šalies neapmokestinimo numerį.</li>
<li><strong>Įmonės pavadinimas</strong> – (nebūtina) įveskite kitos sandorio šalies pavadinimą.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sąranka: </strong>kitų sandorio šalių mokesčių registracija</td>
<td>Nustatykite kitų sandorio šalių mokesčių registracijos informaciją puslapyje <strong>Visi klientai</strong> (spustelėkite <strong>Pardavimas ir rinkodara</strong> &gt; <strong>Klientai</strong> &gt; <strong>Visi klientai</strong>, pasirinkite kliento įrašą ir tada spustelėkite <strong>Parinktys</strong> &gt; <strong>Keisti rodinį</strong> &gt; <strong>Išsamios informacijos rodinys</strong>) arba puslapyje <strong>Tiekėjai</strong> (spustelėkite <strong>Įsigijimas ir šaltinio pasirinkimas</strong> &gt; <strong>Tiekėjai</strong> &gt; <strong>Tiekėjai</strong>, pasirinkite tiekėjo įrašą ir tada spustelėkite <strong>Parinktys</strong> &gt; <strong>Keisti rodinį</strong> &gt; <strong>Išsamios informacijos rodinys</strong>). FastTab <strong>Sąskaita faktūra ir pristatymas</strong> lauke <strong>Neapmokestinimo numeris</strong> pasirinkite mokesčių mokėtojo kodą.</td>
</tr>
<tr class="odd">
<td><strong>Sąranka: </strong>PVM</td>
<td>Nustatykite mokesčių kodus, kuriuos norite įtraukti į ataskaitą <strong>ES pardavimų sąrašas</strong> puslapyje <strong>PVM kodai</strong> (spustelėkite <strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>PVM kodai</strong>). FastTab <strong>Ataskaitos sąranka</strong> išvalykite kiekvieno PVM kodo, kuris turi būti įtrauktas į ataskaitą, žymės langelį <strong>Neįtraukta</strong>. Nustatykite prekių PVM parametrus puslapyje <strong>Prekės PVM grupės</strong> (spustelėkite <strong>Mokestis</strong> &gt; <strong>Netiesioginiai mokesčiai</strong> &gt; <strong>PVM</strong> &gt; <strong>Prekės PVM grupės</strong>). Lauke <strong>Ataskaitų tipas</strong> pasirinkite kiekvienos prekės PVM grupės reikšmę. Pasirinktos reikšmės nustato, į kurį ESL sumos stulpelį bus įtraukta eilutės suma.
<ul>
<li><strong>Tuščia</strong> – eilutės suma įtraukiama į stulpelį <strong>Nepriskirta vertė</strong>.</li>
<li><strong>Prekė</strong> – eilutės suma įtraukiama į stulpelį <strong>Prekių vertė</strong>.</li>
<li><strong>Paslauga</strong> – eilutės suma įtraukiama į stulpelį <strong>Paslaugų vertė</strong>.</li>
<li><strong>Investicijos</strong> – eilutės suma įtraukiama į stulpelį <strong>Investicijų vertė</strong>. Šis stulpelis taikomas tik Belgijai.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Sąranka:</strong> ESL ataskaitų konfigūracijos</td>
<td>Importuokite arba kurkite ESL elektroninių ataskaitų konfigūracijas. Informacijos apie tai, kaip kurti ir tvarkyti elektroninių ataskaitų konfigūracijas, ieškokite elektroninių ataskaitų instrukcijoje.</td>
</tr>
<tr class="odd">
<td><strong>Sąranka: </strong>bendrieji parametrai</td>
<td>Nustatykite ataskaitų parametrus ESL puslapyje <strong>Užsienio prekybos parametrai</strong> (spustelėkite <strong>Mokestis</strong> &gt; <strong>Sąranka</strong> &gt; <strong>Užsienio prekyba</strong> &gt; <strong>Užsienio prekybos parametrai</strong>). Nurodykite šiuos parametrus.
<ul>
<li>Skirtukas <strong>ES pardavimų sąrašas</strong>:
<ul>
<li><strong>Ataskaita apie mokėjimo nuolaidas</strong> – pažymėkite šį žymės langelį, jei įtraukiant operaciją ESL reikia įtraukti į vertę mokėjimo nuolaidą.</li>
<li><strong>Perkelti pirkinius</strong> – pažymėkite šį žymės langelį, jei norite įtraukti į ESL pirkinius.</li>
<li><strong>Failo formato susiejimas</strong> – pasirinkite elektroninių ataskaitų formatą, kuris bus naudojamas generuojant elektroninį ESL failą.</li>
<li><strong>Ataskaitos formato susiejimas</strong> – pasirinkite elektroninių ataskaitų formatą, kuris bus naudojamas generuojant ESL ataskaitos peržiūrą.</li>
<li><strong>Apvalinimo taisyklė</strong> – nurodykite realųjį skaičių, naudojamą apvalinti. ESL sumos bus apvalinamos iki šio skaičiaus kartotinių.</li>
<li><strong>Apvalinimo metodas</strong> – pasirinkite apvalinimo metodą, kuris bus naudojamas ESL sumoms apvalinti (<strong>Įprastas</strong>, <strong>Į mažesnę pusę</strong> arba <strong>Į didesnę pusę</strong>).</li>
<li><strong>Naudoti minimalią vertę</strong> – pažymėkite šį žymės langelį, jei norite, kad sumos, mažesnė nei skaičius <strong>Apvalinimo taisyklė</strong>, būtų apvalinamos iki skaičiaus <strong>Apvalinimo taisyklė</strong>.</li>
<li><strong>Dešimtainių dalių skaičius</strong> – nurodykite, kiek dešimtainio skyriklio vietų bus rodoma ESL sumose (elektroniniuose failuose ir ataskaitoje <strong>ESL peržiūra</strong>).</li>
</ul></li>
<li>Skirtukas <strong>Valstybės / regiono parametrai</strong>: identifikuokite ES valstybes nares. Puslapyje sukurkite kiekvienos ES valstybės narės įrašą ir nurodykite tokią informaciją.
<ul>
<li><strong>Valstybė / regionas</strong> – pasirinkite valstybę / regioną.</li>
<li><strong>Valstybės / regiono tipas</strong> – jei parinkties <strong>Valstybė / regionas</strong> reikšmė yra valstybė / regionas, kuriame įregistruota jūsų įmonė, pasirinkite <strong>Vidaus</strong>. Jei parinkties <strong>Valstybė / regionas</strong> reikšmė yra ES valstybė narė, kurioje jūsų įmonė nėra registruota, pasirinkite <strong>ES</strong>. Jei parinkties <strong>Valstybė / regionas</strong> reikšmė nėra ES valstybė narė, pasirinkite <strong>Trečioji valstybė / regionas</strong>.</li>
</ul></li>
<li>Skirtukas <strong>Numeracijos</strong>: eilutėje, kurios parinkties <strong>Nuoroda</strong> reikšmė yra <strong>ES pardavimų sąrašas</strong>, pasirinkite numeracijos kodą.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Susijusios operacijos</strong></td>
<td><ul>
<li>Užregistruoti pardavimą klientui kitoje ES valstybėje narėje.</li>
<li>Užregistruoti laisvos formos sąskaitą faktūrą klientui kitoje ES valstybėje narėje.</li>
<li>Užregistruoti projekto sąskaitą faktūrą klientui kitoje ES valstybėje narėje.</li>
<li>Užregistruoti sąskaitą faktūrą iš tiekėjo kitoje ES valstybėje narėje.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="working-with-the-esl"></a>Darbas su ESL
### <a name="collecting-information-about-intra-community-trade-transactions"></a>Informacijos apie ES vidaus prekybos operacijas rinkimas

ES vidaus prekybos operacijomis laikytinos šių tipų operacijos.

-   Pardavimo SF
-   Laisvos formos sąskaitos faktūros
-   Projekto SF
-   Tiekėjo SF

Operacija laikoma su ES vidaus prekybos operacija, jei operacijos pristatymo adresas yra ES valstybėje narėje. Tokių valstybių / regionų įrašas turi būti puslapio **Užsienio prekybos parametrai** skirtuke **Valstybės / regiono parametrai**, ir turi būti nustatyta parinkties **Valstybės / regiono tipas** reikšmė **ES**. ES vidaus prekybos operacijos pažymėtos lauke **Sąrašo kodas**. Naudodami šį lauką taip pat galite atskirti bendrąsias ES vidaus prekybos operacijas nuo trišalių prekybos operacijų. Galite rinkti informaciją apie ES vidaus prekybos operacijas puslapyje **ES pardavimų sąrašas** (spustelėkite **Mokestis** &gt; **Deklaracijos** &gt; **Užsienio prekyba** &gt; **ES pardavimų sąrašas**) naudodami funkciją **Perkelti**. Ši funkcija leidžia įtraukti operacijas, kurių sumos yra įvairių ataskaitų tipų (pavyzdžiui, prekių ar paslaugų), atsižvelgiant į prekių PVM grupes, kurios nurodytos operacijų eilutes. Taip pat galite taikyti kitus filtrus norėdami apibrėžti operacijas, kurios turėtų būti įtrauktos. Funkcija **Perkelti** sukuria kiekvienos įtrauktos ES vidaus prekybos operacijos įrašą puslapyje **ES pardavimų sąrašas** ir nurodo kitos sandorio šalies sąskaitos numerį, valstybę / regioną, neapmokestinimo kodą, sąskaitos faktūros numerį ir datą ir bendrąsias kiekvieno ataskaitų tipo eilučių sumas. Taip pat nukopijuoja iš operacijos reikšmę **Sąrašo kodas**. Galite rankiniu būdu pakeisti operacijos sąrašo kodą puslapyje **ES pardavimų sąrašas**. Funkcija **Perkelti** sukuria įrašus, jei nustatyta parinkties **Ataskaitos būsena** reikšmė **Įtraukta**. Tikrinti informaciją, surinktą puslapyje **ES pardavimų sąrašas**, galite naudodami funkciją **Tikrinti**.

### <a name="generating-the-eu-sales-list-report"></a>ES pardavimų sąrašo ataskaitos generavimas

Galite sugeneruoti ataskaitą **ES pardavimų sąrašas** naudodami funkciją **Ataskaitos**, esančią puslapyje **ES pardavimų sąrašas**. Funkcija leidžia pasirinkti ataskaitinį laikotarpį ir taikyti filtrus ESL įrašams, kuriuos norite įtraukti, apibrėžti. Be to, galite nurodyti kitus parametrus, kurie yra būdingi kiekvienai valstybei / regionui. Taip pat galite pasirinkti generuoti peržiūros ataskaitą, elektroninį failą arba abu. Funkcija **Ataskaitos** naudoja ataskaitos ir failo formato parametrus, nurodytus puslapyje **Užsienio prekybos parametrai**. Apskritai ataskaitą **ES pardavimų sąrašas** sudaro atskiros eilutės, kuriose pateiktos bendrosios sumos pagal kitos sandorio šalies valstybę / regioną, neapmokestinimo kodą ir ataskaitų tipą (trišalės prekybos operacijos įtraukiamos). Sukūrę konkretaus laikotarpio ataskaitą **ES pardavimų sąrašas**, galite pažymėti ESL įrašus, kurie yra įtraukti į ataskaitą, nustatydami parinkties **Ataskaitos būsena** reikšmę **Baigta**. Norėdami nustatyti šią būseną, naudokite funkciją **Pažymėti kaip baigtą**, esančią puslapyje **ES pardavimų sąrašas**.

### <a name="closing-the-eu-sales-list-reporting-period"></a>ES pardavimų sąrašo ataskaitinio laikotarpio uždarymas

Baigę tam tikro laikotarpio ataskaitinį procesą (pavyzdžiui, kai mokesčių inspekcija priims ataskaitą **ES pardavimų sąrašas**), galite pažymėti ESL įrašus, kurie yra įtraukti į to laikotarpio ataskaitą, nustatydami parinkties **Ataskaitos būsena** reikšmę **Uždaryta**. Norėdami nustatyti šią būseną, naudokite funkciją **Pažymėti kaip uždarytą**, esančią puslapyje **ES pardavimų sąrašas**. Jei grąžinate uždarytą laikotarpį, galite pažymėti ESL įrašus nustatydami parinkties **Ataskaitos būsena** reikšmę **Įtraukta**. Tada šiuos įrašus galima vėl įtraukti į ataskaitą **ES pardavimų sąrašas**. Norėdami nustatyti šią būseną, naudokite funkciją **Pažymėti kaip** **įtrauktus**, esančią puslapyje **ES pardavimų sąrašas**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]