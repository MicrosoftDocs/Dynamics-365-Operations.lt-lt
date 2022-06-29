---
title: Poreikio prognozės apžvalga
description: Poreikio prognozės naudojamos siekiant klientų užsakymų nepriklausomą poreikį prognozuoti iš pardavimo užsakymų, o priklausomą poreikį – bet kada atsiejimo metu. Patobulintos poreikio prognozės mažinimo taisyklės suteikia idealų masinio pritaikymo sprendimą.
author: t-benebo
ms.date: 07/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "72004"
- intro-internal
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1648808667c8bb9487e7a47b87d8e73cf442d82
ms.sourcegitcommit: d98ecbd9457197ec8f8e281f9c2f24dcce7b8269
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2022
ms.locfileid: "8960198"
---
# <a name="demand-forecasting-overview"></a>Poreikio prognozės apžvalga

[!include [banner](../includes/banner.md)]

Poreikio prognozės naudojamos siekiant klientų užsakymų nepriklausomą poreikį prognozuoti iš pardavimo užsakymų, o priklausomą poreikį – bet kada atsiejimo metu. Patobulintos poreikio prognozės mažinimo taisyklės suteikia idealų masinio pritaikymo sprendimą.

Generuojant pagrindinę prognozę, ankstesnių operacijų suvestinė perduodama „Microsoft Azure“ mašininiam mokymui, kuris yra nuomojamas platformoje „Azure“. Kadangi šios tarnybos vartotojai bendrai nenaudoja, ją galima lengvai pritaikyti, kad ji atitiktų specialius pramonės poreikius. „Supply Chain Management“ galite naudoti norėdami vizualizuoti prognozę, ją koreguoti ir peržiūrėti prognozės tikslumo pagrindinius efektyvumo indikatorius (KPI).

> [!NOTE]
> „Microsoft Azure” mašininio mokymo studija (klasikinė) yra reikalinga prognozės generavimui naudojant mašininį mokymą. Nuo 2021 m. gruodžio 1 d. nebegalėsite sukurti naujų „Machine Learning Studio” (klasikinės versijos) išteklių. Tačiau galėsite ir toliau naudotis savo esamais „Machine Learning studio” (klasikinės versijos) ištekliais iki 2024 m. rugpjūčio 31 d. Atnaujintą informaciją rasite [„Azure Machine Learning Studio”](/azure/machine-learning/overview-what-is-machine-learning-studio#ml-studio-classic-vs-azure-machine-learning-studio).
> 
> „Dynamics 365 Supply Chain Management” 10.0.23 ir naujesnės versijos palaiko naująjį „Azure Machine Learning Studio”.

## <a name="key-features-of-demand-forecasting"></a>Pagrindinės poreikio prognozės funkcijos

Toliau pateikiamos keletas pagrindinių poreikio prognozės funkcijų.

- Pagrindinės statistinės prognozės, pagrįstos retrospektyviniais duomenimis, generavimas.
- Dinaminio prognozės dimensijų rinkinio naudojimas.
- Prognozės poreikio tendencijų, pasitikėjimo intervalų ir koregavimų vizualizavimas.
- Pakoreguotos prognozės įgaliojimas naudoti planavimo procesuose.
- Pašalinių reikšmių šalinimas.
- Prognozės tikslumo matavimų kūrimas.

## <a name="major-themes-in-demand-forecasting"></a>Pagrindinės poreikio prognozės temos

Poreikio prognozėje taikomos trys pagrindinės temos, nurodytos toliau.

- **Moduliarumas** – poreikio prognozė yra modulinė ir ją lengva konfigūruoti. Funkciją galite įjungti ir išjungti, pakeitę konfigūracijos raktą pasirinkdami **Prekyba** &gt; **Atsargų prognozė** &gt; **Poreikio prognozė**.
- **Naujas „Microsoft Stack“ panaudojimas** – „Machine Learning“, kuris yra „Microsoft Cortana Analytics Suite“ dalis leidžia jums greitai ir paprastai sukurti nuspėjamus analizės eksperimentus, tokius kaip poreikio apskaičiavimo eksperimentai naudojant algoritmus R ar „Python“ programavimo kalbas ir paprastą tempimo ir paleidimo sąsają.
  - Galite atsisiųsti poreikio prognozavimo bandymus, keisti juos, kad jie atitiktų jūsų verslo poreikius, publikuoti kaip „Azure“ tinklo tarnybą ir naudoti poreikio prognozėms generuoti. Bandymus galite atsisiųsti, jeigu kaip įmonės lygio vartotojas įsigijote gamybos planuotojo „Supply Chain Management“ prenumeratą.
  - Bet kurį šiuo metu galimą poreikio prognozės bandymą galite atsisiųsti iš čia: [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/). Kadangi poreikio prognozės bandymai yra automatiškai integruojami su „Supply Chain Management“, klientai ir partneriai turi tvarkyti iš puslapio [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/) atsisiųstų bandymų integravimą. Todėl bandymus, atsisiųstus iš puslapio [„Cortana“ analizės galerija](https://gallery.cortanaanalytics.com/), naudoti nėra taip paprasta, kaip „Finance and Operations“ poreikio prognozės bandymus. Turite modifikuoti bandymų kodą, kad būtų naudojama „Finance and Operations“ taikomojo programavimo sąsaja (API).
  - Galite sukurti savo bandymus naudodami „Microsoft Azure“ mašininio mokymo studiją (klasikinė), publikuoti juos kaip „Azure“ tarnybas ir naudoti poreikio prognozėms generuoti.
  - Jei jums nereikia didelio našumo arba jei jums nereikia apdoroti didelio duomenų kiekio, galite naudoti nemokamą mašininio mokymo pakopą. Rekomenduojame visada pradėti nuo šios pakopos, ypač diegimo ir tikrinimo etapų metu. Jei jums reikia didesnio našumo ir papildomos saugyklos, galite naudoti standartinę mašininio mokymo pakopą. Norint naudoti šią pakopą reikalinga „Azure“ prenumerata ir taikomos papildomos išlaidos. Informacijos apie mašininio mokymo kainodarą žr. [Mašininio mokymo įrangos kainodara](https://aka.ms/machine-learning-price-info).
- **Prognozės sumažinimas bet kada atsiejimo metu** – poreikio prognozės, pagrįstos šia funkcija, kuri suteikia galimybę prognozuoti priklausomą ir nepriklausomą poreikį bet kada atsiejimo metu.

## <a name="basic-flow-in-demand-forecasting"></a>Pagrindinė poreikio prognozės eiga

Šioje diagramoje pavaizduota pagrindinė poreikio prognozės eiga.

[![įvado į poreikio prognozę diagrama.](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

„Supply Chain Management“ pradedamas poreikio prognozės generavimas. Retrospektyviniai operacijų duomenys surenkami iš „Supply Chain Management“ operacijų duomenų bazės ir užpildoma išdėstymo lentelė. Vėliau ši išdėstymo lentelė įtraukiama į mašininio mokymo tarnybą. Atlikdami minimalų tinkinimą, prie išdėstymo lentelės galite prijungti įvairius duomenų šaltinius. Duomenų šaltiniai gali būti „Microsoft Excel“ failai, kableliais atskirtų reikšmių (CSV) failai ir duomenys iš „Microsoft Dynamics AX 2009“ ir „Microsoft Dynamics AX 2012“. Todėl galite generuoti poreikio prognozes, kurios apdoroja praeities duomenis iš kelių sistemų. Tačiau bendrieji duomenys, pvz., prekių pavadinimai ir matavimo vienetai, turi būti tokie patys visuose duomenų šaltiniuose.

Jei naudojate poreikio prognozės mašininio mokymo bandymus, jie nustato geriausią iš penkių laiko serijų prognozavimo metodų pagrindinei prognozei apskaičiuoti. Šių prognozavimo metodų parametrai valdomi programoje „Supply Chain Management“.

Tada „Supply Chain Management“ galima naudoti prognozes, retrospektyvinius duomenis ir bet kokius poreikio prognozių pakeitimus, atliktus ankstesnių pakartojimų metu.

„Supply Chain Management“ galite naudoti pagrindinėms prognozėms vizualizuoti ir modifikuoti. Neautomatinius koregavimus reikia įgalioti prieš prognozių planavimą.

## <a name="limitations"></a>Apribojimai

Poreikio prognozė yra įrankis, kuris klientams gamybos pramonėje padeda kurti prognozavimo procesus. Jis teikia poreikio prognozės sprendimo pagrindinę funkciją ir yra sukurtas taip, kad jį būtų galima lengvai išplėsti. Poreikio prognozė gali būti netinkama klientams tokiose pramonės šakose kaip prekyba, didmeninė prekyba, sandėliavimas, transportavimas ar kitose profesionaliose paslaugų teikimo šakose.

### <a name="demand-forecast-variant-conversion-limitation"></a>Poreikio prognozės varianto pavertimo apribojimai

Matavimo vienetas (UOM) varianto pavertimui nėra visiškai palaikomas kuriant poreikio planavimą, jei inventorius UOM skiriasi nuo poreikio prognozės UOM.

Prognozės kūrimas (**Inventorius UOM > Poreikio prognozė UOM**) naudoja UOM produkto pavertimą. Istorinių duomenų užkrovos poreikio prognozės kūrimo metu, pavertimo UOM produkto lygis bus visuomet naudojamas paverčiant iš inventoriaus UOM į prognozės poreikį UOM, net jei esama pavertimų nustatytų varianto lygyje.

Pirmoji leidimo prognozės dalis (**Poreikio prognozė UOM > Inventorius UOM**) naudoja UOM pavertimo produktą. Antroji leidimo prognozės dalis (**Inventorius UOM > Pardavimo UOM**) naudoja UOM pavertimo variantą. Kai poreikio prognozės leidimas yra sukuriamas, UOM inventoriaus pavertimas iš poreikio prognozės UOM bus atliktas naudojant produkto lygio UOM pavertimą. Tuo pačiu metu, konvertavimas tarp inventoriaus padalinio ir prekybos UOM atsižvelgs į varianto lygį, nurodytą konvertavimuose.

Atkreipkite dėmesį, kad poreikio UOM prognozė neprivalo turėti jokios konkrečios reikšmės. Ji gali būti nustatyta kaip „Poreikio prognozės padalinys“. Visiems produktams galite nustatyti pavertimą į 1:1 su UOM inventoriumi.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Poreikio prognozavimo nustatymas](demand-forecasting-setup.md)
- [Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)
- [Neautomatiniai pagrindinės prognozės koregavimai](manual-adjustments-baseline-forecast.md)
- [Pakoreguotos prognozės įgaliojimas](authorize-adjusted-forecast.md)
- [Prognozės tikslumo stebėjimas](monitor-forecast-accuracy.md)
- [Pašalinių reikšmių šalinimas iš praeities operacijų duomenų skaičiuojant poreikio prognozę](remove-historical-outliers-calculating-demand-forecast.md)
- [Vaizdo įrašas: poreikio prognozės funkcijos išplėtimas](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [Webi azure: poreikio prognozė naudojant "Azure" mašinos mokymosi seriją](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
