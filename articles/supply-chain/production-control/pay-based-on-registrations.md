---
title: Apmokėjimas pagal registracijas
description: Šioje temoje paaiškinama, kaip apskaičiuojamas užmokestis pagal darbuotojo registracijas.
author: johanhoffmann
ms.date: 03/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgCalcApproveWeekView, JmgProdStatusListPagePayrollCostDetails, JmgPayCountTable, JmgPayStatConfig, JmgOvertimeSlize, JmgPayAgreementOverride, JmgPayCountSum, JmgPayAdjustSetup, JmgPayAdjustCostType, JmgPayEmployee, JmgMESBreak, JmgPayAddTable, JmgPayAddTransSelectTransId, JmgPayrollCostDetailsPart, jmgProdStatusListPagePayrollCosts, JmgPayrollCostPart, JmgPayEvents, JmgTermRegPayStatSetup, JmgPayStatGroup, JmgPayAddTrans, JmgPayStatTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 58ff2629c2894e85ca5529df5f995ffa5273de67e1c22564f5f9911ea86fbd95
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715727"
---
# <a name="pay-based-on-registrations"></a>Apmokėjimas pagal registracijas

[!include [banner](../includes/banner.md)]

Šioje temoje išsamiai paaiškinama, kaip apskaičiuojamas užmokestis pagal darbuotojo registracijas. Pateikiami pavyzdžiai, kuriuose nurodoma, kaip keičiasi rezultatas priklausomai nuo įvairių skaičiavimo sąrankos pasirinkčių kombinacijų. Toliau nurodoma keletas sričių, kurios bus įtrauktos.

- Nukrypimo laikas
- Viršvalandžiai
- Pertraukos
- Perjungti kodus
- Mokėjimo elementai
- Mokėjimo sąlygos
- Laiko ir buvimo darbe skaičiavimo parametrai
- Neatvykimas

## <a name="the-use-of-flex-time"></a>Nukrypimo laiko naudojimas

Nukrypimo laiko laikotarpiai nustatomi laiko šablonuose, kurie naudojami srityje Laikas ir buvimas darbe. Yra du nukrypimo šablonų tipai: **Nukrypimas+** ir **Nukrypimas-**. Darbuotojui užregistravus laiką pasirenkant laikotarpį Nukrypimas+, darbuotojo nukrypimo balansas didėja pagal atidirbtų darbo valandų skaičių. Už valandas, atidirbtas laikotarpiu Nukrypimas+, darbuotojas jokios kompensacijos negauna. Tačiau darbuotojas gali atostogauti Nukrypimo- laikotarpiais ir gauti kompensaciją, panaudodamas valandas iš savo nukrypimo balanso. Todėl atostogas nukrypimo laikotarpiais sistema laiko neatvykimu į darbą.

## <a name="scenarios-based-on-flex-periods"></a>Scenarijai pagal nukrypimo laikotarpius

Du toliau nurodyti scenarijai paremti darbo dieną atitinkančiu nukrypimo šablonu. Abiejų scenarijų atvejais užmokestis apskaičiuojamas pagal nukrypimo laikotarpį, kai darbuotojas nurodo atėjimo į darbą ir išėjimo iš darbo valandas.

### <a name="flex-profile-for-one-workday"></a>Vienos darbo dienos nukrypimo šablonas

| Šablono tipas  | Pradžios    | Pabaigoje      | Diena     |
|---------------|----------|----------|---------|
| Viršvalandžiai     | 00:00 | 06:00 | Pirmadienis  |
| Nukrypimas+         | 06:00 | 07:00 | Pirmadienis  |
| Atėjimas į darbą      | 07:00 | 07:00 | Pirmadienis  |
| Standartinis laikas | 07:00 | 14:30 | Pirmadienis  |
| Nukrypimas-         | 14:30 | 15:30 | Pirmadienis  |
| Išėjimas iš darbo     | 15:30 | 15:30 | Pirmadienis  |
| Viršvalandžiai     | 15:30 | 06:00 | Antradienis |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>1 scenarijus: darbuotojas užregistruoja atėjimo į darbą valandą laikotarpiu Nukrypimas+, o išėjimo iš darbo valandą laikotarpiu Nukrypimas-

Toliau pateikiami darbuotojo registracijų pavyzdžiai.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      |
|---------------------------|----------|----------|
| Atėjimas į darbą                  | 06:30 | 06:30 |
| Gamybos užduotis            | 06:30 | 14:45 |
| Išėjimas iš darbo                 | 14:45 | 14:45 |

Užregistruoti darbuotojo darbo dienos laikai įskaičiuojami ir perkeliami į puslapyje **Patvirtinimas** nurodytą mokėjimą (**Laikas ir buvimas darbe** &gt; **Peržiūra ir patvirtinimas** &gt; **Patvirtinimas**). Įskaičiavus registruojamus darbo dienos laikus skaičiavimo rezultatą galima peržiūrėti skirtuke **Laikai**. 

Norėdami suprasti šį scenarijų, peržiūrėkite toliau nurodytus laukus.

| Nukrypimas + | Nukrypimas - | Laikas | Mokėjimo laikas |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8,25 | 8,50     |

#### <a name="calculation-of-flex"></a>Nukrypimas+ skaičiavimas

Pagal nukrypimo šabloną, laikas nuo 06:00 iki 07:00 vadinamas laikotarpiu Nukrypimas+. Todėl, jei darbuotojas ateina į darbą 06:30, uždirba už 0,5 valandos. Šis laiko kiekis įskaičiuojamas į darbuotojo nukrypimo sąskaitą.

#### <a name="calculation-of-flex-"></a>Nukrypimas- skaičiavimas

Pagal nukrypimo šabloną, laikotarpis Nukrypimas- prasideda 14:30, o baigiasi 15:30. Todėl, jei darbuotojas išeina iš darbo 14:45, likusios 45 laikotarpio Nukrypimas- minutės (0,75 val.) registruojamos kaip apmokamas laikas ir tas pats laiko kiekis atskaičiuojamas iš darbuotojo nukrypimo sąskaitos. Šios 45 minutės įtraukiamos į apmokamą laiką, nes darbuotojui apmokama už likusias 45 laikotarpio Nukrypimas- minutes. Darbuotojui neatvykus į darbą laikotarpiu Nukrypimas-, šios 45 minutės atskaičiuojamos iš jo nukrypimo sąskaitos.

#### <a name="calculation-of-time"></a>Laiko skaičiavimas

Laikas skaičiuojamas nuo atėjimo į darbą iki išėjimo iš darbo, t. y. nuo 06:30 iki 14:45 ir iš viso apima 8,25 val.

#### <a name="calculation-of-pay-time"></a>Apmokamo laiko skaičiavimas

Apmokamas laikas yra laikas, už kurį darbuotojui apmokama. Pagal šį scenarijų darbuotojas dirba 8,25 val. (**Laikas**). Tačiau **Apmokamas laikas** skaičiuojamas už 8,50 val., nes darbuotojui apmokama už Nukrypimo- laikotarpį po išėjimo iš darbo. Apmokamas laikas atitinka suplanuotas darbo valandas, nes Nukrypimas+ laikas įtraukiamas į darbuotojo nukrypimo sąskaitą, o ne į apmokamą laiką. Neatvykimo į darbą laikas laikotarpiu Nukrypimas- kompensuojamas pagal apmokamą laiką ir atskaičiuojamas iš darbuotojo nukrypimo sąskaitos.

| Laikas              | Registracijos tipas | Apmokamas laikas (valandos)      |
|-------------------|-------------------|-----------------------|
| 6:30 – 7:00 | Nukrypimas+             | 0                     |
| 7:00 – 14:45 | Standartinis laikas     | 7,75                  |
| 14:45 – 15:30 | Nukrypimas-             | 0,75 (neatvykimo laikotarpis) |
|                   | Iš viso             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>2 scenarijus: darbuotojas dirba visą laikotarpį Nukrypimas-, taip pat dirba viršvalandžius

Toliau pateikiami darbuotojo darbo dienos registracijų pavyzdžiai.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      |
|---------------------------|----------|----------|
| Atėjimas į darbą                  | 06:30 | 06:30 |
| Gamybos užduotis            | 06:30 | 17:00 |
| Išėjimas iš darbo                 | 17:00 | 17:00 |

Puslapyje **Patvirtinimas** apskaičiavę žurnalo registracijas, skirtuke **Laikai** galite peržiūrėti skaičiavimo rezultatą. Norėdami suprasti šį scenarijų, peržiūrėkite toliau nurodytus laukus.

| Nukrypimas + | Nukrypimas - | Laikas  | Mokėjimo laikas | Mokėjimas už viršvalandžius |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | 10,50 | 10,00    | 1.50         |

#### <a name="calculation-of-flex"></a>Nukrypimas+ skaičiavimas

Pagal nukrypimo šabloną, laikas nuo 06:00 iki 07:00 vadinamas laikotarpiu Nukrypimas+. Todėl, jei darbuotojas ateina į darbą 06:30, į savo nukrypimo sąskaitą jis uždirba už 0,5 val. Nukrypimo+ laiko.

#### <a name="calculation-of-flex-"></a>Nukrypimas- skaičiavimas

Jei darbuotoja laikotarpiu Nukrypimas- dirba, Nukrypimas- neskaičiuojamas. Nukrypimas- skaičiuojamas tik darbuotojai laikotarpiu Nukrypimas- nesant darbe. Mokėjimo atžvilgiu, jei darbuotojas dirba Nukrypimo- laikotarpiu, jam apmokama pagal standartinio laiko užmokesčio tarifą. Darbuotojui neatvykus į darbą Nukrypimo- laikotarpiu, šios 45 minutės atskaičiuojamos iš jo nukrypimo sąskaitos.

#### <a name="calculation-of-time"></a>Laiko skaičiavimas

Laikas skaičiuojamas nuo atėjimo į darbą 06:30 iki išėjimo iš darbo 17:00 arba 10,50 val.

#### <a name="calculation-of-pay-time"></a>Apmokamo laiko skaičiavimas

Pagal šį scenarijų darbuotojas dirba 10,50 val. (**Laikas**). Tačiau **Apmokamas laikas** skaičiuojamas 10,00 val., nes už laikotarpį Nukrypimas+ darbuotojui nemokama.

#### <a name="calculation-of-pay-overtime"></a>Apmokamų viršvalandžių skaičiavimas

| Laikas               | Registracijos tipas | Apmokamas laikas (valandos) |
|--------------------|-------------------|------------------|
| 6:30 – 7:00  | Nukrypimas+             | 0                |
| 7:00 – 14:30  | Standartinis laikas     | 7,50             |
| 14:30 – 15:30  | Nukrypimas-             | 1,00             |
| 15:30 – 17:00 | Viršvalandžiai          | 1.50             |
|                    | Iš viso             | 10,00            |

### <a name="generation-of-pay-items"></a>Mokėjimo elementų generavimas

Užregistruotus darbuotojo darbo dienos laikus galima perkelti iš puslapio **Patvirtinimas**. Vykstant perkėlimo procesui generuojami mokėjimo elementai ir perkelti užregistruoti laikai. Mokėjimo elementai atitinka mokėjimo laiko paskirstymą į standartinį laiką, viršvalandžius, mokamą pertraukų laiką ir t. t.

Norėdami atidaryti mokėjimo elementų sąrašą, pasirinkite **Laikas ir buvimas darbe** &gt; **Peržiūra ir patvirtinimas** &gt; **Patvirtinimas**. Po to pasirinkite **Užklausa** &gt; **Perkelti užregistruoti laikai**.

Mokėjimo elementai sudaro darbuotojo darbo užmokesčio pagrindą. Galite sukurti failą, į kurį įtraukiama iš mokėjimo elementų gauta informacija, ir perkelti tą failą į algalapio sistemą.

Vykdant perkėlimo procesą, gamybos ir projekto veiklos laikas ir išlaidos perkeliamos į gamybos ir projekto žurnalus, kad būtų rengiama praleisto laiko ir patirtų išlaidų ataskaita. Perkelti užregistruoti laikai sudaro gamybos užsakymų ir projektų laiko ir išlaidų kainos už valandą pagrindą. Perkelti užregistruoti laikai atidaromi naudojantis puslapio **Patvirtinimas** meniu **Užklausa**.

Pavyzdžiui, 2 scenarijaus atveju generuojami toliau nurodyti mokėjimo elementai.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas  | Bendroji savikaina |
|---------------|----------|-----------|-------|------------|
| Standartinis laikas | 1 201     | 10,0      | 10    | 100        |
| Viršvalandžiai      | 1301     | 1.50      | 5     | 7,50       |
|               |          |           | Iš viso | 107,50     |

Standartinio laiko mokėjimo elemento mokėjimo vienetą sudaro 10 valandų ir jis apima standartinį laiką, Nukrypimas- laiką ir viršvalandžius. Standartinis laikas, Nukrypimas- laikas ir viršvalandžiai sujungiami į vieną mokėjimo elementą, nes, pagal numatytąją puslapio **Skaičiavimo parametrai** (**Laikas ir buvimas darbe** &gt; **Sąranka** &gt; **Skaičiavimo parametrai**) parametro nuostatą, visi tipai skaičiuojami kaip standartinis laikas. Viršvalandžiai skaičiuojami kaip pridėtinis laikas prie standartinio laiko naudojant papildomą tarifą 5.

Norint aiškiai atskirti standartinį laiką nuo viršvalandžių, kad mokėjimo tipų mokėjimo vienetai apimtų tik faktinį pridėtinį prie standartinio laiko pridėtą laiką ir viršvalandžius, standartinio laiko mokėjimo vienetai turi būti skaičiuojami kaip 8,50, o viršvalandžių mokėjimo vienetai – kaip 1,50.

Norint sukonfigūruoti, kad sistema aiškiai atskirtų standartinį laiką ir viršvalandžius, viršvalandžiai negali būti įtraukiami į standartinį laiką. Taip pat būtina pakeisti viršvalandžių mokėjimo tipo sąranką, kad užmokesčio už viršvalandžius tarifas apimtų visus mokėjimus už darbą ne darbo valandomis.

### <a name="exclude-overtime-from-the-standard-time"></a>Viršvalandžių neįtraukimas į standartinį laiką

Puslapyje **Skaičiavimo parametrai** pasirinkite šablono specifikacijos tipą **Viršvalandžiai**, po to nustatykite parametro **Mokėjimo laikas** parinktį **Ne**, kaip parodyta toliau.

| Reg. specifikacija | Šablono specifikacijos tipas | Skaičiavimas   | Parametras | Apmokėta         | Parametras |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Darbo laikas       | Viršvalandžiai                   | Standartinis laikas | Taip | Mokėjimo laikas     | nr.  |
|                    |                            | Mokėjimo laikas      | Taip | Mokėjimas už viršvalandžius | Taip |

Pakoregavus skaičiavimo parametrus sugeneruojami toliau nurodyti mokėjimo elementai.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas  | Bendroji savikaina |
|---------------|----------|-----------|-------|------------|
| Standartinis laikas | 1 201     | 8,50      | 10    | 85,0       |
| Viršvalandžiai      | 1301     | 1.50      | 15    | 22,50      |
|               |          |           | Iš viso | 107,50     |

> [!NOTE]
> Rekomenduojama naudoti standartinę skaičiavimo parametrų nuostatą. Apskritai, keisdami šiuos parametrus turėtumėte būti atsargūs. Norėdami atkurti rekomenduojamus standartinius parametrus, puslapyje **Skaičiavimo parametrai** pasirinkite **Atkurti vertes**.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Nuokrypis nuo standartinių mokėjimo šablonų

Puslapyje **Šablonai** (**Laikas ir buvimas darbe** &gt; **Sąranka** &gt; **Laiko šablonai** &gt; **Šablonai**) galite nustatyti šablonų tipus, apimančius kodų perjungimą ir pertraukas.

### <a name="switch-codes"></a>Perjungti kodus

Naudojantis kodų perjungimo funkcija darbuotojai gali nukrypti nuo šablono tipo, pakeisdami jį į kitą šablono tipą. Pavyzdžiui, darbuotojas gali pakeisti Nukrypimas+ laiką į viršvalandžius. Registruodamasis darbuotojas gali įtraukti perjungimo kodą arba registracijas patvirtinančiam asmeniui galite priskirti perjungimo kodo įtraukimo užduotį.

Prieš naudodamiesi perjungimo kodu privalote nustatyti jį kaip netiesioginės veiklos tipą. Po to turite įtraukti tam laikotarpiui, kurio metu norite galėti keisti šablono tipą, skirto laiko šablono perjungimo kodą. Pavyzdžiui, atlikę šiuos veiksmus galite sukurti perjungimo kodą, kad būtų galima keisti laikotarpį Nukrypimas+ į viršvalandžius nuo 06:00 iki 07:00.

1. Sukurkite perjungimo kodą, kurio pavadinimas **OTBCI (nukrypimo pavertimas viršvalandžiais prieš atėjimą į darbą)**. Pasirinkite **Laikas ir buvimas darbe** &gt; **Netiesioginių veiklų valdymas** &gt; **Netiesioginės veiklos**.
2. Stulpelio **Perjungimo kodas** laiko šablono Nukrypimas+ eilutėje įtraukite OTBCI.
3. Stulpelyje **Antrinis** įtraukite šablono tipą **Viršvalandžiai**.

Apsvarstykite galimybę naudotis toliau nurodytu darbo dieną atitinkančiu nukrypimo šablonu.

| Šablono tipas  | Pradžios    | Pabaigoje      | Diena     |
|---------------|----------|----------|---------|
| Viršvalandžiai     | 00:00 | 06:00 | Pirmadienis  |
| Nukrypimas+         | 06:00 | 07:00 | Pirmadienis  |
| Atėjimas į darbą      | 07:00 | 07:00 | Pirmadienis  |
| Standartinis laikas | 07:00 | 14:30 | Pirmadienis  |
| Nukrypimas-         | 14:30 | 15:30 | Pirmadienis  |
| Išėjimas iš darbo     | 15:30 | 15:30 | Pirmadienis  |
| Viršvalandžiai     | 15:30 | 06:00 | Antradienis |

Toliau nurodomos darbuotojo darbo dienos registracijos.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      |
|---------------------------|----------|----------|
| Atėjimas į darbą                  | 06:30 | 06:30 |
| Gamybos užduotis            | 06:30 | 14:45 |
| Išėjimas iš darbo                 | 17:00 | 17:00 |

Po perkėlimo sugeneruojami toliau nurodyti mokėjimo elementai.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas  | Bendroji savikaina |
|---------------|----------|-----------|-------|------------|
| Standartinis laikas | 1 201     | 8,50      | 10    | 85,0       |
| Viršvalandžiai      | 1305     | 1.50      | 15    | 22,50      |
|               |          |           | Iš viso | 107,50     |

Puslapyje **Patvirtinimas** atšaukite perkėlimą, po to, naudodamiesi meniu **Perjungimo kodas**, taikykite **OTBCI** perjungimo kodą. Perkėlus registracijas antrą kartą sugeneruojami toliau nurodyti mokėjimo elementai.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas  | Bendroji savikaina |
|---------------|----------|-----------|-------|------------|
| Standartinis laikas | 1 201     | 8,50      | 10    | 80,0       |
| Viršvalandžiai      | 1305     | 2,00      | 15    | 30,0       |
|               |          |           | Iš viso | 107,50     |

> [!NOTE]
> Taikant perjungimo kodą viršvalandžiai pailginami 0,5 val. nuo 1,50 iki 2,00. Ši 0,5 valandos – tai užregistruotas Nukrypimas+ laikas, paverstas į viršvalandžius nuo 6:30 iki 07:00.

### <a name="breaks"></a>Pertraukos

Darbuotojo užmokestis priklauso ir nuo pertraukų nuo darbo. Pertraukos apibrėžiamos kaip netiesioginės veiklos tipas. Jos gali būti **Apmokamos**, kai užmokestį už pertrauką galima įtraukti į darbuotojo užmokestį, arba **Neapmokamos**, kad užmokesčio už pertrauką negalima įtraukti į darbuotojo užmokestį. Pertrauka taip pat gali būti apibrėžiama kaip **Suplanuota** arba **Registruota**.

#### <a name="planned-breaks"></a>Suplanuotos pertraukos

Jei įmonėje yra nustatytas pastovus pertraukos laikas, pavyzdžiui, fiksuota pietų pertrauka, šią pertrauką galima iš anksto nurodyti laiko šablone. Šiuo atveju darbuotojui nebūtina registruoti pertraukos užduoties kortelės puslapiuose. Puslapyje **Patvirtinimas** skaičiuojant darbuotojo užregistruotus darbo dienos laikus pertrauka įtraukiama automatiškai.

#### <a name="registered-breaks"></a>Registruotos pertraukos

Jei įmonėje pertraukos neplanuojamos, darbuotojai gali registruoti pertraukas per visą darbo dieną. Registruotas pertraukas galima naudoti, pvz., jei darbuotojas dirba pagal nukrypimo laiko šabloną, kai nėra nurodytas atėjimo į darbą ir išėjimo iš darbo laikas. Registruotos pertraukos yra netiesioginės veiklos tipas. Darbuotojas užregistruoja pertrauką terminalo puslapyje **Užduoties kortelė** arba įrenginio puslapyje **Užduoties kortelė**. Naudotojas gali pasirinkti pertraukos tipą abiejuose šiuose puslapiuose esančiuose iš anksto numatytų pertraukos veiklų sąrašuose.

#### <a name="paid-and-unpaid-breaks"></a>Apmokamos ir neapmokamos pertraukos

Galima nustatyti pertraukos veiklos parinktį **Apmokama** arba **Neapmokama**. Apmokama pertrauka įtraukiama skaičiuojant mokėjimo laiką ir sistema naudoja registracijos tipo **Pertrauka** mokėjimo sutartyje nurodytą mokėjimo tipą.

### <a name="example-of-a-planned-break"></a>Suplanuotos pertraukos pavyzdys

Apsvarstykite galimybę naudoti toliau nurodytą laiko šabloną, kuriame nurodoma neapmokama pietų pertrauka.

| Šablono tipas  | Pradžios    | Pabaigoje      | Diena     |
|---------------|----------|----------|---------|
| Viršvalandžiai     | 00:00 | 06:00 | Pirmadienis  |
| Nukrypimas+         | 06:00 | 07:00 | Pirmadienis  |
| Atėjimas į darbą      | 07:00 | 07:00 | Pirmadienis  |
| Standartinis laikas | 07:00 | 12:00 | Pirmadienis  |
| Pertrauka         | 12:00 | 12:30 | Pirmadienis  |
| Standartinis laikas | 12:30 | 14:30 | Pirmadienis  |
| Nukrypimas-         | 14:30 | 15:30 | Pirmadienis  |
| Išėjimas iš darbo     | 15:30 | 15:30 | Pirmadienis  |
| Viršvalandžiai     | 15:30 | 06:00 | Antradienis |

Toliau nurodomos darbuotojo darbo dienos registracijos.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      |
|---------------------------|----------|----------|
| Atėjimas į darbą                  | 06:30 | 06:30 |
| Gamybos užduotis            | 06:30 | 14:45 |
| Išėjimas iš darbo                 | 17:00 | 17:00 |

Puslapyje **Patvirtinimas** apskaičiavę žurnalo registracijas, skirtuke **Laikai** galite peržiūrėti skaičiavimo rezultatą. Norėdami suprasti šį scenarijų, peržiūrėkite toliau nurodytus laukus.

| Nukrypimas + | Nukrypimas - | Laikas  | Mokėjimo laikas | Neapmokamas pertraukos laikas | Mokėjimas už viršvalandžius |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

> [!NOTE] 
> Sistema apskaičiavo 0,5 valandos neapmokamo pertraukos laiko ir šis laikas nepriskiriamas apmokamam darbo laikui.

### <a name="example-of-a-registered-break"></a>Užregistruotos pertraukos pavyzdys

Apsvarstykite galimybę naudoti toliau nurodytą laiko šabloną, kuriame nenurodomos suplanuotos pertraukos.

| Šablono tipas  | Pradžios    | Pabaigoje      | Diena     |
|---------------|----------|----------|---------|
| Viršvalandžiai     | 00:00 | 06:00 | Pirmadienis  |
| Nukrypimas+         | 06:00 | 07:00 | Pirmadienis  |
| Atėjimas į darbą      | 07:00 | 07:00 | Pirmadienis  |
| Standartinis laikas | 07:00 | 14:30 | Pirmadienis  |
| Nukrypimas-         | 14:30 | 15:30 | Pirmadienis  |
| Išėjimas iš darbo     | 15:30 | 15:30 | Pirmadienis  |
| Viršvalandžiai     | 15:30 | 06:00 | Antradienis |

Toliau nurodomos darbuotojo darbo dienos registracijos.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      |
|---------------------------|----------|----------|
| Atėjimas į darbą                  | 06:30 | 06:30 |
| Gamybos užduotis            | 06:30 | 17:00 |
| Pertrauka                     | 12:03 | 12:32 |
| Išėjimas iš darbo                 | 17:00 | 17:00 |

Apskaičiavus registracijas skaičiuojamas veiklų laikas.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      | Laikas  |
|---------------------------|----------|----------|-------|
| Atėjimas į darbą                  | 06:30 | 06:30 |       |
| Gamybos užduotis            | 06:30 | 17:00 | 10,00 |
| Pertrauka                     | 12:03 | 12:32 | 0,50  |
| Išėjimas iš darbo                 | 17:00 | 17:00 |       |

> [!NOTE]
> Pertraukos laikas sutampa su veiklos laiku (šiame pavyzdyje – gamybos užduotis). Ši elgsena visada naudojama pertraukos veikloms. Apskaičiavus užregistruotus darbo dienos laikus pertraukos laikas atimamas iš veiklos laiko. Tokiu atveju gamybos užduoties trukmė – 10,50 val., tačiau skaičiuojamas laikas yra 10 val., nes iš veiklos laiko atimamas 0,5 val. trukmės pertraukos laikas.

Puslapyje **Patvirtinimas** apskaičiavę žurnalo registracijas, skirtuke **Laikai** galite peržiūrėti skaičiavimo rezultatą. Norėdami suprasti šį scenarijų, peržiūrėkite toliau nurodytus laukus.

| Nukrypimas + | Nukrypimas - | Laikas  | Mokėjimo laikas | Neapmokamas pertraukos laikas | Mokėjimas už viršvalandžius |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

Jei vietoj neapmokamos pertraukos suplanuota apmokama pertrauka, toliau nurodomas tokio skaičiavimo rezultato pavyzdys.

| Nukrypimas + | Nukrypimas - | Laikas  | Mokėjimo laikas | Mokamos pertraukos laikas | Mokėjimas už viršvalandžius |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | 10,50 | 10,00    | 0,5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Mokėjimo elementai ir apmokamos pertraukos

Perkėlus puslapyje **Patvirtinimas** esančias registracijas sugeneruojami mokėjimo elementai. Sukuriamas atskiras apmokamų pertraukų mokėjimo elementas.

Apmokamos pertraukos užmokesčio tarifas nustatomas pagal pertraukų apmokėjimo sutartyse nustatytą mokėjimo tipą. Užuot naudojęsi mokėjimo tipu galite nustatyti nurodyto datos intervalo pertraukos savikainą už valandą.

Apsvarstykite galimybę naudoti toliau pateikiamą laiko šabloną.

| Šablono tipas  | Pradžios    | Pabaigoje      | Diena     |
|---------------|----------|----------|---------|
| Viršvalandžiai     | 00:00 | 06:00 | Pirmadienis  |
| Nukrypimas+         | 06:00 | 07:00 | Pirmadienis  |
| Atėjimas į darbą      | 07:00 | 07:00 | Pirmadienis  |
| Standartinis laikas | 07:00 | 14:30 | Pirmadienis  |
| Nukrypimas-         | 14:30 | 15:30 | Pirmadienis  |
| Išėjimas iš darbo     | 15:30 | 15:30 | Pirmadienis  |
| Viršvalandžiai     | 15:30 | 06:00 | Antradienis |

Toliau nurodomos darbuotojo darbo dienos registracijos.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      | Laikas |
|---------------------------|----------|----------|------|
| Atėjimas į darbą                  | 07:00 | 07:00 |      |
| Gamybos užduotis            | 07:00 | 15:00 | 7,5  |
| Pertrauka (apmokama)              | 12:00 | 12:30 | 0,5  |
| Išėjimas iš darbo                 | 15:00 | 15:00 |      |

Pavyzdžiui, nustatomas standartinio laiko mokėjimo tipas **1201**, o mokėjimo sutartyje nustatomas užmokesčio tarifas **10**. Apmokamos pertraukos mokėjimo tipas **1301**, o užmokesčio koeficientas **8**. Perkėlus registracijas sugeneruojami toliau nurodyti mokėjimo elementai.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas |
|---------------|----------|-----------|------|
| Standartinis laikas | 1 201     | 7,50      | 10   |
| Nukrypimas-         | 1 201     | 0,50      | 10   |
| Pertrauka (apmokama)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Kaip išlaidos už apmokamas pertraukas paskirstomos projektams ir gamybos užsakymams

Galima nustatyti tokias valandines išlaidas už projektų veiklas ir gamybos užduotis, kad jos būtų paskiriamos pagal srityje Laikas ir buvimas darbe apskaičiuotus užmokesčio tarifus arba pagal nurodytas veiklų išlaidų kategorijas.

Norėdami nustatyti išlaidų kategoriją, pasirinkite **Gamybos kontrolė** &gt; **Sąranka** &gt; **Gamybos vykdymas** &gt; **Numatytieji gamybos užsakymai** ir nustatykite lauko **Išlaidų kategorija** parinktį **Taip** arba **Ne**.

- **Ne** – išlaidos apskaičiuojamos pagal nustatytus srities Laikas ir buvimas darbe registracijos tipų užmokesčio tarifus.
- **Taip** – išlaidos apskaičiuojamos pagal gamybos ir projekto veiklų išlaidų kategorijas.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Išlaidų skaičiavimas pagal srityje Laikas ir buvimas darbe apskaičiuotus užmokesčio tarifus

Toliau pateiktame pavyzdyje nurodoma, kaip apskaičiuojamos valandinės išlaidos, kai nustatyta, kad išlaidos būtų skaičiuojamos pagal užmokesčio tarifus.

Gamybos užsakymams ir projektams naudojamas valandinių išlaidų tarifas apskaičiuojamas vykdant gamybos procesą. Norėdami peržiūrėti veiklos valandinį tarifą, srityje Laikas ir buvimas darbe atidarykite puslapį **Patvirtinimas**, po to pasirinkite **Užklausa** &gt; **Perkeltos registracijos**. Registracijos valandinį išlaidų tarifą galite peržiūrėti skirtuke **Savikainos**.

Atkreipkite dėmesį į toliau nurodytas registracijas, naudojančias tą patį laiko šabloną, kuris nurodytas pirmiau pateiktame pavyzdyje.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      | Laikas |
|---------------------------|----------|----------|------|
| Atėjimas į darbą                  | 07:00 | 07:00 |      |
| Procesas (užsakymas: 4711)     | 07:00 | 11:00 | 4    |
| Procesas (užsakymas: 4712)     | 11:00 | 15:00 | 3,50 |
| Pertrauka (apmokama)              | 12:00 | 12:30 | 0,50 |
| Išėjimas iš darbo                 | 15:00 | 15:00 |      |

Perkėlus registracijas sugeneruojamos toliau nurodytos perkeltos registracijos.

| Registracijos tipas     | Laikas | Valandos savikaina |
|-----------------------|------|---------------------|
| Atėjimas į darbą              | 0,00 | 0,00                |
| Procesas (užsakymas: 4711) | 4,00 | 10,00               |
| Procesas (užsakymas: 4712) | 3,50 | 11,14               |
| Pertrauka (apmokama)          | 0,50 | 0,00                |
| Išėjimas iš darbo             | 0,00 | 0,00                |

Apmokamos pertraukos valandinė savikaina apskaičiuojama pagal nustatytas tiesiogines atlyginimo išlaidas. Pasirinkite **Laikas ir buvimas darbe** &gt; **Sąranka** &gt; **Laiko ir buvimo darbe parametrai**. Srities **Tiesioginės atlyginimo išlaidos** skirtuke **Savikaina**, lauke **Standartinis laikas** galite pasirinkti **Taip**, **Ne** arba **Paskirstymas**.

- **Taip** – ši vertė naudojama pirmiau pateiktame pavyzdyje. Išlaidos paskirstomos gamybos arba projekto veiklai, kuri vykdoma kartu su apmokamos pertraukos veikla. Pateiktame pavyzdyje ši veikla yra užsakymo 4712 gamybos užduotis. Kaip matote, apmokamos pertraukos valandinė savikaina yra 0 (nulis) ir ji paskirstoma kartu su pertrauka vykdomai užduočiai.

    Apmokamos pertraukos trukmė 0,5 valandos, o užmokesčio tarifas yra 8. Todėl bendros išlaidos už apmokamą pertrauką yra 4. Po to bendros išlaidos paskirstomos 3,5 val. proceso užduočiai. Todėl prie išlaidų pridedama 1,14 vertės valandinė savikaina už apmokamą pertrauką (4 ÷ 3,5 = 1,14).

- **Paskirstymas** – apmokama pertrauka tolygiai paskirstoma užregistruotoms dienos užduotims. Jei ši vertė naudojama ankstesniame pavyzdyje, generuojamos toliau nurodytos perkeliamos registracijos.

    | Registracijos tipas     | Laikas | Valandos savikaina |
    |-----------------------|------|---------------------|
    | Atėjimas į darbą              | 0,00 | 0,00                |
    | Procesas (užsakymas: 4711) | 4,00 | 10,53               |
    | Procesas (užsakymas: 4712) | 3,50 | 10,53               |
    | Pertrauka (apmokama)          | 0,50 | 0,00                |
    | Išėjimas iš darbo             | 0,00 | 0,00                |

    Bendra dviejų gamybos užduočių vykdymo trukmė 7,5 valandos, o bendrosios išlaidos už apmokamą pertrauką yra 4. Todėl išlaidos už pertrauką skaičiuojamos kaip 0,53 (= 4 ÷ 7,5).

- **Ne** – dėl išlaidų už apmokamą pertrauką valandinės išlaidos už proceso veiklas nepadidėja.

    | Registracijos tipas     | Laikas | Valandos savikaina |
    |-----------------------|------|---------------------|
    | Atėjimas į darbą              | 0,00 | 0,00                |
    | Procesas (užsakymas: 4711) | 4,00 | 10,00               |
    | Procesas (užsakymas: 4712) | 3,50 | 10,00               |
    | Pertrauka (apmokama)          | 0,50 | 0,00                |
    | Išėjimas iš darbo             | 0,00 | 0,00                |

## <a name="absence"></a>Neatvykimas

Registruojant darbuotojo neatvykimo laikotarpį naudojamas neatvykimo kodas. Kaip ir pertraukos bei perjungimo kodai, neatvykimo kodas yra netiesioginės veiklos tipas. Neatvykimo laikas gali būti suplanuotas arba užregistruotas ir neatvykimas gali būti leistinas arba neleistinas. Leistinas neatvykimas apima vizitą pas gydytoją, seminarą arba prisiekusiojo tarnybą. Neleistinas neatvykimas – tai neatvykimas dėl nepateisinamų priežasčių, pavyzdžiui, kai darbuotojas vėluoja į darbą. Paprastai dėl leistino neatvykimo nėra atskaitoma iš darbuotojo darbo užmokesčio, o dėl neleistino neatvykimo – atskaitoma.

### <a name="planned-absence"></a>Suplanuotas neatvykimas

Puslapyje **Suplanuoto neatvykimo kūrimas** (**Laikas ir buvimas darbe** &gt; **Suplanuoto neatvykimo kūrimas**) galite kurti darbuotojų suplanuotus neatvykimus. Šiame puslapyje suplanuotas neatvykimas registruojamas kaip nurodytą dieną ir nurodytu laiku atliekama neatvykimo užduotis.

Užduotis kuriama pagal užklausą. Todėl galite kurti kelių darbuotojų suplanuotą neatvykimą, pavyzdžiui, tai pačiai skaičiavimo grupei priklausančių darbuotojų neatvykimą. Jei suplanuotas neatvykimas sukurtas vienam darbuotojui, registraciją galima įvesti puslapyje **Buvimas darbe** arba **Laiko registracijos darbuotojai**.

- Norėdami neatvykimo registraciją įvesti puslapyje **Buvimas darbe**, pasirinkite **Laikas ir buvimas darbe** &gt; **Užklausos ir ataskaitos** &gt; **Buvimas darbe** &gt; **Buvimas darbe**, po to pasirinkite **Neatvykimo registracija**.
- Norėdami neatvykimo registraciją įvesti puslapyje *<strong><em>Laiko registracijos darbuotojai</em></strong>* pasirinkite <strong>Laikas ir buvimas darbe</strong> &gt; <strong>Sąranka</strong> &gt; <strong>Laiko registracijos darbuotojai</strong>, po to srities <strong>Laiko paskyrimas</strong> skirtuke <strong>Laikas</strong> pasirinkite <strong>Neatvykimo registracijos</strong>.

Naudodami ataskaitą **Suplanuoti neatvykimai** galite peržiūrėti suplanuotus darbuotojų neatvykimus. Norėdami atidaryti šią ataskaitą, pasirinkite **Laikas ir buvimas darbe** &gt; **Užklausos ir ataskaitos** &gt; **Neatvykimo ataskaitos** &gt; **Suplanuoti neatvykimai**.

### <a name="registered-absence"></a>Užregistruotas neatvykimas

Apskritai, laikoma, kad darbuotojai neatvyko į darbą, jei jų nėra darbe bet kuriuo metu nuo jų suplanuoto atėjimo į darbą iki suplanuoto išėjimo iš darbo laiko. Jei darbuotojai ateina į darbą vėliau nei suplanuota arba jei išeina iš darbo anksčiau nei suplanuota, jų paprašoma pasirinkti neatvykimo kodą ir nurodyti neatvykimo priežastį. Galima nustatyti tokį neatvykimo kodą, kad jis būtų taikomas registracijai. Sąraše galima pasirinkti tik taikomus kodus.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Įvairiomis darbo valandų registracijų kombinacijomis paremti scenarijai

Toliau pateikiamuose scenarijuose nurodomi darbuotojams pagal jų registracijas generuojami mokėjimo elementai ir patvirtinimo įrašai. Visi scenarijai paremti toliau nurodytu laiko šablonu.

| Šablono tipas  | Pradžios    | Pabaigoje      | Diena     |
|---------------|----------|----------|---------|
| Viršvalandžiai     | 00:00 | 06:00 | Pirmadienis  |
| Nukrypimas+         | 06:00 | 07:00 | Pirmadienis  |
| Atėjimas į darbą      | 07:00 | 07:00 | Pirmadienis  |
| Standartinis laikas | 07:00 | 14:30 | Pirmadienis  |
| Nukrypimas-         | 14:30 | 15:30 | Pirmadienis  |
| Išėjimas iš darbo     | 15:30 | 15:30 | Pirmadienis  |
| Viršvalandžiai     | 15:30 | 06:00 | Antradienis |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>1 scenarijus: darbuotojas ateina į darbą vėliau nei planuota

Darbuotojas ateina į darbą 08:30. Kadangi suplanuotas jo atėjimo į darbą laikas yra 07:00, jis vėluoja į darbą 1,50 valandos. Kadangi šis 1,50 val. laikas laikomas neatvykimo laiku, darbuotojo paprašoma pasirinkti neatvykimo kodą. Darbuotojas išeina iš darbo 15:30, o tai yra suplanuotas išėjimo iš darbo laikas. Apskaičiavus ir patvirtinus darbuotojo registracijas, neatvykimo registracija, kartu su darbuotojui atėjus į darbą pasirinktu neatvykimo kodu, rodoma nuo 07:00 iki 08:30.

Laiko šablone galite sukonfigūruoti registracijos tipą **Atėjimo į darbą laikas**, kad būtų toleruojamas vėlesnis darbuotojų atvykimas į darbą. Pavyzdžiui, nustačius leistiną nuokrypį į 5, darbuotojo prašoma įvesti neatvykimo kodą tik tada, jei jis ateina į darbą vėliau nei 07:05.

Tokiu atveju, kadangi darbuotojas negali nurodyti pateisinamos vėlavimo į darbą priežasties, jis turi pasirinkti nurodytą neleistino neatvykimo kodą. Neatvykimo kodas laikomas taikomu leistinam neatvykimui, jei įjungtas neatvykimo grupės, kuriai priklauso neatvykimo kodas, viršvalandžių atskaitymo nustatymas. Norėdami nustatyti nustatymą, pasirinkite **Laikas ir buvimas darbe** &gt; **Sąranka** &gt; **Grupės** &gt; **Neatvykimo grupės**, po to pažymėkite žymės langelį **Atskaityti viršvalandžius**.

Toliau nurodoma, kaip darbuotojo dienos registracijos rodomos puslapyje **Patvirtinimas** atlikus skaičiavimą.

| Žurnalo registracijos tipas         | Pradžios    | Pabaigoje      | Laikas |
|-----------------------------------|----------|----------|------|
| Neatvykimas (neleistinas – vėlavimas į darbą) | 07:00 | 08:30 | 1.5  |
| Atėjimas į darbą                          | 08:30 | 08:30 |      |
| Gamybos užduotis                    | 07:30 | 15:30 | 7.0  |
| Išėjimas iš darbo                         | 15:30 | 15:30 |      |

Toliau nurodomas perkėlus registracijas gautas mokėjimo elementas.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas |
|---------------|----------|-----------|------|
| Standartinis laikas | 1 201     | 7,00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>2 scenarijus: darbuotojas išeina iš darbo anksčiau negu suplanuotu standartinio laikotarpio išėjimo iš darbo laiku

Darbuotojas ateina į darbą 07:00, o išeina – 13:00. Kadangi laikas 13:00 yra ankstesnis negu suplanuotas išėjimo iš darbo laikas 15:30, o laikas 01:00 priskiriamas standartiniam laikotarpiui, darbuotojas paraginamas pasirinkti neatvykimo kodą. Darbuotojas pasirenka vizito pas gydytoją neatvykimo kodą, kuris laikomas leistinu neatvykimu. Užmokesčio už leistiną neatvykimą tarifas nurodomas registracijos tipo **Neatvykimas** mokėjimo sutartyse (**Laikas ir buvimas darbe** &gt; **Sąranka** &gt; **Algalapis** &gt; **Mokėjimo sutartys**).

Toliau nurodoma, kaip darbuotojo dienos registracijos rodomos puslapyje **Patvirtinimas** atlikus skaičiavimą.

| Žurnalo registracijos tipas              | Pradžios    | Pabaigoje      | Laikas |
|----------------------------------------|----------|----------|------|
| Atėjimas į darbą                               | 07:00 | 07:00 |      |
| Gamybos užduotis                         | 07:00 | 13:00 | 4,0  |
| Išėjimas iš darbo                              | 13:00 | 13:00 |      |
| Neatvykimas (leistinas – vizitas pas gydytoją) | 13:00 | 15:30 | 3.5  |

Toliau nurodomas perkėlus registracijas gautas mokėjimo elementas.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas |
|---------------|----------|-----------|------|
| Standartinis laikas | 1 201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>3 scenarijus: darbuotojas išsiregistruoja iki suplanuoto išėjimo iš darbo laiko nukrypimo laikotarpiu

Darbuotojas ateina į darbą 07:00, o išeina iš darbo 14:15, t. y. suplanuotu nukrypimo laikotarpiu. Laikas nuo faktinio išėjimo iš darbo iki suplanuoto išėjimo iš darbo nelaikomas neatvykimu ir darbuotojo neprašoma pasirinkti neatvykimo kodo. Suma atskaitoma iš darbuotojo nukrypimo sąskaitos ir darbuotojui apmokama už likusią nukrypimo laikotarpio dalį nuo 14:15 iki 15:30.

Toliau nurodoma, kaip darbuotojo dienos registracijos rodomos puslapyje **Patvirtinimas** atlikus skaičiavimą.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      | Laikas |
|---------------------------|----------|----------|------|
| Atėjimas į darbą                  | 07:00 | 07:00 |      |
| Gamybos užduotis            | 07:00 | 14:15 | 7,25 |
| Išėjimas iš darbo                 | 14:15 | 14:15 |      |

Toliau nurodomas perkėlus registracijas gautas mokėjimo elementas.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas |
|---------------|----------|-----------|------|
| Standartinis laikas | 1 201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>4 scenarijus: darbuotojas ateina į darbą pavėlavęs ir išeina iš darbo vėliau negu suplanuotu viršvalandžių laikotarpio išėjimo iš darbo laiku

Darbuotojas ateina į darbą pavėlavęs 09:30, o tada, kad kompensuotų savo pavėlavimą, jis dirba viršvalandžius ir išeina iš darbo 17:00. Kadangi darbuotojas atvyko pavėlavęs ir kompensavo pavėlavimą dirbdamas ilgiau, įmonė nenori mokėti darbuotojui už viršvalandžius, kuriuos jis dirbo nuo suplanuoto išėjimo iš darbo laiko 15:30 iki faktinio išėjimo iš darbo laiko 17:00, nors laiko šablone šis laikotarpis laikomas viršvalandžiais.

Norint naudoti šį scenarijų, galima nustatyti neatvykimo kodą ir sutrumpinti viršvalandžių laikotarpį tiek valandų, kiek darbuotojui tą dieną priskaičiuota neleistinų neatvykimo valandų. Norėdami, kad neleistino neatvykimo valandos būtų skaičiuojamos kaip viršvalandžiai, pasirinkite **Laikas ir buvimas darbe** &gt; **Sąranka** &gt; **Grupės** &gt; **Neatvykimo grupės** ir pažymėkite žymės langelį **Atskaityti viršvalandžius**.

Toliau nurodoma, kaip darbuotojo dienos registracijos rodomos puslapyje **Patvirtinimas** atlikus skaičiavimą.

| Žurnalo registracijos tipas         | Pradžios    | Pabaigoje      | Laikas |
|-----------------------------------|----------|----------|------|
| Neatvykimas (neleistinas – vėlavimas į darbą) | 07:00 | 09:30 | 1.5  |
| Atėjimas į darbą                          | 09:30 | 09:30 |      |
| Gamybos užduotis                    | 09:30 | 17:00 | 7,5  |
| Išėjimas iš darbo                         | 17:30 | 17:30 |      |

Pažymėjus pasirinkto neatvykimo kodo žymės langelį **Atskaityti viršvalandžius** neapmokama už tiek viršvalandžių, kiek valandų darbuotojas neleistinai neatvyko į darbą. Tokiu atveju perkėlus registracijas sugeneruojami toliau nurodyti mokėjimo elementai.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas |
|---------------|----------|-----------|------|
| Standartinis laikas | 1 201     | 9,00      | 10   |
| Viršvalandžiai      | 1301     | 0,5       | 15   |

Šiuo atveju iš 2,0 val. viršvalandžių nuo 15:30 iki 17:30 atimama 1,5 val. neleistino neatvykimo nuo 07:00 iki 09:30. Registracijos rezultatas yra 1,5 val. standartinio laiko ir 0,5 val. viršvalandžių.

Priešingu atveju, jei pasirinkto neatvykimo kodo žymės langelio **Atskaityti viršvalandžius** žymėjimas panaikintas, darbuotojui mokama už viršvalandžius, nors jis ir vėlavo bei neatvyko dėl neleistinos priežasties. Tokiu atveju perkėlus registracijas sugeneruojami toliau nurodyti mokėjimo elementai.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas |
|---------------|----------|-----------|------|
| Standartinis laikas | 1 201     | 7,50      | 10   |
| Viršvalandžiai      | 1301     | 2,0       | 15   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>5 scenarijus: darbuotojas išeina iš darbo anksčiau negu suplanuotu išėjimo iš darbo laiku ir neatvykimo laikotarpį gali paversti laikotarpiu Nukrypimas-

Toliau pateiktame pavyzdyje rodoma, kaip galima sumažinti darbuotojo nukrypimo sąskaitą neatvykimo laikotarpį paverčiant laikotarpiu Nukrypimas-.

Darbuotoja ateina į darbą 07:00, o išeina iš darbo 13:00. Darbuotojas turi sutartį, pagal kurią gali grįžti namo savaitgalį, jei atima šias valandas iš savo nukrypimo sąskaitos. Darbuotojui išeinant iš darbo 13:00, jis paraginamas pasirinkti neatvykimo kodą, nes šis likusios darbo dienos dalies neatvykimo laikotarpis nepriskiriamas suplanuotam Nukrypimo- laikotarpiui. Norėdamas likusią darbo dienos dalį paversti Nukrypimo laikotarpiu-, darbuotojas gali pasirinkti neatvykimo kodą, kuriuo naudojantis pasirenkamas nustatymas sumažinti jo nukrypimo sąskaitą.

Norėdami sumažinti darbo dieną neatvykimą užregistravusių darbuotojų kintamų valandų balansą, pasirinkite **Laikas ir buvimas darbe** &gt; **Sąranka** &gt; **Grupės** &gt; **Neatvykimo grupės** ir pažymėkite žymės langelį **Sumažinti nukrypimą**.

Toliau nurodoma, kaip darbuotojo dienos registracijos rodomos puslapyje **Patvirtinimas** prieš atliekant skaičiavimą.

| Žurnalo registracijos tipas | Pradžios    | Pabaigoje      | Laikas |
|---------------------------|----------|----------|------|
| Atėjimas į darbą                  | 07:00 | 07:00 |      |
| Gamybos užduotis            | 07:00 | 13:00 | 6,0  |
| Išėjimas iš darbo                 | 13:00 | 13:00 |      |

Toliau nurodoma, kaip atrodys gautas mokėjimo elementas perkėlus registraciją darbuotojui pasirinkus neleistino neatvykimo kodą.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas |
|---------------|----------|-----------|------|
| Standartinis laikas | 1 201     | 6,00      | 10   |

Toliau nurodoma, kaip atrodys gauti mokėjimo elementai perkėlus registracijas darbuotojui pasirinkus leistino neatvykimo kodą ir kai nustatyta, kad neatvykimo kodas sumažintų jo nukrypimo sąskaitą.

| Užmokesčio tipas     | Mokėjimo tipas | Mokėjimo vnt. | Tarifas |
|---------------|----------|-----------|------|
| Standartinis laikas | 1 201     | 8,50      | 10   |

Tokiu atveju darbuotojo nukrypimo balansas sumažinamas tiek valandų, kiek jų suskaičiuojama nuo faktinio išėjimo iš darbo laiko iki suplanuoto išėjimo iš darbo laiko (t. y. 2,5 val. nuo 13:00 iki 15:30).

> [!NOTE]
> Nerekomenduojame pažymėti abiejų žymės langelių **Atskaičiuoti nukrypimą** ir **Atskaičiuoti viršvalandžius**, nes naudojantis tokia sąranka iš darbuotojo viršvalandžių atskaitomos neleistinos valandos, tačiau taip pat sumažinama darbuotojo nukrypimo sąskaita.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>6 scenarijus: nėra suplanuotų dienos neatvykimų ir darbuotojo buvimo darbe laikotarpių

Darbuotojui darbo dieną neatvykus į darbą ir tą dieną nesant suplanuotų darbuotojo neatvykimų, skaičiuojant darbuotojo registracijas naudojamas numatytasis neatvykimo kodas. Norėdami nustatyti numatytuosius neatvykimo kodus, pasirinkite **Laikas ir buvimas darbe** &gt; **Laiko ir buvimo darbe parametrai**. Po to toliau nurodytuose laukuose galite pasirinkti neatvykimo kodą.

- Automatinis Nukrypimas- įvedimas
- Automatinis neatvykimo įvedimas

Skaičiuojant darbuotojo, turinčio galimybę naudotis kintamomis valandomis, kasdienes registracijas lauke **Automatinis Nukrypimas- įvedimas** nurodytas neatvykimo kodas naudojamas kaip numatytasis neatvykimo kodas. Jei darbuotojas negali pasinaudoti kintamomis valandomis, naudojamas lauke **Automatinis neatvykimo įvedimas** nurodytas neatvykimo kodas. Jei įmonėje yra ne tik kintamomis valandomis galinčių pasinaudoti darbuotojų, bet ir darbuotojų, kurie kintamomis valandomis pasinaudoti negali, privaloma nustatyti abu parametrus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]