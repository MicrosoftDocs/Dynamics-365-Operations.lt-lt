---
title: Finansinių ataskaitų apžvalga
description: Šioje temoje paaiškinama, kur galima pasiekti „Microsoft Dynamics 365 Finance“ finansines ataskaitas ir kaip naudoti finansinių ataskaitų galimybes.
author: aprilolson
ms.date: 07/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 464092ae2fdcdfd8a0ada254e88f4418c825c1f9
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486975"
---
# <a name="get-started-with-financial-reporting"></a>Pradėkite naudoti finansines ataskaitas 

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kur galima pasiekti „Financial Reporting” ir kaip naudoti „Financial Reporting” galimybes. Ji taip pat apima pateikiamų numatytųjų finansinių ataskaitų aprašymą.

## <a name="accessing-financial-reporting"></a>Prieiga prie finansinių ataskaitų

Galite prieiti prie **„Financial reporting“** meniu šiose vietose:

- **Didžioji knyga** &gt; **Užklausos ir ataskaitos**
- **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Pagrindinio biudžeto sudarymas**
- **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Biudžeto planavimas**
- **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Biudžeto kontrolė**.
- Konsolidacija

Norėdami sukurti ir generuoti juridinio subjekto finansinių ataskaitų, turite nustatyti tolesnę to juridinio subjekto informaciją.

- Finansinis kalendorius
- Didžioji knyga
- Sąskaitų planas
- Valiuta
- Publikuokite transakciją mažiausiai į vieną sąskaitą
- Pagrindinė sąskaita yra įrašyta į **pasirinktą** stulpelį **Finansinės ataskaitos nustatymai** Puslapį (**DK > DK nustatymai > Finansinių ataskaitų nustatymai**)

## <a name="granting-security-access-to-financial-reporting"></a>Saugios prieigos prie „Financial Reporting“

Finansinių ataskaitų funkcijomis gali naudotis naudotojai, kuriems, naudojant jų saugos vaidmenis, priskirtos atitinkamos teisės ir pareigos. Tolesniuose skyriuose išvardijamos šios teisės ir pareigos bei susietieji vaidmenys.

### <a name="duties"></a>Pareigos

| Pareigų žymė                            | Aprašas                                                             | AOT pavadinimas                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Tvarkyti finansinių ataskaitų saugą | Tvarkyti „Financial Reporting” saugą ir atlikti administravimo užduotis. | FinancialReportsSecurityMaintain |
| Tvarkyti finansines ataskaitas            | Kurti ir tvarkyti finansines ataskaitas.                                  | FinancialReportsMaintain         |
| Generuoti finansines ataskaitas            | Generuoti ir atnaujinti finansines ataskaitas.                                 | FinancialReportsGenerate         |
| Peržiūrėti finansinę veiklą          | Peržiūrėti ir analizuoti finansinę veiklą.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Teisės

| Teisės žymė                       | Aprašas                                                             | AOT pavadinimas                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Tvarkyti finansinių ataskaitų saugą | Tvarkyti „Financial Reporting” saugą ir atlikti administravimo užduotis. | FinancialReportsSecuritySystemMaintain |
| Tvarkyti finansines ataskaitas            | Kurti ir tvarkyti finansines ataskaitas.                                  | FinancialReportsMaintainReports  |
| Generuoti finansines ataskaitas            | Generuoti ir atnaujinti finansines ataskaitas.                                 | FinancialReportsGenerateReports  |
| Peržiūrėti finansines ataskaitas                | Peržiūrėti finansines ataskaitas.                                                 | FinancialReportsView             |

### <a name="roles"></a>Vaidmenys

| Teisės žymė                       | Muitas                                  | Vaidmenys                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Tvarkyti finansinių ataskaitų saugą | Tvarkyti „Financial Reporting” saugą | Saugos administratorius                                                          |
| Tvarkyti finansines ataskaitas            | Tvarkyti finansines ataskaitas            | Apskaitos vadovas, Apskaitos prižiūrėtojas, Finansų kontrolierius, Biudžeto vadovas |
| Generuoti finansines ataskaitas            | Generuoti finansines ataskaitas            | Vadovas, Vyriausiasis finansininkas, Buhalteris                                                            |
| Peržiūrėti finansines ataskaitas                | Peržiūrėti finansinę veiklą          | Nepriskirtas joks                                                                   |

Pridėjus naudotoją ar pakeitus vaidmenį, naudotojas finansines ataskaitas turėtų galėti pasiekti po kelių minučių. 

> [!NOTE]
> Sistemos administratoriaus vaidmuo yra įtraukiamas į visus finansinių ataskaitų rengimo vaidmenis.

## <a name="report-deletions-and-expirations"></a>Ataskaitų naikinimai ir galiojimo pabaiga

Vartotojai, kurie sugeneruoja ataskaitą, gali panaikinti savo ataskaitas. Vartotojai, kurių pareiga **Prižiūrėti finansinių ataskaitų saugą**, gali panaikinti kitų ataskaitas. 

Pradedant nuo 10.0.8 versijoje buvo pristatytas galiojimo pabaigos terminų konceptas. Nauja būtina savybė bus įjungta savybės **Visi** puslapyje per funkcijos valdymo darbo sritį. Funkcijoje **Finansinių ataskaitų saugojimo strategijos** yra toliau pateikti keitimai.
* Naujai sukurtos ataskaitos bus automatiškai sužymėtos kaip turinčios 90 dienų galiojimo laiko pabaigą nuo jų sukūrimo momento.
* Visoms esamoms ataskaitoms, buvusioms iki įdiegiant funkciją, bus suteiktas 90 dienų galiojimo laikotarpis. Data gali būti rodoma kaip tuščia trumpam laikotarpiui, kol bus paleista „Financial reporting” tarnyba, kai sugeneruojama ataskaita, tarnyba atlieka naujinimą esamoms ataskaitoms su tuščia galiojimo data. 
* Vartotojai, turintys **Prižiūrėti finansinių ataskaitų saugą**, turi prieigą prie šios funkcijos. Bet kuris vartotojas, turintis pareigą **Prižiūrėti finansines ataskaitas** pagal suteiktą teisę **Prižiūrėti finansinių ataskaitų galiojimo pabaigą** taip pat turės galimybę keisti galiojimo laikotarpį. Šiuo metu yra prieinamos dvi sulaikymo parinktys: 

    * 90 dienų galiojimo laikotarpis.
    * Galimybė nustatyti, kad ataskaita niekada nebaigtų galioti.

Pasirinkus galiojimo pabaigą, tokią kaip 90 dienų, 90 dienų taikoma nuo šiandien. Tai skirtingas elgesys nei 90 dienų nuo pradinės sukūrimo datos nustatymo, kai buvo sugeneruota ataskaita. 

Kuriant būsimas funkcijas bus apsvarstytos papildomos parinktys. 90 dienų galiojimo laikotarpis bus numatytasis, o vartotojai, turintys atitinkamas teises, galės perrašyti numatytąsias reikšmes sąrašo puslapyje **Finansinės ataskaitos**.

## <a name="default-reports"></a>Numatytosios ataskaitos

Finansinių ataskaitų modulyje pateikiamos 22 numatytosios finansinės ataskaitos. Kiekviena ataskaita naudoja numatytąsias pagrindinės sąskaitos kategorijas. Šias ataskaitas galite naudoti tokias, kokios jo yra, arba kaip pradinį tašką savo finansinių ataskaitų poreikiams tenkinti. Be tradicinių finansinių ataskaitų, pvz., Pajamų išrašo ir Balanso, tarp šių numatytųjų ataskaitų yra ataskaitų, kuriose rodomi galimi kurti skirtingi finansinių ataskaitų tipai. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Numatytoji ataskaita                                                                                         | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 mėnesių nuoseklusis vieno stulpelio pajamų išrašas – numatyt. | Peržiūrėkite organizacijos pastarųjų 12 mėnesių pelningumą viename stulpelyje.                                                                                                                                                                                                                                      |
| 12 mėnesių pajamų tendencijos išrašas – numatyt.                 | Peržiūrėkite organizacijos pelningumą kiekvienam iš pastarųjų 12 mėnesių. Šie 12 mėnesių gali apimti daugiau kaip vienus ataskaitinius metus.                                                                                                                                                                                             |
| Faktinis, palyginti su biudžeto – numatyt.                                | Peržiūrėkite išsamią visų pradinio biudžeto sąskaitų informaciją ir patikslintą biudžetą palyginkite su faktinėmis sumomis, turinčiomis nuokrypį.                                                                                                                                                                          |
| Audito informacija – numatyt.                                  | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje ataskaitų valiuta ir vietos valiuta rodomi debeto ir kredito balansai bei papildoma operacijų informacija, pvz., naudotojo ID, naudotojas, kuris paskutinis modifikavo duomenis, paskutinio modifikavimo data ir žurnalo ID. |
| Balansų sąrašas – numatyt.                                   | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje rodomi pradinis bei galutinis likučiai ir dabartinio laikotarpio bei metų iki šios dienos debeto ir kredito balansai bei papildoma operacijų informacija, pvz., kvitas.                                                                    |
| Balansas – numatyt.                                   | Peržiūrėti organizacijos metų finansinę padėtį.                                                                                                                                                                                                                                                             |
| Balansas ir Pajamų išrašas greta vienas kito – numatyt. | Peržiūrėkite organizacijos metų finansinę padėtį ir pelningumą lygiagrečiai.                                                                                                                                                                                                                              |
| Grynųjų pinigų srautas – numatyt.                                       | Gaukite įžvalgų apie grynuosius pinigus, kurie ateina į organizaciją ir iš jos išeina.                                                                                                                                                                                                                                   |
| Išsami JE ir TB peržiūra – numatyt.                      | Peržiūrėkite visų sąskaitų pradinį balansą ir veiklos informaciją.                                                                                                                                                                                                                                                      |
| [Išsamus bandomasis balansas – numatyt.](trial-balance-financial-reports.md)| Peržiūrėkite visų sąskaitų, turinčių debeto bei kredito balansų, balanso informaciją ir jų grynąją reikšmę, taip pat operacijos datą, kvitą ir žurnalo aprašą.                                                                                                                                  |
| Trejų metų ketvirčių išlaidų tendencija – numatyt.             | Gaukite įžvalgų apie pastarųjų trejų metų 12 ketvirčių išlaidas.                                                                                                                                                                                                                                   |
| Finansinių JE ir TB antraščių peržiūra – numatyt.            | Peržvelkite turto balansų ir veiklos, įsipareigojimų, savininko kapitalo, įplaukų, išlaidų, pelno arba nuostolių finansines antraštes.                                                                                                                                                                           |
| [Pajamų išrašas – numatyt.](income-statement-financial-report.md)| Peržiūrėkite organizacijos dabartinio laikotarpio ir šių metų iki šios dienos pelningumą.                                                                                                                                                                                                                                   |
| DK operacijų sąrašas – numatyt.                        | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje rodomi debeto ir kredito balansai bei papildoma operacijų informacija, pvz., operacijos data, žurnalo numeris, kvitas, registravimo tipas ir sekimo numeris.                                                                            |
| Koeficientai – numatyt.                                          | Peržiūrėkite organizacijos metų mokumo, pelningumo ir efektyvumo koeficientus.                                                                                                                                                                                                                           |
| Nuoseklios 12 mėnesių išlaidos – numatyt.                       | Gaukite įžvalgų apie kiekvieno iš pastarųjų 12 mėnesių išlaidas. Šie 12 mėnesių gali apimti daugiau kaip vienus ataskaitinius metus.                                                                                                                                                                                                       |
| Nuoseklusis ketvirčio pajamų išrašas – numatyt.               | Peržiūrėkite organizacijos praėjusių metų ir metų iki šios dienos pelningumą kas ketvirtį.                                                                                                                                                                                                                   |
| Sugretintas balansas – numatyt.                      | Peržiūrėti organizacijos metų finansinę padėtį. Šioje ataskaitoje vienas šalia kito rodomi turtas ir įsipareigojimai bei akcininko kapitalas.                                                                                                                                                                                |
| [Bandomojo balanso suvestinė – numatyt.](trial-balance-financial-reports.md)| Peržiūrėkite visų sąskaitų su pradiniu bei galutiniu balansais balanso informaciją bei debeto ir kredito balansus ir jų grynąjį skirtumą.                                                                                                                                                                  |
| [Bandomojo balanso suvestinė metams bėgant – numatyt.](trial-balance-financial-reports.md)| Peržiūrėkite visų sąskaitų su pradiniu bei galutiniu balansais balanso informaciją bei debeto ir kredito balansus ir jų šių bei praėjusių metų grynąjį skirtumą.                                                                                                                           |
| Savaitės pardavimai ir nuolaidos – numatyt.                     | Gaukite įžvalgų apie kiekvienos mėnesio savaitės pardavimus ir nuolaidas. Šioje ataskaitoje nurodyta bendroji keturių savaičių suma.                                                                                                                                                                                                              |
| Turimos biudžeto lėšos – numatyt.                         | Peržiūrėkite visų sąskaitų patikslinto biudžeto, faktinių išlaidų, biudžeto rezervavimų ir biudžeto lėšų išsamų palyginimą.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finansinių ataskaitų atidarymas

Kai pasirenkate **„Financial Reporting“** meniu, yra rodomas bendrovės nustatytųjų finansinių ataskaitų sąrašas. Tada galite ataskaitą atidaryti arba modifikuoti. Norėdami atidaryti vieną iš numatytųjų ataskaitų, pasirinkite ataskaitos pavadinimą. Pirmą kartą atidarant ataskaitą, ji automatiškai sugeneruojama už praėjusį mėnesį. Pvz., jei pirmą kartą ataskaitą atidarote 2019 m. rugpjūtį, ataskaita generuojama 2019 m. liepos 31 dienai. Kai ataskaita atidaroma, galite pradėti ją tyrinėti detalizuodami konkrečius duomenis ir keisdami ataskaitos parinktis.

## <a name="creating-and-modifying-financial-reports"></a>Finansinių ataskaitų kūrimas ir modifikavimas

Finansinių ataskaitų sąraše galite kurti naują ataskaitą arba modifikuoti esamą ataskaitą. Jei neturite reikiamų leidimų, galite sukurti naują finansinę ataskaitą pasirinkdami **Nauja** veiksmų juostoje. Į jūsų įrenginį atsisiunčiama ir jame paleidžiama ataskaitų dizaino įrankio programa. Paleidus ataskaitų kūrimo įrankį galima kurti naują ataskaitą. Kai turite naująją ataskaitą, ji atsiranda finansinių ataskaitų sąraše. Sąraše rodomos tik tos ataskaitas, kurios buvo sukurtos jūsų bendrovėje jums naudojant „Dynamics 365 Finance“. 

## <a name="reporting-tree-definitions"></a>Ataskaitų medžio apibrėžimai

Viena iš dalių, kuri naudojama finansinių ataskaitų kūrimui, yra ataskaitų medžio sąvoka. Ataskaitų kūrimo aprašas padeda nustatyti organizacijos struktūrą ir hierarchiją. Kelių dimensijų hierarchijų struktūra pagrįsta finansinių duomenų dimensijų ryšiais. Jis suteikia informacijos ataskaitinių vienetų lygiu ir suvestinės lygiu visiems medžio vienetams.

Galite sukurti neribotą skaičių ataskaitų medžių tam, kad parodytumėte savo organizacijos duomenis įvairiais būdais. Visi ataskaitų medžiai gali turėti bet kokią skyrių ir santraukų vienetų kombinaciją, tačiau ataskaitos sąvoka gali susieti tik su vienu ataskaitų medžiu vieną kartą. 

## <a name="update-the-financial-reporting-version-through-slipstreaming"></a>Atnaujinti „Financial reporting” versiją per paprastesnę įdiegtį

„Finance and Operations” programos yra atnaujinamos kas mėnesį. Tačiau „Financial reporting” nebūtinai yra atnaujinamos pagal tokį dažnį. Be to, klientai turi daugiau parinkčių, kada įdiegti „Finance and Operations” programų naujinimus. „Financial reporting” atnaujinimai įdiegiami automatiškai. „Financial reporting” turi numatytąją versiją, naudojama kliento aplinkoje, kai įdiegtas tarnybos naujinimas, kai inicijuojama prastova, arba tada, kai kliento aplinka veikia priežiūros režimu. Šis procesas vadinamas *paprastesne* arba *teisingesne* įdiegtimi, kadangi visi kliento diegimui nustatomi į vienodą „Financial reporting” versiją.

Pakeitimus, atliktus kiekvienoje versijoje, galima rasti [Kas naujo ar pasikeitė „Dynamics 365 Finance”](../../finance/get-started/whats-new-home-page.md). Kiekvieno leidimo puslapio apačioje esančiame skyriuje „Papildomi ištekliai” galima rasti platformos naujinimus ir klaidų pataisas.

Pasirinkta paprastesnė įdiegties versija yra peržiūrėta ir patikrinta „Financial reporting” versija, paruošta gamybai. Ji suderinama su bet kuria ankstesne arba būsima „Dynamics 365 Finance” versija. Pavyzdžiui, „Financial reporting” versija gali būti naujausias 10.0.19 leidimas, o kliento programos versija vis dar yra 10.0.16.

> [!NOTE]
> Vienintelis atvejis, kai klientai gali pereiti prie ankstesnės versijos (ankstesnės versijos scenarijus) įvyksta tada, kai „Microsoft” sustabdo teisingą išvestį dėl trikties. Kai tik pataisymas bus galimas, jis bus taikomas automatiškai.

Paprastesnės įdiegties procesas yra visiškai automatizuotas ir nereikalaujama jokių kliento veiksmų. Trys topologijos naudoja paprastesnę įdiegti, kiekviena jų šiek tiek skirtingai:

- **Vietinis** – Vietiniams diegimams nepalaikomi paprastesnė įdiegtis ir „teisingieji” diegimai.
- **Infrastruktūra kaip tarnyba (IaaS)** – Paprastesnės įdiegties logika yra taikoma bet kurios operacijos, kuri bando atnaujinti „Financial reporting”, metu. Tai apima dvejetainius naujinimus arba transliacijas, turinčias dvejetainius naujinimus.
- **Savitarnos paslauga** – bet kuri operacija, kuriai reikalinga „Financial reporting” prastova, taiko paprastesnės įdiegties logiką:

    - Dvejetainiai naujinimai arba transliacijos, turinčios dvejetainius naujinimus
    - S pataisymai arba kitos infrastruktūros prastovos
    - AOT paketo diegimai

## <a name="troubleshooting-issues-opening-report-designer"></a>Trikčių šalinimo problemų atidarymas „Report Designer“

Esama keletos trikdžių, kurie gali sukelti problemų atidarant „Report Designer“. Šie trikdžiai ir sprendimo žingsniai yra pateikti toliau.

Trikdis 1: „Report Designer“ neįsijungia jums pasirinkus **Naujas** ar **Redaguoti**.

* „Internet Explorer“ pasirinkite **Nustatymai** ir tuomet pasirinkite **Interneto parinktys**. Pasirinkite **Saugos** skirtuką. Pasirinkite patikimas svetaines ir pasirinkite **Svetainės**. **Įtraukti šią interneto svetainę į sritį** įveskite "\*\.dynamics.com" (be kabučių) ir tuomet pasirinkite **Įtraukti**. 
* „Internet Explorer“ pasirinkite **Nustatymai** ir tuomet pasirinkite **Interneto parinktys**. Pasirinkite **Saugos** skirtuką. Pasirinkite patikimas svetaines. Srityje pavadintoje Saugumo lygis šiai sričiai, pakeiskite parinktį į **Vidutinis-Žemas**.
* Išjunkite iššokančių langų blokavimo programą savo naršyklėje.
* Darbo stotyse būtina įdiegti „Microsoft .NET Framework“ 4.6.2 ar aukštesnę versiją. Šią „Microsoft .NET Framework“ versiją galima atsisiųsti ir įdiegti apsilankius puslapyje [„Microsoft“ atsisiuntimo centras](https://www.microsoft.com/download/details.aspx?id=53345).
* Jei naudojate naršyklę „Chrome“, turite įdiegti plėtinį „ClickOnce“, kad atsisiųstumėte ataskaitų dizaino įrankio klientą. Jei naršyklė „Chrome“ veikia inkognito režimu, įsitikinkite, kad plėtinys „ClickOnce“ nustatytas veikti inkognito režimu. Daugiau informacijos apie „Chrome“ plėtinį „ClickOnce“ žr. [Sistemos reikalavimai įdiegtims debesyje](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Jei naudojate „Microsoft Edge“ su „Chrome“ naršykle, jums nereikia įdiegti plėtinio „ClickOnce“, skirto „Edge Chromium“. Tačiau turite įjungti parinktį „ClickOnce“, kad atsisiųstumėte ataskaitų dizaino įrankio klientą. Jei dirbate neatpažintu režimu, įsitikinkite, kad „ClickOnce“ plėtinys yra įjungtas neatpažintu režimu.

    1. Atidarykite naują naršyklę „Microsoft Edge“.
    2. Įveskite **edge://flags** ir pasirinkite **Įvesti**.
    3. Suraskite parinktį **„ClickOnce“ pagalba** arba naudokite šią tiesioginę nuorodą: **edge://flags/#edge-click-once**.
    4. Nustatykite išplečiamojo meniu pasirinktį **Įjungta**.
    5. Pasirinkite **Iš naujo paleisti naršyklę**.

Triktis 2: Vartotojui nebuvo priskirti būtini leidimai naudoti „Financial reporting“. 

* Tam, kad patikrintumėte, ar vartotojas neturi leidimo, pasirinkite **Taip** klaidoje „Neįmanoma prisijungti prie „Financial reporting“ serverio“. Pasirinkite Taip, jeigu norite tęsti ir nurodyti kitą serverio adresą.” Tuomet pasirinkite **+ Testuoti ryšį**. Jei neturite leidimo, tuomet matysite pranešimą sakantį „Ryšio bandymas nepavyko. Vartotojas neturi reikiamų leidimų prisijungti prie serverio. Susisiekite su savo sistemos administratoriumi.”
* Reikiami leidimai yra išvardyti toliau [Saugios prieigos prie „Financial Reporting“ užtikrinimas](#granting-security-access-to-financial-reporting). „Financial Reporting“ saugumas priklauso nuo šių privilegijų. Neturėsite prieigos, nebent šios privilegijos (ar kitas saugumo vaidmuo su šiomis privilegijomis) yra jums priskirtos. 
* **Bendrovės vartotojo tiekėjas bendrovei** integravimo užduotis (kuri taip pat atsakinga už ir yra žinoma kaip vartotojo integravimas) veikia 5 minučių intervalu. Gali užtrukti iki 10 minučių, kol visi leidimai bus pakeisti tam, kad galiotų „Financial reporting“. 

    Jei kitas vartotojas gali atsidaryti „Report Designer“, pasirinkite **Įrankiai** ir tuomet pasirinkite **Integravimo būsena**. Patikrinkite, ar integravimo žemėlapis, „Bendrovės vartotojo tiekėjas bendrovei,“ sėkmingai buvo atliktas, nes jums buvo priskirtas leidimas naudoti „Financial reporting“. 

* Gali būti, kad kita klaida užkirto kelią **„Dynamics“ vartotojo integravimui su „Financial reporting“ vartotoju** užbaigimui. Arba gali būti, kad duomenų saugykla yra perkraunama ir veiksmas dar tęsiasi, arba įvyko kita sistemos klaida. Pabandykite atlikite procesą vėliau. Jei problema nepasišalina, susisiekite su sistemos administratoriumi.

Triktis 3: Galite praeiti pro **ClickOnce Report Designer** prisijungimo puslapį, bet negalite užbaigti prisijungimo su „Report Designer“. 

* Jūsų kompiuteryje nustatytas vietinis laikas, kai įeinate į savo prisijungimo informaciją, gali atsilikti penkias minutes nuo „Financial reporting“ serverio. Jei yra didesnis nei penkių minučių skirtumas, sistema neleis prisijungti. 
* Jei jūsų kompiuterio laikas skiriasi nuo finansinių ataskaitų serverio laiko, rekomenduojame įgalinti „Windows“ pasirinktį, kad būtų automatiškai nustatytas kompiuterio laikas. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>„report designer“ trikčių šalinimas naudojant įvykių peržiūros programą

Įvykių peržiūros programą galite naudoti kai kurioms problemoms, kurios kyla naudojant finansines ataskaitas, analizuoti. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Kas atsitinka, kai yra ryšių su finansinėmis ataskaitomis? 

Štai keletas veiksmų, kuriuos galite atlikti, kad pokalbis su „Microsoft“ palaikytų efektyvesnę ir kad galėtumėte greitai išspręsti. 
 
Toliau pateikiami veiksmai vyksta finansinių ataskaitų įvykių peržiūros programos pranešimų įjungimo proceso metu. Žurnalai, kuriuos generuoja įvykių peržiūros programa, padės inžinieriams greitai nustatyti ryšio problemos šaltinį. Pateikite šių žurnalų kopijas kartu su savo kvitu susisiekdami su palaikymo tarnyba.


1. Kopijuoti RegisterETW.zip failą į kliento darbo vietą (pageidautina darbalaukio) ir ištraukti [RegisterETW.zip](https://dev.azure.com/msdyneng/e6f12261-a46a-4af1-ac0c-e22bc2c5a478/_apis/git/repositories/ff923027-67f0-43fb-b63c-6d6b6423840f/Items?path=%2F.attachments%2FRegisterETW-c1a35291-6aa6-4462-a2bc-4ba117fd5f8e.zip&download=false&resolveLfs=true&%24format=octetStream&api-version=5.0-preview.1&sanitize=true&versionDescriptor.version=wikiMaster).
2. Įsitikinkite, kad „Windows Event" programa uždaryta.
3. Atidarykite „Administrator PowerShell“ komandinę eilutę ir pereikite į katalogą, kuriame yra RegisterETW.ps1.
4. Vykdykite šią komandą: .\RegisterETW.ps1

    Sėkminga „PowerShell" išvestis bus patikrinta naudojant pranešimą **Užbaigtas RegisterETW scenarijus**.

    Iš naujo atidarykite Įvykių peržiūros programą ir pamatysite šiuos žurnalus dalyje **„Microsoft” > „Dynamics”**:

    * MR-Klientas
    * „MR-DVT”
    * MR-Integravimas
    * MR-Registravimasis
    * MR-Ataskaitos
    * „MR_SchedulerTasks”
    * „MR-Sql”
    * „MR-TraceManager”

5. Perkurkite išdavimą „report designer“.
6. Eksportuokite MR-Logger įvykius naudodami įvykių peržiūros programą.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Trikčių šalinimas jungiantis prie finansinių ataskaitų

Problema: gaunate klaidą „Nepavyko prisijungti prie „Financial reporting” serverio".

* Nustatyti, ar problema kyla „Chrome“ ir „Edge“ interneto naršyklėse.
* Jei problema iškyla tik vienoje naršyklėje, tai gali būti ClickOnce išdavimas. 
* Kai gaunate ryšio klaidos pranešimą, pasirinkite **Tikrinti** ar nori patikrinti ryšį, kad pamatytumėte, koks pranešimas pasirodo. 
* Problema galėjo kilti todėl, kad kitas vartotojas neturi prieigos prie finansinių ataskaitų. Jei vartotojas neturi prieigos, jis gaus pranešimą, kuriame teigiama, kad neturi teisės.
* Jei problema iškyla keliose naršyklėse, įsitikinkite, kad jūsų darbo vietos laiko laikrodis nustatytas kaip Automatinis.
* Norėdami prisiregistruoti prie darbo vietos ir sužinoti, ar jis gali prisijungti, dirbkite su vartotojas, kuris turi saugos administratoriaus teises tinklo domene bei „Dynamics 365 Finance“ administratoriaus teises. Jei jos gali prisijungti, problema gali būti susijusi su tinklo teisėmis.
* Darbo vietoje laikinai išjunkite užkardą. Jei tada galėsite prisijungti prie „Report Designer“ problema bus susijusi su užkarda. Norėdami išspręsti problemą, dirbkite su savo organizacijos IT padaliniu.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Peržiūrėti finansines ataskaitas](view-financial-reports.md)
- [Ataskaitų dizaino įrankio ataskaitų medžio apibrėžtys](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
