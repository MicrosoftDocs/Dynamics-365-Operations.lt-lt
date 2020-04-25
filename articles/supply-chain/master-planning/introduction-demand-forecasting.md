---
title: Poreikio prognozės apžvalga
description: Poreikio prognozės naudojamos siekiant klientų užsakymų nepriklausomą poreikį prognozuoti iš pardavimo užsakymų, o priklausomą poreikį – bet kada atsiejimo metu. Patobulintos poreikio prognozės mažinimo taisyklės suteikia idealų masinio pritaikymo sprendimą.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: be60bb5c856020d76d185249fddf09493ea1d2ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213888"
---
# <a name="demand-forecasting-overview"></a>Poreikio prognozės apžvalga

[!include [banner](../includes/banner.md)]

Poreikio prognozės naudojamos siekiant klientų užsakymų nepriklausomą poreikį prognozuoti iš pardavimo užsakymų, o priklausomą poreikį – bet kada atsiejimo metu. Patobulintos poreikio prognozės mažinimo taisyklės suteikia idealų masinio pritaikymo sprendimą.

Generuojant pagrindinę prognozę, ankstesnių operacijų suvestinė perduodama „Microsoft Azure“ mašininiam mokymui, kuris yra nuomojamas platformoje „Azure“. Kadangi šios tarnybos vartotojai bendrai nenaudoja, ją galima lengvai pritaikyti, kad ji atitiktų specialius pramonės poreikius. „Supply Chain Management“ galite naudoti norėdami vizualizuoti prognozę, ją koreguoti ir peržiūrėti prognozės tikslumo pagrindinius efektyvumo indikatorius (KPI).

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
    -   Galite atsisiųsti poreikio prognozavimo bandymus, keisti juos, kad jie atitiktų jūsų verslo poreikius, publikuoti kaip „Azure“ tinklo tarnybą ir naudoti poreikio prognozėms generuoti. Bandymus galite atsisiųsti, jei kaip įmonės lygio vartotojas įsigijote gamybos planuotojo „Supply Chain Management“ prenumeratą.
    -   Bet kurį šiuo metu galimą poreikio prognozės bandymą galite atsisiųsti iš čia: [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/). Kadangi poreikio prognozės bandymai yra automatiškai integruojami su „Supply Chain Management“, klientai ir partneriai turi tvarkyti iš puslapio [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/) atsisiųstų bandymų integravimą. Todėl [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/) bandymus nėra taip lengva naudoti, kaip „Finance and Operations“ poreikio prognozavimo bandymus. Reikia modifikuoti bandymų kodą, kad jie naudotų „Finance and Operations“ taikomojo programavimo sąsają (angl. API).
    -   Galite sukurti savo bandymus naudodami „Microsoft Azure“ mašininio mokymo studiją (klasikinė), publikuoti juos kaip „Azure“ tarnybas ir naudoti poreikio prognozėms generuoti.
    -   Jei jums nereikia didelio našumo arba jei jums nereikia apdoroti didelio duomenų kiekio, galite naudoti nemokamą mašininio mokymo pakopą. Rekomenduojame visada pradėti nuo šios pakopos, ypač diegimo ir tikrinimo etapų metu. Jei jums reikia didesnio našumo ir papildomos saugyklos, galite naudoti standartinę mašininio mokymo pakopą. Norint naudoti šią pakopą reikalinga „Azure“ prenumerata ir taikomos papildomos išlaidos. Informacijos apie mašininio mokymo kainodarą žr. [Mašininio mokymo įrangos kainodara](https://aka.ms/machine-learning-price-info).
-   **Prognozės sumažinimas bet kada atsiejimo metu** – poreikio prognozės, pagrįstos šia funkcija, kuri suteikia galimybę prognozuoti priklausomą ir nepriklausomą poreikį bet kada atsiejimo metu.

## <a name="basic-flow-in-demand-forecasting"></a>Pagrindinė poreikio prognozės eiga
Šioje diagramoje pavaizduota pagrindinė poreikio prognozės eiga. 

[![įvado į poreikio prognozę diagrama](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

„Supply Chain Management“ pradedamas poreikio prognozės generavimas. Retrospektyviniai operacijų duomenys surenkami iš „Supply Chain Management“ operacijų duomenų bazės ir užpildoma išdėstymo lentelė. Vėliau ši išdėstymo lentelė įtraukiama į mašininio mokymo tarnybą. Atlikdami minimalų tinkinimą, prie išdėstymo lentelės galite prijungti įvairius duomenų šaltinius. Duomenų šaltiniai gali būti „Microsoft Excel“ failai, kableliais atskirtų reikšmių (CSV) failai ir duomenys iš „Microsoft Dynamics AX 2009“ ir „Microsoft Dynamics AX 2012“. Todėl galite generuoti poreikio prognozes, kurios apdoroja praeities duomenis iš kelių sistemų. Tačiau bendrieji duomenys, pvz., prekių pavadinimai ir matavimo vienetai, turi būti tokie patys visuose duomenų šaltiniuose.

Jei naudojate poreikio prognozės mašininio mokymo bandymus, jie nustato geriausią iš penkių laiko serijų prognozavimo metodų pagrindinei prognozei apskaičiuoti. Šių prognozavimo metodų parametrai valdomi programoje „Supply Chain Management“. 

Tada „Supply Chain Management“ galima naudoti prognozes, retrospektyvinius duomenis ir bet kokius poreikio prognozių pakeitimus, atliktus ankstesnių pakartojimų metu. 

„Supply Chain Management“ galite naudoti pagrindinėms prognozėms vizualizuoti ir modifikuoti. Neautomatinius koregavimus reikia įgalioti prieš prognozių planavimą.

## <a name="limitations"></a>Apribojimai
Poreikio prognozė yra įrankis, kuris klientams gamybos pramonėje padeda kurti prognozavimo procesus. Jis teikia poreikio prognozės sprendimo pagrindinę funkciją ir yra sukurtas taip, kad jį būtų galima lengvai išplėsti. Poreiko prognozė gali būti netinkama klientams tokiose pramonės šakose kaip prekyba, didmeninė prekyba, sandėliavimas, transportavimas ar kitose profesionaliose paslaugų teikimo šakose.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Poreikio prognozavimo nustatymas](demand-forecasting-setup.md)

[Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)

[Neautomatiniai pagrindinės prognozės koregavimai](manual-adjustments-baseline-forecast.md)

[Pakoreguotos prognozės įgaliojimas](authorize-adjusted-forecast.md)

[Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md)

[Pašalinių reikšmių šalinimas iš praeities operacijų duomenų skaičiuojant poreikio prognozę](remove-historical-outliers-calculating-demand-forecast.md)

[Poreikio prognozių funkcijų išplėtimas](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)



