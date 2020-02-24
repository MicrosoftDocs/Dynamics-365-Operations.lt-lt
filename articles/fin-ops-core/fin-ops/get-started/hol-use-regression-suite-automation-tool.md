---
title: „Regression Suite Automation Tool“ mokymo programos naudojimas
description: Šioje temoje parodoma, kaip naudoti „Regression Suite Automation Tool“ (RSAT). Joje aprašomos įvairios funkcijos ir pateikiami pavyzdžiai, kuriuose naudojami išplėstiniai scenarijai.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 026d1d743b5150f152ef70aa642dcf6841a4e398
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025809"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>„Regression Suite Automation Tool“ mokymo programos naudojimas

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Naudodamiesi interneto naršyklės įrankiais atsisiųskite ir įrašykite šį puslapį PDF formatu. 

Šioje mokymo priemonėje paaiškinamos kai kurios išplėstinės „Regression Suite Automation Tool“ (RSAT) funkcijos, pateikiamas demonstracinis priskyrimas ir aprašoma strategija bei pagrindiniai mokymosi aspektai.

## <a name="features-of-rsattask-recorder"></a>RSAT / užduočių įrašymo priemonės funkcijos

### <a name="validate-a-field-value"></a>Patikrinti lauko reikšmę

Norėdami gauti informacijos apie šią funkciją, žr. [Naujo užduoties įrašo, turinčio tikrinimo funkciją, kūrimas](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).

### <a name="saved-variable"></a>Įrašytas kintamasis

Norėdami gauti informacijos apie šią funkciją, žr. [Esamo užduoties įrašo modifikavimas norint sukurti įrašytą kintamąjį](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).

### <a name="derived-test-case"></a>Išvesto testo atvejis

1. Atidarykite „Regression suite automation tool“ (RSAT) ir pasirinkite abu tikrinimo atvejus, kuriuos sukūrėte [„Regression suite automation tool“ mokymo priemonės nustatymas ir diegimas](./hol-set-up-regression-suite-automation-tool.md).
2. Pasirinkite **Naujas \> Kurti išvestinį tikrinimo atvejį**.

    ![Komanda Kurti išvestinį tikrinimo atvejį meniu Naujas](./media/use_rsa_tool_01.png)

3. Gaunate pranešimą, kuriame teigiama, kad kiekvienam pasirinktam tikrinimui skirtas tikrinimo atvejis bus sukurtas pagal dabartinį tikrinimo komplektą ir kad kiekvienas išvestinis tikrinimo atvejis turės savo „Excel“ parametro failo kopiją. Pasirinkite **Gerai**.

    > [!NOTE]
    > Paleidus išvestinį tikrinimo atvejį, jis naudoja jo pirminio tikrinimo atvejo ir savo „Excel“ parametro failo kopijos užduoties įrašą. Tokiu būdu galite atlikti tą patį tikrinimą su skirtingais parametrais, neprivalėdami tvarkyti daugiau nei vieną užduoties įrašą. Išvestinis tikrinimo atvejis nebūtinai turi priklausyti tam pačiam tikrinimų paketui kaip jo pirminis tikrinimo atvejis.

    ![Pranešimo laukas](./media/use_rsa_tool_02.png)

    Sukuriami du papildomi išvestiniai tikrinimo atvejai ir pažymimas jų žymės langelis **Išvestinis?**.

    ![Sukuriami išvestiniai tikrinimo atvejai](./media/use_rsa_tool_03.png)

    Išvestinis tikrinimo atvejis sukuriamas automatiškai „Azure DevOps“. Tai antrinis tikrinimo atvejo **Kurti naują produktą** elementas ir jis pažymėtas specialiu raktažodžiu: **RSAT:DerivedTestSteps**. Šie tikrinimo atvejai taip pat automatiškai įtraukiami į tikrinimo planą „Azure DevOps“.

    ![Raktažodis RSAT:DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > Jei dėl kokių nors priežasčių išvestiniai tikrinimo atvejai nėra pateikiami tinkama tvarka, atidarykite „Azure DevOps“ ir pertvarkykite tikrinimo atvejus tikrinimo komplekte, kad RSAT galėtų paleisti juos tinkama tvarka.

4. Pasirinkite išvestinius tikrinimo atvejus ir pasirinkite **Redaguoti**, kad atidarytumėte atitinkamus „Excel“ parametrų failus.
5. Redaguokite šiuos „Excel“ parametrų failus tokiu pat būdu, kaip redagavote pirminį failą. Kitaip tariant, įsitikinkite, kad produkto ID nustatytas taip, jog jis būtų automatiškai sugeneruotas. Taip pat įsitikinkite, kad įrašytas kintamasis nukopijuojamas į atitinkamus laukus.
6. Abiejų „Excel“ parametrų failų skirtukuose **Bendra** atnaujinkite lauko **Įmonė** reikšmę į **USSI**, kad išvestiniai tikrinimo atvejai būtų vykdomi kitame juridiniame subjekte nei pirminis tikrinimo atvejis. Norėdami vykdyti tikrinimo atvejus pagal konkretų vartotoją (arba vaidmenį, kuris susietas su konkrečiu vartotoju), galite atnaujinti lauko **Tikrinimo vartotojas** reikšmę.
7. Pasirinkite **Vykdyti** ir įsitikinkite, kad produktas sukurtas ir juridiniame subjekte USMF ir juridiniame subjekte USSI.

### <a name="validate-notifications"></a>Tikrinti pranešimus

Šią funkciją galima naudoti norint patikrinti, ar įvyko veiksmas. Pavyzdžiui, kai sukuriamas, įvertinamas ir pradedamas gamybos užsakymas, programa rodo pranešimą „Gamyba – pradžia“, kad praneštų, jog pradėtas gamybos užsakymas.

![Pranešimas Gamyba – pradžia](./media/use_rsa_tool_05.png)

Šį pranešimą galite patikrinti naudodami RSAT – įveskite pranešimo tekstą atitinkamo įrašo „Excel“ parametro failo skirtuke **MessageValidation**.

![Skirtukas Pranešimo tikrinimas](./media/use_rsa_tool_06.png)

Paleidus tikrinimo atvejį, pranešimas „Excel“ parametro faile palyginamas su rodomu pranešimu. Jei pranešimai nesutampa, tikrinimo atvejis nepavyks.

> [!NOTE]
> „Excel“ parametro failo skirtuke **MessageValidation** galite įvesti daugiau nei vieną pranešimą. Pranešimai taip pat gali būti klaidos arba įspėjantys, o ne informaciniai pranešimai.

### <a name="validate-values-by-using-operators"></a>Tikrinti reikšmes naudojant operatorius

Ankstesnėse RSAT versijose galėjote tikrinti vertes tik jei kontrolinė reikšmė sutapo su numatoma reikšme. Nauja funkcija suteikia galimybę patikrinti, ar kintamasis nėra lygus, yra mažesnis arba yra didesnis už nurodytą reikšmę.

- Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    „Excel“ parametro faile atsiranda naujas laukas **Operatorius**.

    > [!NOTE]
    > Jei naudojate senesnę RSAT versiją, turite sugeneruoti naujus „Excel“ parametrų failus.

    ![Laukas Operatorius](./media/use_rsa_tool_07.png)

Toliau pateiktame pavyzdyje parodyta, kaip galima naudoti šią funkciją norint patikrinti, ar turimos atsargos yra daugiau nei 0 (nulis).

1. Įmonės **USMF** demonstraciniuose duomenyse sukurkite užduoties įrašą, sudarytą iš toliau nurodytų veiksmų.

    1. Eikite į **Produkto informacijos valdymas \> Produktai \> Patvirtinti produktai**.
    2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauko **Prekės numeris** reikšme **1000**.
    3. Pasirinkite **Turimos atsargos**.
    4. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauko **Vieta** reikšme **1**.
    5. Sąraše pažymėkite pasirinktą eilutę.
    6. Patikrinkite, ar lauko **Iš viso turima** yra reikšmė yra **411,0000000000000000**.

2. Įrašykite užduoties įrašą į BPM biblioteką, esančią LCS, ir sinchronizuokite jį į „Azure DevOps“.
3. Įtraukite tikrinimo atvejį į tikrinimo planą ir įkelkite tikrinimo atvejį į RSAT.
4. Atidarykite „Excel“ parametrų failą. Skirtuke **InventOnhandItem** matysite skiltį **Tikrinti InventOnhandItem**, kurioje pateiktas laukas **Operatorius**.

    ![Laukas Operatorius](./media/use_rsa_tool_08.png)

5. Norėdami patikrinti, ar turimos atsargos visada bus didesnės nei 0, pakeiskite lauko **Vertė** reikšmę iš **411** į **0**, o lauko **Operatorius** reikšmę – iš lygybės ženklo (**=**) į ženklą „daugiau nei“ (**\>**).

    ![Pakeistos laukų Vertė ir Operatorius reikšmės](./media/use_rsa_tool_09.png)

6. Įrašykite ir uždarykite „Excel“ parametro failą.
7. Pasirinkite **Įkelti**, kad įrašytumėte keitimus, atliktus „Excel“ parametro faile, į „Azure DevOps“.

Dabar, jei nurodytos atsargų prekės reikšmė lauke **Iš viso turima** yra didesnė nei 0 (nulis), tikrinimai pavyks, nepriklausomai nuo faktinės turimų atsargų vertės.

### <a name="generator-logs"></a>Generatoriaus žurnalai

Ši funkcija sukuria aplanką, kuriame yra paleistų tikrinimo atvejų žurnalai.

- Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.

    ```xml
    <add key="LogGeneration" value="false" />
    ```

Paleidus tikrinimo atvejus, žurnalų failus galima rasti čia: **C:\\Vartotojai\\\<Vartotojo vardas\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.

![Aplankas GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> Jei prieš pakeičiant vertę, esančią .config faile, buvo tikrinimo atvejų, tų tikrinimo atvejų žurnalai nebus generuojami, kol nesugeneruosite naujų tikrinimo vykdymo failų.
> 
> ![Komanda Generuoti tik tikrinimo vykdymo failus meniu Naujas](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>Momentinė kopija

Ši funkcija užfiksuoja veiksmų, kurie buvo atlikti įrašant užduotį, ekrano kopijas.

- Norėdami naudoti šią funkciją atidarykite failą **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** RSAT diegimo aplanke (pvz., **C:\\Program Files (x86)\\Regression Suite Automation Tool**) ir pakeiskite toliau nurodyto elemento reikšmę iš **false** į **true**.

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

Dalyje **C:\\Vartotojai\\\<Vartotojo vardas\>\\AppData\\Roaming\\regressionTool\\atkūrimas** sukuriamas atskiras aplankas, skirtas kiekvienam paleistam atvejui.

![Tikrinimo atvejo momentinės kopijos aplankas](./media/use_rsa_tool_12.png)

Kiekviename iš šių aplankų galite rasti veiksmų, kurie buvo atlikti, kai buvo paleisti tikrinimo atvejai, momentines kopijas.

![Momentinės kopijos failai](./media/use_rsa_tool_13.png)

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

Tolesnėje iliustracijoje vaizduojami šio scenarijaus veiklos procesai RSAT.

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

### <a name="command-line"></a>Komandinė eilutė

RSAT galima iškviesti lange **Komandinė eilutė**.

> [!NOTE]
> Patikrinkite, ar aplinkos kintamasis **TestRoot** nustatytas kaip RSAT diegimo kelias. (Programoje „Microsoft Windows“ atidarykite **valdymo skydą**, pasirinkite **Sistema ir sauga \> Sistema \> Išplėstiniai sistemos parametrai** ir pasirinkite **Aplinkos kintamieji**.)

1. Atidarykite langą **Komandinė eilutė** kaip administratorius.
2. Paleiskite įrankį iš diegimo katalogo.

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
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a>„Windows PowerShell“ pavyzdžiai

#### <a name="run-a-test-case-in-a-loop"></a>Tikrinimo atvejo vykdymas cikle

Turite tikrinimo scenarijų, kuris sukuria naują klientą. Naudojant scenarijų šis tikrinimo atvejis gali būti vykdomas ciklu, nustatant toliau nurodytų duomenų atsitiktinumą prie kiekvieno pakartojimo vykdymą.

- Kliento ID
- Kliento pavadinimas
- Kliento adresas

Kliento ID bus formato *ATCUS\<skaičius\>*, kai \<skaičius\> yra reikšmė tarp **000000001** ir **999999999**.

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
$excelFilename = "full path to excel file parameter file"
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
