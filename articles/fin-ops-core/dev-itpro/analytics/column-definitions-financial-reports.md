---
title: Finansinių ataskaitų stulpelių aprašai
description: Šiame straipsnyje pateikiama informacija apie stulpelių aprašus. Stulpelio aprašas yra ataskaitos komponentas, kuris nurodo ataskaitos stulpelių turinį.
author: aprilolson
ms.date: 10/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.form: FinancialReports
ms.openlocfilehash: 97f6c869e8d05e37ec3001d5de262ab8927d735a
ms.sourcegitcommit: d27fef61593c6d1e9e26d5c9fad21411bc52fabc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9802802"
---
# <a name="column-definitions-in-financial-reports"></a>Finansinių ataskaitų stulpelių aprašai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie stulpelių aprašus. Stulpelio aprašas yra ataskaitos komponentas, arba kūrimo blokas, kuris nurodo ataskaitos stulpelių turinį. Kaip ir eilučių aprašai, pagrindiniai stulpelių aprašai gali būti naudojami keli ataskaitose.

## <a name="create-and-modify-a-column-definition"></a>Stulpelio aprašo kūrimas ir modifikavimas

Stulpelio apraše gali būti nuo dviejų iki 255 stulpelių.

### <a name="create-a-column-definition"></a>Stulpelio aprašo kūrimas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite Stulpelio **apibrėžimai**.
2. Meniu Rinkmena **spustelėkite** Naujas **·**, tada spustelėkite Stulpelio **aprašas**.
3. Pridėkite stulpelio aprašo turinį.

### <a name="open-a-column-definition"></a>Stulpelio aprašo atidarymas

1. Ataskaitų dizaino įrankio naršymo srityje spustelėkite Stulpelio **apibrėžimai**.
2. Dukart spustelėkite stulpelio aprašą, kad atidarytumėte.

### <a name="add-a-column-to-a-column-definition"></a>Stulpelio įtraukimas į stulpelių aprašą

1. Ataskaitų konstruktoriuje spustelėkite **Stulpelio apibrėžimai**, tada atidarykite stulpelio aprašą, kad jį keisite.
2. Pasirinkite stulpelį, į kurį turi būti įterptas naujas stulpelis.
3. Redagavimo **meniu** spustelėkite stulpelį **Įterpti**. Naujas stulpelis rodomas pasirinkto stulpelio kairėje.

### <a name="delete-a-column-from-a-column-definition"></a>Stulpelio naikinimas iš stulpelių aprašo

1. Ataskaitų konstruktoriuje spustelėkite **Stulpelio apibrėžimai**, tada atidarykite stulpelio aprašą, kad jį keisite.
2. Pasirinkite stulpelį, kurį norite panaikinti.
3. Redagavimo **meniu** spustelėkite stulpelį **Naikinti**.

## <a name="contents-of-a-column-definition"></a>Stulpelių aprašo turinys
Stulpelio apraše pateikiama ši informacija:

- Stulpelis, kuriame pateikiami eilutės apibrėžimo aprašymai
- Sumos stulpeliai, kuriuose rodomi finansinių duomenų duomenys arba skaičiavimai pagal kitus stulpelio aprašo duomenis
- Stulpelių formatavimas
- Atributų stulpeliai

Ši informacija rodoma šiose stulpelio aprašo srityse:

- Stulpelio aprašo antraščių srityje yra antraštės tekstas ir ataskaitoje rodomas formatavimas. Antraštė gali būti taikoma vienam duomenų stulpeliui, apimti kelis stulpelius arba gali būti taikoma stulpeliams pagal sąlygas. Stulpelio apibrėžtyje gali būti tiek stulpelių antraščių eilučių, kiek reikia.

    > [!NOTE]
    > Stulpelių antraštės taikomos kiekvienam ataskaitos duomenų stulpeliui. Ataskaitų antraštės taikomos visai ataskaitai. Ataskaitos apibrėžimo skirtuke Antraštės **ir poraštės** apibrėžiate ataskaitų antraštes.

- Stulpelio informacijos eilutės yra po stulpelio aprašo antraštės eilutėmis esančios eilutės. Stulpelio informacijos eilutėse nurodoma į ataskaitą įtraukta informacija. Toliau pateikiamoje lentelėje išvardijamos ir aprašomos stulpelio informacijos eilutės.

    | Stulpelio informacijos eilutės pavadinimas                                                | Prekės/Paslaugos pavadinimas                                                    |
    |-----------------------------------------------------------------------|-------------------------------------------------------------------------|
    | Stulpelio tipas                                                           | (Būtina) Nurodykite stulpelio duomenų tipą.                                      |
    | Knygos kodas / atributo kategorija                                          | Nurodykite **FD** ir **ATTR** tipo stulpelių finansinių duomenų informaciją.     |
    | Į finansinių metų laikotarpį įtraukti laikotarpiai                                    | Nurodykite **FD** tipo stulpelių finansinių duomenų informaciją.              |
    | Formulė                                                               | Nurodykite **CALC** tipo stulpelių skaičiavimo formulę.                  |
    | Stulpelio plotis Papildomi tarpai prieš stulpelį Formato nepaisymas Spausdinimo valdiklis | Nurodykite specialaus formato pasirinktis.                                               |
    | Stulpelio apribojimai                                                   | Apribokite duomenis.                                                                        |
    | Ataskaitinis vienetas.                                                        | Apribokite stulpelį, kad jame būtų rodomi tik nurodyto ataskaitinio vieneto duomenys.      |
    | Valiutos rodinio valiutos filtras                                      | Formatuokite valiutą.                                                                      |
    | Dimensijos filtras                                                      | Nurodykite filtrą, kuriame duomenys apribojami iki konkrečių finansinių duomenų ataskaitinių vienetų.           |
    | Atributo filtras                                                      | Nurodykite filtrą, pagal kurį turėtų būti apribojami finansiniai duomenys.                                      |
    | Pradžios data Pabaigos data                                                   | Apribokite finansinius duomenis pagal tam tikras datas.                                    |
    | Pagrindimas                                                         | Eilutės apraše nurodytą aprašo tekstą sulygiuokite kairėje, centre arba dešinėje. |

## <a name="column-restrictions-in-a-column-definition"></a>Stulpelio apibrėžimo stulpelio apribojimai
Norėdami nurodyti, kaip stulpelio apraše naudojami duomenys arba apskaičiuojama informacija, galite naudoti stulpelio apribojimus. Ataskaitos stulpelį taip pat galima apriboti konkrečiu vienetu arba konkrečiomis datomis.

> [!NOTE]
> Stulpelio **apribojimo** kodas nepaiso visų eilutės apibrėžime priskirtų nesuderinamų parametrų.

### <a name="column-restrictions-cell"></a>Stulpelio apribojimų langelis

Stulpelyje **apribojimų lange** gali būti kodai, kurie apriboja arba nerodo informacijos, pvz., to stulpelio eilučių formatavimą, informaciją ir sumas.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Stulpelio apribojimo įtraukimas į stulpelio aprašą

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Dukart spustelėkite stulpelio **apribojimų langelį** Stulpelis, kad apriboti.
3. Dialogo lange **Stulpelio** apribojimai pasirinkite vieną ar daugiau sąrašo kodų ir spustelėkite **Gerai**.

### <a name="column-restriction-codes"></a>Stulpelio apribojimo kodai

Toliau pateikiamoje lentelėje aprašomi stulpelio apribojimo kodai.

| Stulpelio apribojimo kodas | Prekės/Paslaugos pavadinimas |
|-------------------------|-------------|
| SU                      | Pabraukimo panaikinimas stulpelyje, kurio eilutės apraše įvedama pabraukimo komanda (**---**) arba dvigubo pabraukimo komanda (**===**). Pavyzdžiui, galbūt nenorite pabraukti sumų, kurios gaunamos apskaičiuojant procentinę dalį. |
| ST                      | Bendrųjų sumų panaikinimas, kad stulpelyje būtų rodoma tik informacija (pvz., statistikos stulpelis). |
| SD                      | Slėpti informaciją, kad stulpelyje būtų rodomos tik eilutės **TOT** ir **KPL** (iš eilutės aprašo). |
| DR                      | Apriboti stulpelio **FD** sumas, kad būtų rodomos tik debeto sumos. |
| CR                      | Apriboti stulpelio **FD** sumas, kad būtų rodomos tik kredito sumos. |
| ADJ                     | Apriboti stulpelio sumas, kad būtų rodomos tik laikotarpio koregavimo sumos, jei šios sumos galimos. |
| XAD                     | Apriboti stulpelio sumas, kad būtų nerodomos laikotarpio koregavimo sumos. |
| SP                      | Apriboti stulpelio sumas, kad būtų įtraukiamos tik užregistruotos operacijos, jei šios operacijos galimos. |
| UPT                     | Apriboti stulpelio sumas, kad būtų įtraukiamos tik neužregistruotos operacijos, jei šios operacijos galimos.<p><strong>Pastaba:</strong> ne visi duomenų teikėjai palaiko neužregistruotas operacijas. </p> |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Stulpelio apibojimas iki ataskaitinio vieneto

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Du kartus spustelėkite stulpelio **, kurį** norite apriboti, ataskaitos vieneto langelį.
3. Ataskaitų medžio **sąrašo dialogo** lange Ataskaitų vienetas **pasirinkite** medį.
4. Išplėskite arba sutraukite vienetų sąrašą, pasirinkite ataskaitinį vienetą, tada spustelėkite **Gerai**.

## <a name="format-column-headers"></a>Stulpelių antraščių formatavimas
Galite pridėti, modifikuoti ir panaikinti ataskaitos stulpelių viršuje rodomas antraštes. Taip pat galite konfigūruoti sąlyginių rašto stulpelių antraštes, **pagrįstas** **stulpelių** apibrėžimų lauku Laikotarpis ir ataskaitos apibrėžimų lauku Pagrindinis laikotarpis. Jei naudojatės pagrindinio laikotarpio funkcija, kurdami kintančios prognozės ataskaitas galite sutaupyti laiko.

### <a name="create-and-manage-column-headers"></a>Stulpelio antraščių kūrimas ir tvarkymas

Norėdami pridėti **, modifikuoti ir naikinti** ataskaitos stulpelių viršuje rodomas antraštes, galite naudoti dialogo langą Stulpelio antraštė. Toliau pateikiamoje lentelėje aprašomi dialogo lango Stulpelio **antraštė** laukai.

| Laukas                 | Aprašymas |
|-----------------------|-------------|
| Stulpelio antraštės tekstas    | Šis tekstas rodomas stulpelio antraštėje. Galite tiesiogiai įvesti tekstą į šį lauką arba spustelėti Įterpti automatinį **tekstą, kad pasirinktumėte pasirinktį,** kuri atnaujina stulpelio antraštę kiekvieną kartą, kai generuojama ataskaita. Norėdami įtraukti kelis automatinio teksto kodus, dar kartą **spustelėkite Įterpti autoText** ir sąraše spustelėkite kitą kodą. |
| Formatavimo pasirinktys        | Taikyti formatavimą stulpelio antraštei, pvz., teksto lauką arba pabraukimą. |
| Paskirstyti nuo Paskirstyti iki | Nurodykite, kuriam stulpeliui ar stulpeliams taikomas antraštės tekstas. |
| Pagrindimas         | Nurodykite, kaip stulpelio antraštės tekstas turėtų būti sulygiuotas laukuose **Paskirstyti nuo** ir **Paskirstyti iki** nurodytame stulpelyje arba stulpelių intervale. |

### <a name="create-a-column-header"></a>Stulpelio antraštės kūrimas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Dukart spustelėkite antraštės langelį.
3. Stulpelio **antraštės** dialogo lange įveskite stulpelio antraštės tekstą. Taip pat spustelėkite Įterpti **automatinį tekstą** ir pasirinkite pasirinktį.
4. Lauke **Formatavimo pasirinktys** pasirinkite antraštės formatą.
5. Lauke **Paskirstyti nuo** įveskite stulpelio raidę, kuria turėtų prasidėti stulpelio antraštė. Lauke **Paskirstyti iki** įveskite stulpelio raidę, kuria stulpelio antraštė turėtų pasibaigti.
6. Dalyje **Lygiavimas** pasirinkite, ar stulpelio antraštės tekstas turėtų būti lygiuojamas kairėje, centre, ar dešinėje.
7. Spustelėkite **Gerai**.

### <a name="add-a-column-header-row"></a>Stulpelio antraštės eilutės įtraukimas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Pažymėkite antraštės eilutės langelį.
3. Redagavimo **meniu** spustelėkite eilutę **Įterpti**. Nauja eilutė bus įterpta virš atliekant 2 veiksmą pažymėtos eilutės.

> [!NOTE]
> Jei ataskaitoje yra keturios arba daugiau ataskaitos antraščių eilučių, antraštės persidengs ataskaitą eksportuojant į „Excel“ darbalapį. Norėdami peržiūrėti visas ataskaitos antraštes, padidinkite viršutinę ataskaitos aprašo paraštę.

### <a name="delete-a-column-header-row"></a>Stulpelio antraštės eilutės naikinimas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Antraštės eilutėje pažymėkite norimą naikinti langelį.
3.  **Meniu Redaguoti** spustelėkite eilutę **Naikinti**.

### <a name="create-an-automatically-generated-header"></a>Automatiškai sugeneruotos antraštės kūrimas

Ataskaitų dizaino įrankis gali automatiškai sugeneruoti stulpelių antraštes pagal automatinio teksto kodus. Automatinio teksto kodai yra kintamieji, kurie atnaujinami kiekvieną kartą, kai sugeneruojama ataskaita. Šie kodai gali būti bet kurio stulpelio antraštėje ir juose nurodoma ataskaitos informacija, kuri gali kisti, pvz., datos ar laikotarpio numeriai. Todėl galite naudoti vieną stulpelio aprašą keliems ataskaitos aprašams, laikotarpiams ir ataskaitų medžiams. Kadangi automatinio teksto kodai paremti stulpelio aprašo informacijos eilutėse pateikta kalendoriaus informacija, juos palaiko tik stulpeliai **CALC** ir **FD**. Nuo to, kaip automatinio teksto kodas rodomas stulpelio antraštės langelyje priklauso tai, kaip ta informacija rodoma ataskaitoje. Dialogo lange **Stulpelio antraštė** automatinio teksto kodai rodomi didžiosiomis ir mažosiomis raidėmis. Todėl ataskaitoje tekstas rodomas didžiosiomis ir mažosiomis raidėmis. Pavyzdžiui, standartiniuose kalendoriniuose metuose **\@CalMonthLong** pakeičia **7** mėnesį į **liepą**. Jei mėnesio pavadinimas turėtų būti rodomas didžiosiomis raidėmis (pavyzdžiui, **LIEPA**), **Stulpelio antraštės teksto** lauke autoteksto kodą įveskite didžiosiomis raidėmis. Pavyzdžiui, įveskite **\@CALMONTHLONG**. Galite maišyti kodus ir tekstą. Pavyzdžiui, įveskite šį antraštės tekstą: **Laikotarpis \@FiscalPeriod-\@FiscalYear nuo \@StartDate iki \@EndDate**. Sugeneruotos ataskaitos antraštės tekstas panašus į šį tekstą: **Laikotarpis 1-02 nuo 01/01/02 iki 01/31/02**.

> [!NOTE]
> Kai kurio teksto, pvz., ilgosios datos, formatas priklauso nuo jūsų serverio regiono parametrų. Norėdami pakeisti šiuos parametrus, spustelėkite mygtuką **Pradžia**, spustelėkite **Valdymo skydas**, tada spustelėkite **Regionas ir kalba**. Toliau pateikiamoje lentelėje išvardijamos galimos stulpelio antraščių automatinio teksto pasirinktys.


| Automatinio teksto pasirinktis ir kodas                | Prekės/Paslaugos pavadinimas |
|-----------------------------------------|-------------|
| Mėnesio pavadinimas (@CalMonthLong)              | Spausdinti dabartinio mėnesio pavadinimą stulpelio antraštėje. Jei ataskaitoje nuspręsite apvalinti sumas iki tūkstančių, milijonų ar milijardų, arba jei nustatysite mažesnį negu devynių simbolių ataskaitos stulpelio plotį, mėnesio pavadinimas trumpinamas iki pirmųjų trijų simbolių. |
| Sutrumpintas mėnesio pavadinimas (@CalMonthShort) | Spausdinti pasirinkto ataskaitinio laikotarpio mėnesio sutrumpintą pavadinimą. |
| Laikotarpio numeris (@FiscalPeriod)           | Spausdinti identifikuojamo to stulpelio ataskaitinio laikotarpio skaitinę formą. Jei stulpelis apima kelis laikotarpius, spausdinamas paskutinis intervalo laikotarpis. |
| Laikotarpio aprašas (@FiscalPeriodName)  | Spausdinti finansiniuose duomenyse identifikuojamo ataskaitinio laikotarpio aprašą. |
| Finansiniai metai (@FiscalYear)               | Spausdinti stulpelio finansinių metų skaitinę formą. |
| Kalendoriniai metai (@CalYear)                | Spausdinti stulpelio kalendorinių metų skaitinę formą. |
| Pradžios data (@StartDate)                 | Spausdinti stulpelio pradžios datą. |
| Pabaigos data (@EndDate)                     | Spausdinti stulpelio pabaigos datą. |
| Medžio vieneto pavadinimas (@UnitName)         | Jei nustatysite apribojimą, kad stulpelyje būtų rodomas tik tam tikras ataskaitų medžio vienetas, išspausdinkite to vieneto pavadinimą stulpelio antraštėje. |
| Vieneto aprašas (@UnitDesc)            | Jei nustatysite apribojimą, kad stulpelyje būtų rodomas tik tam tikras ataskaitų medžio vienetas, išspausdinkite to vieneto aprašą stulpelio antraštėje. |
| Knygos kodas (@BookCode)                   | Spausdinti stulpelyje nurodytą knygos kodą. |
| Tuščia eilutė (@Blank)                     | Į stulpelio antraštę įterpkite tuščią eilutę. |

### <a name="create-a-conditional-spanning-header"></a>Sąlyginės aprėpiančios antraštės kūrimas

Sąlyginės aprėpiančios antraštės gali aprėpti kelis tam tikro laikotarpio duomenimis grįstus stulpelius. Pavyzdžiui, jei turite finansinių metų biudžeto ataskaitą ir norite kartu su pastarųjų mėnesių faktiniais biudžetais rodyti ateinančių mėnesių planuojamus biudžetus, naudodami sąlyginę aprėpiančią antraštę galite automatiškai atnaujinti ataskaitos antraštę. Kurdami sąlyginę besitęsiančią antraštę atkreipkite dėmesį į toliau pateiktas situacijas.

- Bet kuri sustabdymo sąlyga **(** paskirstyta laukui), gretinama prieš pradžios sąlygą (**paskirstyti** nuo lauko) nepaisoma. Pavyzdžiui, nurodyta stulpelio B paskirstymo sąlyga nuo BASE+1 iki BASE, kurioje BASE yra stulpelis C, o BASE+1 yra stulpelis D. Šiuo atveju stulpelio C sustabdymo sąlygos nepaisoma, o spausdinimas antraštėje prasideda nuo stulpelio D.
- Jei nurodote persidengiančias stulpelių antraštes, jos persidengia, kai yra spausdinamos ataskaitoje. Ataskaita generuojama, **bet** ataskaitų eilės būsenos lauke rodomas šis įspėjimas: "Stulpelių antraštės, naudojant base sutapimą su kitomis stulpelių antraštėmis, kurios gali persidengti su tekstu." Pavyzdžiui, stulpelio B antraštės aprašas yra nuo B iki BASE+1, o stulpelio D antraštės aprašas yra nuo BASE+1 iki F. Tokiu atveju antraštės spausdinamos viena ant kitos ir yra beveik neįskaitomos. Kiekvieną kartą, kai apraše **Paskirstyti nuo / Paskirstyti iki** naudojamas BASE, būtinai peržiūrėkite generuojamą ataskaitą, kad pamatytumėte, ar antraštės persidengia.
- Jei BASE nurodote stulpelio Nespausdinti (**NP**) paskirstymo apraše, jo bus nepaisoma, neatsižvelgiant į tai, kas nurodyta stulpelio apraše. Iš esmės šis scenarijus yra toks pat kaip tada, kai nesukuriamas stulpelio antraštės aprašas.
- Sąlyginio spausdinimo stulpelių (**P&lt;B**, **P&gt;=B**) sąlyginės aprėpiančios antraštės veikia taip pat, kaip bet kuris įprastas stulpelio antraštės aprašas. Pvz., jei sąlyga klaidinga, bet kuriame kitame stulpelyje, kuris atitinka paskirstymo sąlygą, pradedama spausdinti antraštė.

#### <a name="create-a-conditional-spanning-header"></a>Sąlyginės aprėpiančios antraštės kūrimas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Dukart spustelėkite antraštės langelį.
3. Stulpelio **antraštės** dialogo lange įveskite stulpelio antraštės tekstą. Taip pat spustelėkite Įterpti **automatinį tekstą** ir pasirinkite pasirinktį.
4. Lauke **Formatavimo pasirinktys** pasirinkite antraštės formatavimo stilių.
5. Nurodyti laikotarpį, susijusį su pagrindiniu laikotarpiu, kuris nurodytas generuojant ataskaitą. Laukuose **Paskirstyti nuo** ir **Paskirstyti iki** įveskite vieną iš šių reikšmių: **BASE**, **BASE-X** arba **BASE+X**, kuriose X yra laikotarpių skaičius nuo pagrindinio laikotarpio. Pvz., jei lauke **Paskirstyti nuo** įvesite **BASE**, sąlyginio aprėpiančio stulpelio antraštės tekstas prasideda stulpelio antraštėje, kurioje ataskaitos aprašo **Pagrindinis laikotarpis** reikšmė lygi stulpelio aprašo **Laikotarpis** reikšmei. Jis baigiasi stulpelyje, kuris nurodytas lauke **Paskirstyti iki**. Todėl jei paskirstymas yra iš BASE į M, o ataskaitos aprašo **Pagrindinis laikotarpis** reikšmė yra **4**, antraštė prasideda stulpelyje, kuriame nustatytas laikotarpis **4**, ir baigiasi stulpelyje M. Antraštės sustabdomos ir paleidžiamos tik spausdinimo stulpeliuose.
6. Dalyje **Lygiavimas** pasirinkite, ar stulpelio antraštės tekstas turėtų būti lygiuojamas kairėje, centre, ar dešinėje.
7. Spustelėkite **Gerai**.

#### <a name="example-of-a-conditional-spanning-header"></a>Sąlyginės aprėpiančios antraštės pavyzdys

Vartotojas kuria dinaminės šešių mėnesių prognozės ataskaitą. Vartotojas nori, kad žodis „Faktinis“ būtų išspausdintas stulpeliuose, kuriuose yra faktiniai duomenys, o žodis „Biudžetas“ būtų išspausdintas stulpeliuose, kuriuose yra biudžeto prognozės. Kiekvieną mėnesį, kada paleidžiama ataskaita, faktinių stulpelių yra vienu daugiau, o biudžeto stulpelių – vienu mažiau. Nors norėdamas koreguoti antraštes, kiekvieną kartą, kai generuojama ataskaita, vartotojas gali pati keisti stulpelio aprašą, tam, kad sutaupytų laiko ir pastangų, vartotojas nusprendžia sukurti sąlygines aprėpiančias antraštes, kurios kiekvieną kartą paleidus ataskaitą atitinkamuose stulpeliuose automatiškai sukurs antraštes. Vartotojas atidaro ataskaitų dizaino įrankį, naršymo srityje spusteli **Stulpelio aprašas** ir atidaro ataskaitos stulpelio aprašą. Tada vartotojas įveda toliau nurodomą informaciją. Ataskaitos apraše nurodytas pagrindinis laikotarpis yra 4.

|  Formatuoti   |  A   | Mlrd.     | K      | D       | E        | Pn.       | Ž       | H      | I             | J             | Tūkst.             | L             | P             |
|-----------|------|-------|--------|---------|----------|---------|---------|---------|-------------|---------------|---------------|---------------|---------------|
| 1 antraštė   |    | Faktinis    | Biudžetas        |         |         |        |       |          |        |               |               |               |               |
| 2 antraštė   |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| 3 antraštė    |      |       |        |        |        |         |        |          |               |               |               |               |               |
| Stulpelio tipas  | APRAŠ. | FD   | FD     | FD    | FD   | FD    | FD      | FD            | FD            | FD            | FD            | FD            | FD            |
| Knygos kodas / atributas |      | FAKTINIS        | BIUDŽETAS2012    | FAKTINIS        | BIUDŽETAS2012    | FAKTINIS        | BIUDŽETAS2012    | FAKTINIS        | BIUDŽETAS2012    | FAKTINIS        | BIUDŽETAS2012    | FAKTINIS        | BIUDŽETAS2012    |
| Finansiniai metai |  | PAGRINDINIS   | PAGRINDINIS   | PAGRINDINIS   | PAGRINDINIS   | PAGRINDINIS    | PAGRINDINIS    | PAGRINDINIS     | PAGRINDINIS          | PAGRINDINIS          | PAGRINDINIS          | PAGRINDINIS          | PAGRINDINIS          |
| Laikotarpis  |     | 1      | 1       | 2      | 2      | 3       | 3       | 4        | 4             | 5             | 5             | 6             | 6             |
| Apimami laikotarpiai     |      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      | PERIODINIS      |
| Stulpelio plotis   | 30   | 10    | 10     | 10     | 10    | 10    | 10    | 10     | 10            | 10            | 10            | 10            | 10            |
| Spausdinimo valdiklis  |    | P&lt;=B    | P&gt;B   | P&lt;=B  | P&gt;B   | P&lt;=B   | P&gt;B   | P&lt;=B  | P&gt;B   | P&lt;=B  | P&gt;B   | P&lt;=B       | P&gt;B        |

Vartotojas du kartus spusteli B stulpelio antraštės langelį, kad atidarytų **stulpelio** antraštės dialogo langą, ir įveda šią informaciją.

| Laukas              | Reikšmė                 |
|--------------------|-----------------------|
| Stulpelio antraštės tekstas | Faktinis                |
| Įterpti automatinį tekstą    | Niekas nepasirinkta. |
| Formatavimo pasirinktys     | Langelis                   |
| Pagrindimas      | Niekas nepasirinkta. |
| Paskirstyti nuo        | Mlrd.                     |
| Paskirstyti iki          | PAGRINDINIS                  |

Įvedęs informaciją, vartotojas spusteli **Gerai**. Tada vartotojas du kartus spusteli C stulpelio antraštės langelį, kad atidarytų stulpelio **antraštės** dialogo langą, ir įveda šią informaciją.

| Laukas              | Reikšmė                 |
|--------------------|-----------------------|
| Stulpelio antraštės tekstas | Biudžetas                |
| Įterpti automatinį tekstą    | Niekas nepasirinkta. |
| Formatavimo pasirinktys     | Laukas                   |
| Pagrindimas      | Niekas nepasirinkta. |
| Paskirstyti nuo        | PAGRINDAS+1                |
| Paskirstyti iki          | P                     |

Dabar kiekvieną kartą generuojant ataskaitą žodis „Faktinis“ bus išspausdintas stulpeliuose, kuriuose yra faktiniai duomenys, o žodis „Biudžetas“ bus išspausdintas stulpeliuose, kuriuose yra biudžeto prognozės. Be to, stulpelių skaičius kiekvieną mėnesį bus koreguojamas.

## <a name="apply-column-justification"></a>Stulpelio lygiavimo taikymas
Langelis **Lygiavimas** naudojamas norint ataskaitos aprašo stulpeliui taikyti lygiavimo formatavimą. Ši pasirinktis veikia tik stulpelio aprašymus, ne faktines reikšmes.

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Dukart spustelėkite langelį **Lygiavimas**.
3. Pasirinkite vieną iš šių sąrašo reikšmių:

    - **Nėra** – lygiavimas netaikomas.
    - **Kairėje** – lygiuoti stulpelio aprašus kairėje.
    - **Centre** – lygiuoti stulpelio aprašus centre.
    - **Dešinėje** – lygiuoti stulpelio aprašus dešinėje.

## <a name="add-special-formatting-options"></a>Specialių formatavimo pasirinkčių įtraukimas
Stulpelio apraše naudojant formatavimo stulpelio informacijos eilutes pažymėtiems stulpeliams taikomas specialus formatavimas. Nors kai kurios spausdinimo **kontrolės pasirinktys** ir stulpelių **apribojimų** pasirinktys yra **konkrečios FD** stulpeliams, dauguma pasirinkčių yra taikomos visiems stulpelių tipams. Stulpelio apraše nurodytas formatavimas pakeičia ataskaitos apraše nurodytą formatavimą. Tačiau eilutės apraše nurodytas formatavimas pakeičia stulpelio apraše nurodytą formatavimą. Šios eilutės laikomos formatavimo eilutėmis:

- Stulpelio plotis
- Papildomi tarpai prieš stulpelį
- Formato / valiutos nepaisymas
- Spausdinimo valdiklis

### <a name="changing-the-column-width"></a>Stulpelio pločio keitimas

Stulpelio **pločio** langelis nurodo simbolių skaičių, kuris bus naudojamas šio stulpelio plotyje išspausdintoje ataskaitoje. Stulpelio plotis svarbus stulpeliuose, kuriuose yra sumos (**CALC**, **WKS** arba **FD** tipo stulpeliai), aprašai (**DESC** tipo stulpeliai) arba užpildymas (**FILL** tipo stulpeliai). Pagal numatytuosius parametrus pažymėta pasirinktis **Pritaikyti automatiškai**, kad kiekvieno stulpelio plotis automatiškai būtų nustatomas taip, kad tilptų turinys.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Ataskaitos stulpelio pločio nurodymas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Stulpelyje **pločio langelyje** įveskite tarpų skaičių, pagal kurį plotis yra stulpelis. Didžiausias bet kurio stulpelio plotis yra 255 simboliai (įskaitant šimtines dalis, kablelius ir skliaustelius). Arba norėdami įgalinti ataskaitų konstruktorių pasirinkti tinkamą stulpelio plotį pagal langelio turinį, **du** kartus spustelėkite langelį Stulpelio plotis, tada spustelėkite **AutoFit**.

### <a name="add-space-between-columns"></a>Tarpo tarp stulpelių įtraukimas

Papildomi **tarpai prieš stulpelio** langelį nurodo skyriklio plotį tarp vieno stulpelio ir gretimų stulpelių apibrėžime. Papildomi **tarpai prieš stulpelio nustatymą** daro įtaką visoms stulpelio informacijos eilutėms, bet ne stulpelio antraštės eilutėms. Naudokite šią pasirinktį norėdami atskirti stulpelių grupes arba pridėti keletą tarpų prieš aprašymą, kad aprašo stulpelis būtų įtraukiamas pagal kairėje pusėje sulygiuotus pavadinimus. Numatytasis tarpų tarp kiekvieno stulpelio skaičius yra du. Galite pakeisti šį parametrą ataskaitos aprašo skirtuke **Parametrai**.

#### <a name="specify-the-space-between-columns"></a>Tarpo tarp stulpelių nurodymas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Papildomame tarpe **prieš stulpelio langelį** įveskite tarpų, kuriuos norite įterpti tarp stulpelių, skaičių.

### <a name="specify-a-format-currency-override"></a>Formato valiutos perrašymo nurodymas

Formato **/ valiutos perrašymo** langelis nurodo dešimtainių dalių formatavimą, valiutą ir procento sumas stulpelyje. Šis formatavimas pakeičia bet kurį formatavimą, nurodytą ataskaitos apraše arba sistemos numatytuose parametruose.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Formato ir valiutos perrašymo priskyrimas ataskaitos stulpeliui

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Dukart spustelėkite sumos **stulpelio langelį Formatas /** Valiutos perrašymo langelis.
3. Dialogo lange **Formato nepaisymo** pasirinkite formatavimo pasirinktis.

### <a name="add-a-print-control-code"></a>Spausdinimo kontrolinio kodo įtraukimas

 **Spausdinimo kontrolės langelyje** gali būti kodų, kurie koreguoja stulpelio rodymą arba spausdinimo charakteristikas. Yra du spausdinimo kontrolinių kodų tipai: įprastiniai spausdinimo kontroliniai kodai ir sąlyginiai spausdinimo kontroliniai kodai.

#### <a name="regular-print-control-codes"></a>Įprastiniai spausdinimo kontroliniai kodai

| Spausdinimo kontrolinis kodas | Vertimas                                     | Prekės/Paslaugos pavadinimas |
|--------------------|-------------------------------------------------|-------------|
| NP                 | Nespausdinimas                                     | Šio stulpelio sumų neįtraukti į spausdinamą ataskaitą ir į skaičiavimus. Norėdami į skaičiavimą įtraukti nespausdinamą stulpelį, nurodykite stulpelį tiesiogiai skaičiavimo formulėje. Pavyzdžiui, nespausdinamas stulpelis C įtraukiamas į šį skaičiavimą: **B+C+D**. Tačiau nespausdinamas stulpelis C neįtraukiamas į šį skaičiavimą: **B:D**. |
| XCR                | Ženklo keitimas, jei įprastas eilutės balansas yra kreditas | Sukurkite biudžetą arba palyginamąją ataskaitą, kurioje bet koks nepalankus nuokrypis (pvz., pajamų trūkumas ar išlaidų viršijimas) visada yra neigiamas. Taikykite šį kodą stulpeliui **CALC**, jei norite pakeisti stulpelio sumos ženklą, jei įprastas nurodytos eilutės balansas yra kreditas (kaip nurodyta eilutės aprašo stulpelio **Įprastinis balansas** dalyje **C**).<p><strong>Pastaba:</strong> eilutėse <strong>TOT</strong> ir </strong>CAL</strong>, kuriose paprastai nurodomas kredito balansas, eilutės aprašo stulpelyje <strong>Įprastinis balansas</strong> nepamirškite įvesti <strong>C</strong>.</p> |
| X0            | Stulpelio nerodymas, jei visur nuliai arba tuščios vietos   | Neįtraukite stulpelio **FD** į ataskaitą, jei visi to stulpelio langeliai yra tušti arba juose yra nuliai. |
| SR                 | Apvalinimo sustabdymas                               | Neleiskite, kad sumos šiame stulpelyje būtų apvalinamos. |
| XR                 | Sumavimo sustabdymas                                 | Sustabdykite sumavimą. Jei ataskaita naudoja ataskaitų medį, sumos šiame stulpelyje nėra sumuojamos, kad būtų gauti pirminiai mazgai. |
| RP                 | Stulpelio kartojimas kiekviename puslapyje                      | Pakartokite nurodytą stulpelį kiekviename ataskaitos puslapyje. Pvz., galite naudoti spausdinimo kontrolinį kodą **RP** ir įtraukti **ROW** tipo stulpelį, nurodantį eilutės kodus kiekviename puslapyje. |
| WT                 |  Perkelti tekstą į kitą eilutę                                      |  Jei stulpelio tekstas yra per ilgas, kad tilptų tarpe, perkelkite tekstą į kitą eilutę, kad stulpelyje tilptų visas tekstas. |

#### <a name="conditional-print-control-codes"></a>Sąlyginiai spausdinimo kontroliniai kodai

| Sąlyginis spausdinimo kontrolinis kodas | aprašymas                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (nėra)                         | Išvalyti sąlyginio spausdinimo pasirinkimą.                                                  |
| P&lt;B                         | Rodyti nurodytą stulpelį tik tada, jei laikotarpis yra trumpesnis negu pagrindinis laikotarpis.             |
| P&gt;B                         | Rodyti nurodytą stulpelį tik tada, jei laikotarpis yra ilgesnis negu pagrindinis laikotarpis.             |
| P=B                            | Rodyti nurodytą stulpelį tik tada, jei laikotarpis yra lygus pagrindiniam laikotarpiui.              |
| P&lt;=B                        | Rodyti nurodytą stulpelį tik tada, jei laikotarpis yra trumpesnis negu pagrindinis laikotarpis arba jam lygus. |
| P&gt;=B                        | Rodyti nurodytą stulpelį tik tada, jei laikotarpis yra ilgesnis negu pagrindinis laikotarpis arba jam lygus. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Spausdinimo kontrolinių kodų įtraukimas į ataskaitos stulpelį

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Du kartus spustelėkite langelį **Spausdinti valdiklį** .
3. Dialogo lange **Spausdinimo** valdymas pasirinkite kodą iš sąrašo Pasirinkti **spausdinimo kontrolės pasirinktis** . Norėdami pasirinkti daugiau negu vieną kodą, laikykite nuspaudę klavišą Ctrl ir pasirinkite kodus.
4. Lauke **Sąlyginio spausdinimo pasirinktys** pasirinkite parinktį. Pagal numatytuosius parametrus pažymėta **(nėra)**. Vienu metu galite pasirinkti tik vieną sąlyginio spausdinimo kodą.
5. Spustelėkite **Gerai**.

> [!TIP]
> Taip pat galite tiesiogiai įvesti spausdinimo kodus į spausdinimo **kontrolės** langelį. Atskirkite kelis spausdinimo kontrolinius kodus kableliais.

## <a name="column-types"></a>Stulpelio tipai
Kiekvieno ataskaitos stulpelio informacijos tipas nurodytas pagal stulpelio aprašo eilutėje **Stulpelio tipas** pateiktą reikšmę. Kiekvieną stulpelio aprašą privalo sudaryti bent vienas aprašo (**DESC**) stulpelis ir vienas sumos (**FD**, **WKS** ar **CALC**) stulpelis.

> [!NOTE]
> Stulpelio tipo kodai taikomi ne visoms apskaitos sistemoms. Jei pasirinksite jūsų apskaitos sistemai netinkantį tipą, to tipo stulpelis ataskaitoje bus tuščias.

### <a name="specify-a-column-type"></a>Stulpelio tipo nurodymas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Tinkamame stulpelyje du kartus spustelėkite langelį, esančią eilutėje **Stulpelio** tipas.
3. Sąraše pasirinkite stulpelio tipą. Toliau pateikiamoje lentelėje aprašomi įvairūs stulpelių tipai.

    <table>
    <thead>
    <tr>
    <th>Stulpelio tipo kodas</th>
    <th>Aprašas</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>FD</td>
    <td>Rodykite finansinius duomenis, kai eilutės apraše naudojate stulpelį <strong>Susieti su finansinėmis dimensijomis</strong>. Pasirinkus stulpelio tipą <strong>FD</strong>, automatiškai nurodomos tolesnių eilučių numatytosios nuostatos. <ul>
    <li><strong>Knygos kodas / atributo kategorija:</strong> ACTUAL.</li>
    <li><strong>Knygos kodas / atributo kategorija:</strong> ACTUAL.</li>
    <li><strong>Ataskaitiniai metai:</strong> BASE.</li>
    <li><strong>Laikotarpis:</strong> BASE.</li>
    <li><strong>Apimami laikotarpiai:</strong> PERIODIC.</li>
    <li><strong>Stulpelio plotis:</strong> 14.</li>
    </ul>
Šiuos numatytuosius parametrus galite keisti.</td>
    </tr>
    <tr>
    <td>SKAIČ.</td>
    <td>Rodyti langelyje <strong>Formulė</strong> nurodyto paprasto ar sudėtinio skaičiavimo rezultatą. Daugiau informacijos rasite <a href="advanced-formatting-options-financial-reporting.md">Išplėstinės finansinių ataskaitų formatavimo parinktys</a>.</td>
    </tr>
    <tr>
    <td>APRAŠ.</td>
    <td>Rodyti eilutės apibrėžimo aprašymą. Nors aprašymo stulpelis dažnai yra pirmasis ataskaitos stulpelis, jis gali būti bet kurioje vietoje.</td>
    </tr>
    <tr>
    <td>EILUTĖ</td>
    <td>Rodyti finansinių eilučių atskirus eilučių kodus iš eilutės apibrėžimo stulpelio <strong>Eilutės kodas</strong>. Daugiau informacijos rasite <a href="row-definitions-financial-reporting.md">Finansinių ataskaitų eilučių aprašai</a>.</td>
    </tr>
    <tr>
    <td>ACCT (sąskaitų kodai)</td>
    <td>Rodyti kiekvienai eilutei taikomas finansinių duomenų segmentų reikšmes arba dimensijos reikšmes. Išsamių sąskaitų ir operacijų ataskaitų atveju galima spausdinti visiškai paruoštą sąskaitą (pvz., <strong>110140-070-0101</strong>). Jei susietos eilutės apibrėžties stulpelyje <strong>Saitas su finansinėmis dimensijomis</strong> nurodyti diapazonai, diapazonas rodomas laužtiniuose skliaustuose ir suprantamas kaip viena reikšmė (pavyzdžiui, <strong>[110140:110700]-070-[0101:0200]</strong>). Finansinių ataskaitų ir aukšto lygio ataskaitų, kurios yra kelių sąskaitų derinys, atveju išspausdinamas finansinių duomenų saitas iš eilutės apibrėžties (pvz., <strong>1100:1200</strong>).</td>
    </tr>
    <tr>
    <td>UŽPILDAS</td>
    <td>Užpildyti langelį simboliu, parašytu viengubose kabutėse. Jei neįvesite simbolio, stulpelis bus tuščias. Pavyzdžiui, norėdami užpildyti stulpelį daugtaškiu (...), įveskite užpildydami stulpelį, įveskite <strong>UŽPILDYTI</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr>
    <td>PUSLAPIS</td>
    <td>Ataskaitoje įterpti vertikalų puslapio lūžį. Stulpelio <strong>PAGE</strong> dešinėje esantys stulpeliai rodomi kitame puslapyje.</td>
    </tr>
    <tr>
    <td>ATTR</td>
    <td>Jei jūsų apskaitos sistema palaiko atributus, stulpelyje rodyti sąskaitos arba operacijos atributą. Atributas, kuris turi būti taikomas visai vienai sąskaitai, iš finansinių duomenų išrenka pagrindinės sąskaitos arba operacijos informaciją. Sąskaitos lygio atributai rodo duomenis iš sąskaitos, o operacijos lygio atributai rodo duomenis, kurie įvyko operaciją registruojant. Jei kaip stulpelio tipą pasirenkate <strong>ATTR</strong>, stulpelio apibrėžties informacijos eilutėje <strong>Knygos kodas / atributo kategorija</strong> nurodykite atributo kategoriją.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Finansinių dimensijų stulpelis

Šie stulpelio **apibrėžimo** eilutės apibrėžimai taikomi stulpeliams, kurių stulpelio tipas yra **FD** (Sumos iš finansinių dimensijų).

#### <a name="book-codeattribute-category-cell"></a>Langelis Knygos kodas / atributo kategorija

Knygos **kodo / atributo** kategorijos langelis identifikuoja FD **stulpelio duomenų knygos** kodą. Stulpelio apraše gali būti keli faktinių sumų, biudžeto ir statistikos stulpeliai. Stulpelio apraše taip pat gali būti rodomi skirtingi laikotarpiai, pvz., dabartinis arba metų iki šios dienos, ir skirtingos sumos. Knygos kodų sąraše matomos jūsų finansiniuose duomenyse nurodytos faktinių sumų, biudžeto ir statistikos (nefinansinės) pasirinktys.

#### <a name="fiscal-year-cell"></a>Finansinių metų langelis

Finansinių **metų langelis** identifikuoja finansinius metus, kuriuos turi įtraukti stulpelis. Šie metai gali būti susiję su pagrindiniais metais, kurie nurodomi generuojant ataskaitą. Galimos toliau nurodytos pasirinktys.

| Parinktis  | Prekės/Paslaugos pavadinimas                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| PAGRINDINIS    | Naudoti ataskaitos laiku nurodytus pagrindinius metus.                                                                          |
| BASE+\# | Naudoti metus, kurie yra \# metais vėlesni negu pagrindiniai metai. Pavyzdžiui, norėdami naudoti trečiuosius metus po pagrindinių metų, įveskite **PAGRINDINIS+3**. |
| BASE-\# | Naudoti metus, kurie yra \# metais ankstesni negu pagrindiniai metai. Pavyzdžiui, norėdami naudoti praėjusius metus, įveskite **PAGRINDINIS-1**.                 |
| \#      | Įveskite faktinius finansinius metus.                                                                                                |

#### <a name="period-cell"></a>Langelis Laikotarpis

Langelyje **Laikotarpis** nurodomi finansiniai laikotarpiai, kurie turėtų būti įtraukti į stulpelį. Šis laikotarpis gali būti susijęs su pagrindiniu laikotarpiu, kuris nurodytas generuojant ataskaitą. Galimos toliau nurodytos pasirinktys.

| Parinktis          | aprašymas |
|-----------------|-------------|
| PAGRINDINIS            | Naudoti pagrindinį laikotarpį. |
| BASE+\#         | Naudoti laikotarpį, kuris yra \# laikotarpiais vėlesnis negu pagrindinis laikotarpis. Pavyzdžiui, norėdami naudoti trečiąjį laikotarpį po pagrindinio laikotarpio, įveskite **PAGRINDINIS+3**. |
| BASE-\#         | Naudoti laikotarpį, kuris yra \# laikotarpiais ankstesnis negu pagrindinis laikotarpis. Pavyzdžiui, norėdami naudoti praėjusį laikotarpį, įveskite **PAGRINDINIS-1**. |
| BASE-\#:BASE    | Naudoti kelis laikotarpius nuo kelių laikotarpių prieš pagrindinį laikotarpį iki pagrindinio laikotarpio. Pavyzdžiui, norėdami naudoti tris praėjusius laikotarpius ir pagrindinį laikotarpį, įveskite **PAGRINDINIS-3:PAGRINDINIS**. |
| BASE:BASE+\#    | Naudoti kelis laikotarpius nuo pagrindinio laikotarpio iki kelių laikotarpių po pagrindinio laikotarpio. Pavyzdžiui, norėdami naudoti pagrindinį laikotarpį ir du po jo einančius laikotarpius, įveskite **PAGRINDINIS:PAGRINDINIS+2**. |
| BASE-\#:BASE+\# | Naudoti kelis laikotarpius nuo kelių laikotarpių prieš pagrindinį laikotarpį iki kelių laikotarpių po pagrindinio laikotarpio. Pavyzdžiui, norėdami naudoti tris praėjusius laikotarpius, pagrindinį laikotarpį ir po jo einančius du laikotarpius, įveskite **PAGRINDINIS-3:PAGRINDINIS+2**. |
| 1:PAGRINDINIS          | Naudoti kelis laikotarpius nuo pirmojo laikotarpio iki pagrindinio laikotarpio. |
| \#              | Visada naudokite tam tikrą laikotarpio skaičių. Nerekomenduojame naudoti šios pasirinkties, nes ji sumažina stulpelio apibrėžimo lankstumą. |
| \#                                      : \#           | Visada naudokite tam tikrą laikotarpių intervalą. Nerekomenduojame naudoti šios pasirinkties, nes ji sumažina stulpelio apibrėžimo lankstumą. |

Nurodydami bet kurį laikotarpį galite peržengti finansinių metų ribas ir galite maišyti laikotarpių intervalo metus. Pavyzdžiui, nurodykite laikotarpį **BASE-5** (apimantį paskutinius šešis laikotarpius) ir paleiskite ataskaitą, kurios pagrindinis laikotarpis 2. Šiuo atveju ataskaitoje rodomi nurodytų finansinių metų pirmieji du laikotarpiai ir praėjusių finansinių metų paskutiniai keturi laikotarpiai.

### <a name="specify-the-periods-for-an-fd-column"></a>FD stulpelio laikotarpių nurodymas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Stulpelyje **FD** dukart spustelėkite eilutės **Laikotarpis** langelį, tada sąraše pasirinkite pasirinktį.
3. Virš naršymo srities esančioje formulės juostoje arba langelyje **Laikotarpis** užpildykite formulę. Bet kokį skaičiaus ženklą (\#) pakeiskite atitinkama reikšme.

#### <a name="periods-covered-cell"></a>Padengtų laikotarpių langelis

Laikotarpių **apimamas** langelis identifikuoja sumą, kurią stulpelis turėtų rodyti. Ši suma susijusi su stulpelio langelių **Finansiniai** metai **ir** Laikotarpis reikšme. Galimos toliau nurodytos pasirinktys.

| Parinktis      | Prekės/Paslaugos pavadinimas                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODINIS    | Rodyti dabartinio laikotarpio arba laikotarpių intervalo veiklos sumą. |
| PERIODINIS / BB | Rodyti dabartinio laikotarpio arba laikotarpių intervalo pradžios balansą.   |
| YTD         | Rodyti metų iki šios dienos veiklos sumą.                               |
| YTD/BB      | Rodyti metų pradžios balansą.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>FD stulpeliui taikomų laikotarpių nurodymas

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2.  **FD stulpelyje** du kartus spustelėkite langelį laikotarpių padengtų **eilutėje** ir pasirinkite sąrašo pasirinktį.

### <a name="attribute-filter-in-a-column-definition"></a>Stulpelio apibrėžimo atributo filtras

Atributai yra išsamiau sąskaitas arba operacijas apibrėžiančios finansinių duomenų reikšmės. Sąskaitos atributai apima dalis **Turtas**, **Įsipareigojimai**, **Įplaukos** ir **Išlaidos**. Operacijos atributai apima **operacijos aprašą ir**  **operacijos galiojimo datą**. Atributų palaikymas gali skirtis Microsoft Dynamics nuo 365 Finanace. Atributų **filtro** langelis FD **stulpeliuose riboja duomenis** iki konkrečių atributų kategorijų verčių ar diapazonų. Nors ši funkcija gali būti naudojama kartu su stulpeliu **ATTR**, stulpelis **ATTR** nėra būtinas. Stulpelyje **FD** nurodomas apribojimas, kiek sąskaitų arba operacijų bus įtraukiama į ataskaitą naudojant atributo filtrą.

> [!NOTE]
> Norėdami sužinoti, kokius atributus palaiko jūsų ERP sistema, žr. sistemos integravimo vadovą.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Atributo filtro taikymas ataskaitos FD stulpeliui

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Du kartus spustelėkite FD stulpelio **atributų** filtro langelį **.** 
3. Atributų **filtro** dialogo lange du kartus spustelėkite langelį atributo stulpelyje **ir** pasirinkite filtro tipą.
4. Norėdami dar labiau apriboti rezultatus, stulpeliuose **Nuo** ir **Iki** įveskite intervalą. Langelyje **Nuo** turi būti nurodyta reikšmė.
5. Spustelėkite **GERAI**.

#### <a name="example-of-an-attribute-filter"></a>Atributo filtro pavyzdys

Šiame pavyzdyje rodoma stulpelio aprašymo, kuris turi sąskaitos atributą knygos kodo **/ atributo kategorijos eilutėje,** dalis. Šio stulpelio atributo filtras nurodo į ataskaitą įtrauktinų reikšmių intervalą.

|      Filtruoti                  | A    | Mlrd.                   |
|------------------------------|------|---------------------|
| Stulpelio tipas                  | APRAŠ. | FD                  |
| Knygos kodas / atributo kategorija |      | FAKTINIS              |
| Finansiniai metai                  |      | PAGRINDINIS                |
| Laikotarpis                       |      | 1:PAGRINDINIS              |
| Apimami laikotarpiai              |      | PERIODINIS            |
| ...                          |      |                     |
| Stulpelio plotis                 | 30   |                     |
| ...                          |      |                     |
| Atributo filtras             |      | Nuoroda=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Stulpelio apibrėžimo dimensijos filtras

Dimensijos filtras naudojamas norint apriboti, kad stulpelyje **FD** būtų rodomos tik tam tikros dimensijos reikšmės. Filtras gali apimti vieną dimensiją, dimensijų diapazoną ar dimensijų grupę. Į filtrą taip pat galima įtraukti dimensijos verčių rinkinius. Kadangi dimensijos reikšmės gali skirtis, ..\\financial-dimensions\\dimension-based sistema neturi būti konkretaus ilgio. Filtras taikomas nepaisant to, ar į ataskaitą įtraukiamas ataskaitų medis. Pakaitos simbolį (\* arba ?) galite naudoti bet kurioje vietoje. Kai nurodote kelias sąskaitas, atskirkite jas kableliais, kaip parodyta šiame pavyzdyje: +Sąskaita=\[1200\], +Sąskaita=\[1100\], Skyrius=\[01?\] Norėdami gauti visus tam tikros sąskaitos skyrius, į dimensijos filtrą galite neįtraukti skyriaus dimensijos. Pavyzdžiui, abu toliau pateikiami dimensijos filtrai tvarkomi taip pat.

- +Sąskaita=\[1100\],Padalinys
- +Sąskaita=\[1100\]

Taip pat, jeigu norite tikslaus atitikimo, galite naudoti bet kokią raidinių-skaitinių simbolių kombinaciją ir galite nurodyti dalines dimensijas. Pavyzdžiui, **Vieta = \[10\*\]** apima visas vietos dimensijos reikšmes, kurios prasideda 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Dimensijos filtro taikymas ataskaitos stulpeliui

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Dukart spustelėkite **FD stulpelio** dimensijos filtro **langelį** .
3. Dialogo lange **Dimensijos** įveskite taikytinus filtrus.
4. Spustelėkite **GERAI**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Kelių valiutų ataskaitos formatavimas stulpelio apibrėžime

Kelių valiutų ataskaitoje galima rodyti sumas DK apskaitos valiuta, DK ataskaitoje, pradine operacijos valiuta arba konvertuota ataskaitos valiuta. Įmonės apskaitos valiuta nurodoma DK sąrankoje. Nepainiokite šio parametro su operacinės sistemos regiono pasirinkčių parametru, kurį naudodami galite konfigūruoti ataskaitose naudojamus numatytuosius valiutos simbolius. Stulpelio apibrėžime galimi šie su valiuta susiję langeliai:

- **Valiutos rodymas**  – nurodykite valiutos tipą (apskaitos, ataskaitos, operacijos ar išverstos ataskaitos), kuria rodomos operacijos. Konvertavimo į ataskaitų valiutą funkcija kartais vadinama valiutos konvertavimu. Valiutos konvertavimas yra galimybė pateikti didžiosios knygos sumas tokia valiuta, kuri gali būti ne funkcinė ar ataskaitų įmonės valiuta arba ne ta valiuta, kuria buvo įvesta operacija.
- **Valiutos filtras**  – nurodyti valiutos filtrą. Ataskaitoje rodomos tik pasirinkta valiuta įvestos operacijos.


Norėdami nustatyti įmonės apskaitos valiutą, atlikite toliau nurodytus veiksmus.

1. Ataskaitų konstruktoriuje, meniu **Įmonė**, spustelėkite **Įmonės**.
2. Dialogo lange **Įmonės** pasirinkite įmonę, tada spustelėkite **Peržiūrėti**.
3. Regiono pasirinkčių **dialogo** lange **Peržiūrėti įmonę** galite peržiūrėti pasirinktos įmonės nurodytą valiutą.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Valiutos nurodymas kelių valiutų ataskaitoje

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Dukart spustelėkite **valiutos cisplay**  **langelį tinkamame FD** stulpelyje ir pasirinkite valiutos informacijos rodymo pasirinktį: **DK apskaitos** valiuta, **DK ataskaitos**, operacijos valiuta arba pasirinkite versti į kitą ataskaitų valiutą.
3. Dukart spustelėkite atitinkamo stulpelio **FD** langelį **Valiutos filtras**, tada sąraše pasirinkite atitinkamą valiutos kodą. Ataskaitoje rodomos tik šia valiuta įvestos operacijos.


### <a name="example-for-currency-display-and-currency-filter-cells"></a>Valiutos rodymo ir valiutos filtro langelių pavyzdys

Savo stulpelio apibrėžime vartotojas pasirinko šias valiutos pasirinktis:

- **Valiutos filtras: konvertavimas** 
- **Valiutos rodymas:**  apskaitos valiuta iš DK (JAV doleriai)

Dėl pasirinkto valiutos filtro į ataskaitą įtraukiamos tik tos operacijos, kurios įvestos Japonijos jena (JPY). Dėl pasirinkto valiutos rodinio ataskaitoje tos operacijos rodomos apskaitos valiuta, t.y., JAV doleriais (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Valiutos filtro ir valiutos rodymo kombinacijos

Šioje lentelėje pateikiami ataskaitos rezultatai, **·**  **kurie** gali atsirasti dėl įvairių pasirinkčių derinių valiutos rodymo ir valiutos filtro langeliuose dėl pasirinktų pasirinkčių. Funkcinė valiuta yra USD.


| Langelis Valiutos rodinys                        | Langelis Valiutos filtras | Ataskaitos rezultatas |
|----------------------------------------------|----------------------|---------------|
| Operacijos valiuta                 | **JENA**              | **Y6 000** – rezultate rodomos tik tos operacijos, kurios buvo įvestos JPY. |
| Apskaitos valiuta iš didžiosios knygos | **JENA**              |**$60** – rezultate rodomos tik tos operacijos, kurios buvo įvestos JPY, ir jos rodomos USD.<p><strong>Pastaba:</strong> konvertavimo kursas yra maždaug 100 JPY už 1 USD.</p> |
| Apskaitos valiuta iš didžiosios knygos | Tuščias                | **2 310 USD** – rezultate visi duomenys rodomi apskaitos valiuta, kuri nurodyta DK.<p><strong>Pastaba:</strong> ši suma yra visų apskaitos valiuta nurodomų operacijų suma.</p> |
| Operacijos valiuta                 | Tuščia                | **$2,250** – rezultate visos sumos rodomos ta valiuta, kuria buvo atlikta operacija. Tai reiškia, kad bendra suma sudedama iš sumų skirtingomis valiutomis. |

### <a name="calculation-column-in-a-column-definition"></a>Skaičiavimo stulpelis yra stulpelio apibrėžimas

Stulpelio apibrėžimo stulpelio tipas **CALC** palaiko langelio **Formulė** sudėtinius skaičiavimus ir gali apimti ženklus **+**, **-**, **\**ir*/** bei sakinius **IF / THEN / ELSE**. Skaičiavimo stulpelyje taip pat gali būti nuoroda į bet kurį kitą stulpelį, net paskesnius stulpelius. Be to, skaičiavimo stulpelyje taip pat gali būti nurodyti finansiniai metai ir laikotarpis, kad būtų palaikomos stulpelio antraštės. Skaičiavimo formulė gali būti iki 1024 raidinių-skaitinių simbolių ilgio. Norėdami pateikti skaičiavimo rezultatą procentais, naudokite specialų formato nepaisymą.

> [!NOTE]
> Skaičiavimo formulių rezultatai neapima verčių nespausdinamuose stulpelių diapazonuose. Pavyzdžiui, **A:D** spausdina **0** (nulis), o nespausdinamų reikšmių **A+B+C** apskaičiuoja reikšmę.

#### <a name="operators-in-calculation-columns"></a>Skaičiavimo stulpelių ženklai

Norėdami sudėti, atimti, padauginti, arba padalyti stulpelius, įveskite stulpelio raides skaičiavimo tvarka, tada, naudodami atitinkamą ženklą, atskirkite kiekvieną stulpelio raidę. Toliau pateikiamoje lentelėje paaiškinami ženklai, kuriuos galite naudoti skaičiavimo stulpelyje.

| Operatorius | Skaičiavimo pavyzdys | aprašymas |
|----------|---------------------|-------------|
| +        | A+C                 | Pridėti stulpelio A sumą prie stulpelio C sumos. |
| :        | A:C A:C-D           | Pridėti paskesnių stulpelių intervalą. Pavyzdžiui, formulė **A:C** sudeda sumas nuo stulpelio A iki stulpelio C, o formulė **A:C-D** sudeda sumas nuo stulpelio A iki stulpelio C ir atima stulpelio D sumą. |
| -        | A-C                 | Iš A stulpelyje esančios sumos atimama C stulpelyje esanti suma.<p><strong>Pastaba.</strong> Norėdami pakeisti stulpelio ženklus, taip pat galite naudoti minuso ženklą (-). Pavyzdžiui, norėdami pridėti atvirkštinę stulpelio A sumą prie stulpelio B sumos, naudokite <strong>-A+B</strong>.</p> |
| \*       | A\*C                | Padauginti stulpelio A sumą iš stulpelio C sumos. |
| /        | A/C                 | Padalinti stulpelio A sumą iš stulpelio C sumos. |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Skaičiavimo formulės naudojimas stulpelio apibrėžime

1. Ataskaitų konstruktoriuje atidarykite stulpelio apibrėžimą, norėdami modifikuoti.
2. Atitinkamo stulpelio **CALC** langelyje **Formulė** įveskite formulę.

#### <a name="complex-calculations"></a>Sudėtiniai skaičiavimai

Sudėtinis skaičiavimas gali būti sudarytas iš bet kokios langelio nuorodų, ženklų, reikšmių kombinacijos sudėtinių skliaustelių lygių. Pavyzdžiui, norėdami apskaičiuoti stulpelių A ir B vidurkį, naudokite skaičiavimo formulę **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Ataskaitos langelių nurodymas atliekant stulpelio skaičiavimą

Įvesdami stulpelio raidę ir eilutės kodą galite nurodyti konkretų ataskaitos langelį. Pavyzdžiui, **B.100** nurodo stulpelio B eilutės kodą 100. Visą stulpelį galite padalinti pagal tame pačiame stulpelyje esančią atskirą ataskaitos langelio sumą. Pavyzdžiui, skaičiavimas **B/B.100** reiškia, kad stulpelio B suma turėtų būti padalijama iš stulpelio B eilutės kodo 100 reikšmės. Jei skaičiavime nurodomas stulpelis, kuris priklauso nuo kito stulpelio, pirmiausia apdorojamas priklausantis stulpelis. Jeigu stulpelyje nurodote kitą stulpelį, kuris vėl nurodo pirmąjį stulpelį, bus rodoma ciklinės nuorodos klaida.

> [!NOTE]
> Šis skaičiavimas gali būti netikslus, jei pakeisite atskaitos skaičiavimo prioritetą. Skaičiavimo prioritetą galite nustatyti ataskaitos aprašo skirtuke **Parametrai**.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Stulpelio dauginimas arba dalijimas iš pagrindinės eilutės

Galite sukurti stulpelį, kuriame visos reikšmės rodomos konkrečiame stulpelyje kaip procentinė pagrindinio skaičiaus dalis. Todėl galite rodyti ryšius tarp eilučių, pvz., pardavimo eilutės procentinę dalį arba visų išlaidų eilutės procentinę dalį. Norėdami padauginti arba padalyti kiekvieną konkretaus stulpelio eilutę iš pagrindinės eilutės, įveskite skaičiavime naudotiną stulpelį, tada įveskite **\*BASEROW** arba **/BASEROW**. Pavyzdžiui, įveskite **C\*BASEROW** arba **C/BASEROW**.

> [!NOTE]
> Kai naudojate pagrindinės eilutės skaičiavimą stulpelių apraše, įsitikinkite, kad visuose šiame stulpelių apraše naudojamuose eilučių aprašuose būtų bent viena skaičiuojant naudojama pagrindinė eilutė.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Stulpelio sumos padalijimas į laikotarpių skaičių

Galite padalyti stulpelio sumą į nurodytą laikotarpių skačių. Pavyzdžiui, formulė **B/laikotarpiai** padalija stulpelio B reikšmę į stulpelyje B nurodytą laikotarpių skaičių. Jei skaičiavimas apima kelis stulpelius, nurodykite skaičiuojant naudojamą laikotarpių skaičių. Pavyzdžiui, formulė **(B+C)/laikotarpiai** sudeda stulpelio B ir stulpelio C sumas, o tada padalija rezultatą iš laikotarpio reikšmės.

## <a name="additional-resources"></a>Papildomi ištekliai

[Finansinių ataskaitų dizaino įrankio eilučių aprašai](row-definitions-financial-reporting.md)

[Išplėstinės finansinių ataskaitų formatavimo parinktys](advanced-formatting-options-financial-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
