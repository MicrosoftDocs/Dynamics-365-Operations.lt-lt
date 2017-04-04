---
title: "PVM apžvalga"
description: "Šiame straipsnyje pateikiama PVM sistemos apžvalga. Jame paaiškinami PVM nustatymo elementai ir tai, kaip jie veikia kartu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 1adee145d705f239e0c663d310234286478fead0
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-overview"></a>PVM apžvalga

Šiame straipsnyje pateikiama PVM sistemos apžvalga. Jame paaiškinami PVM nustatymo elementai ir tai, kaip jie veikia kartu.

<a name="overview"></a>Apžvalga
--------

PVM sistema palaiko įvairių rūšių netiesioginius mokesčius, pvz., PVM, pridėtinės vertės mokestis (PVM), prekių ir paslaugų mokestis (GST), vieneto mokestis ir Išskaitomas mokestis. Šie mokesčiai apskaičiuojami ir dokumentuojami per pirkimo ir pardavimo sandorius. Periodiškai, jie turi būti pranešta ir mokėti mokesčių institucijoms. 

Pateiktoje diagramoje parodyti mokesčių sąrankos objektai ir tai, kaip jie susiję.

[![TaxOverview](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Už kiekvieną apyvartos mokestį, kuris sudaro bendrovės, turi būti apibrėžta PVM kodą. PVM kode saugomi PVM tarifai ir skaičiavimo taisyklės. 

Kiekvieną PVM kodą reikia susieti su PVM sudengimo laikotarpiu. PVM sudengimo laikotarpiais apibrėžiami intervalai, kuriais PVM reikia deklaruoti ir sumokėti PVM institucijai. Kiekvieną PVM sudengimo laikotarpį reikia priskirti PVM institucijai. PVM institucija – tai subjektas, kuriam deklaruojamas ir mokamas PVM. Ji taip pat apibrėžia PVM ataskaitos maketą. PVM institucijos gali būti susijusios su tiekėjų sąskaitomis. 

Kiekvieną PVM kodą taip pat reikia susieti su DK registravimo grupe. DK registravimo grupė nurodo pagrindines sąskaitas, į kurias bus registruojamos PVM kodų sumos. 

Taip pat galima apibrėžti pasirinktinius PVM ataskaitų kodus. Juos galima priskirti įvairių tipų apskaičiuotų PVM kodų sumų PVM kodams. Ataskaitoje **PVM mokėjimas pagal kodą** rodomos bendrosios nurodyto PVM sudengimo laikotarpio ir intervalo vieno mokesčių ataskaitų kodo sumos. 

Kiekviena operacija, kuriai reikia apskaičiuoti ir registruoti PVM, turi turėti PVM grupę ir prekių PVM grupę. PVM grupės yra susijusios su operacijos šalimi (pvz., kliento ar tiekėjo), o prekių PVM grupės yra susijusios su operacijos ištekliumi (pvz., prekių arba įsigijimo kategorijos). Mokesčių grupėse yra mokesčių kodų sąrašas. Mokesčių kodai, esantys tiek operacijos PVM grupėje, tiek prekių PVM grupėje, yra kodai, taikomi tai operacijai. 

Toliau pateikiamoje lentelėje aprašomi mokesčių sąrankos objektai ir seka.

| Nustatymo veikla                                                  | Būtina/pasirinktinai ir aprašymas                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kurti pagrindines sąskaitas.                                           | Reikia. Prieš nustatant PVM funkcijas, turi būti sukurtos pagrindinės sąskaitos, kurias įmonė naudoja mokesčiams mokėti ir įrašyti.                                                                                                                                                                             |
| Nustatykite PVM skirtų DK registravimo grupių.                     | Reikia. DK registravimo grupės apibrėžia pagrindines sąskaitas, skirtas registruoti ir mokėti PVM.                                                                                                                                                                                                                            |
| Nustatykite PVM institucijas.                                   | Reikia. PVM institucijos yra subjektai, kuriems turi būti deklaruojamas ir mokamas mokestis.                                                                                                                                                                                                                                   |
| Nustatyti PVM sudengimo laikotarpius.                            | Reikia. PVM sudengimo laikotarpiuose yra informacija apie tai, kada ir kaip dažnai reikia deklaruoti ir mokėti PVM. Jie yra susiję su PVM institucija.                                                                                                                                                       |
| Nustatyti PVM ataskaitų kodus.                               | Pasirinktinai. PVM ataskaitų kodus galima priskirti PVM kodams, norint kelių PVM kodų sumas deklaruoti pagal vieną PVM ataskaitų kodą.                                                                                                                                                                 |
| Nustatyti PVM kodus.                                         | Reikia. PVM koduose yra kiekvieno PVM tarifai ir skaičiavimo taisyklės. PVM kodai yra susiję su PVM sudengimo laikotarpiu ir DK registravimo grupe.                                                                                                                                        |
| Nustatykite PVM grupes.                                        | Reikia. PVM grupėse yra pardavimo kodų, kurie taikomi operacijos šaliai (kliento ar tiekėjo), sąrašas. Vykdant tam tikrą operaciją, PVM kodų sankirta PVM grupėje ir prekių PVM grupėje nustato PVM kodus, taikomus tai operacijai.                  |
| Nustatyti prekių PVM grupes.                                   | Reikia. Prekių PVM grupėse yra pardavimo kodų, kurie taikomi operacijos ištekliui (produkto, paslaugos ir t. t.), sąrašas. Vykdant tam tikrą operaciją, PVM kodų sankirta PVM grupėje ir prekių PVM grupėje nustato PVM kodus, taikomus tai operacijai. |
| Programos parametrų puslapiuose nustatyti PVM parametrus. | Reikia. Skirtingose srityse, pvz., DK, Gautinų sumų ir Mokėtinų sumų, reikia nustatyti parametrus, kad būtų galima teisingai apskaičiuoti netiesioginius mokesčius. Nors dauguma šių parametrų turi numatytąsias reikšmes, jie turi būti modifikuoti, kad atitiktų kiekvienos įmonės reikalavimus.                                          |

## <a name="sales-tax-on-transactions"></a>Operacijų PVM
Norėdami skaičiuoti PVM, kiekvienoje operacijoje (pardavimo / pirkimo dokumentų eilučių, žurnalų ir t. t.), turite įvesti PVM grupę ir prekių PVM grupę. Numatytosios grupės nurodomos bendruosiuose duomenyse (pvz., kliento, tiekėjo, prekės ir įsigijimo kategorijos), tačiau, jei reikia, grupes galite rankiniu būdu keisti vykdydami operaciją. Abiejose grupėse yra PVM kodų sąrašas, o šių dviejų PVM kodų sąrašų sankirta nustato operacijai taikomų PVM kodų sąrašą. 

Vykdydami kiekvieną operaciją, apskaičiuotąjį PVM galite pasižiūrėti atidare puslapį **PVM operacija**. PVM galite pasižiūrėti dokumento eilutės arba viso dokumento. Tam tikruose dokumentuose (pvz., tiekėjo SF ir bendruosiuose žurnaluose), jei pradiniame dokumente rodomos sumos su nuokrypiais, apskaičiuotąjį PVM galite koreguoti.

## <a name="sales-tax-settlement-and-reporting"></a>PVM sudengimas ir deklaravimas
PVM deklaruoti ir sumokėti mokesčių institucijoms reikia reguliuojamais intervalais (kas mėnesį, kas ketvirtį ir taip toliau). Microsoft Dynamics 365 operacijoms pateikia funkcijas, kurios leidžia atsiskaityti mokesčių sąskaitų intervalas ir kompensuoti likučius į mokesčių atsiskaitymo sąskaitą, kaip nurodyta DK registravimo grupės. Šią funkciją galite pasiekti ir **įsikurti ir registruoti PVM** puslapis. Nurodykite PVM sudengimo laikotarpio PVM turėtų atsiskaityti už. 

Sumokėjus PVM, PVM sudengimo sąskaitos balansas turėtų būti subalansuotas pagal banko sąskaitą. Jei PVM institucija, nurodyta PVM sudengimo laikotarpyje, yra susijusi su tiekėjo sąskaita, PVM balansas registruojamas kaip atidaryta tiekėjo SF ir gali būti įtrauktas į reguliarų mokėjimo pasiūlymą.

## <a name="conditional-sales-tax"></a>Sąlyginis PVM
Sąlyginis PVM yra PVM, kad mokama proporcingai faktinė suma mokama sąskaitoje-faktūroje. Priešingai, standartinis PVM yra skaičiuojamas ne sąskaitų faktūrų išrašymo metu. Sąlyginis PVM turi sumokėti PVM kai mokėjimas yra registruojamas, ne tada, kai SF. Užregistravus SF, sandoris turi būti nurodytas PVM knygos ataskaitą. Tačiau sandoris neturi būti įtrauktos į PVM mokėjimo ataskaitą. 

Pažymėjus žymės langelį Sąlyginis PVM formoje DK parametrai, pardavimo mokestis gali būti išskaitomas tol, kol jūs turite sumokėti sąskaitą-faktūrą. Tai teisinis reikalavimas kai kuriose šalyse/regionuose.

> [!NOTE]
> Kai pažymite žymės langelį Sąlyginis PVM, turite nustatyti PVM kodus ir PVM grupes, ir taip pat kurti DK registravimo grupes, funkcionalumui palaikyti. |

###  <a name="example"></a>Pavyzdys

PVM sudengiate kiekvieną mėnesį. Birželio 15 d., galite sukurti kliento SF 10 000, plius PVM.
-   Pardavimo mokestis yra 25 proc., arba 2500.
-   Sąskaita apmokėjimas yra dėl liepos 30.

Jums paprastai reikės atsiskaityti ir mokėti 2500 mokesčių administratoriui, kai SF yra paskelbtas birželį, net jei jūs negavote apmokėjimo iš kliento. 

Vis dėlto naudojant sąlyginį PVM, galite atsiskaityti su mokesčių administratorius gavę mokėjimą iš kliento liepos 30 d.


