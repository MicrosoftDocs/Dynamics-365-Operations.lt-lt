---
title: "Finansinės ataskaitos"
description: "Šioje temoje aprašoma, kur galima pasiekti finansinės atskaitomybės Microsoft Dynamics 365 operacijoms ir kaip naudotis finansinių ataskaitų teikimo galimybės. Ji apima numatytąjį finansines ataskaitas, pateiktas apibūdinimas."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>Finansinės ataskaitos

Šioje temoje aprašoma, kur galima pasiekti finansinės atskaitomybės Microsoft Dynamics 365 operacijoms ir kaip naudotis finansinių ataskaitų teikimo galimybės. Ji apima numatytąjį finansines ataskaitas, pateiktas apibūdinimas.

<a name="accessing-financial-reporting"></a>Prieiga prie finansinių ataskaitų
-----------------------------

Galite rasti ir **finansinė atskaitomybė** meniu šiose vietose Dynamics 365 operacijoms:

-   **Didžioji knyga**&gt;**tyrimai ir ataskaitos**
-   **Biudžeto**&gt;**Inquires ir ataskaitų**&gt;**pagrindinio biudžeto sudarymas**
-   **Biudžeto**&gt;**užklausų ir ataskaitų**&gt;**biudžeto planavimas**
-   **Biudžeto**&gt;**užklausų ir ataskaitų**&gt;**biudžeto kontrolės**
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
| Tvarkyti finansinių ataskaitų saugą | Tvarkyti finansinių ataskaitų saugą ir atlikti administravimo užduotis. | FinancialReportsSecurityMaintain |
| Tvarkyti finansines ataskaitas            | Kurti ir tvarkyti finansines ataskaitas.                                  | FinancialReportsMaintainReports  |
| Generuoti finansines ataskaitas            | Generuoti ir atnaujinti finansines ataskaitas.                                 | FinancialReportsGenerateReports  |
| Peržiūrėti finansines ataskaitas                | Peržiūrėti finansines ataskaitas.                                                 | FinancialReportsView             |

### <a name="roles"></a>Vaidmenys

| Teisės žymė                       | Pareiga                                  | Vaidmenys                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Tvarkyti finansinių ataskaitų saugą | Tvarkyti finansinių ataskaitų saugą | Saugos administratorius                                                          |
| Tvarkyti finansines ataskaitas            | Tvarkyti finansines ataskaitas            | Apskaitos vadovas, apskaitos vadovas, finansų kontrolierius, biudžeto vadybininkas |
| Generuoti finansines ataskaitas            | Generuoti finansines ataskaitas            | Generalinis direktorius, finansų direktorius, buhalteris                                                            |
| Peržiūrėti finansines ataskaitas                | Peržiūrėti finansinę veiklą          | Nepriskirtas joks                                                                   |

Pridėjus naudotoją ar pakeitus vaidmenį, naudotojas finansines ataskaitas turėtų galėti pasiekti po kelių minučių. **Pastaba:** sysadmin vaidmens įtraukiama į visus vaidmenis finansinės atskaitomybės.

## <a name="default-reports"></a>Numatytosios ataskaitos
Finansinių ataskaitų modulyje pateikiamos 22 numatytosios finansinės ataskaitos. Kiekviena ataskaita naudoja numatytąjį sąskaita kategorijos Dynamics "365" operacijas. Šias ataskaitas galite naudoti tokias, kokios jo yra, arba kaip pradinį tašką savo finansinių ataskaitų poreikiams tenkinti. Be tradicinių finansinių ataskaitų, pvz., Pajamų išrašo ir Balanso, tarp šių numatytųjų ataskaitų yra ataskaitų, kuriose rodomi galimi kurti skirtingi finansinių ataskaitų tipai. Kiekvienoje ataskaitoje šias lentelės nuorodas į programos "Office Mix" pristatyme apie ataskaitą.

| Numatytoji ataskaita                                                                                         | aprašymas                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Month Rolling Single Column Income Statement – Default](https://mix.office.com/watch/76kc7bm3wnt1) | Viename stulpelyje peržiūrėkite organizacijos pastarųjų 12 mėnesių pelningumą.                                                                                                                                                                                                                                      |
| [12 Month Trend Income Statement – Default](https://mix.office.com/watch/12brmfge5p8r)                 | Peržiūrėkite organizacijos kiekvieno iš pastarųjų 12 mėnesių pelningumą. Šie 12 mėnesių gali apimti daugiau kaip vienus ataskaitinius metus.                                                                                                                                                                                             |
| [Actual vs Budget – Default](https://mix.office.com/watch/fi439lkwr0no)                                | Peržiūrėkite išsamią visų pradinio biudžeto sąskaitų informaciją ir patikslintą biudžetą palyginkite su faktinėmis sumomis, turinčiomis nuokrypį.                                                                                                                                                                          |
| [Audit Details – Default](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje ataskaitų valiuta ir vietos valiuta rodomi debeto ir kredito balansai bei papildoma operacijų informacija, pvz., naudotojo ID, naudotojas, kuris paskutinis modifikavo duomenis, paskutinio modifikavimo data ir žurnalo ID. |
| [Balance List – Default](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje rodomi pradinis bei galutinis likučiai ir dabartinio laikotarpio bei metų iki šios dienos debeto ir kredito balansai bei papildoma operacijų informacija, pvz., kvitas.                                                                    |
| [Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                                   | Peržiūrėti organizacijos metų finansinę padėtį.                                                                                                                                                                                                                                                             |
| [Balance Sheet and Income Statement Side by Side - Default](https://mix.office.com/watch/zkgq0u7visw9) | Vieną greta kito peržiūrėkite organizacijos metų finansinę padėtį ir pelningumą.                                                                                                                                                                                                                              |
| [Cash Flow – Default](https://mix.office.com/watch/jd3go9pz6390)                                       | Gaukite įžvalgų apie grynuosius pinigus, kurie ateina į organizaciją ir iš jos išeina.                                                                                                                                                                                                                                   |
| [Detailed JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Peržiūrėkite visų sąskaitų pradinį balansą ir veiklos informaciją.                                                                                                                                                                                                                                                      |
| [Detailed Trial Balance - Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Peržiūrėkite visų sąskaitų, turinčių debeto bei kredito balansų, balanso informaciją ir jų grynąją reikšmę, taip pat operacijos datą, kvitą ir žurnalo aprašą.                                                                                                                                  |
| [Expenses Three Year Quarterly Trend – Default](https://mix.office.com/watch/gwm4zu7tmtj8)             | Gaukite įžvalgų apie pastarųjų trejų metų 12 ketvirčių išlaidas.                                                                                                                                                                                                                                   |
| [Financial Captions JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Apžvelkite turto balansų ir veiklos, įsipareigojimų, savininko kapitalo, įplaukų, išlaidų, pelno arba nuostolių finansines antraštes.                                                                                                                                                                           |
| [Income Statement – Default](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Peržiūrėkite organizacijos dabartinio laikotarpio ir metų iki šios dienos pelningumą.                                                                                                                                                                                                                                   |
| [Ledger Transaction List – Default](https://mix.office.com/watch/19h9v2rmh48vy)                        | Peržiūrėkite išsamią visų sąskaitų balanso informaciją. Šioje ataskaitoje rodomi debeto ir kredito balansai bei papildoma operacijų informacija, pvz., operacijos data, žurnalo numeris, kvitas, registravimo tipas ir sekimo numeris.                                                                            |
| [Ratios – Default](https://mix.office.com/watch/b08hfc5h92me)                                          | Peržiūrėkite organizacijos metų mokumo, pelningumo ir efektyvumo koeficientus.                                                                                                                                                                                                                           |
| [Rolling 12 Month Expenses – Default](https://mix.office.com/watch/iywod5qmqhz7)                       | Gaukite įžvalgų apie kiekvieno iš pastarųjų 12 mėnesių išlaidas. Šie 12 mėnesių gali apimti daugiau kaip vienus ataskaitinius metus.                                                                                                                                                                                                       |
| [Rolling Quarter Income Statement – Default](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Rodyti organizacijos pelningumo ketvirtį už praėjusius metus ir metai iki datos.                                                                                                                                                                                                                   |
| [Side by Side Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                      | Peržiūrėti organizacijos metų finansinę padėtį. Šioje ataskaitoje vienas šalia kito rodomi turtas ir įsipareigojimai bei akcininko kapitalas.                                                                                                                                                                                |
| [Summary Trial Balance – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Peržiūrėkite visų sąskaitų su pradiniu bei galutiniu balansais balanso informaciją bei debeto ir kredito balansus ir jų grynąjį skirtumą.                                                                                                                                                                  |
| [Summary Trial Balance Year Over Year – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Peržiūrėti visus abonementus, kurie turi pradžios ir pabaigos balansus ir debeto ir kredito likučių bei jų grynasis skirtumas už einamuosius metus ir praėjusius metus informaciją.                                                                                                                           |
| [Weekly Sales and Discounts - Default](https://mix.office.com/watch/112ng0hy5de0j)                     | Gaukite įžvalgų apie kiekvienos mėnesio savaitės pardavimus ir nuolaidas. Šioje ataskaitoje nurodyta bendroji keturių savaičių suma.                                                                                                                                                                                                              |
| [Biudžeto lėšos - numatytasis](https://mix.office.com/watch/15hcpezcbx7tv)                         | Rodyti išsamiai palyginami Patikslintas biudžetas, faktinės išlaidos, biudžetas rezervacijos ir biudžeto lėšas, skirtas visoms sąskaitoms                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Finansinių ataskaitų atidarymas
Kai spustelite **Finansinių ataskaitų** meniu, rodomas įmonės numatytųjų finansinių ataskaitų sąrašas. Tada galite ataskaitą atidaryti arba modifikuoti. Norėdami atidaryti vieną iš numatytųjų ataskaitų, pasirinkite ataskaitos pavadinimą. Pirmą kartą atidarant ataskaitą, ji automatiškai sugeneruojama už praėjusį mėnesį. Pvz., jei atidarysite ataskaitą pirmą kartą rugpjūčio 2016 metais, ataskaitą generuojamas 2016 m. liepos 31 d. Kai ataskaita atidaroma, galite pradėti ją tyrinėti detalizuodami konkrečius duomenis ir keisdami ataskaitos parinktis.

## <a name="creating-and-modifying-financial-reports"></a>Finansinių ataskaitų kūrimas ir modifikavimas
Finansinių ataskaitų sąraše galite kurti naują ataskaitą arba modifikuoti esamą ataskaitą. Jei turite atitinkamas teises, galite sukurti naują finansinę ataskaitą spustelėdami **naujas** Naujintiveiksmų srityje. Ataskaitos dizaino programa atsisiųsti į savo prietaisą. Paleidus ataskaitų konstruktorius tada galite sukurti naują ataskaitą. Kai turite naująją ataskaitą, ji atsiranda finansinių ataskaitų sąraše. Sąraše rodoma tik pranešimų, kad buvo sukurta įmonė, kuri naudojate Dynamics 365 operacijoms. Daugiau informacijos apie procesą, kuriant ir keičiant finansinių ataskaitų Dynamics 365 operacijoms, nuoroda į šiuos [dienoraščio](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) nuo dinamiką, finansinių ataskaitų dienoraščio. **Pastaba:** prie kompiuterio, kuriame atsisiunčiate ataskaitą, dizainerio klientas turi būti įdiegta Microsoft .NET Framework 4.6.2 versija. Ši Microsoft .NET Framework versiją galima atsisiųsti ir įdiegti iš [čia](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Jei naudojate "Chrome", turite įdiegti "ClickOnce" taikomosios pratęsimo norint atsisiųsti ataskaitą dizainerio klientas. Jei dirbate inkognito režimu, įsitikinkite, kad "ClickOnce" taikomosios plėtinys yra įjungtas inkognito režimu. Ataskaitą, kuri atsiranda finansinių ataskaitų sąraše, taip pat galite modifikuoti. Kai pasirinkta sritis aplink ataskaitos pavadinimą, veiksmų srityje spustelėkite **Redaguoti**. Paleidžiama ataskaitų dizaino įrankio programa.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[View financial reports](view-financial-reports.md)

[„Dynamics‟ Finansinių ataskaitų tinklaraštis](http://blogs.msdn.com/b/dynamics_financial_reporting/)


