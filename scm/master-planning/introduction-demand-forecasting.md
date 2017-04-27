---
title: "Poreikio prognozės apžvalga"
description: "Poreikio prognozės naudojamos siekiant klientų užsakymų nepriklausomą poreikį prognozuoti iš pardavimo užsakymų, o priklausomą poreikį – bet kada atsiejimo metu. Patobulintos poreikio prognozės mažinimo taisyklės suteikia idealų masinio pritaikymo sprendimą."
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

# <a name="demand-forecasting-overview"></a>Poreikio prognozės apžvalga

[!include[banner](../includes/banner.md)]


Poreikio prognozės naudojamos siekiant klientų užsakymų nepriklausomą poreikį prognozuoti iš pardavimo užsakymų, o priklausomą poreikį – bet kada atsiejimo metu. Patobulintos poreikio prognozės mažinimo taisyklės suteikia idealų masinio pritaikymo sprendimą.

Generuojant pagrindinę prognozę, praeities operacijų suvestinė perduodama „Microsoft Azure“ mašininio mokymo tarnybai, kuri yra laikoma „Azure“. Kadangi šios tarnybos vartotojai bendrai nenaudoja, ją galima lengvai pritaikyti, kad ji atitiktų specialius pramonės poreikius. Galite naudoti „Dynamics 365 for Operations“, norėdami vizualizuoti prognozę, koreguoti prognozę ir peržiūrėti prognozės tikslumo pagrindinius efektyvumo indikatorius (KPI).

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

-   **Moduliarumas** – poreikio prognozė yra modulinė ir ją lengva konfigūruoti. Funkciją galite įjungti ir išjungti, pakeitę konfigūracijos raktą pasirinkdami **Prekyba** &gt; **Atsargų prognozė** &gt; **Poreikio prognozė**.
-   **Pakartotinis „Microsoft“ dėklo naudojimas** – „Microsoft“ pristatė mašininio mokymo platformą 2015 m. vasario mėn. Mašininis mokymas, kuris šiuo metu yra „Microsoft Cortana“ analizės rinkinio dalis, suteikia galimybę greitai ir lengvai kurti prognozavimo analizės bandymus, pvz., poreikio įvertinimo bandymus, naudojant R algoritmus arba „Python“ programavimo kalbas ir paprastą nuvilkimo sąsają.
    -   Galite atsisiųsti „Dynamics 365 for Operations“ poreikio prognozės bandymus, keisti juos, kad jie atitiktų jūsų verslo poreikius, publikuoti kaip „Azure“ tinklo tarnybą ir naudoti poreikio prognozėms generuoti. Bandymus galite atsisiųsti, jei kaip įmonės lygio vartotojas įsigijote gamybos planuotojo „Dynamics 365 for Operations“ prenumeratą.
    -   Bet kurį šiuo metu galimą poreikio prognozės bandymą galite atsisiųsti iš čia: [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/). Kadangi „Dynamics 365 for Operations“ poreikio prognozės bandymai yra automatiškai integruojami su „Dynamics 365 for Operations“, klientai ir partneriai turi tvarkyti iš puslapio [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/) atsisiųstų bandymų integravimą. Todėl bandymus, atsisiųstus iš puslapio [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/), naudoti nėra taip paprasta, kaip „Dynamics 365 for Operations“ poreikio prognozės bandymus. Turite modifikuoti bandymų kodą, kad būtų naudojama „Dynamics 365 for Operations“ taikomojo programavimo sąsaja (API).
    -   Galite sukurti savo bandymus naudodami „Microsoft Azure“ mašininio mokymo studiją, publikuoti juos kaip „Azure“ tarnybas ir naudoti poreikio prognozėms generuoti.
    -   Jei jums nereikia didelio našumo arba jei jums nereikia apdoroti didelio duomenų kiekio, galite naudoti nemokamą mašininio mokymo pakopą. Rekomenduojame visada pradėti nuo šios pakopos, ypač diegimo ir tikrinimo etapų metu. Jei jums reikia didesnio našumo ir papildomos saugyklos, galite naudoti standartinę mašininio mokymo pakopą. Norint naudoti šią pakopą reikalinga „Azure“ prenumerata ir taikomos papildomos išlaidos. Išsamesnės informacijos apie mašininio mokymo kainodarą žr. <http://aka.ms/machine-learning-price-info>.
-   **Prognozės sumažinimas bet kada atsiejimo metu** – „Dynamics 365 for Operations“ poreikio prognozės pagrįstos šia funkcija, kuri suteikia galimybę prognozuoti priklausomą ir nepriklausomą poreikį bet kada atsiejimo metu.

## <a name="basic-flow-in-demand-forecasting"></a>Pagrindinė poreikio prognozės eiga
Šioje diagramoje pavaizduota pagrindinė poreikio prognozės eiga. 

[![įvado į poreikio prognozę diagrama](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Poreikio prognozės generavimas prasideda „Dynamics 365 for Operations“. Retrospektyviniai operacijų duomenys surenkami iš „Dynamics 365 for Operations“ operacijų duomenų bazės ir užpildoma išdėstymo lentelė. Vėliau ši išdėstymo lentelė įtraukiama į mašininio mokymo tarnybą. Atlikdami minimalų tinkinimą, prie išdėstymo lentelės galite prijungti įvairius duomenų šaltinius. Duomenų šaltiniai gali būti „Microsoft Excel“ failai, kableliais atskirtų reikšmių (CSV) failai ir duomenys iš „Microsoft Dynamics AX 2009“ ir „Microsoft Dynamics AX 2012“. Todėl galite generuoti poreikio prognozes, kurios apdoroja praeities duomenis iš kelių sistemų. Tačiau bendrieji duomenys, pvz., prekių pavadinimai ir matavimo vienetai, turi būti tokie patys visuose duomenų šaltiniuose.

Jei naudojate „Dynamics 365 for Operations“ poreikio prognozės mašininio mokymo bandymus, jie nustato geriausią iš penkių laiko serijų prognozavimo metodų pagrindinei prognozei apskaičiuoti. Šių prognozavimo metodų parametrus valdomi „Dynamics 365 for Operations“. 

Tada „Dynamics 365 for Operations“ galima naudoti prognozes, retrospektyvinius duomenis ir bet kokius poreikio prognozių keitimus, atliktus ankstesnių pakartojimų metu. 

„Dynamics 365 for Operations“ galite naudoti pagrindinėms prognozėms vizualizuoti ir modifikuoti. Neautomatinius koregavimus reikia įgalioti prieš prognozių planavimą.

## <a name="limitations"></a>Apribojimai
Poreikio prognozė yra „Dynamics 365 for Operations“ įrankis, kuris klientams gamybos pramonėje padeda kurti prognozavimo procesus. Jis teikia poreikio prognozės sprendimo pagrindinę funkciją ir yra sukurtas taip, kad jį būtų galima lengvai išplėsti. Poreikio prognozė gali būti ne pats tinkamas pasirinkimas klientams tam tikrose pramonės šakose, pvz., mažmeninėje prekyboje, didmeninėje prekyboje, sandėliavime, transportavime arba kitose profesionalių paslaugų srityse.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Poreikio prognozių nustatymas](demand-forecasting-setup.md)

[Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)

[Neautomatiniai pagrindinės prognozės koregavimai](manual-adjustments-baseline-forecast.md)

[Pakoreguotos poreikio prognozės įgaliojimas](authorize-adjusted-forecast.md)

[Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md)

[Skaičiuodami poreikio prognozę iš praeities operacijų duomenų pašalinkite pašalines reikšmes](remove-historical-outliers-calculating-demand-forecast.md)




