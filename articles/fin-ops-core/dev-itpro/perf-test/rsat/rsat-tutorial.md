---
title: „Regression Suite Automation Tool“ mokymas
description: Šioje temoje parodoma, kaip naudoti „Regression Suite Automation Tool“ (RSAT). Joje aprašomos įvairios funkcijos ir pateikiami pavyzdžiai, kuriuose naudojami išplėstiniai scenarijai.
author: FrankDahl
ms.date: 09/23/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: e2273aefb98880a1ae746ef7ec65b4f2262f3560
ms.sourcegitcommit: 49c97b0c94e916db5efca5672d85df70c3450755
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/29/2022
ms.locfileid: "8492926"
---
# <a name="regression-suite-automation-tool-tutorial"></a>„Regression Suite Automation Tool“ mokymas

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Naudodamiesi interneto naršyklės įrankiais atsisiųskite ir įrašykite šį puslapį PDF formatu.

Šioje mokymo priemonėje paaiškinamos kai kurios išplėstinės „Regression Suite Automation Tool“ (RSAT) funkcijos, pateikiamas demonstracinis priskyrimas ir aprašoma strategija bei pagrindiniai mokymosi aspektai.

## <a name="notable-features-of-rsat-and-task-recorder"></a>Įsidėmėtinos RSAT ir užduočių įrašymo priemonės funkcijos

### <a name="validate-a-field-value"></a>Patikrinti lauko reikšmę

RSAT leidžia įtraukti tikrinimo veiksmus jūsų testavimo atveju, kad galėtumėte tikrinti numatomas vertes. Daugiau informacijos apie šią funkciją žr. straipsnyje [Numatomų verčių tikrinimas](rsat-validate-expected.md).

Toliau pateiktame pavyzdyje parodyta, kaip galima naudoti šią funkciją norint patikrinti, ar turimos atsargos yra daugiau nei 0 (nulis).

1. Įmonės **USMF** demonstraciniuose duomenyse sukurkite užduoties įrašą, sudarytą iš toliau nurodytų veiksmų.

    1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
    2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauko **Prekės numeris** reikšme **1000**.
    3. Pasirinkite **Turimos atsargos**.
    4. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauko **Vieta** reikšme **1**.
    5. Sąraše pažymėkite pasirinktą eilutę.
    6. Patikrinkite, ar lauko **Iš viso turima** yra reikšmė yra **411,0000000000000000**.

2. Įrašykite užduoties įrašymą kaip **programuotojo įrašą** ir pridėkite jį prie testo atvejo Azure DevOps.
3. Įtraukite tikrinimo atvejį į tikrinimo planą ir įkelkite tikrinimo atvejį į RSAT.
4. Atidarykite „Excel” parametro failą ir eikite į **Testavimo atvejo veiksmai** skirtuką.
5. Norėdami patikrinti, ar turimų atsargų reikšmė visada bus daugiau nei **„0”**, eikite į veiksmą **Tikrinti iš viso turima** ir pakeiskite jo vertę iš **„411”** į **„0”**. Pakeiskite lauko **Operatorius** vertę iš lygybės ženklo (**„=**) į daugiau ženklą (**\>**).
6. Įrašykite ir uždarykite „Excel“ parametro failą.
7. Pasirinkite **Įkelti**, kad įrašytumėte keitimus, atliktus „Excel“ parametro faile, į „Azure DevOps“.

Dabar, jei nurodytos atsargų prekės reikšmė lauke **Iš viso turima** yra didesnė nei 0 (nulis), tikrinimai pavyks, nepriklausomai nuo faktinės turimų atsargų vertės.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Įrašyti kintamieji ir testavimo atvejų sujungimas

Viena iš pagrindinių RSAT funkcijų – testavimo atvejų sujungimas, t. y. testavimo galimybė perkelti kintamuosius į kitus testus. Daugiau informacijos žr. straipsnyje [Kopijuoti kintamuosius į sujungtus testavimo atvejus](rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Išvesto testo atvejis

RSAT leidžia naudoti tą patį užduoties įrašą su keliais testavimo atvejais, o tai leidžia vykdyti užduotį naudojant skirtingas duomenų konfigūracijas. Daugiau informacijos žr. straipsnyje [Išvestiniai testavimo atvejai](rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Pranešimų tikrinimas

Šią funkciją galima naudoti norint patikrinti, ar įvyko veiksmas. Pavyzdžiui, kai sukuriamas, įvertinamas ir pradedamas gamybos užsakymas, programa rodo pranešimą „Gamyba – pradžia“, kad praneštų, jog pradėtas gamybos užsakymas.

![Pranešimas Gamyba – pradžia.](./media/use_rsa_tool_05.png)

Šį pranešimą galite patikrinti naudodami RSAT – įveskite pranešimo tekstą atitinkamo įrašo „Excel“ parametro failo skirtuke **MessageValidation**.

![Skirtukas Pranešimo tikrinimas.](./media/use_rsa_tool_06.png)

Paleidus tikrinimo atvejį, pranešimas „Excel“ parametro faile palyginamas su rodomu pranešimu. Jei pranešimai nesutampa, tikrinimo atvejis nepavyks.

> [!NOTE]
> „Excel“ parametro failo skirtuke **MessageValidation** galite įvesti daugiau nei vieną pranešimą. Pranešimai taip pat gali būti klaidos arba įspėjantys, o ne informaciniai pranešimai.

### <a name="snapshot"></a>Momentinė kopija

Ši funkcija užfiksuoja veiksmų, kurie buvo atlikti įrašant užduotį, ekrano kopijas. Ji naudinga audito arba programinių klaidų taisymo tikslais.

- Norėdami naudoti šią funkciją atidarykite failą vykdant RSAT su vartotojo sąsaja, **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **teisingas** į **klaidingas**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

- Norėdami naudoti šią funkciją atidarykite failą vykdant RSAT su vartotojo sąsaja, (pavyzdžiui „Azure DevOps“), atverkite **Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe.config** failą RSAT diegimo kataloge (pavyzdžiui, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), ir pakeiskite tolesnio elemento vertę iš **klaidingas** į **teisingas**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Kai vykdote tikrinimo atvejus, RSAT sugeneruoja veiksmų momentines kopijas (vaizdus) ir įrašo juos į tikrinimo atvejų aplanką darbo kataloge. Antrinėje aplanke sukuriamas atskiras poaplankių pavadinimas **StepSnapshots**. Šiame aplanke yra paleisties bandymų atvejų momentinės kopijos.

## <a name="assignment"></a>Priskyrimas

### <a name="scenario"></a>Scenarijus

1. Produkto dizaino įrankis sukuria naują išleistą produktą.
2. Gamybos vadovas inicijuoja gamybos užsakymą, kad atsargų lygį pakeltų dviem vienetais.
3. Gamyba pradeda ir baigia gamybos užsakymą bei patikrina, ar turimas kiekis yra du vienetai.
4. Pardavimo komanda gauna keturių naujo produkto vienetų užsakymą. Todėl pardavimo komanda atnaujina grynuosius poreikius naudodami dinaminį planą. Kadangi papildomų pajėgumų nėra, numatytoji užsakymo strategija nustatyta kaip „pirkti, o ne gaminti“. Todėl sukuriamas suplanuotas pirkimo užsakymas.
5. Pirkėjas įtraukia tiekėją, sutvirtina suplanuotą pirkimo užsakymą, o tada patvirtina pirkimo užsakymą.
6. Kai įsigytos prekės pristatomos į parduotuvę, parduotuvės operatorius ieško susijusio pirkimo užsakymo ir gauna prekes. Kadangi užsakymas yra baigtas, prekes galima paimti ir supakuoti į pardavimo užsakymą.
7. „Finance“ registruoja pirkimo SF ir pardavimo SF.

Tolesnėje iliustracijoje vaizduojamas šio scenarijaus srautas.

![Tikrinimo scenarijaus srautas.](./media/use_rsa_tool_14.png)

Tolesnėje iliustracijoje rodoma šio scenarijaus verslo procesų hierarchija LCS verslo procesų modeliavimo įrankyje.

![Tikrinimo scenarijaus veiklos procesai.](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>Strategija – pagrindinis mokymasis

### <a name="data"></a>Duomenys

- Įsitikinkite, kad turite reprezentatyvius duomenis (gamybos / auksinės konfigūracijos duomenų kopiją ir migravo duomenų kopiją).
- Kai generuojate naujus duomenis naudodami užduočių įrašymo priemonę, sukurkite tikrinimo pavadinimus, kurie derės su esamais pavadinimais (pavyzdžiui, naudokite prefiksą **RSATxxx**).
- Naudokite „Azure“ tam tikro laiko atkūrimą, kad iš naujo paleistumėte tikrinimus ne 1 pakopos aplinkose.
- Nors galite naudoti „Excel“ funkcijas **ATSITIKTINIS** ir **DABAR**, kad sugeneruotumėte unikalų derinį, prireiks gana daug pastangų. Toliau pateikiamas pavyzdys.

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>Užduoties įrašymo priemonė

- Apibrėžkite scenarijus prieš pradėdami įrašyti. Gerai valdomas projektas turi iš anksto apibrėžtus tikrinimo scenarijus. Norėdami sukurti tikrinimo atvejį, pagalvokite, kiek nuspėjamas šių tikrinimo scenarijų rezultatas.
- Išskaidykite įrašus, jei jie atlikti skirtingais vaidmenimis arba jei laukimo laikas ar išorinis įvykis yra prieš kitą veiksmą.
- Venkite pasirinkti reikšmes sąrašuose. Vietoje to naudokite teksto formatus, pvz., **FIFO**, **AudioRM** ir **SiteWH**. Pasirinkus sąraše, įrašoma sąrašo reikšmės padėtis, o ne pati reikšmė. Jei prekės yra įtrauktos į tą sąrašą, reikšmės padėtis gali pasikeisti. Todėl jūsų įraše bus naudojamas kitoks parametras ir likusi scenarijaus dalis gali būti paveikta.
- Pagalvokite apie kelių vartotojų elgseną. Pavyzdžiui, nemanykite, kad jūsų naujai sukurtas pardavimo užsakymas visada bus parenkamas automatiškai. Vietoje to visada naudokite filtrą, kad rastumėte tinkamą užsakymą.
- Norėdami užduočių įrašymo priemonės funkciją Kopijuoti, kad įrašytumėte naujai sukurto produkto pavadinimą ir jį būtų galima naudoti grandininio tikrinimo atvejais.
- Norėdami nustatyti kontrolės punktus, kurie patikrina, ar veiksmai buvo vykdyti tinkamai, naudokite užduočių įrašymo priemonės funkciją Tikrinti.

### <a name="rsat"></a>RSAT

- Norėdami vykdyti tikrinimą kitoje įmonėje, galite pakeisti įmonę „Excel“ parametro failo skirtuke **Bendra**. Įsitikinkite, kad parametrai ir duomenys yra prieinami naujai pasirinktoje įmonėje.
- Galite pakeisti tikrinimo vartotoją „Excel“ parametro failo skirtuke **Bendra**. Nurodykite vartotojo, kuris vykdys tikrinimo atvejį, el. pašto ID. Tokiu būdu tikrinimo atvejį galima vykdyti naudojant nurodyto vartotojo saugos teises.
- Norėdami palaukti prieš pradėdami tikrinimą, galite nustatyti pauzę „Excel“ parametro failo skirtuke **Bendra**. Ši pauzė gali būti naudojama paketinėje užduotyje (pvz., jei darbo eiga turi būti vykdoma prieš atliekant kitus veiksmus).

## <a name="advanced-scripting"></a>Išplėstinis scenarijus

### <a name="cli"></a>CLI

RSAT galima iškviesti lange **Komandinė eilutė** arba **„PowerShell“**.

> [!NOTE]
> Patikrinkite, ar aplinkos kintamasis **TestRoot** nustatytas kaip RSAT diegimo kelias. (Programoje „Microsoft Windows“ atidarykite **valdymo skydą**, pasirinkite **Sistema ir sauga \> Sistema \> Išplėstiniai sistemos parametrai** ir pasirinkite **Aplinkos kintamieji**.)

1. Atidarykite langą **Komandinė eilutė** arba **„PowerShell“** kaip administratorius.
2. Nueikite į RSAT įdiegimo katalogą.

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. Išvardykite visas komandas.

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        downloadsuite
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitebyid
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        playbacksuitebyid
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>?

Išvardija visas konkrečios komandos komandas arba rodo žinyną kartu su galimais parametrais.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?: Pasirinktiniai parametrai

`command```[command]``: kur yra viena iš ankstesnio sąrašo komandų.

#### <a name="about"></a>apie

Rodo įdiegto RSAT versiją.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

Išvalomas ekranas.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>atsisiųsti

Nurodyto tikrinimo atvejo priedai (įrašymas, vykdymas ir parametrų failai) atsisiunčiami iš Azure DevOps išvesties katalogo. Naudodami komandą galite gauti ``list`` visus galimų vykdyti bandymų atvejus ir naudoti bet kokią pirmojo stulpelio vertę kaip **test_case_id** parametrą.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="download-optional-switches"></a>atsisiųsti: pasirinktiniai raktų

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, atsisiuntimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.

##### <a name="download-required-parameters"></a>atsisiuntimas: būtini parametrai

+ `test_case_id`: Nurodo testavimo atvejo ID.

##### <a name="download-optional-parameters"></a>atsisiųsti: nebūtini parametrai

+ `output_dir`: nurodo išvesties darbo katalogą. Katalogas privalo būti. Jei šis parametras nenurodytas, bus naudojamas parametrų darbo katalogas.

##### <a name="download-examples"></a>atsisiuntimas: pavyzdžiai

`download 123 c:\temp\rsat`

`download /retry=240 765`

#### <a name="downloadsuite"></a>atsisiuntimas

Iš išvesties katalogo atsisiunčia visų tikrinimo atvejų priedus (įrašymas, Azure DevOps vykdymas ir parametrų failai). Galite naudoti komandą norėdami ``listtestsuitenames`` gauti visus naudingus bandymus ir naudoti bet kokią vertę kaip **test_suite_name parametrą**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``downloadsuite``**``[/retry[=<seconds>]] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="downloadsuite-optional-switches"></a>Download atsisiųsti: pasirinktiniai raktų:

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, atsisiuntimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.
+ `/byid`: šis perjungimas nurodo, kad pageidaujamas bandymų komplektas Azure DevOps identifikuojamas pagal jo ID, o ne bandymų komplekto pavadinimą.

##### <a name="downloadsuite-required-parameters"></a>Download komplektas: būtini parametrai

+ `test_suite_name`: Nurodo testavimo paketo pavadinimą. Šis parametras reikalingas, jei nenurodytas perjungimas /byid **·**. Šis pavadinimas yra bandymų Azure DevOps komplekto pavadinimas.
+ `test_suite_id`: Nurodo testavimo paketo ID. Šis parametras reikalingas, jei nurodytas perjungimas / **byid**. Šis ID yra bandymų komplekto Azure DevOps ID.

##### <a name="downloadsuite-optional-parameters"></a>Download komplektas: nebūtini parametrai

+ `output_dir`: nurodo išvesties darbo katalogą. Katalogas privalo būti. Jei šis parametras nenurodytas, bus naudojamas parametrų darbo katalogas.

##### <a name="downloadsuite-examples"></a>Download komplektas: pavyzdžiai

`downloadsuite NameOfTheSuite c:\temp\rsat`

`downloadsuite /byid 123 c:\temp\rsat`

`downloadsuite /retry=240 /byid 765`

`downloadsuite /retry=240 /byid 765 c:\temp\rsat`

#### <a name="edit"></a>redaguoti

Leidžia programoje „Excel“ atverti parametrų failą ir jį redaguoti.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>redagavimas: būtini parametrai

+ `excel_file`: Turi būti nurodytas visas esamo „Excel“ failo kelias.

##### <a name="edit-examples"></a>redagavimas: pavyzdžiai

`edit c:\RSAT\123\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generavimas

Išvesties kataloge sugeneruojami nurodyto testavimo atvejo testavimo vykdymo ir parametrų failai. Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``. Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] [test_case_id] [output_dir]``

##### <a name="generate-optional-switches"></a>generuoti: pasirinktiniai raktų:

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, generavimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.
+ `/dllonly`: generuoti tik tikrinimo vykdymo failus. Iš naujo negeneruokite "Excel" parametrų failo.
+ `/keepcustomexcel`: atnaujinkite esamą parametrų failą. Taip pat iš naujo generuoti vykdymo failus.

##### <a name="generate-required-parameters"></a>generavimas: būtini parametrai

+ `test_case_id`: Nurodo testavimo atvejo ID.

##### <a name="generate-optional-parameters"></a>generuoti: nebūtini parametrai

+ `output_dir`: nurodo išvesties darbo katalogą. Katalogas privalo būti. Jei šis parametras nenurodytas, bus naudojamas parametrų darbo katalogas.

##### <a name="generate-examples"></a>generavimas: pavyzdžiai

`generate 123 c:\temp\rsat`

`generate /retry=240 765 c:\rsat\last`

`generate /retry=240 /dllonly 765`

`generate /retry=240 /keepcustomexcel 765`

#### <a name="generatederived"></a>generatederived

Generuojamas naujas išvestas tikrinimo atvejis (antrinis tikrinimo atvejis) pateiktame tikrinimo atvejui. Naujas bandymų atvejis taip pat įtraukiamas į nurodytą bandymų komplektą. Naudodami komandą galite gauti ``list`` visus galimų vykdyti bandymų atvejus ir naudoti bet kokią pirmojo stulpelio vertę kaip **test_case_id** parametrą.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[/retry[=<seconds>]] [parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-optional-switches"></a>sugeneruotas: pasirinktinis perjungiamas

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, generavimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.

##### <a name="generatederived-required-parameters"></a>sugeneruota: būtini parametrai

+ `parent_test_case_id`: Nurodo pirminio testavimo atvejo ID.
+ `test_plan_id`: Nurodo testavimo plano ID.
+ `test_suite_id`: Nurodo testavimo paketo ID.

##### <a name="generatederived-examples"></a>sugeneruota: pavyzdžiai

`generatederived 123 8901 678`

`generatederived /retry 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

Generuoja tik nurodyto tikrinimo atvejo tikrinimo vykdymo failus. Jis negeneruoja "Excel" parametrų failo. Failai generuojami nurodytame išvesties kataloge. Naudodami komandą galite gauti ``list`` visus galimų vykdyti bandymų atvejus ir naudoti bet kokią pirmojo stulpelio vertę kaip **test_case_id** parametrą.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[/retry[=<seconds>]] [test_case_id] [output_dir]``

##### <a name="generatetestonly-optional-switches"></a>generatetestonly: pasirinktinis perjungiamas

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, generavimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.

##### <a name="generatetestonly-required-parameters"></a>tik generavimo testavimas: būtini parametrai

+ `test_case_id`: Nurodo testavimo atvejo ID.

##### <a name="generatetestonly-optional-parameters"></a>generatetestonly: nebūtini parametrai

+ `output_dir`: nurodo išvesties darbo katalogą. Katalogas privalo būti. Jei šis parametras nenurodytas, bus naudojamas parametrų darbo katalogas.

##### <a name="generatetestonly-examples"></a>tik generavimo testavimas: pavyzdžiai

`generatetestonly 123 c:\temp\rsat`

`generatetestonly /retry=240 765`

#### <a name="generatetestsuite"></a>generatetestsuite

Generuoja visų tikrinimo atvejų tikrinimo automatizavimo failus nurodytame tikrinimo komplekte. Galite naudoti komandą norėdami ``listtestsuitenames`` gauti visus naudingus bandymus ir naudoti bet kokią vertę kaip **test_suite_name parametrą**.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[/retry[=<seconds>]] [/dllonly] [/keepcustomexcel] ([test_suite_name] | [/byid] [test_suite_id]) [output_dir]``

##### <a name="generatetestsuite-optional-switches"></a>Generatetest tarp: pasirinktiniai raktai

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, generavimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.
+ `/dllonly`: generuoti tik tikrinimo vykdymo failus. Iš naujo negeneruokite "Excel" parametrų failo.
+ `/keepcustomexcel`: atnaujinkite esamą parametrų failą. Taip pat iš naujo generuoti vykdymo failus.
+ `/byid`: šis perjungimas nurodo, kad pageidaujamas bandymų komplektas Azure DevOps identifikuojamas pagal jo ID, o ne bandymų komplekto pavadinimą.

##### <a name="generatetestsuite-required-parameters"></a>generavimo testo programų paketas: būtini parametrai

+ `test_suite_name`: Nurodo testavimo paketo pavadinimą. Šis parametras reikalingas, jei nenurodytas perjungimas /byid **·**. Šis pavadinimas yra bandymų Azure DevOps komplekto pavadinimas.
+ `test_suite_id`: Nurodo testavimo paketo ID. Šis parametras reikalingas, jei nurodytas perjungimas / **byid**. Šis ID yra bandymų komplekto Azure DevOps ID.

##### <a name="generatetestsuite-optional-parameters"></a>Generatetest tarp: nebūtini parametrai

+ `output_dir`: nurodo išvesties darbo katalogą. Katalogas privalo būti. Jei šis parametras nenurodytas, bus naudojamas parametrų darbo katalogas.

##### <a name="generatetestsuite-examples"></a>generavimo testavimo programų paketas: pavyzdžiai

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite /retry Purchase c:\rsat\last`

`generatetestsuite /dllonly /byid 121`

`generatetestsuite /keepcustomexcel /byid 121`

#### <a name="help"></a>pagalba

Identiška elementui [?](#section) komanda.

#### <a name="list"></a>sąrašas

Išvarditi visi galimi dabartinio tikrinimo plano bandymų atvejai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

Išvardijami visi galimi testavimo planai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

Išvardijami nurodyto testavimo paketo testavimo atvejai. Galite naudoti komandą, ``listtestsuitenames`` norėdami gauti visus naudingus testus ir naudoti bet kokią sąrašo vertę kaip **suite_name** parametrą.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[test_suite_name]``

##### <a name="listtestsuite-required-parameters"></a>sąrašo testavimo programų paketas: būtini parametrai

+ `test_suite_name`: norimo komplekto pavadinimas.

##### <a name="listtestsuite-examples"></a>sąrašo testavimo programų paketas: pavyzdžiai

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitebyid"></a>listtesttesttestbyid

Išvardijami nurodyto testavimo paketo testavimo atvejai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitebyid``**``[test_suite_id]``

##### <a name="listtestsuitebyid-required-parameters"></a>listtesttesttestbyid: būtini parametrai

+ `test_suite_id`: norimo komplekto ID.

##### <a name="listtestsuitebyid-examples"></a>listtesttesttestbyid: pavyzdžiai

`listtestsuitebyid 12345`

#### <a name="listtestsuitenames"></a>listtestsuitenames

Išvarditi visi galimi dabartinio tikrinimo plano testai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>atkūrimas

Grįžta į tikrinimo atvejį, susijusį su nurodytu "Excel" parametrų failu. Ši komanda naudoja esamus vietinio automatizavimo failus ir neišsiųstų failų iš Azure DevOps. Ši komanda nepalaikoma EKA "Commerce" tikrinimo atvejams.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file]``

##### <a name="playback-optional-switches"></a>:: pasirinktiniai raktų režimai

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, paleidimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.
+ `/comments[="comment"]`: pateikti pasirinktinę informacijos eilutę, kuri bus įtraukta į **suvestinės** komentarų lauką ir tikrinimo rezultatų puslapius, skirti tikrinimo Azure DevOps atvejui.

##### <a name="playback-required-parameters"></a>atkūrimas: būtini parametrai

+ `excel_parameter_file`: visas Excel parametrų failo maršrutas. Failas turi būti.

##### <a name="playback-examples"></a>atkūrimas: pavyzdžiai

`playback c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playback /retry e:\temp\test.xlsx`

`playback /retry=300 e:\temp\test.xlsx`

`playback /comments="Payroll solution 10.0.0" e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

Kurkite kelis tikrinimo atvejus vienu metu. Bandymo atvejai identifikuojami pagal jų ID. Ši komanda atsisiųs failus iš Azure DevOps. Galite naudoti komandą visiems ``list`` galimams tikrinimo atvejams **gauti ir bet kurias pirmojo stulpelio vertes naudoti kaip test_case_id** parametrą.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[/retry[=<seconds>]] [/comments[="comment"]] [test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-optional-switches"></a>"/ibyid:" pasirinktinis perjungiamas

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, paleidimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.
+ `/comments[="comment"]`: pateikti pasirinktinę informacijos eilutę, kuri bus įtraukta į **suvestinės** komentarų lauką ir tikrinimo rezultatų puslapius, skirti tikrinimo Azure DevOps atvejui.

##### <a name="playbackbyid-required-parameters"></a>atkūrimas pagal ID: būtini parametrai

+ `test_case_id1`: esamo tikrinimo atvejo ID.
+ `test_case_id2`: esamo tikrinimo atvejo ID.
+ `test_case_idN`: esamo tikrinimo atvejo ID.

##### <a name="playbackbyid-examples"></a>atkūrimas pagal ID: pavyzdžiai

`playbackbyid 878`

`playbackbyid 2345 667 135`

`playbackbyid /comments="Payroll solution 10.0.0" 2345 667 135`

`playbackbyid /retry /comments="Payroll solution 10.0.0" 2345 667 135`

#### <a name="playbackmany"></a>daugelio atkūrimas

Vienu metu atlieka daug bandymų atvejų atgal. Bandymo atvejai identifikuojami pagal Excel parametrų failus. Ši komanda naudoja esamus vietinio automatizavimo failus ir neišsiųstų failų iš Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[/retry[=<seconds>]] [/comments[="comment"]] [excel_parameter_file1] [excel_parameter_file2] ... [excel_parameter_fileN]``

##### <a name="playbackmany-optional-switches"></a>:- pasirinktinis perjungia

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, paleidimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.
+ `/comments[="comment"]`: pateikti pasirinktinę informacijos eilutę, kuri bus įtraukta į **suvestinės** komentarų lauką ir tikrinimo rezultatų puslapius, skirti tikrinimo Azure DevOps atvejui.

##### <a name="playbackmany-required-parameters"></a>daugelio atkūrimas: būtini parametrai

+ `excel_parameter_file1`: visas "Excel" parametrų failo maršrutas. Failas turi būti.
+ `excel_parameter_file2`: visas "Excel" parametrų failo maršrutas. Failas turi būti.
+ `excel_parameter_fileN`: visas "Excel" parametrų failo maršrutas. Failas turi būti.

##### <a name="playbackmany-examples"></a>daugelio atkūrimas: pavyzdžiai

`playbackmany c:\RSAT\2745\attachments\Create_Purchase_Order_2745_Base.xlsx`

`playbackmany e:\temp\test.xlsx f:\RSAT\sample1.xlsx c:\RSAT\sample2.xlsx`

`playbackmany /retry=180 /comments="Payroll solution 10.0.0" e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>atkūrimo programų paketas

Atlieka visų bandymų atvejus iš vieno ar daugiau nurodytų bandymų dar. Jei yra nurodytas /local switch, vietoje bus naudojami vietiniai priedai. Kitaip priedai bus atsisiųsti iš Azure DevOps. Galite naudoti komandą, ``listtestsuitenames`` norėdami gauti visus naudingus testus ir naudoti bet kokią pirmojo stulpelio vertę, kaip **suite_name** parametrą.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] ([test_suite_name1] .. [test_suite_nameN] | [/byid] [test_suite_id1] .. [test_suite_idN])``

##### <a name="playbacksuite-optional-switches"></a>Papildomais perjungikliais

+ `/updatedriver`: jei šis perjungimas nurodytas, interneto naršyklės webininkas bus atnaujintas pagal reikalingų veiksmų procesą.
+ `/local`: šis perjungimas nurodo, kad vietoj failų atsisiuntimo iš turi būti naudojami vietiniai priedai Azure DevOps.
+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, paleidimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.
+ `/comments[="comment"]`: pateikti pasirinktinę informacijos eilutę, kuri bus įtraukta į **suvestinės** komentarų lauką ir tikrinimo rezultatų puslapius, skirti tikrinimo Azure DevOps atvejui.
+ `/byid`: šis perjungimas nurodo, kad pageidaujamas bandymų komplektas Azure DevOps identifikuojamas pagal jo ID, o ne bandymų komplekto pavadinimą.

##### <a name="playbacksuite-required-parameters"></a>atkūrimo programų paketas: būtini parametrai

+ `test_suite_name1`: Nurodo testavimo paketo pavadinimą. Šis parametras reikalingas, jei nenurodytas perjungimas /byid **·**. Šis pavadinimas yra bandymų Azure DevOps komplekto pavadinimas.
+ `test_suite_nameN`: Nurodo testavimo paketo pavadinimą. Šis parametras reikalingas, jei nenurodytas perjungimas /byid **·**. Šis pavadinimas yra bandymų Azure DevOps komplekto pavadinimas.
+ `test_suite_id1`: Nurodo testavimo paketo ID. Šis parametras reikalingas, jei nurodytas perjungimas / **byid**. Šis ID yra bandymų komplekto Azure DevOps ID.
+ `test_suite_idN`: Nurodo testavimo paketo ID. Šis parametras reikalingas, jei nurodytas perjungimas / **byid**. Šis ID yra bandymų komplekto Azure DevOps ID.

##### <a name="playbacksuite-examples"></a>atkūrimo programų paketas: pavyzdžiai

`playbacksuite suiteName`

`playbacksuite suiteName suiteNameToo`

`playbacksuite /updatedriver /local /retry=180 /byid 151 156`

`playbacksuite /updatedriver /local /comments="Payroll solution 10.0.0" /byid 150`

#### <a name="playbacksuitebyid"></a>d.d.

Paleidžia visus bandymų atvejus nurodytame bandymų Azure DevOps komplekte.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuitebyid``**``[/updatedriver] [/local] [/retry[=<seconds>]] [/comments[="comment"]] [test_suite_id]``

##### <a name="playbacksuitebyid-optional-switches"></a>"twitter"byid: pasirinktinis perjungiamas

+ `/retry[=seconds]`: jei šis perjungimas yra nurodytas, o atvejo tikrinimo atvejus užblokuoja kiti RSAT egzemplioriai, paleidimo procesas palauks nurodyto sekundžių skaičiaus ir bandykite dar kartą. Numatytoji sekundžių \[vertė\] yra 120 sekundžių. Jei nėra šio perjungimo, procesas bus atšauktas iš karto, jei bus užblokuoti bandymo atvejai.
+ `/comments[="comment"]`: pateikti pasirinktinę informacijos eilutę, kuri bus įtraukta į **suvestinės** komentarų lauką ir tikrinimo rezultatų puslapius, skirti tikrinimo Azure DevOps atvejui.
+ `/byid`: šis perjungimas nurodo, kad pageidaujamas bandymų komplektas Azure DevOps identifikuojamas pagal jo ID, o ne bandymų komplekto pavadinimą.

##### <a name="playbacksuitebyid-required-parameters"></a>"twitter"byid: būtini parametrai

+ `test_suite_id`: nurodo bandymų komplekto ID, kuris yra Azure DevOps.

##### <a name="playbacksuitebyid-examples"></a>Irbąs subyid: pavyzdžiai

`playbacksuitebyid 2900`

`playbacksuitebyid /retry 2099`

`playbacksuitebyid /retry=200 2099`

`playbacksuitebyid /retry=200 /comments="some comment" 2099`

#### <a name="quit"></a>uždarymas

Uždaro programą. Ši komanda naudinga tik tada, kai programos veikia interaktyviu režimu.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

##### <a name="quit-examples"></a>išjunkite: pavyzdžiai

`quit`

#### <a name="upload"></a>nusiuntimas

Įkeliami priedų failai (įrašymas, vykdymas ir parametrų failai), kurie priklauso nurodytam tikrinimo komplektui arba bandymų atvejams Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``([test_suite_name] | [test_case_id1] .. [test_case_idN])``

##### <a name="upload-required-parameters"></a>nusiuntimas: būtini parametrai

+ `test_suite_name`: bus įkelti visi nurodytam bandymų komplektui priklausantys failai.
+ `test_case_id1`: nurodo pirmojo tikrinimo atvejo ID, kurį reikia įkelti. Šį parametrą naudokite tik tada, kai pateikiamas joks bandymų komplekto pavadinimas.
+ `test_case_idN`: pateikiamas paskutinio tikrinimo atvejo ID, kurį reikia įkelti. Šį parametrą naudokite tik tada, kai pateikiamas joks bandymų komplekto pavadinimas.

##### <a name="upload-examples"></a>nusiuntimas: pavyzdžiai

`upload sample_suite`

`upload 2900`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

Įkelia tik įrašymo failą, kuris priklauso vienam ar daugiau nurodytų tikrinimo atvejų Azure DevOps.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[test_case_id1] .. [test_case_idN]``

##### <a name="uploadrecording-required-parameters"></a>įrašo nusiuntimas: būtini parametrai

+ `test_case_id1`: nurodo pirmojo tikrinimo atvejo ID, skirtas įrašui, kuris turi būti įkeltas į Azure DevOps.
+ `test_case_idN`: pateikiamas paskutinio tikrinimo atvejo ID, skirtas įrašui, į kurį reikia įkelti Azure DevOps.

##### <a name="uploadrecording-examples"></a>įrašo nusiuntimas: pavyzdžiai

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>naudojimas

Rodomi trys šios programos naudojimo būdai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

Interaktyviai veikia programa:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``

Veikia programa, nurodant komandą:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp ``**``[command]``**

Veikia programa, pateikdami parametrų failą:

+ ``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``/settings [drive:\Path to\file.settings] [command]``**

### <a name="windows-powershell-examples"></a>„Windows PowerShell“ pavyzdžiai

#### <a name="run-a-test-case-in-a-loop"></a>Tikrinimo atvejo vykdymas cikle

Turite tikrinimo scenarijų, kuris sukuria naują klientą. Naudojant scenarijų šis tikrinimo atvejis gali būti vykdomas ciklu, nustatant toliau nurodytų duomenų atsitiktinumą prie kiekvieno pakartojimo vykdymą.

- Kliento ID
- Kliento pavadinimas
- Kliento adresas

Kliento ID formatas bus *ATCUS\<number\>*, kur \<number\> yra reikšmė nuo **000000001** iki **999999999**.

Tolesnis pavyzdys naudoja vieną parametrą, **pradžia**, kad apibrėžtų pirmą naudojamą skaičių. Jis naudoja antrą parametrą, **Nr.**, kad apibrėžtų klientų, kurie turi būti sukurti, skaičių. Kiekvieno pakartojimo metu „Excel“ parametro failo parametrai pakeičiami naudojant funkciją UpdateCustomer. Tada RSAT komandinė eilutė iškviečiama funkcijoje RunTestCase.

Atidarykite „Microsoft Windows PowerShell Integrated Scripting Environment“ (ISE) administratorius režimu ir įklijuokite toliau nurodytą kodą į langą, pavadintą **Untitled1.ps1.**

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>Vykdykite scenarijų, kuris priklauso nuo duomenų „Microsoft Dynamics 365“

Toliau pateiktame pavyzdyje naudojamas „Open Data Protocol“ („OData“) iškvietimas, kad būtų galima rasti pirkimo užsakymo būseną. Jei būsena nėra **išrašyta SF**, galite, pavyzdžiui, iškviesti RSAT tikrinimo atvejį, kuris užregistruos SF.

```powershell
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
