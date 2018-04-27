---
title: "Elektroninių ataskaitų formulių kūrimo įrankis"
description: "Šioje temoje paaiškinama, kaip naudoti formulių kūrimo įrankį teikiant elektronines ataskaitas (ER)."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: adbbb36da2bc1e9a2211c703823370571105ecab
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="formula-designer-in-electronic-reporting"></a>Elektroninių ataskaitų formulių kūrimo įrankis

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip naudoti formulių kūrimo įrankį teikiant elektronines ataskaitas (ER). Kurdami ER konkretaus elektroninio dokumento formatą, naudodami formules galite transformuoti duomenis, kad jie atitiktų dokumento įvykdymo ir formatavimo reikalavimus. Šios formulės panašios į „Microsoft Excel“ formules. Formulėse palaikomos įvairių tipų funkcijos: tekstinės, datos ir laiko, matematinės, loginės, informacijos, duomenų tipo konvertavimo ir kitos (konkrečios verslo srities funkcijos).

## <a name="formula-designer-overview"></a>Formulių kūrimo įrankio apžvalga

ER palaiko formulių kūrimo įrankį. Todėl kūrimo metu galite konfigūruoti išraiškas, kurias galima naudoti tolesnių užduočių vykdymo metu.

- Iš „Microsoft Dynamics 365 for Finance and Operations“ duomenų bazės gautų duomenų, kurie turėtų būti įvesti ER duomenų modelyje, sukurtame kaip ER formatų duomenų šaltinis, transformavimas. (Pavyzdžiui, toks transformavimas gali būti filtravimas, grupavimas ir duomenų tipo konvertavimas.)
- Duomenų, kurie turi būti siunčiami į generuojamą elektroninį dokumentą pagal konkretaus ER formato maketą ir sąlygas, formatavimas. (Pvz., formatuoti galima pagal norimą kalbą ar kultūrą, arba kodavimą).
- Elektroninių dokumentų kūrimo proceso kontroliavimas. (Pavyzdžiui, pagal apdorojamus duomenis išraiškomis galima įjungti ar išjungti tam tikrus išvedamus formato elementus. Jomis taip pat galima pertraukti dokumentų kūrimo procesą, ar pateikti pranešimus vartotojams.)

Puslapį **Formulių konstruktorius**galite atidaryti atlikdami bet kurį iš tolesnių veiksmų.

- Susiejus duomenų šaltinio elementus su duomenų modelio komponentais.
- Susiejus duomenų šaltinio elementus su formato komponentais.
- Atlikus apskaičiuotų laukų, kurie yra duomenų šaltinių dalis, priežiūrą.
- Nurodžius vartotojo įvesties parametrų matomumo sąlygas.
- Sukūrus formato pakeitimus.
- Nurodžius formato komponentus įgalinančių sąlygas.
- Nurodžius formato FILE komponentų failų vardus.
- Nurodžius proceso kontrolės tikrinimų sąlygas.
- Nurodžius proceso kontrolės tikrinimų pranešimo tekstą.

## <a name="designing-er-formulas"></a>ER formulių kūrimas

### <a name="data-binding"></a>Duomenų susiejimas

ER formulių kūrimo įrankį galima naudoti apibrėžiant išraišką, kuri transformuoja iš duomenų šaltinių gautus duomenis, kad tuos duomenis būtų galima įvesti į duomenų vartotoją vykdymo metu:

- iš „Finance and Operations“ duomenų šaltinių ir vykdymo laiko parametrų į ER duomenų modelį;
- iš ER duomenų modelio į ER formatą;
- iš „Finance and Operations“ duomenų šaltinių ir vykdymo laiko parametrų į ER formatą.

Tolesnė iliustracija rodo šio tipo išraiškos kūrimą. Šiame pavyzdyje išraiška suapvalina „Finance and Operations“ Intrastat lentelės lauko **Intrastat.AmountMST** reikšmę iki dviejų skaičių po kablelio ir pateikia suapvalintą reikšmę.

[![Duomenų susiejimas](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Tolesnėje iliustracijoje parodyta, kaip galima naudoti šio tipo išraišką. Šiame pavyzdyje sukurtos išraiškos rezultatas įvedamas į duomenų modelio **Mokesčių ataskaitos modelis** komponentą **Transaction.InvoicedAmount**.

[![Naudojamas duomenų susiejimas](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Vykdymo metu sukurta formulė **ROUND (Intrastat.AmountMST, 2)** kiekvieno Intrastat lentelės įrašo lauko **AmountMST** reikšmę suapvalina iki dviejų skaičių po kablelio. Suapvalintą reikšmę ji tada įveda į duomenų modelio **Mokesčių ataskaitos** komponentą **Transaction.InvoicedAmount**.

### <a name="data-formatting"></a>Duomenų formatavimas

ER formulių kūrimo įrankį galima naudoti apibrėžiant išraišką, kuri formatuoja iš duomenų šaltinių gautus duomenis, kad tuos duomenis būtų galima siųsti kaip generuojamo elektroninio dokumento dalį. Galite turėti formatavimą, kuris turi būti taikomas kaip įprasta pakartotinai naudojama formato taisyklė. Tokiu atveju šį formatavimą galite vienu kartu įvesti į formato konfigūraciją kaip įvardytąją transformaciją, kuri turi formatavimo išraišką. Tada šią įvardytąją transformaciją galima susieti su daug formato komponentų, kurių išvedami duomenys turi būti formatuojami pagal jūsų sukurtą formatavimo išraišką.

Tolesnė iliustracija rodo šio tipo pakeitimo kūrimą. Šiame pavyzdyje transformacija **TrimmedString** sutrumpina duomenų tipo **Eilutė** duomenis pašalindama priekinius ir galinius tarpus. Tada ji pateikia sutrumpintą eilutės reikšmę.

[![Transformacija](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Tolesnė iliustracija parodo, kaip galima naudoti tipo transformaciją. Šiame pavyzdyje keletas formato komponentų vykdymo metu siunčia tekstą kaip išeigą į generuojamą elektroninį dokumentą. Visi šie formato keitimai nurodo transformaciją **TrimmedString** pagal pavadinimą.

[![Naudojama transformacija](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Kai formato komponentai, pvz., komponentas **partyName** ankstesnėje iliustracijoje, nurodo transformaciją **TrimmedString**, transformacija į generuojamą elektrinį dokumentą kaip išeigą siunčia tekstą. Šiame tekste nėra priekinių ir galinių tarpų.

Jei formatavimą būtina taikyti atskirai, galite jį nustatyti kaip atskirą konkretaus formato komponento susiejimo išraišką. Tolesnė iliustracija rodo šio tipo išraišką. Šiame pavyzdyje formato komponentas **partyType** yra susietas su duomenų šaltiniu per išraišką, kuri konvertuoja iš duomenų šaltinyje esančio lauko **Model.Company.RegistrationType** gaunamus duomenis į tekstą didžiosiomis raidėmis. Tada išraiška šį tekstą kaip išeigą siunčia į elektroninį dokumentą.

[![Formatavimo taikymas atskiram komponentui](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Proceso eigos valdymas

ER formulių dizaino įrankis gali būti naudojamas apibrėžiant išraiškas, kurios valdo elektroninių dokumentų generavimo proceso eigą. Galite atlikti šias užduotis:

- Apibrėžkite sąlygas, kurios lemia, kada sustabyti dokumentų kūrimo procesą.
- Nurodykite išraiškas, kurios kuria vartotojams skirtus pranešimus apie sustabdytus procesus arba pateikia vykdymo žurnalo pranešimus apie besitęsiantį ataskaitų generavimo procesą.
- Nurodykite generuojamų elektroninių dokumentų failų pavadinimus ir kontroliuokite jų kūrimo sąlygas.

Kiekviena proceso eigos valdymo taisyklė sukuriama kaip atskiras tikrinimo elementas. Tolesnė iliustracija rodo šio tipo tikrinimą. Čia pateikiamas šiame pavyzdyje esančios konfigūracijos paaiškinimas:

- Tikrinimas įvertinamas, kai generuojant XML failą sukuriamas mazgas **INSTAT**.
- Jei operacijų sąrašas yra tuščias, tikrinimas sustabdo vykdymo procesą ir pateikia **FALSE**.
- Tikrinimas pateikia klaidos pranešimą, kuriame yra „Finance and Operations“ žymos SYS70894 tekstas vartotojo pageidaujama kalba.

[![Tikrinimas](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER formulių dizaino įrankį taip pat galima naudoti ir generuojamo elektroninio dokumento failo pavadinimui generuoti bei failų kūrimo procesui kontroliuoti. Tolesnė iliustracija rodo šio tipo proceso eigos valdymo kūrimą. Čia pateikiamas šiame pavyzdyje esančios konfigūracijos paaiškinimas:

- Duomenų šaltinio **model.Intrastat** įrašų sąrašas padalijamas į paketus. Kiekviename pakete yra iki 1000 įrašų.
- Išeiga sukuria „zip“ failą, kuriame yra po vieną failą XML formatu kiekvienam sukurtam paketui.
- Išraiška pateikia generuojamų elektroninių dokumentų failo pavadinimą sujungdama failo pavadinimą ir jo plėtinį. Antrojo paketo ir visų vėlesnių paketų failo varde kaip priedėlis nurodytas paketo ID.
- Išraiška įgalina (pateikdama reikšmę **TRUE**) paketų, kuriuose yra bent vienas įrašas, failų kūrimo procesą.

[![Failų kontrolė](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Pagrindinė sintaksė

ER išraiškos gali turėti bet kurį arba visus iš šių elementų:

- Konstantos
- Operatoriai
- Nuorodos
- Keliai
- Funkcijos

#### <a name="constants"></a>Konstantos

Kurdami išraiškas galite naudoti tekstines ir skaitines konstantas (t. y., reikšmes, kurios nėra apskaičiuojamos). Pavyzdžiui, išraiška **VALUE ("100") + 20** naudoja skaitinę konstantą **20** ir eilutės konstantą **"100"** bei pateikia skaitinę reikšmę **120**. ER formulių dizaino įrankis palaiko kaitos sekas. Todėl galite nurodyti, kurią išraiškos eilutę reikėtų tvarkyti kitaip. Pvz., išraiška **„Levas Tolstojus „„Karas ir taika““ 1 tomas“** pateikia teksto eilutę **Levas Tolstojus „Karas ir taika“ 1 tomas**.

#### <a name="operators"></a>Operatoriai

Toliau pateikiamoje lentelėje parodyti aritmetiniai operatoriai, kuriais galite atlikti pagrindines matematikos operacijas, pvz., sudėtį, atimtį, daugybą ir dalybą.

| Operatorius | Reikšmė               | Pavyzdys |
|----------|-----------------------|---------|
| +        | Priedas              | 1+2     |
| -        | Atimtis, neigimas | 5–2, –1 |
| \*       | Daugyba        | 7 \* 8    |
| /        | Padalinys              | 9/3     |

Toliau pateikiamoje lentelėje parodyti palyginimo operatoriai, kurie yra palaikomi. Juos naudodami galite palyginti dvi reikšmes.

| Operatorius | Reikšmė                  | Pavyzdys    |
|----------|--------------------------|------------|
| =        | Lygu                    | X=Y        |
| &gt;     | Didesnis nei             | X &gt; Y     |
| &lt;     | Mažesnis nei                | X &lt; Y     |
| &gt;=    | Daugiau arba lygu | X &gt;= Y    |
| &lt;=    | Mažiau arba lygu    | X &lt;= Y    |
| &lt;&gt; | Nelygu             | X &lt;&gt; Y |

Be to, galite naudoti ampersendą (&) kaip teksto sujungimo operatorių. Taip vieną ar kelias teksto eilutes galite sujungti ar susieti į vientisą tekstą.

| Operatorius | Reikšmė     | Pavyzdys                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Sujungti | „Nėra ką spausdinti“ & „:&nbsp;“ & „įrašų nerasta“ |

##### <a name="operator-precedence"></a>Operatoriaus pirmenybė

Tvarka, kuria vertinamos sudėtinės išraiškos dalys, yra svarbi. Pavyzdžiui, išraiškos **1 + 4 / 2** rezultatas skiriasi, atsižvelgiant į tai, ar pirma atliekama sudėties, ar dalybos operacija. Galite naudoti skliaustus, kad aiškiai apibrėžtumėte, kaip vertinti išraišką. Pavyzdžiui, jei norite nurodyti, kad pirma turėtų būti atliekama sudėties operacija, minėtą išraišką galite pakeisti į **(1 + 4) / 2**. Jei aiškiai nenurodote išraiškoje atliekamų operacijų tvarkos, ji nustatoma pagal numatytąją pirmenybę, kuri priskiriama palaikomiems operatoriams. Tolesnėje lentelėje parodyta pirmenybė, priskirta kiekvienam operatoriui. Aukštesnę pirmenybę (pvz., 7) turintys operatoriai vertinami prieš žemesnę pirmenybę (pvz., 1) turinčius operatorius.

| Pirmumas | Operatoriai      | Sintaksė                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Grupavimas       | ( … )                                                                   |
| 6          | Nario prieiga  | … . …                                                                   |
| 5          | Funkcijos iškvietimas  | … ( … )                                                                 |
| 4          | Dauginamasis | … \* …<br>… / …                                                         |
| 3          | Priedas       | … + …<br>… - …                                                          |
| 2          | Palyginimas     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Atskyrimas     | … , …                                                                   |

Jei išraiškoje iš eilės yra keli operatoriai, turintys tokią pačią pirmenybę, operacijos vertinamos iš kairės į dešinę. Pvz., išraiška **1 + 6 / 2 \* 3 &gt; 5** pateikia reikšmę **true**. Aiškiai nurodyti norimą išraiškų vertinimo tvarką rekomenduojame naudojant skliaustus, kad išraiškas būtų lengviau skaityti ir tvarkyti.

#### <a name="references"></a>Nuorodos

Visi dabartinio ER komponento duomenų šaltiniai, kurie yra pasiekiami kuriant išraišką, gali būti naudojami kaip įvardytosios nuorodos. (Dabartinis ER komponentas gali būti modelis arba formatas.) Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **ReportingDate**, kuris pateikia duomenų tipo **DATETIME** reikšmę. Norint, kad reikšmė generuojamame dokumente būtų pateikiama tinkamai suformatuota, išraiškoje duomenų šaltinį galima nurodyti tokį: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**.

Prieš visus nuorodos duomenų šaltinio pavadinime esančius simbolius, kurie nėra abėcėlės raidė, turi būti padėtas viengubos kabutės ženklas ('). Jei nuorodos duomenų šaltinio pavadinime yra bent vienas simbolis, kuris nėra abėcėlės raidė, pavadinimas turi būti išskiriamas viengubomis kabutėmis. (Pavyzdžiui, šie neabėcėliniai simboliai gali būti skyrybos ženklai arba kiti rašytiniai simboliai). Toliau pateikiama keletas pavyzdžių.

- Duomenų šaltinis **Today's date & time** ER išraiškoje turi būti nurodytas taip: **'Today''s date & time'**.
- Duomenų šaltinio **Klientai** metodas **name()** ER išraiškoje turi būti nurodytas taip: **Customers.'name()'**.

Jei „Finance and Operations“ duomenų šaltinių metodai turi parametrų, šie metodai iškviečiami naudojant tolesnę sintaksę.

- Jei duomenų šaltinio **Sistema** metodas **isLanguageRTL** turi duomenų tipo **Eilutė** parametrą **EN-US**, šis metodas ER išraiškoje turi būti nurodytas kaip **System.'isLanguageRTL'("EN-US")**.
- Kai metodo pavadinimą sudaro tik raidiniai ir skaitiniai simboliai, kabutės neprivalomos. Tačiau jos būtinos lentelės metodo atveju, jei pavadinime yra skliaustai.

Prie ER susiejimo, kuris nurodo „Finance and Operations“ programos klasę **Visuotinė**, pridėjus duomenų šaltinį **Sistema**, išraiška pateikia Būlio logikos reikšmę **FALSE**. Modifikuotoji išraiška **System.' isLanguageRTL'("AR")** pateikia Būlio logikos reikšmę **TRUE**.

Galite riboti tai, kaip reikšmės perduodamos šio tipo metodo parametrams.

- Šio tipo metodams galima perduoti tik konstantas. Konstantų reikšmės apibrėžiamos kūrimo metu.
- Tokie parametrai palaiko tik nesudėtingus (pagrindinius) duomenų tipus. (Nesudėtingi duomenų tipai yra sveikasis skaičius, realusis skaičius, Būlio logika, eilutė ir t. t.).

#### <a name="paths"></a>Keliai

Kai išraiška nurodo susistemintų duomenų šaltinį, galite naudoti kelio aprašą, kad pasirinktumėte konkretų nesudėtingą duomenų šaltinio elementą. Taško simbolis (.) naudojamas atskiriant atskirus susistemintų duomenų šaltinio elementus. Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **InvoiceTransactions**, kuris pateikia įrašų sąrašą. **InvoiceTransactions** įrašo struktūroje yra laukai **AmountDebit** ir **AmountCredit**, kurie abu pateikia skaitines reikšmes. Todėl SF sumą galite apskaičiuoti sukūrę tokią išraišką: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>Funkcijos

Kitame skyriuje aprašomos funkcijos, kurias galima naudoti ER išraiškose. Visi išraiškos konteksto (esamo ER duomenų modelio arba ER formato) duomenų šaltiniai pagal iškvietimo funkcijų argumentų sąrašą gali būti naudojamos kaip iškvietimo funkcijų parametrai. Kaip iškvietimo funkcijos parametrus taip pat galima naudoti konstantas. Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **InvoiceTransactions**, kuris pateikia įrašų sąrašą. **InvoiceTransactions** įrašo struktūroje yra laukai **AmountDebit** ir **AmountCredit**, kurie abu pateikia skaitines reikšmes. Dėl to, kad apskaičiuotumėte SF sumą, galite sukurti tokią išraišką, kuri naudoja įtaisytąją ER apvalinimo funkciją: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Palaikomos funkcijos

Toliau pateikiamose lentelėse aprašomos duomenų tvarkymo funkcijos, kurias galite naudoti ER duomenų modeliams ir ER ataskaitoms kurti. Funkcijų sąrašas nėra galutinis. Programuotojai gali jį papildyti. Norėdami matyti galimų naudoti funkcijų sąrašą, ER formulių dizaino įrankyje atidarykite funkcijų sritį.

### <a name="date-and-time-functions"></a>Datos ir laiko funkcijos

| Funkcija | Prekės/Paslaugos pavadinimas | Pavyzdys |
|----------|-------------|---------|
| ADDDAYS (data ir laikas, dienos) | Į nurodytą datos / laiko reikšmę įtraukti nurodytą dienų skaičių. | **ADDDAYS (NOW(), 7)** nukelia datą ir laiką septyniomis dienomis į ateitį. |
| DATETODATETIME (data) | Nurodytą datos reikšmę konvertuoti į datos / laiko reikšmę. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** pateikia dabartinio „Finance and Operations” seanso datą – 2015 m. gruodžio 24 d. – kaip **2015-12-24 00:00:00**. Šiame pavyzdyje **CompInfo** yra **„Finance and Operations“ / lentelės** tipo ER duomenų šaltinis, nurodantis lentelę CompanyInfo. |
| NOW () | Pateikti dabartinę „Finance and Operations“ programos serverio datą ir laiką kaip datos / laiko reikšmę. | |
| TODAY () | Pateikti dabartinę „Finance and Operations“ programos serverio datą kaip datos reikšmę. | |
| NULLDATE () | Pateikti **neapibrėžtą** datos reikšmę. | |
| NULLDATETIME () | Pateikti **neapibrėžtą** datos / laiko reikšmę. | |
| DATETIMEFORMAT (data ir laikas, formatas) | Konvertuoti nurodytą datos / laiko reikšmę į nurodyto formato eilutę. (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), „mmmm-MM-dd“)** pateikia dabartinio „Finance and Operations“ programos seanso datą – 2015 m. gruodžio 24 d. – kaip **„2015-12-24“** pagal nurodytą pasirinktinį formatą. |
| DATETIMEFORMAT (data ir laikas, formatas, principas) | Konvertuoti nurodytą datos / laiko reikšmę į nurodyto formato eilutę ir [kultūrą](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (NOW(), „d“, „de“)** pateikia dabartinio „Finance and Operations“ programos serverio datą – 2015 m. gruodžio 24 d. – kaip **„24.12.2015“** pagal pasirinktą vokišką kultūrą. |
| SESSIONTODAY () | Pateikti dabartinę „Finance and Operations“ seanso datą kaip datos reikšmę. | |
| SESSIONNOW () | Pateikti dabartinę „Finance and Operations“ seanso datą ir laiką kaip datos / laiko reikšmę. | |
| DATEFORMAT (data, formatas) | Pateikti nurodytos datos eilutę nurodytu formatu. | **DATEFORMAT (SESSIONTODAY (), "mmmm-MM-dd“)** pateikia dabartinio „Finance and Operations“ seanso datą – 2015 m. gruodžio 24 d. – kaip **„2015-12-24“** pagal nurodytą pasirinktinį formatą. |
| DATEFORMAT (data, formatas, principas) | Konvertuokite nurodytą datos reikšmę į nurodyto formato eilutę ir [principą](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (SESSIONNOW (), „d“, „de“)** pateikia dabartinio „Finance and Operations“ seanso datą – 2015 m. gruodžio 24 d. – kaip **„24.12.2015“** pagal pasirinktą vokišką kultūrą. |
| DAYOFYEAR (data) | Pateikti dienų nuo sausio 1 d. iki nurodytos datos sveikąjį skaičių. | **DAYOFYEAR (DATEVALUE („2016-03-01“, „mmmm-MM-dd“))** pateikia **61**. **DAYOFYEAR (DATEVALUE („2016-01-01“, „mmmm-MM-dd“))** pateikia **1**. |
| DAYS (1 data, 2 data) | Pateikti dienų tarp pirmosios nurodytos datos ir antrosios nurodytos dienos skaičių. Kai pirmoji data yra vėlesnė nei antroji, pateikti teigiamą reikšmę, kai pirmoji data sutampa su antrąja, pateikti **0** (nulį), kitu atveju pateikti neigiamą reikšmę. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** pateikia **-1**. |

### <a name="data-conversion-functions"></a>Duomenų konvertavimo funkcijos

| Funkcija | aprašymas | Pavyzdys |
|----------|-------------|---------|
| DATETODATETIME (data) | Nurodytą datos reikšmę konvertuoti į datos / laiko reikšmę. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** pateikia dabartinio „Finance and Operations” seanso datą – 2015 m. gruodžio 24 d. – kaip **2015-12-24 00:00:00**. Šiame pavyzdyje **CompInfo** yra **„Finance and Operations“ / lentelės** tipo ER duomenų šaltinis, nurodantis lentelę CompanyInfo. |
| DATEVALUE (eilutė, formatas) | Pateikti nurodytos eilutės datą nurodytu formatu. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** pateikia datą (2016 m. gruodžio 21 d.) pagal nurodytą pasirinktinį formatą ir numatytosios programos **EN-US** kultūrą. |
| DATEVALUE (eilutė, formatas, principas) | Pateikti nurodytos eilutės datą nurodytu formatu ir kultūra. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** pateikia datą (2016 m. sausio 21 d.) pagal nurodytą pasirinktinį formatą ir kultūrą. Tačiau **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** pateiks išimtį, kad informuotų vartotoją, jog nurodyta eilutė nėra atpažįstama kaip tinkama data. |
| DATETIMEVALUE (eilutė, formatas) | Pateikti nurodytos eilutės datą / laiką nurodytu formatu. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** pateikia 2016 m. gruodžio 21 d. 2:55:00 AM pagal nurodytą pasirinktinį formatą ir numatytosios programos **EN-US** kultūrą. |
| DATETIMEVALUE (eilutė, formatas, principas) | Pateikti nurodytos eilutės datą / laiką nurodytu formatu ir kultūra. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** pateikia 2016 m. gruodžio 21 d. 2:55:00 AM pagal nurodytą pasirinktinį formatą ir kultūrą. Tačiau **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** pateiks išimtį, kad informuotų vartotoją, jog nurodyta eilutė nėra atpažįstama kaip tinkama data / laikas. |

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
<td>Tolesnėje iliustracijoje duomenų šaltinis <strong>Eilutės</strong> sukurtas kaip trijų įrašų sąrašas. Šis sąrašas suskirstytas į paketus, iš kurių kiekviename yra iki dviejų įrašų.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Tolesnėje iliustracijoje parodytas sukurtas formato maketas. Šiame formato makete sukuriami susiejimai su duomenų šaltiniu <strong>Eilutės</strong>, siekiant generuoti išeigą XML formatu. Ši išeiga pateikia atskirus kiekvieno paketo ir jame esančių įrašų mazgus.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (1 įrašas [, 2 įrašas, ...])</td>
<td>Pateikti naują sąrašą, sukurtą iš nurodytų argumentų.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> pateikia tuščią įrašą, kur laukų sąraše yra visi <strong>MainData</strong> ir <strong>OtherData</strong> įrašų sąrašų laukai.</td>
</tr>
<tr class="even">
<td>LISTJOIN (1 sąrašas, 2 sąrašas, …)</td>
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
<td>Pateikti naują lygųjį sąrašą, kuriame nurodomi visi elementai, atitinkantys nurodytą kelią. Kelias turi būti nurodytas kaip tinkamas duomenų šaltinio kelias į įrašų sąrašo duomenų tipo duomenų šaltinio elementą. Duomenų elementai, pvz., kelio eilutė ir data, kūrimo metu ER išraiškų daryklėje turėtų pateikti klaidą.</td>
<td>Jei kaip duomenų šaltinį (DS) įvesite <strong>SPLIT(&quot;abcdef&quot; , 2)</strong>,<strong>COUNT( ALLITEMS (DS.Value))</strong> pateikia <strong>3</strong>.</td>
</tr>
<tr class="odd">
<td>ORDERBY (sąrašas [, 1 išraiška, 2 išraiška, ...])</td>
<td>Pateikti nurodytą sąrašą, surūšiuotą pagal nurodytus argumentus. Šiuos argumentus galima apibrėžti kaip išraiškas.</td>
<td>Jei <strong>Tiekėjas </strong>sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, <strong>ORDERBY (Vendors, Vendors.&#39;name()&#39;)</strong> pateikia tiekėjų sąrašą, surūšiuotą pagal pavadinimą didėjančia tvarka.</td>
</tr>
<tr class="even">
<td>REVERSE (sąrašas)</td>
<td>Pateikti nurodytą sąrašą atvirkštine rūšiavimo tvarka.</td>
<td>Jei <strong>Tiekėjas</strong> sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, <strong>REVERSE (ORDERBY (Vendors, Vendors.&#39;name()&#39;)) )</strong> pateikia tiekėjų sąrašą, surūšiuotą pagal pavadinimą mažėjančia tvarka.</td>
</tr>
<tr class="odd">
<td>WHERE (sąrašas, sąlyga)</td>
<td>Pateikti nurodytą sąrašą, filtruotą pagal nurodytą sąlygą. Nurodyta sąlyga yra taikoma sąrašui atmintyje. Taip funkcija <strong>WHERE</strong> skiriasi nuo funkcijos <strong>FILTER</strong>.</td>
<td>Jei <strong>Tiekėjas</strong> sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> pateikia tik tų tiekėjų, kurie priklauso 40 tiekėjų grupei, sąrašą.</td>
</tr>
<tr class="even">
<td>ENUMERATE (sąrašas)</td>
<td>Pateikti naują sąrašą, sudarytą iš išvardytų nurodyto sąrašo įrašų ir parodantį šiuos elementus:
<ul>
<li>nurodytus sąrašo įrašus kaip įprastus sąrašus (<strong>Vertės </strong>komponentas);</li>
<li>dabartinio įrašo indeksą (<strong>Numerio </strong>komponentas).</li>
</ul></td>
<td>Tolesnėje iliustracijoje duomenų šaltinis <strong>Išvardytas</strong> sukurtas kaip išvardytas tiekėjo įrašų sąrašas iš duomenų šaltinio <strong>Tiekėjai</strong>, kuris nurodo lentelę VendTable.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Tolesnėje iliustracijoje parodytas formatas. Šiame formate sukuriami duomenų susiejimai, siekiant generuoti išeigą XML formatu. Ši išeiga atskirus tiekėjus pateikia kaip išvardytus mazgus.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (sąrašas)</td>
<td>Pateikti nurodytame sąraše esančių įrašų skaičių, jei sąrašas nėra tuščias. Kitu atveju pateikti <strong>0</strong> (nulis).</td>
<td><strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> pateikia <strong>2</strong>, nes funkcija <strong>SPLIT</strong> sukuria sąrašą, kurį sudaro du įrašai.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (kelias)</td>
<td>Pateikti įrašų sąrašą, sukurtą naudojant vieną iš toliau nurodytų tipų argumentų.
<ul>
<li>Modelių išvardijimas</li>
<li>Formatų išvardijimas</li>
<li>Konteineris</li>
</ul>
<p>Sukurtą sąrašą sudaro įrašai su tolesniais laukais.</p>
<ul>
<li>Vardas ir (arba) pavardė</li>
<li>Etiketė</li>
<li>aprašymas</li>
</ul>
Vykdymo metu laukuose <strong>Žyma</strong> ir <strong>Aprašas</strong> pateikiamos reikšmės pagal formato kalbos parametrus.</td>
<td>Tolesnėje iliustracijoje duomenų modelyje įvestas išvardijimas.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.</p>
<ul>
<li>Modelio išvardijimas įtrauktas į ataskaitą kaip duomenų šaltinis.</li>
<li>ER išraiškoje modelio išvardijimas naudojamas kaip funkcijos <strong>LISTOFFIELDS</strong> parametras.</li>
<li>Įrašų sąrašo tipo duomenų šaltinis įtrauktas į ataskaitą naudojant sukurtą ER išraišką.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Toliau pateiktame pavyzdyje parodyti ER formato elementai, susieti su įrašų sąrašo tipo duomenų šaltiniu, kuris buvo sukurtas naudojant funkciją <strong>LISTOFFIELDS</strong>.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas sukurtas formatas.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE]<br>
Pagal pirminių formato elementų FAILAS ir APLANKAS kalbos parametrus išverstas žymų ir aprašų tekstas yra įvedamas į ER formato išeigą.</blockquote></td>
</tr>
<tr class="odd">
<td>LISTOFFIELDS (kelias, kalba)</td>
<td>Pateikti įrašų sąrašą, sukurtą iš argumento, pvz., modelio išvardijimo, formato išvardijimo ar konteinerio. Sukurtą sąrašą sudaro įrašai su tolesniais laukais.
<ul>
<li>Vardas ir (arba) pavardė</li>
<li>Etiketė</li>
<li>aprašymas</li>
<li>Išversta</li>
</ul>
<p>Vykdymo metu laukuose <strong>Žyma</strong> ir <strong>Aprašas</strong> pateikiamos reikšmės pagal formato kalbos parametrus ir nurodytą kalbą. Laukas <strong>Išversta</strong> rodo, kad laukas <strong>Žyma</strong> išverstas į nurodytą kalbą.</td>
<td>Pavyzdžiui, duomenų šaltinio tipas <strong>Apskaičiuotasis laukas</strong> naudojamas konfigūruoti duomenų modelio išvardijimo <strong>enumType</strong> duomenų šaltinius <strong>enumType_de</strong> ir <strong>enumType_deCH</strong>:
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
Tokiu atveju, norėdami gauti išvardijimo reikšmės žymą Šveicarijos vokiečių kalba (jei šis vertimas yra), galite naudoti tolesnę išraišką. Jei vertimo Šveicarijos vokiečių kalba nėra, žyma pateikiama vokiečių kalba: <strong>IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)</strong>.</td>
</tr>
<tr class="even">
<td>STRINGJOIN (sąrašas, lauko pavadinimas, skyriklis)</td>
<td>Pateikti eilutę, kurią sudaro sujungtos nurodyto lauko, esančio nurodytame sąraše, reikšmės. Reikšmes skiria nurodytas skyriklis.</td>

<td>Jei kaip duomenų šaltinį įvedate <strong>SPLIT(&quot;abc&quot; , 1)</strong>, išraiška <strong>STRINGJOIN (DS, DS.Value, &quot;:&quot;)</strong> pateikia <strong>&quot;a</strong><strong>:b</strong><strong>:c&quot;</strong>.</td>

</tr>
<tr class="odd">
<td>SPLITLISTBYLIMIT (sąrašas, ribinė reikšmė, ribos šaltinis)</td>
<td>Nurodytą sąrašą padalyti į naują antrinių sąrašų sąrašą ir pateikti rezultatą įrašų sąrašo turinyje. Ribinės reikšmės parametras nustato ribos reikšmę, taikomą dalijant pradinį sąrašą. Ribos šaltinio parametras nustato veiksmą, kurį atliekant bendra suma didėja. Riba netaikoma vienam pradinio sąrašo elementui, jei ribos šaltinis viršija nustatytą ribą.</td>
<td>Tolesnėse iliustracijose parodytas formatas ir naudojami jo duomenų šaltiniai. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas formatas. Šiuo atveju išeiga yra standartinis prekių sąrašas.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>Toliau pateiktose iliustracijose rodomas tas pats formatas, pakoreguotas norint pateikti prekių sąrašą paketais, kai viename pakete turi būti prekės, o bendrasis svoris negali viršyti ribos 9.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Tolesnėje iliustracijoje parodytas vaizdas, kai vykdomas pakoreguotas formatas.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE]<br>
Riba nėra taikoma paskutinei pradinio sąrašo prekei, nes ribos šaltinio (svorio) reikšmė (11) viršija nustatytą ribą (9). Naudokite funkciją <strong>WHERE</strong> arba atitinkamo formato elemento išraišką <strong>Įjungta</strong>, norėdami nepaisyti (praleisti) antrinių sąrašų generuojant ataskaitą (pagal poreikį).</blockquote></td>
</tr>
<tr class="even">
<td>FILTER (sąrašas, sąlyga)</td>
<td>Pateikti nurodytą sąrašą, kai užklausa modifikuota filtruoti pagal nurodytą sąlygą. Ši funkcija skiriasi nuo funkcijos <strong>WHERE</strong>, nes nurodyta sąlyga duomenų bazės lygiu taikoma bet kuriam ER duomenų šaltiniui, kurio tipas – <strong>Lentelės įrašai</strong>. Sąrašą ir sąlygas galima nustatyti naudojant lenteles ir ryšius.</td>
  <td>Jei <strong>Tiekėjas</strong> sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę VendTable, <strong>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong> pateikia tik tų tiekėjų, kurie priklauso 40 tiekėjų grupei, sąrašą. Jei <strong>Tiekėjas</strong> sukonfigūruotas kaip ER duomenų šaltinis, nurodantis lentelę <strong>VendTable</strong>, ir <strong>parmVendorBankGroup</strong>, sukonfigūruotas kaip ER duomenų šaltinis, pateikia eilutės duomenų tipo reikšmę, <strong>FILTER (Vendor.&#39;&lt;Relations&#39;.VendBankAccount, Vendor.&#39;&lt;Relations&#39;.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> pateikia tik konkrečiai bankų grupei priklausančių tiekėjų sąskaitų sąrašą.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loginės funkcijos

| Funkcija | aprašymas | Pavyzdys |
|----------|-------------|---------|
| CASE (išraiška, 1 parinktis, 1 rezultatas \[, 2 parinktis, 2 rezultatas\] … \[, numatytasis rezultatas\]) | Įvertinti nurodytą išraiškos reikšmę pagal nurodytas alternatyvias parinktis. Pateikti parinkties rezultatą, kuris yra lygus išraiškos reikšmei. Kitu atveju pateikti pasirenkamą numatytąjį rezultatą, jei numatytasis rezultatas nurodytas. (Numatytasis rezultatas yra paskutinis parametras, prieš kurį nėra parinkties.) | **CASE( DATETIMEFORMAT( NOW(), „MM“), „10“, „ŽIEMA“, „11“, „ŽIEMA“, „12“, „ŽIEMA“, „“)** pateikia eilutę **„ŽIEMA“**, kai dabartinio „Finance and Operations“ seanso data yra tarp spalio ir gruodžio mėn. Kitu atveju pateikia tuščią eilutę. |
| IF (sąlyga, 1 reikšmė, 2 reikšmė) | Pateikti pirmą nurodytą reikšmę, kai išpildoma nurodyta sąlyga. Kitu atveju pateikti antrą nurodytą reikšmę. Jei 1 ir 2 reikšmės yra įrašai ar įrašų sąrašai, rezultatas pateikia tik abiejuose sąrašuose esančius laukelius. | **IF (1 = 2, „sąlyga išpildyta“, „sąlyga neišpildyta“)** pateikia eilutę **„sąlyga neišpildyta“**. |
| NOT (sąlyga) | Pateikti atšauktą nurodytos sąlygos loginę reikšmę. | **NOT (TRUE)** pateikia **FALSE**. |
| AND (1 sąlyga\[, 2 sąlyga, …\]) | Pateikti **TRUE**, jei *visos* nurodytos sąlygos teisingos. Kitu atveju pateikti **FALSE**. | **AND (1=1, „a“=„a“)** pateikia **TRUE**. **AND (1=2, „a“=„a“)** pateikia **FALSE**. |
| OR (1 sąlyga\[, 2 sąlyga, …\]) | Pateikti **FALSE**, jei *visos* nurodytos sąlygos klaidingos. Pateikti **TRUE**, jei *bet kuri iš* nurodytų sąlygų yra teisinga. | **OR (1=2, „a“=„a“)** pateikia **TRUE**. |

### <a name="mathematical-functions"></a>Matematinės funkcijos

| Funkcija | Prekės/Paslaugos pavadinimas | Pavyzdys |
|----------|-------------|---------|
| ABS (skaičius) | Pateikti absoliučiąją nurodyto skaičiaus reikšmę. (Kitaip tariant, pateikti skaičių be ženklo). | **ABS (-1)** pateikia **1**. |
| POWER (skaičius, kėlimas laipsniu) | Pateikti nurodyto teigiamo skaičiaus kėlimo nurodytu laipsniu rezultatą. | **POWER (10, 2)** pateikia **100**. |
| NUMBERVALUE (eilutė, dešimtainis skyriklis, skaitmenų grupės skyriklis) | Konvertuoti nurodytą eilutę į skaičių. Nurodytas dešimtainis skyriklis naudojamas tarp dešimtainio skaičiaus sveikojo skaičiaus ir trupmeninės dalių. Nurodytas skaitmenų grupavimo skyriklis naudojamas kaip tūkstančių skyriklis. | **NUMBERVALUE(„1 234,56“, „,“, „ “)** pateikia reikšmę **1234,56**. |
| VALUE (eilutė) | Konvertuoti nurodytą eilutę į skaičių. Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas. Pateikti išimtį, jei nurodytoje eilutėje yra kitų neskaitinių simbolių. | **VALUE („1 234,56“)** pateikia išimtį. |
| ROUND (skaičius, dešimtainės dalys) | Pateikti nurodytą skaičių, suapvalintą iki nurodyto skaičiaus po kablelio.<ul><li>Jei dešimtainių dalių parametro reikšmė yra didesnė už 0 (nulį), nurodytas skaičius apvalinamas iki tiek skaitmenų po kablelio.</li><li>Jei dešimtainių dalių parametro reikšmė yra **0** (nulis), nurodytas skaičius apvalinamas iki artimiausio sveikojo skaičiaus.</li><li>Jei dešimtainių dalių parametro reikšmė yra mažesnė už 0 (nulį), nurodytas skaičius apvalinamas į kairę nuo skaičiaus po kablelio.</li></ul> | **ROUND (1200,767, 2)** suapvalina iki dviejų skaičių po kablelio ir pateikia **1200,77**. **ROUND (1200,767, -3)** suapvalina iki artimiausio 1000 kartotinio ir pateikia **1000**. |
| ROUNDDOWN (skaičius, dešimtainės dalys) | Pateikti nurodytą skaičių, suapvalintą žemyn iki nurodyto skaičiaus po kablelio.<blockquote>[!NOTE]<br>Ši funkcija veikia kaip ir <strong>ROUND</strong>, bet ji visada apvalina nurodytą skaičių į mažesnę pusę (link nulio).</blockquote> | **ROUNDDOWN (1200,767, 2)** suapvalina į mažesnę pusę iki dviejų skaičių po kablelio ir pateikia **1200,76**. **ROUNDDOWN (1700,767, -3)** suapvalina į mažesnę pusę iki artimiausio 1,000 kartotinio ir pateikia **1000**. |
| ROUNDUP (skaičius, dešimtainės dalys) | Pateikti nurodytą skaičių, suapvalintą aukštyn iki nurodyto skaičiaus po kablelio.<blockquote>[!NOTE]<br>Ši funkcija veikia kaip ir <strong>ROUND</strong>, bet ji visada apvalina nurodytą skaičių į didesnę pusę (nuo nulio).</blockquote> | **ROUNDUP (1200,763, 2)** suapvalina į didesnę pusę iki dviejų skaičių po kablelio ir pateikia **1200,77**. **ROUNDUP (1200,767, -3)** suapvalina į didesnę pusę iki artimiausio 1,000 kartotinio ir pateikia **2000**. |

### <a name="data-conversion-functions"></a>Duomenų konvertavimo funkcijos

| Funkcija | aprašymas | Pavyzdys |
|----------|-------------|---------|
| VALUE (eilutė) | Konvertuoti nurodytą eilutę į skaičių. Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas. Pateikti išimtį, jei nurodytoje eilutėje yra kitų neskaitinių simbolių. | **VALUE („1 234,56“)** pateikia išimtį. |
| NUMBERVALUE (eilutė, dešimtainis skyriklis, skaitmenų grupės skyriklis) | Konvertuoti nurodytą eilutę į skaičių. Nurodytas dešimtainis skyriklis naudojamas tarp dešimtainio skaičiaus sveikojo skaičiaus ir trupmeninės dalių. Nurodytas skaitmenų grupavimo skyriklis naudojamas kaip tūkstančių skyriklis. | **NUMBERVALUE("1 234,56", ",", " ")** pateikia **1234.56**. |
| INTVALUE (eilutė) | Pateikti nurodytą eilutę sveikuoju skaičiumi. Visi skaičiai po kablelio pašalinami. | **INTVALUE ("100.77")** pateikia **100**. |
| INTVALUE (numeris) | Pateikti nurodytą skaičių sveikuoju skaičiumi. Visi skaičiai po kablelio pašalinami. | **INTVALUE (-100,77)** pateikia **-100**. |
| INT64VALUE (eilutė) | Pateikti nurodytą eilutę int64 išraiška. Visi skaičiai po kablelio pašalinami. | **INT64VALUE ("22565422744")** pateikia **22565422744**. |
| INT64VALUE (skaičius) | Pateikti nurodytą skaičių int64 išraiška. Visi skaičiai po kablelio pašalinami. | **INT64VALUE (22565422744,00)** pateikia **22565422744**. |

### <a name="record-functions"></a>Įrašo funkcijos

| Funkcija | aprašymas | Pavyzdys |
|----------|-------------|---------|
| NULLCONTAINER (sąrašas) | Pateikti **neapibrėžtą** įrašą, kuris turi tokią pačią struktūrą, kaip ir nurodytas įrašų sąrašas arba įrašas.<blockquote>[!NOTE]<br>Ši funkcija nebenaudojama. Vietoje jos naudokite <strong>EMPTYRECORD</strong>.</blockquote> | **NULLCONTAINER (SPLIT („abc“, 1))** pateikia naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį pateikia funkcija **SPLIT**. |
| EMPTYRECORD (įrašas) | Pateikti **neapibrėžtą** įrašą, kuris turi tokią pačią struktūrą, kaip ir nurodytas įrašų sąrašas arba įrašas.<blockquote>[!NOTE]<br><strong>Neapibrėžtas</strong> įrašas yra toks, kurio visų laukų reikšmės yra tuščios. Tuščia skaičių reikšmė yra <strong>0</strong> (nulis), eilučių – tuščia eilutė ir t. t.</blockquote> | **EMPTYRECORD (SPLIT („abc“, 1))** pateikia naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį pateikia funkcija **SPLIT**. |

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
<th>aprašymas</th>
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
<td><strong>CHAR (255)</strong> pateikia <strong>&quot;ÿ&quot;</strong>.
<blockquote>[!NOTE]<br>
Šios funkcijos pateikta eilutė priklauso nuo kodavimo, kuris pažymėtas pirminiame formato FAILAS elemente. Norėdami matyti palaikomų kodavimų sąrašą, žr. <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodavimo klasė</a>.</blockquote>
</td>
</tr>
<tr class="even">
<td>CONCATENATE (1 eilutė [, 2 eilutė, ...])</td>
<td>Pateikti visas nurodytas teksto eilutes, sujungtas į vieną eilutę.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong> pateikia <strong>&quot;abcdef&quot;</strong>.
<blockquote>[!NOTE]<br>
Išraiška <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> taip pat pateikia <strong>&quot;abcdef&quot;</strong>.</blockquote>
</td>
</tr>
<tr class="odd">
<td>TRANSLATE (eilutė, šablonas, pakeitimas)</td>
<td>Pateikti nurodytą eilutę, kai visi simboliai, atitinkantys nurodytą šabloną, pakeisti atitinkamose kitos nurodytos eilutės vietose esančiais simboliais.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> pakeičia simbolius <strong>&quot;cd&quot;</strong> eilute <strong>&quot;GH&quot;</strong> ir pateikia <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (eilutė, šablonas, pakeitimas, įprastos išraiškos žymė)</td>
<td>Kai nurodyta reguliariosios išraiškos žymė yra <strong>true</strong>, pateikti nurodytą eilutę, modifikuotą pritaikant reguliariąją išraišką, nurodytą kaip šios funkcijos argumento šablonas. Ši išraiška naudojama ieškant simbolių, kuriuos reikia pakeisti. Rasti simboliai pakeičiami nurodyto pakeitimo argumento simboliais. Kai nurodyta įprastos išraiškos žymė yra <strong>klaidinga</strong>, ši funkcija veikia kaip <strong>TRANSLATE</strong>.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> pritaiko įprastą išraišką, kuri pašalina visus neskaitinius simbolius ir pateikia <strong>&quot;19234564971&quot;</strong>. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, false)</strong> pakeičia simbolius <strong>&quot;cd&quot;</strong> eilute <strong>&quot;GH&quot;</strong> ir pateikia <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (įvestis)</td>
<td>Pateikti nurodytą įvestį, konvertuotą į teksto eilutę, kuri formatuojama pagal dabartinio „Finance and Operations“ egzemplioriaus serverio lokalės parametrus. <strong>Realaus skaičiaus</strong> tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.</td>
<td>Jei „Finance and Operations“ egzemplioriaus serverio vieta apibrėžiama kaip <strong>EN-US</strong>, <strong>TEXT (NOW ())</strong> pateikia dabartinio „Finance and Operations“ seanso datą – 2015 m. gruodžio 17 d. – kaip teksto eilutę <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEXT (1/3)</strong> pateikia <strong>&quot;0.33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (1 eilutė, 2 eilutė[, 3 eilutė, …])</td>
<td>Pateikti nurodytą eilutę, suformatuotą pakeičiant visus <strong>%N</strong> pasikartojimus <em>-uoju</em> argumentu. Argumentai yra eilutės. Jei nėra pateiktas parametro argumentas, parametras eilutėje pateikiamas kaip <strong>&quot;%N&quot;</strong>. <strong>Realaus skaičiaus</strong> tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.</td>
<td>Tolesnėje iliustracijoje duomenų šaltinis <strong>PaymentModel</strong> pateikia klientų įrašus komponente <strong>Klientas</strong> ir apdorojimo datos reikšmę lauke <strong>ProcessingDate</strong>.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>ER formate, skirtame generuoti elektroninį failą pasirinktiems klientams, <strong>PaymentModel</strong> yra pasirinktas kaip duomenų šaltinis ir kontroliuoja proceso eigą. Pateikiama išimtis, informuojanti vartotoją, kai pasirinktas klientas sustabdomas ataskaitos apdorojimo dieną. Formulė, sukurta šio tipo apdorojimo kontrolei, gali naudoti tokius išteklius:</p>
<ul>
<li>„Finance and Operations“ žymė SYS70894, kur nurodytas toks tekstas:
<ul>
<li><strong>EN-US kalba:</strong> &quot;Nothing to print&quot;</li>
<li><strong>DE kalba:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>„Finance and Operations“ žymė SYS18389, kur nurodytas toks tekstas:
<ul>
<li><strong>EN-US kalba:</strong> &quot;Customer %1 is stopped for %2.&quot;</li>
<li><strong>DE kalba:</strong> &quot;Debitor &#39;%1&#39; wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Tai yra formulė, kurią galima kurti.</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Jei ataskaita apdorojama klientui <strong>„Litware Retail“</strong> 2015 m. gruodžio 17 d., pagal <strong>EN-US</strong> kultūrą ir <strong>EN-US</strong> kalbą, ši formulė pateikia tokį tekstą, kuris galutiniam vartotojui gali būti pateiktas kaip tolesnis išimties pranešimas.</p>
<p>&quot;Nėra ką spausdinti. Customer Litware Retail is stopped for 12/17/2015.&quot;</p>
<p>Jei ta pati ataskaita apdorojama klientui <strong>„Litware Retail“</strong> 2015 m. gruodžio 17 d. pagal <strong>DE</strong> kultūrą ir <strong>DE</strong> kalbą, ši formulė pateikia tokį tekstą, kuris naudoja toliau nurodytą kitokį datos formatą.</p>
<p>&quot;Nichts zu drucken. Debitor &#39;Litware Retail&#39; wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE]<br>
ER formulėse žymoms taikoma tokia sintaksė:
<ul>
<li><strong>Žymėms iš „Finance and Operations“ išteklių:</strong> <strong>@&quot;X&quot;</strong>, kur X yra žymės ID programos objektų medyje (AOT)</li>
<li><strong>ER konfigūracijose esančioms žymėms:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, kur X yra žymės ID ER konfigūracijoje.</li>
</ul></blockquote></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (skaičius, formatas)</td>
<td>Pateikti nurodyto skaičiaus eilutę nurodytu formatu. (Daugiau informacijos apie palaikomus formatus rasite čia: <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standartinis</a> ir <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">pasirinktinis</a>.) Kontekstas, kuriame vykdome ši funkcija, nulemia, kokiu principu bus formatuojami skaičiai.</td>
<td>Pagal LT principą <strong>NUMBERFORMAT (0,45, &quot;p&quot;)</strong> pateikia <strong>&quot;45.00 %&quot;</strong>. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong> pateikia <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (numeris, kalba, valiuta, spausdinimo valiutos pavadinimo žymė, dešimtainiai skaičiai)</td>
<td>Pateikti nurodytą skaičių, užrašytą žodžiais (konvertuotą) nurodytos kalbos teksto eilutėse. Kalbos kodas nėra būtinas. Kai jis nurodytas kaip tuščia eilutė, naudojamas vykdomo konteksto kalbos kodas. (Vykdomo konteksto kalbos kodas nustatomas generuojamam aplankui arba failui). Valiutos kodas taip pat nėra būtinas. Kai jis nustatytas kaip tuščia eilutė, naudojama įmonės valiuta.
<blockquote>[!NOTE]<br>
Analizuojami tik šių kalbos kodų spausdinimo valiutos pavadinimo žymė ir dešimtainių dalių parametrai: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> ir<strong>RU</strong>. Be to, spausdinimo valiutos žymės parametras analizuojamas tik „Finance and Operations“ įmonėms, kurių šalies are regiono kontekste palaikomas valiutos pavadinimų linksniavimas.</blockquote></td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> pateikia <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong>. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> pateikia <strong>&quot;Sto dwadzieścia&quot;</strong>. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> pateikia <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>PADLEFT (eilutė, ilgis, užpildymo simboliai)</td>
<td>Pateikti nurodyto ilgio eilutę, kurioje eilutės pradžia užpildyta nurodytais simboliais.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> pateikia teksto eilutę <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong>.</td>
</tr>
<tr class="even">
<td>TRIM (eilutė)</td>
<td>Pateikti nurodytą teksto eilutę, sutrumpinus priekinius ir galinius tarpus bei pašalinus kelis tarpus tarp žodžių iki vieno.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Teksto&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;pavyzdys&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong> pateikia <strong>&quot;Teksto pavyzdys&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>GETENUMVALUEBYNAME (išvardijimo duomenų šaltinio kelias, išvardijimo reikšmės žymės tekstas)</td>
<td>Pateikti nurodyto išvardijimo duomenų šaltinio reikšmę pagal nurodytą išvardijimo žymos tekstą.</td>
<td>Tolesnėje iliustracijoje duomenų modelyje įvestas išvardijimas <strong>ReportDirection</strong>. Atkreipkite dėmesį, kad išvardijimo reikšmėms nurodytos žymės.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Tolesnėje iliustracijoje parodyta tolesnė išsami informacija.</p>
<ul>
<li>Modelio išvardijimas <strong>ReportDirection</strong> įtrauktas į ataskaitą kaip duomenų šaltinis <strong>$Direction</strong>.</li>
<li>ER išraiška <strong>$IsArrivals</strong> sukurta naudoti modelio išvardijimą kaip šios funkcijos parametrą. Šios išraiškos reikšmė yra <strong>TRUE</strong>.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Duomenų konvertavimo funkcijos

| Funkcija | aprašymas | Pavyzdys |
|----------|-------------|---------|
| TEXT (įvestis) | Pateikti nurodytą įvestį, konvertuotą į teksto eilutę, kuri formatuojama pagal dabartinio „Finance and Operations“ egzemplioriaus serverio lokalės parametrus. **Realaus skaičiaus** tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio. | Jei „Finance and Operations“ egzemplioriaus serverio lokalė apibrėžiama kaip **EN-US**, **TEXT (NOW ())** pateikia dabartinio „Finance and Operations“ seanso datą – 2015 m. gruodžio 17 d. – kaip teksto eilutę **"12/17/2015 07:59:23 AM"**. **TEXT (1/3)** pateikia **„0,33“**. |
| QRCODE (eilutė) | Pateikti nurodytos eilutės QR kodo vaizdą dvejetainiu „base64‟ formatu. | **QRCODE ("Teksto pavyzdys")** pateikia **U2FtcGxlIHRleHQ=**. |

### <a name="data-collection-functions"></a>Duomenų rinkinio funkcijos

| Funkcija | aprašymas | Pavyzdys |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Pateikti šio formato elemento pavadinimą. Pateikti tuščią eilutę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta. | Norėdami daugiau sužinoti apie tai, kaip naudoti šią funkciją, žr. užduočių vedlį **ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant** (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis). |
| SUMIFS (rakto eilutė, skirta sumuoti, 1 kriterijų klasės eilutėje, 1 kriterijų reikšmės eilutė \[, 2 kriterijų diapazono eilutė, 2 kriterijų reikšmių eilutė, ...\]) | Pateikti XML mazgų (kurių pavadinimas apibrėžtas kaip raktas) reikšmių, kurios surinktos vykdant šį formatavimą ir kurios tenkina nurodytas sąlygas (diapazoną ir reikšmę), sumą. Pateikti **0** (nulis) reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta. | |
| SUMIF (rakto eilutė, skirta sumuoti, kriterijų diapazono eilutė, kriterijų reikšmių eilutė) | Pateikti XML mazgų (kurių pavadinimas apibrėžtas kaip raktas) reikšmių, kurios surinktos vykdant šį formatavimą ir kurios tenkina nurodytą sąlygą (diapazoną ir reikšmę), sumą. Pateikti **0** (nulis) reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta. | |
| COUNTIFS (1 kriterijų klasės eilutėje, 1 kriterijų reikšmės eilutė \[, 2 kriterijų intervalo eilutė, 2 kriterijų reikšmės eilutė, ...\]) | Pateikti XML mazgų, kurie buvo surinkti vykdant šį formatavimą ir kurie tenkina nurodytas sąlygas (diapazonų ir reikšmių poras), skaičių. Pateikti **0** (nulis) reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta. | |
| COUNTIF (kriterijų diapazono eilutė, kriterijų reikšmių eilutė) | Pateikti XML mazgų, kurie surinkti vykdant šį formatavimą ir kurie tenkina įvestą sąlygą (diapazoną ir reikšmę), skaičių. Pateikti **0** (nulis) reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta. | |
| COLLECTEDLIST (1 kriterijų klasės eilutėje, 1 kriterijų reikšmės eilutė \[, 2 kriterijų intervalo eilutė, 2 kriterijų reikšmės eilutė, ...\]) | Pateikti XML mazgų, kurie buvo surinkti vykdant šį formatavimą ir kurie tenkina įvestas sąlygas (diapazoną ir reikšmę), reikšmių sąrašą. Pateikti tuščią sąrašą, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta. | |

### <a name="other-business-domainspecific-functions"></a>Kitos (konkrečios verslo srities) funkcijos

| Funkcija | aprašymas | Pavyzdys |
|----------|-------------|---------|
| CONVERTCURRENCY (suma, pirminė valiuta, norima valiuta, data, įmonė) | Konvertuoti nurodytą piniginę sumą iš nurodytos pirminės valiutos į nurodytą norimą valiutą naudojant nurodytos „Finance and Operations“ įmonės parametrus nurodytą dieną. | **CONVERTCURRENCY (1, „EUR“, „USD“, TODAY(), „DEMF“)** pateikia vieno euro atitikmenį doleriais dabartinio seanso dieną, atsižvelgiant į DEMF įmonės parametrus. |
| ROUNDAMOUNT (skaičius, dešimtainės dalys, apvalinimo taisyklė) | Apvalinti nurodytą sumą pagal nurodytą skaičių po kablelio ir nurodytą apvalinimo taisyklę.<blockquote>[!NOTE]<br>Apvalinimo taisyklė turi būti nurodyta kaip „Finance and Operations“ <strong>RoundOffType</strong> išvardijimo reikšmė.</blockquote> | Jei nustatyta parametro **model.RoundOff** reikšmė **Į mažesnę pusę**, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** pateikia reikšmę **1000.78**. Jei parametrui **model.RoundOff** nustatyta reikšmė **Įprastai** arba **Į didesnę pusę**, **ROUNDAMOUNT (1000,787, 2, model.RoundOff)** pateikia reikšmę **1000,79**. |
| CURCredRef (skaitmenys) | Pateikti kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis. | **CURCredRef („VEND-200002“)** pateikia **„2200002“**. |
| MOD\_97 (skaitmenys) | Pateikti kreditoriaus nuorodą kaip MOD97 išraišką pagal nurodyto SF numerio skaitmenis. | **MOD\_97 ("VEND-200002")** pateikia **"20000285"**. |
| ISOCredRef (skaitmenys) | Pateikti Tarptautinės standartizacijos organizacijos (ISO) kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis ir raidinius simbolius.<blockquote>[!NOTE]<br>Norint iš abėcėlės pašalinti simbolius, kurie nėra suderinami su ISO, įvesties parametras turi būti išverstas prieš jį perduodant į šią funkciją.</blockquote> | **ISOCredRef („VEND-200002“)** pateikia **„RF23VEND-200002“**. |
| CN\_GBT\_AdditionalDimensionID (eilutė, numeris) | Gaukite papildomos finansinės dimensijos ID. Dimensijos šioje eilutėje rodomos kaip kableliais atskirti ID. Šioje eilutėje numeriai nurodo pageidaujamos dimensijos sekos kodą. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** pateikia **"CC"**. |
| GetCurrentCompany () | Pateikti juridinio subjekto (įmonės), prie kurio šiuo metu vartotojas prisijungęs, kodą tekstine išraiška. | Vartotojui, prisijungusiam prie „Finance and Operations” įmonės **„Contoso Entertainment System USA“**, **(GETCURRENTCOMPANY)** pateikia **USMF**. |
| CH\_BANK\_MOD\_10 (skaitmenys) | Pateikti kreditoriaus nuorodą kaip MOD10 išraišką pagal nurodyto SF numerio skaitmenis. | **CH\_BANK\_MOD\_10 ("VEND-200002")** pateikia **3**. |
| FA\_SUM (ilgalaikio turto kodas, vertinimo modelio kodas, pradžios datas, pabaigos data) | Pateikti paruoštą nurodyto laikotarpio ilgalaikio turto sumos duomenų konteinerį. | **FA\_SUM ("COMP-000001", “Current”, Date1, Date2)** pateikia paruoštą ilgalaikio turto **COMP-000001**, kurio vertinimo modelis – **Dabartinis**, duomenų konteinerį, skirtą laikotarpiui nuo **Date1** iki **Date2**. |
| FA\_BALANCE (ilgalaikio turto kodas, vertinimo modelio kodas, ataskaitiniai metai, ataskaitų data) | Pateikti paruoštą ilgalaikio turto balanso duomenų konteinerį. Ataskaitiniai metai turi būti nurodyti kaip „Finance and Operations“ išvardijimo **AssetYear** reikšmė. | **FA\_SUM („COMP-000001“, "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** pateikia paruoštą ilgalaikio turto **COMP-000001**, kurio dabartinio „365 for Finance and Operations“ seanso dieną vertinimo modelis – **„Dabartinis“**, balansų duomenų konteinerį. |
| TABLENAME2ID (eilutė) | Pateikti nurodyto pavadinimo lentelės ID sveikuoju skaičiumi. | **TABLENAME2ID ("Intrastat")** pateikia **1510**. |
| ISVALIDCHARACTERISO7064 (eilutė) | Pateikti Būlio logikos reikšmę **TRUE**, kai nurodyta eilutė rodo tinkamą tarptautinį banko sąskaitos numerį (IBAN). Kitu atveju pateikti Būlio logikos reikšmę **FALSE**. | **ISVALIDCHARACTERISO7064 („AT61 1904 3002 3457 3201“)** pateikia **TEISINGA**. **ISVALIDCHARACTERISO7064 („AT61“)** pateikia **KLAIDINGA**. |

### <a name="functions-list-extension"></a>Funkcijų sąrašo papildymas

ER leidžia papildyti ER išraiškose naudojamų funkcijų sąrašą. Tam reikės atitinkamų inžinerinių pastangų. Daugiau informacijos rasite [Elektroninių ataskaitų funkcijų sąrašo papildymas](general-electronic-reporting-formulas-list-extension.md).

## <a name="see-also"></a>Taip pat žiūrėkite

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų (ER) funkcijų sąrašo išplėtimas](general-electronic-reporting-formulas-list-extension.md)

