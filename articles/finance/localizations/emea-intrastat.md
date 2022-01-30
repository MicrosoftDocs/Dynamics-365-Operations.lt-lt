---
title: Intrastat apžvalga
description: Šioje temoje pateikta informacija apie Intrastat ataskaitas už prekybą prekėmis ir, kai kuriais atvejais, paslaugomis Europos Sąjungos (ES) šalyse / regionuose.
author: EvgenyPopovMBS
ms.date: 01/13/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 97c2b4068f3b8d38281e637ec80f04b19d19be61
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986040"
---
# <a name="intrastat-overview"></a>Intrastat apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje pateikta informacija apie Intrastat ataskaitas už prekybą prekėmis ir, kai kuriais atvejais, paslaugomis Europos Sąjungos (ES) šalyse / regionuose. Šioje temoje taip pat pateikiama ataskaitų proceso apžvalga ir aprašomi reikalingi parametrai ir būtinosios sąlygos.

Intrastat yra informacijos rinkimo ir statistikos generavimo apie prekybą prekėmis Europos Sąjungos (ES) šalyse / regionuose sistema. Intrastat ataskaitų reikia, kai produktas kerta kitos ES šalies / regiono sieną. Keliose šalyse / regionuose Intrastat ataskaitos taip pat taikomos paslaugoms. Intrastat ataskaitose gali būti renkami privalomi ir neprivalomi elementai. Privalomi yra šie elementai: šalies, kuri yra atsakinga už informacijos teikimą, pridėtinės vertės mokesčio (PVM) numeris, ataskaitinis laikotarpis, srautas (gavimo ar išsiuntimo), aštuonių skaitmenų prekės kodas, partnerė šalis narė (konsignacijos šalis narė gaunant ir paskirties šalis narė išsiunčiant), prekių vertė, prekių kiekis (neto svoris ir papildomas vienetas) ir operacijos pobūdis. Šalys / regionai taip pat gali įvairiomis sąlygomis rinkti neprivalomų elementų. Kai kurie neprivalomi elementai yra kilmės šalis / regionas, pristatymo sąlygos, transportavimo būdas, išsamesnis už CN8 prekės kodas, kilmės regionas išsiunčiant ir paskirties regionas gaunant, statistinė procedūra, statistinė vertė, prekių aprašas ir pakrovimo / iškrovimo uostas / oro uostas.

## <a name="overview-of-the-intrastat-reporting-process"></a>Intrastat ataskaitų teikimo proceso apžvalga
Toliau pateikiamuose skyriuose aprašomas bendras informacijos, kuri naudojama teikti Intrastat ataskaitoms, srautas.

### <a name="enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>Įvesti operaciją, kuri peržengia kitos ES šalies / regiono kraštinę

Kliento SF, laisvos formos SF, pirkimo SF, projekto SF, kliento važtaraštis, tiekėjo produkto kvitas ar perkėlimo užsakymas į Intrastat žurnalą perkeliami tik jei paskirties (išsiunčiant) arba konsignacijos (gaunant) šalies / regiono tipas yra **ES**. Šią funkciją taip pat palaiko „Microsoft Dynamics 365 for Operations“ (1611). Funkcija suteikia galimybę nurodyti ES vidaus operacijos pakrovimo adresą. Jei pakrovimo adresas skiriasi nuo tiekėjo darbo adreso (arba grąžinimo užsakymo kliento darbo adreso), Intrastat ataskaitose bus naudojama ši informacija. Kai kuriate pardavimo užsakymą, laisvos formos SF, pirkimo užsakymą, tiekėjo SF, projekto SF ar perkėlimo užsakymą, dokumento antraštėje arba eilutėje kai kurių laukų, kurie yra susiję su užsienio prekyba, reikšmės yra numatytosios. Numatytasis operacijos kodas yra paimamas iš atitinkamo lauko **Užsienio prekybos parametrų** puslapyje. Numatytasis prekės kodas, kilmės šalis / regionas ir kilmės apskritis / rajonas paimami iš prekės. Galite keisti numatytąsias reikšmes ir taip pat galite užpildyti kitą su užsienio prekyba susijusią informaciją: statistikos procedūrą, transportavimo būdą ir uostą.

### <a name="use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>Norėdami generuoti informaciją apie prekybą ES šalyse / regionuose, naudokite Intrastat žurnalą

Statistikos tikslais informacija apie prekybą tarp ES šalių / regionų generuojama kas mėnesį. Operacijas iš laisvos formos SF, kliento SF, kliento važtaraščio, tiekėjo SF, tiekėjo važtaraščio, projekto SF ar perkėlimo užsakymo galite perkelti pagal perkėlimo kriterijus, kurie nustatomi **Užsienio prekybos parametrų** puslapyje. Operacijas galite įvesti ir rankiniu būdu. Jei reikia ką naujinti, galite rankiniu būdu atnaujinti perkeltas operacijas Intrastat žurnale. Konkrečiomis aplinkybėmis, nustatomomis **Intrastat glaudinimo** puslapyje, Intrastat žurnale galite glaudinti operacijas. Kai kuriose šalyse / regionuose leidžiama taikyti operacijos ribinę reikšmę. Tada operacijas, esančias žemiau tos ribinės reikšmės, galite pateikti nurodytu prekės kodu. Prekės kodą galite atnaujinti atitinkamose Intrastat žurnalo eilutėse, atsižvelgdami į **Minimalios ribos** nuostatą **Užsienio prekybos parametrų** puslapyje. Pagal **Intrastat glaudinimo** nuostatą taip pat galite tas operacijas glaudinti. Intrastat žurnale tikrinti operacijų užbaigtumą galite pagal nuostatą **Tikrinti sąranką**, esančią **Užsienio prekybos parametrų** puslapyje. Galima tikrinti atitinkamų laukų duomenų užbaigtumą: šalies / regiono, apskrities ar rajono, svorio, prekės kodo, operacijos kodo, papildomo vieneto, uosto, kilmės, pristatymo sąlygų, transportavimo būdo ir mokesčių lengvatos numerio. Operacijos, kurios nėra užbaigtos, bus pažymėtos kaip negaliojančios.

### <a name="use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>Naudokite Intrastat žurnalą, norėdami pateikti informaciją apie prekybą TARP ES šalių / regionų

Statistikos tikslais informacija apie prekybą tarp ES šalių / regionų skelbiama kas mėnesį. Intrastat ataskaitą galite spausdinti pagal **Ataskaitų formatų susiejimo** nuostatas **Užsienio prekybos parametrų** puslapyje. Taip pat pagal **Failų formatų susiejimo** nuostatas **Užsienio prekybos parametrų** puslapyje galite generuoti elektroninį failą. Norėdami daugiau informacijos apie Intrastat ataskaitas, įskaitant būtinąsias sąlygas, žr. toliau nurodytus Intrastat ataskaitų užduočių įrašus.

  - ES Intrastat deklaracijos generavimas,
  - Operacijų perkėlimas į Intrastat,
  - ES vidaus operacijos pakrovimo adreso nurodymas.

## <a name="prerequisites"></a>Būtinieji komponentai
Toliau pateikiamoje lentelėje nurodytos Intrastat ataskaitų būtinosios sąlygos.

|  Būtinoji sąlyga  |  Prekės/Paslaugos pavadinimas  |
|-------------------------|-------------------------|
| Adreso sąranka | Nustatykite šalių / regionų Tarptautinės standartizacijos organizacijos (ISO) kodus. |
| Juridinis subjektas | Nustatykite importavimo / eksportavimo mokesčių lengvatų numerius, importavimo / eksportavimo filialo numerio plėtinį ir Intrastat kodą, priskirtą juridiniam subjektui. |
| Produktų kategorijų hierarchija (pardavimo hierarchija, įsigijimo hierarchija) | **Kategorijų hierarchijos** puslapio skirtuke **Prekių kodai** kategorijų mazgams priskirkite Intrastat prekių kodus. Kai prekės kodą priskiriate pirminės kategorijos mazgui, tas kodas taikomas visiems antrinių kategorijų mazgams. Prekės kodą pasirinkus išleisto produkto informacijoje ir pardavimo užsakymo, pirkimo užsakymo bei perkėlimo užsakymo eilutėse, pasirinkti prekių kodai bus prieinami rodinyje **Pasirinkta**. |
| Patvirtinto produkto informacija | Nustatykite toliau nurodytus išleistų produktų užsienio prekybos duomenis.<ul><li>**Prekės kodas** – pasirinkite iš pasirinktų prekių sąrašo, gauto iš priskirtų produktų kategorijų, arba iš viso Intrastat prekių kodų sąrašo.</li><li>**Statistinis išlaidų procentinis dydis**</li><li>**Kilmės šalis / regionas** – pasirinkite numatytąją šalį / regioną, kur buvo gautos ar pagamintos visos prekės.</li><li>**Kilmės / paskirties apskritis / rajonas** – pasirinkite numatytąją gavimo paskirties apskritį / rajoną ir išsiuntimo kilmės rajoną / apskritį.</li><li>**Grynasis svoris, kg**</li><li>**Pašalinti** – įgalinti šį parametrą, jei norite, kad su šiuo produktu nebūtų perkeliamos operacijos į Intrastat</li></ul> |
| Klientai | Nustatykite kliento pristatymo adresą ES šalyje / regione. |
| Tiekėjai | Nustatykite tiekėjo adresą ES šalyje / regione. |
| Papildomos išlaidos | Nustatykite papildomų išlaidų kodą, kurį reikia įtraukti į SF sumą, į statistinę sumą arba į jas abi. **Išlaidų kodų** puslapyje, **Užsienio prekybos** skirtuke įgalinkite **Intrastat SF vertę**, kad išlaidų suma būtų įtraukta į SF vertę, ir įgalinkite **Intrastat statistinę vertę**, kad išlaidų suma būtų įtraukta į statistinę vertę.</br>Daugiau informacijos rasite operacijos [kodų ir papildomų išlaidų](#transaction-codes-and-miscellaneous-charges) pavyzdyje. |
| Elektroninė ataskaita | Nustatykite elektroninių ataskaitų konfigūracijas, kad Intrastat duomenys būtų eksportuojami elektroninio failo formatu, kurio reikalauja aktualios institucijos, ir kad Intrastat duomenis peržiūrėtumėte naudotojui patogiu, įskaitomu formatu (pvz., „Microsoft Excel“). |
| Sandėliavimas | Tiekėjų sąskaitas susieti su sandėlio kodais, kad būtų galima įvesti mokesčių lengvatos numerį perkeliant perkėlimo užsakymą.</br>Norėdami gauti daugiau informacijos, [peržiūrėkite perkėlimo užsakymo](#transfer-order) pavyzdį.|

## <a name="setup"></a>Sąranka
Toliau pateikiamuose skyriuose aprašomos nuostatos, kurios reikalingos kuriant Intrastat ataskaitas.

### <a name="set-up-all-required-intrastat-related-lists"></a>Nustatyti visus reikiamus su Intrastat susijusius sąrašus

|   Sąrašas   |   Papildoma informacija   |
|-------------------------|-------------------------|
| Prekių kodai | Nustatykite **Prekės kodo** tipo kategorijų hierarchiją ir pagal jungtinį nomenklatūrų sąrašą įveskite visų prekių kodus. Kiekvienai prekei nustatykite toliau nurodytą informaciją.<ul><li>Prekės pavadinimas ir prekės kodas.</li><li>Patogus pavadinimas ir (arba) išverstas pavadinimas.</li><li>Papildomų vienetų skelbimo parametrai skirtuke **Užsienio prekyba**. Papildomą vienetą galite pasirinkti vienetų sąraše. Taip pat galite nurodyti, ar be pasirinkto papildomo vieneto reikia skelbti prekių svorį.</li></ul>Norėdami gauti daugiau informacijos, peržiūrėkite [papildomų vienetų](#additional-units) pavyzdį.|
| Operacijų kodai | Nustatykite operacijos pobūdį pagal šalies / regiono reikalavimus. Kiekvienam operacijos kodui, kurį nustatote, turite nustatyti taisykles, skirtas skaičiuoti perkėlimo užsakymų ir pardavimo / pirkimo užsakymų SF sumoms ir statistinėms sumoms.<ul><li>Perkėlimo užsakymams nustatote vieną iš toliau pateiktų SF sumų ir statistinių sumų skaičiavimo taisyklių.<ul><li>**Tuščia** – suma bus 0 (nulis).</li><li>**Finansinių išlaidų suma** – suma bus lygi finansinėms išlaidoms.</li><li>**Bendrosios išlaidos** – suma bus lygi benrosioms operacijos išlaidoms.</li><li>**Rankin.** – suma bus lygi sumai, kuri rankiniu būdu nurodyta perkėlimo užsakymo eilutėje.</li></ul></li><li>Pardavimo užsakymams ir pirkimo užsakymams nustatote vieną iš toliau pateiktų SF sumų ir statistinių sumų skaičiavimo taisyklių.<ul><li>**Tuščia** – suma bus 0 (nulis).</li><li>**SF suma** – suma bus lygi prekės sumai, kuriai išrašyta SF.</li><li>**Bazinė suma** – suma bus lygi sumai, kuriai būtų išrašoma SF prieš taikant bet kokią nuolaidą.</li></ul></ul>Daugiau informacijos rasite operacijos [kodų ir papildomų išlaidų](#transaction-codes-and-miscellaneous-charges) pavyzdyje. |
| Transportavimo metodai | Nustatyti transportavimo režimą pagal šalies / regiono poreikius. Kiekvieno pristatymo būdo numatytąjį transportavimo būdą galite nustatyti **Užsienio prekybos** skirtuke. |
| Uostai | Jei toki informacija yra renkama jūsų šalyje / regione, nustatykite pakrovimo / iškrovimo uostą / oro uostą. |
| Statistikos procedūros | Jei tokia informacija yra renkama jūsų šalyje / regione, nustatykite statistinę procedūrą. |



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
<li>Pardavimo užsakymų, pirkimo užsakymų, kredito pažymų ir perkėlimo užsakymų numatytuosius operacijų kodus. Nustatytas kredito pažymų operacijų kodas taip pat naudojamas kaip fizinių prekių grąžinimo kodas bei naudojamas gretinti nuokrypio fizinių prekių grąžinimams ir koregavimo kredito pažymoms. Fizinių prekių grąžinimai yra pranešami „Intrastat“ perdavime su kita kryptimi. Atvykimo grąžinimas yra pranešamas kaip siuntimas ir siuntimo grąžinimas pranešamas kaip atvykimas.</li>
<li>Darbuotojas, atsakingas už Intrastat ataskaitų rengimą.</li>
</ul></li>
<li><strong>Minimali riba</strong> – nurodykite nuostatas, skirtas naujinti operacijoms, kurios yra žemiau ribinės reikšmės.
<ul>
<li>Ribinė suma ir svoris.</li>
<li>Prekės kodas, taikytinas operacijoms, esančioms žemiau ribinės reikšmės</li>
</ul></li>
<li><strong>Perkėlimas</strong> – nurodykite operacijų perkėlimo į Intrastat žurnalą kriterijus. Galite nurodyti, kad operacijos būtų perkeliamos tik tada, kai prekės atitinka vieną ar visus toliau nurodytus kriterijus.
<ul>
<li>Prekės nėra&#39; aptarnavimo prekės.</li>
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
  <li> <strong>Valiutos kurso tipas</strong> – (pasirinktinai) nurodykite valiutos kursą, kuris bus naudojamas Intrastat pardavimo ir pirkimo operacijų ataskaitoms užsienio valiutomis. Tai naudojama, jei tarifas yra kitoks, nei taikomas registruojant operaciją.</li>  
</ul></td>
</tr>
<tr class="even">
<td>Agento kontaktinė informacija</td>
<td>Nurodykite agento&#39; vardą ir pavardę, adresą, mokesčių lengvatos numerį, telefono numerį ir fakso numerį.</td>
</tr>
<tr class="odd">
<td>Šalies / regiono ypatybės</td>
<td>Dabartinio juridinio subjekto šalį / regioną nustatykite į <strong>Vietin.</strong>. ES šalių / regionų, dalyvaujančių ES prekyboje su dabartiniu juridiniu subjektu, šalį / regioną nustatykite į <strong>ES</strong>. Taip pat identifikuojate kiekvienos šalies / regiono kodą, skirtą užsienio prekybai.</td>
</tr>
<tr class="even">
<td>Numerių seka</td>
<td>Nurodykite Intrastat žurnalo numeraciją.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Pavyzdys

### <a name="transaction-codes-and-miscellaneous-charges"></a><a name= "transaction-codes-and-miscellaneous-charges"></a> Operacijų kodai ir papildomos išlaidos

Ši tema apima scenarijų, kuriame Vokietijos įmonė turi pirkti prekes iš Italijos įmonės. Kad šį pirkimą būtų galima atlikti, Vokietijos įmonė turi nustatyti naujus operacijų kodus ir konfigūruoti SF sumos ir statistinės sumos skaičiavimo taisykles tiems operacijų kodams. Be to, kai įmonė sukuria SF, ji turi nurodyti papildomas išlaidas ir jų procentus. Tos vertės bus skaičiuojamos apskaičiavus statistinę vertę.

Šis scenarijus naudoja **DEMF** juridinį subjektą.

#### <a name="preliminary-setup"></a>Pirminis nustatymas

1. Eikite **į organizacijos administravimo organizacijos** > **·** > **juridinius** subjektus ir pasirinkite **DEMF**.
2. Adresų **·** "FastTab" patikrinkite, ar **laukas Šalis /** regionas yra nustatytas į **DEU(Vokietija)**.
3. Eiti į **Mokėtinų** > **sumų tiekėjus** > **Visi** tiekėjai.
4. Tinklelyje pasirinkite **DE-001.**
5. Adreso **·** "FastTab" pasirinkite **Redaguoti**.
6. Dialogo lange **Redaguoti adresą** lauke **Šalis / regionas** pasirinkite **ITA**.
7. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

#### <a name="set-up-transaction-codes"></a>Nustatyti operacijų kodus

1. Pasirinkite **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **Operacijų kodai**.
2. Tinklelyje pasirinkite **„11”**. Tada veiksmų srityje pasirinkite **Naikinti**.
3. Veiksmų srityje pasirinkite **Naujas**.
4. Operacijų **kodų** "FastTab", lauke **Operacijos** **kodas**, įveskite **11.**
5. Lauke **Pavadinimas** įveskite stačio **pirkimo/pardavimo.**
6. Skyriaus **Pardavimas ir** Pirkimas lauke SF suma pasirinkite **SF** **sumą**.
7. Lauke **Statistinė** suma pasirinkite SF **sumą**.
8. Veiksmų srityje pasirinkite **Įrašyti**.

#### <a name="set-up-miscellaneous-charges"></a>Papildomų išlaidų nustatykite

1. Eikite **į mokėtinų** > **sumų išlaidų nustatymo** > **mokesčių** kodą.
2. Tinklelyje pasirinkite **Transportavimas**.
3. Veiksmų srityje pasirinkite **Redaguoti**.
4. Užsienio **prekybos** "FastTab" nustatykite **Intrastat SF vertės ir Intrastat statistinės vertės** **pasirinktis kaip** **Taip**.

#### <a name="set-up-foreign-trade-parameters"></a>Nustatyti užsienio prekybos parametrus

1. Pasirinkite **Mokesčiai** > **Nustatymai** > **Užsienio prekyba** > **Užsienio prekybos parametrai**.
2. Skirtuke **Intrastat** „FastTab” **Bendri**, **Perlaidos** **kode** laukelis rinkitės **11**.
3. Prekių **kodų hierarchijos** "FastTab" patikrinkite, **ar kategorijų** hierarchijos laukas nustatytas kaip **Intrastat**.

#### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

1. Eikite į **Mokėtinos sumos** > **Pirkimo užsakymai** > **Visi pirkimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Sukurti pirkimo užsakymą** lauke **Tiekėjo paskyra** pasirinkite **DE-001**.
4. Pasirinkite **Gerai**.
5. Skirtuko **Antraštė** „FastTab” **Užsienio** **prekyba** patikrinkite, ar laukas **Operacijos kodas** nustatytas į **11**.
6. Skirtuko **Eilutės** „FastTab” **Pirkimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **D0003**. Tada, lauke **Kiekis** įveskite **10**.
7. Eilutės **informacijos** "FastTab", skirtuke Užsienio prekyba, užsienio prekybos skyriuje patikrinkite, ar **automatiškai nustatytas operacijos kodo** **·** **laukas**.
8. Pirkimo **užsakymo eilučių** "FastTab", **esančiame meniu Finansai, skyriuje** **Mokesčiai**, pasirinkite Prižiūrėti **išlaidas**.
9. Lauke **Išlaidų kodas** pasirinkite **TRANSPORTAVIMAS**.
10. Lauke **Mokesčių vertė** įveskite **30**.
11. Veiksmų srityje pasirinkite **Įrašyti**. Tada uždarykite puslapį.
12. Veiksmų srities skirtuke **Pirkimas**, grupėje **Veiksmai**, pasirinkite **Patvirtinti**.
13. Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.
14. Veiksmų juostoje, pasirinkite **Numatyt. iš**. Lauke **Numatytasis eilučių kiekis** pasirinkite **Užsakytas kiekis**. Tada pasirinkite **Gerai**.
15. „FastTab” **Tiekėjo SF antraštė** skyriaus **Sąskaitos faktūros identifikavimas** lauke **Numeris** įveskite **00100**.
16. SF datų skyriaus SF datos lauke **pasirinkite** **·** **2021-11-24** (2021 m. lapkričio 24 d.).
17. Norėdami registruoti sąskaitą faktūrą, veiksmų srityje pasirinkite **Registruoti**.

### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Perkelti tiekėjo SF į Intrastat žurnalą

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Perduoti**.
3. Dialogo lange **„Intrastat” (perkėlimas)** nustatykite parinktį **Tiekėjo SF** į **Taip**.
4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą.

   ![Eilutė, nurodanti pirkimo užsakymą su papildomas išlaidas Intrastat puslapyje](media/intrastat_overview_1.png)

5. Pirkimo užsakymo skirtuko **Bendra** peržiūra. Atkreipkite dėmesį, kad SF vertės lauke rodoma SF sumos ir SF mokesčių sumos laukų suma, o lauke Statistinė vertė – statistinės sumos ir statistinių išlaidų **sumos** **laukų** **·** **·** **·** **suma**.

   ![Išsami pirkimo užsakymo informacija su išsamesnės informacijos apie papildomas išlaidas Intrastat puslapio skirtuke Bendra](media/intrastat_overview_2.png)

### <a name="transfer-order"></a>Perkėlimo užsakymas

Šiame pavyzdyje Įmonė Vokietijoje turi perkelti du prekių vienetus iš Vokietijos sandėlio į Italijos sandėlį. Šio produkto apskaitos išlaidos, kurių tarifas yra 20 procentų, taip pat turi būti nurodytos **lauke Statistinė** vertė. Šiame pavyzdyje naudojamas **DEMF** juridinis subjektas.

#### <a name="preliminary-setup"></a>Pirminis nustatymas

1. Eikite **į organizacijos administravimo organizacijos** > **·** > **juridinius** subjektus ir pasirinkite **DEMF**.
2. Adresų **·** "FastTab" patikrinkite, ar **laukas Šalis /** regionas yra nustatytas į **DEU(Vokietija)**.
3. Pasirinkite **Mokesčiai** > **Nustatymai** > **Užsienio prekyba** > **Užsienio prekybos parametrai**.
4. Prekių **kodų hierarchijos** "FastTab" patikrinkite, **ar kategorijų** hierarchijos laukas nustatytas kaip **Intrastat**.
5. Eiti į **Mokėtinų** > **sumų tiekėjus** > **Visi** tiekėjai.
6. Tinklelyje pasirinkite **DE-001.**
7. Adreso **·** "FastTab" pasirinkite **Redaguoti**.
8. Dialogo lange **Redaguoti adresą** lauke **Šalis / regionas** pasirinkite **ITA**.
9. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

#### <a name="set-up-transaction-codes"></a>Nustatyti operacijų kodus

1. Pasirinkite **Mokesčiai** > **Nustatymas** > **Užsienio prekyba** > **Operacijų kodai**.
2. Tinklelyje pasirinkite **„11”**. Tada veiksmų srityje pasirinkite **Naikinti**.
3. Veiksmų srityje pasirinkite **Naujas**.
4. Operacijų **kodų** "FastTab", lauke **Operacijos** **kodas**, įveskite **11.**
5. Lauke **Pavadinimas** įveskite stačio **pirkimo/pardavimo.**
6. Perkėlimo **užsakymų** skyriaus lauke **SF suma pasirinkite** Bendros **išlaidos**.
7. Lauke **Statistinė** suma pasirinkite Bendrosios **išlaidos**.
8. Veiksmų srityje pasirinkite **Įrašyti**.
9. Pasirinkite **Mokesčiai** > **Nustatymai** > **Užsienio prekyba** > **Užsienio prekybos parametrai**.
10. Intrastat **skirtuko** bendro **·** "FastTab" perkėlimo užsakymo **lauke pasirinkite** **11.**

#### <a name="set-up-charges-for-an-item"></a>Nustatyti prekės išlaidas

1. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Patvirtinti produktai**.
2. Tinklelyje pasirinkite **D0001**.
3. Užsienio **prekybos** "FastTab", esančio **Intrastat** skyriuje, išlaidų **procento** lauke, įveskite **20.**

#### <a name="change-the-site-address"></a>Vietos adreso keitimas

1. Eikite į **Sandėlio valdymas** > **Sąranka** > **Sandėlis** > **Vietos**.
2. Tinklelyje pasirinkite **„1”**.
3. „FastTab“ **Adresai** pasirinkite **Redaguoti**.
4. Dialogo lange **Redaguoti adresą** lauke **Šalis / regionas** pasirinkite **DEU**.
5. Pasirinkite **Gerai**.
6. Tinklelyje pasirinkite **„2”**.
7. „FastTab“ **Adresai** pasirinkite **Redaguoti**.
8. Dialogo lange **Redaguoti adresą** lauke **Šalis / regionas** pasirinkite **ITA**.
9. Pasirinkite **Gerai**.
10. Eikite į **„Warehouse Management”** > **Nustatymas** > **Sandėlis** > **Sandėliai**.
11. Tinklelyje pasirinkite **„21”**.
12. Skirtuko **Bendra** "FastTab" Nuorodos **skyriuje**, tiekėjo sąskaitos **lauke**, pasirinkite **DE-001.**

#### <a name="create-a-transfer-order"></a>Perdavimo užsakymo kūrimas

1. Eikite **į Atsargų valdymo siuntimo** > **užsakymus Perkėlimo** > **užsakymas**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Skirtuko **Eilutės** dalies Perkėlimo užsakymo **antraštės** "FastTab", skyriaus Peržiūra lauke **Iš** **sandėlio**, pasirinkite **11.** Lauke **Į** sandėlį pasirinkite **21.**
4. Skirtuko **Eilutės** perkėlimo užsakymo **eilutės** "FastTab" pasirinkite **Įtraukti**.
5. Lauke **Prekės numeris** pasirinkite **D0001**. Tada lauke **Perkelti kiekį** įveskite **2**.
6. Eilutės **informacijos** "FastTab", skirtuke Užsienio prekyba, užsienio prekybos skyriuje patikrinkite, ar **automatiškai nustatytas operacijos kodo** **·** **laukas**.
7. Veiksmų srities skirtuko Siuntimas **grupėje** **Operacijos pasirinkite** Siuntimo perkėlimo **užsakymas**.
8. Dialogo **lango** Siuntimas skirtuko Peržiūra lauke Atnaujinimas **pasirinkite** **·** **Visi**.
9. Pasirinkti **Gerai**, kad būtų galima siųsti užsakymą.
10. Veiksmų srities skirtuko Gauti **grupėje** **Operacijos pasirinkite** **Gauti**.
11. Dialogo **lango** Gauti skirtuko **Peržiūra lauke Atnaujinimas** pasirinkite **·** **Visi**.
12. Pasirinkti **Gerai**, kad būtų galima siųsti užsakymą.

#### <a name="transfer-the-transfer-order-to-the-intrastat-journal"></a>Perkelti perkėlimo užsakymą į Intrastat žurnalą

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Perduoti**.
3. Dialogo lange **Intrastat (Perkėlimas)** nustatykite perkėlimo užsakymo **pasirinktį** Taip, o **visas kitas** pasirinktis nustatykite **Ne**.
4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą.

   ![Eilutė, kuri rodo perkėlimo užsakymą Intrastat puslapyje](media/intrastat_overview_3.png)

5.  Peržiūrėti **perkėlimo** užsakymo skirtuką Bendra.

    Atkreipkite dėmesį, kad sf **vertės ir statistinės vertės skyrių laukai yra nustatomi** **automatiškai**. SF sumos **ir statistinės** sumos laukų vertės **paremtos** parametrais operacijų **kodų** puslapyje. Vertė **20** lauke Mokesčių procentas yra **vertė**, kuri nustatyta puslapyje **Išleistas** produktas. Lauke Statistinių išlaidų suma esanti vertė yra kiekybinė išlaidų **išraiška** (kadangi 107,24 lygi 20 procentų iš 536,18). Lauko Statistinė **vertė vertė yra** verčių iš laukų Statistinė **suma ir** **Statistinių išlaidų suma suma** suma.

  ![Perkėlimo užsakymo informacija Intrastat puslapio skirtuke Bendra](media/intrastat_overview_4.png)

### <a name="additional-units"></a>Papildomi vienetai

Šiame pavyzdyje Įmonė Vokietijoje turi pirkti 10 prekių vienetų iš Italijos įmonės. Turi būti nurodyti ne tik prekių kodai, bet ir papildomi šių prekių vienetai. Pavyzdys rodo, kaip sukurti naujus matavimo vienetus, Intrastat prekių kodui priskirti papildomus vienetus, registruoti operacijas, kuriose yra papildomų vienetų, ir peržiūrėti Intrastat žurnalą, kuriame nustatytas papildomų vienetų laukas.

#### <a name="preliminary-setup"></a>Pirminis nustatymas

1. Eikite **į organizacijos administravimo organizacijos** > **·** > **juridinius** subjektus ir pasirinkite **DEMF**.
2. Adresų **·** "FastTab" patikrinkite, ar **laukas Šalis /** regionas yra nustatytas į **DEU(Vokietija)**.
3. Pasirinkite **Mokesčiai** > **Nustatymai** > **Užsienio prekyba** > **Užsienio prekybos parametrai**.
4. Skirtuke **Intrastat** „FastTab” **Bendri**, **Perlaidos** **kode** laukelis rinkitės **11**.
5. Prekių **kodų hierarchijos** "FastTab" patikrinkite, **ar kategorijų** hierarchijos laukas nustatytas kaip **Intrastat**.
6. Eiti į **Mokėtinų** > **sumų tiekėjus** > **Visi** tiekėjai.
7. Tinklelyje pasirinkite **DE-001.**
8. Adreso **·** "FastTab" pasirinkite **Redaguoti**.
9. Dialogo lange **Redaguoti adresą** lauke **Šalis / regionas** pasirinkite **ITA**.
10. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą.

#### <a name="create-a-unit-of-measure"></a>Kurti matavimo vienetą

1. Eiti į Organizacijos **administravimo** > **nustatymo vienetų** > **·** > **vienetus**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Vienetas** įveskite matavimo vieneto pavadinimą. Šiame pavyzdyje įveskite **GRM**.
4. Skirtuko **Bendra** FastTab dalies **Klasifikacija lauke** Vieneto klasė pasirinkite **vieneto** matavimo ypatybę. Šiame pavyzdyje pasirinkite **Masinė**.
5. Vienetų **sistemos lauke** pasirinkite matavimo sistemą, kuriai priklauso vienetas. Pavyzdžiui, pasirinkite **metrikos** vienetus.

#### <a name="set-up-unit-conversions"></a>Nustatyti vienetų konvertavimus

1. Eikite **į Organizacijos administravimo nustatymo vienetų vienetų** > **·** > **·** > **konvertavimą**.
2. Skirtuke **Vidinės klasės** konvertavimai pasirinkite **Naujas**.
3. Vieneto **konvertavimo** dialogo lange, produkto **lauke**, pasirinkite **F00007.**
4. Lauke **Iš** vieneto pasirinkite **el**.
5. Lauke **Į** vienetą pasirinkite **GRM**.
6. Patikrinkite, ar konvertavimo kursas yra **1 =** 1.
7. Pasirinkite **Gerai**.
8. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Patvirtinti produktai**.
9. Tinklelyje pasirinkite **F00007**.
10. Skirtuko **Valdyti atsargas** "FastTab", atsargų **skyriaus** lauke **Vienetas**, pasirinkite **GRM**.
11. Veiksmų srityje pasirinkite **Įrašyti**.

#### <a name="set-up-product-information"></a>Produkto informacijos nustatymas

1. Eikite į **Produkto informacijos valdymas** > **Produktai** > **Patvirtinti produktai**.
2. Tinklelyje pasirinkite **F00007**.
3. „FastTab” **Užsienio prekyba** srityje **Intrastat** lauke **Prekės** rinkitės **920 20 34**.
4. Veiksmų srityje pasirinkite **Įrašyti**.

#### <a name="assign-the-additional-unit-to-an-intrastate-commodity-code"></a>Priskirti papildomą vienetą Intrastat prekės kodui

1. Pasirinkite **Produkto informacijos valdymas** > **Nustatymas** > **Kategorijos ir atributai** > **Kategorijų hierarchijos**.
2. Sąraše pasirinkite **Intrastat**.
3. Tinklelyje pasirinkite **dėsniai**.
4. Užsienio **prekybos** "FastTab", lauke **Papildomi** vienetai, pasirinkite **GRM**.
5. Veiksmų srityje pasirinkite **Įrašyti**.

   Daugiau informacijos rasite Valdyti [matavimo vienetus](../../supply-chain/pim/tasks/manage-unit-measure.md).

#### <a name="create-a-purchase-order"></a>Pirkimo užsakymo kūrimas

1. Eikite į **Mokėtinos sumos** > **Pirkimo užsakymai** > **Visi pirkimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Dialogo lango **Sukurti pirkimo užsakymą** lauke **Tiekėjo paskyra** pasirinkite **DE-001**.
4. Pasirinkite **Gerai**.
5. Skirtuko **Antraštė** „FastTab” **Užsienio** **prekyba** patikrinkite, ar laukas **Operacijos kodas** nustatytas į **11**.
6. Skirtuko **Eilutės** „FastTab” **Pirkimo užsakymo eilutės** lauke **Prekės numeris** pasirinkite **F00007**. Tada, lauke **Kiekis** įveskite **10**.
7. Eilutės informacijos FastTab, skirtuke Užsienio prekyba, užsienio prekybos skyriuje patikrinkite, ar operacijos kodas ir **prekių** laukai yra **nustatyti** **·** **·** **automatiškai**.
8. Veiksmų srities skirtuke **Pirkimas**, grupėje **Veiksmai**, pasirinkite **Patvirtinti**.
9. Veiksmų srities skirtuke **SF**, esančiame grupėje **Generuoti**, pasirinkite **SF**.
10. Veiksmų juostoje, pasirinkite **Numatyt. iš**. Lauke **Numatytasis eilučių kiekis** pasirinkite **Užsakytas kiekis**. Tada pasirinkite **Gerai**.
11. Tiekėjo **SF antraštės** "FastTab", SF identifikavimo **skyriaus** lauke **Numeris**, įveskite **VE-0010.**
12. SF datų skyriaus SF datos lauke **pasirinkite** **·** **2021-05-10** (2021 m. spalio 5 d.).
13. Norėdami registruoti sąskaitą faktūrą, veiksmų srityje pasirinkite **Registruoti**.

#### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Perkelti tiekėjo SF į Intrastat žurnalą

1. Pasirinkite **Mokesčiai** > **Deklaracijos** > **Užsienio prekyba** > **Intrastat**.
2. Veiksmų srityje pasirinkite **Perduoti**.
3. Dialogo lange **„Intrastat” (perkėlimas)** nustatykite parinktį **Tiekėjo SF** į **Taip**.
4. Norėdami perkelti operacijas, pasirinkite **Gerai**, tada peržiūrėkite „Intrastat” žurnalą.

   ![Eilutė, kuri rodo pirkimo užsakymą Intrastat puslapyje](media/intrastat_overview_5.png)

5. Pirkimo užsakymo skirtuko **Bendra** peržiūra. Atkreipkite **dėmesį, kad** skyriaus **Vienetas laukai** Papildomų vienetų kiekis ir Papildomi vienetai nustatomi **automatiškai**.

   ![Išsami pirkimo užsakymo informacija Intrastat puslapio skirtuke Bendra](media/intrastat_overview_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
