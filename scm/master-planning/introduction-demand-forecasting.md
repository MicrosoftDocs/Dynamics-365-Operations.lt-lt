---
title: "Paklausos prognozavimas apžvalga"
description: "Poreikio prognozės naudojamos siekiant klientų užsakymų nepriklausomą poreikį prognozuoti iš pardavimo užsakymų, o priklausomą poreikį – bet kada atsiejimo metu. Patobulintas paklausos prognozė mažinimo taisyklėse yra idealus sprendimas masės pritaikymas."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Paklausos prognozavimas apžvalga

Poreikio prognozės naudojamos siekiant klientų užsakymų nepriklausomą poreikį prognozuoti iš pardavimo užsakymų, o priklausomą poreikį – bet kada atsiejimo metu. Patobulintas paklausos prognozė mažinimo taisyklėse yra idealus sprendimas masės pritaikymas.

Generuojant pagrindinę prognozę, praeities operacijų suvestinė perduodama „Microsoft Azure“ mašininio mokymo tarnybai, kuri yra laikoma „Azure“. Kadangi šios tarnybos vartotojai bendrai nenaudoja, ją galima lengvai pritaikyti, kad ji atitiktų specialius pramonės poreikius. Dynamics 365 operacijoms galite vizualizuoti prognozę, koreguoti prognozes ir Rodyti pagrindinius veiklos rodiklius (KPI) apie prognozės tikslumas.

## <a name="key-features-of-demand-forecasting"></a>Pagrindinės poreikio prognozės funkcijos
Toliau pateikiamos keletas pagrindinių poreikio prognozės funkcijų.

-   Pagrindinės statistinės prognozės, pagrįstos retrospektyviniais duomenimis, generavimas.
-   Dinaminio prognozės dimensijų rinkinio naudojimas.
-   Prognozės poreikio tendencijų, pasitikėjimo intervalų ir koregavimų vizualizavimas.
-   Pakoreguotos prognozės įgaliojimas naudoti planavimo procesuose.
-   Pašalinių reikšmių šalinimas.
-   Prognozės tikslumo matavimų kūrimas.

## <a name="major-themes-in-demand-forecasting"></a>Pagrindinės poreikio prognozės temos
Poreikio prognozėje taikomos trys pagrindinės temos, nurodytos toliau.

-   **Moduliarumas** – poreikio prognozė yra modulinė ir ją lengva konfigūruoti. Galite įjungti funkciją įjungti ir išjungti pakeisdami konfigūracijos raktas ne **prekybos**&gt;**atsargų prognozė**&gt;**paklausos prognozavimo**.
-   **Pakartotinai naudoti "Microsoft" kamino** – "Microsoft" pradėjo mašinos mokymosi platforma atliko 2015 m. vasarį. Sistemos mokymasis, kuris dabar yra "Microsoft" Cortana "Analytics" numeris, leidžia greitai ir lengvai sukurti prognozinę analizę eksperimentai, pavyzdžiui, poreikio įvertinimo eksperimentus, naudojant algoritmų R ar Python programavimo kalbos ir paprasta vilkimo ir numetimo sąsaja.
    -   Galite atsisiųsti Dynamics 365 operacijų paklausos prognozavimo eksperimentus, pakeisti juos patenkinti jūsų verslo poreikius, kaip Azure žiniatinklio tarnybos ir naudoti jas generuoti paklausos prognozes. Eksperimentai yra prieinami atsisiųsti, jei nusipirkote Dynamics 365 operacijų pasirašymo dėl gamybos planavimo kaip įmonės lygio vartotojų.
    -   Bet kurį šiuo metu galimą poreikio prognozės bandymą galite atsisiųsti iš čia: [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/). Kadangi Dynamics 365 operacijų paklausos prognozavimo eksperimentų automatiškai integruotas su Dynamics 365 operacijoms, Klientai ir partneriai turi dirbti eksperimentų, kad jie atsisiųsti iš integracijos į ["Cortana" "Analytics" Gallery](https://gallery.cortanaanalytics.com/). Todėl eksperimentus iš į ["Cortana" "Analytics" Gallery](https://gallery.cortanaanalytics.com/) nėra taip paprasta naudoti kaip Dynamics 365 operacijų paklausos prognozavimo eksperimentus. Modifikuokite kodą eksperimentų, kad jie naudoja Dynamics 365 operacijų taikomojo programavimo sąsaja (API).
    -   Galite sukurti savo bandymus naudodami „Microsoft Azure“ mašininio mokymo studiją, publikuoti juos kaip „Azure“ tarnybas ir naudoti poreikio prognozėms generuoti.
    -   Jei jums nereikia didelio našumo arba jei jums nereikia apdoroti didelio duomenų kiekio, galite naudoti nemokamą mašininio mokymo pakopą. Rekomenduojame visada pradėti nuo šios pakopos, ypač diegimo ir tikrinimo etapų metu. Jei jums reikia didesnio našumo ir papildomos saugyklos, galite naudoti standartinę mašininio mokymo pakopą. Norint naudoti šią pakopą reikalinga „Azure“ prenumerata ir taikomos papildomos išlaidos. Išsamesnės informacijos apie mašininio mokymo kainodarą žr. <http://aka.ms/machine-learning-price-info>.
-   **Prognozė mažinimo atsiejimo taške** – paklausos prognozavimo dinamikoje 365 operacijų stato į šį funkcionalumą, kuris leidžia numatyti priklausomų ir nepriklausomų paklausą atsiejimo taške.

## <a name="basic-flow-in-demand-forecasting"></a>Pagrindinė poreikio prognozės eiga
Šioje diagramoje pavaizduota pagrindinė poreikio prognozės eiga. 

[![paklausos prognozavimo Įvadas schema](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Paklausos prognozė kartos pradeda Dynamics 365 operacijoms. Sandorio istorinius Dynamics "365" dėl sandorio operacijos duomenų bazės yra surinkta ir užpildo sustojimo lentelės. Šio sustojimo lentelės yra vėliau įtrauktos į mašinos mokymosi paslaugas. Atliekant minimaliai tinkinimas, galite įjungti įvairius duomenų šaltinius ir į sustojimo lentelės. Duomenų šaltiniais gali būti Microsoft Excel failus, kableliais atskirtų reikšmių (CSV) failų ir duomenų iš Microsoft Dynamics AX 2009 ir Microsoft Dynamics AX 2012. Todėl, jūs galite kurti paklausos prognozes, kad mano ankstesnių laikotarpių duomenimis, plinta tarp kelias sistemas. Tačiau bendrieji duomenys, pvz., prekių pavadinimai ir matavimo vienetai, turi būti tokie patys visuose duomenų šaltiniuose.

Jei naudojate Dynamics 365 operacijų paklausos prognozavimo sistemos mokymasis eksperimentus, jie atrodo geriausiai tinka tarp penkių laiko eilučių prognozavimo metodus apskaičiuoti bazinę prognozė. Šių prognozavimo metodų parametrai valdomi Dynamics 365 operacijoms. 

Prognozės, istorinius duomenis ir bet kokius pakeitimus, atliktus ankstesniais iteracijų paklausos prognozes yra tada Dynamics 365 operacijoms. 

Dynamics 365 operacijoms galite vizualizuoti ir keisti pradinio prognozes. Neautomatinius koregavimus reikia įgalioti prieš prognozių planavimą.

## <a name="limitations"></a>Apribojimai
Paklausos prognozavimo Dynamics 365 operacijoms yra įrankis, kuris padeda klientams gamybos pramonės sukurti prognozės procesus. Jame veikia pagrindinė funkcija paklausos prognozavimo sprendimas, yra suprojektuoti taip, kad jį lengvai galima pratęsti. Paklausos prognozavimas gali būti geriausias netinkama klientams pramonės šakose, pvz., mažmeninė, didmeninė prekyba, sandėliavimo, transportavimo ar kitų profesionalių paslaugų.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


