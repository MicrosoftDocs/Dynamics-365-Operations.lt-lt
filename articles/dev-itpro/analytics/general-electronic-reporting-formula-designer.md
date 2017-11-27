---
title: "Elektroninių ataskaitų formulių kūrimo įrankis"
description: "Šioje temoje paaiškinama, kaip naudoti formulių kūrimo įrankį teikiant elektronines ataskaitas (ER)."
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 58bef33642d83def841eaa8334ea6f942063e0b3
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="formula-designer-in-electronic-reporting"></a>Elektroninių ataskaitų formulių kūrimo įrankis

[!include[banner](../includes/banner.md)]


Šioje temoje paaiškinama, kaip naudoti formulių kūrimo įrankį teikiant elektronines ataskaitas (ER). Kurdami ER konkretaus elektroninio dokumento formatą, duomenis galite transformuoti ir išpildyti atitinkamo dokumento kūrimo ir formatavimo reikalavimus naudodami „Microsoft Excel“ stiliaus formules. Palaikomos įvairių tipų funkcijos: tekstinės, datos ir laiko, matematinės, loginės, informacijos, duomenų tipo konvertavimo ir kitos (konkrečios verslo srities funkcijos).

<a name="formula-designer-overview"></a>Formulių kūrimo įrankio apžvalga
-------------------------

Elektroninės ataskaitos (ER) palaiko formulių kūrimo įrankį. Todėl kūrimo metu galite konfigūruoti išraiškas, kurias galima naudoti šių užduočių vykdymo metu:

-   transformuodami iš „Microsoft Dynamics 365 for Finance and Operations“ duomenų bazės gautus duomenis, kurie turėtų būti automatiškai įvesti ER duomenų modelyje, sukurtame kaip ER formatų (filtravimo, grupavimo, duomenų tipo konvertavimo ir t. t.) duomenų šaltinis;
-   formatuodami duomenis, kurie turi būti siunčiami į generuojamą elektroninį dokumentą pagal konkretaus ER formato maketą ir sąlygas (pagal norimą kalbą arba principą, kodavimą ir t. t.);
-   valdydami elektroninių dokumentų generavimo procesą (pagal apdorojamus duomenis įjungdami / išjungdami konkrečius formato elementus, pertraukdami dokumentų kūrimą, pateikdami pranešimus galutiniams vartotojams ir t. t.).

Formulės dizaino įrankio puslapį galima atlikus vieną iš tolesnių veiksmų.

-   Susiejus duomenų šaltinio elementus su duomenų modelio komponentais.
-   Susiejus duomenų šaltinio elementus su formato komponentais.
-   Atlikus apskaičiuotų laukų kaip duomenų šaltinių dalies priežiūrą.
-   Nurodžius vartotojo įvesties parametrų matomumo sąlygas.
-   Sukūrus formato pakeitimus.
-   Nurodžius formato komponentus įgalinančių sąlygas.
-   Nurodžius formato FILE komponentų failų vardus.
-   Nurodžius proceso kontrolės tikrinimų sąlygas.
-   Nurodžius proceso kontrolės tikrinimų pranešimo tekstą.

## <a name="designing-er-formulas"></a>ER formulių kūrimas
### <a name="data-binding"></a>Duomenų susiejimas

ER formulių kūrimo įrankį galima naudoti apibrėžiant išraišką, kuri transformuoja iš duomenų šaltinių gautus duomenis, kad tuos duomenis būtų galima automatiškai įvesti į duomenų vartotoją vykdymo metu:

-   iš „Finance and Operations“ duomenų šaltinių ir vykdymo laiko parametrų į ER duomenų modelį;
-   iš ER duomenų modelio į ER formatą;
-   iš „Finance and Operations“ duomenų šaltinių ir vykdymo laiko parametrų į ER formatą.

Tolesnė iliustracija rodo šio tipo išraiškos kūrimą. Šiame pavyzdyje išraiška pateikia „Finance and Operations“ **Intrastat** lentelės lauko **Intrastat.AmountMST** reikšmę po to, kai ši reikšmė suapvalinama iki dviejų skaičių po kablelio. [![picture-expression-binding](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) Tolesnėje iliustracijoje parodyta, kaip naudoti tokio tipo išraišką. Šiame pavyzdyje sukurtos išraiškos rezultatas automatiškai įvedamas į duomenų modelio **Mokesčių ataskaitos modelis** komponentą **Transaction.InvoicedAmount**. [![picture-expression-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) Sukurta formulė **ROUND (Intrastat.AmountMST, 2)** vykdymo metu suapvalins kiekvieno lentelės **Intrastat** įrašo lauko **AmountMST** reikšmę iki dviejų skaičių po kablelio ir automatiškai įves suapvalintą reikšmę į **mokesčių ataskaitos** duomenų modelio komponentą **Transaction.InvoicedAmount**.

### <a name="data-formatting"></a>Duomenų formatavimas

ER formulių kūrimo įrankį galima naudoti apibrėžiant išraišką, kuri formatuoja iš duomenų šaltinių gautus duomenis, kad tuos duomenis būtų galima siųsti kaip generuojamo elektroninio dokumento dalį. Jei turite formatavimą, kuris turi būti taikomas kaip įprasta pakartotinai naudojama formato taisyklė, tokį formatavimą galite vienu kartu įvesti į formato konfigūraciją kaip įvardytąjį pakeitimą, kuris turi formatavimo išraišką. Tada šį įvardytąjį pakeitimą galima susieti su daug formato komponentų, kurių išvedami duomenys turi būti formatuojami pagal sukurtą išraišką. Tolesnė iliustracija rodo šio tipo pakeitimo kūrimą. Šiame pavyzdyje pakeitimas **TrimmedString** gauna duomenų tipo **Eilutė** duomenis ir pateikdamas eilutės reikšmę sutrumpina priekinius ir galinius tarpus. [![picture-transformation-design](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) Tolesnė iliustracija parodo, kaip galima naudoti tipo transformaciją. Šiame pavyzdyje keletas formato komponentų, kurie vykdymo metu siunčia tekstą kaip išeigą į generuojamą elektroninį dokumentą, nurodo pakeitimą **TrimmedString** pagal pavadinimą. [![picture-transformation-usage](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Kai formato komponentų nurodo pakeitimą **TrimmedString** (pvz., komponentą **partyName** ankstesniame paveikslėlyje), į generuojama dokumentą siunčiamas tekstas kaip išeiga. Tame tekste nebūna priekinių ir galinių tarpų. Jei formatavimą būtina taikyti atskirai, galite jį nustatyti kaip atskirą konkretaus formato komponento susiejimo išraišką. Tolesnė iliustracija rodo šio tipo išraišką. Šiame pavyzdyje formato komponentas **partyType** yra susietas su duomenų šaltiniu per išraišką, kuri konvertuoja iš duomenų šaltinyje esančio lauko **Model.Company.RegistrationType** gaunamus duomenis į tekstą didžiosiomis raidėmis ir siunčia šį tekstą kaip elektroninio dokumento išeigą. [![picture-binding-with-formula](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Proceso eigos valdymas

ER formulių dizaino įrankis gali būti naudojamas apibrėžiant išraiškas, kurios valdo dokumentų generavimo proceso eigą. Galite:

-   Apibrėžkite sąlygas, kurios lemia, kada sustabyti dokumentų kūrimo procesą.
-   Nurodykite išraiškas, kurios kuria galutiniams vartotojams skirtus pranešimus apie sustabdytus procesus arba pateikia vykdymo žurnalo pranešimus apie besitęsiantį ataskaitų generavimo procesą.
-   Nurodykite generuojamų dokumentų failų vardus ir jų kūrimo kontrolės sąlygas.

Kiekviena proceso eigos valdymo taisyklė sukuriama kaip atskiras tikrinimo elementas. Tolesnė iliustracija rodo šio tipo tikrinimą. Čia pateikiamas šiame pavyzdyje esančios konfigūracijos paaiškinimas:

-   Tikrinimas įvertinamas, kai generuojamame XML faile sukuriamas mazgas **INSTAT**.
-   Jei operacijų sąrašas yra tuščias, tikrinimas sustabdo vykdymo procesą ir pateikia **FALSE**.
-   Tikrinimas pateikia klaidos pranešimą, kuriame yra žymės SYS70894 tekstas vartotojo pageidaujama kalba.

[![picture-validation](./media/picture-validation.jpg)](./media/picture-validation.jpg) Tikrinimo pavyzdys ER formulių kūrimo įrankį taip pat galima naudoti ir generuojamo elektroninio dokumento failo vardui nurodyti bei failų kūrimo procesui valdyti. Tolesnė iliustracija rodo šio tipo proceso eigos valdymo kūrimą. Čia pateikiamas šiame pavyzdyje esančios konfigūracijos paaiškinimas:

-   Duomenų šaltinio **model.Intrastat** įrašų sąrašas padalinamas į paketus, iš kurių kiekviename yra iki 1000 įrašų.
-   Išeiga sukuria „zip“ failą, kuriame yra po vieną failą XML formatu kiekvienam sukurtam paketui.
-   Išraiška pateikia generuojamų elektroninių dokumentų failo vardą sujungdama failo vardą ir failo plėtinį. Antrojo paketo ir visų vėlesnių paketų failo varde kaip priedėlis nurodytas paketo ID.
-   Išraiška įgalina (pateikdama reikšmę **TRUE**) paketų, kuriuose yra bent vienas įrašas, failų kūrimo procesą.

[![picture-file-control](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Pagrindinė sintaksė

ER išraiškos gali turėti bet kurį arba visus iš šių elementų:

-   Konstantos
-   Operatoriai
-   Nuorodos
-   Keliai
-   Funkcijos

#### <a name="constants"></a>Konstantos

Kurdami išraiškas galite naudoti tekstines ir skaitines konstantas (reikšmes, kurios nėra apskaičiuojamos). Pvz., išraiška **VALUE („100“) + 20** naudoja skaitinę konstantą 20 ir eilutės konstantą „100“, ir pateikia skaitinę reikšmę **120**. ER formulių dizaino įrankis palaiko kaitos sekas leisdamas nurodyti, kurią išraiškos eilutės dalį reikėtų tvarkyti kitaip. Pvz., išraiška **„Levas Tolstojus „„Karas ir taika““ 1 tomas“** pateikia teksto eilutę **Levas Tolstojus „Karas ir taika“ 1 tomas**.

#### <a name="operators"></a>Operatoriai

Toliau pateikiamoje lentelėje parodyti aritmetiniai operatoriai, kuriais galite atlikti pagrindines matematikos operacijas, pvz., sudėtį, atimtį, dalybą ir daugybą.

| Operatorius | Reikšmė              | Pavyzdys |
|----------|----------------------|---------|
| +        | Priedas             | 1+2     |
| -        | Atimties neigimas | 5-2 -1  |
| \*       | Daugyba       | 7 \* 8    |
| /        | Padalinys             | 9/3     |

Toliau pateikiamoje lentelėje parodyti palyginimo operatoriai, kurie yra palaikomi ir kuriuos galite naudoti dviem reikšmėms palyginti.

| Operatorius | Reikšmė                  | Pavyzdys    |
|----------|--------------------------|------------|
| =        | Lygu                    | X=Y        |
| &gt;     | Didesnis nei             | X &gt; Y     |
| &lt;     | Mažesnis nei                | X &lt; Y     |
| &gt;=    | Daugiau arba lygu | X &gt;= Y    |
| &lt;=    | Mažiau arba lygu    | X &lt;= Y    |
| &lt;&gt; | Nelygu             | X &lt;&gt; Y |

Be to, galite naudoti ampersendą (&) kaip teksto sujungimo operatorių, kad sujungtumėte ar susietumėte vieną ar daugiau teksto eilučių į vientisą tekstą.

| Operatorius | Reikšmė     | Pavyzdys                                        |
|----------|-------------|------------------------------------------------|
| &        | Sujungti | „Nėra ką spausdinti“ & „: „ & „įrašų nerasta“ |

#### <a name="operator-precedence"></a>Operatoriaus pirmenybė

Tvarka, kuria vertinamos sudėtinės išraiškos dalys, yra svarbi. Pvz., išraiškos **1 + 4 / 2** rezultatas skiriasi, atsižvelgiant į tai, ar pirma atliekama sudėties, ar dalybos operacija. Galite naudoti skliaustus, kad aiškiai apibrėžtumėte, kaip vertinti išraišką. Pvz., jei norite nurodyti, kad pirma turėtų būti atliekama sudėties operacija, minėtą išraišką galite pakeisti į **(1 + 4) / 2**. Jei išraiškoje atliekamų operacijų tvarka nėra aiškiai apibrėžta, ji nustatoma pagal numatytąją pirmenybę, kuri priskiriama palaikomiems operatoriams. Tolesnėje lentelėje parodyti operatoriai ir kiekvienam iš jų priskiriama pirmenybė. Aukštesnę pirmenybę (pvz., 7) turintys operatoriai vertinami prieš žemesnę pirmenybę (pvz., 1) turinčius operatorius.

| Pirmumas | Operatoriai      | Sintaksė                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Grupavimas       | ( … )                                                    |
| 6          | Nario prieiga  | … . …                                                    |
| 5          | Funkcijos iškvietimas  | … ( … )                                                  |
| 4          | Dauginamasis | … \* … … / …                                             |
| 3          | Priedas       | … + … … - …                                              |
| 2          | Palyginimas     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Atskyrimas     | … , …                                                    |

Toje pačioje eilutėje esantys operatoriai turi vienodą pirmenybę. Jei išraiška apima daugiau nei vieną iš šių operatorių, išraiška vertinama iš kairės į dešinę. Pvz., išraiška **1 + 6 / 2 \* 3 &gt; 5** pateikia reikšmę **true**. Aiškiai nurodyti norimą išraiškų vertinimo tvarką rekomenduojame naudojant skliaustus, kad išraiškas būtų lengviau skaityti ir prižiūrėti.

#### <a name="references"></a>Nuorodos

Visi dabartinio ER komponento (modelio arba formato) duomenų šaltiniai, kurie yra pasiekiami kuriant išraišką, gali būti naudojami kaip įvardytosios nuorodos. Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **ReportingDate**, kuris pateikia duomenų tipo **DATETIME** reikšmę. Norėdami gauti tinkamai suformatuotą reikšmę generuojamame dokumente, duomenų šaltinį galite nurodyti išraiškoje tokiu būdu: **DATETIMEFORMAT (ReportingDate, „MMMM-MM-dd“)** Prieš visus nuorodos duomenų šaltinio pavadinime esančius simbolius, kurie nėra abėcėlės raidė, turi būti padėtas viengubos kabutės ženklas ('). Jei nuorodos duomenų šaltinio pavadinime yra bent vienas simbolis, kuris nėra abėcėlės raidė (pvz., skyrybos ženklai arba bet kokie kiti rašytiniai simboliai), pavadinimas turi būti išskiriamas viengubomis kabutėmis. Štai keletas pavyzdžių:

-   Duomenų šaltinis **Today's date & time** ER išraiškoje turi būti nurodytas taip: **'Today''s date & time'**
-   Duomenų šaltinio **Klientai** metodas **name()** ER išraiškoje turi būti nurodytas taip: **Customers.'name()'**

Atkreipkite dėmesį, kad ši sintaksė naudojama iškviesti „Dynamics 365 for Operation“ duomenų šaltinių metodus naudojant parametrus:

- Sistemos duomenų šaltinio isLanguageRTL metodas su EN-US eilutės duomenų tipo parametru ER išraiškoje turi būti nurodytas taip:
- Kai metodo pavadinimą sudaro tik raidiniai ir skaitiniai simboliai, kabutės neprivalomos. Jos privalomos lentelės metodo atveju, kai pavadinime yra skliaustai.

Prie ER išdėstymo, kuris nurodo „Dynamics 365 for Operation“ programos klasę Visuotinė, pridėjus sistemos duomenų šaltinį, išraiška pateikia Būlio logikos reikšmę KLAIDINGA. Modifikuota išraiška, Sistema.’ isLanguageRTL'(„AR“) pateikia Būlio logikos reikšmę TEISINGA.

Atkreipkite dėmesį, kad perdavimą šiems metodų parametrams galima apibrėžti naudojant šiuos apribojimus:

- Šiems metodams galima perduoti tiktai tas konstantas, kurių reikšmė apibrėžta kūrimo metu.
- Tokie parametrai palaiko tik nesudėtingus (pagrindinius) duomenų tipus (sveikasis skaičius, realusis skaičius, Būlio logika, eilutė, ir t. t.).

#### <a name="path"></a>Maršrutas

Kai išraiška nurodo susistemintų duomenų šaltinį, galite naudoti kelio aprašą, kad pasirinktumėte konkretų nesudėtingą duomenų šaltinio elementą. Taško simbolis (.) naudojamas atskiriant atskirus susistemintų duomenų šaltinio elementus. Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **InvoiceTransactions**, kurį naudojant pateikiamas įrašų sąrašas. **InvoiceTransactions** įrašo struktūroje yra laukai **AmountDebit** ir **AmountCredit**, kurie pateikia skaitines reikšmes. Todėl galite SF sumą galite apskaičiuoti sukūrę tokią išraišką: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funkcijos

Kitame skyriuje aprašomos funkcijos, kurias galima naudoti ER išraiškose. Visi išraiškos konteksto (esamo ER duomenų modelio arba ER formato) duomenų šaltiniai bei konstantos pagal iškvietimo funkcijų argumentų sąrašą gali būti naudojamos kaip iškvietimo funkcijų parametrai. Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **InvoiceTransactions**, kurį naudojant pateikiamas įrašų sąrašas. **InvoiceTransactions** įrašo struktūroje yra laukai **AmountDebit** ir **AmountCredit**, kurie pateikia skaitines reikšmes. Dėl to, kad apskaičiuotumėte SF sumą, galite sukurti tokią išraišką, kuri naudoja įtaisytąją ER apvalinimo funkciją: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Palaikomos funkcijos
Toliau pateikiamose lentelėse aprašomos duomenų tvarkymo funkcijos, kurias galite naudoti ER duomenų modeliams ir ER ataskaitoms kurti. Funkcijų sąrašas nėra galutinis, o programuotojai gali jį papildyti. Norėdami matyti galimų naudoti funkcijų sąrašą, ER formulių dizaino įrankyje atidarykite funkcijų sritį.

### <a name="date-and-time-functions"></a>Datos ir laiko funkcijos

| Funkcija                                   | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                                                      | Pavyzdys                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (data ir laikas, dienos)                   | Įtraukti nurodytą dienų skaičių į nurodytą datos ir laiko reikšmę.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** nukelia datą ir laiką septyniomis dienomis į ateitį.                                                                                                                                                                                                                            |
| DATETODATETIME (data)                      | Konvertuoti nurodytos datos reikšmę į datos ir laiko reikšmę.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. 'getCurrentDate()')** pateikia dabartinio „Finance and Operations” seanso datą 2015-12-24 kaip **2015-12-24 00:00:00**. Šiame pavyzdyje **CompInfo** yra **„Finance and Operations“ / lentelės** tipo ER duomenų šaltinis, kuris nurodo lentelę CompanyInfo. |
| NOW ()                                     | Pateikti dabartinę „Finance and Operations“ programos serverio datą ir laiką kaip datos ir laiko reikšmę.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Pateikti dabartinę „Finance and Operations“ programos serverio datą kaip datos reikšmę.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Pateikti **neapibrėžtą** datos reikšmę.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Pateikti **neapibrėžtą** datos ir laiko reikšmę.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (data ir laikas, formatas)          | Konvertuoti nurodytą datos ir laiko reikšmę į nurodyto formato eilutę. (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), „mmmm-MM-dd“)** pateikia dabartinio „Finance and Operations“ programos seanso datą 2015-12-24 kaip **„2015-12-24“** pagal nurodytą pasirinktinį formatą.                                                                                                          |
| DATETIMEFORMAT (data ir laikas, formatas, principas) | Konvertuoti nurodytą datos ir laiko reikšmę į nurodyto formato eilutę ir [principą](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (NOW(), „d“, „de“)** pateikia dabartinio „Finance and Operations“ programos serverio datą 2015-12-24 kaip **„24.12.2015“** pagal pasirinktą vokišką principą.                                                                                                             |
| SESSIONTODAY ()                            | Pateikia dabartinio „Dynamics 365 for Finance and Operations“ seanso datą kaip datos reikšmę.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Pateikia dabartinio „Dynamics 365 for Finance and Operations“ seanso datą ir laiką kaip datos ir laiko reikšmę.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (data, formatas)                  | Pateikiama nurodyto formato datos eilutė.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), „mmmm-MM-dd“)** pateikia dabartinio „Dynamics 365 for Finance and Operations“ seanso datą 2015-12-24 kaip „**24-12-2015**“ pagal nurodytą pasirinktinį formatą.                                                                                                                      |
| DATEFORMAT (data, formatas, principas)         | Konvertuokite nurodytą datos reikšmę į nurodyto formato eilutę ir [principą](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)).     | **DATETIMEFORMAT (NOW(), „d“, „de“)** pateikia dabartinio „Finance and Operations“ seanso datą 2015-12-24 kaip **„24.12.2015“** pagal pasirinktą vokišką principą.                                                                                                                       |
| DAYOFYEAR (data)              | Pateikia dienų nuo sausio 1 d. iki nurodytos datos skaičių tekstine išraiška.       | **DAYOFYEAR (DATEVALUE („2016-03-01“, „mmmm-MM-dd“))** pateikia **61**. **DAYOFYEAR (DATEVALUE („2016-01-01“, „mmmm-MM-dd“))** pateikia **1**. 
                                                                                                                      |

**Duomenų konvertavimo funkcijos**

| Funkcija                                   | aprašymas                                                                                                                                                                                                                                                                                                                                                      | Pavyzdys                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DATETODATETIME (data)                 | Konvertuoti nurodytos datos reikšmę į datos ir laiko reikšmę.           | **DATETODATETIME (CompInfo. 'getCurrentDate()')** pateikia dabartinio „Finance and Operations” seanso datą 2015-12-24 kaip **2015-12-24 00:00:00**. Šiame pavyzdyje **CompInfo** yra **„Finance and Operations“ / lentelės** tipo ER duomenų šaltinis, kuris nurodo lentelę **CompanyInfo**.                                                                                                                       |
| DATEVALUE (eilutė, formatas)              | Pateikia nurodyto formato eilutės datos išraišką.       | **DATEVALUE („21-Dec-2016“, „dd-MM-mmmm“)** pateikia datą 2016-12-21 pagal nurodytą pasirinktinį formatą ir numatytosios programos **EN-US** principą.                                                                                                                       |
| DATEVALUE (eilutė, formatas, principas)              | Pateikia nurodyto formato ir principo eilutės datos išraišką.       | **DATEVALUE („21-Gen-2016“, „dd-MM-mmmm“, „IT“)** pateikia datą 2016-01-21 pagal nurodytą pasirinktinį formatą ir principą. Šios funkcijos iškvietimui, bus pateikta išimtis **DATEVALUE („21-Gen-2016“, „dd-MM-mmmm“, „EN-US“)** informuojanti, kad nurodyta eilutė neatpažinta kaip tinkama data.                                                                                                                       |
| DATETIMEVALUE (eilutė, formatas)              | Pateikia nurodyto formato eilutės datos ir laiko išraišką.       | **DATETIMEVALUE („21-Dec-2016 02:55:00“, „dd-MM-mmmm hh:mm:ss“)** pateikia 2016 m. gruodžio 21 d. 2:55:00 pagal nurodytą pasirinktinį formatą ir numatytosios programos **EN-US** principą.                                                                                                                       |
| DATETIMEVALUE (eilutė, formatas, principas)              | Pateikia nurodyto formato ir principo datos ir laiko eilutės išraišką.       | **DATETIMEVALUE („21-Gen-2016 02:55:00“, „dd-MM-mmmm hh:mm:ss“, „IT“)** pateikia 2016 m. gruodžio 21 d. 2:55:00 pagal nurodytą pasirinktinį formatą ir principą. Šios funkcijos iškvietimui, bus pateikta išimtis **DATEVALUE („21-Gen-2016 02:55:00“, „dd-MM-mmmm hh:mm:ss“, „EN-US“)** informuojanti, kad nurodyta eilutė neatpažinta kaip tinkama data ir laikas.                                                                                                                       |
### <a name="list-functions"></a>Sąrašo funkcijos

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkcija</th>
<th>aprašymas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (įvestis, ilgis)</td>
<td>Skaidyti nurodytą įvesties eilutę į antrines eilutes, iš kurių kiekvienos ilgis nurodomas atskirai. Pateikti rezultatą naujame sąraše.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> pateikia naują sąrašą, sudarytą iš dviejų įrašų, kuriuose yra laukas <strong>STRING</strong>. Pirmame įraše esančiame lauke yra tekstas <strong>&quot;abc&quot;</strong>, o antrame įraše esančiame lauke yra tekstas <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (sąrašas, numeris)</td>
<td>Skaidyti nurodytą sąrašą į paketus, iš kurių kiekviename būtų nurodytas įrašų skaičius. Pateikti rezultatą naujame paketų sąraše, kuriame yra šie elementai:
<ul>
<li>Paketai kaip įprasti sąrašai (<strong>Vertės </strong>komponentas)</li>
<li>Dabartinio paketo numeris (<strong>BatchNumber</strong>komponentas)</li>
</ul></td>
<td>Šiame pavyzdyje duomenų šaltinis <strong>Eilutės</strong> sukurtas kaip trijų įrašų sąrašas, suskirstytas į paketus, iš kurių kiekviename yra iki dviejų įrašų. 
<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> 

Tai yra sukurtas formato maketas, kur sukuriami susiejimai su duomenų šaltiniu <strong>Eilutės</strong>, siekiant generuoti išeigą XML formatu, kuris pateikia atskirus kiekvieno paketo ir jame esančių įrašų mazgus. 
<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> 

Tai yra sukurto formato vykdymo rezultatas. 
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (1 įrašas [, 2 įrašas,...])</td>
<td>Pateikti naują sąrašą, sukurtą iš nurodytų argumentų.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> pateikia tuščią įrašą, kur laukų sąraše yra visi <strong>MainData</strong> ir <strong>OtherData</strong> įrašų sąrašų laukai.</td>
</tr>
<tr class="even">
<td>LISTJOIN (1 sąrašas, 2 sąrašas, ...)</td>
<td>Pateikti jungtinį sąrašą, sukurtą iš nurodytų argumentų sąrašų.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> pateikia šešių įrašų sąrašą, kur viename <strong>STRING</strong> duomenų tipo lauke yra atskiros raidės.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (sąrašas)</td>
<td>Pateikti <strong>TRUE</strong>, jei nurodytame sąraše nėra jokių elementų. Kitu atveju pateikti <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (sąrašas)</td>
<td>Pateikti tuščią sąrašą naudojant nurodytą sąrašą kaip sąrašo struktūros šaltinį.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> pateikia naują tuščią sąrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį pateikia funkcija <strong>SPLIT</strong>.</td>
</tr>
<tr class="odd">
<td>FIRST (sąrašas)</td>
<td>Pateikti pirmą nurodyto sąrašo įrašą, jei tas įrašas nėra tuščias. Kitu atveju pateikti išimtį.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (sąrašas)</td>
<td>Pateikti pirmą nurodyto sąrašo įrašą, jei tas įrašas nėra tuščias. Kitu atveju pateikti <strong>neapibrėžtą</strong> įrašą.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (sąrašas)</td>
<td>Pateikti sąrašą, kuriame yra tik pirmas nurodyto sąrašo elementas.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (kelias)</td>
<td>Pateikti naują lygųjį sąrašą, kuriame nurodomi visi elementai, atitinkantys nurodytą kelią. Kelias turi būti nurodytas kaip tinkamas duomenų šaltinio kelias į įrašų sąrašo duomenų tipo duomenų šaltinio elementą. Nurodžius kelią į eilutę, datą ir pan. duomenų elementus, kūrimo metu ER išraiškos daryklėje turėtų kilti klaida.</td>
<td>Jei kaip duomenų šaltinį (DS) įvesite <strong>SPLIT(&quot;abcdef&quot; , 2)</strong>,<strong>COUNT( ALLITEMS (DS.Value))</strong> pateikia <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (sąrašas [, 1 išraiška, 2 išraiška, ...])</td>
<td>Pateikti nurodytą sąrašą, surūšiuotą pagal nurodytus argumentus, kuriuos galima apibrėžti kaip išraiškas.</td>
<td>Kai <strong>Tiekėjas </strong>sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable,<strong> ORDERBY (Tiekėjai, Vendors.'name()')</strong> pateikia tiekėjų sąrašą, surūšiuotą pagal pavadinimą didėjančia tvarka.</td>
</tr>
<tr class="even">
<td>REVERSE (sąrašas)</td>
<td>Pateikti nurodytą sąrašą atvirkštine rūšiavimo tvarka.</td>
<td>Kai <strong>Tiekėjas </strong>sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, <strong>REVERSE (ORDERBY (Tiekėjai, Vendors.'name()')) )</strong> pateikia tiekėjų sąrašą, surūšiuotą pagal pavadinimą mažėjančia tvarka.</td>
</tr>
<tr class="odd">
<td>WHERE (sąrašas, sąlyga)</td>
<td>Pateikti nurodytą sąrašą, filtruotą pagal nurodytą sąlygą. Kitaip nei naudojant funkciją <strong>FILTRAS</strong>, nurodyta sąlyga yra taikoma sąrašui atmintyje.</td>
<td>Kai <strong>Tiekėjas</strong> sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> pateikia tiekėjų sąrašą, kuris priklauso 40 tiekėjų grupei.</td>
</tr>
<tr class="even">
<td>ENUMERATE (sąrašas)</td>
<td>Pateikti naują sąrašą, sudarytą iš išvardytų nurodyto sąrašo įrašų ir parodantį šiuos elementus:
<ul>
<li>nurodytus sąrašo įrašus kaip įprastus sąrašus (<strong>Vertės </strong>komponentas);</li>
<li>dabartinio įrašo indeksą (<strong>Numerio </strong>komponentas).</li>
</ul></td>
<td>Šiame pavyzdyje <strong>Išvardytas</strong> duomenų šaltinis sukurtas kaip išvardytas tiekėjo įrašų sąrašas iš duomenų šaltinio <strong>Tiekėjai</strong>, kuris nurodo lentelę <strong>VendTable</strong>. 
<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a> 

Tai yra formatas, kur kuriami duomenų susiejimai siekiant generuoti išeigą XML formatu, kuris pateikia atskirus tiekėjus kaip išvardytus mazgus. 
<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> 

Tai yra sukurto formato vykdymo rezultatas. 
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (sąrašas)</td>
<td>Pateikti nurodytame sąraše esančių įrašų skaičių, jei sąrašas nėra tuščias. Kitu atveju pateikti <strong>0</strong> (nulis).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> pateikia <strong>2</strong>, nes funkcija <strong>SPLIT</strong> sukuria sąrašą, kurį sudaro du įrašai.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (kelias)</td>
<td>Pateikia įrašų sąrašą, sukurtą naudojant vieną iš toliau nurodytų tipų argumentų.
<ul>
<li>Modelių išvardijimas</li>
<li>Formatų išvardijimas</li>
<li>Konteineris</li>
</ul>
Sukurtą sąrašą sudarys įrašai su tolesniais laukais.
<ul>
<li>Vardas</li>
<li>Žyma</li>
<li>aprašymas</li>
</ul>
Laukuose Žyma ir Aprašas pateikiamos vykdymo metu gautos reikšmės pagal formato kalbos parametrus.</td>
<td>Toliau pateiktame pavyzdyje parodytas duomenų modelyje įvestas išvardijimas. 
<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Tolesniame pavyzdyje parodyta:
<ul>
<li>modelio išvardijimas, įtrauktas į ataskaitą kaip duomenų šaltinis;</li>
<li>ER išraiška, sukurta naudoti modelio išvardijimą kaip šios funkcijos parametrą;</li>
<li>įrašų sąrašo tipo duomenų šaltinis, įtrauktas į ataskaitą naudojant sukurtą ER išraišką.</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> 

Toliau pateiktame pavyzdyje parodyti ER formato elementai, susieti su įrašų sąrašo tipo duomenų šaltiniu, kuris buvo sukurtas naudojant LISTOFFIELDS funkciją.
<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Tai yra sukurto formato vykdymo rezultatas.
<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>

Pastaba:</strong> išverstas žymių ir aprašų tekstas yra įvedamas į ER formato išvestį pagal sukonfigūruotus pirminių formato elementų FAILAS ir APLANKAS kalbos parametrus.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (sąrašas, lauko pavadinimas, skyriklis)</td>
<td>Pateikia sujungtų lauko reikšmių eilutę iš sąrašo, atskirto pasirinktu skyrikliu.</td>
<td>Jei SPLIT(“abc” , 1) įvedėte kaip duomenų šaltinio DS, išraiška STRINGJOIN (DS, DS.Value, “:”) pateikia grąžina „a:b:c“</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (sąrašas, ribinė reikšmė, ribos šaltinis)</td>
<td>Nurodytą sąrašą padalija į naują antrinių sąrašų sąrašą ir pateikia rezultatą įrašų sąrašo turinyje. Ribinės reikšmės parametras nurodo ribos reikšmę, taikomą dalijant pradinį sąrašą. Ribos šaltinio parametras nurodo veiksmą, kurį atliekant bendra suma didėja. Riba netaikoma vienam konkretaus sąrašo elementui, kai ribos šaltinis viršija nustatytą ribą.</td>
<td>Toliau pateiktame pavyzdyje rodomas formato pavyzdys naudojant duomenų šaltinius. 
<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Tai yra formato vykdymo rezultatas, pateikiantis standartinį prekių sąrašą.
<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Toliau pateiktame pavyzdyje rodomas tas pats formatas, pakoreguotas norint pateikti prekių sąrašą paketais, kai viename pakete turi būti prekės, kurių bendrasis svoris negali viršyti ribos 9.
<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Tai pakoreguoto formato vykdymo rezultatas. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

<strong>Pastaba:</strong> riba nėra taikoma paskutinei pradinio sąrašo prekei, nes ribos šaltinio (svorio) reikšmė (11) viršija nustatytą ribą (9). Naudokite funkciją <strong>KUR</strong> arba atitinkamo formato elemento išraišką <strong>Įjungta</strong>, norėdami nepaisyti (praleisti) antrinius sąrašus generuojant ataskaitą (jei reikia).</td>
</tr>
<tr class="odd">
<td>FILTER (sąrašas, sąlyga)</td>
<td>Pateikia nurodytą sąrašą, filtruotą pagal nurodytą sąlygą, pakeičiant užklausą. Kitaip nei naudojant funkciją <strong>KUR</strong>, nurodyta sąlyga duomenų bazės lygiu taikoma bet kuriam ER duomenų šaltiniui, kurio tipas Lentelės įrašai.</td>
<td>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;) pateikia tiekėjų sąrašą, kuris priklauso 40 tiekėjų grupei, kai <strong>Tiekėjas</strong> sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę <strong>VendTable</strong></td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loginės funkcijos

| Funkcija                                                                                | aprašymas                                                                                                                                                                                                                                                                     | Pavyzdys                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CASE (išraiška, 1 parinktis, 1 rezultatas \[, 2 parinktis, 2 rezultatas\] ... \[, numatytasis rezultatas\]) | Įvertinti nurodytą išraiškos reikšmę pagal nurodytas alternatyvias parinktis. Pateikti pariunkties rezultatą, kuris yra lygus išraiškos reikšmei. Kitu atveju pateikti pasirinktinai įvestą numatytąjį rezultatą (paskutinį parametrą, prieš kurį nėra parinkties). | **CASE( DATETIMEFORMAT( NOW(), „MM“), „10“, „ŽIEMA“, „11“, „ŽIEMA“, „12“, „ŽIEMA“, „“)** pateikia eilutę **„ŽIEMA“**, kai dabartinio „Finance and Operations“ seanso data yra tarp spalio ir gruodžio mėn. Kitu atveju pateikia tuščią eilutę. |
| IF (sąlyga, 1 reikšmė, 2 reikšmė)                                                        | Pateikti nurodytą 1 reikšmę, kai išpildoma nurodyta sąlyga. Kitu atveju pateikti 2 reikšmę. Jei 1 ir 2 reikšmės yra įrašai ar įrašų sąrašai, rezultatas pateiks tik abiejuose sąrašuose esančius laukelius.                                                                     | **IF (1 = 2, „sąlyga išpildyta“, „sąlyga neišpildyta“)** pateikia eilutę **„sąlyga neišpildyta“**.                                                                                                                                                      |
| NOT (sąlyga)                                                                         | Pateikti atšauktą nurodytos sąlygos loginę reikšmę.                                                                                                                                                                                                                   | **NOT (TRUE)** pateikia **FALSE**.                                                                                                                                                                                                                            |
| AND (1 sąlyga\[, 2 sąlyga, ...\])                                                 | Pateikti **TRUE**, jei *visos* nurodytos sąlygos teisingos. Kitu atveju pateikti **FALSE**.                                                                                                                                                                                            | **AND (1=1, „a“=„a“)** pateikia **TRUE**. **AND (1=2, „a“=„a“)** pateikia **FALSE**.                                                                                                                                                                           |
| OR (1 sąlyga\[, 2 sąlyga, ...\])                                                  | Pateikti **FALSE**, jei *visos* nurodytos sąlygos klaidingos. Pateikti **TRUE**, jei *bet kuri iš* nurodytų sąlygų yra teisinga.                                                                                                                                                                 | **OR (1=2, „a“=„a“)** pateikia **TRUE**.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Matematinės funkcijos

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkcija</th>
<th>Prekės/Paslaugos pavadinimas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (skaičius)</td>
<td>Pateikti absoliučiąją nurodyto skaičiaus reikšmę (skaičius be ženklo).</td>
<td><strong>ABS (-1)</strong> pateikia <strong>1</strong>.</td>
</tr>
<tr class="even">
<td>POWER (skaičius, kėlimas laipsniu)</td>
<td>Pateikti nurodyto teigiamo skaičiaus kėlimo nurodytu laipsniu rezultatą.</td>
<td><strong>POWER (10, 2)</strong> pateikia <strong>100</strong>.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (eilutė, dešimtainis skyriklis, skaitmenų grupės skyriklis)</td>
<td>Konvertuoti nurodytą eilutę į skaičių. Nurodytas simbolis naudojamas atskirti sveikąjį skaičių ir dešimtainio skaičiaus trupmenines dalis, taip pat naudojamas nurodytas tūkstantųjų dalių skyriklis.</td>
<td><strong>NUMBERVALUE(&quot;1 234,56&quot;, &quot;,&quot;, &quot; &quot;)</strong> pateikia reikšmę <strong>1234.56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (eilutė)</td>
<td>Konvertuoti nurodytą eilutę į skaičių. Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas. Pateikti išimtį, jei nurodytoje eilutėje aptinkama kitų neskaitinių simbolių.</td>
<td><strong>VALUE (&quot;1 234,56&quot;)</strong> pateikia išimtį.</td>
</tr>
<tr class="odd">
<td>ROUND (skaičius, dešimtainės dalys)</td>
<td>Pateikti nurodytą skaičių, kuris apvalinamas iki nurodyto skaičiaus po kablelio:
<ul>
<li>Jei nurodytų dešimtainių dalių reikšmė yra didesnė už 0 (nulį), nurodytas skaičius apvalinamas iki nurodytos skaičiaus po kablelio.</li>
<li>Jei nurodytų dešimtainių dalių reikšmė yra 0 (nulis), nurodytas skaičius apvalinamas iki artimiausio sveikojo skaičiaus.</li>
<li>Jei nurodytų dešimtainių dalių reikšmė yra mažesnė už 0 (nulį), nurodytas skaičius apvalinamas į kairę nuo skaičiaus po kablelio.</li>
</ul></td>
<td><strong>ROUND (1200,767, 2)</strong> suapvalina iki dviejų skaičių po kablelio ir pateikia <strong>1200,77</strong>. <strong>ROUND (1200,767, -3)</strong> suapvalina iki artimiausio 1000 kartotinio ir pateikia <strong>1000</strong>.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (skaičius, dešimtainės dalys)</td>
<td>Pateikti nurodytą skaičių, kuris apvalinamas į mažesnę pusę (link nulio) iki nurodyto skaičiaus po kablelio. <strong>Pastaba:</strong> ši funkcija veikia kaip ir <strong>ROUND</strong>, bet ji visada apvalina nurodytą skaičių į mažesnę pusę.</td>
<td><strong>ROUNDDOWN (1200,767, 2)</strong> suapvalina į mažesnę pusę iki dviejų skaičių po kablelio ir pateikia <strong>1200,76</strong>. <strong>ROUNDDOWN (1700,767, -3)</strong> suapvalina į mažesnę pusę iki artimiausio 1,000 kartotinio ir pateikia <strong>1000</strong>.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (skaičius, dešimtainės dalys)</td>
<td>Pateikti nurodytą skaičių, kuris apvalinamas į didesnę pusę (tolyn nulio) iki nurodyto skaičiaus po kablelio. <strong>Pastaba:</strong> ši funkcija veikia kaip ir <strong>ROUND</strong>, bet ji visada apvalina nurodytą skaičių į didesnę pusę.</td>
<td><strong>ROUNDUP (1200,763, 2)</strong> suapvalina į didesnę pusę iki dviejų skaičių po kablelio ir pateikia <strong>1200,77</strong>. <strong>ROUNDUP (1200,767, -3)</strong> suapvalina į didesnę pusę iki artimiausio 1,000 kartotinio ir pateikia <strong>2000</strong>.</td>
</tr>
</tbody>
</table>

**Duomenų konvertavimo funkcijos**

| Funkcija             | aprašymas                                                                                                                                                                                                                                     | Pavyzdys                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| VALUE (eilutė) | Konvertuoti nurodytą eilutę į skaičių. Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas. Jei nurodytoje eilutėje aptinkama kitų neskaitinių simbolių, įvyksta klaida.                                                                                  | **VALUE („1 234,56“)** pateikia išimtį.   |
| NUMBERVALUE (eilutė, dešimtainis skyriklis, skaitmenų grupės skyriklis) | Konvertuoti nurodytą eilutę į skaičių. Nurodytas simbolis naudojamas atskirti sveikąjį skaičių ir dešimtainio skaičiaus trupmenines dalis, taip pat naudojamas nurodytas tūkstantųjų dalių skyriklis.                                                                                  | **NUMBERVALUE(„1 234,56“, „,“, „ “)** pateikia reikšmę **1234,56**.    |
| INTVALUE (eilutė) | Pateikia eilutę tekstine išraiška. Visos galimos dešimtainės dalys bus sutrumpintos.                                                                                  | **INTVALUE („100,77“)** pateikia **100**. |
| INTVALUE (numeris) | Pateikia numerį tekstine išraiška. Visos galimos dešimtainės dalys bus sutrumpintos.                                                                                  | **INTVALUE (-100,77)** pateikia **-100**. |
| INT64VALUE (eilutė) | Pateikia eilutę int64 išraiška. Visos galimos dešimtainės dalys bus sutrumpintos.                                                                                  | **INT64VALUE („22565422744“)** pateikia **22565422744**. |
| INT64VALUE (skaičius) | Pateikia numerį int64 išraiška. Visos galimos dešimtainės dalys bus sutrumpintos.                                                                                  | **INT64VALUE (22565422744,00)** pateikia **22565422744**. |



### <a name="record-functions"></a>Įrašo funkcijos

| Funkcija             | aprašymas                                                                                                                                                                                                                                     | Pavyzdys                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (sąrašas) | Pateikti **neapibrėžtą** įrašą, kuris turi tokią pačią struktūrą, kaip ir nurodytas įrašų sąrašas arba įrašas. **Pastaba:** ši funkcija nebenaudojama. Vietoje jos naudokite **EMPTYRECORD**.                                                                                  | **NULLCONTAINER (SPLIT („abc“, 1))** pateikia naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį pateikia funkcija **SPLIT**. |
| EMPTYRECORD (įrašas) | Pateikti **neapibrėžtą** įrašą, kuris turi tokią pačią struktūrą, kaip ir nurodytas įrašų sąrašas arba įrašas. **Pastaba:** tipo **null** įrašas yra įrašas, kurio visuose laukuose reikšmė nenurodyta (**0** \[nulis\] – skaičiams, tuščia eilutė – eilutėms ir t. t.). | **EMPTYRECORD (SPLIT („abc“, 1))** pateikia naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį pateikia funkcija **SPLIT**.   |

### <a name="text-functions"></a>Tekstinės funkcijos

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Funkcija</th>
<th>Prekės/Paslaugos pavadinimas</th>
<th>Pavyzdys</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (eilutė)</td>
<td>Pateikti nurodytą eilutę, kurios raidės konvertuotos į didžiąsias raides.</td>
<td><strong>UPPER(&quot;Sample&quot;)</strong> pateikia <strong>&quot;SAMPLE&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (eilutė)</td>
<td>Pateikti nurodytą eilutę, kurios raidės konvertuotos į mažąsias raides.</td>
<td><strong>LOWER (&quot;Sample&quot;)</strong> pateikia <strong>&quot;sample&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (eilutė, simbolių skaičius)</td>
<td>Pateikti nurodytą simbolių skaičių iš nurodytos eilutės pradžios.</td>
<td><strong>LEFT (&quot;Sample&quot;, 3)</strong> pateikia <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (eilutė, simbolių skaičius)</td>
<td>Pateikti nurodytą simbolių skaičių iš nurodytos eilutės pabaigos.</td>
<td><strong>RIGHT (&quot;Sample&quot;, 3)</strong> pateikia <strong>&quot;ple&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (eilutė, pradinė padėtis, simbolių skaičius)</td>
<td>Pateikti nurodytą simbolių skaičių iš nurodytos eilutės, pradedant nuo nurodytos padėties.</td>
<td><strong>MID (&quot;Sample&quot;, 2, 3)</strong> pateikia <strong>&quot;amp&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (eilutė)</td>
<td>Pateikti simbolių skaičių nurodytoje eilutėje.</td>
<td><strong>LEN (&quot;Sample&quot;)</strong> pateikia <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (skaičius)</td>
<td>Pateikti simbolių eilutę, kurią nurodo pateiktas „Unicode“ numeris.</td>
<td><strong>CHAR (255)</strong> pateikia <strong>&quot;ÿ&quot;</strong>. <strong>Pastaba:</strong> pateikta eilutė priklauso nuo kodavimo, kuris pažymėtas pirminiame formato FAILAS elemente. Palaikomų kodavimų sąrašą galima rasti temoje <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodavimo klasė</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (1 eilutė [, 2 eilutė, ...])</td>
<td>Pateikti visas nurodytas teksto eilutes, kurios sujungiamos į vieną eilutę.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> pateikia <strong>&quot;abcdef&quot;</strong>. <strong>Pastaba:</strong> išraiška <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> taip pat pateikia <strong>&quot;abcdef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (eilutė, šablonas, pakeitimas)</td>
<td>Pateikti nurodytą eilutę, kur visi simboliai, atitinkantys nurodytą šabloną, pakeičiami atitinkamose kitos nurodytos eilutės vietose esančiais simboliais.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> pakeičia simbolius <strong>&quot;cd&quot;</strong> eilute <strong>&quot;GH&quot;</strong> ir pateikia <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (eilutė, šablonas, pakeitimas, įprastos išraiškos žymė)</td>
<td>Kai nurodyta įprasta išraiškos žymė yra <strong>teisinga</strong>, pateikti nurodytą eilutę, kuri modifikuojama pritaikant įprastą išraišką, nurodytą kaip šios funkcijos argumento šablonas. Ši išraiška naudojama ieškant simbolių, kuriuos reikia pakeisti. Rasti simboliai pakeičiami nurodyto pakeitimo argumento simboliais. Kai nurodyta įprastos išraiškos žymė yra <strong>klaidinga</strong>, ši funkcija veikia kaip <strong>TRANSLATE</strong>.</td>
<td>  <strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> pritaiko įprastą išraišką, kuri pašalina visus neskaitinius simbolius ir pateikia <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> pakeičia simbolius <strong>&quot;cd&quot;</strong> eilute <strong>&quot;GH&quot;</strong> ir pateikia <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (įvestis)</td>
<td>Pateikti nurodytą įvestį, konvertuojamą į teksto eilutę, kuri formatuojama pagal dabartinio „Finance and Operations“ egzemplioriaus serverio vietos parametrus. <strong>Realaus skaičiaus</strong> tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.</td>
<td>Jei „Finance and Operations“ egzemplioriaus serverio vieta apibrėžiama kaip <strong>EN-US</strong>, <strong>TEXT (NOW ())</strong> pateikia dabartinio „Finance and Operations“ seanso datą 2015-12-17 kaip teksto eilutę <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> pateikia <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (1 eilutė, 2 eilutė[, 3 eilutė, ...])</td>
<td>Pateikti nurodytą eilutę, kuri formatuojama pakeičiant visus <strong>%N</strong> pasikartojimus <em>n</em>-uoju argumentu. Argumentai yra eilutės. Jei nėra pateiktas parametro argumentas, parametras eilutėje pateikiamas kaip <strong>&quot;%N&quot;</strong>. <strong>Realaus skaičiaus</strong> tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.</td>
<td>Šiame pavyzdyje duomenų šaltinis <strong>PaymentModel</strong> pateikia klientų įrašus komponente <strong>Klientas</strong> ir apdorojimo datos reikšmę lauke <strong>ProcessingDate</strong>. 
<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a> 

ER formate, skirtame generuoti elektroninį failą pasirinktiems klientams, <strong>PaymentModel</strong> yra pasirinktas kaip duomenų šaltinis ir kontroliuoja proceso eigą. Galutiniams vartotojams pateikiama išimtis, kai pasirinktas klientas sustabdomas ataskaitos apdorojimo dieną. Formulė, sukurta šio tipo apdorojimo kontrolei, gali naudoti tokius išteklius:
<ul>
<li>„Finance and Operations“ žymė SYS70894, kur nurodytas toks tekstas:
<ul>
<li><strong>EN-US kalba:</strong> &quot;Nothing to print&quot;</li>
<li><strong>DE kalba:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>„Finance and Operations“ žymė SYS18389, kur nurodytas toks tekstas:
<ul>
<li><strong>EN-US kalba:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>DE kalba:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Tai yra formulė, kurią galima sukurti: FORMAT (CONCATENATE @&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;)) Jei ataskaita apdorojama klientui <strong>„Litware Retail“</strong> 2015 m. gruodžio 17 d., pagal <strong>EN-US</strong> principą ir <strong>EN-US</strong> kalbą ši formulė pateikia tokį tekstą, kuris galutiniam vartotojui gali būti pateiktas kaip išimties pranešimas: &quot;Nothing to print. Klientas „Litware Retail“ sustabdytas 2015-12-17.&quot; Jei ta pati ataskaita apdorojama<strong> klientui „Litware Retail“</strong> 2015 m. gruodžio 17 d. pagal <strong>DE</strong> principą ir <strong>DE</strong> kalbą, ši formulė pateikia tokį tekstą, kuris naudoja kitokį datos formatą: &quot;Nichts zu drucken. Debitor "Litware Retail" wird für 17.12.2015 gesperrt.&quot; <strong>Pastaba:</strong> ER formulėse žymėms taikoma tokia sintaksė:
<ul>
<li><strong>Žymėms iš „Finance and Operations“ išteklių:</strong> <strong>@&quot;X&quot;</strong>, kur X yra žymės ID programos objektų medyje (AOT)</li>
<li><strong>ER konfigūracijose esančioms žymėms:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, kur X yra žymės ID ER konfigūracijoje.</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (skaičius, formatas)</td>
<td>Pateikti nurodyto skaičiaus eilutę nurodytu formatu. (Daugiau informacijos apie palaikomus formatus rasite čia: <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standartinis</a> ir <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">pasirinktinis</a>.) Kontekstas, kuriame vykdome ši funkcija, nulemia, kokiu principu bus formatuojami skaičiai.</td>
<td>Pagal LT principą <strong>NUMBERFORMAT (0,45, &quot;p&quot;)</strong> pateikia <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> pateikia <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (numeris, kalba, valiuta, spausdinimo valiutos pavadinimo žymė, dešimtainiai skaičiai)</td>
<td>Pateikia skaičių, parašytą (konvertuotą) į teksto eilutes nurodyta kalba. Kalbos kodas neprivalomas: kai jis nurodytas kaip tuščia eilutė, bus naudojamas vykdomo konteksto kalbos kodas (skirtas generuojamam aplankui arba failui). Valiutos kodas nėra būtinas. Kai jis nurodytas kaip tuščia eilutė, naudojama įmonės valiuta. Atkreipkite dėmesį, kad parametrai <strong>Spaudinio valiutos pavadinimas</strong> ir <strong>Dešimtainiai skaičiai</strong> yra analizuojami tik pagal šiuos kalbų kodus: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Atkreipkite dėmesį, kad parametras <strong>Spaudinio valiutos pavadinimas</strong> analizuojamas tik „Finance and Operations“ įmonėms, kurių šalies kontekste palaikomas valiutos linksniavimas.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2) pateikia „One Thousand Two Hundred Thirty Four and 56“ NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0) pateikia „Sto dwadzieścia“ NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2) pateikia „Сто двадцать евро 21 евроцент“</td>
</tr>
<tr class="odd">
<td>PADLEFT (eilutė, ilgis, užpildymo simboliai)</td>
<td>Pateikiama nustatyto ilgio eilutė, kurioje eilutės pradžia užpildyta nurodytais simboliais.</td>
<td>PADLEFT (“1234”, 10, “ “) pateikia teksto eilutę „      1234“</td>
</tr>
<tr class="even">
<td>TRIM (eilutė)</td>
<td>Pateikiamas duotas tekstas, sutrumpintas pašalinus pradžioje ir gale esančius tarpus, ir pašalinami keli tarp žodžių esantys tarpai. </td>
<td><strong>TRIM („     Pavyzdinis     tekstas     “)</strong> pateikia <strong>„Pavyzdinis tekstas“.</strong></td>
</tr>
<tr class="odd">
<td>GETENUMVALUEBYNAME (išvardijimo duomenų šaltinio kelias, išvardijimo reikšmės žymės tekstas)</td>
<td>Pateikia nurodytų išvardijimo duomenų šaltinio reikšmę šios išvardijimo žymės nurodytu tekstu.</td>
<td>Toliau pateiktame pavyzdyje parodytas duomenų modelyje įvestas išvardijimas ReportDirection. Atkreipkite dėmesį, kad išvardijimo reikšmėms nurodytos žymės.
<a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>  
<p>Tolesniuose pavyzdžiuose parodyta:</p>
<ul><li>modelio išvardijimas <strong>ReportDirection</strong>, įtrauktas į ataskaitą kaip duomenų šaltinis <strong>$Direction</strong>;</li>
<li>ER išraiška <strong>$IsArrivals</strong>, sukurta naudoti modelio išvardijimą kaip šios funkcijos parametrą. Šios išraiškos reikšmė yra <strong>TRUE</strong>.
</li></ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></td>
</tr>
</tbody>
</table>

**Duomenų konvertavimo funkcijos**

| Funkcija             | aprašymas                                                                                                                                                                                                                                     | Pavyzdys                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| TEXT (įvestis) | Pateikti nurodytą įvestį, konvertuojamą į teksto eilutę, kuri formatuojama pagal dabartinio „Finance and Operations“ egzemplioriaus serverio vietos parametrus.
Realaus skaičiaus tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.| Jei „Finance and Operations“ egzemplioriaus serverio vieta apibrėžiama kaip **EN-US, TEXT (NOW ())**, dabartinio „Finance and Operations“ seanso data, 2015-12-17, pateikiama kaip teksto eilutė **2015-12-17 07:59:23**.
**TEKSTAS (1/3) pateikia „0,33“**. |
| QRCODE (eilutė) | Pateikiamas nurodytos eilutės QR kodo vaizdas dvejetainiu „base64‟ formatu. | **QRCODE („Pavyzdinis tekstas“)** pateikia **U2FtcGxlIHRleHQ=**.   |

### <a name="data-collection-functions"></a>Duomenų rinkinio funkcijos

| Funkcija             | aprašymas                                                                                                                                                                                                                                     | Pavyzdys                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATELEMENTNAME () | Pateikia šio formato elemento pavadinimą. Pateikia tuščią eilutę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.| Žr. užduočių vedlį **ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant** (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis), norėdami daugiau sužinoti apie šios funkcijos naudojimą. |
| SUMIFS (rakto eilutė, skirta sumuoti, 1 kriterijų klasės eilutėje, 1 kriterijų reikšmės eilutė \[, 2 kriterijų diapazono eilutė, 2 kriterijų reikšmių eilutė, ...\]) |Pateikia XML mazgų (kurių pavadinimas apibrėžtas kaip raktas) reikšmių, kurios surinktos vykdant šį formatavimą ir kurios tenkina įvestas sąlygas (diapazoną ir reikšmę), sumą. Pateikia nulio reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta. |            |
| SUMIF (rakto eilutė, skirta sumuoti, kriterijų diapazono eilutė, kriterijų reikšmių eilutė) | Pateikia XML mazgų (kurių pavadinimas apibrėžtas kaip raktas) reikšmių, kurios surinktos vykdant šį formatavimą ir kurios tenkina įvestą sąlygą (diapazoną ir reikšmę), sumą. Pateikia nulio reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.|           |
| COUNTIFS (1 kriterijų klasės eilutėje, 1 kriterijų reikšmės eilutė \[, 2 kriterijų intervalo eilutė, 2 kriterijų reikšmės eilutė, ...\]) | Pateikia XML mazgų, kurie buvo surinkti vykdant šį formatavimą ir kurie tenkina įvestas sąlygas (diapazoną ir reikšmę), numerį. Pateikia nulio reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.|     |
| COUNTIF (kriterijų diapazono eilutė, kriterijų reikšmių eilutė) | Pateikia XML mazgų, kurie surinktos vykdant šį formatavimą ir kurie tenkina įvestą sąlygą (diapazoną ir reikšmę), numerį. Pateikia nulio reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.|          |
| COLLECTEDLIST (1 kriterijų klasės eilutėje, 1 kriterijų reikšmės eilutė \[, 2 kriterijų intervalo eilutė, 2 kriterijų reikšmės eilutė, ...\]) | Pateikia XML mazgų reikšmių, kurios surinktos vykdant šį formatavimą ir kurios tenkina įvestas sąlygas (diapazoną ir reikšmę), sąrašą. Pateikia tuščią sąrašą, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.|               |   




### <a name="other-business-domainspecific-functions"></a>Kitos (konkrečios verslo srities) funkcijos

| Funkcija                                                                         | aprašymas                                                                                                                                                                                                                                                        | Pavyzdys                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (suma, pirminė valiuta, norima valiuta, data, įmonė)        | Konvertuoti nurodytą piniginę sumą iš pirminės valiutos į norimą valiutą naudojant nurodytos „Finance and Operations“ įmonės parametrus nurodytą dieną.                                                                            | **CONVERTCURRENCY (1, „EUR“, „USD“, TODAY(), „DEMF“)** pateikia vieno euro atitikmenį doleriais dabartinio seanso dieną, atsižvelgiant į DEMF įmonės parametrus.                                                                                                                                  |
| ROUNDAMOUNT (skaičius, dešimtainės dalys, apvalinimo taisyklė)                                       | Apvalinti nurodytą sumą pagal nurodytą apvalinimo taisyklę ir nurodytą skaičių po kablelio. **Pastaba:** apvalinimo taisyklė turi būti nurodyta kaip „Finance and Operations“ **RoundOffType** išvardijimo reikšmė.                          | Jei nustatyta parametro **model.RoundOff** reikšmė ****Į mažesnę pusę****, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** pateikia reikšmę **1000.78**. Jei parametrui **model.RoundOff** nustatyta reikšmė **Įprastai** arba **Į didesnę pusę**, **ROUNDAMOUNT (1000,787, 2, model.RoundOff)** pateikia reikšmę **1000,79**. |
| CURCredRef (skaitmenys)                                                              | Pateikti kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis.                                                                                                                                                                                  | **CURCredRef („VEND-200002“)** pateikia **„2200002“**.                                                                                                                                                                                                                                                         |
| MOD\_97 (skaitmenys)                                                                 | Pateikti kreditoriaus nuorodą kaip MOD97 išraišką pagal nurodyto SF numerio skaitmenis.                                                                                                                                                            | **MOD\_97 ("VEND-200002")** pateikia **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (skaitmenys)                                                              | Pateikti ISO kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis ir raidinius simbolius. **Pastaba:** norint iš abėcėlės pašalinti simbolius, kurie nėra suderinami su ISO, įvesties parametras turi būti išverstas prieš jį perduodant į šią funkciją. | **ISOCredRef („VEND-200002“)** pateikia **„RF23VEND-200002“**.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (eilutė, numeris)                                  | Gaukite papildomos finansinės dimensijos ID. Dimensijos šioje eilutėje rodomos kaip kableliais atskirti ID. Numeriai nurodyto pageidaujamą dimensijos numeracijos kodą šioje eilutėje.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3) pateikia „CC“                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Pateikia juridinio subjekto (įmonės), prie kurio šiuo metu vartotojas prisijungęs, kodą tekstine išraiška.                                                                                                                                                                                                                    | Vartotojui, prisijungusiam prie „Finance and Operations” įmonės **„Contoso Entertainment System USA“**, **(GETCURRENTCOMPANY)** pateikia **USMF**.                                                                                                                                                                                                                                                                                                              |
| CH\_BANK\_MOD\_10 (skaitmenys)                                                       | Pateikia kreditoriaus nuorodą kaip MOD10 išraišką pagal nurodyto SF numerio skaitmenis.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") pateikia 3                                                                                                                                                                                                                                                                   |
| FA\_SUM (ilgalaikio turto kodas, vertinimo modelio kodas, pradžios datas, pabaigos data)               | Pateikia paruoštą tam tikro laikotarpio ilgalaikio turto sumų duomenų konteinerį.                                                                                                                                                                                         | FA\_SUM ("COMP-000001", “Current”, Date1, Date2) pateikia paruoštą ilgalaikio turto COMP-000001 duomenų konteinerį su vertinimo modeliu Dabartinis, skirtu laikotarpiui nuo Date1 iki Date2.                                                                                                                        |
| FA\_BALANCE (ilgalaikio turto kodas, vertinimo modelio kodas, ataskaitiniai metai, ataskaitų data) | Pateikiamas paruoštas ilgalaikio turto balansų duomenų konteineris. Ataskaitiniai metai turi būti nurodyti kaip „Finance and Operations“ išvardijimo reikšmė **AssetYear**.                                                                                           | FA\_SUM („COMP-000001“, „Dabartinis“, AxEnumAssetYear.ThisYear, SESSIONTODAY ()) pateikia paruoštą ilgalaikio turto COMP-000001 balansų duomenų konteinerį su vertinimo modeliu „Dabartinis“ dabartinio „365 for Finance and Operations“ seanso datą.                                                                |
| TABLENAME2ID (eilutė)                                                       | Pateikia nurodyto lentelės pavadinimo lentelės ID tekstine išraiška.                                                                                                                                                                      | **TABLENAME2ID („Intrastat“)** pateikia **1510**.                                                                                                                                                                                                                                                                   |
| ISVALIDCHARACTERISO7064 (eilutė)                                                       | Pateikia Būlio logikos reikšmę **TEISINGA**, kai pateikta eilutė rodo tinkamą tarptautinį banko sąskaitos numerį (IBAN). Pateikia Būlio logikos reikšmę **KLAIDINGA** kitu atveju.                                                                                                                                                                      | **ISVALIDCHARACTERISO7064 („AT61 1904 3002 3457 3201“)** pateikia **TEISINGA**. **ISVALIDCHARACTERISO7064 („AT61“)** pateikia **KLAIDINGA**.                                                                                                                                                                                                                                                                   |

### <a name="functions-list-extension"></a>Funkcijų sąrašo papildymas

ER leidžia papildyti ER išraiškose naudojamų funkcijų sąrašą. Tam reikės atitinkamų inžinerinių įgūdžių. Daugiau informacijos rasite [Elektroninių ataskaitų funkcijų sąrašo papildymas](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų (ER) funkcijų sąrašo išplėtimas](general-electronic-reporting-formulas-list-extension.md)




