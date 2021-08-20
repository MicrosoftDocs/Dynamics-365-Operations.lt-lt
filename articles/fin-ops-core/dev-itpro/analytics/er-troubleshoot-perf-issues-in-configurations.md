---
title: ER konfigūracijų našumo trikčių šalinimas
description: Šioje temoje paaiškinama, kaip rasti ir išspręsti efektyvumo problemas elektroninių ataskaitų (ER) konfigūracijose.
author: NickSelin
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b5f5308f171b6cd4224debec897dbde133e6d8424673aabfab51e6b83b9014e2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744391"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>ER konfigūracijų našumo trikčių šalinimas

Šioje temoje paaiškinama, kaip rasti ir išspręsti efektyvumo problemas [Elektroninių ataskaitų](general-electronic-reporting.md) (ER) [konfigūravimus](general-electronic-reporting.md#Configuration).

Paprastai, našumo tyrimas susideda iš kelių veiksmų.

1. [Rinkti](#collecting-data) duomenis.
2. Analizuoti surinktus duomenis.
3. Atsižvelgdami į analizės rezultatus, norėdami atlikti pakeitimus naudokite ER konfigūracijas [arba nuspręskite](#making-changes) surinkti daugiau duomenų.

## <a name="troubleshooting"></a>Trikčių šalinimas

### <a name="analyze-execution-time"></a>Analizuoti vykdymo laiką

Vykdymo laikas gali priklausyti nuo neprognozuojamo faktoriaus, pvz., nuo kitų užduočių, kurios vykdomos toje pačioje aplinkoje, ir duomenų kaupimo talpykloje, kuri naudoja duomenis pirmą kartą. Todėl vykdymą ir matavimą turėtumėte kartoti kelis kartus.

Kartais efektyvumo problemų lemia ER formato konfigūracija, naudojama ataskaitoms. Todėl juos lemia X++ kodas, naudojamas atidaryti tą ER formato konfigūraciją.

1. Veiksmų centre [arba įvykių žurnale](#infolog-time) ar [peržiūrėkite](#event-log-time) ataskaitos vykdymo laiką.
2. Palyginkite ataskaitos vykdymo laiką su viso scenarijaus vykdymo laiku.
3. Jei ataskaitos vykdymo laikas yra daug trumpesnis už bendrą vykdymo laiką, atsižvelkite į duomenų, kuriuos apdoroja ataskaita, kiekį:

    - Jei ataskaita apdoroja nepildą duomenų kiekį, problema gali apimti konfigūracijos įkėlimo laiką.
    - Jei ataskaitoje apdorojama daug duomenų, išdavimas gali apimti išankstinį X++apdorojimą. Šiam [atvejui analizuoti naudokite](#analyze-trace-parser-trace) „Trace pacer“.

    Daugiau informacijos apie kitus atvejus rasite tolesniuose skyriuose.

4. Vykdykite keletą bandymų, kuriuose dalyvauja skirtingi duomenų kiekiai, kad nustatytumėte, kaip vykdymo laikas priklauso nuo duomenų kiekio.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Analizuoti „Trace parser“ sekimą

Parengti smulkų pavyzdį arba surinkti keletą sekimo duomenų atsitiktinėse ataskaitos generavimo dalyse.

Tada, [„trace parser“](#trace-parser) atlikite standartinę analizę "iš apačios į viršų" ir atsakykite į šiuos klausimus:

- Kokie yra pagrindiniai laiko suvartojimo metodai?
- Kokia viso laiko dalis naudojama šiais metodais?

Atsakyti į tuos pačius klausimus į užklausas.

Jei pamatysite, kad metodai su prefiksu „ER" pereis prie kito skyriaus.

Jei pamatysite, kad metodai arba užklausos kilę iš programų komplekto, apsvarstykite bendrąjį optimizavimą (pvz., sukurkite indeksus).

Analizuoti skambučių skaičių. Jei skaičius žymiai didesnis nei tikėtasi, galite kaupti talpykloje atitinkamus konfigūracijos mazgus.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Analizuoti duomenų bazės skambučius

Paruoškite pavyzdį, kuriame yra mažas duomenų kiekis, kad jūs galite rinkti [ER sekimą](#electronic-reporting-traces).

Tada atidarykite sekimą ER modelio susiejimo konstruktoriuje ir pažiūrėkite puslapio apačioje. Atsakyti į šiuos klausimus:

- Ar yra užklausų dubliavimo? Jei yra, apsvarstykite vieną iš šių pataisų:

    - [Kaupimą talpykloje](#use-caching) naudokite, jei manote, kad viename pirminiame įraše yra keli skambučiai.
    - [Naudokite talpykloje parametruotą apskaičiuotą lauką,](#cached-parameterized) jei manote, kad yra to paties įrašo, esančio skirtinguose įrašuose, skambučių.
    - [Naudokite **JOIN** duomenų šaltinį](#use-join-datasource), jei jums reikia skaityti perskaitytą įvairių duomenų bazės įrašų skaičių.

- Ar užklausų skaičius ir išrinktų įrašų skaičius atitinka bendrą duomenų kiekį? Pavyzdžiui, jei dokumente yra 10 eilučių, ar statistika rodo, kad ataskaitoje išskleista 10 eilučių ar 1000 eilučių? Jei turite daug išrinktų įrašų, apsvarstykite vieną iš šių pataisymų:

    - [Naudokite **FILTRO** funkciją, o ne **WHERE** funkciją](#filter) norėdami apdoroti duomenis SQL serverio pusėje.
    - Kaupdami talpykloje nenaudokite tų pačių duomenų.
    - [Naudokite surinktų duomenų](#collected-data) funkcijas, kad išvengtumėte tų pačių duomenų apibendrinimo duomenų.

### <a name="analyze-perfview-traces"></a>Analizuoti „PerfView“ sekimą

[„PerfView“](#perfview) yra įrankis patyrusiems programuotojams. Išsamesnės informacijos apie šiuos veiksmus žr. [„Wall Clock Time Investigation Basics“](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Surinkkite sekimą naudodami gijos laiką.
2. Įtraukite tik dėklus, kuriuose naudojamas **runUnattended** filtruoti tik gijas, kurios konfigūracijos vykdymas. (Įtraukti **runUnattended** pridėjimą prie **IncPats** įvesties langelio.)
3. Atmeskite visus, tinklo ir užblokuotą laiką.
4. Įkelti [„PerfView/ įkėlimo ER išrašus](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml)i.
5. Pasirinkite **ER** \> **Kitą išankstinį rinkinį**.
6. Peržiūrėkite vardus:

    - Tikriausiai matysite platformos kodą, kuris suvartoja daugiausia laiko.
    - Galite du kartus spustelėti (arba du kartus spustelėti) ir eiti aukštyn **per dvipusį**.

        Jei surandate klases, kuriose yra prefiksas „ERExpression", ir jei tai funkcijos, susijusios su formulėmis, galite pagal klasės pavadinimą paisyti funkcijos pavadinimo, o norėdami peržiūrėti atributus galite peržiūrėti ER repo.

### <a name="fixes"></a>Pataisymai

- Jei matote, kad didžiąją prekybos laiko sumą suvartoja užklausos, pabandykite sumažinti užklausų skaičių:

    - [Peržiūrėti besidubliuotų](#analyze-database-calls) užklausų ER sekimą.
    - Pažiūrėkite, kiek įrašų yra rasta, ir įvertinkite, kiek duomenų teoriškai reikia rasti.

- Jei matote, kad didžiąją laiko dalis YRA suvartojama pagal naudojamas funkcijas, pabandykite rasti vietą konfigūracijoje, naudojančioje daugiausia išteklių.
- Jei matote, kad didžiąją laiko dalis YRA suvartojama pagal duomenų rinkimo funkcijas, apsvarstykite galimybę pakeisti jas *SQL grupe* modelio susiejimo pusėje.

### <a name="collecting-data"></a><a name="collecting-data"></a>Rinkti duomenis

Atsižvelgiant į aplinką, galimas duomenis galima rinkti keliais būdais:

- Gauti visą darbo laiką:

    - Iš veiksmų centro
    - Iš įvykių žurnalo

- Vykdyti šabloną:

    - Naudojant ER įrankius
    - Naudojant „Trace Parser“
    - Naudojant „PerfView“

#### <a name="collecting-data-in-a-production-environment"></a>Duomenų rinkimas gamybos aplinkoje

Kartais problemos gali būti atkuriamos tik gamybos aplinkoje. Duomenis galima rinkti šiais būdais:

- Naudojant [„Trace parser“](../perf-test/trace-trace-tutorial.md) sekimą
- Naudojant [ER vykdymo](trace-execution-er-troubleshoot-perf.md) sekimą
- Naudojant visą vykdymo laiką

#### <a name="collecting-data-in-a-development-environment"></a>Renkant duomenis vystymo aplinkoje

Be įrankių, kuriuos galima naudoti gamybos aplinkoje, dar yra keletas įrankių, kuriuos galima naudoti programavimo aplinkoje:

- Įvykių žurnalas („Microsoft-Dynamics-ElectronicReporting“). Šis žurnalas gali suteikti jums visą vykdymo laiką.
- Į bendruosius .NET įrankius, pvz., „PerfView“.

Be to, programavimo aplinka suteikia jums daugiau lankstumo prie mokymosi. Pavyzdžiui, norėdami pamatyti, kaip veikia vykdymo laikas, galima išjungti ataskaitų dalis.

### <a name="tools"></a><a name="tools"></a>Įrankiai

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Vykdymo laikas veiksmų centre

ER gali rodyti konfigūracijos vykdymo laiką veiksmų centre. Ši pasirinktis veikia tik konkrečiam vartotojui ir konkrečiai įmonei bei tik interaktyviems seansams. Norėdami, kad ši funkcija būtų pasiekiama, atlikite šiuos veiksmus.

1. Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Dialogo lange **Vartotojo parametrai** nustatykite **Rodyti failo sukūrimo laiko** parinktį į **Taip**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Vykdymo laikas įvykių žurnale

1. Atidarykite „Windows Event Viewer“.
2. Dalyje **Programų ir paslaugų žurnalai** atidarykite **Microsoft-Dynamics-ElectronicReporting/Operational**.
3. Ieškoti **„FormatMapingRun“** vykių, kuriuose **EventID=2**, nes šiuose įvykiams yra informacijos apie praleistą laiką.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Sekti „Trace parser“ sekimą 

Kadangi ER yra įdiegtas X++, našumui analizuoti galite naudoti bendrus X++ įrankius. Norėdami gauti daugiau informacijos, [žr. Sekti naudojant „Trace parser"](../perf-test/trace-trace-tutorial.md).

Yra keletas šio požiūrio apribojimų. Kadangi ER dalis įdiegta C#, bus pateikta ne visa informacija. Tačiau galite peržiūrėti išsamią duomenų naudojimo informaciją. Be to, ilgos ataskaitos trukmes galima viršyti sekimo saugojimo apribojimus.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER sekimas

ER gali rinkti savo sekimo duomenis ir turi šių sekimą vizualizavimo ir analizės įrankių. Daugiau informacijos, žr. [ER formatų vykdymo sekimas, siekiant pašalinti našumo problemas](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>„PerfView“

Kadangi X++ ir ER yra įdiegtas .NET platformoje, galite naudoti bendrus .NET įrankius. Pavyzdžiui, galite naudoti nemokamą [„PerfView“](https://github.com/Microsoft/perfview) įrankį.

Taip pat galite rinkti duomenis iš komandų eilutės. Pvz., toliau pateiktas „Windows PowerShell" scenarijus renka vykdymo laiką, kol kompiuteryje sustabdomas bet kokio formato vykdymas.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Yra keletas šio požiūrio apribojimų. Turite administruoti prieigą prie mašinos. Be to, turite būti patyrusio programuotojo, nes yra stačios mokymosi kreivės.

### <a name="making-changes"></a><a name="making-changes"></a>Keitimų atlikimas

#### <a name="use-caching"></a><a name="use-caching"></a>Naudoti kaupimą talpykloje

Nors kaupimas talpykloje sumažina laiko, kuris reikalingas duomenims vėl surasti, kiekį, jis kainuoja atminties. Kaupimą talpykloje naudokite atvejus, kai išrinktų duomenų kiekis nėra labai didelis. Daugiau informacijos ir pavyzdį, kuriame parodyta, kaip naudoti kaupimą talpykloje, žr. Patobulinkite modelio susiejimą, [remiantis vykdymo sekimo informacija](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Naudoti talpykloje parametruotą apskaičiuotą lauką

Kartais vertės turi būti peržvalgos pakartotinai. Pavyzdžiai gali būti sąskaitų pavadinimai ir sąskaitų numeriai. Norėdami sutaupyti laiko, galite sukurti apskaičiuotą lauką, kuriame yra aukščiausio lygio parametrų, tada į talpyklą įtraukite lauką.

Šį būdą rekomenduojame naudoti tik tada, kai talpykloje saugomų duomenų dydis yra mažas. Daugiau informacijos rasite patobulinkite [ER sprendimų našumą pridėdami parametrų APSKAIČIUOTO LAUKO duomenų šaltinius](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>Naudoti JOIN duomenų šaltinį

**JOIN** duomenų šaltinis leidžia vienoje užklausoje rasti kelis prijungtus įrašus. Norint surasti kiekvieną prijungtą įrašą, nereikia naudoti atskiros užklausos. Pavyzdžiui, jei turite 1000 eilučių, o kiekvienos eilutės prekės duomenis surasti pagal ryšį, turėsite 1001 užklausas (= 1000 + 1). Jei naudojate **JOIN** duomenų šaltinį, norėdami surasti tuos pačius duomenis naudosite tik vieną užklausą. Dėl daugiau informacijos, žr. [Naudoti JOIN duomenų šaltinius ER modelio žemėlapyje siekiant gauti kelias programos lenteles](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Užuot naudojus funkciją WHERE, naudoti funkciją FILTER

Funkcija **[FILTER](er-functions-list-filter.md)** vykdoma SQL serveryje, o **WHERE** iš sąrašo išrenka visus duomenis, po vieną įrašą ir kiekvienam įrašui taiko sąlygą. Pavyzdžiui, norite pasirinkti vieną įrašą iš 1000 įrašų. Jei naudojate **WHERE**, bus išrinkta visa 1000 įrašų. Tačiau jei naudosite **FILTER**, bus rastas tik vienas įrašas. **FILTER** taip pat gali naudoti indeksus duomenų bazės pusėje.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Surinktų duomenų funkcijų arba sukauptų duomenų šaltinio naudojimas

Jei jūsų konfigūracijoje yra *grupė pagal* komponentą, kuris apibendrina anksčiau rastos ataskaitos duomenis, komponentas vėl surasti visus duomenis. Naudodamiesi surinktų duomenų funkcijomis, įgalinate ER sukaupti duomenis pirmojo rinkimo metu. Norėdami gauti daugiau informacijos, žr. [ER konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Perrašyti konfigūracijos dalis, esantis X++

ER palaiko lentelių ir klasių, įskaitant plėtinius, iškviešiimą. Apsvarstykite galimybę perrašyti modelio susiejimo dalis X++, kad būtų pagerintas našumas.

ER gali naudoti duomenis iš šių šaltinių:

- Klasės (**objekto** ir **klasės** duomenų šaltiniai)
- Lentelės (**lentelė** ir **lentelės įrašo** duomenų šaltiniai)

[ER API](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) taip pat suteikia būdą iš anksto apskaičiuotims duomenims iš iškvietimo kodo siųsti. Programos komplekte yra keletas šio požiūrio pavyzdžių.
