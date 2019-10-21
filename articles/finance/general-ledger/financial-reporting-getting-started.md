---
title: Finansinių ataskaitų apžvalga
description: Šioje temoje paaiškinama, kur galima pasiekti „Microsoft Dynamics 365 Finance“ finansines ataskaitas ir kaip naudoti finansinių ataskaitų galimybes. Ji apima pateikiamų numatytųjų finansinių ataskaitų aprašymą.
author: aprilolson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: caa449feba22c5804799b5317a8e29c139cc440e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178990"
---
# <a name="financial-reporting-overview"></a>Finansinių ataskaitų apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kur galima pasiekti finansines ataskaitas ir kaip naudoti finansinių ataskaitų galimybes. Ji taip pat apima pateikiamų numatytųjų finansinių ataskaitų aprašymą.

<a name="accessing-financial-reporting"></a>Prieiga prie finansinių ataskaitų
-----------------------------

Meniu **Finansinės ataskaitos** galite rasti toliau nurodytose vietose.

-   **Didžioji knyga** &gt; **Užklausos ir ataskaitos**
-   **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Pagrindinio biudžeto sudarymas**
-   **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Biudžeto planavimas**
-   **Biudžeto sudarymas** &gt; **Užklausos ir ataskaitos** &gt; **Biudžeto kontrolė**.
-   Konsolidacija

Norėdami sukurti ir generuoti juridinio subjekto finansinių ataskaitų, turite nustatyti tolesnę to juridinio subjekto informaciją.

-   Finansinis kalendorius
-   Didžioji knyga
-   Sąskaitų planas
-   Valiuta

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

Pridėjus naudotoją ar pakeitus vaidmenį, naudotojas finansines ataskaitas turėtų galėti pasiekti po kelių minučių. **Pastaba.** Sistemos administratoriaus vaidmuo finansinėse ataskaitose įtrauktas į visus vaidmenis.

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
| Išsamus bandomasis balansas – numatyt.                         | Peržiūrėkite visų sąskaitų, turinčių debeto bei kredito balansų, balanso informaciją ir jų grynąją reikšmę, taip pat operacijos datą, kvitą ir žurnalo aprašą.                                                                                                                                  |
| Trejų metų ketvirčių išlaidų tendencija – numatyt.             | Gaukite įžvalgų apie pastarųjų trejų metų 12 ketvirčių išlaidas.                                                                                                                                                                                                                                   |
| Finansinių JE ir TB antraščių peržiūra – numatyt.            | Apžvelkite turto balansų ir veiklos, įsipareigojimų, savininko kapitalo, įplaukų, išlaidų, pelno arba nuostolių finansines antraštes.                                                                                                                                                                           |
| Pajamų išrašas – numatyt.                                | Peržiūrėkite organizacijos dabartinio laikotarpio ir metų iki šios dienos pelningumą.                                                                                                                                                                                                                                   |
| DK operacijų sąrašas – numatyt.                        | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje rodomi debeto ir kredito balansai bei papildoma operacijų informacija, pvz., operacijos data, žurnalo numeris, kvitas, registravimo tipas ir sekimo numeris.                                                                            |
| Koeficientai – numatyt.                                          | Peržiūrėkite organizacijos metų mokumo, pelningumo ir efektyvumo koeficientus.                                                                                                                                                                                                                           |
| Nuoseklios 12 mėnesių išlaidos – numatyt.                       | Gaukite įžvalgų apie kiekvieno iš pastarųjų 12 mėnesių išlaidas. Šie 12 mėnesių gali apimti daugiau kaip vienus ataskaitinius metus.                                                                                                                                                                                                       |
| Nuoseklusis ketvirčio pajamų išrašas – numatyt.               | Ketvirčiais peržiūrėkite organizacijos praėjusių metų ir metų iki šios dienos pelningumą.                                                                                                                                                                                                                   |
| Sugretintas balansas – numatyt.                      | Peržiūrėti organizacijos metų finansinę padėtį. Šioje ataskaitoje vienas šalia kito rodomi turtas ir įsipareigojimai bei akcininko kapitalas.                                                                                                                                                                                |
| Bandomojo balanso suvestinė – numatyt.                          | Peržiūrėkite visų sąskaitų su pradiniu bei galutiniu balansais balanso informaciją bei debeto ir kredito balansus ir jų grynąjį skirtumą.                                                                                                                                                                  |
| Bandomojo balanso suvestinė metams bėgant – numatyt.           | Peržiūrėkite visų sąskaitų su pradiniu bei galutiniu balansais balanso informaciją bei debeto ir kredito balansus ir jų šių bei praėjusių metų grynąjį skirtumą.                                                                                                                           |
| Savaitės pardavimai ir nuolaidos – numatyt.                     | Gaukite įžvalgų apie kiekvienos mėnesio savaitės pardavimus ir nuolaidas. Šioje ataskaitoje nurodyta bendroji keturių savaičių suma.                                                                                                                                                                                                              |
| Turimos biudžeto lėšos – numatyt.                         | Peržiūrėkite visų sąskaitų patikslinto biudžeto, faktinių išlaidų, biudžeto rezervavimų ir biudžeto lėšų išsamų palyginimą.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finansinių ataskaitų atidarymas
Kai spustelite **Finansinių ataskaitų** meniu, rodomas įmonės numatytųjų finansinių ataskaitų sąrašas. Tada galite ataskaitą atidaryti arba modifikuoti. Norėdami atidaryti vieną iš numatytųjų ataskaitų, pasirinkite ataskaitos pavadinimą. Pirmą kartą atidarant ataskaitą, ji automatiškai sugeneruojama už praėjusį mėnesį. Pvz., jei pirmą kartą ataskaitą atidarote 2016 m. rugpjūtį, ataskaita generuojama 2016 m. liepos 31 dienai. Kai ataskaita atidaroma, galite pradėti ją tyrinėti detalizuodami konkrečius duomenis ir keisdami ataskaitos parinktis.

## <a name="creating-and-modifying-financial-reports"></a>Finansinių ataskaitų kūrimas ir modifikavimas
Finansinių ataskaitų sąraše galite kurti naują ataskaitą arba modifikuoti esamą ataskaitą. Jei turite reikiamas teises, naują finansinę ataskaitą galite sukurti veiksmų srityje spustelėdami **Nauja**. Į jūsų įrenginį atsisiunčiama ir jame paleidžiama ataskaitų dizaino įrankio programa. Paleidus ataskaitų kūrimo įrankį galima kurti naują ataskaitą. Kai turite naująją ataskaitą, ji atsiranda finansinių ataskaitų sąraše. Sąraše pateikiamos tik tos įmonės, kurią naudojate programoje „Finance‟, sukurtos ataskaitos. 

> [!NOTE] 
> Kompiuteryje, į kurį atsisiunčiate ataskaitų dizaino įrankio klientą, turi būti įdiegta 4.6.2 „Microsoft .NET Framework“ versija. Šią „Microsoft .NET Framework“ versiją galima atsisiųsti ir įdiegti apsilankius puslapyje [„Microsoft“ atsisiuntimo centras](https://www.microsoft.com/download/details.aspx?id=53345). Jei naudojate „Chrome“, turite įdiegti plėtinį „ClickOnce“, kad galėtumėte atsisiųsti ataskaitų dizaino įrankį. Jei naršyklė veikia inkognito režimu, įsitikinkite, kad plėtinys „ClickOnce“ nustatytas veikti inkognito režimu. Ataskaitą, kuri atsiranda finansinių ataskaitų sąraše, taip pat galite modifikuoti. Kai pasirinkta sritis aplink ataskaitos pavadinimą, veiksmų srityje spustelėkite **Redaguoti**. Paleidžiama ataskaitų dizaino įrankio programa.

## <a name="additional-resources"></a>Papildomi ištekliai
- [Finansinių ataskaitų peržiūra](view-financial-reports.md)


