---
title: PVM apžvalga
description: Šiame straipsnyje pateikiama PVM sistemos apžvalga. Jame paaiškinami PVM nustatymo elementai ir tai, kaip jie veikia kartu.
author: kailiang
ms.date: 10/28/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3261552b60f30afc1a564b50a8269a12f4eeb2b3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871281"
---
# <a name="sales-tax-overview"></a>PVM apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama PVM sistemos apžvalga. Jame paaiškinami PVM nustatymo elementai ir tai, kaip jie veikia kartu.

## <a name="overview"></a>Apžvalga

PVM sistema palaiko įvairių tipų netiesioginius mokesčius, pvz., pridėtinės vertės mokestį (PVM), prekių ir paslaugų mokestį (GST), vienetinius mokesčius ir išskaitomą mokestį. Šie mokesčiai apskaičiuojami ir dokumentuojami vykdant pirkimo ir pardavimo operacijas. Periodiškai jie turi būti deklaruojami ir sumokami mokesčių institucijoms. 

Pateiktoje diagramoje parodyti mokesčių sąrankos objektai ir tai, kaip jie susiję.

[![Diagrama, rodanti mokesčio sąrankos objektų apžvalgą.](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Reikia nurodyti kiekvieno PVM, kurį įmonė turi deklaruoti, kodą. PVM kode saugomi PVM tarifai ir skaičiavimo taisyklės. 

Kiekvieną PVM kodą reikia susieti su PVM sudengimo laikotarpiu. PVM sudengimo laikotarpiais apibrėžiami intervalai, kuriais PVM reikia deklaruoti ir sumokėti PVM institucijai. Kiekvieną PVM sudengimo laikotarpį reikia priskirti PVM institucijai. PVM institucija – tai subjektas, kuriam deklaruojamas ir mokamas PVM. Ji taip pat apibrėžia PVM ataskaitos maketą. PVM institucijos gali būti susijusios su tiekėjų sąskaitomis. Daugiau informacijos žr. [Nustatyti PVM sudengimo laikotarpius](tasks/set-up-sales-tax-settlement-periods.md).

Kiekvieną PVM kodą taip pat reikia susieti su DK registravimo grupe. DK registravimo grupė nurodo pagrindines sąskaitas, į kurias bus registruojamos PVM kodų sumos. 

Taip pat galima apibrėžti pasirinktinius PVM ataskaitų kodus. Juos galima priskirti įvairių tipų apskaičiuotų PVM kodų sumų PVM kodams. Ataskaitoje **PVM mokėjimas pagal kodą** rodomos bendrosios nurodyto PVM sudengimo laikotarpio ir intervalo vieno PVM ataskaitų kodo sumos. 

Kiekviena operacija, kuriai reikia apskaičiuoti ir registruoti PVM, turi turėti PVM grupę ir prekių PVM grupę. PVM grupės yra susijusios su operacijos šalimi (pvz., kliento ar tiekėjo), o prekių PVM grupės yra susijusios su operacijos ištekliumi (pvz., prekių arba įsigijimo kategorijos). Mokesčių grupėse yra mokesčių kodų sąrašas. Mokesčių kodai, esantys tiek operacijos PVM grupėje, tiek prekių PVM grupėje, yra kodai, taikomi tai operacijai. 

Toliau pateikiamoje lentelėje aprašomi mokesčių sąrankos objektai ir seka.

| Nustatymo veikla                                                  | Būtina/pasirinktinai ir aprašymas                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kurti pagrindines sąskaitas.                                           | Reikia. Prieš nustatant PVM funkcijas, turi būti sukurtos pagrindinės sąskaitos, kurias įmonė naudoja mokesčiams mokėti ir įrašyti.                                                                                                                                                                             |
| Nustatykite PVM skirtų DK registravimo grupių.                     | Reikia. DK registravimo grupės apibrėžia pagrindines sąskaitas, skirtas registruoti ir mokėti PVM.   Daugiau informacijos žr. [Didžiosios knygos registravimo grupių nustatymas pardavimo mokesčiui](tasks/set-up-ledger-posting-groups-sales-tax.md).                                                                                 |
| Nustatykite PVM institucijas.                                   | Reikia. PVM institucijos yra subjektai, kuriems turi būti deklaruojamas ir mokamas mokestis.    Daugiau informacijos žr. [Nustatyti PVM rinkėjus](tasks/set-up-sales-tax-authorities.md).                                                                                                                                          |
| Nustatyti PVM sudengimo laikotarpius.                            | Reikia. PVM sudengimo laikotarpiuose yra informacija apie tai, kada ir kaip dažnai reikia deklaruoti ir mokėti PVM. Jie yra susiję su PVM institucija.                                                                                                                                                       |
| Nustatyti PVM ataskaitų kodus.                               | Pasirinktinai. PVM ataskaitų kodus galima priskirti PVM kodams, norint kelių PVM kodų sumas deklaruoti pagal vieną PVM ataskaitų kodą. Daugiau informacijos žr. [Nustatyti PVM ataskaitų kodus](tasks/set-up-sales-tax-reporting-codes.md).                                         |
| Nustatyti PVM kodus.                                         | Reikia. PVM koduose yra kiekvieno PVM tarifai ir skaičiavimo taisyklės. PVM kodai yra susiję su PVM sudengimo laikotarpiu ir DK registravimo grupe. Daugiau informacijos žr. [Nustatyti PVM kodus](tasks/set-up-sales-tax-codes.md).                                |
| Nustatykite PVM grupes.                                        | Reikia. PVM grupėse yra pardavimo kodų, kurie taikomi operacijos šaliai (kliento ar tiekėjo), sąrašas. Vykdant tam tikrą operaciją, PVM kodų sankirta PVM grupėje ir prekių PVM grupėje nustato PVM kodus, taikomus tai operacijai.                  |
| Nustatyti prekių PVM grupes.                                   | Reikia. Prekių PVM grupėse yra pardavimo kodų, kurie taikomi operacijos ištekliui (produkto, paslaugos ir t. t.), sąrašas. Vykdant tam tikrą operaciją, PVM kodų sankirta PVM grupėje ir prekių PVM grupėje nustato PVM kodus, taikomus tai operacijai. Daugiau informacijos žr. [Nustatyti PVM grupes ir prekių PVM grupes](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md). |
| Programos parametrų puslapiuose nustatyti PVM parametrus. | Reikia. Skirtingose srityse, pvz., DK, Gautinų sumų ir Mokėtinų sumų, reikia nustatyti parametrus, kad būtų galima teisingai apskaičiuoti netiesioginius mokesčius. Nors dauguma šių parametrų turi numatytąsias reikšmes, jie turi būti modifikuoti, kad atitiktų kiekvienos įmonės reikalavimus.                                          |

## <a name="sales-tax-on-transactions"></a>Operacijų PVM
Norėdami skaičiuoti PVM, kiekvienoje operacijoje (pardavimo / pirkimo dokumentų eilučių, žurnalų ir t. t.), turite įvesti PVM grupę ir prekių PVM grupę. Numatytosios grupės nurodomos bendruosiuose duomenyse (pvz., kliento, tiekėjo, prekės ir įsigijimo kategorijos), tačiau, jei reikia, grupes galite rankiniu būdu keisti vykdydami operaciją. Abiejose grupėse yra PVM kodų sąrašas, o šių dviejų PVM kodų sąrašų sankirta nustato operacijai taikomų PVM kodų sąrašą. 

Vykdydami kiekvieną operaciją, apskaičiuotąjį PVM galite pasižiūrėti atidare puslapį **PVM operacija**. PVM galite pasižiūrėti dokumento eilutės arba viso dokumento. Tam tikruose dokumentuose (pvz., tiekėjo SF ir bendruosiuose žurnaluose), jei pradiniame dokumente rodomos sumos su nuokrypiais, apskaičiuotąjį PVM galite koreguoti.

## <a name="sales-tax-settlement-and-reporting"></a>PVM sudengimas ir deklaravimas
PVM deklaruoti ir sumokėti mokesčių institucijoms reikia reguliuojamais intervalais (kas mėnesį, kas ketvirtį ir taip toliau). Galite sudengti intervalo mokesčių sąskaitas ir balansus subalansuoti PVM sudengimo sąskaitoje, kaip nurodyta DK registravimo grupėse. Šias funkcijas galite pasiekti puslapyje **Sudengti ir registruoti PVM**. Turite nurodyti PVM sudengimo laikotarpį, už kurį reikia sudengti PVM. 

Sumokėjus PVM, PVM sudengimo sąskaitos balansas turėtų būti subalansuotas pagal banko sąskaitą. Jei PVM institucija, nurodyta PVM sudengimo laikotarpyje, yra susijusi su tiekėjo sąskaita, PVM balansas registruojamas kaip atidaryta tiekėjo SF ir gali būti įtrauktas į reguliarų mokėjimo pasiūlymą.

## <a name="conditional-sales-tax"></a>Sąlyginis PVM
Sąlyginis PVM yra PVM, mokamas proporcingai faktinei sumai, sumokėtai SF. Standartinis PVM, priešingai, yra apskaičiuojamas SF išrašymo metu. Sąlyginis PVM turi būti sumokėtas PVM rinkėjui mokėjimo registravimo metu, bet ne SF registravimo metu. SF išrašymo metu apie operaciją turi būti pranešta PVM knygos ataskaitoje. Tačiau operacija negali būti įtraukta į PVM mokėjimo ataskaitą. 

Jei formoje DK parametrai pasirenkate žymės langelį Sąlyginis PVM, PVM negalima atskaityti, kol neapmokėsite SF. Kai kuriose šalyse / regionuose tai yra teisiškai būtina.

> [!NOTE]
> Pasirinkus žymės langelį Sąlyginis PVM, reikia nustatyti PVM kodus ir PVM grupes bei taip pat sukurti DK registravimo grupes, kad funkcija būtų palaikoma. |

###  <a name="example"></a>Pavyzdys

Sudengiate PVM kas mėnesį. Birželio 15 d. sukuriate kliento SF, kurios vertė 10 000 eurų (PVM pridedamas).
-   PVM yra 25 procentai arba 2 500 eurų.
-   SF reikia apmokėti iki liepos 30 d.

Paprastai turėtumėte sudengti ir sumokėti 2 500 mokesčių rinkėjui, kai SF užregistruojama birželį, nors mokėjimo iš kliento dar negavote. 

Tačiau, jei naudojate sąlyginį PVM, mokesčių rinkėjui sumą sudengiate, kai gaunate mokėjimą iš kliento liepos 30 d.

### <a name="postdated-check"></a>Vėlesnis čekis

Banko sąskaita nebus išvalyta, jei apmokėjimo būdui pasirinksite vėlesnį čekį, kai bus sukurtas apmokėjimas. Kai kuriose šalyse PVM tampa įvykdytu įsipareigojimu, kai bankas patvirtina mokėjimą, o tai reiškia, kad vėlesnis čekis yra sudengtas. Galite įgalinti jį pasirinkdami parinktį **Sukurti sąlyginį mokestį, kai nurašomi vėlesni čekiai**, esančią **Grynųjų pinigų ir banko valdymas > Sąranka > Grynųjų pinigų ir banko valdymo parametrai > Vėlesni čekiai**.

Daugiau informacijos žr. [Nustatyti išskaitomą mokestį](tasks/set-up-withholding-tax.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
