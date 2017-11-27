---
title: Intrastat
description: "Šiame straipsnyje pateikta informacija apie Intrastat ataskaitas už prekybą prekėmis ir, kai kuriais atvejais, paslaugomis Europos Sąjungos (ES) šalyse / regionuose. Jame pateikta ataskaitų proceso apžvalga ir aprašyti reikiami parametrai ir būtinosios sąlygos."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7c713f3a1cb5aa4758a72a7cc42c73c57b602219
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="intrastat"></a>Intrastat

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikta informacija apie Intrastat ataskaitas už prekybą prekėmis ir, kai kuriais atvejais, paslaugomis Europos Sąjungos (ES) šalyse / regionuose. Jame pateikta ataskaitų proceso apžvalga ir aprašyti reikiami parametrai ir būtinosios sąlygos.

Intrastat yra informacijos rinkimo ir statistikos generavimo apie prekybą prekėmis Europos Sąjungos (ES) šalyse / regionuose sistema. Intrastat ataskaitų reikia, kai produktas kerta kitos ES šalies / regiono sieną. Keliose šalyse / regionuose Intrastat ataskaitos taip pat taikomos paslaugoms. Intrastat ataskaitose gali būti renkami privalomi ir neprivalomi elementai. Privalomi yra šie elementai: šalies, kuri yra atsakinga už informacijos teikimą, pridėtinės vertės mokesčio (PVM) numeris, ataskaitinis laikotarpis, srautas (gavimo ar išsiuntimo), aštuonių skaitmenų prekės kodas, partnerė šalis narė (konsignacijos šalis narė gaunant ir paskirties šalis narė išsiunčiant), prekių vertė, prekių kiekis (neto svoris ir papildomas vienetas) ir operacijos pobūdis. Šalys / regionai taip pat gali įvairiomis sąlygomis rinkti neprivalomų elementų. Kai kurie neprivalomi elementai yra kilmės šalis / regionas, pristatymo sąlygos, transportavimo būdas, išsamesnis už CN8 prekės kodas, kilmės regionas išsiunčiant ir paskirties regionas gaunant, statistinė procedūra, statistinė vertė, prekių aprašas ir pakrovimo / iškrovimo uostas / oro uostas.

## <a name="overview-of-the-intrastat-reporting-process"></a>Intrastat ataskaitų teikimo proceso apžvalga
Toliau pateikiamuose skyriuose aprašomas bendras informacijos, kuri naudojama teikti Intrastat ataskaitoms, srautas.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Įvesti operaciją, kuri kerta kitos ES šalies / regiono sieną

Kliento SF, laisvos formos SF, pirkimo SF, projekto SF, kliento važtaraštis, tiekėjo produkto kvitas ar perkėlimo užsakymas į Intrastat žurnalą perkeliami tik jei paskirties (išsiunčiant) arba konsignacijos (gaunant) šalies / regiono tipas yra **ES**. Šią funkciją taip pat palaiko „Microsoft Dynamics 365 for Operations“ (1611). Funkcija suteikia galimybę nurodyti ES vidaus operacijos pakrovimo adresą. Jei pakrovimo adresas skiriasi nuo tiekėjo darbo adreso (arba grąžinimo užsakymo kliento darbo adreso), Intrastat ataskaitose bus naudojama ši informacija. Kai kuriate pardavimo užsakymą, laisvos formos SF, pirkimo užsakymą, tiekėjo SF, projekto SF ar perkėlimo užsakymą, dokumento antraštėje arba eilutėje kai kurių laukų, kurie yra susiję su užsienio prekyba, reikšmės yra numatytosios. Numatytasis operacijos kodas yra paimamas iš atitinkamo lauko **Užsienio prekybos parametrų** puslapyje. Numatytasis prekės kodas, kilmės šalis / regionas ir kilmės apskritis / rajonas paimami iš prekės. Galite keisti numatytąsias reikšmes ir taip pat galite užpildyti kitą su užsienio prekyba susijusią informaciją: statistikos procedūrą, transportavimo būdą ir uostą.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Naudoti Intrastat žurnalą, norint generuoti informaciją apie prekybą tarp ES šalių / regionų

Statistikos tikslais informacija apie prekybą tarp ES šalių / regionų generuojama kas mėnesį. Operacijas iš laisvos formos SF, kliento SF, kliento važtaraščio, tiekėjo SF, tiekėjo važtaraščio, projekto SF ar perkėlimo užsakymo galite perkelti pagal perkėlimo kriterijus, kurie nustatomi **Užsienio prekybos parametrų** puslapyje. Operacijas galite įvesti ir rankiniu būdu. Jei reikia ką naujinti, galite rankiniu būdu atnaujinti perkeltas operacijas Intrastat žurnale. Konkrečiomis aplinkybėmis, nustatomomis **Intrastat glaudinimo** puslapyje, Intrastat žurnale galite glaudinti operacijas. Kai kuriose šalyse / regionuose leidžiama taikyti operacijos ribinę reikšmę. Tada operacijas, esančias žemiau tos ribinės reikšmės, galite pateikti nurodytu prekės kodu. Prekės kodą galite atnaujinti atitinkamose Intrastat žurnalo eilutėse, atsižvelgdami į **Minimalios ribos** nuostatą **Užsienio prekybos parametrų** puslapyje. Pagal **Intrastat glaudinimo** nuostatą taip pat galite tas operacijas glaudinti. Intrastat žurnale tikrinti operacijų užbaigtumą galite pagal nuostatą **Tikrinti sąranką**, esančią **Užsienio prekybos parametrų** puslapyje. Galima tikrinti atitinkamų laukų duomenų užbaigtumą: šalies / regiono, apskrities ar rajono, svorio, prekės kodo, operacijos kodo, papildomo vieneto, uosto, kilmės, pristatymo sąlygų, transportavimo būdo ir mokesčių lengvatos numerio. Operacijos, kurios nėra užbaigtos, bus pažymėtos kaip negaliojančios.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Naudoti Intrastat žurnalą, norint pranešti informaciją apie prekybą tarp ES šalių / regionų

Statistikos tikslais informacija apie prekybą tarp ES šalių / regionų skelbiama kas mėnesį. Intrastat ataskaitą galite spausdinti pagal **Ataskaitų formatų susiejimo** nuostatas **Užsienio prekybos parametrų** puslapyje. Taip pat pagal **Failų formatų susiejimo** nuostatas **Užsienio prekybos parametrų** puslapyje galite generuoti elektroninį failą. Norėdami daugiau informacijos apie Intrastat ataskaitas, įskaitant būtinąsias sąlygas, žr. toliau nurodytus Intrastat ataskaitų užduočių įrašus.

-   ES Intrastat deklaracijos generavimas,
-   Operacijų perkėlimas į Intrastat,
-   ES vidaus operacijos pakrovimo adreso nurodymas.

## <a name="prerequisites"></a>Būtinieji komponentai
Toliau pateikiamoje lentelėje nurodytos Intrastat ataskaitų būtinosios sąlygos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>Prekės/Paslaugos pavadinimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Adreso sąranka</td>
<td>Nustatykite šalių / regionų Tarptautinės standartizacijos organizacijos (ISO) kodus.</td>
</tr>
<tr class="even">
<td>Juridinis subjektas</td>
<td>Nustatykite importavimo / eksportavimo mokesčių lengvatų numerius, importavimo / eksportavimo filialo numerio plėtinį ir Intrastat kodą, priskirtą juridiniam subjektui.</td>
</tr>
<tr class="odd">
<td>Produktų kategorijų hierarchija (pardavimo hierarchija, įsigijimo hierarchija)</td>
<td><strong>Kategorijų hierarchijos</strong> puslapio skirtuke <strong>Prekių kodai</strong> kategorijų mazgams priskirkite Intrastat prekių kodus. Kai prekės kodą priskiriate pirminės kategorijos mazgui, tas kodas taikomas visiems antrinių kategorijų mazgams. Prekės kodą pasirinkus išleisto produkto informacijoje ir pardavimo užsakymo, pirkimo užsakymo bei perkėlimo užsakymo eilutėse, pasirinkti prekių kodai bus prieinami rodinyje <strong>Pasirinkta</strong>.</td>
</tr>
<tr class="even">
<td>Patvirtinto produkto informacija</td>
<td>Nustatykite toliau nurodytus išleistų produktų užsienio prekybos duomenis.
<ul>
<li><strong>Prekės kodas</strong> – pasirinkite iš pasirinktų prekių sąrašo, gauto iš priskirtų produktų kategorijų, arba iš viso Intrastat prekių kodų sąrašo.</li>
<li><strong>Statistinis išlaidų procentinis dydis</strong></li>
<li><strong>Kilmės šalis / regionas</strong> – pasirinkite numatytąją šalį / regioną, kur buvo gautos ar pagamintos visos prekės.</li>
<li><strong>Kilmės / paskirties apskritis / rajonas</strong> – pasirinkite numatytąją gavimo paskirties apskritį / rajoną ir išsiuntimo kilmės rajoną / apskritį.</li>
<li><strong>Grynasis svoris, kg</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Klientai</td>
<td>Nustatykite kliento pristatymo adresą ES šalyje / regione.</td>
</tr>
<tr class="even">
<td>Tiekėjai</td>
<td>Nustatykite tiekėjo adresą ES šalyje / regione.</td>
</tr>
<tr class="odd">
<td>Papildomos išlaidos</td>
<td>Nustatykite papildomų išlaidų kodą, kurį reikia įtraukti į SF sumą, į statistinę sumą arba į jas abi. <strong>Išlaidų kodų</strong> puslapyje, <strong>Užsienio prekybos</strong> skirtuke įgalinkite <strong>Intrastat SF vertę</strong>, kad išlaidų suma būtų įtraukta į SF vertę, ir įgalinkite <strong>Intrastat statistinę vertę</strong>, kad išlaidų suma būtų įtraukta į statistinę vertę.</td>
</tr>
<tr class="even">
<td>Elektroninė ataskaita</td>
<td>Nustatykite elektroninių ataskaitų konfigūracijas, kad Intrastat duomenys būtų eksportuojami elektroninio failo formatu, kurio reikalauja aktualios institucijos, ir kad Intrastat duomenis peržiūrėtumėte naudotojui patogiu, įskaitomu formatu (pvz., „Microsoft Excel‟).</td>
</tr>
<tr class="even">
<td>Sandėliavimas</td>
<td>Tiekėjų sąskaitas susieti su sandėlio kodais, kad būtų galima įvesti mokesčių lengvatos numerį perkeliant perkėlimo užsakymą.</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Sąranka
Toliau pateikiamuose skyriuose aprašomos nuostatos, kurios reikalingos kuriant Intrastat ataskaitas.

### <a name="set-up-all-required-intrastat-related-lists"></a>Nustatyti visus reikiamus su Intrastat susijusius sąrašus

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sąrašas</th>
<th>Papildoma informacija</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Prekių kodai</td>
<td>Nustatykite <strong>Prekės kodo</strong> tipo kategorijų hierarchiją ir pagal jungtinį nomenklatūrų sąrašą įveskite visų prekių kodus. Kiekvienai prekei nustatykite toliau nurodytą informaciją.
<ul>
<li>Prekės pavadinimas ir prekės kodas.</li>
<li>Patogus pavadinimas ir (arba) išverstas pavadinimas.</li>
<li>Papildomų vienetų skelbimo parametrai skirtuke <strong>Užsienio prekyba</strong>. Papildomą vienetą galite pasirinkti vienetų sąraše. Taip pat galite nurodyti, ar be pasirinkto papildomo vieneto reikia skelbti prekių svorį.</li>
</ul></td>
</tr>
<tr class="even">
<td>Operacijų kodai</td>
<td>Pagal savo šalies / regiono reikalavimus nustatykite operacijos pobūdį. Kiekvienam operacijos kodui, kurį nustatote, turite nustatyti taisykles, skirtas skaičiuoti perkėlimo užsakymų ir pardavimo / pirkimo užsakymų SF sumoms ir statistinėms sumoms.
<ul>
<li>Perkėlimo užsakymams nustatote vieną iš toliau pateiktų SF sumų ir statistinių sumų skaičiavimo taisyklių.
<ul>
<li><strong>Tuščia</strong> – suma bus 0 (nulis).</li>
<li><strong>Finansinių išlaidų suma</strong> – suma bus lygi finansinėms išlaidoms.</li>
<li><strong>Bendrosios išlaidos</strong> – suma bus lygi benrosioms operacijos išlaidoms.</li>
<li><strong>Rankin.</strong> – suma bus lygi sumai, kuri rankiniu būdu nurodyta perkėlimo užsakymo eilutėje.</li>
</ul></li>
<li>Pardavimo užsakymams ir pirkimo užsakymams nustatote vieną iš toliau pateiktų SF sumų ir statistinių sumų skaičiavimo taisyklių.
<ul>
<li><strong>Tuščia</strong> – suma bus 0 (nulis).</li>
<li><strong>SF suma</strong> – suma bus lygi prekės sumai, kuriai išrašyta SF.</li>
<li><strong>Bazinė suma</strong> – suma bus lygi sumai, kuriai būtų išrašoma SF prieš taikant bet kokią nuolaidą.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Transportavimo metodai</td>
<td>Pagal savo šalies / regiono reikalavimus nustatykite transportavimo būdą. Kiekvieno pristatymo būdo numatytąjį transportavimo būdą galite nustatyti <strong>Užsienio prekybos</strong> skirtuke.</td>
</tr>
<tr class="even">
<td>Uostai</td>
<td>Jei toki informacija yra renkama jūsų šalyje / regione, nustatykite pakrovimo / iškrovimo uostą / oro uostą.</td>
</tr>
<tr class="odd">
<td>Statistikos procedūros</td>
<td>Jei tokia informacija yra renkama jūsų šalyje / regione, nustatykite statistinę procedūrą.</td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Nustatyti Intrastat operacijų glaudinimo taisykles

**Intrastat glaudinimo** puslapyje galite pasirinkti laukus, kurie bus naudojami glaudinant. Intrastat žurnale paleidus funkciją Glaudinti, visos operacijos, kurių Intrastat žurnale pasirinktų laukų reikšmių deriniai bus tokie patys, bus suglaudintos į vieną operaciją.

### <a name="set-up-foreign-trade-parameters"></a>Nustatyti užsienio prekybos parametrus

Norėdami nustatyti toliau pateiktos lentelės parametrus, naudokite **Užsienio prekybos parametrų** puslapį.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tabuliavimo ženklas</th>
<th>Parametrai</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bendra</td>
<td><ul>
<li><strong>Bendra</strong> – nurodykite toliau pateiktą informaciją.
<ul>
<li>Pardavimo užsakymų, pirkimo užsakymų, kredito pažymų ir perkėlimo užsakymų numatytuosius operacijų kodus. Nustatytas kredito pažymų operacijų kodas taip pat naudojamas kaip fizinių prekių grąžinimo kodas bei naudojamas gretinti nuokrypio fizinių prekių grąžinimams ir koregavimo kredito pažymoms.</li>
<li>Darbuotojas, atsakingas už Intrastat ataskaitų rengimą.</li>
</ul></li>
<li><strong>Minimali riba</strong> – nurodykite nuostatas, skirtas naujinti operacijoms, kurios yra žemiau ribinės reikšmės.
<ul>
<li>Ribinė suma ir svoris.</li>
<li>Prekės kodas, taikytinas operacijoms, esančioms žemiau ribinės reikšmės</li>
</ul></li>
<li><strong>Perkėlimas</strong> – nurodykite operacijų perkėlimo į Intrastat žurnalą kriterijus. Galite nurodyti, kad operacijos būtų perkeliamos tik tada, kai prekės atitinka vieną ar visus toliau nurodytus kriterijus.
<ul>
<li>Prekės nėra aptarnavimo prekės.</li>
<li>Prekės turi prekės kodą.</li>
<li>Prekės turi svorį.</li>
<li>Prekės turi papildomų vienetų.</li>
</ul></li>
<li><strong>Tikrinti sąranką</strong> – nurodykite taisykles, skirtas tikrinti Intrastat duomenų užbaigtumui. Galite pasirinkti, kuriuos duomenis tikrinti.</li>
<li><strong>Apvalinimo taisyklės</strong> – nurodykite toliau pateiktas sumų ir svorių apvalinimo Intrastat ataskaitose nuostatas.
<ul>
<li>Apvalinimo taisyklė (tikslumas).</li>
<li>Apvalinimo būdas: aukštyn, žemyn arba įprastas.</li>
<li>Sumų ir svorių skaitmenų po kablelio skaičius.</li>
<li>Svorių, mažesnių nei 1 kilogramas (kg), apvalinimo instrukcijos: iki 1 kg, įprastai arba neapvalinti.</li>
</ul></li>
<li><strong>Elektroninės ataskaitos</strong> – nurodykite nuorodas į elektroninių ataskaitų konfigūracijas, kad galėtumėte generuoti elektroninį failą ir ataskaitą.</li>
<li><strong>Prekių kodų hierarchija</strong> – nurodykite <strong>Prekės kodo</strong> tipo, kuris atstoja Intrastat prekės kodą CN8, kategorijų hierarchiją.</li>
</ul></td>
</tr>
<tr class="even">
<td>Agento kontaktinė informacija</td>
<td>Nurodykite agento vardą ir pavardę, adresą, mokesčių lengvatos numerį, telefono numerį ir fakso numerį.</td>
</tr>
<tr class="odd">
<td>Šalies / regiono ypatybės</td>
<td>Dabartinio juridinio subjekto šalį / regioną nustatykite į <strong>Vietin.</strong>. ES šalių / regionų, dalyvaujančių ES prekyboje su dabartiniu juridiniu subjektu, šalį / regioną nustatykite į <strong>ES</strong>. Taip pat identifikuojate kiekvienos šalies / regiono kodą, skirtą užsienio prekybai.</td>
</tr>
<tr class="even">
<td>Numeravimas</td>
<td>Nurodykite Intrastat žurnalo numeraciją.</td>
</tr>
</tbody>
</table>

 




