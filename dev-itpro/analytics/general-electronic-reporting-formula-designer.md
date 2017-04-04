---
title: "Elektroninių ataskaitų formulių kūrimo įrankis"
description: "Šioje temoje paaiškinama, kaip naudoti formulių kūrimo įrankį teikiant elektronines ataskaitas (ER). Kurdami ER konkretaus elektroninio dokumento formatą, duomenis galite transformuoti ir išpildyti atitinkamo dokumento kūrimo ir formatavimo reikalavimus naudodami „Microsoft Excel“ stiliaus formules. Palaiko įvairių tipų funkcijų - tekstą, datą ir laiką, matematiniai loginiai, informacija, duomenų tipo konvertavimo ir kitų (verslo domeno-specialių funkcijų)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ac8d6c064ca826cc1c2fed07578ca9ce0c66ef66
ms.lasthandoff: 03/31/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Elektroninių ataskaitų formulių kūrimo įrankis

Šioje temoje paaiškinama, kaip naudoti formulių kūrimo įrankį teikiant elektronines ataskaitas (ER). Kurdami ER konkretaus elektroninio dokumento formatą, duomenis galite transformuoti ir išpildyti atitinkamo dokumento kūrimo ir formatavimo reikalavimus naudodami „Microsoft Excel“ stiliaus formules. Palaiko įvairių tipų funkcijų - tekstą, datą ir laiką, matematiniai loginiai, informacija, duomenų tipo konvertavimo ir kitų (verslo domeno-specialių funkcijų).

<a name="formula-designer-overview"></a>Formulių kūrimo įrankio apžvalga
-------------------------

Elektroninės ataskaitos (ER) palaiko formulių kūrimo įrankį. Todėl kūrimo metu galite konfigūruoti išraiškas, kurias galima naudoti šių užduočių vykdymo metu:

-   transformuodami iš „Microsoft Dynamics 365 for Operations“ duomenų bazės gautus duomenis, kurie turėtų būti automatiškai įvesti ER duomenų modelyje, sukurtame kaip ER formatų (filtravimo, grupavimo, duomenų tipo konvertavimo ir t. t.) duomenų šaltinis;
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

-   iš „Microsoft Dynamics 365 for Operations“ duomenų šaltinių ir vykdymo laiko parametrų į ER duomenų modelį;
-   iš ER duomenų modelio į ER formatą;
-   iš „Microsoft Dynamics 365 for Operations“ duomenų šaltinių ir vykdymo laiko parametrų į ER formato.

Tolesnė iliustracija rodo šio tipo išraiškos kūrimą. Šiame pavyzdyje išraiška pateikia „Dynamics 365 for Operations“ **Intrastat** lentelės lauko **Intrastat.AmountMST** reikšmę po to, kai ši reikšmė suapvalinama iki dviejų skaičių po kablelio. [![nuotraukų-išraiška-privalomas](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) iliustracijoje parodyta, kaip gali būti naudojamas šio tipo išraiška. Šiame pavyzdyje dizaino išraiškos rezultatas yra gyventojų į **Transaction.InvoicedAmount** dalis, **mokesčių ataskaitų teikimo pavyzdžio** duomenų modelis. [![nuotraukų-išraiška-binding2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) vykdymo metu, sukurta formulė, **apvalus (Intrastat.AmountMST, 2)**, suapvalins vertė į **AmountMST** lauko kiekvienam įrašui, į **Intrastat** lentelė su dviem dešimtainėmis vietomis, ir užpildyti suapvalinta reikšmė, kuri, **Transaction.InvoicedAmount** sudėtinė dalis, **mokesčių ataskaitų** duomenų modelis.

### <a name="data-formatting"></a>Duomenų formatavimas

ER formulių kūrimo įrankį galima naudoti apibrėžiant išraišką, kuri formatuoja iš duomenų šaltinių gautus duomenis, kad tuos duomenis būtų galima siųsti kaip generuojamo elektroninio dokumento dalį. Jei turite formatavimą, kuris turi būti taikomas kaip įprasta pakartotinai naudojama formato taisyklė, tokį formatavimą galite vienu kartu įvesti į formato konfigūraciją kaip įvardytąjį pakeitimą, kuris turi formatavimo išraišką. Tada šį įvardytąjį pakeitimą galima susieti su daug formato komponentų, kurių išvedami duomenys turi būti formatuojami pagal sukurtą išraišką. Tolesnė iliustracija rodo šio tipo pakeitimo kūrimą. Šiame pavyzdyje pakeitimas **TrimmedString** gauna duomenų tipo **Eilutė** duomenis ir pateikdamas eilutės reikšmę sutrumpina priekinius ir galinius tarpus. [![nuotraukų-transformavimo-dizainas](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) iliustracijoje parodyta kaip tokia pertvarka gali būti naudojamas. Šiame pavyzdyje keletas formato komponentų, kurie vykdymo metu siunčia tekstą kaip išeigą į generuojamą elektroninį dokumentą, nurodo pakeitimą **TrimmedString** pagal pavadinimą. [![nuotraukų-transformavimo-naudojimo](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Kada formatas komponentų perduoti į ** TrimmedString ** transformacijos (pvz., į **partyName** komponento ankstesnėje iliustracijoje) tai siunčia tekstą kaip išvesties dokumento generavimo. Tame tekste nebūna priekinių ir galinių tarpų. Jei formatavimą būtina taikyti atskirai, galite jį nustatyti kaip atskirą konkretaus formato komponento susiejimo išraišką. Tolesnė iliustracija rodo šio tipo išraišką. Šiame pavyzdyje formato komponentas **partyType** yra susietas su duomenų šaltiniu per išraišką, kuri konvertuoja iš duomenų šaltinyje esančio lauko **Model.Company.RegistrationType** gaunamus duomenis į tekstą didžiosiomis raidėmis ir siunčia šį tekstą kaip elektroninio dokumento išeigą. [![nuotraukų privalomas su formulė](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>Proceso eigos valdymas

ER formulių dizaino įrankis gali būti naudojamas apibrėžiant išraiškas, kurios valdo dokumentų generavimo proceso eigą. Galite:

-   Apibrėžkite sąlygas, kurios lemia, kada sustabyti dokumentų kūrimo procesą.
-   Nurodykite išraiškas, kurios kuria galutiniams vartotojams skirtus pranešimus apie sustabdytus procesus arba pateikia vykdymo žurnalo pranešimus apie besitęsiantį ataskaitų generavimo procesą.
-   Nurodykite generuojamų dokumentų failų vardus ir jų kūrimo kontrolės sąlygas.

Kiekviena proceso eigos valdymo taisyklė sukuriama kaip atskiras tikrinimo elementas. Tolesnė iliustracija rodo šio tipo tikrinimą. Čia pateikiamas šiame pavyzdyje esančios konfigūracijos paaiškinimas:

-   Tikrinimas įvertinamas, kai generuojamame XML faile sukuriamas mazgas **INSTAT**.
-   Jei operacijų sąrašas yra tuščias, tikrinimas sustabdo vykdymo procesą ir pateikia **FALSE**.
-   Tikrinimas pateikia klaidos pranešimą, kuriame yra žymės SYS70894 tekstas vartotojo pageidaujama kalba.

[![nuotraukų tikrinimas](./media/picture-validation.jpg)](./media/picture-validation.jpg) The ER formulių kūrimo priemonę taip pat galima nurodyti gamybos elektroninio dokumento failo vardas ir failo kūrimo procesą kontroliuoti. Tolesnė iliustracija rodo šio tipo proceso eigos valdymo kūrimą. Čia pateikiamas šiame pavyzdyje esančios konfigūracijos paaiškinimas:

-   Duomenų šaltinio **model.Intrastat** įrašų sąrašas padalinamas į paketus, iš kurių kiekviename yra iki 1000 įrašų.
-   Išeiga sukuria „zip“ failą, kuriame yra po vieną failą XML formatu kiekvienam sukurtam paketui.
-   Išraiška pateikia generuojamų elektroninių dokumentų failo vardą sujungdama failo vardą ir failo plėtinį. Antrojo paketo ir visų vėlesnių paketų failo varde kaip priedėlis nurodytas paketo ID.
-   Išraiška įgalina (pateikdama reikšmę **TRUE**) paketų, kuriuose yra bent vienas įrašas, failų kūrimo procesą.

[![nuotraukų failų valdymo](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Pagrindinė sintaksė

ER išraiškos gali turėti bet kurį arba visus iš šių elementų:

-   Konstantos
-   Operatoriai
-   Nuorodos
-   Keliai
-   Funkcijos

#### <a name="constants"></a>Konstantos

Kurdami išraiškas galite naudoti tekstines ir skaitines konstantas (reikšmes, kurios nėra apskaičiuojamos). Pavyzdžiui, išraiška ** vertę ("100") + 20 ** naudoja nuolat 20 skaitinių, ir eilutės konstanta "100", ir grąžina skaitinė reikšmė **120**. ER formulių dizaino įrankis palaiko kaitos sekas leisdamas nurodyti, kurią išraiškos eilutės dalį reikėtų tvarkyti kitaip. Pvz., išraiška **„Levas Tolstojus „„Karas ir taika““ 1 tomas“** pateikia teksto eilutę **Levas Tolstojus „Karas ir taika“ 1 tomas**.

#### <a name="operators"></a>Operatoriai

Toliau pateikiamoje lentelėje parodyti aritmetiniai operatoriai, kuriais galite atlikti pagrindines matematikos operacijas, pvz., sudėtį, atimtį, dalybą ir daugybą.

| Operatorius | Reikšmė              | Pavyzdys |
|----------|----------------------|---------|
| +        | Priedas             | 1+2     |
| -        | Atimties neigimas | 5-2 -1  |
| \*       | Daugyba       | 7\*8    |
| /        | Padalinys             | 9/3     |

Toliau pateikiamoje lentelėje parodyti palyginimo operatoriai, kurie yra palaikomi ir kuriuos galite naudoti dviem reikšmėms palyginti.

| Operatorius | Reikšmė                  | Pavyzdys    |
|----------|--------------------------|------------|
| =        | Lygu                    | X=Y        |
| &gt;     | Didesnis nei             | X&gt;Y     |
| &lt;     | Mažesnis nei                | X&lt;Y     |
| &gt;=    | Daugiau arba lygu | X&gt;=Y    |
| &lt;=    | Mažiau arba lygu    | X&lt;=Y    |
| &lt;&gt; | Nelygu             | X&lt;&gt;Y |

Be to, galite naudoti ampersendą (&) kaip teksto sujungimo operatorių, kad sujungtumėte ar susietumėte vieną ar daugiau teksto eilučių į vientisą tekstą.

| Operatorius | Reikšmė     | Pavyzdys                                        |
|----------|-------------|------------------------------------------------|
| &        | Sujungti | „Nėra ką spausdinti“ & „: „ & „įrašų nerasta“ |

#### <a name="operator-precedence"></a>Operatoriaus pirmenybė

Tvarka, kuria vertinamos sudėtinės išraiškos dalys, yra svarbi. Pavyzdžiui, dėl žodžio ** 1 + 4 / 2 ** skiriasi priklausomai nuo to, ar be operacijos ar skaidymo atliekama pirmą kartą. Galite naudoti skliaustus, kad aiškiai apibrėžtumėte, kaip vertinti išraišką. Pvz., jei norite nurodyti, kad pirma turėtų būti atliekama sudėties operacija, minėtą išraišką galite pakeisti į **(1 + 4) / 2**. Jei išraiškoje atliekamų operacijų tvarka nėra aiškiai apibrėžta, ji nustatoma pagal numatytąją pirmenybę, kuri priskiriama palaikomiems operatoriams. Tolesnėje lentelėje parodyti operatoriai ir kiekvienam iš jų priskiriama pirmenybė. Aukštesnę pirmenybę (pvz., 7) turintys operatoriai vertinami prieš žemesnę pirmenybę (pvz., 1) turinčius operatorius.

| Pirmumas | Operatoriai      | Sintaksė                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Grupavimas       | ( … )                                                    |
| 6          | Nario prieiga  | … . …                                                    |
| 5          | Funkcijos iškvietimas  | … ( … )                                                  |
| 4          | Dauginamasis | … \* … … / …                                             |
| 3          | Priedas       | … + … … - …                                              |
| 2          | Palyginimas     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Atskyrimas     | … , …                                                    |

Toje pačioje eilutėje esantys operatoriai turi vienodą pirmenybę. Jei išraiška apima daugiau nei vieną iš šių operatorių, išraiška vertinama iš kairės į dešinę. Pavyzdžiui, išraiška **1 + 6 / 2 \*3 &gt;5** pateikia **tikras**. Aiškiai nurodyti norimą išraiškų vertinimo tvarką rekomenduojame naudojant skliaustus, kad išraiškas būtų lengviau skaityti ir prižiūrėti.

#### <a name="references"></a>Nuorodos

Visi dabartinio ER komponento (modelio arba formato) duomenų šaltiniai, kurie yra pasiekiami kuriant išraišką, gali būti naudojami kaip įvardytosios nuorodos. Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **ReportingDate**, kuris pateikia duomenų tipo **DATETIME** reikšmę. Tinkamai formatuoti reikšmės gamybos dokumento, galite nurodyti duomenų šaltinio išraiška taip: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")** visų simbolių vardą nuorodų duomenų šaltinį, kad nekelia abėcėlės raidė turi būti rašomas viengubą kabutę ('). Jei nuorodų duomenų šaltinio pavadinimas yra bent vienas simbolis, kuris neturi atstovauti laišką abėcėlė (pvz., skyrybos ženklų arba kitais rašytiniais simboliais), pavadinimo reikia rašyti viengubose kabutėse. Štai keletas pavyzdžių:

-   Duomenų šaltinis **Today's date & time** ER išraiškoje turi būti nurodytas taip: **'Today''s date & time'**
-   Duomenų šaltinio **Klientai** metodas **name()** ER išraiškoje turi būti nurodytas taip: **Customers.'name()'**

#### <a name="path"></a>Kelias

Kai išraiška nurodo susistemintų duomenų šaltinį, galite naudoti kelio aprašą, kad pasirinktumėte konkretų nesudėtingą duomenų šaltinio elementą. Taško simbolis (.) naudojamas atskiriant atskirus susistemintų duomenų šaltinio elementus. Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **InvoiceTransactions**, kurį naudojant pateikiamas įrašų sąrašas. ** InvoiceTransactions** įrašo struktūroje yra laukai **AmountDebit** ir **AmountCredit**, kurie pateikia skaitines reikšmes. Todėl galite SF sumą galite apskaičiuoti sukūrę tokią išraišką: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>Funkcijos

Kitame skyriuje aprašomos funkcijos, kurias galima naudoti ER išraiškose. Visi išraiškos konteksto (esamo ER duomenų modelio arba ER formato) duomenų šaltiniai bei konstantos pagal iškvietimo funkcijų argumentų sąrašą gali būti naudojamos kaip iškvietimo funkcijų parametrai. Pvz., dabartiniame ER duomenų modelyje yra duomenų šaltinis **InvoiceTransactions**, kurį naudojant pateikiamas įrašų sąrašas. ** InvoiceTransactions** įrašo struktūroje yra laukai **AmountDebit** ir **AmountCredit**, kurie pateikia skaitines reikšmes. Dėl to, kad apskaičiuotumėte SF sumą, galite sukurti tokią išraišką, kuri naudoja įtaisytąją ER apvalinimo funkciją: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Palaikomos funkcijos
Toliau pateikiamose lentelėse aprašomos duomenų tvarkymo funkcijos, kurias galite naudoti ER duomenų modeliams ir ER ataskaitoms kurti. Funkcijų sąrašas nėra galutinis, o programuotojai gali jį papildyti. Norėdami matyti galimų naudoti funkcijų sąrašą, ER formulių dizaino įrankyje atidarykite funkcijų sritį.

### <a name="date-and-time-functions"></a>Datos ir laiko funkcijos

| Funkcija                                   | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                                                      | Pavyzdys                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (data ir laikas, dienos)                   | Įtraukti nurodytą dienų skaičių į nurodytą datos ir laiko reikšmę.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** nukelia datą ir laiką septyniomis dienomis į ateitį.                                                                                                                                                                                                                            |
| DATETODATETIME (data)                      | Konvertuoti nurodytos datos reikšmę į datos ir laiko reikšmę.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. "getCurrentDate()')** grąžina dabartinę Dynamics 365 operacijų seanso datą, 12/24/2015, kaip **12/24/2015 12:00:00 val.**. Šiame pavyzdyje **CompInfo** yra **„Dynamics 365 for Operations“/lentelės** tipo ER duomenų šaltinis, kuris nurodo lentelę CompanyInfo. |
| NOW ()                                     | Pateikti dabartinio „Dynamics 365 for Operations“ programos serverio datą ir laiką kaip datos ir laiko reikšmę.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Pateikti dabartinio „Dynamics 365 for Operations“ programos serverio datą kaip datos reikšmę.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Pateikti **neapibrėžtą** datos reikšmę.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Pateikti **neapibrėžtą** datos ir laiko reikšmę.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (data ir laikas, formatas)          | Konvertuoti nurodytą datos ir laiko reikšmę į nurodyto formato eilutę. (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** pateikia dabartinio „Dynamics 365 for Operations“ programos serverio datą, 2015-12-24, kaip **2015-12-24** pagal nurodytą pasirinktinį formatą.                                                                                                          |
| DATETIMEFORMAT (data ir laikas, formatas, principas) | Konvertuoti nurodytą datos ir laiko reikšmę į nurodyto formato eilutę ir [principą](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (NOW(), "d", "de")** pateikia dabartinio „Dynamics 365 for Operations“ programos serverio datą, 2015-12-24, kaip **2015-12-24** pagal pasirinktą vokišką principą.                                                                                                             |
| SESSIONTODAY ()                            | Pateikia dabartinio „Dynamics 365 for Operations“ seanso datą kaip datos reikšmę.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Pateikia dabartinio „Dynamics 365 for Operations“ seanso datą ir laiką kaip datetime reikšmę.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (data, formatas)                  | Pateikiama nurodyto formato datos eilutė.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** pateikia dabartinio „Dynamics 365 for Operations“ seanso datą, 2015-12-24, kaip **2015-12-24** pagal nurodytą pasirinktinį formatą.                                                                                                                      |
| DATEFORMAT (data, formatas, principas)         | Konvertuokite nurodytą datos reikšmę į nurodyto formato eilutę ir [principą](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx). (Daugiau informacijos apie palaikomus formatus rasite [standartinis](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ir [pasirinktinis](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)).     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** pateikia dabartinio „Dynamics 365 for Operations“ seanso datą, 2015-12-24, kaip **2015-12-24** pagal pasirinktą vokišką principą.                                                                                                                       |

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
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> grąžina naują sąrašą, kurį sudaro du įrašus, kurie yra <strong>eilutė</strong> srityje. Laukas pirmame įraše yra tekstas <strong>&quot;abc&quot;</strong>, ir antrojoje įrašo laukas yra tekstas <strong>&quot;d&quot;</strong>.</td>
</tr>
<tr class="even">
<td>SPLITLIST (sąrašas, numeris)</td>
<td>Skaidyti nurodytą sąrašą į paketus, iš kurių kiekviename būtų nurodytas įrašų skaičius. Pateikti rezultatą naujame paketų sąraše, kuriame yra šie elementai:
<ul>
<li>Paketai kaip įprasti sąrašai (<strong>Vertės </strong>komponentas)</li>
<li>Dabartinio paketo numeris (<strong>BatchNumber </strong>komponentas)</li>
</ul></td>
<td>Šiame pavyzdyje duomenų šaltinis <strong>Eilutės</strong> sukurtas kaip trijų įrašų sąrašas, suskirstytas į paketus, iš kurių kiekviename yra iki dviejų įrašų. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>Tai rodo sukurtas formatas išdėstymą, kur sąsajos turi ir <strong>linijos</strong> duomenų šaltinis yra sukurta siekiant sukurti išvesties XML formatu, kurį pristato atskirų mazgų kiekvienos partijos ir įrašų jame. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>Toliau pateikiamas rezultatas veikia suprojektuoti formatu. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (1 įrašas [, 2 įrašas,...])</td>
<td>Pateikti naują sąrašą, sukurtą iš nurodytų argumentų.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong> pateikia tuščią įrašą, kur laukų sąraše yra visi <strong>MainData</strong> ir <strong>OtherData</strong> įrašų sąrašų laukai.</td>
</tr>
<tr class="even">
<td>LISTJOIN (1 sąrašas, 2 sąrašas, ...)</td>
<td>Pateikti jungtinį sąrašą, sukurtą iš nurodytų argumentų sąrašų.</td>
<td><strong>LISTJOIN (padalinti (&quot;abc&quot;, 1), PERSKIRTI (&quot;def&quot;, 1))</strong> pateikia šešis įrašus, sąrašą, kai viena sritis, <strong>eilutė</strong> duomenų tipas yra atskiros raidės.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (sąrašas)</td>
<td>Pateikti <strong>TRUE</strong>, jei nurodytame sąraše nėra jokių elementų. Kitu atveju pateikti <strong>FALSE</strong>.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (sąrašas)</td>
<td>Pateikti tuščią sąrašą naudojant nurodytą sąrašą kaip sąrašo struktūros šaltinį.</td>
<td><strong>EMPTYLIST (padalinti (&quot;abc&quot;, 1))</strong> grąžina naują tuščią sąrašą, kuriame yra tokios pačios struktūros kaip sąraše, kuris yra grąžinamas iš <strong>padalinti</strong> funkcija.</td>
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
<td>Jei įvesite <strong>padalinti (&quot;GE&quot;, 2)</strong> kaip duomenų šaltinis (DS), <strong>skaičius (ALLITEMS (DS. Vertė))</strong> pateikia <strong>3</strong>.</td>
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
<td>Kai <strong>tiekėjo</strong> yra sukonfigūruotas kaip ER duomenų šaltinio, kuris nurodo VendTable stalo, <strong>kur (tiekėjams, Vendors.VendGroup = &quot;40&quot;)</strong> pateikia sąrašą tiekėjus, kurie priklauso 40 tiekėjų grupei.</td>
</tr>
<tr class="even">
<td>ENUMERATE (sąrašas)</td>
<td>Pateikti naują sąrašą, sudarytą iš išvardytų nurodyto sąrašo įrašų ir parodantį šiuos elementus:
<ul>
<li>nurodytus sąrašo įrašus kaip įprastus sąrašus (<strong>Vertės </strong>komponentas);</li>
<li>dabartinio įrašo indeksą (<strong>Numerio </strong>komponentas).</li>
</ul></td>
<td>Šiame pavyzdyje <strong>Išvardytas</strong> duomenų šaltinis sukurtas kaip išvardytas tiekėjo įrašų sąrašas iš duomenų šaltinio <strong>Tiekėjai</strong>, kuris nurodo lentelę <strong>VendTable</strong>. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Čia yra formatas, kur duomenų sąryšius yra sukurta siekiant sukurti išvesties XML formatu, kurį pristato atskirų tiekėjų kaip išvardyto mazgai. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>Tai rezultatas veikia suprojektuoti formatu. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (sąrašas)</td>
<td>Pateikti nurodytame sąraše esančių įrašų skaičių, jei sąrašas nėra tuščias. Kitu atveju pateikti <strong>0</strong> (nulis).</td>
<td><strong>SKAIČIUS (padalinti (&quot;Tomas&quot;, 3))</strong> grąžina <strong>2</strong>, nes į <strong>padalinti</strong> funkcija sukuria sąrašą, kurį sudaro du įrašai.</td>
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
<td>Toliau pateiktame pavyzdyje parodytas duomenų modelyje įvestas išvardijimas. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Toliau pateiktame pavyzdyje:
<ul>
<li>modelio išvardijimas, įtrauktas į ataskaitą kaip duomenų šaltinis;</li>
<li>ER išraiška, sukurta naudoti modelio išvardijimą kaip šios funkcijos parametrą;</li>
<li>įrašų sąrašo tipo duomenų šaltinis, įtrauktas į ataskaitą naudojant sukurtą ER išraišką.</li>
</ul><ph id="t1">
< a href="./media/ger-listoffields-function-in-format-expression.png" ></ph><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> toliau pateiktame pavyzdyje ER formato elementus, susietus su duomenų šaltinio įrašų sąrašo tipas, kuris buvo sukurtas naudojant LISTOFFIELDS funkciją. <a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Tai yra sukurtas formatas vykdymo rezultatas. <a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Pastaba:</strong> išversti teksto etiketes ir aprašymai yra apgyvendintos ER formatas išvesties pagal kalbos parametrai sukonfigūruotas naudoti pirminio failo ir aplanko formos elementų.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (sąrašas, lauko pavadinimas, skyriklis)</td>
<td>Pateikia sujungtų lauko reikšmių eilutę iš sąrašo, atskirto pasirinktu skyrikliu.</td>
<td>Jei SPLIT(“abc” , 1) įvedėte kaip duomenų šaltinio DS, išraiška STRINGJOIN (DS, DS.Value, “:”) pateikia grąžina „a:b:c“</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (sąrašas, ribinė reikšmė, ribos šaltinis)</td>
<td>Nurodytą sąrašą padalija į naują antrinių sąrašų sąrašą ir pateikia rezultatą įrašų sąrašo turinyje. Ribinės reikšmės parametras nurodo ribos reikšmę, taikomą dalijant pradinį sąrašą. Ribos šaltinio parametras nurodo veiksmą, kurį atliekant bendra suma didėja. Riba netaikoma vienam konkretaus sąrašo elementui, kai ribos šaltinis viršija nustatytą ribą.</td>
<td>Toliau pateiktame pavyzdyje rodomas formato pavyzdys naudojant duomenų šaltinius. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Tai rezultatas formatas vykdymo, pateikianti butas prekių elementų sąrašas. <a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>Šiame pavyzdyje rodoma tuo pačiu formatu, kurią koregavo pateikti prekių elementų sąrašas partijomis, kai siunta turi turėti prekių bendras svoris, kuris neturi viršyti 9 riba. <a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Tai koreguota formatas vykdymo rezultatas. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Pastaba:</strong> riba nėra taikomas kilmės sąrašus paskutinį elementą kaip savo ribą šaltinis (svoris) (11) vertė viršija nustatytą ribą (9). Naudokite funkciją <strong>KUR</strong> arba atitinkamo formato elemento išraišką <strong>Įjungta</strong>, norėdami nepaisyti (praleisti) antrinius sąrašus generuojant ataskaitą (jei reikia).</td>
</tr>
<tr class="odd">
<td>FILTER (sąrašas, sąlyga)</td>
<td>Pateikia nurodytą sąrašą, filtruotą pagal nurodytą sąlygą, pakeičiant užklausą. Kitaip nei naudojant funkciją <strong>KUR</strong>, nurodyta sąlyga duomenų bazės lygiu taikoma bet kuriam ER duomenų šaltiniui, kurio tipas Lentelės įrašai.</td>
<td>FILTRAS (tiekėjams, Vendors.VendGroup = &quot;40&quot;) grąžina tik nuo tiekėjų grupei "40" tiekėjų sąrašas kai <strong>tiekėjo</strong> yra sukonfigūruotas kaip ER duomenų šaltinio nuoroda į į <strong>VendTable</strong> lentelėje</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Loginės funkcijos

| Funkcija                                                                                | aprašymas                                                                                                                                                                                                                                                                     | Pavyzdys                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ATVEJU (išraiška, variantas 1, sukelti 1 \[, 2 variantas, sukelti 2\] ... \[, numatytasis rezultatas\]) | Įvertinti nurodytą išraiškos reikšmę pagal nurodytas alternatyvias parinktis. Pateikti pariunkties rezultatą, kuris yra lygus išraiškos reikšmei. Kitu atveju pateikti pasirinktinai įvestą numatytąjį rezultatą (paskutinį parametrą, prieš kurį nėra parinkties). | **CASE( DATETIMEFORMAT( NOW(), „MM“), „10“, „WINTER“, „11“, „WINTER“, „12“, „WINTER“, „“)** pateikia eilutę **„WINTER“**, kai dabartinio „Dynamics 365 for Operations“ seanso data yra tarp spalio ir gruodžio. Kitu atveju pateikia tuščią eilutę. |
| IF (sąlyga, 1 reikšmė, 2 reikšmė)                                                        | Pateikti nurodytą 1 reikšmę, kai išpildoma nurodyta sąlyga. Kitu atveju grąžina reikšmę 2. Jei 1 ir 2 reikšmė yra dokumentų ar įrašų sąrašus, bus būtų tik laukai, kad egzistuoja abiejuose sąrašuose.                                                                     | **IF (1 = 2, „sąlyga išpildyta“, „sąlyga neišpildyta“)** pateikia eilutę **„sąlyga neišpildyta“**.                                                                                                                                                      |
| NOT (sąlyga)                                                                         | Pateikti atšauktą nurodytos sąlygos loginę reikšmę.                                                                                                                                                                                                                   | **NOT (TRUE)** pateikia **FALSE**.                                                                                                                                                                                                                            |
| IR (jeigu 1\[, sąlyga, 2,... \])                                                 | Pateikti **TRUE**, jei *visos *nurodytos sąlygos teisingos. Kitu atveju pateikti **FALSE**.                                                                                                                                                                                            | **AND (1=1, „a“=„a“)** pateikia **TRUE**. **AND (1=2, „a“=„a“)** pateikia **FALSE**.                                                                                                                                                                           |
| ARBA (jeigu 1\[, sąlyga, 2,... \])                                                  | Pateikti **FALSE**, jei *visos *nurodytos sąlygos klaidingos. Pateikti **TRUE**, jei *bet kuri iš *nurodytų sąlygų yra teisinga.                                                                                                                                                                 | **OR (1=2, „a“=„a“)** pateikia **TRUE**.                                                                                                                                                                                                                      |

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
<td><strong>NUMBERVALUE (&quot;1 234,56&quot;, &quot;,&quot;, &quot;&quot;)</strong> grąžina reikšmę <strong>1234.56</strong>.</td>
</tr>
<tr class="even">
<td>VALUE (eilutė)</td>
<td>Konvertuoti nurodytą eilutę į skaičių. Kableliai ir taško simboliai (.) laikomi dešimtainiais skyrikliais, o prieš skaičių rašomas brūkšnelis (-) naudojamas kaip neigiamas ženklas. Pateikti išimtį, jei nurodytoje eilutėje aptinkama kitų neskaitinių simbolių.</td>
<td><strong>VERTĖS (&quot;1 234,56&quot;)</strong> suskumba išimtis.</td>
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

### <a name="record-functions"></a>Įrašo funkcijos

| Funkcija             | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                     | Pavyzdys                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (sąrašas) | Pateikti **neapibrėžtą** įrašą, kuris turi tokią pačią struktūrą, kaip ir nurodytas įrašų sąrašas arba įrašas. **Pastaba: **ši funkcija nebenaudojama. Vietoje jos naudokite **EMPTYRECORD**.                                                                                  | **NULLCONTAINER (SPLIT („abc“, 1))** pateikia naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį pateikia funkcija **SPLIT**. |
| EMPTYRECORD (įrašas) | Pateikti **neapibrėžtą** įrašą, kuris turi tokią pačią struktūrą, kaip ir nurodytas įrašų sąrašas arba įrašas. **Pastaba:** A **neapibrėžtas** įrašas yra įrašas, kur visi laukai turi tuščią reikšmę (**0**\[nuliui\] numeriai, tuščia eilutė stygos, ir t.t.). | **EMPTYRECORD (SPLIT („abc“, 1))** pateikia naują tuščią įrašą, kuris yra tokios pačios struktūros kaip ir sąrašas, kurį pateikia funkcija **SPLIT**.   |

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
<td><strong>VIRŠUTINIS (&quot;mėginio&quot;)</strong> pateikia <strong>&quot;mėginio&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LOWER (eilutė)</td>
<td>Pateikti nurodytą eilutę, kurios raidės konvertuotos į mažąsias raides.</td>
<td><strong>MAŽESNIS (&quot;mėginio&quot;)</strong> pateikia <strong>&quot;mėginio&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>LEFT (eilutė, simbolių skaičius)</td>
<td>Pateikti nurodytą simbolių skaičių iš nurodytos eilutės pradžios.</td>
<td><strong>KAIRĖJE (&quot;pavyzdys&quot;, 3)</strong> pateikia <strong>&quot;Sam&quot;</strong>.</td>
</tr>
<tr class="even">
<td>RIGHT (eilutė, simbolių skaičius)</td>
<td>Pateikti nurodytą simbolių skaičių iš nurodytos eilutės pabaigos.</td>
<td><strong>TEISĖ (&quot;pavyzdys&quot;, 3)</strong> pateikia <strong>&quot;AMA&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>MID (eilutė, pradinė padėtis, simbolių skaičius)</td>
<td>Pateikti nurodytą simbolių skaičių iš nurodytos eilutės, pradedant nuo nurodytos padėties.</td>
<td><strong>VIDURYJE (&quot;pavyzdys&quot;, 2, 3)</strong> pateikia <strong>&quot;ir&quot;</strong>.</td>
</tr>
<tr class="even">
<td>LEN (eilutė)</td>
<td>Pateikti simbolių skaičių nurodytoje eilutėje.</td>
<td><strong>LEN (&quot;pavyzdys&quot;)</strong> pateikia <strong>6</strong>.</td>
</tr>
<tr class="odd">
<td>CHAR (skaičius)</td>
<td>Pateikti simbolių eilutę, kurią nurodo pateiktas „Unicode“ numeris.</td>
<td><strong>CHAR (255)</strong> pateikia <strong>&quot;ÿ&quot;</strong>. <strong>Pastaba:</strong> pateikta eilutė priklauso nuo kodavimo, kuris pažymėtas pirminiame formato FAILAS elemente. Palaikomų kodavimų sąrašą galima rasti temoje <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodavimo klasė</a>.</td>
</tr>
<tr class="even">
<td>CONCATENATE (1 eilutė [, 2 eilutė, ...])</td>
<td>Pateikti visas nurodytas teksto eilutes, kurios sujungiamos į vieną eilutę.</td>
<td><strong>SUSIETI (&quot;abc&quot;, &quot;def&quot;)</strong> pateikia <strong>&quot;GE&quot;</strong>. <strong>Pastaba:</strong> išraiška <strong>&quot;abc&quot;&amp;&quot;def&quot;</strong> taip pat grąžina <strong>&quot;GE&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (eilutė, šablonas, pakeitimas)</td>
<td>Pateikti nurodytą eilutę, kur visi simboliai, atitinkantys nurodytą šabloną, pakeičiami atitinkamose kitos nurodytos eilutės vietose esančiais simboliais.</td>
<td><strong>VERSTI (&quot;GE&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> pakeičia modelio <strong>&quot;cd&quot;</strong> su seka, <strong>&quot;GH&quot;</strong> ir pateikia <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (eilutė, šablonas, pakeitimas, įprastos išraiškos žymė)</td>
<td>Kai nurodyta įprasta išraiškos žymė yra <strong>teisinga</strong>, pateikti nurodytą eilutę, kuri modifikuojama pritaikant įprastą išraišką, nurodytą kaip šios funkcijos argumento šablonas. Ši išraiška naudojama ieškant simbolių, kuriuos reikia pakeisti. Rasti simboliai pakeičiami nurodyto pakeitimo argumento simboliais. Kai nurodyta įprastos išraiškos žymė yra <strong>klaidinga</strong>, ši funkcija veikia kaip <strong>TRANSLATE</strong>.</td>
<td>  <strong>PAKEISTI (&quot;+1 923 456 4971&quot;, &quot;[^ 0-9]&quot;, &quot;&quot;, tiesa)</strong> taikoma reguliarios išraiškos, kuri pašalina visus neskaitinių simbolių, ir grąžina <strong>&quot;19234564971&quot;</strong>. <strong>PAKEISTI (&quot;GE&quot;, &quot;cd&quot;, &quot;GH&quot;, klaidingai)</strong> pakeičia modelio <strong>&quot;cd&quot;</strong> su seka, <strong>&quot;GH&quot;</strong> ir pateikia <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="odd">
<td>TEXT (įvestis)</td>
<td>Pateikti nurodytą įvestį, konvertuojamą į teksto eilutę, kuri formatuojama pagal „Dynamics 365 for Operations“ egzemplioriaus serverio vietos parametrus. <strong>Realaus skaičiaus</strong> tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.</td>
<td>Jei Dynamics 365 operacijų instancijos server lokalės yra apibrėžiamas kaip <strong>lt</strong>, <strong>teksto (dabar ())</strong> grąžina dabartinę Dynamics 365 operacijų seanso datą, 12/17/2015, kaip teksto eilutė <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong>. <strong>TEKSTAS (1/3)</strong> pateikia <strong>&quot;0,33&quot;</strong>.</td>
</tr>
<tr class="even">
<td>FORMAT (1 eilutė, 2 eilutė[, 3 eilutė, ...])</td>
<td>Pateikti nurodytą eilutę, kuri formatuojama pakeičiant visus <strong>%N</strong> pasikartojimus <em>n</em>-uoju argumentu. Argumentai yra eilutės. Jei argumentas nėra parametro, parametras yra grąžinami kaip <strong>&quot;%N&quot;</strong> eilutėje. <strong>Realaus skaičiaus</strong> tipo reikšmių eilutės konvertavimas apribotas dviem skaičiais po kablelio.</td>
<td>Šiame pavyzdyje duomenų šaltinis <strong>PaymentModel</strong> pateikia klientų įrašus komponente <strong>Klientas</strong> ir apdorojimo datos reikšmę lauke <strong>ProcessingDate</strong>. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>ER formatas, sukurtas kurti elektronine pasirinktiems klientam, <strong>PaymentModel</strong> yra pažymėtas kaip duomenų šaltinį ir kontrolės eigą. Galutiniams vartotojams pateikiama išimtis, kai pasirinktas klientas sustabdomas ataskaitos apdorojimo dieną. Formulė, sukurta šio tipo apdorojimo kontrolei, gali naudoti tokius išteklius:
<ul>
<li>„Dynamics 365 for Operations“ žymė SYS70894, kur nurodytas toks tekstas:
<ul>
<li><strong>LT kalba:</strong>&quot;nieko spausdinti&quot;</li>
<li><strong>DE kalba:</strong>&quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>„Dynamics 365 for Operations“ žymė SYS18389, kur nurodytas toks tekstas:
<ul>
<li><strong>LT kalba:</strong>&quot;sustojo kliento %1 % 2.&quot;</li>
<li><strong>DE kalba:</strong>&quot;'%1' Debitor wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Čia yra formulės, kurios gali būti skirtos: formatas (CONCATENATE (@&quot;SYS70894&quot;,&quot;. &quot;@&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (modelis. ProcessingDate, &quot;d&quot;)) Jei ataskaitoje išnagrinėjama per į <strong>Litware mažmeniniam vartotojui</strong> 2015 m. gruodžio 17 d. – į <strong>lt</strong> kultūra ir <strong>lt</strong> kalba, ši formulė grąžina šį tekstą, kuris gali būti pateikta kaip išimtis pranešimą galutiniam vartotojui: &quot;nieko spausdinti. Klientų Litware mažmeninės prekybos sustoja 12/17/2015.&quot; Jei pagal tą pačią ataskaitą yra tvarkomi su<strong> Litware mažmeniniam vartotojui</strong> 2015 m. gruodžio 17 d. – į <strong>DE</strong> kultūra ir <strong>DE</strong> kalba, ši formulė grąžina šį tekstą, kuris naudoja skirtingos datos formatą: &quot;Nichts zu drucken. Debitor "Litware Retail" wird für 17.12.2015 gesperrt.&quot; <strong>Pastaba: </strong>ER formulėse žymėms taikoma tokia sintaksė:
<ul>
<li><strong>Etikečių Dynamics 365 operacijų išteklių:</strong> <strong>@&quot;X&quot;</strong>, kur X yra šis žymės ID programos objektų medis (AOT)</li>
<li><strong>Etikečių, kurie gyvena ER konfigūracijų:</strong> <strong>@&quot;ER_LABEL:X&quot;</strong>, kur X yra šis žymės ID ER konfigūracijos</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (skaičius, formatas)</td>
<td>Pateikti nurodyto skaičiaus eilutę nurodytu formatu. (Informacijos apie palaikomus formatus rasite <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standartinis</a> ir <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">vartotojo</a>.) To, kad ši funkcija veiktų pagal lemia kultūrą, kuri yra naudojama formatuoti numerius.</td>
<td>LT kultūros <strong>skaičiaus formatas (0,45, &quot;p&quot;)</strong> pateikia <strong>&quot;45,00 %&quot;</strong>. <strong>Skaičiaus formatas (10.45, &quot;#&quot;)</strong> pateikia <strong>&quot;10&quot;</strong>.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (numeris, kalba, valiuta, spausdinimo valiutos pavadinimo žymė, dešimtainiai skaičiai)</td>
<td>Pateikia skaičių, parašytą (konvertuotą) į teksto eilutes nurodyta kalba. Kalbos kodas neprivalomas: kai jis nurodytas kaip tuščia eilutė, bus naudojamas vykdomo konteksto kalbos kodas (skirtas generuojamam aplankui arba failui). Valiutos kodas nėra būtinas. Kai jis nurodytas kaip tuščia eilutė, naudojama įmonės valiuta. Atkreipkite dėmesį, kad parametrai <strong>Spaudinio valiutos pavadinimas</strong> ir <strong>Dešimtainiai skaičiai</strong> yra analizuojami tik pagal šiuos kalbų kodus: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. Atkreipkite dėmesį, kad parametras <strong>Spaudinio valiutos pavadinimas</strong> analizuojamas tik „Dynamics 365 for Operations“ įmonėms, kurių šalies kontekste palaikomas valiutos linksniavimas.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, klaidingai, 2) grąžina "Vienas tūkstantis du šimtai trisdešimt keturi ir 56" NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, klaidingai, 0) grąžina "Sto dwadzieścia" NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, tiesa, 2) grąžina "Сто двадцать евро 21 евроцент"</td>
</tr>
<tr class="odd">
<td>PADLEFT (eilutė, ilgis, užpildymo simboliai)</td>
<td>Pateikiama nustatyto ilgio eilutė, kurioje eilutės pradžia užpildyta nurodytais simboliais.</td>
<td>PADLEFT (“1234”, 10, “ “) pateikia teksto eilutę „      1234“</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Duomenų rinkinio funkcijos

Funkcija

aprašymas

Pavyzdys

FORMATELEMENTNAME ()

Pateikia šio formato elemento pavadinimą. Pateikia tuščią eilutę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.

Žr. užduočių vedlį **ER: duomenų formato išvesties duomenų naudojimas skaičiuojant ir sumuojant** (verslo proceso **Įsigyti / sukurti IT paslaugų ir sprendimų komponentų** dalis), norėdami daugiau sužinoti apie šios funkcijos naudojimą.

SUMIFS (pagrindinės eilutės susumuojant, kriterijus klasėje1 eilutė, kriterijus reikšmė1 eilutė \[, kriterijus range2 eilutė, kriterijus reikšmė2 eilutę,... \])

Pateikia XML mazgų (kurių pavadinimas apibrėžtas kaip raktas) reikšmių, kurios surinktos vykdant šį formatavimą ir kurios tenkina įvestas sąlygas (diapazoną ir reikšmę), sumą. Pateikia nulio reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.

SUMIF (rakto eilutė, skirta sumuoti, kriterijų diapazono eilutė, kriterijų reikšmių eilutė)

Pateikia XML mazgų (kurių pavadinimas apibrėžtas kaip raktas) reikšmių, kurios surinktos vykdant šį formatavimą ir kurios tenkina įvestą sąlygą (diapazoną ir reikšmę), sumą. Pateikia nulio reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.

COUNTIFS (kriterijus klasėje1 eilutė, kriterijus reikšmė1 eilutė \[, kriterijus range2 eilutė, kriterijus reikšmė2 eilutę,... \])

Pateikia XML mazgų, kurie buvo surinkti vykdant šį formatavimą ir kurie tenkina įvestas sąlygas (diapazoną ir reikšmę), numerį. Pateikia nulio reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.

COUNTIF (kriterijų diapazono eilutė, kriterijų reikšmių eilutė)

Pateikia XML mazgų, kurie surinktos vykdant šį formatavimą ir kurie tenkina įvestą sąlygą (diapazoną ir reikšmę), numerį. Pateikia nulio reikšmę, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.

COLLECTEDLIST (kriterijus klasėje1 eilutė, kriterijus reikšmė1 eilutė \[, kriterijus range2 eilutė, kriterijus reikšmė2 eilutę,... \])

Pateikia XML mazgų reikšmių, kurios surinktos vykdant šį formatavimą ir kurios tenkina įvestas sąlygas (diapazoną ir reikšmę), sąrašą. Pateikia tuščią sąrašą, kai dabartinių failų žymė **Rinkti išeigos informaciją** yra išjungta.

### <a name="other-business-domainspecific-functions"></a>Kitos (konkrečios verslo srities) funkcijos

| Funkcija                                                                         | aprašymas                                                                                                                                                                                                                                                        | Pavyzdys                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (suma, pirminė valiuta, norima valiuta, data, įmonė)        | Konvertuoti nurodytą piniginę sumą iš pirminės valiutos į norimą valiutą naudojant nurodytos „Dynamics 365 for Operations“ įmonės parametrus nurodytą dieną.                                                                            | **CONVERTCURRENCY (1, „EUR“, „USD“, TODAY(), „DEMF“)** pateikia vieno euro atitikmenį doleriais dabartinio seanso dieną, atsižvelgiant į DEMF įmonės parametrus.                                                                                                                                  |
| ROUNDAMOUNT (skaičius, dešimtainės dalys, apvalinimo taisyklė)                                       | Apvalinti nurodytą sumą pagal nurodytą apvalinimo taisyklę ir nurodytą skaičių po kablelio. **Pastaba:** apvalinimo taisyklė turi būti nurodyta kaip „Dynamics 365 for Operations“ **RoundOffType** išvardijimo reikšmė.                          | Jei su **modelis. Apvalinimas** parametras nustatytas kaip *** Downward ***, **ROUNDAMOUNT (1000.787, 2, modelis. Apvalinimas)** grąžina reikšmę **1000.78**. Jei parametrui **model.RoundOff** nustatyta reikšmė **Įprastai** arba **Į didesnę pusę**, **ROUNDAMOUNT (1000,787, 2, model.RoundOff)** pateikia reikšmę **1000,79**. |
| CURCredRef (skaitmenys)                                                              | Pateikti kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis.                                                                                                                                                                                  | **CURCredRef („VEND-200002“)** pateikia **„2200002“**.                                                                                                                                                                                                                                                         |
| MOD\_97 (skaičiai)                                                                 | Pateikti kreditoriaus nuorodą kaip MOD97 išraišką pagal nurodyto SF numerio skaitmenis.                                                                                                                                                            | **MOD\_("VEND 200002") 97** pateikia **"20000285"**.                                                                                                                                                                                                                                                           |
| ISOCredRef (skaitmenys)                                                              | Pateikti ISO kreditoriaus nuorodą pagal nurodyto SF numerio skaitmenis ir raidinius simbolius. **Pastaba: **norint iš abėcėlės pašalinti simbolius, kurie nėra suderinami su ISO, įvesties parametras turi būti išverstas prieš jį perduodant į šią funkciją. | **ISOCredRef („VEND-200002“)** pateikia **„RF23VEND-200002“**.                                                                                                                                                                                                                                                 |
| KN\_direktorius\_AdditionalDimensionID (eilute, numeris)                                  | Gaukite papildomos finansinės dimensijos ID. Dimensijos šioje eilutėje rodomos kaip kableliais atskirti ID. Numeriai nurodyto pageidaujamą dimensijos numeracijos kodą šioje eilutėje.                                                                            | KN\_direktorius\_AdditionalDimensionID ("AA, BB, CC, DD, EE, FF, GG, HH", 3) grąžinti "CC"                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Pateikia šiuo metu prisijungusios įmonės kodą.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_banko\_MOD\_10 (skaičiai)                                                       | Pateikia kreditoriaus nuorodą kaip MOD10 išraišką pagal nurodyto SF numerio skaitmenis.                                                                                                                                                                      | CH\_banko\_MOD\_grąžina 3, 10 ("VEND 200002")                                                                                                                                                                                                                                                                   |
| IT\_suma (nustatyta turto kodas, vertės modelio kodą, pradžios data, pabaigos data)               | Pateikia paruoštą tam tikro laikotarpio ilgalaikio turto sumų duomenų konteinerį.                                                                                                                                                                                         | IT\_SUMAI ("COMP-000001", "Srovė", data1 ir data2) grąžina paruoštų duomenų talpyklos ilgalaikio turto "COMP-000001" su vertės modeliu "Srovė" laikotarpiui nuo data1 iki datos2.                                                                                                                        |
| IT\_vertės (ilgalaikio turto kodas, vertės modelio kodą, ataskaitiniais metais, ataskaitų sudarymo dieną) | Pateikiamas paruoštas ilgalaikio turto balansų duomenų konteineris. Ataskaitiniai metai turi būti nurodyti kaip „Dynamics 365 for Operations“ operacijų išvardijimo reikšmė **AssetYear**.                                                                                           | IT\_SUMAI ("COMP-000001", "Srovė", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) grąžina paruoštų duomenų konteinerio likutinės ilgalaikio turto "COMP-000001" su vertės modeliu "Srovės" apie dabartinę 365 operacijų seanso datą.                                                                |

### <a name="functions-list-extension"></a>Funkcijų sąrašo papildymas

ER leidžia papildyti ER išraiškose naudojamų funkcijų sąrašą. Tam reikės atitinkamų inžinerinių įgūdžių. Daugiau informacijos rasite [Elektroninių ataskaitų funkcijų sąrašo papildymas](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų (ER) funkcijų sąrašo išplėtimas](general-electronic-reporting-formulas-list-extension.md)


