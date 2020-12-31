---
title: „Regression Suite Automation Tool“ mokymo programos naudojimas
description: Šioje temoje parodoma, kaip naudoti „Regression Suite Automation Tool“ (RSAT). Joje aprašomos įvairios funkcijos ir pateikiami pavyzdžiai, kuriuose naudojami išplėstiniai scenarijai.
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 798717b276e68949a9425350720bf683a37d6fb5
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692995"
---
# <a name="regression-suite-automation-tool-tutorial"></a>„Regression Suite Automation Tool“ mokymas

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Naudodamiesi interneto naršyklės įrankiais atsisiųskite ir įrašykite šį puslapį PDF formatu. 

Šioje mokymo priemonėje paaiškinamos kai kurios išplėstinės „Regression Suite Automation Tool“ (RSAT) funkcijos, pateikiamas demonstracinis priskyrimas ir aprašoma strategija bei pagrindiniai mokymosi aspektai. 

## <a name="notable-features-of-rsat-and-task-recorder"></a>Įsidėmėtinos RSAT ir užduočių įrašymo priemonės funkcijos

### <a name="validate-a-field-value"></a>Patikrinti lauko reikšmę

RSAT leidžia įtraukti tikrinimo veiksmus jūsų testavimo atveju, kad galėtumėte tikrinti numatomas vertes. Daugiau informacijos apie šią funkciją žr. straipsnyje [Numatomų verčių tikrinimas](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).

Toliau pateiktame pavyzdyje parodyta, kaip galima naudoti šią funkciją norint patikrinti, ar turimos atsargos yra daugiau nei 0 (nulis).

1. Įmonės **USMF** demonstraciniuose duomenyse sukurkite užduoties įrašą, sudarytą iš toliau nurodytų veiksmų.

    1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
    2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauko **Prekės numeris** reikšme **1000**.
    3. Pasirinkite **Turimos atsargos**.
    4. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauko **Vieta** reikšme **1**.
    5. Sąraše pažymėkite pasirinktą eilutę.
    6. Patikrinkite, ar lauko **Iš viso turima** yra reikšmė yra **411,0000000000000000**.

2. Įrašykite užduoties įrašą ir pridėkite jį prie testavimo atvejo, esančio „Azure Devops”.
3. Įtraukite tikrinimo atvejį į tikrinimo planą ir įkelkite tikrinimo atvejį į RSAT.
4. Atidarykite „Excel“ parametrų failą. Skirtuke **InventOnhandItem** matysite skiltį **Tikrinti InventOnhandItem**, kurioje pateiktas laukas **Operatorius**.

    ![Laukas Operatorius](./media/use_rsa_tool_08.png)

5. Norėdami patikrinti, ar turimos atsargos visada bus didesnės nei 0, pakeiskite lauko **Vertė** reikšmę iš **411** į **0**, o lauko **Operatorius** reikšmę – iš lygybės ženklo (**=**) į ženklą „daugiau nei“ (**\>**).

    ![Pakeistos laukų Vertė ir Operatorius reikšmės](./media/use_rsa_tool_09.png)

6. Įrašykite ir uždarykite „Excel“ parametro failą.
7. Pasirinkite **Įkelti**, kad įrašytumėte keitimus, atliktus „Excel“ parametro faile, į „Azure DevOps“.

Dabar, jei nurodytos atsargų prekės reikšmė lauke **Iš viso turima** yra didesnė nei 0 (nulis), tikrinimai pavyks, nepriklausomai nuo faktinės turimų atsargų vertės.

### <a name="saved-variables-and-chaining-of-test-cases"></a>Įrašyti kintamieji ir testavimo atvejų sujungimas

Viena iš pagrindinių RSAT funkcijų – testavimo atvejų sujungimas, t. y. testavimo galimybė perkelti kintamuosius į kitus testus. Daugiau informacijos žr. straipsnyje [Kopijuoti kintamuosius į sujungtus testavimo atvejus](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).

### <a name="derived-test-case"></a>Išvesto testo atvejis

RSAT leidžia naudoti tą patį užduoties įrašą su keliais testavimo atvejais, o tai leidžia vykdyti užduotį naudojant skirtingas duomenų konfigūracijas. Daugiau informacijos žr. straipsnyje [Išvestiniai testavimo atvejai](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md).

### <a name="validate-notifications-and-messages"></a>Pranešimų tikrinimas

Šią funkciją galima naudoti norint patikrinti, ar įvyko veiksmas. Pavyzdžiui, kai sukuriamas, įvertinamas ir pradedamas gamybos užsakymas, programa rodo pranešimą „Gamyba – pradžia“, kad praneštų, jog pradėtas gamybos užsakymas.

![Pranešimas Gamyba – pradžia](./media/use_rsa_tool_05.png)

Šį pranešimą galite patikrinti naudodami RSAT – įveskite pranešimo tekstą atitinkamo įrašo „Excel“ parametro failo skirtuke **MessageValidation**.

![Skirtukas Pranešimo tikrinimas](./media/use_rsa_tool_06.png)

Paleidus tikrinimo atvejį, pranešimas „Excel“ parametro faile palyginamas su rodomu pranešimu. Jei pranešimai nesutampa, tikrinimo atvejis nepavyks.

> [!NOTE]
> „Excel“ parametro failo skirtuke **MessageValidation** galite įvesti daugiau nei vieną pranešimą. Pranešimai taip pat gali būti klaidos arba įspėjantys, o ne informaciniai pranešimai.

### <a name="snapshot"></a>Momentinė kopija

Ši funkcija užfiksuoja veiksmų, kurie buvo atlikti įrašant užduotį, ekrano kopijas. Ji naudinga audito arba programinių klaidų taisymo tikslais.

- Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Kai vykdote testavimo atvejį, RSAT sugeneruoja veiksmų momentines kopijas (vaizdus), esančias darbo kataloge, testavimo atvejų atkūrimo aplanke. Jei naudojate senesnę RSAT versiją, vaizdai įrašomi **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, kiekvienam vykdomam testavimo atvejui sukuriamas atskiras aplankas.

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

![Tikrinimo scenarijaus srautas](./media/use_rsa_tool_14.png)

Tolesnėje iliustracijoje rodoma šio scenarijaus verslo procesų hierarchija LCS verslo procesų modeliavimo įrankyje.

![Tikrinimo scenarijaus veiklos procesai](./media/use_rsa_tool_15.png)

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
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a>? 
Rodoma pagalba apie visas galimas komandas ir jų parametrus.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a>Neprivalomi parametrai

**``command``**


Kur ``[command]`` yra viena iš toliau nurodytų komandų.


#### <a name="about"></a>about
Rodoma dabartinė versija.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls
Išvalomas ekranas.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a>atsisiųsti
Į išvesties katalogą atsiunčiami nurodyto testavimo atvejo priedai. Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``. Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Būtini parametrai
**``test_case_id``** Nurodo testavimo atvejo ID.  
**``output_dir``** Nurodo išvesties katalogą. Katalogas privalo būti.

##### <a name="examples"></a>Pavyzdžiai

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a>redaguoti
Leidžia programoje „Excel“ atverti parametrų failą ir jį redaguoti.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a>Būtini parametrai
**``excel_file``** Turi būti nurodytas visas esamo „Excel“ failo kelias.

##### <a name="examples"></a>Pavyzdžiai
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a>generate
Išvesties kataloge sugeneruojami nurodyto testavimo atvejo testavimo vykdymo ir parametrų failai.
Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``. Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Būtini parametrai
**``test_case_id``** Nurodo testavimo atvejo ID.  
**``output_dir``** Nurodo išvesties katalogą. Katalogas privalo būti.

##### <a name="examples"></a>Pavyzdžiai
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a>generatederived
Sugeneruojamas naujas testavimo atvejis, išvestas iš pateikto testavimo atvejo. Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``. Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a>Būtini parametrai
**``parent_test_case_id``** Nurodo pirminio testavimo atvejo ID.  
**``test_plan_id``** Nurodo testavimo plano ID.  
**``test_suite_id``** Nurodo testavimo paketo ID.

##### <a name="examples"></a>Pavyzdžiai
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a>generatetestonly
Išvesties kataloge sugeneruojamas tik nurodyto testavimo atvejo testavimo vykdymo failas. Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``. Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a>Būtini parametrai
**``test_case_id``** Nurodo testavimo atvejo ID.  
**``output_dir``** Nurodo išvesties katalogą. Katalogas privalo būti.

##### <a name="examples"></a>Pavyzdžiai
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a>generatetestsuite
Išvesties kataloge sugeneruojami visi nurodyto paketo testavimo atvejai.
Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``. Kaip **test_suite_name** parametrą naudokite bet kokią vertę iš stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a>Būtini parametrai
**``test_suite_name``** Nurodo testavimo paketo pavadinimą.  
**``output_dir``** Nurodo išvesties katalogą. Katalogas privalo būti.

##### <a name="examples"></a>Pavyzdžiai
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a>help
Identiška elementui [?](#section) command


#### <a name="list"></a>sąrašas
Išvardijami visi galimi testavimo atvejai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a>listtestplans
Išvardijami visi galimi testavimo planai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a>listtestsuite
Išvardijami nurodyto testavimo paketo testavimo atvejai. Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``. Kaip **suite_name** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a>Būtini parametrai
**``suite_name``** Norimo paketo pavadinimas.

##### <a name="examples"></a>Pavyzdžiai
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a>listtestsuitenames
Išvardijami visi galimi testavimo paketai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a>playback
Atkuriamas testavimo atvejis naudojant „Excel“ failą.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a>Būtini parametrai
**``excel_file``** Visas kelias iki „Excel“ failo. Failas privalo būti. 

##### <a name="examples"></a>Pavyzdžiai
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a>playbackbyid
Vienu metu atkuriami keli testavimo atvejai.
Norėdami gauti visus galimus testavimo atvejus, galite naudoti komandą ``list``. Kaip **test_case_id** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a>Būtini parametrai
**``test_case_id1``** Esamo testavimo atvejo ID.  
**``test_case_id2``** Esamo testavimo atvejo ID.  
**``test_case_idN``** Esamo testavimo atvejo ID.  

##### <a name="examples"></a>Pavyzdžiai
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a>playbackmany
Naudojant „Excel“ failus vienu metu atkuriama daug testavimo atvejų.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a>Būtini parametrai
**``excel_file1``** Visas kelias iki „Excel“ failo. Failas privalo būti.  
**``excel_file2``** Visas kelias iki „Excel“ failo. Failas privalo būti.  
**``excel_fileN``** Visas kelias iki „Excel“ failo. Failas privalo būti.  

##### <a name="examples"></a>Pavyzdžiai
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a>playbacksuite
Atkuriami visi testavimo atvejai iš nurodyto testavimo paketo. Norėdami gauti visus galimus testavimo paketus, galite naudoti komandą ``listtestsuitenames``. Kaip **suite_name** parametrą naudokite bet kokią vertę iš pirmojo stulpelio.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a>Būtini parametrai
**``suite_name``** Norimo paketo pavadinimas.

##### <a name="examples"></a>Pavyzdžiai
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a>quit
Uždaroma programa.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a>upload
Nusiunčiami visi nurodyto testavimo paketo ar testavimo atvejų failai.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a>Būtini parametrai
**``suite_name``** Bus nusiųsti visi nurodyto testavimo paketo failai.
**``testcase_id``** Bus nusiųsti visi nurodyto (-ų) testavimo atvejo (-ų) failai.

##### <a name="examples"></a>Pavyzdžiai
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a>uploadrecording
Nusiunčiamas tik nurodytų testavimo atvejų įrašo failas.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a>Būtini parametrai
**``testcase_id``** Bus nusiųstas nurodytų testavimo atvejų įrašo failas.

##### <a name="examples"></a>Pavyzdžiai
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a>usage
Rodomi du būdai, kaip iškviesti šią programą: naudojant numatytąjį parametrų failą arba pateikiant parametrų failą.

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a>„Windows PowerShell“ pavyzdžiai

[!IMPORTANT] Toliau nurodyti pavyzdiniai scenarijai yra pateikiami iliustravimo tikslais ir nėra palaikomi „Microsoft”.

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

```xpp
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
