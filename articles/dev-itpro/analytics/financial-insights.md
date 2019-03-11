---
title: Finansinės įžvalgos
description: Darbo srityje Finansų įžvalgos naudojant „Microsoft Power BI“, kartu pateikiami pagrindiniai efektyvumo indikatoriai (KPI), diagramos ir finansinės ataskaitos.
author: kweekley
manager: AnnBe
ms.date: 08/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 2c261d2aea66b578bc976a66b6184384f0a5bf5d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "308856"
---
# <a name="financial-insights"></a>Finansinės įžvalgos

[!include [banner](../includes/banner.md)]

Darbo srityje **Finansų įžvalgos** naudojant „Microsoft Power BI“ kartu pateikiami pagrindiniai efektyvumo indikatoriai (KPI), diagramos ir finansinės ataskaitos. „Power BI“ yra įdėtas į „Microsoft Dynamics 365 for Finance and Operations“. Darbo srityje **Finansinės įžvalgos** dėmesys skiriamas analizės ataskaitoms. Visos organizacijos asmenys gali peržiūrėti, tirti, suprasti ir veikti. 

Sujungdama didžiosios knygos ir papildomų knygų duomenis, darbo sritis **Finansinės įžvalgos** pateikia visapusiškesnį organizacijos finansinės padėties vaizdą.

> [!NOTE]
> Šiame dokumente naudojama tolesnė „Power BI“ terminija.
> 
> - **Ataskaita** – atskiras .pbix failas, kuriame įrašomi visi visų skirtukų vaizdiniai elementai.
> - **Puslapis** – atskiro .pbix failo skirtukas. Kiekviename puslapyje gali būti vienas ar keli vaizdiniai elementai.
> - **Vaizdinis elementas** – vienas duomenų šaltinis, pvz., kortelė, KPI, diagrama, grafikas, matrica ar finansinė ataskaita. Puslapyje, kuriame kaip vaizdinis elementas naudojama finansinė ataskaita, kitų vaizdinių elementų būti negali dėl duomenų, apie kuriuose rengiamos ataskaitos, dydžio.

Šiuo metu naudojant darbo sritį **Finansinės įžvalgos** galima peržiūrėti aktyvaus juridinio subjekto arba visų juridinių subjektų duomenis. Būsimuose leidimuose ši darbo sritis virs vieta, kurioje naudodami „Power BI“ galėsite redaguoti ir kurti vaizdinius elementus.

Darbo srityje **CFO apžvalga** rodomi tie patys vaizdiniai elementai, kaip ir darbo srityje **Finansinės įžvalgos**, tačiau joje galite peržiūrėti ir filtruoti esamų ataskaitų duomenis. Būsimuose leidimuose į darbo sritį **Finansinės įžvalgos** galėsite įtraukti naujų vaizdinių elementų. Nauji vaizdiniai elementai taip pat gali būti pasiekiami darbo srityse, orientuotose į kitus vaidmenis, pvz., projektų vadovus ar mokėtinų sumų vadovus. Darbo srityje **CFO apžvalga** toliau rodomi visų juridinių subjektų duomenys, nesvarbu, prie kurių juridinių subjektų vaidmuo turi prieigą.

## <a name="finance-and-operations-setup"></a>„Finance and Operations“ sąranka
**Didžioji knyga**

Pagrindinės sąskaitos tipu ir pagrindinių sąskaitų kategorijomis užpildomos atitinkamos numatytosios pagrindinės sąskaitos, esančios darbo srities **Finansinės įžvalgos** finansinėje ataskaitoje **Balansas** ir įvairiose finansinėse ataskaitose **Pajamų išrašas**.

Puslapyje **Pagrindines sąskaitos** turite nustatyti savo pagrindinę sąskaitą, kad jai būtų priskirtas vienas iš tolesnių tipų.

- Įplaukos
- Expense
- Turtas
- Skolos
- Kapitalas

Savo pagrindinėms sąskaitoms nepriskirkite jokio kito pagrindinės sąskaitos tipo, pvz., **Balansas** ar **Pelnas ir nuostolis**. Ataskaitų įrankis negali nustatyti pagrindinės sąskaitos tipo, kai priskirti kiti pagrindinės sąskaitos tipai, nes jie nėra pakankamai detalūs. Turi būti nustatytas toks pagrindinės sąskaitos tipas, kad finansinėse ataskaitose įsipareigojimai ir įplaukos būti rodomi kaip teigiamos sumos.

Kad pagrindinės sąskaitos būtų rodomos finansinėse ataskaitose ir įtrauktos į įvairius kitus vaizdinius elementus, pvz., KPI, kiekvienai iš jų reikia priskirti pagrindinės sąskaitos kategoriją. Pagrindinės sąskaitos kategorijas patobulintos – į jas įtraukta rodymo tvarka. Rodymo tvarka naudojama konkrečiai darbo srities **Finansinės įžvalgos** finansinėse ataskaitose. Redagavę ar įtraukę naują pagrindinės sąskaitos kategoriją, galite pakeisti reikšmę **Rodymo tvarka**, kad nustatytumėte tvarką, kuria pagrindinės sąskaitos kategorijos turėtų būti rodomos finansinėje ataskaitoje. Jei turite pakeisti kelių pagrindinės sąskaitos kategorijų rodymo tvarką, galite naudoti funkciją Atidaryti programoje „Excel“ ir keitimus greitai redaguoti bei publikuoti sprendime „Finance and Operations“.

## <a name="entity-store"></a>Objekto parduotuvė
Darbo srities **Finansinės įžvalgos** duomenys imami iš objektų saugyklos (**Sistemos administravimas** \> **Sąranka** \> **Objektų saugykla**). Jei atidarote darbo sritį **CFO apžvalga** arba **Finansinės įžvalgos** ir vaizdiniuose elementuose rodomas tolesnis įspėjamasis pranešimas, turite atnaujinti objektus.

![Perspėjimas](./media/Cantdisplay.png)

Kad darbo srityse **Finansinės įžvalgos** ir **CFO apžvalga** matytumėte duomenis, turite atnaujinti tolesnius objektus.

- CustCollectionsBIMeasurements
- FinancialReportingOtherData
- FinancialReportingReferenceData
- FinancialReportingTransactionData
- LedgerCovLiquidityMeasurement
- Pirkimo kubas
- Pardavimo kubas

Ankstesniame leidime objektai LedgerActivityMeasure ir VendPaymentBIMeasure buvo naudojami darbo srities **CFO apžvalga** duomenims. Tačiau dabartiniame leidime jie nebenaudojami.

Galite nustatyti pasikartojančią paketinę užduotį, kuri reguliariai atnaujintų objektų duomenis. Kadangi kiekvienas naujinamas objektas yra visiškai perkuriamas, atidžiai pasirinkite objektų naujinimo laiką ir dažnį. Pagrindinis finansinėse ataskaitose naudojamas objektas yra FinancialReportingTransactionData. Todėl galite nuspręsti šį objektą naujinti dažniau.

## <a name="security"></a>Sauga
Šiuo metu įdėtosiose „Power BI“ ataskaitose negalima pateikti tik tų juridinių subjektų, prie kurių vartotojas turi prieigą, duomenų. Todėl įdėtosios „Power BI“ ataskaitos kontroliuojamos naudojant saugos sąrankos pareigas. Nustatytos pareigos leidžia pasiekti visų juridinių subjektų arba tik aktyvios įmonės duomenis. Toliau pateikiamoje lentelėje parodytos esamos pareigos ir joms priskirti vaidmenys. Atsižvelgiant į jūsų organizacijos reikalavimus, pareigas galima pašalinti arba priskirti skirtingiems vaidmenims.

| Pareiga                                    | Vaidmenys | Aprašas |
|-----------------------------------------|-------|------------|
| Peržiūrėti CFO peržiūros darbo sritį             | Finansų direktorius | Ši pareiga suteikia prieigą prie darbo srities CFO apžvalga. Pagal numatytuosius parametrus kaip filtras naudojama aktyvioji įmonė. Tačiau galite įtraukti visus juridinius subjektus, nesvarbu, ar vartotojas turi prieigą prie kitų juridinių subjektų. |
| Finansinių dabartinės įmonės įžvalgų peržiūra | <ul><li>Buhalteris</li><li>Apskaitos vadovas</li><li>Apskaitos prižiūrėtojas</li><li>Auditorius</li><li>Biudžeto vadybininkas</li><li>Generalinis direktorius</li><li>Finansų direktorius</li><li>Finansų kontrolierius</li></ul> | Ši pareiga suteikia prieigą prie darbo srities Finansinės įžvalgos. Pagal numatytuosius parametrus kaip filtras naudojama aktyvioji įmonė. Kitų juridinių subjektų įtraukti negalite. |
| Finansinių visų įmonių įžvalgų peržiūra   | Sprendime „Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3“ ši pareiga vaidmeniui nepriskirta. Būsimame leidime ši pareiga bus paskirta vaidmeniui Finansų direktorius. | Ši pareiga suteikia prieigą prie darbo srities CFO apžvalga meniu elemento. Pagal numatytuosius parametrus kaip filtras naudojama aktyvioji įmonė. Tačiau galite įtraukti visus juridinius subjektus, nesvarbu, ar vartotojas turi prieigą prie kitų juridinių subjektų. |


## <a name="financial-reporting-vs-finanical-insights"></a>Finansinės ataskaitos ir finansinės įžvalgos
**Finansinės įžvalgos** apima finansines ataskaitas, tačiau tai nepakeičia „Finance and Operations“ modulio Finansinės ataskaitos. Numatytųjų darbo srities **Finansinės įžvalgos** finansinių ataskaitų aprėptis yra ribota ir į šią darbo sritį įtraukti ne visi finansinių ataskaitų tipai. Modulis Finansinės ataskaitos vis dar yra pagrindinis įstatymų nustatytų finansinių ataskaitų projektavimo, kūrimo ir generavimo įrankis.

Ši palyginamoji diagrama padės atskirti šias dvi parinktis:


|                                                          | Finansinės ataskaitos                                               | Finansinės įžvalgos |
|----------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| **Numatytųjų ataskaitų redagavimas**                                 | Taip                                                               | Nr. |
| **Naujų ataskaitų kūrimas**                                   | Taip                                                               | Nr. |
| **Ataskaitų spausdinimas**                                        | Taip                                                               | Nr. |
| **Eksportuoti į Excel**                                      | Taip                                                               | Ribotas neapdorotų duomenų eksportavimas į „Excel“, neformatuota ataskaita |
| **Palaiko ataskaitų hierarchiją / organizacinę hierarchiją**   | Taip                                                               | Nr. |
| **Papildomos knygos duomenų ataskaita**                             | Taip Apsiriboja tik tiekėju, klientu                              | Taip Tiekėjo, kliento, tiekėjo / kliento grupės, tiekėjo / kliento adresai ir t. t. |
| **Ataskaitų valiuta**                                   | Taip Apskaitos valiuta konvertuojama į ataskaitų valiutą       | Ne Tik apskaitos valiuta |
| **Sauga**                                             | Taip Laikomasi „Finance and Operations” ir ataskaitų medžio saugumo | Ribota Visų įmonių (neatsižvelgiant į „Finance and Operations” saugumą) arba tik aktyvios įmonės ataskaitų peržiūra |
| **Palaiko skirtingus sąskaitų planus ir finansinius metus** | Taip                                                               | Nr. |
| **išorinių duomenų ataskaitos**                              | Nr.                                                                | Nr. |
| **Palaiko konsolidacijas**                               | Taip                                                               | Ribota Galima teikti kelių įmonių ataskaitas, bet naudoti tik apskaitos valiutą |

Be naujos vartotojo sąsajos pradinėje darbo srityje **CFO apžvalga**, dabar yra ir nauji KPI, diagramos bei finansinės ataskaitos. Galimos tolesnės finansinės ataskaitos.

- Bandomasis balansas
- Balanso lapas
- Pajamų išrašas pagal regioną
- Pajamų išrašas – faktinis, palyginti su biudžeto
- Pajamų išrašas su nuokrypiais
- 12 mėnesių pajamų tendencijos išrašas
- Trejų metų išlaidų tendencija
- Išlaidos pagal tiekėją
- Pardavimas pagal klientą

## <a name="edit-visuals"></a>Vaizdinių elementų redagavimas
Pradiniame darbo srities **Finansinės įžvalgos** leidime negalima redaguoti jokių vaizdinių elementų. Būsimuose leidimuose atitinkamas saugos teises turintys vartotojai galės kurti naujus vaizdinius elementus, kopijuoti esamus ir vaizdinius elementus redaguoti. Nors .pbix failai su ataskaitomis yra prieinami kaip ištekliai, nerekomenduojame redaguoti numatytųjų ataskaitų. Bus papildomai keičiamas duomenų modelis, numatytosios ataskaitos ir pasirinktinė finansinė ataskaita, naudojami kurti finansines ataskaitas. Todėl, norėdami pasinaudoti naujomis būsimo leidimo funkcijomis ir duomenų modelio pakeitimais, turėsite perdaryti visus atliktus numatytųjų ataskaitų keitimus naudodami „Microsoft Power BI Desktop“.

## <a name="filtering"></a>Filtravimas
Vartotojai ataskaitą gali filtruoti naudodami kairėje esančią sritį **Filtras**. Tai – ta pati sritis, kuri pasiekiama naudojant „Power BI Desktop“. Yra įvairių filtravimo lygių, kai kurie iš jų gali būti neprieinami – tai priklauso nuo to, ką pasirinkote puslapyje (skirtuke), arba to, ar naudojate detalizavimo galimybes.

- **Ataskaitos lygio filtrai** – šie filtrai taikomi visiems visų puslapių (skirtukų) vaizdiniams elementams.
- **Puslapio lygio filtrai** – šie filtrai taikomi visiems aktyvaus skirtuko vaizdiniams elementams. Šie filtrai taikomi ant ataskaitos lygio filtrų viršaus.
- **Vaizdinio elemento lygio filtrai** – šie filtrai taikomi tik pasirinktam vaizdiniam elementui. Šie filtrai taikomi ant puslapio lygio filtrų viršaus.
- **Detalizavimo filtras** – šis filtras filtruoja iš „šaltinio“ vaizdinio elemento, taikomo dabartiniam vaizdiniam elementui, kai šaltinio vaizdinį elementą detalizuojate iki dabartinio vaizdinio elemento.

![Filtras](./media/filter.png)

Norėdami pašalinti konkrečią filtro reikšmę, pasirinkite šalia esantį trintuko simbolį. Nešalinkite filtro pasirinkdami X. Jei pasirenkate X, jūsų filtruojamas laukas pašalinamas kaip filtro parinktis. Jei netyčia pašalinate kokį nors filtro lauką, uždarykite ir vėl atidarykite darbo sritį. Bus vėl pritaikyti numatytieji filtrų parametrai.

Pagal numatytuosius parametrus, pirmą kartą atidarant darbo sritis, kaip ataskaitos lygio filtras naudojamas aktyvusis juridinis subjektas. Vartotojams gali būti leidžiama įtraukti kitų juridinių subjektų arba pakeisti filtre pasirinktą numatytąjį juridinį subjektą – tai priklauso nuo vartotojų saugos teisių.

Filtras **Ataskaitinis kalendorius** reikalingas, kad būtų naudojamas teisingas vaizdinio elemento kalendorius. Pagal numatytuosius parametrus ataskaitos lygio filtras nustatomas kaip aktyvaus juridinio subjekto ataskaitinis kalendorius. Jei filtrą nustatysite kaip ataskaitinį kalendorių su skirtinga pradžios arba pabaigos data, pradžios balansai nebus įtraukti. Todėl jūsų finansinėse ataskaitose **Balansas** nebus rodomi teisingi balansai. Jei filtre pasirinksite papildomą ataskaitinį kalendorių, galėsite naudoti papildomų stulpelių. Kiekvienuose papildomuose stulpeliuose rodomos kito ataskaitinio kalendoriaus sumos.

Taip pat reikalingas filtras **Registravimo sluoksnis**. Pagal numatytuosius parametrus šis filtras nustatytas kaip Dabartinis. Filtre galite pasirinkti papildomų registravimo sluoksnių, kad būtų rodomos sujungtos sumos.

Filtrus taip pat galima naudoti su laukais **Data** ir **Finansiniai metai**. Paprastai šie filtrai taikomi puslapio lygiu. Pagal numatytuosius parametrus filtras **Data** naudoja reliacinę datą, kurią galite keisti. Taip pat galite pašalinti reliacinės datos filtrą ir vietoj jos naudoti filtrą **Finansiniai metai**.

## <a name="currency"></a>Valiuta

Visi vaizdiniai elementai, teikiantys ataskaitas apie didžiosios knygos duomenis, sumas rodo apskaitos valiuta. Todėl, filtruodami juridinį subjektą, turite būti atidūs ir įtraukti tik tuos juridinius subjektus, kurie naudoja tą pačią apskaitos valiutą. Kitu atveju duomenis sujungsite skirtingomis valiutomis.

Visi vaizdiniai elementai, teikiantys ataskaitas apie papildomų knygų duomenis, pvz., vaizdiniai elementai **Pinigų srautų prognozė** ir **10 viršutinių**, sumas rodo sistemos valiuta. Sistemos valiuta ir sistemos valiutos kurso tipas nustatomi puslapyje **Sistemos parametrai**.

Vaizdinis elementas **Balansas pagal banko sąskaitą** naudoja sumas banko sąskaitų valiuta.

## <a name="dimensions"></a>Dimensijos

Numatytosiose finansinėse ataskaitose nėra jokių finansinių dimensijų, jos orientuotos tik į pagrindinę sąskaitą. Finansinės dimensijos bus palaikomos būsimuose leidimuose, kai ataskaitas bus galima redaguoti. Organizacijos tada galės filtruoti finansinių dimensijų reikšmes.

Kai kuriose finansinėse ataskaitose yra dimensijų, pagrįstų papildomų knygų operacijomis. Naujųjų finansinių ataskaitų tikslas – įjungti filtravimo funkciją dimensijose, kurios nenustatytos kaip finansinės dimensijos. Pavyzdžiui, numatytojoje ataskaitoje Išlaidos pagal tiekėją galite išplėsti žemiau pagrindinės sąskaitos, kad matytumėte balansus, suskirstytus pagal tiekėją. Tiekėjas nėra nustatytas kaip finansinė dimensija. Vietoj to, kad rastų tiekėją, sistema grįžtą į pradinę papildomos knygos operaciją.

Numatytosiose ataskaitose naudojamos tolesnės dimensijos. Nė viena iš šių dimensijų yra finansinė.

- Tiekėjas
- Tiekėjų grupė
- Klientas
- Klientų grupė
- Šalis/regionas
- Rajonas / apskritis
- Miestas

> [!IMPORTANT] 
> Jei kelių viename kvite esančių tiekėjų ar klientų operacijas apibendrinsite naudodami finansinius žurnalus, duomenys bus neteisingi. Ataskaitų įrankis negali nustatyti, kuris tiekėjas ar klientas yra susijęs su konkrečia žurnalo įraše nurodyta DK sąskaita, nes ši informacija niekur netvarkoma. Todėl nerekomenduojame viename kvite įvesti kelių tiekėjų, klientų, ilgalaikio turto ar projektų.

## <a name="drill-on-data"></a>Duomenų detalizavimas

Naudojant „Power BI“ galimi įvairūs detalizavimo lygiai. Skiriasi kiekvieno lygio pavadinimas ir funkcijos. Taip pat gali detalizuoti eilutes ir stulpelius. Šiame skyriuje aptariamos įvairios parinktys kaip pavyzdį naudojant finansinę ataskaitą **Bandomasis balansas** ir parodant, kaip galite detalizuoti eilutes. Tas pačias funkcijas galima naudoti ir su stulpeliais. Tiesiog turite pakeisti parametrą **Detalizuoti**.

Tolesnėje iliustracijoje ataskaita **Bandomasis balansas** sutraukta iki aukščiausio eilučių hierarchijos lygio – pagrindinės sąskaitos tipo.

![Bandomasis balansas](./media/trial-balance.png)

Norėdami peržiūrėti tolesnį hierarchijos lygį – pagrindinių sąskaitų kategorijas – galite lauką **Detalizuoti** nustatyti kaip **Eilutės**, o tada pasirinkti mygtuką **Išplėsti** (trečiasis mygtukas po lauko Detalizuoti). Dabar matote išplėstas visas pagrindinių sąskaitų kategorijas. Šiuo metu „Power BI“ neleidžia išplėsti tik vienos eilutės ar stulpelio, tačiau vis tiek matyti visas kitas eilutes ar stulpelius.

![Bandomasis balansas](./media/trial-balance2.png)

Norėdami hierarchiją išplėsti iki visų eilučių pagrindinių sąskaitų, galite vėl naudoti mygtuką **Išplėsti**. Tačiau, norėdami iki pagrindinių sąskaitų detalizuoti tik vieną eilutę, pirmiausia pasirinkite mygtuką **Detalizuoti** (viena žemyn nukreipta rodyklė dešinėje lango pusėje) ir tada pasirinkite detalizuotiną eilutę. Tolesnėje iliustracijoje parodytas vaizdas, kada, pasirinkus mygtuką **Detalizuoti**, pasirenkama eilutė **Pardavimas**.

![Bandomasis balansas](./media/trial-balance3.png)

Detalizavus vieną eilutę, norint grįžti į visą bandomąjį balansą reikia kelis kartus spustelėti pele. Mygtuku **Pereiti prie bendresnio** (pirmas mygtukas po lauko **Detalizuoti**) prie bendresnių elementų pereinama tik kategorijos **Pardavimas** kontekste, kaip pavaizduota tolesnėje iliustracijoje.

![Bandomasis balansas](./media/trial-balance4.png)

Galite toliau naudoti mygtuką **Pereiti prie bendresnio**, kad grįžtumėte į aukščiausią eilučių apibendrinimo lygį.

Sprendime „Power BI“ taip pat yra mygtukas, leidžiantis pereiti į tolesnį hierarchijos lygį (antras mygtukas po lauko **Detalizuoti**). Šis mygtukas veikia skirtingai nei mygtukas **Išplėsti** (trečias mygtukas po lauko **Detalizuoti**), kuriuo išplečiama hierarchija. Kai išplečiate hierarchiją, ji tvarkoma ataskaitoje. Pavyzdžiui, kaip buvo parodyta anksčiau, jei išplečiate pagrindinės sąskaitos tipą, jį vis tiek matote ataskaitoje. Tačiau, kai pereinate į tolesnį hierarchijos lygį, ataskaitoje pirminis hierarchijos lygis neberodomas, kaip parodyta tolesnėje iliustracijoje.

![Bandomasis balansas](./media/trial-balance5.png)

Norėdami peržiūrėti apibendrintų balansų operacijų informaciją, galite pasirinkti kai kurias sumas detalizuoti atgal į „Financial and Operations“.

Detalizuojant atgal iš finansinių ataskaitų, pereinama į apskaitos šaltinių naršyklę (ASE), o ne į kvito operacijas. ASE naršyklėje rodomi ne tik didžiosios knygos apskaitos įrašai. Vietoj to joje rodoma išsami informacija apie papildomos knygos operaciją. Todėl gaunate daug daugiau informacijos apie pradinę operaciją ir ją galite naudoti analizei. Pavyzdžiui, galite matyti, kas buvo tiekėjas arba klientas, ką pirko klientas ar pardavė tiekėjas, ir net koks projektas buvo įtrauktas į operaciją.

Į ASE siunčiami tolesni finansinių ataskaitų filtrai, kad ASE rodytų sujungtas operacijas.

Būtini laukai norint filtruoti:

- Juridinis subjektas
- Finansinis kalendorius
- Metai
- Pagrindinės sąskaitos ID

Pasirenkami laukai norint filtruoti:

- Ketvirtis
- Mėnuo
- Laikotarpis

Jei pakankamai neišskleidžiate eilutės, detalizavimo funkcija neveikia. Pavyzdžiui, jei išplečiate žemyn tik iki pagrindinių sąskaitų kategorijos, balanse iki ASE detalizuoti negalite, nes pagrindinė sąskaita yra būtinas laukas norint filtruoti ASE naršyklėje.

Jei eilutę išplečiate per daug, papildomi finansinių ataskaitų filtrai nėra siunčiami į ASE. Todėl galite matyti skirtingus skaičius. Pavyzdžiui, jei finansinės ataskaitos Pajamų išrašas pagal regioną eilutėse išplečiate žemyn iki šalies ar regiono, šalis ar regionas nėra įtraukiami kaip ASE filtras.

> [!NOTE]
> Finansinių ataskaitų eilutes ar stulpelius galite detalizuoti labiau nei šiuo metu ASE palaikoma filtravimo funkcija. Todėl kai kuriose situacijose išsamių ASE operacijų suma nesutaps su atgal detalizuojamu balansu. Ši funkcija toliau bus tobulinama ateityje.

## <a name="hierarchies"></a>Hierarchijos

Numatytosiose finansinėse ataskaitose duomenys detalizuojami ir iškleidžiami naudojant dvi hierarchijas. Viena hierarchija skirta eilutėms, o kita hierarchija skirta stulpeliams. Abi hierarchijos yra iš anksto nustatomos kuriant finansinę ataskaitą. Daugumos finansinių ataskaitų eilučių hierarchija yra **Pagrindinės sąskaitos tipas** \> **Pagrindinių sąskaitų kategorijos** \> **Pagrindinė sąskaita**. Tačiau kai kuriose ataskaitose yra papildomų laukų, pvz., Šalis ir Regionas. Papildomi hierarchijos mazgai pagrįsti kiekvienos operacijos papildomos knygos duomenimis.

Stulpelių hierarchija orientuota į juridinius subjektus ir ataskaitinius laikotarpius. Daugumos finansinių ataskaitų stulpelių hierarchija yra **Juridinis subjektas** \> **Ataskaitinis kalendorius** \> **Finansiniai metai** \> **Ketvirtis** \> **Laikotarpis**.

Šiuo metu finansinės ataskaitos nepalaiko organizacijų hierarchijų, leidžiančių jungti duomenis.

## <a name="data-limitations"></a>Duomenų apribojimai
Finansinių ataskaitų vaizdiniuose elementuose ribojamas galimų rodyti eilučių skaičius. Šiuo metu nustatytas limitas yra 30 000. Jei viršysite šį limitą, vaizdiniame elemente bus įspėjamasis simbolis, pranešantis apie šią situaciją.

![Duomenų apribojimai](./media/data-limit.png)

Jei viršijamas didžiausias skaičius, finansinėje ataskaitoje rodomos bendrosios sumos bus neteisingos, nes į vaizdinį elementą bus įkeltos ne visos eilutės.

### <a name="empty-rows"></a>Tuščios eilutės
Sprendime „Power BI“ nėra parinkties slėpti ir rodyti tuščias eilutes. Jei eilutėje nėra duomenų, ji vaizdiniame elemente nebus rodoma.


## <a name="additional-resources-for-power-bi"></a>Papildomi „Power BI“ ištekliai

Norint gamybos aplinkoje įjungti įdėtąsias darbo sričių **CFO apžvalga** arba **Finansinės įžvalgos** ataskaitas, tolesnių išteklių informacija nėra būtina. Jie yra naudingi dirbant su kūrimo langeliais ir jei norite į „Finance and Operations“ įdėti savo „Power BI“ ataskaitų.

- <https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/>

- <https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces>
