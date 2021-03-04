---
title: Finansinių ataskaitų apžvalga
description: Šioje temoje paaiškinama, kur galima pasiekti „Microsoft Dynamics 365 Finance“ finansines ataskaitas ir kaip naudoti finansinių ataskaitų galimybes.
author: aprilolson
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88436b4a5d6be4172e15fa4a9dadc34696417fb9
ms.sourcegitcommit: eec96c64f44d1b4877d49ee15665a774019d42d7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672449"
---
# <a name="get-started-with-financial-reporting"></a>Pradėkite su „Financial reporting“ 

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kur galima pasiekti finansines ataskaitas ir kaip naudoti finansinių ataskaitų galimybes. Ji taip pat apima pateikiamų numatytųjų finansinių ataskaitų aprašymą.

<a name="accessing-financial-reporting"></a>Prieiga prie finansinių ataskaitų
-----------------------------

Galite prieiti prie **„Financial reporting“** meniu šiose vietose:

-   **Didžioji knyga** &gt; **Užklausos ir ataskaitos**
-   **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Pagrindinio biudžeto sudarymas**
-   **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Biudžeto planavimas**
-   **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Biudžeto kontrolė**.
-   Konsolidacija

Norėdami sukurti ir generuoti juridinio subjekto finansinių ataskaitų, turite nustatyti tolesnę to juridinio subjekto informaciją.

-   Finansinis kalendorius
-   Ledger
-   Sąskaitų planas
-   Valiuta

## <a name="granting-security-access-to-financial-reporting"></a>Saugios prieigos prie „Financial Reporting“
Finansinių ataskaitų funkcijomis gali naudotis naudotojai, kuriems, naudojant jų saugos vaidmenis, priskirtos atitinkamos teisės ir pareigos. Tolesniuose skyriuose išvardijamos šios teisės ir pareigos bei susietieji vaidmenys.

### <a name="duties"></a>Pareigos

| Pareigų žymė                            | Prekės/Paslaugos pavadinimas                                                             | AOT pavadinimas                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Tvarkyti finansinių ataskaitų saugą | Tvarkyti finansinių ataskaitų saugą ir atlikti administravimo užduotis. | FinancialReportsSecurityMaintain |
| Tvarkyti finansines ataskaitas            | Kurti ir tvarkyti finansines ataskaitas.                                  | FinancialReportsMaintain         |
| Generuoti finansines ataskaitas            | Generuoti ir atnaujinti finansines ataskaitas.                                 | FinancialReportsGenerate         |
| Peržiūrėti finansinę veiklą          | Peržiūrėti ir analizuoti finansinę veiklą.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Teisės

| Teisės žymė                       | Prekės/Paslaugos pavadinimas                                                             | AOT pavadinimas                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Tvarkyti finansinių ataskaitų saugą | Tvarkyti finansinių ataskaitų saugą ir atlikti administravimo užduotis. | FinancialReportsSecuritySystemMaintain |
| Tvarkyti finansines ataskaitas            | Kurti ir tvarkyti finansines ataskaitas.                                  | FinancialReportsMaintainReports  |
| Generuoti finansines ataskaitas            | Generuoti ir atnaujinti finansines ataskaitas.                                 | FinancialReportsGenerateReports  |
| Peržiūrėti finansines ataskaitas                | Peržiūrėti finansines ataskaitas.                                                 | FinancialReportsView             |

### <a name="roles"></a>Vaidmenys

| Teisės žymė                       | Pareiga                                  | Vaidmenys                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Tvarkyti finansinių ataskaitų saugą | Tvarkyti finansinių ataskaitų saugą | Saugos administratorius                                                          |
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
* Visoms esamoms ataskaitoms, buvusioms iki įdiegiant funkciją, bus suteiktas 90 dienų galiojimo laikotarpis. Data gali būti rodoma kaip tuščia trumpam laikotarpiui, kol bus paleista finansinių ataskaitų tarnyba, kai sugeneruojama ataskaita, tarnyba atlieka naujinimą esamoms ataskaitoms su tuščia galiojimo data. 
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
| 12 mėnesių nuoseklusis vieno stulpelio pajamų išrašas – numatyt. | Viename stulpelyje peržiūrėkite organizacijos pastarųjų 12 mėnesių pelningumą.                                                                                                                                                                                                                                      |
| 12 mėnesių pajamų tendencijos išrašas – numatyt.                 | Peržiūrėkite organizacijos kiekvieno iš pastarųjų 12 mėnesių pelningumą. Šie 12 mėnesių gali apimti daugiau kaip vienus ataskaitinius metus.                                                                                                                                                                                             |
| Faktinis, palyginti su biudžeto – numatyt.                                | Peržiūrėkite išsamią visų pradinio biudžeto sąskaitų informaciją ir patikslintą biudžetą palyginkite su faktinėmis sumomis, turinčiomis nuokrypį.                                                                                                                                                                          |
| Audito informacija – numatyt.                                  | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje ataskaitų valiuta ir vietos valiuta rodomi debeto ir kredito balansai bei papildoma operacijų informacija, pvz., naudotojo ID, naudotojas, kuris paskutinis modifikavo duomenis, paskutinio modifikavimo data ir žurnalo ID. |
| Balansų sąrašas – numatyt.                                   | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje rodomi pradinis bei galutinis likučiai ir dabartinio laikotarpio bei metų iki šios dienos debeto ir kredito balansai bei papildoma operacijų informacija, pvz., kvitas.                                                                    |
| Balansas – numatyt.                                   | Peržiūrėti organizacijos metų finansinę padėtį.                                                                                                                                                                                                                                                             |
| Balansas ir Pajamų išrašas greta vienas kito – numatyt. | Vieną greta kito peržiūrėkite organizacijos metų finansinę padėtį ir pelningumą.                                                                                                                                                                                                                              |
| Grynųjų pinigų srautas – numatyt.                                       | Gaukite įžvalgų apie grynuosius pinigus, kurie ateina į organizaciją ir iš jos išeina.                                                                                                                                                                                                                                   |
| Išsami JE ir TB peržiūra – numatyt.                      | Peržiūrėkite visų sąskaitų pradinį balansą ir veiklos informaciją.                                                                                                                                                                                                                                                      |
| [Išsamus bandomasis balansas – numatyt.](trial-balance-financial-reports.md)| Peržiūrėkite visų sąskaitų, turinčių debeto bei kredito balansų, balanso informaciją ir jų grynąją reikšmę, taip pat operacijos datą, kvitą ir žurnalo aprašą.                                                                                                                                  |
| Trejų metų ketvirčių išlaidų tendencija – numatyt.             | Gaukite įžvalgų apie pastarųjų trejų metų 12 ketvirčių išlaidas.                                                                                                                                                                                                                                   |
| Finansinių JE ir TB antraščių peržiūra – numatyt.            | Apžvelkite turto balansų ir veiklos, įsipareigojimų, savininko kapitalo, įplaukų, išlaidų, pelno arba nuostolių finansines antraštes.                                                                                                                                                                           |
| [Pajamų išrašas – numatyt.](income-statement-financial-report.md)| Peržiūrėkite organizacijos dabartinio laikotarpio ir metų iki šios dienos pelningumą.                                                                                                                                                                                                                                   |
| DK operacijų sąrašas – numatyt.                        | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje rodomi debeto ir kredito balansai bei papildoma operacijų informacija, pvz., operacijos data, žurnalo numeris, kvitas, registravimo tipas ir sekimo numeris.                                                                            |
| Koeficientai – numatyt.                                          | Peržiūrėkite organizacijos metų mokumo, pelningumo ir efektyvumo koeficientus.                                                                                                                                                                                                                           |
| Nuoseklios 12 mėnesių išlaidos – numatyt.                       | Gaukite įžvalgų apie kiekvieno iš pastarųjų 12 mėnesių išlaidas. Šie 12 mėnesių gali apimti daugiau kaip vienus ataskaitinius metus.                                                                                                                                                                                                       |
| Nuoseklusis ketvirčio pajamų išrašas – numatyt.               | Ketvirčiais peržiūrėkite organizacijos praėjusių metų ir metų iki šios dienos pelningumą.                                                                                                                                                                                                                   |
| Sugretintas balansas – numatyt.                      | Peržiūrėti organizacijos metų finansinę padėtį. Šioje ataskaitoje vienas šalia kito rodomi turtas ir įsipareigojimai bei akcininko kapitalas.                                                                                                                                                                                |
| [Bandomojo balanso suvestinė – numatyt.](trial-balance-financial-reports.md)| Peržiūrėkite visų sąskaitų su pradiniu bei galutiniu balansais balanso informaciją bei debeto ir kredito balansus ir jų grynąjį skirtumą.                                                                                                                                                                  |
| [Bandomojo balanso suvestinė metams bėgant – numatyt.](trial-balance-financial-reports.md)| Peržiūrėkite visų sąskaitų su pradiniu bei galutiniu balansais balanso informaciją bei debeto ir kredito balansus ir jų šių bei praėjusių metų grynąjį skirtumą.                                                                                                                           |
| Savaitės pardavimai ir nuolaidos – numatyt.                     | Gaukite įžvalgų apie kiekvienos mėnesio savaitės pardavimus ir nuolaidas. Šioje ataskaitoje nurodyta bendroji keturių savaičių suma.                                                                                                                                                                                                              |
| Turimos biudžeto lėšos – numatyt.                         | Peržiūrėkite visų sąskaitų patikslinto biudžeto, faktinių išlaidų, biudžeto rezervavimų ir biudžeto lėšų išsamų palyginimą.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finansinių ataskaitų atidarymas
Kai pasirenkate **„Financial Reporting“** meniu, yra rodomas bendrovės nustatytųjų finansinių ataskaitų sąrašas. Tada galite ataskaitą atidaryti arba modifikuoti. Norėdami atidaryti vieną iš numatytųjų ataskaitų, pasirinkite ataskaitos pavadinimą. Pirmą kartą atidarant ataskaitą, ji automatiškai sugeneruojama už praėjusį mėnesį. Pvz., jei pirmą kartą ataskaitą atidarote 2019 m. rugpjūtį, ataskaita generuojama 2019 m. liepos 31 dienai. Kai ataskaita atidaroma, galite pradėti ją tyrinėti detalizuodami konkrečius duomenis ir keisdami ataskaitos parinktis.

## <a name="creating-and-modifying-financial-reports"></a>Finansinių ataskaitų kūrimas ir modifikavimas
Finansinių ataskaitų sąraše galite kurti naują ataskaitą arba modifikuoti esamą ataskaitą. Jei neturite reikiamų leidimų, galite sukurti naują finansinę ataskaitą pasirinkdami **Nauja** veiksmų juostoje. Į jūsų įrenginį atsisiunčiama ir jame paleidžiama ataskaitų dizaino įrankio programa. Paleidus ataskaitų kūrimo įrankį galima kurti naują ataskaitą. Kai turite naująją ataskaitą, ji atsiranda finansinių ataskaitų sąraše. Sąrašasr rodo tik ataskaitas, kurios buvo sukurtos jūsų bendrovėje jums naudojant „Dynamics 365 Finance“. 

## <a name="reporting-tree-definitions"></a>Ataskaitų medžio apibrėžimai 
Viena iš dalių, kuri naudojama finansinių ataskaitų kūrimui, yra ataskaitų medžio sąvoka. Ataskaitų kūrimo aprašas padeda nustatyti organizacijos struktūrą ir hierarchiją. Kelių dimensijų hierarchijų struktūra pagrįsta finansinių duomenų dimensijų ryšiais. Jis suteikia informacijos ataskaitinių vienetų lygiu ir suvestinės lygiu visiems medžio vienetams.

Galite sukurti neribotą skaičių ataskaitų medžių tam, kad įvairiais būdais parodytumėte savo organizacijos duomenis. Visi ataskaitų medžiai gali turėti bet kokią skyrių ir santraukų vienetų kombinaciją, tačiau ataskaitos sąvoka gali susieti tik su vienu ataskaitų medžiu vieną kartą. 


## <a name="troubleshooting-issues-opening-report-designer"></a>Trikčių šalinimo problemų atidarymas „Report Designer“
Esama keletos trikdžių, kurie gali sukelti problemų atidarant „Report Designer“. Šie trikdžiai ir sprendimo žingsniai yra pateikti toliau.

Trikdis 1: „Report Designer“ neįsijungia jums pasirinkus **Naujas** ar **Redaguoti**.

* „Internet Explorer“ pasirinkite **Nustatymai** ir tuomet pasirinkite **Interneto parinktys**. Pasirinkite **Saugos** skirtuką. Pasirinkite patikimas svetaines ir pasirinkite **Svetainės**. **Įtraukti šią interneto svetainę į sritį** įveskite "\*\.dynamics.com" (be kabučių) ir tuomet pasirinkite **Įtraukti**. 
* „Internet Explorer“ pasirinkite **Nustatymai** ir tuomet pasirinkite **Interneto parinktys**. Pasirinkite **Saugos** skirtuką. Pasirinkite patikimas svetaines. Srityje pavadintoje Saugumo lygis šiai sričiai, pakeiskite parinktį į **Vidutinis-Žemas**.
* Išjunkite iššokančių langų blokavimo programą savo naršyklėje.
* Darbo stotyse būtina įdiegti „Microsoft .NET Framework“ 4.6.2 ar aukštesnę versiją. Šią „Microsoft .NET Framework“ versiją galima atsisiųsti ir įdiegti apsilankius puslapyje [„Microsoft“ atsisiuntimo centras](https://www.microsoft.com/download/details.aspx?id=53345).
* Jei naudojate naršyklę „Chrome“, turite įdiegti plėtinį „ClickOnce“, kad atsisiųstumėte ataskaitų dizaino įrankio klientą. Jei naršyklė „Chrome“ veikia inkognito režimu, įsitikinkite, kad plėtinys „ClickOnce“ nustatytas veikti inkognito režimu. Daugiau informacijos apie „Chrome“ plėtinį „ClickOnce“ žr. [Sistemos reikalavimai įdiegtims debesyje](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements).
* Jei naudojate „Microsoft Edge“ su „Chrome“ naršykle, jums nereikia įdiegti plėtinio „ClickOnce“, skirto „Edge Chromium“. Tačiau turite įjungti parinktį „ClickOnce“, kad atsisiųstumėte ataskaitų dizaino įrankio klientą. Jei dirbate neatpažintu režimu, įsitikinkite, kad „ClickOnce“ plėtinys yra įjungtas neatpažintu režimu.
     1. Atidarykite naują naršyklę „Microsoft Edge“.
     2. Įveskite **edge://flags** ir pasirinkite **Įvesti**.
     3. Suraskite parinktį **„ClickOnce“ pagalba** arba naudokite šią tiesioginę nuorodą: **edge://flags/#edge-click-once**.
     4. Nustatykite išplečiamojo meniu pasirinktį **Įjungta**.
     5. Pasirinkite **Iš naujo paleisti naršyklę**.

Triktis 2: Vartotojui nebuvo priskirti būtini leidimai naudoti „Financial Reporting“. 

* Tam, kad patikrintumėte, ar vartotojas neturi leidimo, pasirinkite **Taip** klaidoje, „Neįmanoma prisijungti prie „Financial Reporting“ serverio“. Pasirinkite Taip, jei norite tęsti ir nurodyti kitą serverio adresą.” Tuomet pasirinkite **+ Testuoti ryšį**. Jei neturite leidimo, tuomet matysite pranešimą sakantį „Ryšio bandymas nepavyko. Vartotojas neturi reikiamų leidimų prisijungti prie serverio. Susisiekite su sistemos administratoriumi.”
* Reikiami leidimai yra išvardyti toliau [Saugios prieigos prie „Financial Reporting“ užtikrinimas](#granting-security-access-to-financial-reporting). „Financial Reporting“ saugumas priklauso nuo šių privilegijų. Neturėsite prieigos, nebent šios privilegijos (ar kitas saugumo vaidmuo su šiomis privilegijomis) yra jums priskirtos. 
* **Bendrovės vartotojo tiekėjas bendrovei** integravimo užduotis (kuri taip pat atsakinga už ir yra žinoma kaip vartotojo integravimas) veikia 5 minučių intervalu. Gali užtrukti iki 10 minučių, kol visi leidimai bus pakeisti tam, kad galiotų „Financial Reporting“. 
  Jei kitas vartotojas gali atsidaryti „Report Designer“, pasirinkite **Įrankiai** ir tuomet pasirinkite **Integravimo būsena**. Patikrinkite, ar integravimo žemėlapis, „Bendrovės vartotojo tiekėjas bendrovei,“ sėkmingai buvo atliktas, nes jums buvo priskirtas leidimas naudoti „Financial Reporting“. 
* Gali būti, kad kita klaida užkirto kelią **„Dynamics“ vartotojo integravimas su „Financial Reporting“ vartotoju** užbaigimui. Arba gali būti, kad duomenų saugykla yra perkraunama ir veiksmas dar tęsiasi, arba įvyko kita sistemos klaida. Pabandykite atlikite procesą vėliau. Jei problema nepasišalina, susisiekite su sistemos administratoriumi.

Triktis 3: Galite praeiti pro „ClickOnce Report Designer“ prisijungimo puslapį, tačiau negalite užbaigti prisijungimo prie „Report Designer“. 

* Jūsų kompiuteryje nustatytas vietinis laikas, kai įeinante į savo prisijungimo informaciją, gali atsilikti penkias minutes nuo „Financial Reporting“ serverio. Jei yra didesnis nei penkių minučių skirtumas, sistema neleis prisijungti. 
* Tuo atveju, rekomenduojame įjungti „Windows“ parinktį, kad nustatytumėte savo kompiuterio laiką automatiniu būdu. 

## <a name="additional-resources"></a>Papildomi ištekliai
- [Peržiūrėti finansines ataskaitas](view-financial-reports.md)
- [Ataskaitų dizaino įrankio ataskaitų medžio apibrėžtys](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]